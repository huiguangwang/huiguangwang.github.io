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
    Automated Point Positioning for Robotic Spot Welding through the Integrated 2D Drawings and Structured Light Cameras<br/>
  </p>
  <p style="margin-top: 10px;">Lu Deng, <strong>Huiguang Wang</strong>, Ran Cao, Jingjing Guo</p>
  <p style="margin-top: 10px;">College of Civil Engineering, Hunan University, Changsha 410082, PR China</p>

  <div style="display: flex; justify-content: center; align-items: center; width: 400px; margin: 0 auto;">
    <a href="https://www.hnu.edu.cn/" target="_blank">
      <img src="/web_resources/Hunan_University.svg" style="width: 200px; height: auto; margin-bottom: 10px;" />
    </a>
    &nbsp;&nbsp;&nbsp;&nbsp;
    <a href="https://www.dengteam.com/index.php?m=content&c=index&a=show&catid=70&id=251" target="_blank">
      <img src="/web_resources/dengteam.png" style="width: 200px; height: auto; margin-bottom: 10px;" />
    </a>
  </div>

</div>




<div style="display: flex; justify-content: center; align-items: center;">
  <a href="https://youtu.be/-3JwZIYJyXY?si=GirI83uAahH1MXck"><img src="/web_resources\youtube.svg" style="max-width: 40px; height: auto;" /></a> &nbsp;&nbsp;<a href="https://youtu.be/-3JwZIYJyXY?si=GirI83uAahH1MXck"><strong>[Video]</strong></a>
  &nbsp;&nbsp;&nbsp;
  <a href="https://github.com/huiguangwang"><img src="/web_resources\github.svg" style="max-width: 30px; height: auto;" /></a> &nbsp;&nbsp;<a href="https://github.com/huiguangwang"><strong>[Code]</strong></a>
</div>

<br>

<div style="text-align: center;">
  <p style="color: red; font-size: 25px; font-weight: bold;">
    The code will be open-source after this paper being published.
  </p>
</div>

<div style="text-align: center;">
  <p style="font-size: 30px; font-weight: bold;">
    Abstract
  </p>
</div>

<div style="text-align: justify;">
  <p style="margin-top: 10px;">Precise point positioning is crucial for implementing robotic spot welding. Traditional 2D drawings of structural components lack depth information, making them insufficient for guiding robotic welding. This paper introduces an automated robotic welding framework for spot welding based on 2D drawings and structured light cameras. To enhance the efficiency of point positioning, a new algorithm was also developed with a spatial complexity level of log4(N), where N is the resolution of the image. Three different 3D cameras with distinct imaging principles were used in the experiments, and their performances were compared and discussed in detail. The proposed framework was validated against a scaled experiment, where the positioning accuracy by the proposed method met the code requirements. It was also found that the proposed vision-based welding approach could provide similar accuracy in welding orientation estimation as light section sensors but at a much lower cost.
  </p>
  <p><strong>Keywords:</strong> Point positioning; 2D drawings; Supplementation of depth information; Stud welding; 3D vision
  </p>
</div>


<div style="text-align: center;">
  <p style="font-size: 30px; font-weight: bold;">
    Tutorial
  </p>
</div>

<div style="text-align: center;">
  <p><strong>The first step: Extract 2D drawing coordinates information from .dwg files</strong>
  </p>
</div>

<div style="display: flex; justify-content: center; align-items: center; width: 600px; margin: 0 auto;">
  <img src="/web_resources\post\FPM_paper\Snipaste_2024-12-05_15-43-40.png" style="max-width: 100%; height: auto; margin-bottom: 10px;" />
</div>

<div style="text-align: justify;">
  
  In this stage, we provide an AutoCAD plug-in (pistion.dll) to extract 2d welding coordinates from 2d drawings based on C sharp programming language and Visual Studio 2019. Now, let us tell you how to compile .dll file and extract 2d welding coordinates in 2d drawings.<br>
  <strong>1. Compile .dll file: </strong>Initially, we should download Visual Studio 2019, then just open our code in Visual Studio 2019. It is noticeable that you should change your .csv file save directory in line 11. After that, you can compile .dll file<br>

  <strong>2. Extract 2D welding coordinates information: </strong>Initially, we should download Visual Studio 2019, then just open our code in Visual Studio 2019. It is noticeable that you should change your .csv file save directory in line 39. After that, compile .dll file<br>

  <strong>3. Output 2D welding coordinates information .csv file: </strong>There is a video in Youtube which can be referred to how to use position.dll.<a href="https://youtu.be/-3JwZIYJyXY?si=GirI83uAahH1MXck"><strong>[Video]</strong></a>  
  <div style="display: flex; justify-content: center; align-items: center; width: 900px; margin: 0 auto;">
    <img src="/web_resources\post\FPM_paper\plug_in_tutorial.png" style="max-width: 100%; height: auto; margin-bottom: 10px;" />
  </div>
