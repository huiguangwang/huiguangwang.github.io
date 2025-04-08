---
title: Tutorial-How to apply Rotate-ICP algorithm
classes: wide
author_profile: true
date: 2025-04-08
categories: 
  - Tutorial
last_modified_at: 2025-04-08
---


<div style="text-align: center;">
  <p style="font-size: 30px; font-weight: bold; margin-bottom: 5px;">
    Automated Complex Joint Welding for Rebar Cages in Prefabricated Concrete Shear Walls<br/>
  </p>
  <p style="margin-top: 10px;">Lu Deng, Yu Dai, Shaopeng Xu, Ran Cao, <strong>Huiguang Wang (Corresponding author)</strong></p>
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
  <a href="https://www.youtube.com/watch?v=uixmualasgU"><img src="/web_resources\youtube.svg" style="max-width: 40px; height: auto;" /></a> &nbsp;&nbsp;<a href="https://www.youtube.com/watch?v=uixmualasgU"><strong>[Video]</strong></a>
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
  <p style="margin-top: 10px;">Against the background of an aging society and the low degree of automation in the construction industry, experienced welders are gradually retiring, and younger individuals are unwilling to engage in physically demanding and high-risk welding work. Regarding the welding of rebar cage joints, existing technology can only handle the welding of simple joints in rebar meshes and cannot weld the complex joints of rebar cages, which still requires experienced welders. Therefore, we propose a new algorithm, Rotate-ICP, for welding complex joints. This algorithm successfully addresses the symmetry issue in 6-DOF welding pose prediction, improving the registration rate by 15% compared to Ransac-ICP and reducing the registration time by 0.28 seconds. The welding success rate is nearly 100%, with an efficiency of 8.328 seconds per joint, and the welding quality meets the requirements of code.
  </p>
  <p><strong>Keywords:</strong> Robotic welding; Complex joints; Symmetry issue; Point cloud registration; 3D vision;
  </p>
</div>

{% include video id="uixmualasgU" provider="youtube" %}




<div style="text-align: justify;">
    <div style="display: flex; justify-content: center; align-items: center; margin: 0 auto;">
      <img src="/web_resources\post\Rotate-ICP\welding.png" style="max-width: 100%; height: auto; margin-bottom: 10px;" />
    </div>
    <div style="display: flex; justify-content: center; align-items: center; margin: 0 auto;">
      <img src="/web_resources\post\Rotate-ICP\welding1.png" style="max-width: 100%; height: auto; margin-bottom: 10px;" />
    </div>
</div>




<div style="text-align: center;">
  <p style="color: red; font-size: 25px; font-weight: bold;">
    If you have any questions, please contact me without any hesitations at: whg0917@hnu.edu.cn
  </p>
</div>


