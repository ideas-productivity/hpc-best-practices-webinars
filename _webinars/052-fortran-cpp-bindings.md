---
webinar-id: 52
date: 2021-05-12T13:00-0400
title: "Automated Fortran–C++ Bindings for Large-Scale Scientific Applications"
presenter-ids: [johnson-seth]
registration-url: https://exascaleproject.zoomgov.com/meeting/register/vJItdOugqDwsH-ickhvZjTXVfYMkLFBDzvc
ecp-abbreviation: fortran-cpp-bindings
qa-public-url: http://bit.ly/HPCBP-QA
survey-public-url: http://bit.ly/HPCBP-survey-210512
artifacts:
  - label: Recording
    format: YouTube
    yt-video-id: pNGsLxm69r8
  - label: Slides
    format: PDF
    url: http://ideas-productivity.org/wordpress/wp-content/uploads/2021/05/hpcbp052-fortran-cpp-bindings.pdf
  - label: Q&A
    format: PDF
    url: http://ideas-productivity.org/wordpress/wp-content/uploads/2021/05/hpcbp052-fortran-cpp-bindings-qa.pdf
---
Although many active scientific codes use modern Fortran, most contemporary scientific software libraries are implemented in C and C++. Providing their numerical, algorithmic, or data management features to Fortran codes requires writing and maintaining substantial amounts of glue code. In the same vein, some projects are actively moving key kernels from Fortran toward C++ to support performance portability models and other rapidly-developing, dynamic programming paradigms. How can a project smoothly connect existing Fortran code to new internal C++ kernels or external C++ libraries? SWIG-Fortran provides a solution with a wide range of flexibility, including support for performant data transfers, MPI support, and direct translation of C++ features to Fortran interfaces.
