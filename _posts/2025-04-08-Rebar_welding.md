---
title: "Which Is Better for Reducing Domain Gap: Point Clouds or RGB?"
layout: splash
date: 2026-01-21
header:
  overlay_color: "#000"
  overlay_filter: "0.5"
  overlay_image: /web_resources\post\Rotate-ICP\Snipaste_2026-01-21_12-38-27.png
  actions:
    - label: "Video"
      url: "https://www.youtube.com/watch?v=uixmualasgU"
    - label: "Dataset"
      url: "https://github.com/mmistakes/minimal-mistakes/"
excerpt: "We propose a geometry-driven, domain-gap-free framework for automated rebar cage welding that eliminates manual annotation by generating labels directly from real-world RGB-D scans. By exploiting geometric priors and symmetric pose reasoning, the system achieves 99.12% segmentation and 98.30% welding success."


categories: 
  - Tutorial
---

<div style="text-align: center; line-height: 1.3; margin-bottom: 20px;">
  <p style="font-size: 28px; font-weight: bold; margin: 0 0 10px 0;">
    Domain-Gap-Free Automatic Real-world Point Cloud Annotation for Tie Bar Welding in Complex Rebar Joint
  </p>

  <p style="margin: 0 0 5px 0;">
    Lu Deng, Yu Dai, <strong>Huiguang Wang<sup>*a</sup></strong>,<br>
    College of Civil Engineering, Hunan University<br>
    * Corresponding author: whg0917@hnu.edu.cn
  </p>

  <div style="display: flex; justify-content: center; align-items: center; width: 400px; margin: 0 auto;">
    <a href="https://www.hnu.edu.cn/" target="_blank">
      <img src="/web_resources/Hunan_University.svg" style="width: 200px; height: auto; margin-bottom: 10px;" />
    </a>
    &nbsp;&nbsp;&nbsp;&nbsp;
    <a href="https://www.dengteam.com/index.php?m=content&c=index&a=show&catid=70&id=251" target="_blank">
      <img src="/web_resources/dengteam.png" style="width: 200px; height: auto; margin-bottom: 10px;" />
    </a>
  </div>
</div>


<div style="text-align: center; margin-bottom: 15px;">
  <p style="font-size: 28px; font-weight: bold; margin: 0;">
    Background & Methodology
  </p>
</div>




<div style="text-align: center;">
  <p style="font-size: 30px; font-weight: bold;">
    Abstract
  </p>
</div>

<div style="text-align: justify;">
  <p style="margin-top: 10px;">The automation of rebar cage welding is challenged by the geometric complexity of joints with tie bars and the prohibitive labor costs associated with annotating real-world datasets. To overcome these challenges, this paper proposes a geometry-driven, domain-gap-free perception and execution framework. Specifically, an automated annotation pipeline generates training labels directly from real-world RGB-D scans. By integrating density-based heatmap analysis for regions of interest localization and local density statistics, the system accurately distinguishes complex joints from standard X-type joints, thereby automatically selecting target ROIs. Leveraging inherent longitudinal-transverse geometric priors, background structures are explicitly modeled and subtracted to extract valid instances. Furthermore, to resolve pose ambiguities caused by geometric symmetry, a symmetric candidate pose strategy is introduced that accounts for multiple feasible tie bar orientations. Experiments demonstrate a 99.12% segmentation success rate and a 98.30% welding success rate, validating the proposed methods.
  </p>
  <p><strong>Keywords:</strong> Robotic welding; Rapid annotation; Instance segmentation; Symmetry issue
  </p>
</div>

