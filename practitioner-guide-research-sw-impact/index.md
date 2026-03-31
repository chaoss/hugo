---
title: Practitioner Guide Research SW Impact
author: Dawn Foster
type: page
date: 2026-03-12T15:44:06+00:00
ppma_authors_name:
  - Dawn Foster
nectar-metabox-portfolio-display:
  - all
nectar-metabox-portfolio-display-sortable:
  - off

---
\[vc\_row type=&#8221;in\_container&#8221; full\_screen\_row\_position=&#8221;middle&#8221; column\_margin=&#8221;default&#8221; column\_direction=&#8221;default&#8221; column\_direction\_tablet=&#8221;default&#8221; column\_direction\_phone=&#8221;default&#8221; scene\_position=&#8221;center&#8221; text\_color=&#8221;dark&#8221; text\_align=&#8221;left&#8221; row\_border\_radius=&#8221;none&#8221; row\_border\_radius\_applies=&#8221;bg&#8221; overlay\_strength=&#8221;0.3&#8243; gradient\_direction=&#8221;left\_to\_right&#8221; shape\_divider\_position=&#8221;bottom&#8221; bg\_image\_animation=&#8221;none&#8221;\]\[vc\_column column\_padding=&#8221;no-extra-padding&#8221; column\_padding\_tablet=&#8221;inherit&#8221; column\_padding\_phone=&#8221;inherit&#8221; column\_padding\_position=&#8221;all&#8221; background\_color\_opacity=&#8221;1&#8243; background\_hover\_color\_opacity=&#8221;1&#8243; column\_shadow=&#8221;none&#8221; column\_border\_radius=&#8221;none&#8221; column\_link\_target=&#8221;\_self&#8221; gradient\_direction=&#8221;left\_to\_right&#8221; overlay\_strength=&#8221;0.3&#8243; width=&#8221;1/1&#8243; tablet\_width\_inherit=&#8221;default&#8221; tablet\_text\_alignment=&#8221;default&#8221; phone\_text\_alignment=&#8221;default&#8221; column\_border\_width=&#8221;none&#8221; column\_border\_style=&#8221;solid&#8221; bg\_image\_animation=&#8221;none&#8221;\]

# Practitioner Guide: Research Software Impact

If you haven’t already read the [Practitioner Guide: Introduction - Things to Think about When Interpreting Metrics][1], please pause now and read that guide.

# Audience / Scope

Researchers, evaluative teams, and funding agencies who are interested in determining the impact of software and/or community work as a product of research. This expert guide is specifically aimed at researchers and academic evaluation committees using open source research software work as part of reappointment, tenure, and promotion cases. 

# Introduction

“Research software is a key driver of innovation and the economy” (ReSA, 2025). This expert guide focuses on the impact of open source software and/or communities created and maintained by individuals and teams as part of their research role. This includes evaluators who are part of researcher reappointment, tenure, and promotion cases. This expert guide focuses on open source software and communities developed and maintained by a researcher or team to recognize the social and technical impact from that work. This expert guide highlights the importance of open source software and community work as significant scholarly outputs.

# Challenges

  * Software work does not have a history of being part of reappointment, tenure, and promotion cases and has not represented a traditional outcome of university research work.
  * Participation with communities is a complex and intensive endeavor and if incentive structures do not exist to recognize this work, there are few incentives to prioritize the additional effort required to maintain open source research software.
  * There are no consistent international practices for using software identifiers or citing software. 

# Lessons Learned

  * Universities are now exploring research software and community development as research outputs. This expert guide helps in the alignment between researchers and evaluators, identifying initial metrics that can be considered in light of research software impact. While these metrics do not constitute the entirety of all metrics that could be reported, they represent an important starting point. 

# How to Take Action

### Community Metrics

  * [Contributor Absence Factor][2] (also referred to as the Lottery Factor)

<img decoding="async" src="https://github.com/chaoss/wg-data-science/blob/main/practitioner-guides/images/rsi-contributor-absence.png?raw=true" alt="Lottery Factor" /> 

(from [<https://eightknot.osci.io/contributors/contribution_types>][3])

The **Contributor Absence Factor** assesses the degree to which a project relies on a small number of contributors by identifying the smallest number of contributors responsible for 50% of total contributions. A lower Contributor Absence Factor indicates higher dependency on fewer contributors, posing a risk if these individuals leave the project. This metric helps project maintainers evaluate resilience and continuity risks associated with contributor reliance. 

For researchers and evaluators, the contributor absence factor is helpful in understanding how an open source project is growing to include new contributors who are responsible for more than 50% of the code base. 

  * [New Contributors][4]

<img decoding="async" src="https://github.com/chaoss/wg-data-science/blob/main/practitioner-guides/images/rsi-contrib-growth.png?raw=true" alt="Contributor Growth" /> 

This metric measures the number of new contributors making their first contribution to a project, offering insight into the project's growth and engagement. Tracking new contributors helps in understanding patterns of participation and potential barriers to engagement, providing opportunities for community support, onboarding, and outreach. A steady influx of new contributors may indicate a healthy, inviting project, while declines can be a signal for potential challenges in engagement or accessibility. 

### Software Metrics

  * [Project Velocity][5]

<img decoding="async" src="https://github.com/chaoss/wg-data-science/blob/main/practitioner-guides/images/rsi-project-velocity.png?raw=true" alt="Project Velocity" /> 

  * The bubble’s area is proportional to the number of authors 
  * The y-axis is the total number of pull requests and issues 
  * The x-axis is the number of commits

Project velocity measures the number of issues, the number of pull requests, volume of commits, and number of contributors as an indicator of innovation. It gives a researcher a way to compare the project velocity across a portfolio of projects. A researcher can use the Project Velocity metric to report project velocity of their own open source project and compare project velocity across a portfolio of projects.

  * [Change Requests][6]

<img decoding="async" src="https://github.com/chaoss/wg-data-science/blob/main/practitioner-guides/images/rsi-pr-over-time.png?raw=true" alt="Change Requests over time" /> 

The Change Requests metric tracks the proposals for modifications to a project's source code that have been submitted for review during a given time frame. Tracking the number of change requests over time provides insight into the overall coding activity within a project. While this metric alone cannot measure the quality of the changes, it gives a good indication of how frequently contributors are engaging with the codebase.

# Conclusion

Use JOSS such that the software can be peer-reviewed and get a DOI.

Additional metrics could include: 

  * **Software Citations**: Software can be cited in research by referencing using an ID (e.g., its DOI, version number, and repository location, or a persistent software identifier such as the [SWHID from Software Heritage][7]), often using services like Zenodo. However, it is not universal practice to either provide an identifier for research software or cite software usage or dependencies in academic papers. 
  * **Use**: Use is a primary measure of research software impact, however, that cannot solely be measured by number of downloads or users. It is important to consider both the number of users and the context of usage. A particular piece of research software may be critical to a niche field, and so even a small number of users may make it highly impactful. Alternatively, another open source research software package may be used by many researchers, but may only be a small part of the whole solution, not critical and easily replaced. Usage may not be a reliable proxy for impact in this case. An innovative piece of software that enabled just one breakthrough scientific discovery might be heralded as extremely impactful. 
  * **Stars**: Stars can be a proxy for how “popular” a project is. 
  * **External Funding**: Open source research software that receives funding to develop, maintain or manage their projects have demonstrated value in their domain or field. 

# Cautions and Considerations

  * It is important that all with an interest in research software impact are aligned on initial metrics to discuss as presented in this guide. If different groups are applying different metrics, little will be gained in improving the conversation for all. 

# Additional Reading

  * [Research Software Citation:Cite and Make Citable][8] 
  * ReSA (2025) Available at: [About ReSA · Research Software Alliance][9] 

# Contributors

  * Matt Germonprez 
  * Clare Dillon

# References

CHAOSS Practitioner Guides are MIT licensed, living documents, and we welcome your feedback and input. You can suggest edits to this document at <https://github.com/chaoss/wg-data-science/blob/main/practitioner-guides/research-sw-impact.md>

\[/vc\_column\]\[/vc\_row\]

 [1]: https://chaoss.community/practitioner-guide-introduction/
 [2]: https://chaoss.community/?p=3944
 [3]: https://eightknot.osci.io/contributors/contribution_types
 [4]: https://chaoss.community/?p=3613
 [5]: https://chaoss.community/?p=3572
 [6]: https://chaoss.community/?p=3610
 [7]: https://www.softwareheritage.org/software-hash-identifier-swhid/
 [8]: https://cite.research-software.org/
 [9]: https://www.researchsoft.org/about-resa/