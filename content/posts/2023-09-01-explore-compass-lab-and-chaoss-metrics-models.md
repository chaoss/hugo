---
title: Explore Compass Lab and CHAOSS Metrics Models
author:
  - ZhouRan
type: post
date: 2023-09-01T18:27:38+00:00
url: /explore-compass-lab-and-chaoss-metrics-models/
nectar_blog_post_view_count:
  - 2042
publish_post_category:
  - 5
ppma_authors_name:
  - ZhouRan
categories:
  - Blog Post
tags:
  - compass
  - metrics models

---
 

The following is a blog post from our friends in the [OSS Compass Project][1]. OSS Compass is a SaaS solution, hosted in China, that is built from CHAOSS GrimoireLab software and deploys CHAOSS metrics and metrics models. There is also a video demonstrating how Compass Lab works from our August 29, 2023, CHAOSS Metrics Models meeting. You can check out that video [here][2].

<hr class="wp-block-separator" />

## Explore Compass Lab, Making it easy to create an open source project evaluation model! {.wp-block-heading}

Hi, open source adventurers! Today, I&#8217;m here to introduce the latest marvel from the open source realm – the new darling of the OSS Compass (hereinafter referred to as &#8220;Compass&#8221;) world! Yes, you heard it right. It&#8217;s our new SaaS service – Compass Lab! Wait, you haven&#8217;t heard about it yet? Don&#8217;t worry, let me explain it all to you step by step. I promise it will leave you dazzled and excited!

In the world of open source, countless projects emerge every day. However, accurately measuring the health of an open source project remains a vexing challenge. Luckily, we have Compass, which is like a health check doctor for open source projects. And recently, a new member has joined – Compass Lab!

### 01🌟 What is Compass Lab? {.wp-block-heading}

Compass Lab is an incubator for open source community evaluation metric models. It might sound sophisticated, but actually it&#8217;s essentially a &#8220;health evaluation center&#8221; that provides a comprehensive checkup for open source projects. This evaluation center not only offers data but also serves as a platform filled with fun and creativity.

Compass Lab gathers an enormous amount of data from over 20,000 open source projects, offering more than 200 project categories and over 100 evaluation metrics. This means you can conduct an all-encompassing health assessment for a project – the possibilities are endless! You can select different evaluation metrics and datasets based on your needs, making it a paradise for assessment enthusiasts!

### 02🚀 How to &#8220;play&#8221; with Compass Lab? {.wp-block-heading}

It&#8217;s actually quite simple! First, you need to approach it with a curious mindset. Then, register and log in to the SaaS service platform of [Compass Lab][3], where you&#8217;ll discover a fascinating world. You can choose existing evaluation models or customize one based on your interests.

### ➤General Steps to Create a Model {.wp-block-heading}

### **1. Open the model creation page:** {.wp-block-heading}

On the [Compass official website][4], locate the model creation area on the right side of the Lab page and click “Create a model now”or use the button “Create a model”at the top.<figure class="wp-block-image">

<img decoding="async" src="https://chaoss.local/wp-content/uploads/2023/09/yaf7Bwg98ZOJnEbsXBKPHJhJlk4rmFLfqVchw7EyXE_ZlbZU6r36k60YvVtvqOWfbHM18z-ZSTMiAnMH5yYsV09qKCxVc01w7URkcmLSEaHHoR9rtSeXZiJrXaCzmzpg5zzOKInQ4W9zbro6s32GE3A.png" alt="" /> </figure> 

### **2. Fill in basic information:** {.wp-block-heading}

Provide basic model information, such as ecosystem dimension, model name, applicable industry, and whether it&#8217;s public or private.<figure class="wp-block-image">

<img decoding="async" src="https://chaoss.local/wp-content/uploads/2023/09/0Wo5Gvgowy576ha_zaeQWH3mmrm5i6ixE-70ciZmGLi35_A3YY8V3uK0uKMFA0_y3E2hgO2HSiSdk_wwBU79wlV0CfYDh5ahsq73apQeguiKaCWwifgF_qB_7_83eY0lPx8nu8tBbk6x7t4Uvpkc_Ak.png" alt="" /> </figure> 