</div>

<div style="text-align: center;">
  <p><strong>The second step: Map 2D welding coordinates to 3D space: FPM algorithm</strong>
  </p>
</div>

<div style="text-align: justify;">
  
  <p>
  We have open sourced all codes in Github, and the structure of program as shown below <br>
  </p>

</div>


```bash
FPM_code
├── 1_TargetPointExtract              # file includes programs aimed to identify mark board
|  ├── Camera2Robot.txt               # the homogeneous matrix from Camera frame to robotic arm world frame
|  ├── CenterExtract.py               # main program aims to identify circular marks
|  ├── circle_info.txt                # The identifications results of Hough-Transformation Method
|  ├── ColorMap.png                   # RGB image of the mark board
|  ├── DepthMap.tiff                  # depth map of the mark board
|  └── mark.png                       # The identifications results (RGB image)of Hough-Transformation Method
├── 2_Cad2Base                        # file includes program aimed to transform 2D coordinate from local frame to world frame
|  ├── Cad2Base.py                    # main program aims to transform 2D coordinate from local frame to world frame
|  ├── Centers.csv                    # 2d welding coordinates in CAD frame
|  ├── Centers_modified.csv           # 2d welding coordinates in local frame
|  └── Transformed_Centers.csv        # fianl results: 2d welding coordinates in world frame
├── 3_MainProgram                     # main programs include BFS and FPM algorithm to map 2D coordinates
|  |  ├── BFS.py                      # BFS algorithm
|  |  └── FPM.py                      # Fast-Pixel-Matching algorithm
|  ├── Camera2Robot.txt               # the homogeneous matrix from Camera frame to robotic arm world frame (A area)
|  ├── ColorMap.png                   # RGB image of A area
|  ├── DepthMap.tiff                  # depth map of A area
|  └── Transformed_Centers.csv        # fianl results: 2d welding coordinates in world frame
├── API                               # Application Programming Interface
|  ├── Came2End.txt                   # the result of eye-in-hand calibration
|  ├── Camera2Robot.txt               # the pose of camera
|  ├── CameraIntrinsics.txt           # the intrinsics matrix of camera
|  ├── Rigid_transformation.py        # an API for rigid transformation
└──└── UR10_robot.py                  # an API for controling robotic arm
```


<div style="text-align: justify;">
  <p><strong>1. Identify the circular marks: </strong>We recommend that just ultilize the results as shown in file: circle_info.txt. Because program: CenterExtract.py can be run when it connects with robotic arm and camera. Additionally, we draw the results of identification in mark.png.<br></p>

  <p><strong>2. Transform 2D coordinates from local frame to world frame: </strong>Centers.csv file includes 2D welding coordinates in CAD frame, which can be extracted by the AutoCAD plug-in. Transformed_Centers.csv is the final results of running program: Cad2Base.py.<br></p>

  <p><strong>3. Map 2D coordinates to 3D space: </strong>We provide two method in filefold 3_MainProgram, including Brute force search (BFS) and our method: Fast-Pixel-Matching (FPM). <font color='red'>Actually, you just run BFS.py and FPM.py.</font><br>

  </p>
</div>


<div style="text-align: justify;">
  <p><strong>Finally, several typical results of FPM algorithm are shown below, compared with BFS method.</strong><br>
  </p>
    <div style="display: flex; justify-content: center; align-items: center; width: 900px; margin: 0 auto;">
      <img src="/web_resources\post\FPM_paper\efficiency.png" style="max-width: 100%; height: auto; margin-bottom: 10px;" />
    </div>
    <div style="display: flex; justify-content: center; align-items: center; width: 900px; margin: 0 auto;">
      <img src="/web_resources\post\FPM_paper\efficiency_table.png" style="max-width: 100%; height: auto; margin-bottom: 10px;" />
    </div>
</div>




<div style="text-align: center;">
  <p style="color: red; font-size: 25px; font-weight: bold;">
    If you have any questions, please contact me without any hesitations at: whg0917@hnu.edu.cn
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



