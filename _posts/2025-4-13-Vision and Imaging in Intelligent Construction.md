---
title: Visual Sensing and Imaging Principles in Intelligent Construction
classes: wide
author_profile: true
date: 2025-04-13
categories: 
  - Course
last_modified_at: 2025-04-13
comments: true
---

# 📘 Course Homepage: Visual Sensing and Imaging in Intelligent Construction

This course introduces the fundamentals of camera imaging, 3D vision technologies, coordinate system transformations in robotics, and practical applications of vision systems in the context of intelligent construction. It bridges the gap between sensing principles and engineering implementation.

---

## 🧠 1. Camera Imaging Principles

Cameras project the 3D world onto a 2D image plane. Key concepts include:

- **Pinhole Camera Model**:  
  A basic model ignoring distortion. The projection is described by:

  \[
  \begin{bmatrix}
  u \\
  v \\
  1
  \end{bmatrix}
  =
  K \cdot
  \begin{bmatrix}
  X_c \\
  Y_c \\
  Z_c
  \end{bmatrix}
  \]

  Where \( K \) is the intrinsic matrix, \( (u, v) \) are pixel coordinates, and \( (X_c, Y_c, Z_c) \) are coordinates in the camera frame.



- **Camera Intrinsics and Distortion**:
  - Focal length and principal point
  - Radial and tangential distortion

- **Image Sensor Sampling**:
  - CMOS / CCD
  - RGB and grayscale image acquisition

---

## 📷 2. Introduction to 3D Camera Technologies

3D cameras capture both color and depth information. Four common principles are:

### ✅ 2.1 Stereo Vision

- Simulates human vision using **two cameras**
- Calculates **disparity** and triangulates depth
- Depends on reliable feature matching

### ✅ 2.2 Structured Light

- Projects **known patterns** onto the object
- Camera captures the deformation of the pattern to compute depth
- High accuracy, suitable for static scenes
- Used in Kinect v1

### ✅ 2.3 Time of Flight (TOF)

- Emits modulated light and measures **travel time**
- Directly obtains depth for each pixel
- Real-time performance, suitable for dynamic scenes

### ✅ 2.4 Laser Line Scanning

- Uses a **laser line** to scan objects line by line
- The camera captures the deformation of the line
- Suitable for high-precision industrial applications

---

## 🔄 3. Coordinate Systems and Transformations

Visual systems in robotics involve four major coordinate systems:

| Coordinate System     | Description                                        |
|-----------------------|----------------------------------------------------|
| Pixel Coordinate      | Origin at top-left of image, in pixels \((u, v)\) |
| Image Coordinate      | Origin at image center, in millimeters            |
| Camera Coordinate     | Origin at optical center, \(Z\)-axis points forward |
| World Coordinate      | Global reference system \((x_w, y_w, z_w)\)       |

Common transformations:

1. **Pixel → Image Coordinates**:  
   Considering principal point and pixel size.

2. **Image → Camera Coordinates**:  
   $$
   \begin{bmatrix}
   X_c \\
   Y_c \\
   Z_c
   \end{bmatrix}
   = Z \cdot K^{-1} \cdot
   \begin{bmatrix}
   u \\
   v \\
   1
   \end{bmatrix}
   $$

3. **Camera → World Coordinates**:  
   $$
   \mathbf{X}_w = R \cdot \mathbf{X}_c + t
   $$

Where \( R \) and \( t \) are the extrinsic transformation matrices.

---

## 🧪 4. Application Cases in Construction

Several practical use cases will be discussed throughout the course:

### 🛠️ Precast Component Inspection
- Detecting boundaries of precast elements using 3D cameras
- Comparing physical models with CAD blueprints

### 🤖 Welding Point Localization
- Mapping 2D drawing coordinates to 3D surfaces
- Guiding robotic arms for shear stud welding

### 🧱 Brick Positioning & Robotic Laying
- Real-time detection of brick positions
- Automatic calculation of robot arm placement paths

### 📏 Site Measurement & 3D Modeling
- Capturing point clouds of construction sites
- Generating BIM models and performing construction deviation analysis

---

## 🎓 Learning Objectives

By the end of this course, students will:

- Understand the fundamentals of camera imaging and 3D vision
- Master coordinate system transformations in robotic vision
- Analyze and design vision tasks in construction scenarios
- Gain practical skills using depth cameras and calibration tools

---

## 📂 Recommended Tools and Software

- OpenCV / Open3D
- Intel RealSense SDK
- ROS / ROS2 + tf2
- MATLAB Camera Toolbox

---

For questions or discussions, feel free to comment or reach out to the instructor.
