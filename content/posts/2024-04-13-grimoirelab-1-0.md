---
title: GrimoireLab 1.0
author:
  - Georg Link
type: post
date: 2024-04-13T16:28:41+00:00
url: /grimoirelab-1-0/
nectar_blog_post_view_count:
  - 3758
ppma_authors_name:
  - linkgeorg
categories:
  - Blog Post
  - News
tags:
  - GrimoireLab
  - new release
  - software

---
 

# GrimoireLab 1.0 {.wp-block-heading}

For eight years, we have been working to produce the best platform for software development analytics possible. With the work of more than 150 developers and after over 11,600 commits, we’re excited to announce the release of the first major version of GrimoireLab.

GrimoireLab is an evolution of the work done during more than 10 years by [Bitergia][1], LibreSoft URJC research group, and several contributors in [Metrics Grimoire][2] and [VizGrimorie][3] projects.. Since 2017, GrimoireLab has been part of The Linux Foundation [CHAOSS Software][4] community as one of its founding projects.

GrimoireLab has become common for open source project health dashboards. It has been used by some of the most important software companies and open source foundations in the world. The platform has also been used as the underlying foundation for other applications, including [Bitergia Analytics][5], [OSS Compass][6], [LFX Insights][7], [Cauldron][8], and [Mystic][9]. 

## What’s included in this GrimoireLab release? {.wp-block-heading}

<ul class="wp-block-list">
  <li>
    An automated platform to generate software analytics and insights.&nbsp;
  </li>
  <li>
    Data collection from more than 30 data sources.
  </li>
  <li>
    Generation of more than 150 metrics and visualizations to understand activity, performance, and community of open source projects.
  </li>
  <li>
    Identities manager to track the activity of an individual across platforms and organizations.&nbsp;
  </li>
  <li>
    Integration with third-party applications to visualize and analyze data (Kibana/OpenSearch Dashboards/Jupiter Notebooks).
  </li>
</ul>

## Why are we releasing this major version right now? {.wp-block-heading}

As our [roadmap][10] lays out, we’ve identified some challenges that require a major shift in how the platform works. We expect that version 2.0 of GrimoireLab will be significantly different, improving on scalability and maintenance and addressing advancements in AI.&nbsp; Therefore, we believe that releasing a stable version now will give our users predictability and stability moving forward.

## What can you expect from now on? {.wp-block-heading}

Version 1.0 will be maintained as a stable release that will continue to power enterprise, open source, and research users. Meanwhile, we will create a branch named 1.x to fix bugs and to include new features that will be part of the next major release. The active development of GrimoireLab 2.0 will show up in the main branch.&nbsp;

Some of the architectural changes detailed in our [roadmap][10] for version 2.0 include:

<ul class="wp-block-list">
  <li>
    Maintenance effort will be reduced in version 2.0 with a graphical user interface and an API for configuring data collection in GrimoireLab. Currently, system administrators need to manually update text files when new data is to be collected.
  </li>
  <li>
    Scalability and performance will be improved to handle more than 5,000 data endpoints and deliver insights faster. Currently, 3,500 high-active repositories require three days of data analysis before the data is ready for the user.
  </li>
  <li>
    Integration with other tools will be made easier. Users will be able to use different tools for visualizing and analyzing the data from GrimoireLab.
  </li>
</ul>

## Our thanks! {.wp-block-heading}

This release would not have been possible without the help of the entire community. We are deeply thankful to all our users. We would especially like to thank Álvaro del Castillo, Valerio Cosentino, Jesús González-Barahona, Alberto Pérez García-Plaza, J. Manrique López, Venu Vardhan Reddy Tekula, David Moreno, Gregorio Robles, Andy Grunwald, and the members of the CHAOSS project.&nbsp;

We recognize Bitergia and The Document Foundation for being early adopters and to be the first ones to enter their names on the new ADOPTERS.md file. If you use GrimoireLab, please add your organization to our [ADOPTERS.md file][11] so that we can recognize you. If you’ve done research with GrimorieLab, please add a citation and link to your publication.

The GrimoireLab Developers

 [1]: https://bitergia.com
 [2]: http://metricsgrimoire.github.io
 [3]: http://vizgrimoire.github.io
 [4]: https://chaoss.local
 [5]: https://github.com/bitergia-analytics
 [6]: https://compass.gitee.com/
 [7]: https://lfx.linuxfoundation.org/tools/insights/
 [8]: https://gitlab.com/cauldronio/
 [9]: https://opensource.ieee.org/rit/mystic-group
 [10]: https://github.com/chaoss/grimoirelab/blob/master/ROADMAP.md
 [11]: https://github.com/chaoss/grimoirelab/blob/master/ADOPTERS.md