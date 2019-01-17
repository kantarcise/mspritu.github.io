---
title: "Object Tracking by Integrating PF Trackers with Deep Object Detectors "
collection: research
type: "Research"
permalink: /research/tracking
---

We pursue our research on Tracking-by-Detection (TbD) such by improving the tracking performance of particle filter trackers and object detection performance of deep object detectors. 


IDPF - RP
======

IDPF-RP (interleaving deep learning and particle filtering by region proposal suppression) is a tracking-by-detection (TBD) method that aims to combine the strengths of discriminative (deep detector) and generative frameworks (particle filter) to fulfill the requirements of efficient tracking. Firstly, region proposal alignment (RPA) that indicates low level decision fusion, eliminate unqualified region proposals that highly improves the localization accuracy. At the upper level, a decision level fusion scheme that interleaves variable rate color based particle filter (VRCPF) with Mask R-CNN resulting in an improved object tracking accuracy is proposed. This provides adaptively update the target model that improves robustness to appearance changes arising from high motion and occlusion.

 

Overall tracking performance of IDPF-RP is reported on 37 videos of the VOT2016 benchmarking data set.  IDPR-RP highly improves the localization accuracy of tracking particularly under size, illumination appearance and motion change, because of the superior localization capability of deep detector. It also provides the highest success rate and outperforms the top trackers of benchmarking.

[The link to our videos showing results can be found here.](https://www.youtube.com/playlist?list=PLMzonaXew-57RYoqFr4-sGbkdnUkHnqg3 "Youtube Page")