### **3. Select datasets:** {.wp-block-heading}

Choose a dataset from the 200+ datasets that suits your needs, offering flexibility for various domains.<figure class="wp-block-image">

<img decoding="async" src="https://chaoss.local/wp-content/uploads/2023/09/0TGsqAGR1YNO4lQrRD-WwIIaoVJFdSI9MxPV6fQDaSCA4zkEka_W11EN52KoRUTZDcAskKnIIZp_cfzUQ_my7HNCvZugixYOBI5Rv62YV5H5oMiPmchjiepuKu2IYw7Ik0jXvHI1AYZbd8NJliYdbxg.png" alt="" /> </figure> 

### **4. Choose evaluation metrics:** {.wp-block-heading}

Select the metrics you care about from the 100+ metrics provided by CHAOSS and Compass, categorized by code, issues, pull requests, repositories, contributors, etc. And confirm your selection.<figure class="wp-block-image">

<img decoding="async" src="https://chaoss.local/wp-content/uploads/2023/09/BwjjJrlhAVNpoHhSQAknJmQTEaUGSa0w36gRob37niQRWy6VvgSO0WR5yg2cqXx9rJQI_5sN1hJIajWerkJjNr-XZ5seuPEb6yVsVn7D4Ftw7QnuZCyQYLtqFqc1bHRnuvlQQfwMrejizQf4IIav3n8.png" alt="" /> </figure> 

### **5. Adjust weights and thresholds:** {.wp-block-heading}

Next, modify weight values in the percentage input box or drag the slider to adjust weights (default is rightward only). Revise thresholds in the right input box (ensuring the values stay within the provided range). This process is similar to customizing your own pizza, adding toppings according to your taste!<figure class="wp-block-image">

<img decoding="async" src="https://chaoss.local/wp-content/uploads/2023/09/Wmo3QCBdIyygeVyccR7rqIY4RlEmLDKJFSstbTej_4LXw3dbWBgca8ME1fEr37wwINB1X02jSP-R_l-O2G2l946HTNY0kyLpTRUoQx4vizKfBh4TgJ23a2dGazwasn5C-MG0BlLDFJESD6wLx-Ws_Ts.png" alt="" /> </figure> 

### **6. Choose algorithms:** {.wp-block-heading}

Currently, we only support the default algorithm (as shown below), but don&#8217;t worry, it&#8217;s a remarkable algorithm crafted by the expert Rob Pike himself! For an in-depth understanding of this algorithm, refer to our previously released article &#8220;[OSS Compass Scoring System Switch：Watch Algorithms Transforming into Magic!][5]&#8221; If you have more thoughts on algorithms, join the [Compass Slack channel][6] to discuss with fellow open source adventurers.<figure class="wp-block-image">

<img decoding="async" src="https://chaoss.local/wp-content/uploads/2023/09/FBcO3x3laAPGAr62QZF1Np9vnXfBCCs6FQ5qrkDL5S0MqN2cn6WB5VYt7RCStf22HFwGveXOvogwVQsz6Qrr86xgXJ7o-Iq0XrzjaNmZTQYPpIDKV8yT_7TPybLhS8KWZpuMytF6kym2rqVpL-M68_Q.png" alt="" /> </figure> 

### **7. Publish the model:** {.wp-block-heading}

After confirming all the information, click “save” to publish the model.<figure class="wp-block-image">

<img decoding="async" src="https://chaoss.local/wp-content/uploads/2023/09/H-YsUNOpFvT2ZEAsfJVa6OBTkOLF3ykI4yUsJpN-m0IpeQn2uMHh7aagX7NxSb1_UDaDxop5FHXFHv-lTu1KUrWheS1m9v03L3CSmJ5OrSxJi6wwzfda4qS5Sp8x7_mcuBDbvSKONET8X8d4bkdTv-g.png" alt="" /> </figure> 

Next, let data and creativity collide here to create your own project health model!

### 03🌈 Your creativity finds a home here: creating a LLMs projects evaluation model! {.wp-block-heading}

