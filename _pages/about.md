---
permalink: /
title: "个人简介"
author_profile: true
redirect_from: 
  - /about/
  - /about.html
---

现于哈尔滨工业大学（深圳）控制科学与工程专业攻读硕士学位（师从李衍杰教授），本科以优异学业表现（前3%）保送本校继续深造。作为[RLG实验室](https://www.rlg-hitsz.net) 的一员，专注于深度强化学习算法在智能机器人领域中的应用研究，现正在进行基于强化学习在机器人规划控制领域研究，已发表会议论文一篇。[IROS-2025](https://arxiv.org/abs/2503.02649)。

教育背景
======
- **工学硕士**，控制科学与工程  
  *哈尔滨工业大学（深圳）*  
  *[RLG实验室](https://www.rlg-hitsz.net)，2024年9月 – 2027年3月*

- **工学学士**，自动化  
  *哈尔滨工业大学（深圳）*  
  *2020年9月 – 2024年6月*

实习经历
======

## 深圳市大疆创新科技有限公司  
*AI模型算法 - 飞行系统部 ｜ 2025.07 - 2025.12*
### 项目一：基于强化学习的涵道穿越机刹车姿态控制  
项目内容：针对涵道穿越机刹车跑姿态问题，采用**强化学习**方法降低刹车阶段跑姿态概率。  
- **空气动力学建模**: 基于实机飞行数据训练残差动力学模型；提出**单桨叶残差网络架构**，大幅提升数据利用效率与模型泛化性；成功在仿真中复现刹车跑姿态现象；
- **强化学习训练**: 基于**rsl**库设计刹车场景的观测空间、奖励函数与课程学习机制完成策略训练，采用**扫频频谱辨识**、**域随机化**和**数据回放**方法实现Sim2Real迁移。

**项目成果**：实测RL较传统方法降低跑姿态概率**50%**以上，并实现不同风速下刹车速度的自适应调节。

### 项目二：基于可微仿真的无人机智能跟拍算法  
项目内容：构建基于**可微物理仿真**的训练框架，解决**PPO**训练难收敛问题，实现无人机智能避障跟拍。  
- **仿真器开发**: 基于**PyTorch**构建可微无人机动力学模型(质点+惯性延迟)，采用**CUDA**算子实现高效距离场计算**(10000+ FPS)**，实现单卡20分钟内收敛；
- **网络设计**: 搭建**CNN+GRU+多头MLP**架构，融合语义深度图、本体状态及用户指令等；多头解耦输出虚拟指令、行人预测速度与Jerk轨迹；  
- **Loss与决策**: 设计语义避障Loss和轨迹一致性Loss，提高轨迹平滑性与避障能力；针对遮挡工况引入虚拟指令Loss，驱动策略网络实现跟拍模态自主切换。

**项目成果**：打通完整训练Pipeline并完成**实机验证**；实现**智能避障、跟拍自动降高与切尾随**等功能。


研究经历
======

## 基于强化学习的无人机被动容错控制算法研究  
*负责人 ｜ 2024.01 – 2025.01*  
项目内容：基于**强化学习**方法实现无人机在任意单个旋翼失效任意程度下仍能保持有效的位置控制。
- **架构设计**: 提出**Selector-Controller**网络架构，实现“故障感知-容错控制”一体化框架；
- **仿真搭建**: 构建旋翼故障模型，基于OpenMP与Pybind实现底层并行加速与Python接口封装；
- **策略训练**: 设计状态观测空间、奖励函数及针对性故障场景，采用**强化学习**与**行为克隆**联合训练；
- **实机验证**: 完成模型参数辨识，采用**域随机化**实现**Sim2Real**，将策略成功部署至**PX4**飞控实测。

**成果：IROS-2025，*J. Chen, K. Zhao, Z. Liu, Y. Li and Y. Lou, "Learning-Based Passive Fault-Tolerant Control of a Quadrotor with Rotor Failure," 2025 IEEE/RSJ International Conference on Intelligent Robots and Systems (IROS), Hangzhou, China, 2025, pp. 1876-1883, doi: 10.1109/IROS60139.2025.11245951.**
<iframe 
  src="https://player.bilibili.com/player.html?bvid=BV1bm94YPE5x" 
  width="720" 
  height="405" 
  frameborder="0" 
  allowfullscreen>
</iframe>

****
## 基于MPCC的狭窄空间多机器人运动规划  
*负责人 ｜ 2023.10 – 2024.01*  
项目内容：采用模型预测轮廓控制（**MPCC**）实现**多机器人轨迹规划**，在实物机器人上验证所提方法。  
- 采用MPCC作为顶层规划模块, 同时将时空两个维度引入优化问题中, 实现多机器人的**动态避障**。
- 采用MPC作为底层控制模块, 提高控制频率使算法满足**实时性**要求。

**成果：葛亚明,陈杰浩.模型预测轮廓控制的机器人群运动规划[J].实验室研究与探索,2024,43(07):28-33+58.DOI:10.19927/j.cnki.syyt.2024.07.006.**

****
## 无人机轨迹跟踪控制的研究  
*负责人 ｜ 2023.02 – 2023.08*
- 采用优化求解和闭式求解两种方法实现给定路径点MinimumSnap多项式轨迹的生成。
- 分别采用**NMPC**和**微分平坦**方法，在仿真环境RotorS中实现控制无人机跟踪轨迹，速度大于15m/s。
- 在实物无人机中，采用 PX4 框架实现对八字和圆形轨迹的跟踪。

<video width="720" height="405" controls>
  <source src="https://hitszcjh.github.io/files/traj_x264.mp4" type="video/mp4">
  Your browser does not support the video tag.
</video>

****

项目经历
======

### 基于鱼眼相机的全景环视拼接  
*核心成员 ｜ 2023.11 – 2024.01*  
项目内容：基于车辆前后左右方向的四个鱼眼摄像头实现**鸟瞰图拼接**，主要方法包括: 去畸变、定位与投影、图形拼接、亮度平衡和多线程加速.  
**成果：星闪杯高校应用挑战赛总决赛 (全国第二名)**  
<video width="720" height="405" controls>
  <source src="https://hitszcjh.github.io/files/sparklink_x264.mp4" type="video/mp4">
  Your browser does not support the video tag.
</video>

****
### 永磁同步电机模拟负载系统  
*负责人 ｜ 2022.04 – 2023.04*  
项目内容：使用永磁同步电机（PMSM）模拟可调阻尼、弹簧、随机扰动等负载情况。  
- 电路硬件设计: 设计系统电路原理图，主要包含主控芯片、电源转换、外设接口、功率放大和信号采集部分；设计PCB并进行打板，焊接，测试实物电路板。
- 软件算法设计: 实现对电机电磁力矩的控制以及获取电机角速度速角加速度，主要包括电机参数的辨识、电机**矢量控制**算法、**滑模反电动势观测器**和**拓展卡尔曼滤波器**的设计与实现。在Matlab仿真和STM32实物平台上验证算法。

**成果：软件著作权一项**  
<video width="720" height="405" controls>
  <source src="https://hitszcjh.github.io/files/motor_x264.mp4" type="video/mp4">
  Your browser does not support the video tag.
</video>

****
### 基于深度学习的电磁循迹小车  
*核心成员 ｜ 2021.01 – 2021.08*  
项目内容：对小车的软硬件进行设计，实现小车对电磁轨迹进行跟踪，并以最快的速度完成比赛。  
- 设计与制作小车的单片机主控电路板，电机驱动电路板和电磁信号采集整流放大电路板。
- 结合**神经网络**对不同的控制方案进行探索并验证（特征分类或端到端控制）。

**成果：第十六届全国大学生智能汽车竞赛 (全国一等奖)**  
<video width="720" height="405" controls>
  <source src="https://hitszcjh.github.io/files/smart_car_x264.mp4" type="video/mp4">
  Your browser does not support the video tag.
</video>

****
### 基于深度学习的FPGA目标物体识别系统  
*负责人 ｜ 2022.09 – 2022.11*  
项目内容：使用FPGA纯硬件语言实现手写数字识别，结合FPGA并行构架特点对网络模型进行加速，设计**多级流水线**，在资源受限的FPGA平台上实现500Hz的处理频率。  
<video width="720" height="405" controls>
  <source src="https://hitszcjh.github.io/files/FPGA_x264.mp4" type="video/mp4">
  Your browser does not support the video tag.
</video>
