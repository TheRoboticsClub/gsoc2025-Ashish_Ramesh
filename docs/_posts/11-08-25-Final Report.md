---
title: Final Report- Robotics Academy Porting Exercises to Native ROS2 with Direct Topic Integration 
date: 2025-08-10
categories: [Coding Period, Phase Two]
tags: [robotics-academy, ros2, vaccum-cleaner, coding-period, phase-two]
---

Organization: [JdeRobot](https://jderobot.github.io/)  
Student: Ashish Ramesh ([GitHub](https://github.com/AshishRamesh), [LinkedIn](https://linkedin.com/in/ashish-ramesh-7566ba245))  
Mentors: Pedro Arias-Perez, Apoorv Garg, Pawan Wadhwani, Prajyot Jadhav  
Link to GSoC Project Page: [Robotics-Academy: Porting Exercises to Native ROS2 with Direct Topic Integration](https://summerofcode.withgoogle.com/programs/2025/projects/EXcpJT5g)

---

Hello everyone,

This summer, I had the opportunity to contribute to [Robotics Academy](https://jderobot.github.io/RoboticsAcademy/) through the Google Summer of Code 2025 program. My project focused on upgrading the Robotics-Academy’s Docker-based framework by porting exercises to native ROS2 with direct topic integration. My project proposal can be found here.

### About me

I have a Bachelor’s degree in Computer Science Engineering from MVJ College of Engineering, India. My interests lie in software engineering and robotics. Google Summer of Code 2025 marked my first substantial contribution to open source, and it was an amazing experience.

### About the Project

JdeRobot’s Robotics-Academy provides exercises to learn robotics and AI while abstracting students from the complexities of the framework. The dockerized containers and web templates offer cross-platform functionality, simplifying the setup process. This allows beginners to focus on coding and testing their algorithms without dealing with extensive software installation.

Currently, Robotics-Academy uses Gazebo11 in the Robotics-Academy Docker Image (RADI) framework. The primary goal of my project was to migrate the RADI to Gazebo Harmonic and update exercises accordingly. Also, I replaced PX4 with the lighter Aerostack2 Gazebo platform for drone-based exercises, enhancing efficiency.

---

### GitHub Contributions

Over the summer, I submitted 14 pull requests across 3 repositories, all of which have been merged. These pull requests addressed 12 issues, and my contributions will be incorporated into the upcoming releases of JdeRobot’s Robotics-Academy.

| Pull Request | Solves Issue | Description | More |
|:------------:|:------------:|:-----------:|:----:|
|[Robotics Academy](https://github.com/JdeRobot/RoboticsAcademy)  |
| [#3150](https://github.com/JdeRobot/RoboticsAcademy/pull/3150)         | [#3148](https://github.com/JdeRobot/RoboticsAcademy/pull/3148)          | Follow Line Exercise docs update with <br> ROS 2 topics & new modules info | [Week 4 Blog](link) |
| [#3157](https://github.com/JdeRobot/RoboticsAcademy/pull/3157)         | [#3156](https://github.com/JdeRobot/RoboticsAcademy/pull/3156)          | Vacuum Cleaner Exercise docs update with <br> ROS 2 topics & new modules info | [Week 5 Blog](link) |
| [#3168](https://github.com/JdeRobot/RoboticsAcademy/pull/3168)         | [#3167](https://github.com/JdeRobot/RoboticsAcademy/pull/3167)          | Update GUI to support publishing of images <br> for the Web UI (Ros Native Follow Line) | [Week 6 Blog](link) |
| [Robotics Application Manager](https://github.com/JdeRobot/RoboticsApplicationManager)  |
| [#216](https://github.com/JdeRobot/RoboticsApplicationManager/pull/216)        | [#217](https://github.com/JdeRobot/RoboticsApplicationManager/issues/217)          | ROS 2 spin() support to user code| [Week 2 Blog](link) |
| [#221](https://github.com/JdeRobot/RoboticsApplicationManager/pull/221)        | [#218](https://github.com/JdeRobot/RoboticsApplicationManager/issues/218)          | Support for rclpy.spin_once()| [Week 3 Blog](link) |
| [#228](https://github.com/JdeRobot/RoboticsApplicationManager/pull/228)        | [#227](https://github.com/JdeRobot/RoboticsApplicationManager/issues/227)          | Frequency control using rate| [Week 4 Blog](link) |
| [#230](https://github.com/JdeRobot/RoboticsApplicationManager/pull/230)        | [#227](https://github.com/JdeRobot/RoboticsApplicationManager/issues/227)          | Branch Sync| [Week 5 Blog](link) |
| [Robotics Academy Solutions <br> (This is a private repo)](https://github.com/JdeRobot/RoboticsAcademy-solutions) |
| [#100](https://github.com/JdeRobot/RoboticsAcademy-solutions/pull/100), [#103](https://github.com/JdeRobot/RoboticsAcademy-solutions/pull/103)         | [#98](https://github.com/JdeRobot/RoboticsAcademy-solutions/issues/98), [#102](https://github.com/JdeRobot/RoboticsAcademy-solutions/issues/102)          | Follow line ROS Native Solution | [Week 5 Blog](link), <br> [Week 6 Blog](link) |


Thanks for reading! I’m excited about the progress made this week and looking forward to tackling the challenges ahead. If you have any questions or feedback, feel free to reach out!

Until next week —  
_Ashish_