Compass Lab not only offers general project evaluation models but also provides a special space for developers with unique ideas. If you have an extraordinary open source project and want to assign it a health score, this is the place for you! Here, you can customize an evaluation model for your project, allowing your creativity to soar!

For example, if you&#8217;re interested in open source LLMs projects or have your own open source LLMs project, you can create an evaluation model for it:

### ➤Steps for creating an LLMs projects evaluation model {.wp-block-heading}

### **1. Give your model a catchy name:** {.wp-block-heading}

Besides naming, remember to choose whether it&#8217;s for a general or specific domain and whether you&#8217;re willing to make the model public.<figure class="wp-block-image">

<img decoding="async" src="https://chaoss.local/wp-content/uploads/2023/09/WGZav9GLmwxZ3diRtkZJEJqm1RWQe9hTJ_m7HcboFPlGRnXBQnLV3AntN4NbFBI2y1EtCcFCZirJXM3wYBB6m8KKzqUpZxpS2fq4K3MRSxgGaFgqd7RkywA0zn2S8qm3wi8bYlfyPUPBaz9dPlVbFWU.png" alt="" /> </figure> 

### **2. Select datasets:** {.wp-block-heading}

Choose projects under the categories of open source LLMs and open source LLMs tools to facilitate cross-category comparisons. (Our dataset is continuously expanding!)<figure class="wp-block-image">

<img decoding="async" src="https://chaoss.local/wp-content/uploads/2023/09/jbfFaOuM_wtW9tHffzvzR27aXVioGQO8Z9_KffeGsnQ3KG6J6fz-zXCcM2T84meE-Am0d-94Vfx51M6Rob2Iaj8unMgcXuyWhZvQq6wlqW8nNYA3QDjJP3VGf2vBiEp0AQjU3U6pcqoUOCHzyQ11jgY.png" alt="" /> </figure> 

### **3. Choose metrics and adjust weights and thresholds:** {.wp-block-heading}

Select appropriate metrics based on the characteristics of open source LLMs projects, such as organization count, code commit frequency, ongoing contributions, etc.&nbsp;<figure class="wp-block-image">

<img decoding="async" src="https://chaoss.local/wp-content/uploads/2023/09/IniqFFYTunaCl2ao5DgsXOuIdoCVr0pq197KrYgF82xXvBuNuIvlR84KO7y-Sjj0klTA3pfXiiibmJmjYwgh7TzQ5gOw_TRsqneXvwn2spcV2rA5V2_EGYZHD5sNHBewrPPdvnecBxDuig3k2B72g1c.png" alt="" /> </figure> 

Adjust weights and thresholds for each metric following the previously demonstrated steps.

Then, click “save” and the model is created.

### **4. Analyze and view assessment results:** {.wp-block-heading}

Click &#8220;Analyze&#8221; and wait for it to complete – then you can view the assessment report.<figure class="wp-block-image">

<img decoding="async" src="https://chaoss.local/wp-content/uploads/2023/09/pnx0GoBfy-Hkk_n_XpMh_xM3afO3OTNnRmD6aP9BG480Jq4Mtx8C06gMZtNoCyeNPDI5dDkdUdO-fok5kuP3jnA5GoYPT3G0lZ8nBEBh8t4HfWSC2l5aRydm7pZxuKoFhZxuZFM0Ws01NtYyGvhLWgE.png" alt="" /> </figure> 

### **5. Add comments:** {.wp-block-heading}

In addition, we&#8217;ve added a comment feature to the dashboard page. Click the comment button in the upper right corner to share your thoughts.<figure class="wp-block-image">

<img decoding="async" src="https://chaoss.local/wp-content/uploads/2023/09/1SDY_ajsVPYix31xyBANyDjzocoI6XhFvx3-OEzgn21whl0-4Ip__QaLdjH6qFEr3aXe45zKLF92B54jTLu4RIpKC8kU1poffDOIYkHAJj5E9GnAuugKYctiDashTEpvtH6ysXF6pKccp3axtlWFvpA.png" alt="" /> </figure> 

### **6. Invite friends to collaborate:** {.wp-block-heading}

