---
title: 'Guide for OSS Viability: A CHAOSS Metric Model'
author:
  - Gary White
type: post
date: 2023-12-19T18:59:15+00:00
url: /chaoss-guide-oss-viability/
nectar_blog_post_view_count:
  - 2304
publish_post_category:
  - 5
ppma_authors_name:
  - Gary White
categories:
  - Blog Post
tags:
  - Augur
  - GrimoireLab
  - metrics models
  - viability

---
 <figure class="wp-block-image size-large"><img loading="lazy" decoding="async" width="1024" height="596" src="https://chaoss.local/wp-content/uploads/2023/12/william-bout-7cdFZmLlWOM-unsplash-1024x596.jpg" alt="" class="wp-image-5517" srcset="https://chaoss.local/wp-content/uploads/2023/12/william-bout-7cdFZmLlWOM-unsplash-1024x596.jpg 1024w, https://chaoss.local/wp-content/uploads/2023/12/william-bout-7cdFZmLlWOM-unsplash-300x175.jpg 300w, https://chaoss.local/wp-content/uploads/2023/12/william-bout-7cdFZmLlWOM-unsplash-768x447.jpg 768w, https://chaoss.local/wp-content/uploads/2023/12/william-bout-7cdFZmLlWOM-unsplash-1536x894.jpg 1536w, https://chaoss.local/wp-content/uploads/2023/12/william-bout-7cdFZmLlWOM-unsplash-2048x1191.jpg 2048w, https://chaoss.local/wp-content/uploads/2023/12/william-bout-7cdFZmLlWOM-unsplash-200x116.jpg 200w, https://chaoss.local/wp-content/uploads/2023/12/william-bout-7cdFZmLlWOM-unsplash-1320x768.jpg 1320w" sizes="auto, (max-width: 1024px) 100vw, 1024px" /><figcaption>_Photo by [William Bout][1] on [Unsplash][2]_</figcaption></figure> 

_This guide is part of a three part series. This is part three. Read part [one][3] or [two][4] for [context][3] and a [deep][4]_[ _dive_][5] _into the metrics respectively._

In the last two posts of this series, we covered the existence of the CHAOSS Metrics (Super) Model for Viability. We then covered what exactly comprises that metrics model, and gave brief impressions of why and how they comprise a whole.

In this guide, we’ll talk about what’s possible with the CHAOSS tools, and how we can comprise a Viability metrics model. Namely, we’ll focus on [GrimoireLab][6] and [Augur][7].

Consider the chart below to see the breakdown of what is available for which service.

## Breakdown by Category {.wp-block-heading}<figure class="wp-block-table">

