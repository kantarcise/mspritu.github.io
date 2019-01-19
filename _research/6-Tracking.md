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

<!--- A quick demo can be seen here.
#[![Ball Movement](files/ball2.gif)](https://www.youtube.com/watch?v=B8EGeEquzGI&t=0s&list=PLMzonaXew-57RYoqFr4-sGbkdnUkHnqg3&index=2)
-->
[The playlist to our videos showing results can be found here.](https://www.youtube.com/playlist?list=PLMzonaXew-57RYoqFr4-sGbkdnUkHnqg3 "Youtube Page")


MM - VRPF
======

Fixed rate state space models are the conventional models used to track the maneuvering objects.
In contrast to fixed rate models, recently introduced variable rate particle filter (VRPF) is capable
of tracking the target with a small number of states by imposing a Gamma distribution on the state
arrival times while the object trajectory is approached by a single dynamic motion model. Using a
single dynamic motion model limits the capability of estimating the characteristics of maneuvering
and smooth regions of the trajectory. To overcome this weakness we introduce an adaptive tracking
method which incorporates multiple model approach with the variable rate model structure.

The proposed model referred to as multiple model variable rate particle filter (MM-VRPF) adaptively locates frequent
state points to the maneuvering regions resulting in a much more accurate tracking while preserving the
parsimonious representation for the smooth regions of the trajectory. This is achieved by including a mode
variable into the conventional variable rate state vector that enables us to define different sojourn and
motion parameters for each motion mode using the multiple model structure. Simulation results show that the
proposed algorithm outperforms the conventional variable rate particle filter, fixed rate multiple model
particle filter and interacting multiple model.
