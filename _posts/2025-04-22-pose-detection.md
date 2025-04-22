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

- ultralytics\cfg\models\v9\yolov9-pose.yaml
```bash
# Parameters
nc: 1  # number of classes
kpt_shape: [2, 3] # number of keypoints, just change the first parameter, '3' means visibility
```


- ultralytics\cfg\datasets\coco-pose.yaml
```bash
# Keypoints
kpt_shape: [2, 3] # number of keypoints, number of dims (2 for x,y or 3 for x,y,visible)
# Classes
names:
  0: Joint
```

- ultralytics\utils\plotting.py 
```bash
# line 243 'radius' to control the size of keypoints
cv2.circle(self.im, (int(x_coord), int(y_coord)), radius, color_k, -1, lineType=cv2.LINE_AA)
# cv2.circle(self.im, (int(x_coord), int(y_coord)), , color_k, -1, lineType=cv2.LINE_AA)
```

- ultralytics\cfg\default.yaml: default configuration file

### Train

`yolo pose train data=ultralytics\cfg\datasets\coco-pose.yaml model=ultralytics\cfg\models\v9\yolov9-pose.yaml epochs=300 imgsz=640`



---
### Related links

code:[Github](https://github.com/senseable-ai/yolov9-pose) / [Our code](https://github.com/senseable-ai/yolov9-pose)
<br>
dataset:

