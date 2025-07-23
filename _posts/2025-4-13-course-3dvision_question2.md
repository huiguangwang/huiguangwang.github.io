---
title: Course-Relationship Between Principal Point and Image Dimensions
classes: wide
author_profile: true
date: 2025-04-13
categories: 
  - Course
last_modified_at: 2025-04-13
comments: True
---


## 📌 Theoretical Relationship

In theory, the **principal point** refers to the intersection of the camera's **optical axis** with the image plane. This point is typically located **near the center of the image**. Thus:

$$
p_x \approx \frac{W}{2}  
$$

$$
p_y \approx \frac{H}{2}
$$

---

## 🎯 More Precise Expression

Let:

- **W** = image width  
- **H** = image height

In a pixel coordinate system (origin at top-left corner):

- If pixel centers are at integer positions:
  $$
  p_x = \frac{W - 1}{2}  
  $$

  $$
  p_y = \frac{H - 1}{2}
  $$

- If pixel centers are at half-integer positions:
  $$
  p_x = \frac{W}{2}  
  $$

  $$
  p_y = \frac{H}{2}
  $$

---

## 📸 Example

For a 1920×1080 image:

$$
p_x \approx 960  
$$

$$
p_y \approx 540
$$

---

## ⚠️ Practical Considerations

- The actual principal point **may deviate** from the image center
- Reasons: lens manufacturing tolerances, sensor alignment, calibration accuracy
- Calibration often returns **non-integer values** for \( p_x, p_y \)
- Offsets are more prominent in:
  - Wide-angle lenses
  - Mobile phone cameras
  - Industrial cameras

---

## 📐 Camera Intrinsic Matrix

The camera intrinsic matrix \( K \) is defined as:

$$
K = \begin{bmatrix}
f_x & 0 & p_x \\
0 & f_y & p_y \\
0 & 0 & 1
\end{bmatrix}
$$

Where:

- \( f_x = f \cdot s_x \): focal length scaled in x direction  
- \( f_y = f \cdot s_y \): focal length scaled in y direction  
- \( p_x, p_y \): principal point coordinates in pixels  
- \( s_x, s_y \): number of pixels per unit distance in the x and y directions (i.e., pixel density). These are used to convert physical focal length (in mm) to pixel units.

---

## ✅ Summary

| Concept             | Theoretical Value                   | Practical Observation         |
|---------------------|-------------------------------------|-------------------------------|
| \( p_x \)           | ~ image width / 2                   | Slightly offset from center   |
| \( p_y \)           | ~ image height / 2                  | May vary by a few pixels      |
| Pixel origin        | Top-left (0,0)                      | Standard in most systems      |
| Deviation reason    | Lens/sensor misalignment, distortion | Corrected via calibration     |
