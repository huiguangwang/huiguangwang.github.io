---
title: "How feasible is it to perform multi-topology rebar joint labeling and tying with minimal data?"
layout: splash
date: 2026-01-28
header:
  overlay_color: "#000"
  overlay_filter: "0.1"
  overlay_image: /web_resources/post/Topology_Agnostic/IMG_7263.PNG
  actions:
    - label: "Dataset"
      url: "https://huggingface.co/Huiguang"
excerpt: "We show that diverse rebar joints can be reliably annotated from minimal data using a geometry-driven, two-stage pipeline, enabling robust sim-to-real generalization for robotic rebar tying."

feature_row:
  - image_path: /web_resources/post/Topology_Agnostic/1.png
    alt: "placeholder image 1"
    title: "Background"
    excerpt:
  - image_path: /web_resources/post/Topology_Agnostic/2.png
    alt: "placeholder image 2"
    title: "Two-stage Pseudo-labeling"
    excerpt:
  - image_path: /web_resources/post/Topology_Agnostic/3.png
    title: "Topology-agnostic Tying Policy"
    excerpt:
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

{% include feature_row id="intro" type="center" %}

{% include feature_row %}




<div style="text-align: center;">
  <p style="font-size: 30px; font-weight: bold;">
    Abstract
  </p>
</div>

<div style="text-align: justify;">
  <p style="margin-top: 10px;">Robust detection of rebar joints remains difficult due to geometric diversity, irregular intersection configurations, and noise introduced by real-world sensing. Prior approaches predominantly depend on appearance-based cues and topology-dependent supervision, which constrains their ability to generalize. This paper reframes rebar joint perception as a geometry-dominated structural inference task and introduces a two-stage learning framework that promotes the acquisition of geometric invariants without explicit domain adaptation. In the first stage, a synthetic dataset containing only geometric information is generated to train a detector, which is subsequently fixed and used as an automatic annotator to produce reliable pseudo-labels for simple cross-type intersections in real-world images. In the second stage, a new model is trained from scratch using these pseudo-labeled real samples, thereby incorporating realistic geometric variations without manual labeling effort. Building on this formulation, a unified perception-to-action pipeline is developed that operates independently of intersection topology for robotic rebar tying.
  </p>
  <p><strong>Keywords:</strong> Geometry-dominated perception; Rebar joint detection; Sim-to-real generalization; Topology-agnostic perception; Robotic rebar tying
  </p>
</div>

<div style="text-align: center;">
  <p style="font-size: 30px; font-weight: bold;">
    Framework
  </p>
</div>

<div style="display: flex; justify-content: center; align-items: center; margin: 0 auto;">
  <img src="/web_resources\post\Topology_Agnostic\tying.png" style="max-width: 100%; height: auto; margin-bottom: 10px;" />
</div>