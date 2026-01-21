---
title: "How feasible is it to perform multi-topology rebar joint labeling and tying with minimal data?"
layout: splash
date: 2016-03-23T11:48:41-04:00
header:
  overlay_color: "#000"
  overlay_filter: "0.5"
  overlay_image: /web_resources/logo/AIS_logo.png
excerpt: "We show that diverse rebar joints can be reliably annotated from minimal data using a geometry-driven, two-stage pipeline, enabling robust sim-to-real generalization for robotic rebar tying."
categories: 
  - Tutorial
---

<div style="text-align: center; line-height: 1.3; margin-bottom: 20px;">
  <p style="font-size: 28px; font-weight: bold; margin: 0 0 10px 0;">
    Geometry-Driven Perception and Action for Topology-Agnostic Robotic Rebar Tying
  </p>

  <p style="margin: 0 0 5px 0;">
    <strong>Huiguang Wang<sup>a</sup></strong>, Zekai Jin<sup>a</sup>, Yi Shao<sup>a,*</sup><br>
    <sup>a</sup> McGill University, Montreal, Canada<br>
    * Corresponding author: yi.shao2@mcgill.ca
  </p>

  <div style="display: flex; justify-content: center; align-items: center; width: 400px; margin: 0 auto;">
    <a href="https://www.mcgill.ca/" target="_blank">
      <img src="/web_resources/McGill.png" style="width: 200px; height: auto; margin-bottom: 10px;" />
    </a>
    &nbsp;&nbsp;&nbsp;&nbsp;
    <a href="https://www.shao-lab.com/" target="_blank">
      <img src="/web_resources/AIS.png" style="width: 400px; height: auto; margin-bottom: 10px;" />
    </a>
  </div>
</div>


<div style="text-align: center; margin-bottom: 15px;">
  <p style="font-size: 28px; font-weight: bold; margin: 0;">
    Background & Methodology
  </p>
</div>




<!-- 并列图片 + 说明（加粗文字） -->
<div style="display: flex; justify-content: center; gap: 20px; flex-wrap: wrap; margin: 30px 0;">
  
  <!-- 第一张图片 -->
  <div style="text-align: center; max-width: 300px;">
    <img src="/web_resources/post/Topology_Agnostic/1.png" style="width: 100%; height: auto; margin-bottom: 5px;" />
    <p style="margin: 0;"><strong>Background</strong></p>
  </div>
  
  <!-- 第二张图片 -->
  <div style="text-align: center; max-width: 300px;">
    <img src="/web_resources/post/Topology_Agnostic/2.png" style="width: 100%; height: auto; margin-bottom: 5px;" />
    <p style="margin: 0;"><strong>Two-stage Pseudo-labeling</strong></p>
  </div>

  <!-- 第三张图片 -->
  <div style="text-align: center; max-width: 300px;">
    <img src="/web_resources/post/Topology_Agnostic/3.png" style="width: 100%; height: auto; margin-bottom: 5px;" />
    <p style="margin: 0;"><strong>Topology-agnostic Tying Policy</strong></p>
  </div>

</div>




<div style="text-align: center;">
  <p style="font-size: 30px; font-weight: bold;">
    Abstract
  </p>
</div>

<div style="text-align: justify;">
  <p style="margin-top: 10px;">Robust perception of rebar joints is challenging due to geometric variability, irregular intersection topologies, and real-world sensing imperfections. Existing methods largely rely on appearance-driven recognition and topology-specific supervision, which limits generalization. We reformulate rebar joint perception as a geometry-dominated structural understanding problem and propose a two-stage learning pipeline that biases learning toward geometric invariants without explicit domain adaptation. In the first stage, a geometry-only synthetic dataset is constructed to train a detector that is used exclusively as a fixed annotator to generate reliable pseudo-labels for simple cross-shaped intersections in real images. In the second stage, a final perception model is trained from scratch using only these pseudo-labeled, background-removed real images, introducing authentic geometric variability without manual annotation. Based on this formulation, we further design a unified, topology-agnostic perception-to-action pipeline for robotic rebar tying. Experiments demonstrate robust sim-to-real generalization across diverse rebar topologies and configurations.
  </p>
  <p><strong>Keywords:</strong> Geometry-dominated perception; Rebar joint detection; Sim-to-real generalization; Topology-agnostic perception; Robotic rebar tying
  </p>
</div>

