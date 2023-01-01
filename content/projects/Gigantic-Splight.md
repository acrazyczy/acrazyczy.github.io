---
title: "Gigantic Splight"
date: 2022-06-12T16:44:39+08:00
description: CS403 homework in ACM 2019 class, a 3D fluid simulation project based on Taichi framework. Several fun ways of interactions are combined.
authors: [ziyi-cai, yechen-xu, lejun-min]
tags: [computer graphics, fluid simulation, taichi, course projects]
categories: [projects]
featuredVideo: https://www.youtube.com/embed/yLRa-U5cDIQ 
draft: false
---
Fluid simulation has been a challenge in Computer Graphics domain. In this project we implemented Macklin and Müller’s algorithm specified in their paper [Macklin and Müller 2013](https://mmacklin.com/pbf_sig_preprint.pdf). To achieve real-timeness, we utilized Taichi framework to render the fluid in real time, which is proven to be robust and handy comparing to CUDA programming. We also raised several interactive ways to enhance its playability. In order to have a better realistic view, foam simulation is also added into our scene. Generally, our work can be regarded as a re-implementation of the algorithm with augmentations in rendering, gaming and interaction. In the end, we also prove with statistics that the algorithm is efficient and robust.

You can find our midi paper [here](https://github.com/PorygonGroup/Gigantic-Splight/blob/master/Simulating_Particle_Based_Fluids.pdf). Our code can be found [here](https://github.com/PorygonGroup/Gigantic-Splight/).
