---
title: "Which Is Better for Reducing Domain Gap: Point Clouds or RGB?"
layout: splash
date: 2026-01-21
header:
  overlay_color: "#000"
  overlay_filter: "0.1"
  overlay_image: /web_resources/post/Rotate-ICP/highlight.gif
  actions:
    - label: "Code"
      url: "https://github.com/huiguangwang"
    - label: "Dataset"
      url: "https://github.com/huiguangwang"
    - label: "Video"
      url: "https://www.youtube.com/watch?v=uixmualasgU"
excerpt: "We propose a geometry-driven, domain-gap-free framework for automated rebar cage welding that eliminates manual annotation by generating labels directly from real-world RGB-D scans. By exploiting geometric priors and symmetric pose reasoning, the system achieves 99.12% segmentation and 98.30% welding success."


categories: 
  - Tutorial
---

<div style="text-align: center; line-height: 1.3; margin-bottom: 20px;">
  <p style="font-size: 28px; font-weight: bold; margin: 0 0 10px 0;">
    Geometry-driven Automatic Point Cloud Annotation for Tie Bar Welding in Complex Rebar Joint
  </p>

  <p style="margin: 0 0 5px 0;">
    Lu Deng, Yu Dai, <strong>Huiguang Wang<sup>*</sup></strong>, Peng Shi, Mi Liu, Jiayao Zou<br>
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





<div style="text-align: center;">
  <p style="font-size: 30px; font-weight: bold;">
    Abstract
  </p>
</div>

<div style="text-align: justify;">
  <p style="margin-top: 10px;">The automation of rebar cage welding is challenged by the geometric complexity of joints with tie bars and the prohibitive labor costs associated with annotating real-world datasets. To overcome these challenges, this paper proposes a geometry-driven perception and execution framework. Specifically, an automated annotation pipeline generates training labels directly from real-world RGB-D scans. By employing a heatmap-based mechanism for global ROI localization and classification, the system accurately distinguishes complex joints from standard X-type joints via local density statistics, thereby automatically providing valid candidate regions for data labeling. Leveraging inherent longitudinal-transverse geometric priors, background structures are explicitly modeled and subtracted to extract valid instances. Furthermore, to resolve pose ambiguities caused by geometric symmetry, a symmetric candidate pose strategy is introduced that accounts for multiple feasible tie bar orientations. Experiments on real-world data demonstrate a 99.12% segmentation success rate and a 98.30% welding success rate, validating the proposed methods.
  </p>
  <p><strong>Keywords:</strong> Robotic welding; Rapid annotation; Instance segmentation; Symmetry issue
  </p>
</div>

<div style="text-align: center; margin-bottom: 15px;">
  <p style="font-size: 28px; font-weight: bold; margin: 0;">
    Background
  </p>
</div>

<div style="display: flex; justify-content: center; align-items: center; margin: 0 auto;">
  <img src="/web_resources\post\Rotate-ICP\bg.png" style="max-width: 100%; height: auto; margin-bottom: 10px;" />
</div>


<div style="text-align: center; margin-bottom: 15px;">
  <p style="font-size: 28px; font-weight: bold; margin: 0;">
    Pipeline
  </p>
</div>

<div style="display: flex; justify-content: center; align-items: center; margin: 0 auto;">
  <img src="/web_resources\post\Rotate-ICP\pipeline.png" style="max-width: 100%; height: auto; margin-bottom: 10px;" />
</div>



<div style="text-align: center; margin-bottom: 15px;">
  <p style="font-size: 28px; font-weight: bold; margin: 0;">
    Final Results
  </p>
</div>

<div style="display: flex; justify-content: center; align-items: center; margin: 0 auto;">
  <img src="/web_resources\post\Rotate-ICP\图片1.png" style="max-width: 100%; height: auto; margin-bottom: 10px;" />
</div>