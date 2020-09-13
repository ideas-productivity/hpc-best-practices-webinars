---
webinar-id: 45
date: 2020-10-14T13:00-0400
title: "Scalable Precision Tuning of Numerical Software"
presenter-ids: [rubiogonzalez-cindy]
registration-url: https://exascaleproject.zoomgov.com/meeting/register/vJIsfuGoqDkjGLi_8sVyWQSFEsaXHEL6EM4
ecp-abbreviation: scalableprecisiontuning
#vtc-url: https://exascaleproject.zoomgov.com/s/1615639477 
#vtc-session: "161 563 9477"
qa-public-url: http://bit.ly/HPCBP-QA
#survey-public-url: https://www.surveymonkey.com/r/8MVC5Q6
#archives:
#  - label: Recording
#    format: YouTube
#    yt-video-id: 4VgdwL01ClM
#  - label: Slides
#    format: PDF
#    url: http://ideas-productivity.org/wordpress/wp-content/uploads/2020/07/webinar043-spack.pdf
#  - label: Q&A
#    format: PDF
#    url: http://ideas-productivity.org/wordpress/wp-content/uploads/2020/07/webinar043-spack-qa.pdf
---
The use of numerical software has grown rapidly over the past few years, providing the foundation for a large variety of applications including scientific software and machine learning. Given the variety of numerical errors that can occur, floating-point programs are difficult to write, test and debug. One common practice among developers is to use the highest available precision when allocating variables. While more robust, this can degrade program performance significantly. This webinar describes our research on developing tools to assist programmers in tuning the precision of their floating-point programs. These tools conduct a data-driven approach to search over the types of floating-point variables to lower their precision subject to accuracy constraints and performance goals. In the last part of the webinar, I will discuss challenges and opportunities for scalable precision tuning of large HPC applications.