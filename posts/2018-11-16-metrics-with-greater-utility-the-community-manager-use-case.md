---
title: 'Metrics With Greater Utility: The Community Manager Use Case'
author:
  - CHAOSS Community
type: post
date: 2018-11-16T17:04:31+00:00
excerpt: Community managers take a variety of perspectives, depending on where their communities are in the lifecycle of growth, maturity, and decline. This is an evolving report of what we are learning from community managers, some of whom we are working with on live experiments with a CHAOSS project prototyping software tool called Augur (http://www.github.com/CHAOSS/augur). At this point, we are paying particular focus to how community managers consume metrics and how the presentation of open source software health and sustainability metrics could make them more and in some cases less useful for doing their jobs.
url: /metrics-with-greater-utility-the-community-manager-use-case/
nectar_blog_post_view_count:
  - 3521
ppma_authors_name:
  - CHAOSS Community
categories:
  - Blog Post
tags:
  - Augur
  - Community Manager
  - Sean Goggins
  - Use Case

---
\[vc\_row type=&#8221;in\_container&#8221; full\_screen\_row\_position=&#8221;middle&#8221; bg\_color=&#8221;#ffffff&#8221; scene\_position=&#8221;center&#8221; text\_color=&#8221;dark&#8221; text\_align=&#8221;left&#8221; overlay\_strength=&#8221;0.3&#8243; shape\_divider\_position=&#8221;bottom&#8221; shape\_type=&#8221;&#8221;\]\[vc\_column column\_padding=&#8221;padding-3-percent&#8221; column\_padding\_position=&#8221;all&#8221; background\_color\_opacity=&#8221;1&#8243; background\_hover\_color\_opacity=&#8221;1&#8243; column\_shadow=&#8221;none&#8221; column\_border\_radius=&#8221;none&#8221; width=&#8221;1/1&#8243; tablet\_text\_alignment=&#8221;default&#8221; phone\_text\_alignment=&#8221;default&#8221; column\_border\_width=&#8221;none&#8221; column\_border\_style=&#8221;solid&#8221;\][vc\_column_text]**By Sean Goggins **

# Introduction

Community managers take a variety of perspectives, depending on where their communities are in the lifecycle of growth, maturity, and decline. This is an evolving report of what we are learning from community managers, some of whom we are working with on live experiments with a CHAOSS project prototyping software tool called Augur (<http://www.github.com/CHAOSS/augur>). At this point, we are paying particular focus to how community managers consume metrics and how the presentation of open source software health and sustainability metrics could make them more and in some cases less useful for doing their jobs.

Right now, based on Augur prototypes and follow up discussions so far, we have the following observations that will inform our work both the &#8220;Growth Maturity and Decline&#8221; working group and in Augur Development. Here are a few things we have learned from prototyping Augur with community managers. These features in Augur are particularly valued:

  1. Allowing comparisons with projects within a defined universe of of projects is essential
  2. Allow community managers to add and remove repositories that they monitor from their repertories periodically
  3. Downloadable graphics
  4. Downloadable data (.csv or .json)
  5. Availability of a &#8220;Metrics API&#8221;, limiting the amount of software infrastructure the community manager needs to maintain for themselves. This is more valued by program managers overseeing larger portfolios right now, but we think it has potential to grow as awareness of the relatively light weight of this approach becomes more apparent. By apparent, we really mean &#8220;easy to use and understand&#8221;; right now it is easy for a programmer, but less so for a community manager without this background or current interest.

# Date Summarized Comparison Metrics

With these advantages in mind, making the most of this opportunity to help community managers with useful metrics is going to include the availability of _date summarized comparison metrics_. These types of metrics have two &#8220;filters&#8221; or &#8220;parameters&#8221; fed into them that are more abstractly defined in the Growth, Maturity, and Decline metrics on the CHAOSS project.

  1. Given a pool of repositories of interest for a community manager, rank them in ascending or descending order by a metric
  2. Over a specified time period or
  3. Over a specified periodicity (e.g., month) for a length of time (e.g., year).

For example, one open source program officer we talked with is interested in the following set of _date summarized comparison metrics_. Given a pool of repositories of interest to the program officer (dozens to hundreds of repositories):

  1. What ten repositories have the most commits this year (straight commits, and lines of code)?
  2. How many new projects were launched this year?
  3. What are the top ten new repositories in terms of commits this year (straight commits, and lines of code)?
  4. How many commits and lines of code were contributed by outside contributors this calendar year? Organizationally sponsored contributors?
  5. What organizations are the top five external contributors of commits, comments, and merges?
  6. What are the total number of repository watchers we have across all of our projects?
  7. Which repositories have the most stars? Of the ones new this year? Of all the projects? Which projects have the most new stars this year?

# Open Ended Community Manager Questions to Support with Metrics

There are other, more open ended questions that may be useful to open source community managers:

  1. Is a repository active? 
      1. Visual differentiation that examines issue and commit data
      2. Activity in the past 30 days
      3. Across all repositories, present the 50th percentile as a baseline and show repositories above and below that line
  2. Should we archive this repository? 
      1. Enable an input from the manager after reviewing statistics
      2. Activity level, inactivity level and dependencies
      3. Mean/Median/Mode histogram for commits/repo
  3. Should we feature this repository in our top 10? (Probably a subjective decision based on some kind of _composite scoring system_ that is likely specific to the needs of every community manager or program office.)
  4. Who are our top authors? (Some kind of aggregated contribution ranking by time period [year, month, week, day?]. _nominally, I have a concern about these kinds of metrics being &#8220;gameable&#8221;, but if they are not visible to contributors themselves, there is less &#8220;gaming&#8221; opportunity._)
  5. What are our top repositories? (Probably a subjective decision based on some kind of _composite scoring system_ that is likely specific to the needs of every community manager or program office.)
  6. Most active repositories by time period [year, month, week?]. Activity to be revealed through a mix of retention and maintainer activity primarily focusing on the latter. Number of issues and commits. Also the frequency of pull requests and the number of closed issues.
  7. Least active repositories by time period [Week? Month? Year?]. _Bottom of scores calculated, as above._
  8. Who is our most active contributor (Some kind of aggregated contribution ranking by time period [year, month, week, day?]. _nominally, I have a concern about these kinds of metrics being &#8220;gameable&#8221;, but if they are not visible to contributors themselves, there is less &#8220;gaming&#8221; opportunity._)
  9. What new contributors submitted their first new patches/issues this week? (_Visualization Note:_ New contributors can be colored in visualizations and then additionally a graph can be made for number of new contributors)
 10. Which contributors became inactive? (Will need a mechanism for setting &#8220;inactive&#8221; thresholds.)
 11. Baseline level for the &#8220;average&#8221; repository in an organization and for each, individual organization repository.
 12. What projects outside of a community manager&#8217;s general view (GitHub organization or other boundary) do my repositories depend on or do my contributors also significantly contribute to?
 13. Build a summary report in 140 characters or less. For example, &#8220;Your total commits in this time period [month, week?] across the organization increased 12% over the last period. Your most active repositories remained the same. You have 8 new contributors, which is 1 below your mean for the past year. For more information, click here.&#8221;
 14. Once a metrics baseline is established, what can be done to move them? [^1]
 15. Are there optimal measures for some metrics? 
      1. Pull request size?
      2. Ratio of maintainers to contributors?
      3. New contributor to consistent contributor ratio?
      4. New contributor to maintainer ratio?

# Augur Specific Design Change Recommendations

Next is a list of Augur specific design changes suggested thus far, based on conversations with community managers.

  1. Showing all of the projects in a GitHub organization in a dashboard by default is generally useful.
  2. Make the lines more clear in the charts, especially when there are multiple lines in comparison
  3. How to zoom in and out is not intuitive. In the case of Google Finance, for example, a default, subset period was displayed when they used the &#8220;below the line mirrored line&#8221; interface this is modeled after. That old model makes it fairly clear that the ability to adjust the range of dates is what that box below the line in google finance _is for_. Alternately, Google&#8217;s more updated way of representing time, providing users choices, and showing comparisons may be even more useful and engaging. In general, its important that the time zooming is more clear. <div style="width: 745px" class="wp-caption aligncenter">
      <a href="https://github.com/chaoss/website/blob/master/Community/News/images/post5-1.jpg" target="_blank" rel="noopener noreferrer"><img loading="lazy" decoding="async" src="https://github.com/chaoss/website/raw/master/Community/News/images/post5-1.jpg" alt="In one view, Google lets you see a 1 year window of a stock's performance." width="735" height="723" /></a></p> 
      
      <p class="wp-caption-text">
        <strong>Figure 1: In one view, Google lets you see a 1 year window of a stock&#8217;s performance.</strong>
      </p>
    </div>
    
    &nbsp;
    
    <div style="width: 712px" class="wp-caption aligncenter">
      <a href="https://github.com/chaoss/website/blob/master/Community/News/images/post5-2.jpg" target="_blank" rel="noopener noreferrer"><img loading="lazy" decoding="async" src="https://github.com/chaoss/website/raw/master/Community/News/images/post5-2.jpg" alt="In another view, you can choose a 3 month period. Comparing the two time periods also draws out the trend with red or green colors, depending on whether or not the index, in this case a stock's price, has increased or decreased overall during the selected time period." width="702" height="700" /></a></p> 
      
      <p class="wp-caption-text">
        <strong>Figure 2: In another view, you can choose a 3 month period. Comparing the two time periods also draws out the trend with red or green colors, depending on whether or not the index, in this case a stock&#8217;s price, has increased or decreased overall during the selected time period.</strong>
      </p>
    </div>
    
    &nbsp;
    
    <div style="width: 544px" class="wp-caption aligncenter">
      <a href="https://github.com/chaoss/website/blob/master/Community/News/images/post5-3.jpg" target="_blank" rel="noopener noreferrer"><img loading="lazy" decoding="async" src="https://github.com/chaoss/website/raw/master/Community/News/images/post5-3.jpg" alt="Comparisons are similarly interesting in Google's finance interface. You can simply add a number of stocks in much the same way our users want to add a number of different repositories." width="534" height="854" /></a></p> 
      
      <p class="wp-caption-text">
        <strong>Figure 3: Comparisons are similarly interesting in Google&#8217;s finance interface. You can simply add a number of stocks in much the same way our users want to add a number of different repositories</strong>
      </p>
    </div>

  4. For the projects a community manager chooses to follow, go ahead and give them comparison check-boxes at the top of the page. I think from a design point of view, we should limit comparisons as discussed, to 7 or 8, simply due to the limits in human visual perception.
  5. The ability to adjust the viewing windows to a month summary level is desired.
  6. Right now, Augur does not make it clear that metrics are, by default, aggregated by week.
  7. New contributor response time. When a new contributor joins a project, what is the response time for their contribution?
  8. A graph \*\*comparing\*\* commits and commit comments on x and y axes \*\*between projects\*\* is desired. Same with Issue and Issue comments.
  9. In general, the last two years of data gets the most use. We should focus our default display on this range.

# Data Source Trust Issues

  1. Greater transparency of metrics data origins will be helpful for understanding discrepancies between current understanding and what metrics show. 
      1. We should include some detailed notes from Brian Warner about how Facade is counting lines of code, and possibly some instrumentation to enable those counts to be altered by user provided parameters.
      2. Outside contributor organization Data. One community manager reported that their lines of code by organization data seems to look wrong. I did explain that these are mapped from a list of companies and emails we put together, and getting this right is something community managers will need some kind of mapping tool to do. GitDM is a tool that people sometimes use to create these maps, and Augur does follow a derivative of that work. It is probably the case that maintaining these affiliation lists is something that needs to be made easier for community managers, especially in cases where the number of organizations contributing to a project is diverse (there is a substantial range among community managers we spoke with. Some are managing complex ecosystems involving mostly outside contributors. Most are in the middle. And some of contributor lists highly skewed toward their own organization.)
  2. GHTorrent data, while excellent for prototyping, faces some limitations under the scrutiny of community managers. For example, when using the cloned repositories, and then going back to \*issues\*, the issues data in GHTorrent does not &#8220;look right&#8221;. I think the graph API might offers some possibilities for us to store issue statistics we pull directly from GitHub and update periodically as an alternative to GHTorrent.
  3. When issues are moved from an older system, like Gerrit, into GitHub issues, in general, the statistics for the converted issues are dodgy, even through the GitHub API. We are likely to encounter this, and at some point may want to include Gerrit data in a common data structure with issues from GitHub and other sources.

# New Metrics Suggested

  1. Add metric &#8220;number of clones&#8221;
  2. &#8220;Unique visitors&#8221; to a repository is a data point available from the GitHub API which is interesting.
  3. Include a metric that is a comparison of the ratio of new committers and total committers in a time period. Or, perhaps simply those two metrics in alignment. Seeing the number of new committers in a set of repositories can be a useful indication of momentum in one direction or another; though I hasten to add that this is not canonically the case.
  4. Some kind of representation of the ratio between commits and lines of code per commit
  5. Test coverage within a repository is something to consider measuring for safety critical systems software.
  6. Identifying the relationship between the DCO (Developer Certificate of Origin) and the CLA (Contributor License Agreement).
  7. There is a tension between risk and value that, as our metrics develop in those areas, we are well advised to keep in mind.
  8. The work that Matt Snell and Matt Germonprez at the University of Nebraska-Omaha are starting related to risk metrics is of great interest. Getting these metrics into Augur is something we should plan for as soon as reasonably possible.

# Design Possibilities

## Augur

For Augur, I think the interface changes that enable comparisons and adjust the level of self apparent ways to compress or expand the time, as per the Google examples, are at the top of the list of things that will make Augur more useful for community managers. Feedback on these notes will be helpful. I think the new committers to committers ratio is important, as well as enabling comparisons across projects in the bubble graphs as well. Transparency of data sources and limitations of data sources for both the API and the front end, which are above average but not complete, are important.

## Growth Maturity and Decline Working Group

Many of the metrics of interest to community managers fall under the &#8220;Growth Maturity and Decline&#8221; working group. From a design perspective it appears that, possibly, the way that metrics are expressed and consumed by these stakeholders in their individual derivatives of the _community manager use case_ is quite far removed from the detailed definition work occurring around specific metrics. Discussion around an example implementation like Augur is helping draw out some of this more &#8220;zoomed out&#8221; feedback. The design of system interfaces frequently includes the need to navigate between granular details and the overall user experience [@zemel\_what\_2007; @barab\_our\_2007]. This is less of a focus in the development of software engineering metrics, though recent research is beginning to illustrate the criticality of visual design for interpreting analytic information [@gonzalez-torres\_knowledge\_2016].

# References

  * Barab, S, T Dodge, MK Thomas, C Jackson, and H Tuzun. 2007. Our designs and the social agendas they carry. Journal of the Learning Sciences 16 (2): 263-305.
  * Gonzalez-Torres, Antonio, Francisco J. Garcia-Penalvo, Roberto Theron- Sanchez, and Ricardo Colomo-Palacios. 2016. Knowledge discovery in software teams by means of evolutionary visual software analytics. Sci- ence of Computer Programming 121: 55{74. doi:10.1016/j.scico.2015.09.005. <a href="https://linkinghub.elsevier.com/retrieve/pii/S0167642315002658" rel="nofollow">https://linkinghub.elsevier.com/retrieve/pii/S0167642315002658</a>.
  * Zemel, Alan, Timothy Koschmann, Curtis LeBaron, and Paul Feltovich. 2007. What are we Missing? Usability&#8217;s Indexical Ground. Computer Supported Cooperative Work.

# Acknowledgements

Many members of the CHAOSS community contributed to this report and analysis. I am happy to share names with permission from the contributors, but I have not requested permission as of the publication date.

[^1]: Once we are to this point, I think CHAOSS is kicking butt and taking names.

[A PDF Version of this Post is Available Here.][1]\[/vc\_column\_text\]\[/vc\_column\][/vc\_row]

 [1]: https://github.com/chaoss/website/blob/master/Community/News/20181114_community_mangers.pdf