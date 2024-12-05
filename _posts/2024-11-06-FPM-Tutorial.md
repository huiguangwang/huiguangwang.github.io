---
title: Tutorial-How to apply FPM algorithm
classes: wide
author_profile: true
date: 2024-11-06
categories: 
  - Tutorial
last_modified_at: 2024-12-03
---


<div style="text-align: center;">
  <p style="font-size: 30px; font-weight: bold; margin-bottom: 5px;">
    Automated Point Positioning for Robotic Spot Welding through Integrated 2D Drawings and Structured Light Cameras<br/>
  </p>
  <p style="margin-top: 10px;">Lu Deng, <strong>Huiguang Wang</strong>, Ran Cao, Jingjing Guo</p>
  <p style="margin-top: 10px;">College of Civil Engineering, Hunan University, Changsha 410082, PR China</p>

  <div style="display: flex; justify-content: center; align-items: center; width: 200px; margin: 0 auto;">
    <img src="/web_resources/Hunan_University.svg" style="max-width: 100%; height: auto; margin-bottom: 10px;" />
  </div>

</div>




<div style="display: flex; justify-content: center; align-items: center;">
  <a href="https://youtu.be/-3JwZIYJyXY?si=GirI83uAahH1MXck"><img src="/web_resources\youtube.svg" style="max-width: 40px; height: auto;" /></a> &nbsp;&nbsp;<a href="https://youtu.be/-3JwZIYJyXY?si=GirI83uAahH1MXck"><strong>[Video]</strong></a>
  &nbsp;&nbsp;&nbsp;
  <a href="https://github.com/huiguangwang"><img src="/web_resources\github.svg" style="max-width: 30px; height: auto;" /></a> &nbsp;&nbsp;<a href="https://github.com/huiguangwang"><strong>[Code]</strong></a>
</div>

<br>

<div style="text-align: center;">
  <p style="font-size: 30px; font-weight: bold;">
    Abstract
  </p>
</div>

<div style="text-align: justify;">
  <p style="margin-top: 10px;">Precise point positioning is crucial for implementing robotic spot welding. Traditional 2D drawings of structural components lack depth information, making them insufficient for guiding robotic welding. This paper introduces an automated robotic welding framework for spot welding based on 2D drawings and structured light cameras . To enhance the efficiency of point positioning, a new algorithm was also developed with a spatial complexity level of log4(N), where N is the resolution of the image. Three different 3D cameras with distinct imaging principles were used in the experiments, and their performances were compared and discussed in detail. The proposed framework was validated against a scaled experiment, where the positioning accuracy by the proposed method met the code requirements. It was also found that the proposed vision-based welding approach could provide similar accuracy in welding orientation estimation as light section sensors but at a much lower cost.
  </p>
  <p><strong>Keywords:</strong> Point positioning; 2D drawings; Supplementation of depth information; Stud welding; 3D vision
  </p>
</div>


<div style="text-align: center;">
  <p style="font-size: 30px; font-weight: bold;">
    Tutorial
  </p>
</div>

<div style="text-align: justify;">
  <p><strong>The first step: </strong>Extract 2D drawing coordinates information from .dwg files<br>
  In this stage, we provide an AutoCAD plug-in (pistion.dll) to extract 2d welding coordinates from 2d drawings based on C sharp programming language and Visual Studio 2019. Now, let us tell you how to compile .dll file and extract 2d welding coordinates in 2d drawings.<br>
  <strong>1. Compile .dll file: </strong>Initially, we should download Visual Studio 2019, then just open our code in Visual Studio 2019. It is noticeable that you should change your .csv file save directory in line 11. After that, you can compile .dll file<br>

  <strong>2. Extract 2D welding coordinates information: </strong>Initially, we should download Visual Studio 2019, then just open our code in Visual Studio 2019. It is noticeable that you should change your .csv file save directory in line 39. After that, compile .dll file<br>

  <strong>3. Output 2D welding coordinates information .csv file: </strong>There is a video in Youtube which can be referred to how to use position.dll.<a href="https://youtu.be/-3JwZIYJyXY?si=GirI83uAahH1MXck"><strong> [Video]</strong></a>  
    <div style="display: flex; justify-content: center; align-items: center; width: 900px; margin: 0 auto;">
      <img src="/web_resources\post\FPM_paper\plug_in_tutorial.png" style="max-width: 100%; height: auto; margin-bottom: 10px;" />
    </div>

  </p>

</div>

```bash
FPM_code
├── 1_TargetPointExtract                      # data files for customizing the theme
|  ├── Camera2Robot.txt          # main navigation links
|  ├── CenterExtract.py          # main navigation links
|  ├── circle_info.txt          # main navigation links
|  ├── ColorMap.png          # main navigation links
|  ├── DepthMap.tiff          # main navigation links
|  └── mark.png             # text used throughout the theme's UI
├── 2_Cad2Base
|  ├── Cad2Base.py     # snippets for analytics (Google and custom)
|  ├── Centers.csv      # snippets for comments
|  ├── Centers_modified.csv
|  └── Transformed_Centers.csv
├── 3_MainProgrram
|  |  ├── BFS.py             # plugin settings and other scripts to load after jQuery
|  |  └── FPM.py          # optimized and concatenated script file loaded before </body>
|  ├── Camera2Robot.txt   # tag/category archive for Jekyll Archives plugin
|  ├── ColorMap.png            # archive base
|  ├── DepthMap.tiff         # archive listing posts grouped by category
|  └── Transformed_Centers.csv           # archive listing posts grouped by specific category
├── API
|  ├── Came2End.txt
|  ├── Camera2Robot.txt                  # image assets for posts/pages/collections/etc.
|  ├── CameraIntrinsics.txt
|  ├── CameraIntrinsics.txt
|  ├── Rigid_transformation.py
└──└── UR10_robot.py
```


<div style="text-align: justify;">
  <p><strong>The second step: </strong>Map 2D welding coordinates to 3D space: FPM algoritm<br>

  We usually adopt four circular marks as a mark board, actually only three circular will be utilized. In this stage, we adopt Hough Transformation Method to recognize the circular marks.<br>
  <strong>1. Compile .dll file: </strong>Initially, we should download Visual Studio 2019, then just open our code in Visual Studio 2019. It is noticeable that you should change your .csv file save directory in line 11. After that, you can compile .dll file<br>



  </p>

</div>











<hr>

<div style="display: flex; align-items: center; margin-top: 20px; margin-bottom: 20px;">
  <img src="/web_resources\publication\picture\第二篇文章.png" style="flex-shrink: 0; width: 200px; margin-right: 20px;"/>
  <div style="text-align: justify;">
    <span style="color:#1772d0; display: block; margin-bottom: 10px;">
      <b>Automated Point Positioning for Robotic Spot Welding Based on the Integration of 2D Drawings and Structured Light Cameras (Under Review)</b>
    </span>
    <p>
      Lu Deng, <strong>Huiguang Wang</strong>,  Ran Cao, Jingjing Guo
      <br/>        
      <a href="https://youtu.be/-3JwZIYJyXY?si=GirI83uAahH1MXck"><b>[Demo]</b></a>
      <!-- <a href="https://huiguangwang.top/file/Code_FPM.rar"><b>[Code]</b></a> -->
      <br/>
    </p>
  </div>
</div>



