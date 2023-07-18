---
webinar-id: 73
date: 2023-04-12T13:00-0400
title: "Facilitating Electronic Structure Calculations on GPU-based Exascale Platforms"
presenter-ids: [fattebert-jeanluc]
topics: ["software engineering",  "high-performance computing (hpc)", "performance at leadership computing facilities", “online learning”]
registration-url: https://exascaleproject.zoomgov.com/meeting/register/vJIsdu2trz4oHcvHfBiEco7RFJzPWwNfh3E
ecp-abbreviation: copa
qa-public-url: http://bit.ly/HPCBP-QA
survey-public-url: http://bit.ly/HPCBP-feedback
artifacts:
  - label: Recording
    format: YouTube
    yt-video-id: T5JInOIMcdw
  - label: Slides
    format: PDF
    url: http://ideas-productivity.org/wordpress/wp-content/uploads/2023/04/hpcbp-073-copa.pdf
  - label: Q&A
    format: PDF
    url: http://ideas-productivity.org/wordpress/wp-content/uploads/2023/04/hpcbp-073-qa.pdf
---
GPUs accelerators offer the prospect of speeding up ab initio molecular dynamics and other large-scale first-principles atomistic simulations. Taking advantage of these devices is, however, not a trivial task given their specificities. Some algorithms struggle, while others thrive with the high level of thread concurrency available on modern GPUs. The PROGRESS and BML libraries, developed within ECP’s Co-design Center for Particle Applications (CoPA) project, allow electronic structure codes to offload their most expensive kernels, with a unified interface for various matrix formats and computer architectures. The webinar will focus on implementations and algorithmic choices made in those libraries, and lessons learned while trying to achieve performance portability on exascale platforms. Specifically, the webinar will discuss eigensolvers and their alternatives, as well as strong scaling in fast time-to-solution in molecular dynamics.
