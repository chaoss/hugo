---
title: What we Learned from the CHAOSS Data Science Hackathon
author:
  - Dawn Foster
type: post
date: 2025-07-17T20:05:21+00:00
url: /what-we-learned-from-the-chaoss-data-science-hackathon/
featured_image: /wp-content/uploads/2025/07/leif-christoph-gottwald-iM8dxccK1sY-unsplash-scaled.jpg
ppma_authors_name:
  - Dawn Foster
nectar_blog_post_view_count:
  - 983
categories:
  - Blog Post
tags:
  - data science
  - hackathon

---
\[vc\_row type=&#8221;in\_container&#8221; full\_screen\_row\_position=&#8221;middle&#8221; column\_margin=&#8221;default&#8221; column\_direction=&#8221;default&#8221; column\_direction\_tablet=&#8221;default&#8221; column\_direction\_phone=&#8221;default&#8221; scene\_position=&#8221;center&#8221; text\_color=&#8221;dark&#8221; text\_align=&#8221;left&#8221; row\_border\_radius=&#8221;none&#8221; row\_border\_radius\_applies=&#8221;bg&#8221; overlay\_strength=&#8221;0.3&#8243; gradient\_direction=&#8221;left\_to\_right&#8221; shape\_divider\_position=&#8221;bottom&#8221; bg\_image\_animation=&#8221;none&#8221;\]\[vc\_column column\_padding=&#8221;no-extra-padding&#8221; column\_padding\_tablet=&#8221;inherit&#8221; column\_padding\_phone=&#8221;inherit&#8221; column\_padding\_position=&#8221;all&#8221; background\_color\_opacity=&#8221;1&#8243; background\_hover\_color\_opacity=&#8221;1&#8243; column\_shadow=&#8221;none&#8221; column\_border\_radius=&#8221;none&#8221; column\_link\_target=&#8221;\_self&#8221; gradient\_direction=&#8221;left\_to\_right&#8221; overlay\_strength=&#8221;0.3&#8243; width=&#8221;1/1&#8243; tablet\_width\_inherit=&#8221;default&#8221; tablet\_text\_alignment=&#8221;default&#8221; phone\_text\_alignment=&#8221;default&#8221; column\_border\_width=&#8221;none&#8221; column\_border\_style=&#8221;solid&#8221; bg\_image\_animation=&#8221;none&#8221;\][vc\_column\_text]This blog post was co-authored by Chan Voong, Sal Kimmich, Nandana Krishnan, and Ishan Juneja</p> 

We held our first ever [CHAOSS Data Science Hackathon][1] in Denver co-located with the Linux Foundation’s [Open Source Summit][2] and [CHAOSScon NA][3]. Some first time hackathon participants had a really good time! We felt like it was successful overall, and we hope some of the participants will stick around and continue to participate in the [CHAOSS Data Science Working Group][4].

During the hackathon, we focused on 3 ongoing CHAOSS Data Science Working Group projects: [Relicensing and Forks][5], [Archival of Open Source Projects][6], and [Projects Moving to Foundations][7], and here’s what we accomplished for each of these projects.

## [Relicensing and Forks][5] {.wp-block-heading}

Analyzing PR data before and after a relicense/fork event helps us understand open source project and community behavior. For the hackathon, we took inspiration from Dawn’s code, which looked at commits by people and organizations. To build on the case study, we focused on pull requests and visualized how the number of PRs changed before and after a relicense or fork.

This group was led by Chan Voong and Cali Dolfi and consisted of CU Denver’s  Department of Mathematical and Statistical Sciences students and faculty. The group went in a slightly different direction to explore projects that they were interested in, instead of the projects we expected them to look at, but that’s great! Some projects important to them included Bayesian-Inference, Stan, and TensorFlow, and the team’s primary project that they maintain is [<T>LAPACK][8].

After visualizing those project PRs in a Jupyter Notebook, we checked out [8knot][9], which led to interest in submitting these projects to be added to 8knot for visualizations.

There was great discussion around other metrics such as lottery factor and the possible repercussions if the projects they cared about were to be relicensed to a non-OSI&nbsp; license. Learn more about the [Relicensing and Forks][5] project and how to get involved.

## [Archival of Open Source Projects][6] {.wp-block-heading}

The archive project was focused on data cleaning and classification, since data scientists spend a lot of time doing these kinds of manual tasks that are necessary for ensuring data accuracy. The advantage was that anyone could help out with this project regardless of their skillsets. For this project, we categorized popular open source projects that had been archived on GitHub with a primary reason that the project had been archived.

We categorized 45 out of 729 projects as part of the hackathon, and here are the categories for those 45 projects.

<ul class="wp-block-list">
  </p> 
  
  <li>
    Corporate 3
  </li>
  <li>
    Inactive 13
  </li>
  <li>
    Moved 7
  </li>
  <li>
    Personal 4
  </li>
  <li>
    Technology 18
  </li>
  <li>
    Unevaluated 684
  </li>
  <li>
    Grand Total 729
  </li>
  <p>
    </ul> 
    
    <p>
      While we classified projects into a single, primary category, we also had some interesting discussions about how and why projects are archived and how the reasoning for archival can be complex. For each project that we classified, we added notes about how we came to our decision and any other categories that might have influenced the decision.
    </p>
    
    <p>
      Learn more about the <a href="https://github.com/chaoss/wg-data-science/tree/main/dataset/archive#hackathon-project-details">Archival project</a> and how to get involved.
    </p>
    
    <h2 class="wp-block-heading">
      <a href="https://colab.research.google.com/drive/1AebzquGmtsQ6c1JtC4Koj82lHQ39l-OD?usp=sharing">Projects Moving to Foundations</a>
    </h2>
    
    <p>
      This group explored the question, “How can we better understand the health of open source projects across different ecosystems?” Using public datasets from Apache, CNCF, and Eclipse, several developers: Sal Kimmich, Ejiro Oghenekome, Nandana Krishnan, and Ishan Juneja &#8211; transformed raw project metadata into visual insights. Their work revealed how lifecycle patterns, language choices, and infrastructure gaps impact the sustainability of open source.
    </p>
    
    <p>
      <strong>Which Projects Graduate—and Which Get Stuck?</strong> One of the central findings was the creation of a unified status timeline (Incubated → Graduated → Retired) to track project lifecycles across Apache and CNCF. By merging public metadata from foundation websites and CSV datasets, it became possible to identify projects that had stalled or succeeded in reaching maturity. We had a few key insights:
    </p>
    
    <ul class="wp-block-list">
      </p> 
      
      <li>
        Projects written in Go and Python showed significantly higher graduation rates.
      </li>
      <li>
        Projects built with Java were more likely to be retired or linger in long-term incubation.
      </li>
      <li>
        Some Apache projects had been in incubation for over a decade without graduating.
      </li>
      <p>
        </ul> 
        
        <p>
          <strong>What Can Metadata Tell Us About a Project’s Health?</strong> Another analysis looked at the quality and structure of available metadata across foundation datasets. Specifically, the distribution of path types and status fields from podling histories and CNCF websites was explored to reveal inconsistencies. Findings included:
        </p>
        
        <ul class="wp-block-list">
          </p> 
          
          <li>
            Overrepresentation of certain paths like sandbox, with minimal detail on contributor activity or oversight.
          </li>
          <li>
            Incomplete lifecycle data in projects still marked as “current” or “incubating.”
          </li>
          <li>
            Descriptive gaps that could obscure the true state of a project’s community or release status.
          </li>
          <p>
            </ul> 
            
            <p>
              <strong>Are Contributors Visible—and Is Anyone Listening?</strong> Contributor and communication data were analyzed for Eclipse and CNCF projects. This revealed a startling insight: many active projects are flying blind when it comes to external visibility. The team found that:
            </p>
            
            <ul class="wp-block-list">
              </p> 
              
              <li>
                A significant percentage of projects lacked a public-facing blog or news source.
              </li>
              <li>
                Many projects did not offer a Slack, Gitter, or any other form of community channel.
              </li>
              <li>
                Contributor and committer data was sparse, inconsistent, or missing altogether.
              </li>
              <p>
                </ul> 
                
                <p>
                  There is still much work left to do, but you can read more about this <a href="https://github.com/chaoss/wg-data-science/issues/138">group’s results from the hackathon</a> and how to get involved.
                </p>
                
                <h2 class="wp-block-heading">
                  Learn more
                </h2>
                
                <p>
                  All of these are ongoing projects that people can get involved with by joining the <a href="https://github.com/chaoss/wg-data-science">CHAOSS Data Science WG</a>! You can learn more about what we’ve been up to by reading our <a href="{{ baseURL }}chaoss-data-science-working-group-new-guides-research-and-more/">latest update from June</a> on the CHAOSS blog.
                </p>
                
                <p>
                  Photo by <a href="https://unsplash.com/@project2204?utm_content=creditCopyText&utm_medium=referral&utm_source=unsplash">Leif Christoph Gottwald</a> on <a href="https://unsplash.com/photos/a-bunch-of-television-screens-hanging-from-the-ceiling-iM8dxccK1sY?utm_content=creditCopyText&utm_medium=referral&utm_source=unsplash">Unsplash</a>
                </p> [/vc_column_text][/vc_column][/vc_row]

 [1]: {{ baseURL }}chaoss-data-science-hackathon-2025/
 [2]: https://ossna2025.sched.com/
 [3]: {{ baseURL }}chaosscon-2025-na/
 [4]: {{ baseURL }}chaoss-data-science-working-group-new-guides-research-and-more/
 [5]: https://github.com/chaoss/wg-data-science/tree/main/dataset/license-changes/fork-case-study#hackathon-project-details
 [6]: https://github.com/chaoss/wg-data-science/tree/main/dataset/archive#hackathon-project-details
 [7]: https://colab.research.google.com/drive/1AebzquGmtsQ6c1JtC4Koj82lHQ39l-OD?usp=sharing
 [8]: https://github.com/tlapack/
 [9]: https://eightknot.osci.io/