<table>
  <tr>
    <td>
      <strong>Category</strong>
    </td>
    
    <td>
      <strong>Metric</strong>
    </td>
    
    <td>
      <strong>Grimoirelab</strong>
    </td>
    
    <td>
      <strong>Augur</strong>
    </td>
  </tr>
  
  <tr>
    <td>
      Strategy
    </td>
    
    <td>
      Programming Language Distribution
    </td>
    
    <td>
      Available
    </td>
    
    <td>
      Available
    </td>
  </tr>
  
  <tr>
    <td>
      Strategy
    </td>
    
    <td>
      Bus Factor
    </td>
    
    <td>
      Available
    </td>
    
    <td>
      Available
    </td>
  </tr>
  
  <tr>
    <td>
      Strategy
    </td>
    
    <td>
      Elephant Factor
    </td>
    
    <td>
      Available
    </td>
    
    <td>
      Available
    </td>
  </tr>
  
  <tr>
    <td>
      Strategy
    </td>
    
    <td>
      Organizational Influence
    </td>
    
    <td>
      Available
    </td>
    
    <td>
      Available
    </td>
  </tr>
  
  <tr>
    <td>
      Strategy
    </td>
    
    <td>
      Release Frequency
    </td>
    
    <td>
      Not Available
    </td>
    
    <td>
      Available
    </td>
  </tr>
  
  <tr>
    <td>
      Community
    </td>
    
    <td>
      Clones
    </td>
    
    <td>
      Not Available
    </td>
    
    <td>
      Not Available
    </td>
  </tr>
  
  <tr>
    <td>
      Community
    </td>
    
    <td>
      Forks
    </td>
    
    <td>
      Available
    </td>
    
    <td>
      Available
    </td>
  </tr>
  
  <tr>
    <td>
      Community
    </td>
    
    <td>
      Types of Contributions
    </td>
    
    <td>
      Not Available
    </td>
    
    <td>
      Not Available
    </td>
  </tr>
  
  <tr>
    <td>
      Community
    </td>
    
    <td>
      Change Requests
    </td>
    
    <td>
      Available
    </td>
    
    <td>
      Not Available
    </td>
  </tr>
  
  <tr>
    <td>
      Community
    </td>
    
    <td>
      Committers
    </td>
    
    <td>
      Available
    </td>
    
    <td>
      Not Available
    </td>
  </tr>
  
  <tr>
    <td>
      Community
    </td>
    
    <td>
      Change Request Closure Ratio
    </td>
    
    <td>
      Available
    </td>
    
    <td>
      Available
    </td>
  </tr>
  
  <tr>
    <td>
      Community
    </td>
    
    <td>
      Project Popularity
    </td>
    
    <td>
      Available
    </td>
    
    <td>
      Available
    </td>
  </tr>
  
  <tr>
    <td>
      Community
    </td>
    
    <td>
      Libyears
    </td>
    
    <td>
      Not Available
    </td>
    
    <td>
      Available
    </td>
  </tr>
  
  <tr>
    <td>
      Governance
    </td>
    
    <td>
      Issue Label Inclusivity
    </td>
    
    <td>
      Available
    </td>
    
    <td>
      Available
    </td>
  </tr>
  
  <tr>
    <td>
      Governance
    </td>
    
    <td>
      Documentation Usability
    </td>
    
    <td>
      Not Available
    </td>
    
    <td>
      Not Available
    </td>
  </tr>
  
  <tr>
    <td>
      Governance
    </td>
    
    <td>
      Time to Close
    </td>
    
    <td>
      Available
    </td>
    
    <td>
      Available
    </td>
  </tr>
  
  <tr>
    <td>
      Governance
    </td>
    
    <td>
      Change Request Closure Ratio
    </td>
    
    <td>
      Available
    </td>
    
    <td>
      Available
    </td>
  </tr>
  
  <tr>
    <td>
      Governance
    </td>
    
    <td>
      Project Popularity
    </td>
    
    <td>
      Available
    </td>
    
    <td>
      Available
    </td>
  </tr>
  
  <tr>
    <td>
      Governance
    </td>
    
    <td>
      Libyears
    </td>
    
    <td>
      Not Available
    </td>
    
    <td>
      Available
    </td>
  </tr>
  
  <tr>
    <td>
      Governance
    </td>
    
    <td>
      Issue Age
    </td>
    
    <td>
      Available
    </td>
    
    <td>
      Available
    </td>
  </tr>
  
  <tr>
    <td>
      Governance
    </td>
    
    <td>
      Release Frequency
    </td>
    
    <td>
      Not Available
    </td>
    
    <td>
      Not Available
    </td>
  </tr>
  
  <tr>
    <td>
      Compliance / Security
    </td>
    
    <td>
      OpenSSF Best Practices
    </td>
    
    <td>
      Not Available
    </td>
    
    <td>
      Not Available
    </td>
  </tr>
  
  <tr>
    <td>
      Compliance / Security
    </td>
    
    <td>
      License Coverage
    </td>
    
    <td>
      Not Available
    </td>
    
    <td>
      Available
    </td>
  </tr>
  
  <tr>
    <td>
      Compliance / Security
    </td>
    
    <td>
      OSI Approved Licenses
    </td>
    
    <td>
      Not Available
    </td>
    
    <td>
      Available
    </td>
  </tr>
  
  <tr>
    <td>
      Compliance / Security
    </td>
    
    <td>
      Licenses Declared
    </td>
    
    <td>
      Not Available
    </td>
    
    <td>
      Available
    </td>
  </tr>
  
  <tr>
    <td>
      Compliance / Security
    </td>
    
    <td>
      Defect Resolution Duration
    </td>
    
    <td>
      Available
    </td>
    
    <td>
      Not Available
    </td>
  </tr>
  
  <tr>
    <td>
      Compliance / Security
    </td>
    
    <td>
      Libyears
    </td>
    
    <td>
      Not Available
    </td>
    
    <td>
      Available
    </td>
  </tr>
  
  <tr>
    <td>
      Compliance / Security
    </td>
    
    <td>
      Upstream Code Depencies
    </td>
    
    <td>
      Not Available
    </td>
    
    <td>
      Not Available
    </td>
  </tr>
</table><figcaption>A Summary of Available CHAOSS metrics and their fit to Viability across Grimoire and Augur</figcaption></figure> 

## Breakdown by Tool {.wp-block-heading}<figure class="wp-block-table">

<table>
  <tr>
    <td>
      <em>Augur Summary</em>
    </td>
    
    <td>
      &nbsp;
    </td>
    
    <td>
      &nbsp;
    </td>
  </tr>
  
  <tr>
    <td>
      <em>Category</em>
    </td>
    
    <td>
      Available
    </td>
    
    <td>
      Not Available
    </td>
  </tr>
  
  <tr>
    <td>
      Community
    </td>
    
    <td>
      50.00%
    </td>
    
    <td>
      50.00%
    </td>
  </tr>
  
  <tr>
    <td>
      Compliance / Security
    </td>
    
    <td>
      57.14%
    </td>
    
    <td>
      42.86%
    </td>
  </tr>
  
  <tr>
    <td>
      Governance
    </td>
    
    <td>
      75.00%
    </td>
    
    <td>
      25.00%
    </td>
  </tr>
  
  <tr>
    <td>
      Strategy
    </td>
    
    <td>
      100.00%
    </td>
    
    <td>
      &nbsp;
    </td>
  </tr>
  
  <tr>
    <td>
      <strong>Grand Total</strong>
    </td>
    
    <td>
      <strong>67.86%</strong>
    </td>
    
    <td>
      <strong>32.14%</strong>
    </td>
  </tr>
