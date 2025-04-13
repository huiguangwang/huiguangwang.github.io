---
title: Course-Eye-in-Hand Camera Calibration Guide (Using RGB + Pose Data)
classes: wide
author_profile: true
date: 2025-04-13
categories: 
  - Course
last_modified_at: 2025-04-13
comments: True
---

<script type="text/javascript" async
  src="https://cdn.jsdelivr.net/npm/mathjax@3/es5/tex-mml-chtml.js">
</script>

Here is an inline equation: \\( E = mc^2 \\)

And here is a block-level matrix:

{% raw %}
$$
K =
\\begin{bmatrix}
f_x & 0 & p_x \\\\
0 & f_y & p_y \\\\
0 & 0 & 1
\\end{bmatrix}
$$
{% endraw %}

# Question 1: Eye-in-Hand Camera Calibration Guide (Using RGB + Pose Data)

## 🎯 Objective

The goal of this calibration is to determine the **intrinsic** and **extrinsic** parameters of an RGB camera that is mounted on a robotic arm (eye-in-hand configuration).

- **Intrinsic Parameters**: Describe the internal characteristics of the camera (e.g., focal length, principal point, distortion).
- **Extrinsic Parameters**: Describe the spatial relationship (rotation and translation) between the camera and the robot end-effector.

---

## 🗃️ Dataset Description

- **Data Format**: Each calibration sample includes:
  - One **RGB image**
  - One **6-DOF pose** of the robot end-effector
- **Total Samples**: 37
- **Pose Representation**:
  - **Translation**: \((x, y, z)\), in **millimeters**
  - **Rotation**: \((rx, ry, rz)\), in **radians**
  - **Rotation Order**: **XYZ**, using **fixed angles**
  - **Coordinate System**: **Right-hand coordinate system**

---

## 📌 Calibration Setup

- **Camera Mounting**: Eye-in-hand (camera is fixed on the robot end-effector)
- **Target**: Usually a checkerboard or AprilTag board fixed in the world coordinate frame
- **Assumption**: The transformation between the robot base and the calibration target is static

---

## 🧮 Calibration Procedure

### Step 1: Image and Pose Collection
- Move the robotic arm to various poses while ensuring the target is visible in the camera view.
- For each pose:
  - Record the RGB image
  - Record the 6-DOF pose of the robot end-effector

### Step 2: Detect Features in Image
- Detect corner points or tag centers (e.g., checkerboard corners) in each image.
- These 2D image points correspond to known 3D points on the target.

### Step 3: Estimate Intrinsic Parameters
- Use OpenCV or similar toolboxes to compute:
  - Focal lengths \( f_x, f_y \)
  - Principal point \( p_x, p_y \)
  - Lens distortion coefficients

### Step 4: Estimate Extrinsic Parameters
- Solve the **Hand-Eye Calibration** problem:
  - Input: Robot poses + camera poses relative to the calibration board
  - Output: Transformation from camera to robot flange \( \mathbf{T}_{\text{camera}}^{\text{end-effector}} \)
- Common method: Tsai-Lenz or Dual Quaternion-based approach

---

## 📐 Output

- **Intrinsic Matrix** \( K \):

{% raw %}
$$
K = 
\begin{bmatrix}
f_x & 0 & p_x \\
0 & f_y & p_y \\
0 & 0 & 1
\end{bmatrix}
$$
{% endraw %}

- **Distortion Coefficients**: \( k_1, k_2, p_1, p_2, k_3 \)

- **Extrinsic Matrix** \( [R | t] \): Rotation and translation from robot end-effector to camera

---

## ✅ Notes

- Accuracy improves with more diverse poses and clear feature detection
- Avoid positions with poor visibility or insufficient viewpoint change
- Double-check unit consistency (e.g., mm vs m, degrees vs radians)

---

## 📚 Recommended Libraries

- [OpenCV](https://docs.opencv.org/)
- [Kalibr](https://github.com/ethz-asl/kalibr)
- [ROS camera_calibration](http://wiki.ros.org/camera_calibration)

---

## 📎 Application

This calibration result can be used in:
- 3D vision-based grasping
- Visual servoing
- Pose estimation
- Robotic SLAM and mapping
