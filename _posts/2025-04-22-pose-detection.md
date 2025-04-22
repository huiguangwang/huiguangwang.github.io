---
title: YoloV9:2D bounding boxes and keypoints detection
classes: wide
author_profile: true
date: 2025-04-22
last_modified_at: 2024-04-22
categories: 
  - Resources
---


### Create Dataset
1. X-Anylabeling(Version 2.5.4)
2. Installation tutorial: [Bilibili](https://www.bilibili.com/video/BV1LHUkYzEwY/?vd_source=423235ba3c8c6b4fb4962ae292f89130)
3. label: [class_ID x_center y_center bbox_width bbox_height x1 y1 vis x2 y2 vis ...]

### Important files in the Yolov9 pose detection algorithm file
1. datasets/pose_json2txt.py: Transfer label files from .json to .txt
2. datasets/split.py: split dataset
3. change configuration files
- ultralytics\cfg\models\v9\yolov9-pose.yaml nc & kpt_shape
- ultralytics\cfg\datasets\coco-pose.yaml 
- ultralytics\utils\plotting.py line 243 radius to control the size of keypoints

### Train
`yolo pose train data=ultralytics\cfg\datasets\coco-pose.yaml model=ultralytics\cfg\models\v9\yolov9-pose.yaml epochs=300 imgsz=640`