</table></figure> <figure class="wp-block-table">

<table>
  <tr>
    <td>
      Grimoirelab Summary
    </td>
    
    <td>
      &nbsp;
    </td>
    
    <td>
      &nbsp;
    </td>
  </tr>
  
  <tr>
    <td>
      <em>Category</em>
    </td>
    
    <td>
      Available
    </td>
    
    <td>
      Not Available
    </td>
  </tr>
  
  <tr>
    <td>
      Community
    </td>
    
    <td>
      62.50%
    </td>
    
    <td>
      37.50%
    </td>
  </tr>
  
  <tr>
    <td>
      Compliance / Security
    </td>
    
    <td>
      14.29%
    </td>
    
    <td>
      85.71%
    </td>
  </tr>
  
  <tr>
    <td>
      Governance
    </td>
    
    <td>
      62.50%
    </td>
    
    <td>
      37.50%
    </td>
  </tr>
  
  <tr>
    <td>
      Strategy
    </td>
    
    <td>
      80.00%
    </td>
    
    <td>
      20.00%
    </td>
  </tr>
  
  <tr>
    <td>
      <strong>Grand Total</strong>
    </td>
    
    <td>
      <strong>53.57%</strong>
    </td>
    
    <td>
      <strong>46.43%</strong>
    </td>
  </tr>
</table></figure> 

While we can’t get every metric for every service, we can get a good majority of what we need through a mix of Grimoire Lab, and Augur. We intend to continue building the ability to get this data into services like Grimore and Augur, then update the CHAOSS metrics wiki to reflect how we’ve done it.

Augur provides the most metrics overall for three categories, while Grimoire is best for Community management. Grimoire also provides [sigils][8], which create panels for you as a user for a good amount of metrics you may want to use. Augur also has a tool supported by RedHat that [visualizes metrics within it][9].

## How Does this Guide My Decisions? {.wp-block-heading}

Depending on your use case, you may find different opportunities to use the Viability model. It was originally developed for use evaluating using open source products, and your thresholds for each model category will vary based on your assumption of risk.

For example:

<ul class="wp-block-list">
  <li>
    Organizations starting their journey in governing Open Source Software at their organization usually start with Compliance and Security, cornering vulnerabilities and licensing information to choose their software.
  </li>
  <li>
    Large companies may consider strategy to be the next-most important. Given that many organizations build software that is in use for years, the importance of the strategy in a project &#8212; and indeed who maintains that strategy &#8212; can be a critical decision.
  </li>
  <li>
    Community is important for cutting-edge or newer implementations of technology. While older technology will likely have a less volatile community, where maintainers and flow of new contributions can be judged over time, a new project may need a stronger community with more vigilance on it&#8217;s competitors to ensure that a software stack isn&#8217;t abandoned.
  </li>
  <li>
    Governance is crucial for organizations that intend to engage the open source community; or contribute to a project to shape new functionality. If an organization is willing to commit time and resources to maintaining a project &#8212; the Governance of that project becomes important to consider
  </li>
</ul>

## Getting Started {.wp-block-heading}

Consult the documentation of [GrimoireLab][6] and [Augur][7] for more details on how to get started. Based on what your team needs or cares about, consider choosing the tool that has the highest coverage, or use them both to maximize your results. If you find that you can trace some metrics that I’ve gotten wrong here, I’d love to know! Drop by our OSPO working group, metrics working group, or somewhere else to publish your contributions!  
  
Until then, you can find me on CHAOSS community slack, as Gary White. Thanks for reading!

 [1]: https://unsplash.com/@williambout?utm_content=creditCopyText&utm_medium=referral&utm_source=unsplash
 [2]: https://unsplash.com/photos/gray-lighthouse-on-islet-with-concrete-pathway-at-daytime-7cdFZmLlWOM?utm_content=creditCopyText&utm_medium=referral&utm_source=unsplash
 [3]: https://chaoss.local/oss-viability-metric-supermodel/
 [4]: https://chaoss.local/viability-metrics-what-its-made-of/
 [5]: https://docs.google.com/document/d/1_5cMkDYmi7wvO8PV2ZUxme5je2Cxxskbs8dx8j9r79Q/edit#heading=h.iik92t6gkfct
 [6]: https://github.com/chaoss/grimoirelab
 [7]: https://github.com/chaoss/augur
 [8]: https://github.com/chaoss/grimoirelab-sigils
 [9]: https://github.com/oss-aspen/8Knot