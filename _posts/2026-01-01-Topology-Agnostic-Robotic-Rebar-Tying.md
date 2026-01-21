---
title: "Geometry-Driven Perception and Action for Topology-Agnostic Robotic Rebar Tying"
layout: splash
date: 2016-03-23T11:48:41-04:00
header:
  overlay_color: "#000"
  overlay_filter: "0.5"
  overlay_image: /web_resources/logo/AIS_logo.png
  overlay_excerpt: |
    <div style="text-align: center;">
      <p style="margin-top: 10px;">
        <strong>Huiguang Wang <sup>a</sup></strong>, 
        Zekai Jin<sup>a</sup>, 
        Yi Shao <sup>a,*</sup>
      </p>

      <p style="margin-top: 10px;">
        a McGill University, Montreal, Canada<br>
        * Corresponding author, email address: yi.shao2@mcgill.ca
      </p>
    </div>
  actions:
    - label: "Code"
      url: "https://github.com/mmistakes/minimal-mistakes/"
    - label: "Dataset"
      url: "https://github.com/mmistakes/minimal-mistakes/"


feature_row:
  - image_path: /web_resources/post/Topology_Agnostic/1.png
    alt: "placeholder image 1"
    title: "Background"
    excerpt: "This is some sample content that goes here with **Markdown** formatting."
  - image_path: /web_resources/post/Topology_Agnostic/2.png
    alt: "placeholder image 2"
    title: "Two-stage Pseudo-labeling"
    excerpt: "This is some sample content that goes here with **Markdown** formatting."
  - image_path: /web_resources/post/Topology_Agnostic/3.png
    title: "Topology-agnostic Tying Policy"
    excerpt: "This is some sample content that goes here with **Markdown** formatting."
categories: 
  - Tutorial
---

{% include feature_row id="intro" type="center" %}

{% include feature_row %}



<div style="text-align: center;">
  <p style="font-size: 30px; font-weight: bold; margin-bottom: 5px;">
    Geometry-Driven  Perception and Action for Topology-Agnostic Robotic Rebar Tying<br/>
  </p>
  <p style="margin-top: 10px;">
    <strong>Huiguang Wang <sup>a</sup></strong>, Zekai Jin<sup>a</sup>, Yi Shao <sup>a,*</sup>
  </p>
  <p style="margin-top: 10px;">a McGill University, Montreal, Canada<br>* Corresponding author, email address: yi.shao2@mcgill.ca
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

<br>

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

<div style="text-align: center;">
  <p style="color: red; font-size: 25px; font-weight: bold;">
    The code and dataset will be open-source after this paper being published.
  </p>
</div>