You can also invite friends to collaborate and help you create a more perfect model. Just click &#8220;Member&#8221; on the model page, set collaboration permissions, and send invitations!<figure class="wp-block-image">

<img decoding="async" src="https://chaoss.local/wp-content/uploads/2023/09/OQtcTQpfibu8f_7DOIyn5eAS8UyB8dVv1g_8y6zkz9vcg2lSAwBoQQCgtat6pTcGdpIl18DlDkpguTUl-nuYRGA7UzMsD0S7h9P3A7fbPnZcxHAdB49w_Dfh3QfzFUmZypL6ivxOaJCmmV0XIeBfRgg.png" alt="" /> </figure> <figure class="wp-block-image"><img decoding="async" src="https://chaoss.local/wp-content/uploads/2023/09/Zq93Pmgx6TOiRAQT-a6vim3FU-4WVhYq9GBNkCnIrd2nNORAEcJWI_PQKaetQyXQkdjwhXuMyLvkalLmCR5AIBOE23UHHd5C6w5h1JDbxw4yO1JadzRBdOMF6b-xrECSqY3CrSSfPco_2HmH46z-s.png" alt="" /></figure> 

### 04🌟 Explore limitless fun in the open source world, all in Compass! {.wp-block-heading}

Through today&#8217;s introduction, I believe you now have a deeper understanding of Compass Lab. Here, you can not only explore various dimensions of open source projects but also customize evaluation models for your own ideas, combining creativity and data. This &#8220;evaluation playground&#8221; in the open source world awaits your participation!&nbsp;

If you haven&#8217;t experienced Compass Lab yet, take action now! Refer to below operation demonstration and create your evaluation model! Let&#8217;s explore the boundless fun of the open source world together, and unravel the mysteries of data!&nbsp;<figure class="wp-block-image">

<img decoding="async" src="https://chaoss.local/wp-content/uploads/2023/09/0ECYdhDrQPp9hFj_Fw0GynUbFi83OrR_h4AbHcNkBErRaVgqy0hWzg5J_EN6x6srmDGS9CSCH_4GJzqJIubx6vII1wuWOJvTHDi8rDUZp3UIHB2a11L6o0YUDLLP-OtiIu9rG3fmIPYikDvhbrI39nE.gif" alt="" /> </figure> 

Remember to stay tuned for more interesting tech news and creative activities. Until next time, let&#8217;s embark on an infinite journey of open source creativity together!

## **Join OSS Compass Community** {.wp-block-heading}

In the future, OSS Compass will continue to evolve and give back to the broader user base, providing greater convenience for open source project evaluation and assisting in the healthy and sustainable development of open source communities.

We look forward to more developers joining the OSS Compass community and contributing to its development. At the same time, we welcome users to continue using Compass SaaS services and providing feedback, continuously powering the enhancement of OSS Compass&#8217;s capabilities.<figure class="wp-block-image">

[<img decoding="async" src="https://chaoss.local/wp-content/uploads/2023/09/7U_elfeQfgkMvAtbVsfk6Flu5JUX1GRXFzz2bX8SJfJYlBdp6hxwCD6uS-uwNmunz9wcvhKFvv02CDq8zB49KBOCl183yMBTRisaoe986PmVzrBkHtgnEvnhpmRppVMuoZGXqWjDG8bXKMaiJ5jAmIk.jpg" alt="image2.png" />][7]<figcaption><https://join.slack.com/t/oss-compass/shared_invite/zt-1ttt9sv5h-8E~oPP6VJqm8ero5qH9LlA></figcaption></figure> 

&nbsp;

 [1]: https://oss-compass.org
 [2]: https://www.youtube.com/watch?v=YErpyXkSrN8
 [3]: https://oss-compass.org/lab
 [4]: https://oss-compass.org/
 [5]: https://oss-compass.org/blog/scoring-system-switch
 [6]: https://app.slack.com/client/T046XT1LUHG/C046HATH6MV
 [7]: https://join.slack.com/t/oss-compass/shared_invite/zt-1ttt9sv5h-8E~oPP6VJqm8ero5qH9LlA