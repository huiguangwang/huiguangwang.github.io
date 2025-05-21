---
title: Course-Pixel Coordinate Estimation from 2D World Coordinates on a Plane Using an RGB-D Camera
classes: wide
author_profile: true
date: 2025-04-13
categories: 
  - Course
last_modified_at: 2025-04-13
comments: True
---


## 📌 Problem Description

Given:
- A planar surface (infinite plane) observed by an RGB-D camera.
- A known 2D world coordinate on the plane: $ P: (x_w, y_w) $
- The Z coordinate $ z_w $ of $P$  of the point is **unknown**
- The RGB-D camera provides both color and depth images

**Goal**: Find the pixel coordinate $ (u, v) $ in the image that corresponds to the world point $ (x_w, y_w) $.

---

## ✅ Key Insight from Literature

Based on the paper:  
**"Automated point positioning for robotic spot welding using integrated 2D drawings and structured light cameras"**, a method named **Fast Pixel Matching (FPM)** is proposed to solve this problem efficiently.

---

## 📐 Standard Projection Equation

When the depth $ z_{\text{cam}} $ is known, the 3D point in the **camera coordinate system** can be computed by:

$$
\mathbf{X}_c =
z_{\text{cam}} \cdot K^{-1} \cdot
\begin{bmatrix}
u \\ v \\ 1
\end{bmatrix}
$$

To convert it into **world coordinates**, apply the extrinsic transformation:

$$
\mathbf{X}_w =
R \cdot \mathbf{X}_c + t
$$

where:
- $ K $ is the camera intrinsic matrix,
- $ R $, $ t $ are the rotation and translation matrices from the camera to world frame,
- $ \mathbf{X}_c $ and $ \mathbf{X}_w $ are the 3D coordinates in camera and world frames respectively.

> But in our case, we **already know** $ x_w, y_w $ and want to **find** the corresponding $ (u, v) $, so we need to **reverse** the process using FPM.

## 🚀 FPM Algorithm Summary

1. **Brute-force idea**:  
   For each pixel $ (u,v) $, retrieve depth $ z_{\text{cam}} $, and project it into world coordinates.  
   Then compare $ (x_w, y_w) $ with the computed 3D point.

2. **FPM improvement**:
   - Avoids linear scan of all pixels (O(N)).
   - Performs **logarithmic spatial subdivision** (quadtree-like search), reaching time complexity $ O(\log_4 N) $.
   - Efficiently narrows down to pixels where:
     $$
     \left\| \text{World}(u,v) - (x_w, y_w) \right\| < \varepsilon
     $$

   - Example: For a 1280×1024 depth image, only **11 iterations** are needed.

---

## 🔄 Overall Procedure

1. **Inputs**:
   - Target world coordinate: $ (x_w, y_w) $
   - Camera intrinsics $ K $, extrinsics $ M_{\text{cam2world}} $
   - Depth image $ D(u,v) $

2. **Search using FPM**:
   - For each candidate pixel in a shrinking search region:
     - Get depth $ z_{\text{cam}} $ at $ (u,v) $
     - Back-project to 3D world coordinate
     - Check distance to target $ (x_w, y_w) $

3. **Output**:
   - Pixel coordinate $ (u,v) $ such that back-projected point is close to $ (x_w, y_w) $

---

## 📎 Applications

- Robotic welding and drilling with 2D blueprints
- Mapping CAD-drawn 2D points onto physical surfaces
- Pose estimation and 3D grasping on flat surfaces

---

## 🧠 Tips

- Ensure accurate calibration of intrinsic and extrinsic parameters
- Use depth filtering/smoothing to reduce noise
- Choose a small $ \varepsilon $ (e.g., 1 mm) for fine alignment
