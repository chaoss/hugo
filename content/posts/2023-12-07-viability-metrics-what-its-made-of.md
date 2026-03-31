---
title: Metrics for OSS Viability
author:
  - Gary White
type: post
date: 2023-12-07T14:49:32+00:00
url: /viability-metrics-what-its-made-of/
nectar_blog_post_view_count:
  - 3015
publish_post_category:
  - 5
ppma_authors_name:
  - Gary White
categories:
  - Blog Post
tags:
  - metrics models
  - viability

---
\[vc\_row type=&#8221;in\_container&#8221; full\_screen\_row\_position=&#8221;middle&#8221; column\_margin=&#8221;default&#8221; column\_direction=&#8221;default&#8221; column\_direction\_tablet=&#8221;default&#8221; column\_direction\_phone=&#8221;default&#8221; scene\_position=&#8221;center&#8221; text\_color=&#8221;dark&#8221; text\_align=&#8221;left&#8221; row\_border\_radius=&#8221;none&#8221; row\_border\_radius\_applies=&#8221;bg&#8221; overlay\_strength=&#8221;0.3&#8243; gradient\_direction=&#8221;left\_to\_right&#8221; shape\_divider\_position=&#8221;bottom&#8221; bg\_image\_animation=&#8221;none&#8221;\]\[vc\_column column\_padding=&#8221;no-extra-padding&#8221; column\_padding\_tablet=&#8221;inherit&#8221; column\_padding\_phone=&#8221;inherit&#8221; column\_padding\_position=&#8221;all&#8221; background\_color\_opacity=&#8221;1&#8243; background\_hover\_color\_opacity=&#8221;1&#8243; column\_shadow=&#8221;none&#8221; column\_border\_radius=&#8221;none&#8221; column\_link\_target=&#8221;\_self&#8221; gradient\_direction=&#8221;left\_to\_right&#8221; overlay\_strength=&#8221;0.3&#8243; width=&#8221;1/1&#8243; tablet\_width\_inherit=&#8221;default&#8221; tablet\_text\_alignment=&#8221;default&#8221; phone\_text\_alignment=&#8221;default&#8221; column\_border\_width=&#8221;none&#8221; column\_border\_style=&#8221;solid&#8221; bg\_image\_animation=&#8221;none&#8221;\][vc\_column\_text] 

[In the last post][1], we gave a background on Viability in Open Source. We covered the motivation, and implementation plan of how we’ll collect and measure metrics about open source that we use or might use at Verizon.

<div class="wp-block-image">
  <figure class="aligncenter size-large"><img loading="lazy" decoding="async" width="678" height="1024" class="wp-image-5489" src="https://chaoss.local/wp-content/uploads/2023/12/marissa-grootes-ck0i9Dnjtj0-unsplash-678x1024.jpg" alt="Metrics on a list next to a laptop, ruler, and calendar" srcset="https://chaoss.local/wp-content/uploads/2023/12/marissa-grootes-ck0i9Dnjtj0-unsplash-678x1024.jpg 678w, https://chaoss.local/wp-content/uploads/2023/12/marissa-grootes-ck0i9Dnjtj0-unsplash-199x300.jpg 199w, https://chaoss.local/wp-content/uploads/2023/12/marissa-grootes-ck0i9Dnjtj0-unsplash-768x1160.jpg 768w, https://chaoss.local/wp-content/uploads/2023/12/marissa-grootes-ck0i9Dnjtj0-unsplash-1017x1536.jpg 1017w, https://chaoss.local/wp-content/uploads/2023/12/marissa-grootes-ck0i9Dnjtj0-unsplash-1356x2048.jpg 1356w, https://chaoss.local/wp-content/uploads/2023/12/marissa-grootes-ck0i9Dnjtj0-unsplash-200x302.jpg 200w, https://chaoss.local/wp-content/uploads/2023/12/marissa-grootes-ck0i9Dnjtj0-unsplash-1320x1993.jpg 1320w, https://chaoss.local/wp-content/uploads/2023/12/marissa-grootes-ck0i9Dnjtj0-unsplash-scaled.jpg 1696w" sizes="auto, (max-width: 678px) 100vw, 678px" /></p> <figcaption><em>Considering all these metrics together takes a list and a laptop, and maybe a ruler.</em><br />Photo by <a href="https://unsplash.com/@stilclassis?utm_content=creditCopyText&utm_medium=referral&utm_source=unsplash">Marissa Grootes</a> on <a href="https://unsplash.com/photos/silver-laptop-computer-near-notebook-ck0i9Dnjtj0?utm_content=creditCopyText&utm_medium=referral&utm_source=unsplash">Unsplash</a></figcaption> </figure>
</div>

In this post, we will cover the nitty-gritty details of which metrics we’re using in our model, and why they fit together. Rather than covering each metric individually, I’ll summarize what metrics are in each model, and give an overview on why they fit together for a good picture of the model. We’ll also cover the value proposition of metrics that cross between the categories comprising the full model.

What follows is the list of metrics comprising the Viability model, and why they are included:

## Compliance + Security {.wp-block-heading}

#### **Just for this model:** {.wp-block-heading}

[OpenSSF Best Practices][2]

<ul class="wp-block-list">
  <li>
    This is a proxy metric for us to ensure that a project responds to security incidents, and has enough protections in place to generally interpret a reliable <strong>Compliance and Security</strong> strategy.
  </li>
  <li>
    This allows us to avoid using costly SCA/SAST scanning on every open source project we consider.
  </li>
</ul>

[License Coverage][3]

<ul class="wp-block-list">
  <li>
    We use this to make decisions about risk of using unlicensed software, or determine if our use case of the software is compatible with the license provided.
  </li>
</ul>

[Licenses Declared][4]

<ul class="wp-block-list">
  <li>
    This lets us compare our intended usage and project policy against the policy of our dependencies.
  </li>
</ul>

[OSI Approved Licenses][5]

<ul class="wp-block-list">
  <li>
    Knowing we’ve reviewed the implication of each OSI license provides confidence that we understand how to use the software in compliance with those licenses.
  </li>
</ul>

[Defect Resolution Duration][6]

<ul class="wp-block-list">
  <li>
    This metric allows us to consider, apples to apples, radically different response rates to defects when they occur between projects. 
  </li>
  <li>
    Our understanding of this metric across projects and across a suite of dependencies calibrates our risk profile and tolerance.
  </li>
</ul>

[Upstream Code Dependencies][7]

<ul class="wp-block-list">
  <li>
    Where we intend this metric for the model of viability is to ensure that dependencies of a project are also included in any viability evaluation we perform. 
  </li>
  <li>
    It is important to consider an application alongside dependencies it shares to give a full picture of a particular project’s risk portfolio.
  </li>
</ul>

#### **Shared between models:** {.wp-block-heading}

[Libyears][8]

<ul class="wp-block-list">
  <li>
    “A <strong>simple</strong> measure of <em>software dependency freshness</em>. It is a <strong>single number</strong> telling you how up-to-date your dependencies are.”
  </li>
  <li>
    This metric allows for apples-to-apples comparisons between projects of freshness. 
  </li>
  <li>
    Scales to show complex projects with many dependencies, and the risk associated with using those projects with the massive maintenance cost behind the scenes.
  </li>
</ul>

### What the metrics for Viability {.wp-block-heading}

Overall, we use this metrics model to gauge how well both the community and the maintainers of the application consider the security and compliance of their application. We expect to use these indicators to gauge risk. We have showstoppers like licensing, where a license can be flatly incompatible with our intended use case, through security-centric badges and metrics, to how fast and regularly a team maintains the dependencies and defects reported to their application. 

Additionally, like in other models, some metrics are very tricky to trace or visualize. We leave a healthy amount of flexibility in how we rank applications against tricky-to-gather metrics, and we recommend that users of our models do the same. For example: Much like the Defect Resolution Duration; the appetite for how many Libyears is appropriate for a project will always be up to maintainers. Depending on how or where an app may run, and how frequently we can update it, we think about Libyears critically. 

Following other metrics and models, Libyears notably contributes to three of our metrics models: Compliance/Security, Governance, and Community. We believe that it fits particularly well in Compliance + Security as it gives an indicator not only about how critically maintainers consider compliance and security in their own project, but in the projects they’re dependent on.

## Governance {.wp-block-heading}

#### **Just for this model:** {.wp-block-heading}

[Issues Inclusivity][9]

<ul class="wp-block-list">
  <li>
    Provides an effective measurement for intentional aggregation of issues
  </li>
  <li>
    Indicates how community skills are applied to project responsibilities.
  </li>
</ul>

[Documentation Usability][10]

<ul class="wp-block-list">
  <li>
    Strong, usable documentation is required.
  </li>
  <li>
    Though this can include a lot of manual effort, this is a very important metric to attempt to collect.
  </li>
</ul>

[Time to Close][11]

<ul class="wp-block-list">
  <li>
    How long it usually takes for a contribution to the project to make its way to the codebase
  </li>
  <li>
    Will give us an idea of consistency in the project (median, mean, mode) <ul>
      <li>
        This is not to be confused with defect resolution (we hold a higher standard for)
      </li>
    </ul>
  </li>
  
  <li>
    Other processes may occur alongside opening and closing a PR, for example, but this provides enough of an indicator to be inherently useful to the Governance of a project.
  </li>
</ul>

[Issue Age][12]

<ul class="wp-block-list">
  <li>
    How long questions / suggestions / etc. generally hang around a project.
  </li>
  <li>
    Simple to understand, easy to dive further into by looking at what issues are about.
  </li>
</ul>

#### Shared Between Models: {.wp-block-heading}

[Change Request Closure Ratio][13]

<ul class="wp-block-list">
  <li>
    Compare the drift of new requests to their rate of closure. 
  </li>
  <li>
    Gives us an idea of how the project is maintained – or if more maintainers might be needed to keep up with demand for new features.
  </li>
</ul>

[Project Popularity][14]

<ul class="wp-block-list">
  <li>
    Aggregate of other smaller metrics one might expect to find in a cursory glance over a project landing page. 
  </li>
  <li>
    Likes, stars, badges, forks, clones, downstream dependencies, mentions on social media, and more.
  </li>
</ul>

[Release Frequency][15]

<ul class="wp-block-list">
  <li>
    Knowing the timing of regular releases, and being able to understand frequency and cadence we may expect security patches and new features to identify how well our project’s release cadence and strategy fits with potential dependencies. 
  </li>
  <li>
    This is somewhat a proxy for LTS / release strategy that may otherwise be available for larger projects.
  </li>
</ul>

[Libyears][8]

<ul class="wp-block-list">
  <li>
    “A <strong>simple</strong> measure of <em>software dependency freshness</em>. It is a <strong>single number</strong> telling you how up-to-date your dependencies are.”
  </li>
  <li>
    This metric allows for apples-to-apples comparisons between projects of freshness. 
  </li>
  <li>
    Scales to show complex projects with many dependencies, and the risk associated with using those projects with the massive maintenance cost behind the scenes.
  </li>
</ul>

### What the metrics mean for Viability {.wp-block-heading}

These metrics are useful to show the intention or lack of intention in the project Governance. For example, If there’s a lack of inclusive labels on issues: it identifies a gap in welcoming new contributors and softing existing contributors through workstreams. The Governance of a project is reflected in turn. Same goes for many of these metrics. The ability to contribute, understand, or depend on a project is highly coupled to the effort behind Governance.

This isn’t to say poor Governance metrics indicate that a project is governed by fools. Low CRCR, for example, may simply indicate that there are not as many maintainers to support a contributing community. A lack of new issues could be the result of a recent large release that addresses many recurring issues. These metrics are important to aggregate these reasons not to cast doubt on maintainers of projects. Only to identify the Governance capacity and effort across projects in a software portfolio.

If some of these metrics feel like they could be strong community metrics, I think they can be. Many of the shared metrics here are a combination of the effort a community has with a project, and the effort of the body governing a project. We think the overlap of shared metrics captures this relationship well, considering the responsibility contributors and maintainers share in creating OSS.

## Community {.wp-block-heading}

#### **Just for this model:** {.wp-block-heading}

[Clones][16]

<ul class="wp-block-list">
  <li>
    How many times a project has been pulled from a repository into a local machine. 
  </li>
  <li>
    Indicator of how many people are using or evaluating the project.
  </li>
</ul>

[Technical Forks][17]

<ul class="wp-block-list">
  <li>
    How many <a href="https://docs.github.com/en/get-started/quickstart/fork-a-repo">forks</a> have been made of a given project.
  </li>
  <li>
    Forks, in our estimation, are normally performed to create contributions through changes or to take the project in a new direction in their own community.
  </li>
</ul>

[Types of Contributions][18]

<ul class="wp-block-list">
  <li>
    Not all contributions are code, strategy / issues / Reviews / events / Writing articles / etc. gives a strong indication of the maintainer’s ability to grow or continue building a project. <ul>
      <li>
        Likewise, if contributions are coming in only as requests with no coding alongside it – we can assume the project doesn’t have active contributors. 
      </li>
      <li>
        Any large ratio distribution might tip the scales of if we should or should not recommend a project as viable.
      </li>
    </ul>
  </li>
</ul>

[Change Requests][19]

<ul class="wp-block-list">
  <li>
    The volume of regular requests, or the emergence of a pattern of change requests (around holidays, weekends, weekdays) can tell us a lot about a project. 
  </li>
  <li>
    By identifying trends, we can make many educated guesses about the strength, patterns, and sustainability of a project Community.
  </li>
</ul>

[Committers][20]

<ul class="wp-block-list">
  <li>
    We don’t say “no projects under x committers is viable” – because the two are not related. <ul>
      <li>
        We care about <em>committer trends</em>. 
      </li>
    </ul>
  </li>
</ul>

#### **Shared Between Models:** {.wp-block-heading}

[Change Request Closure Ratio][13]

<ul class="wp-block-list">
  <li>
    Compare the drift of new requests to their rate of closure. 
  </li>
  <li>
    Can help indicate a cooling or heating contribution community by monitoring merged community requests.
  </li>
</ul>

[Project Popularity][14]

<ul class="wp-block-list">
  <li>
    Aggregate of other smaller metrics one might expect to find in a cursory glance over a project landing page. 
  </li>
  <li>
    Likes, stars, badges, forks, clones, downstream dependencies, mentions on social media, and more.
  </li>
</ul>

[Libyears][8]

<ul class="wp-block-list">
  <li>
    “A <strong>simple</strong> measure of <em>software dependency freshness</em>. It is a <strong>single number</strong> telling you how up-to-date your dependencies are.”
  </li>
  <li>
    This metric allows for apples-to-apples comparisons between projects of freshness. 
  </li>
  <li>
    Scales to show complex projects with many dependencies, and the risk associated with using those projects with the massive maintenance cost behind the scenes.
  </li>
</ul>

### What the metrics mean for Viability {.wp-block-heading}

With Community, we seek to understand the “tinkering” that happens with a project, as well as being able to measure the contributions that are made. Clones and forks indicate how many users of software have pulled it to build from source, inspect the source code, submit a contribution, or take the project in a new direction. That flavor of popularity feels meaningful to trace community engagement in a project. 

With committer trends, types of contributions, and change requests, we can see how a Community is interacting. Maybe more markdown RFC’s are created than features, maybe vice-versa. With an understanding on what types of contributions are made, and how regular they are, we make a more informed judgment on project viability. In an example: we think it’s reasonable to expect that a project which has shed 90% of its committers in a three month period is less viable than a stable (flat) committer trend. The inverse could indicate a growing or stable project gaining popularity around a particular technology trend. Where some “tinkering” metrics feel micro, other metrics take a macro lens.

By measuring some shared metrics, we give this model an opportunity to be viewed from the perspective of how much the community maintains a project, and how much interest there is generally. We find this distinct from the Governance angle, even with significant overlap, as trends in these metrics are almost never entirely at fault of the community or in the maintainers of a given project. The numbers could be meaningful for either space, so they exist in both models.

## Strategy {.wp-block-heading}

#### **Just for this model:** {.wp-block-heading}

[Programming Language Distribution][21]

<ul class="wp-block-list">
  <li>
    We have strong opinions on which languages are viable at Verizon. <ul>
      <li>
        Many companies have similar standards and expectations – or normally center around a particular language. 
      </li>
    </ul>
  </li>
  
  <li>
    Unsupported or unused languages are a strong indicator of project viability. 
  </li>
</ul>

[Bus Factor][20]

<ul class="wp-block-list">
  <li>
    A count of the fewest number of committers that comprise 50% of activity over a period. 
  </li>
  <li>
    We can better understand the risk of using a particular project or set of projects, regarding how much support the project would get if top contributors left.
  </li>
</ul>

[Elephant Factor][22]

<ul class="wp-block-list">
  <li>
    Elephant factor is a lot like bus factor – but it counts the fewest “entities” that comprise 50% of activity on a project. 
  </li>
  <li>
    We use this to infer the influence companies have on a project, or how detrimental it would be if that company shifted priority.
  </li>
</ul>

[Organizational Influence][23]

<ul class="wp-block-list">
  <li>
    Organizational Influence measures the amount of control an organization may have in a project. This is an estimate, and an aggregation of several other metrics. 
  </li>
  <li>
    Details in the link, but <a href="https://docs.google.com/document/d/1TqX3pKHizRAFPv4HAEjOn9rUwJRlpGJLJD8r5piC0UE/edit#heading=h.dypm0c26wva3">organizational diversity</a> is one example of a metric that can aggregate to create an imprint of influence. 
  </li>
</ul>

#### **Shared Between Models:** {.wp-block-heading}

[Release Frequency][15]

<ul class="wp-block-list">
  <li>
    Knowing the timing of regular releases, and being able to understand frequency and cadence we may expect security patches and new features identifies how well our project’s release cadence and strategy fits with potential dependencies. 
  </li>
  <li>
    This is somewhat a proxy for LTS / release strategy that may otherwise be available for larger projects.
  </li>
</ul>

### What the metrics mean for Viability {.wp-block-heading}

Metrics we trace in this model trace the strategy, or expected influence from individuals and organizations. For example: With a bus factor of 1, it’s very possible that burnout or other factors could pull that one person away. With a more resilient count of folks, we are more likely to see a stable and viable maintenance strategy. As a highly regulated and large entity, Verizon considers which other entities might be developing critical infrastructure for our applications. We consider our risk appetite and tolerance in the scope of a project we use, to ensure we don’t rely too heavily on one particular provider. These metrics continue our mission of managing that risk profile.

We share release frequency between Strategy and Governance. This categorizes the overlap of how the maintainers of a project provide both a governance plan and a maintenance strategy.

## Wrap Up {.wp-block-heading}

Compliance + Security, Governance, Community, and Strategy. These are the tenets we use for our Viability Metrics (Super) Model. I’m excited to share this model with the broader software community for input and feedback, and to make it better over time. We will share our lessons learned and what practices we find the most effective for maintaining a viable software portfolio as we iterate.

Tune in next time for us to share a guide on OSS viability. We include recommended tools to set up Viability monitoring on projects. If you’d like to connect to talk about this post, join the CHAOSS community slack and find me, Gary White!

&nbsp; \[/vc\_column\_text\]\[/vc\_column\][/vc\_row]

 [1]: https://chaoss.local/oss-viability-metric-supermodel/
 [2]: https://chaoss.local/?p=3939
 [3]: https://chaoss.local/?p=3961
 [4]: https://chaoss.local/?p=3963
 [5]: https://chaoss.local/?p=3962
 [6]: https://chaoss.local/?p=4727
 [7]: https://chaoss.local/?p=3977
 [8]: https://chaoss.local/?p=3976
 [9]: https://chaoss.local/?p=3533
 [10]: https://chaoss.local/?p=3532
 [11]: https://chaoss.local/?p=3446
 [12]: https://chaoss.local/?p=3629
 [13]: https://chaoss.local/?p=4834
 [14]: https://chaoss.local/?p=3573
 [15]: https://chaoss.local/?p=4765
 [16]: https://chaoss.local/?p=3429
 [17]: https://chaoss.local/?p=3431
 [18]: https://chaoss.local/?p=3432
 [19]: https://chaoss.local/?p=3610
 [20]: https://chaoss.local/?p=3945
 [21]: https://chaoss.local/?p=3430
 [22]: https://chaoss.local/?p=3940
 [23]: https://chaoss.local/?p=3560