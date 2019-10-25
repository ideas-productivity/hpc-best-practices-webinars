---
webinar-id: 25
date: 2019-01-23T13:00-0500
title: "Quantitatively Assessing Performance Portability with Roofline"
presenter-ids: [pennycook-john, yang-charlene, deslippe-jack]
archives:
  - label: Recording
    format: YouTube
    yt-video-id: 2OvsMUQ2mj8
  - label: Slides
    format: PDF
    url: http://ideas-productivity.org/wordpress/wp-content/uploads/2019/02/webinar025-perfport.pdf
  - label: Q&A
    format: PDF
    url: http://ideas-productivity.org/wordpress/wp-content/uploads/2019/02/webinar025-qa.pdf
---
 Wouldn’t it be great if we could port a code to a new
 high-performance architecture without substantially changing the code
 yet achieving a similar level of performance as hand-optimized code?
 This webinar will frame the discussion around ‘performance
 portability’, why it is important and desirable, and how to
 quantitatively measure it. The webinar will start with a background
 check on how the concept of performance portability came about and
 past attempts to define it and quantify it. Then we will introduce a
 simple yet powerful metric and an empirical methodology to
 quantitatively assess a code’s performance portability across
 multiple platforms. The methodology uses the Roofline performance
 model to measure an ‘architectural efficiency’ term in the metric
 proposed by Pennycook et al. We will dive into a few nuances of this
 methodology, for example, how and why empirical ceilings should be
 used for performance bounds, how to accurately account for complex
 instructions such as divides, how to model strided memory accesses,
 and how to select the appropriate Roofline ceilings and application
 performance points to make sure that the performance portability
 analysis is not erroneously skewed. We will also show some results of
 measuring performance portability using the aforementioned metric and
 methodology on two modern architectures, Intel Xeon Phi and NVIDIA
 V100 GPUs.
