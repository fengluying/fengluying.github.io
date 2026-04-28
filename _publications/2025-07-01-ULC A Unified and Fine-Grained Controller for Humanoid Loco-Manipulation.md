---
title: "ULC: A Unified and Fine-Grained Controller for Humanoid Loco-Manipulation"
collection: publications
permalink: /publication/2025-07-01-ULC-A-Unified-and-Fine-Grained-Controller-for-Humanoid-Loco-Manipulation
excerpt: 'Presents a unified and fine-grained controller for humanoid loco-manipulation. (Co-first author, second listed)'
date: 2025-07-01
venue: 'In submission'
paperurl: 'https://arxiv.org/abs/2507.06905'
citation: 'Sun W*, Feng L*, Baoshi Cao, et al. "ULC: A Unified and Fine-Grained Controller for Humanoid Loco-Manipulation."'
year: 2025
in_submission: true
preview_video: /images/publications/ULC/ulc.mp4
preview_image: /images/publications/ULC/ulc.jpg
---

## Abstract
Loco-manipulation for humanoid robots aims to enable robots to integrate mobility with upper-body tracking capabilities. Most existing approaches adopt hierarchical architectures that decompose control into isolated upper-body (manipulation) and lower-body (locomotion) policies. While it reduces training complexity, this decomposition inherently limits coordination between subsystems and contradicts the unified whole-body control exhibited by humans. We demonstrate that a single unified policy can achieve a combination of tracking accuracy, large workspace, and robustness for humanoid loco-manipulation. We propose a Unified Loco-Manipulation Controller (ULC), a single-policy framework that simultaneously tracks root velocity, root height, torso rotation, and dual-arm joint positions in an end-to-end manner, demonstrating the feasibility of unified control without sacrificing the performance. We achieve this unified control through integrating a set of key technologies, including sequential skill acquisition for progressive learning complexity, residual action modeling for fine-grained control adjustments, command polynomial interpolation for smooth motion transitions, random delay release for robustness to deploy variations, load randomization for generalization to external disturbances, and center of mass tracking for providing explicit policy gradients to maintain stability. We validate our method on the Unitree G1 humanoid robot with a three-degrees-of-freedom waist. Compared with the state-of-the-art, ULC shows better tracking performance than disentangled methods and demonstrates larger workspace coverage. The unified dual-arm tracking enables precise manipulation under external loads while maintaining coordinated whole-body control for complex loco-manipulation tasks. The code and videos are available on our project website at [https://hellod035.github.io/ULC/](https://hellod035.github.io/ULC/).

<div style="display:flex;justify-content:center;">
  <video width="700" autoplay muted loop playsinline controls preload="metadata">
    <source src="/images/publications/ULC/ulc.mp4" type="video/mp4">
    Your browser does not support the video tag.
  </video>
</div>

