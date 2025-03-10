---
permalink: /
title: "个人简介"
author_profile: true
redirect_from: 
  - /about/
  - /about.html
---

现于哈尔滨工业大学（深圳）控制科学与工程专业攻读硕士学位（师从李衍杰教授），本科以优异学业表现（前3%）保送本校继续深造。作为[RLG实验室](https://www.rlg-hitsz.net) 的一员，专注于深度强化学习算法在智能机器人领域中的应用研究，主导基于强化学习的无人机容错控制算法研究，相关算法已投稿于IROS-2025。[点击下载完整PDF版简历](https://hitszcjh.github.io/files/cv.pdf)。

教育背景
======
- **工学硕士**，控制科学与工程  
  *哈尔滨工业大学（深圳）*  
  *[RLG实验室](https://www.rlg-hitsz.net)，2024年9月 – 至今*

- **工学学士**，自动化  
  *哈尔滨工业大学（深圳）*  
  *2020年9月 – 2024年6月*

项目经历
======

## 基于强化学习的无人机被动容错控制算法研究
***项目负责人** ｜ 2024.01 – 2025.01*

项目内容：基于**强化学习**方法实现四旋翼在任意单个旋翼失效任意程度下仍能保持有效的位置控制。
- 提出**Selector-Controller**策略网络架构，能够结合现有被动和主动容错控制方法的优点，同时通过**强化学习**，**行为克隆**和结合故障信息的**监督学习**方法共同训练策略网络，进一步提升策略网络的性能。
- 搭建仿真环境: 对无人机旋翼故障进行建模，采用RK45方法实现前向积分，同时利用OpenMP和Pybind实现并行化以及封装为Python接口。
- 训练控制策略: 搭建PPO训练框架，设计策略观测值和奖励函数，设计训练场景等。
- 实物实验: 搭建无人机平台，辨识无人机动力学参数，**Sim2Real迁移**，**策略网络部署 (PX4)** 等。

成果：IROS-2025 (一作在投)，github：https://github.com/HITSZcjh/uav_ftc
<iframe 
  src="https://player.bilibili.com/player.html?bvid=BV1bm94YPE5x" 
  width="720" 
  height="405" 
  frameborder="0" 
  allowfullscreen>
</iframe>

### Apple Vision Pro Teleoperation  
<video width="720" height="405" controls>
  <source src="https://hitszcjh.github.io/files/FPGA.mp4" type="video/mp4">
  Your browser does not support the video tag.
</video>

### Apple Vision Pro Teleoperation  
<video width="720" height="405" controls>
  <source src="https://hitszcjh.github.io/files/motor.mp4" type="video/mp4">
  Your browser does not support the video tag.
</video>

### Apple Vision Pro Teleoperation  
<video width="720" height="405" controls>
  <source src="https://hitszcjh.github.io/files/smart_car.mp4" type="video/mp4">
  Your browser does not support the video tag.
</video>

### Apple Vision Pro Teleoperation  
<video width="720" height="405" controls>
  <source src="https://hitszcjh.github.io/files/traj.mp4" type="video/mp4">
  Your browser does not support the video tag.
</video>

### Apple Vision Pro Teleoperation  
<video width="720" height="405" controls>
  <source src="https://hitszcjh.github.io/files/sparklink.mp4" type="video/mp4">
  Your browser does not support the video tag.
</video>