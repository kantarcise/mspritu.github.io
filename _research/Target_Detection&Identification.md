---
title: "Target Detection & Identification"
collection: research
type: "Research"
permalink: /research/Target_Detection&Identification
venue: "UC San Francisco, Department of Testing"
date: 2012-03-02
location: "San Francisco, California"
---

Fixed rate state space models are the conventional models used to track the maneuvering objects.
In contrast to fixed rate models, recently introduced variable rate particle filter (VRPF) is capable
of tracking the target with a small number of states by imposing a Gamma distribution on the state
arrival times while the object trajectory is approached by a single dynamic motion model. Using a
single dynamic motion model limits the capability of estimating the characteristics of maneuvering
and smooth regions of the trajectory. To overcome this weakness we introduce an adaptive tracking
method which incorporates multiple model approach with the variable rate model structure. The proposed
model referred to as multiple model variable rate particle filter (MM-VRPF) adaptively locates frequent
state points to the maneuvering regions resulting in a much more accurate tracking while preserving the
parsimonious representation for the smooth regions of the trajectory. This is achieved by including a mode
variable into the conventional variable rate state vector that enables us to define different sojourn and
motion parameters for each motion mode using the multiple model structure. Simulation results show that the
proposed algorithm outperforms the conventional variable rate particle filter, fixed rate multiple model
particle filter and interacting multiple model.
