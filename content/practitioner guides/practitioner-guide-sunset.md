---
title: Practitioner Guide – Sunsetting an Open Source Project
author: elizabeth
type: page
date: 2025-05-27T15:39:20+00:00
ppma_authors_name:
  - elizabeth
  - elizabeth
nectar-metabox-portfolio-display:
  - all
nectar-metabox-portfolio-display-sortable:
  - off
url: /practitioner-guide-sunset
---
\[vc\_row type=&#8221;in\_container&#8221; full\_screen\_row\_position=&#8221;middle&#8221; column\_margin=&#8221;default&#8221; column\_direction=&#8221;default&#8221; column\_direction\_tablet=&#8221;default&#8221; column\_direction\_phone=&#8221;default&#8221; scene\_position=&#8221;center&#8221; text\_color=&#8221;dark&#8221; text\_align=&#8221;left&#8221; row\_border\_radius=&#8221;none&#8221; row\_border\_radius\_applies=&#8221;bg&#8221; overlay\_strength=&#8221;0.3&#8243; gradient\_direction=&#8221;left\_to\_right&#8221; shape\_divider\_position=&#8221;bottom&#8221; bg\_image\_animation=&#8221;none&#8221;\]\[vc\_column column\_padding=&#8221;no-extra-padding&#8221; column\_padding\_tablet=&#8221;inherit&#8221; column\_padding\_phone=&#8221;inherit&#8221; column\_padding\_position=&#8221;all&#8221; background\_color\_opacity=&#8221;1&#8243; background\_hover\_color\_opacity=&#8221;1&#8243; column\_shadow=&#8221;none&#8221; column\_border\_radius=&#8221;none&#8221; column\_link\_target=&#8221;\_self&#8221; gradient\_direction=&#8221;left\_to\_right&#8221; overlay\_strength=&#8221;0.3&#8243; width=&#8221;1/1&#8243; tablet\_width\_inherit=&#8221;default&#8221; tablet\_text\_alignment=&#8221;default&#8221; phone\_text\_alignment=&#8221;default&#8221; column\_border\_width=&#8221;none&#8221; column\_border\_style=&#8221;solid&#8221; bg\_image\_animation=&#8221;none&#8221;\]

# Practitioner Guide: Getting Started with Sunsetting an Open Source Project

Primary metrics:

  * [Change Requests][1]
  * [Issues New][2]
  * [Technical Forks][3]

If you haven’t already read the [Insight Guide: Introduction - Things to Think about When Interpreting Metrics][4], please pause now and read that guide.

Many open source projects, even widely used ones, become abandoned for a variety of reasons (e.g., evolving interests, family situations, employment changes), but abandonment can be done in a responsible way by proactively sunsetting the project (Miller et al. 2025). Sunsetting is an important consideration for corporate environments where it can be easy to lose track of projects that were created by employees who later walked away from the project and left if abandoned. You don’t want abandoned open source projects with security vulnerabilities sitting in your organization’s source code repositories where someone might trust that project simply because they trust your organization. Finding inactive projects and responsibly sunsetting them is a good business decision and something that many open source teams / Open Source Program Offices (OSPOs) do on a regular basis.

It’s important to remember that not every open source project can or should exist forever: technologies evolve, corporate priorities change, and people’s interests change. Part of the beauty of open source is that we work in the open as we innovate, and some of those innovative projects will stand the test of time, while others should be responsibly deprecated via a sunset process. Sunsetting an open source project should take your user’s needs into account, and where possible, offer users time to migrate to a replacement technology. At a minimum, it’s important to signal that the project will no longer be maintained, updated, or have security patches so that users know that they should no longer be using the project.

The most important step you can take when sunsetting a project is to be transparent at every step of the way. Thus, being open about your intentions and ensuring trust for future open source work.

# Step 1: Identify Trends

There are several metrics that can help you identify whether there is any activity or usage for a project to make decisions about responsibly sunsetting a project. Looking at [Change Requests][1] (aka Pull Requests / Merge Requests) and [New Issues][2] can be a good start when looking at whether there are still people using and contributing to a project. Another good metric is [Technical Forks][3], which tend to be an indication of usage and potential contribution.

## Change Requests

The Change Requests metric can help you understand whether people are trying to contribute to your project, which signals whether there is interest in your project. It helps to look at both closed and open requests, since closed change requests indicate that a project might still be maintained, while open change requests that are not being resolved can indicate that a project might be abandoned. If there are no recently merged change requests, then it’s also likely that there have not been any security updates.

<img decoding="async" src="https://github.com/chaoss/wg-data-science/blob/main/practitioner-guides/images/change_requests_abandoned.png?raw=true" alt="Abandoned project - change requests" title="Example of project change requests decreasing to almost nothing over time. These might be from an abandoned project" /> 

## New Issues

Many new issues are created when a user finds a bug, has a question, or wants a new feature, so new issues may be filed because people are using your project or are otherwise interested in your project. When there are few to no issues created over a period of some time, then it might indicate that the project has been abandoned.

<img decoding="async" src="https://github.com/chaoss/wg-data-science/blob/main/practitioner-guides/images/issues_abandoned.png?raw=true" alt="Abandoned project - new issues" title="Example of new issues decreasing to almost nothing over time. These might be from an abandoned project" /> 

## Technical Forks

These are the forks that people create when they are using your project or planning to contribute to it, but it can help to look beyond the numbers of forks to see who has forked your project and whether they are continuing to update their fork. Recently updated forks can indicate usage, and by gathering data about who has forked your project, you might also be able to reach out to some of these people to ask if they are still using it before you decide whether, or how, to sunset it. 

# Step 2: Diagnosis

If you are part of an organization who is auditing their repositories to find projects that seem to be abandoned, you should start by talking to the people who were involved in the project so that you can better understand whether the project is truly abandoned, and if so, why. This will likely require looking at the most recent change requests to see who made the last few changes to the project so that you can reach out to them. In some cases, a project might not need to be updated regularly and might seem to be abandoned when it has simply stabilized and might still be widely used. For example, a small library that performs some complex mathematical function might not need to be updated after it is written, assuming that it doesn’t have dependencies that need to be updated. If the project is primarily distributed via package managers, usage metrics from those sources should also be considered.

If the project has truly been abandoned, then it can help to understand why it was abandoned and whether anyone might still be using it before you decide to sunset it. This is where the technical fork data can be useful to see if other people have forked your project and are continuing to update their fork, which might indicate usage of your project. [Criticality Score][5], an OpenSSF project, can also shed light on usage, since it also calculates the number of projects that depend on your project. There is a [Python script][6] called that uses criticality score and the GitHub API fork data that can be used to gather and analyze this data.

# Step 3: Gather Additional Data if Needed

CHAOSS has other metrics to understand project activity and usage that can be helpful when deciding whether to sunset a project.

Additional Metrics: 

  * [Collaboration Platform Activity][7]
  * [Clones][8]
  * [Code Changes Commits][9]
  * [Release Frequency][10]
  * [Project Popularity][11]
  * [Criticality Score][5] (an OpenSSF tool, not a CHAOSS metric)
  * Package Manager usage metrics

# Step 4: Make the Change

After you have completed your diagnosis and have decided to sunset a project, there are several things you can do to ensure that you are sunsetting the project in a responsible manner. Preparing the repository for archival by following the tasks below helps reduce risk, simplifies maintenance, and leaves the repository in a clear final state before sunsetting.

**Communication**

Communication should start with any existing contributors to make sure that they agree with this decision. In some cases, there may be contributors who would like to continue the project, instead of sunsetting it.

When you have agreement to sunset the project, then this needs to be communicated to any existing users, including any other internal teams who may be using the project. This communication should be done in a transparent manner by being clear about the reasons for sunsetting it. There are quite a few places that this should be communicated and documented:

  * README: Clearly state at the top the README that the project has been deprecated and will no longer be updated. If possible, suggest alternate projects that provide similar functionality.
  * Project communication channels: This may include Slack, mailing lists, forums, social media, and any other channels used for communication within the project.
  * Documentation: Project documentation should also be updated. This may include wikis, project boards, websites, and other project documentation.
  * Package managers / distribution channels: Since most projects are distributed via package managers (e.g., npm, PyPI, RubyGems), those should also be updated with a deprecation warning that clearly states that the project is no longer being maintained or updated.
  * Additional channels: If this is a corporate project, marketing and other internal teams should also be notified.
  * Users: Known users of the project should also be notified.

**Code & Security Review**

At a minimum, review the repositories for secrets, keys, and personal identifiable information (PII). Be sure to remove or redact any sensitive information found.

For larger projects, it is worth doing a thorough review of the code and its commit history. Resolve any code scanning and security alerts found through Dependabot, CodeQL, and other code analysis tools. If the repository has a CHANGELOG and/or releases/tags, making sure it reflects all completed work and the project's final state.

**Issues**

Review all open issues, close those that are already fixed, and add context on unresolved items. Apply appropriate labels and close issues as `won't fix` where applicable.

**Change Requests**

Review all change requests, merge those that have no conflicts and pass tests. Dependabot PRs should also be tested and merged to ensure security vulnerabilities are addressed. Comment on any remaining open change requests with their current status, and close change requests as `won't fix` where applicable.

**Repository Metadata**

If your project contains metadata files (e.g. `code.json`, `publiccode.yml`, or `codemeta`), update them to reflect archival status and ensure all fields are current.

If your project does not contain this type of file, consider adding one to the repository.  
Adding a metadata file improves discoverability, helps users and internal teams understand project status, and makes lifecycle and compliance tracking easier over time for your organization's software inventory.

**Housekeeping**

Perform an audit reviewing all users with committer access permissions to the repository. Remove access for users who no longer need it. Alongside, clean up the repository by deleting stale/inactive branches and unnecessary files/artifacts.

**Checklists & Tools**

The checklists below summarize the tasks listed above:

  * [CMS.gov OSPO Basic Repository Archival Checklist][12]
  * [CMS.gov OSPO Comprehensive Repository Archival Checklist][13]
  * [Template Checklist][14]

There are various tools that can assist with the completion of the archival preparation tasks. For instance, the [repo-sunsetter GitHub Action][15] prepares a repository for archival by generating a review checklist (found above) as a repository issue and automating documentation updates.

**Archival**

The project should be officially archived using something like GitHub’s archival method. It might also be a good idea to keep these projects in a separate location to make it clear that these projects have reached the end of their life. For example, VMware has a separate ‘vmware-archive’ organization, and Apache has something similar called the ‘Apache Attic’.

Taking the additional step of adding your code to the [Software Heritage][16] archive can help preserve it over time. This is especially true if you are self-hosting your source code repositories, but it can also help archived code outlive potential platform changes and make it easier for people to find in the future. 

Keep in mind that projects can always be unarchived if you change your mind later. Stressing this fact can often make it easier to get people to agree to the sunset process.

**Special Case: Sunsetting Active Projects**

Unfortunately, even active projects may need to be sunsetted, which can be much more difficult. This can happen when a project is being maintained entirely by a company, and that company has a shift in strategy and decides that they no longer wish to staff or maintain a project that is being widely used. There are a number of additional considerations in this case that should happen before the project is archived:

  * Public Relations (PR): Archiving an active project can be a tricky situation that might result in negative press as soon as you start talking to people about your desire to sunset the project, so before talking to anyone outside of your company, you want to get your PR team involved so that they can be ready to handle any queries.
  * Option to continue under new ownership: Determine if there are other contributors or other organizations who would be willing and able to take over new development and / or maintenance of the project.
  * Sunset plan: It can help to create a detailed plan that outlines all of the steps that need to be taken along with a timeframe for when the project will be sunsetted.
  * Timing: A responsible sunset plan will give users time to migrate to another solution before you stop making security updates and releases. 6 months is a good starting point.
  * Customers, users, and communication: Careful communication is required to communicate this decision along with the timing to any existing customers and users.

# Cautions and Considerations

  * It is worth taking some extra time to talk to contributors and make sure that the decision to sunset a project is the right decision before you do it.
  * Be as transparent as possible about the decision to sunset a project and why you made that decision.
  * Sunsetting a project is not an indication of failure and should not be positioned as such. Projects have life cycles; they endure for as long as they are needed and then they should be responsibly deprecated when they are no longer needed.
  * Consider providing transition details, and if possible, tooling that helps your existing users transition to an alternative solution if a reasonable one is available. 
  * As with all of the CHAOSS Practitioner Getting Started Guides, these materials are designed to help you get started when sunsetting a project, but it is not a comprehensive guide with everything you might need to know for every situation.

# Additional Reading

  * We have a [short video][17] (2 minutes) devoted to this guide on the CHAOSS YouTube channel.
  * [CHAOSScast Episode 123: Practitioner Guides: #6 Sunsetting an Open Source Project][18]
  * Stefka Dimitrova on When and How to Deprecate an Open Source Project ([Part 1][19] and [Part 2][20]) along with a video from the Open Source Summit in Europe in 2022 about [Simple Steps for a Calm “Sunset”][21]. Much of the content for this guide is based on these materials.
  * [GitHub’s Do’s and Don'ts When Sunsetting Open Source Projects][22]
  * [TODO Group Guide: Shutting Down an Open Source Project][23]
  * [Allen Friedman on End of Life and End of Support Across the Ecosystem][24] (video)
  * [10 Quick tips for making software outlive your job (white paper)][25]
  * [CMS.gov OSPO Repository Archival Guide][26]

# Contributors

The following people contributed to this guide:

  * Dawn Foster
  * Ria Schalnat
  * Damián Vicino
  * Matt Germonprez
  * Elizabeth Barron
  * Tara Tarakiyee
  * Natalia Luzuriaga
  * Isaac Milarsky
  * Sachin Panayil
  * Dinne Kopelevich
  * Remy DeCausemaker

# References

  * Miller, C., Jahanshahi, M., Mockus, A., Vasilescu, B., & Kästner, C. (2025). [Understanding the response to open-source dependency abandonment in the npm ecosystem][27]. In _Int’l Conf. Software Engineering (ICSE), IEEE/ACM_.
  * [repo-sunsetter GitHub Action][15]

CHAOSS Practitioner Guides are MIT licensed, living documents, and we welcome your feedback and input. You can suggest edits to this document at [<https://github.com/chaoss/wg-data-science/blob/main/practitioner-guides/sunset.md>][28]

\[/vc\_column\]\[/vc\_row\]

 [1]: https://chaoss.community/?p=3610
 [2]: https://chaoss.community/?p=3634
 [3]: https://chaoss.community/?p=3431
 [4]: https://chaoss.community/practitioner-guide-introduction/
 [5]: https://github.com/ossf/criticality_score
 [6]: https://github.com/geekygirldawn/project-api-metrics/blob/main/scripts/sunset.py
 [7]: https://chaoss.community/?p=3484
 [8]: https://chaoss.community/?p=3429
 [9]: https://chaoss.community/?p=4707
 [10]: https://chaoss.community/?p=4765
 [11]: https://chaoss.community/?p=3573
 [12]: https://github.com/DSACMS/repo-sunsetter/blob/main/checklists/BASIC_ARCHIVAL_CHECKLIST.md
 [13]: https://github.com/DSACMS/repo-sunsetter/blob/main/checklists/COMPREHENSIVE_ARCHIVAL_CHECKLIST.md
 [14]: https://github.com/DSACMS/repo-sunsetter/blob/main/checklists/TEMPLATE_ARCHIVAL_CHECKLIST.md
 [15]: https://github.com/marketplace/actions/repo-sunsetter
 [16]: https://www.softwareheritage.org/
 [17]: https://www.youtube.com/watch?v=dsiWoapOHzA&list=PL60k37cxI-HSHV4-rEsWMzExw2y2Oq79Z&index=6
 [18]: https://podcast.chaoss.community/123
 [19]: https://blogs.vmware.com/opensource/2022/09/29/when-and-how-to-deprecate-an-open-source-project/
 [20]: https://blogs.vmware.com/opensource/2023/05/17/deprecating-an-open-source-project-part-2/
 [21]: https://www.youtube.com/watch?v=OdpkMkoKtDY
 [22]: https://github.blog/open-source/maintainers/dos-and-donts-when-sunsetting-open-source-projects/
 [23]: https://todogroup.org/resources/guides/shutting-down-an-open-source-project/
 [24]: https://www.youtube.com/watch?v=ZgWwiKLB6hE
 [25]: https://arxiv.org/abs/2505.06484
 [26]: https://dsacms.github.io/ospo-guide/outbound/archiving-repositories/
 [27]: http://www.cs.cmu.edu/~ckaestne/pdf/icse25_abandonment.pdf
 [28]: https://github.com/chaoss/wg-data-science/blob/main/practitioner-guides/sunset.md