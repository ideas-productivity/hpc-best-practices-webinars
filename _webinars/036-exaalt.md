---
webinar-id: 36
date: 2020-01-15T13:00-0500
title: "Refactoring EXAALT MD for Emerging Architectures"
presenter-ids: [thompson-aidan, moore-stan, gayatri-rahulkumar]
registration-url: https://www.eventbrite.com/e/refactoring-exaalt-md-for-emerging-architectures-tickets-85789477637
ecp-abbreviation: exaalt-md
---
As part of the DOE Exascale Computing Project, members of the EXAALT project are working to increase the accuracy, time, and length scales of molecular dynamics simulations of materials for fusion energy. Simulations rely on the SNAP machine-learning interatomic potential to accurately capture material properties. The SNAP kernel recursively evaluates a set of complex polynomial functions, requiring many deeply nested loops with irregular loop bounds. Last year, a worrisome trend in the SNAP force kernel was identified. With each new generation of emerging architectures, performance relative to theoretical peak was decreasing, particularly on GPUs. This webinar will discuss the approach used to rewrite the SNAP kernel from the ground up, using more compact memory representation, refactoring the main loop, using sub-kernels to reduce pressure on GPU threads, and improving coalesced memory accesses on the GPU. This work has enabled a spectacular increase of roughly 10x in performance over the baseline implementation of the SNAP benchmark running on NVIDIA V100 GPUs. Extrapolated to the full machine, this predicts an increase of over 100x in the Figure of Merit over the baseline on the ALCF/Mira system, putting EXAALT on track to meeting, and even exceeding performance targets on exascale systems. The webinar will emphasize key strategies and lessons learned in code transitions for emerging architectures.
