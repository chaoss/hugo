---
title: 'Viability: An Open Source CHAOSS Metric (Super)Model'
author:
  - Gary White
type: post
date: 2023-12-01T13:09:09+00:00
url: /oss-viability-metric-supermodel/
nectar_blog_post_view_count:
  - 4170
ppma_authors_name:
  - Gary White
categories:
  - Blog Post
tags:
  - metrics
  - viability

---
 

_This post is part of a three part series. This is part one. Stay tuned to the CHAOSS blog for a deep dive into the metrics around Viability, and a guide on how we can use this model._

Companies who use open source software (so, all of them) have been thinking more and more about bills of material, vulnerabilities, and license risks. This has especially been encouraged through recent [United States efforts][1] regarding Software Bills of Material (SBOM’s). This push is a good opportunity to observe and report on software supply chains. We can all learn a lot from knowing what’s in our software dependencies! Proliferation of [SBOM’s][2], [SAST][3], and [SCA][4] scanning tools allows for users and developers of software everywhere to better understand their risk portfolio. Most people find significant value by using these reports to surface critically important vulnerabilities and license information.&nbsp;

## Choosing and Updating Components {.wp-block-heading}

When Verizon, and the OSPO within, looked through our own SBOM’s and assessed which dependencies we should update. We found that common practice sparsely dictates relative priority. Barely any priority is set as industry practice for updating dependencies. Outside of CVE’s (with their own criticality rating), and licensing resolution (usually a hard yes/no from legal teams). Old dependencies without any open vulnerabilities are regularly put behind new features and critical breakages. That felt **wrong** to us. Over time, dependencies that had “never needed updating&#8221; find themselves painfully entrenched in our applications. When they _do_ need upgrading the effort to do so can take dramatic time away from other development. We thought for sure, there has to be a way to identify (and reduce) that risk.

<div class="wp-block-image is-style-default">
  <figure class="aligncenter size-large is-resized"><img loading="lazy" decoding="async" src="{{ baseURL }}wp-content/uploads/2023/11/zaini-izzuddin-55btQzyDiO8-unsplash-768x1024.jpg" alt="" class="wp-image-5468" width="649" height="867" srcset="{{ baseURL }}wp-content/uploads/2023/11/zaini-izzuddin-55btQzyDiO8-unsplash-225x300.jpg 225w, {{ baseURL }}wp-content/uploads/2023/11/zaini-izzuddin-55btQzyDiO8-unsplash-200x267.jpg 200w" sizes="auto, (max-width: 649px) 100vw, 649px" /><figcaption><em>A visual representation of open source libraries available to accomplish a minor engineering task</em><br />Photo by <a href="https://unsplash.com/@izzuddindanial?utm_content=creditCopyText&utm_medium=referral&utm_source=unsplash">Zaini Izzuddin</a> on <a href="https://unsplash.com/photos/books-on-shelves-55btQzyDiO8?utm_content=creditCopyText&utm_medium=referral&utm_source=unsplash">Unsplash</a></figcaption></figure>
</div>

What else should we be looking for in our open source software **choices**? What guidance can we give to encourage good decisions not just when maintaining software? Should that guidance be different than when people decide on software to use? Software technologists regularly make decisions about which software they should use in their project. Rarely is this done with an SCA tool, SAST tool, or an SBOM. Could we provide tools and metrics to guide decisions? How can we create less risk in our choices, providing more sustainable software infrastructure? From these question we set to develop a model to make sense of the complexity.

## More than Vulnerabilities and Licensing {.wp-block-heading}

Enter: Viability. Metrics (and [metrics models][5]) about open source projects. These provide insight into the [Community][6], [Strategy][7], [Governance][8], and [Compliance/Security][9] of open source projects.&nbsp; This series of blog posts will cover the motivation and background, what metrics are included in the model, and finally how we can use those metrics to measure Viability in OSS. Viability is built with metrics [detailed by CHAOSS][10], as CHAOSS has spent a while talking about how to make these metrics serviceable and understandable for technologists across geography and industry focus.&nbsp;

For brevity and focus Viability is split into four [metrics models][5]: Community, Strategy, Governance, and Compliance + Security. The individual value proposition of metrics per model is best described in their respective pages. The whole includes many metrics, and some overlap per sub-model. We did this so they may be used independently or in concert for a full picture of viable open source projects. We recommend using all of the models together, but mixing and matching them is also expected and appropriate.

The application of these metrics at Verizon allows us to operationalize tasks for choosing and maintaining software. While evaluating dependencies, engineers have a better idea of what parts of an open source project excel, and what may fall short. Depending on the application intended, OSPOs and application teams can decide if the risk is worth taking on a project together.&nbsp;

Viability provides direction to what dependencies should be updated. Instead of lumping old dependencies into a ball of vague “technical debt”, we can estimate the fit of community, strategy, governance, and compliance / licensing against a particular project. We can also approximate the risk of **not** addressing projects in a way that is quantifiable to stakeholders; and in review of priorities.

## Thanks, and come see us! {.wp-block-heading}

I’m excited to share this model with everyone; it’s been a while in the making. Be part of the next project, ask questions, and get involved with CHAOSS working group by dropping into the [CHAOSS slack channel.][11] You can ping me (Gary White!) while you’re there.

 [1]: https://www.federalregister.gov/documents/2021/05/17/2021-10460/improving-the-nations-cybersecurity
 [2]: https://en.wikipedia.org/wiki/Software_supply_chain
 [3]: https://en.wikipedia.org/wiki/Static_application_security_testing
 [4]: https://en.wikipedia.org/wiki/Software_composition_analysis
 [5]: {{ baseURL }}kbtopic/all-metrics-models/
 [6]: {{ baseURL }}kb/metrics-model-oss-project-viability-community/
 [7]: {{ baseURL }}kb/metrics-model-oss-project-viability-strategy/
 [8]: {{ baseURL }}kb/metrics-model-oss-project-viability-governance/
 [9]: {{ baseURL }}kb/metrics-model-oss-project-viability-compliance-security/
 [10]: {{ baseURL }}kbtopic/all-metrics/
 [11]: https://join.slack.com/t/chaoss-workspace/shared_invite/zt-1fah5gu35-5oUQEPT32O2Zt~3MFVNMlw