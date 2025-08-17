---
title: Final Report- Robotics Academy Porting Exercises to Native ROS 2 with Direct Topic Integration 
date: 2025-08-11
categories: [Coding Period, Phase Two, Final Report]
tags: [robotics-academy, ros2, vaccum-cleaner, follow-line, coding-period, phase-two, final-report]
pin: true
---

Organization: [JdeRobot](https://jderobot.github.io/)  
Student: Ashish Ramesh ([GitHub](https://github.com/AshishRamesh), [LinkedIn](https://linkedin.com/in/ashish-ramesh-7566ba245))  
Mentors: Pedro Arias-Perez, Apoorv Garg, Pawan Wadhwani, Prajyot Jadhav  
Link to GSoC Project Page: [Robotics-Academy: Porting Exercises to Native ROS2 with Direct Topic Integration](https://summerofcode.withgoogle.com/programs/2025/projects/EXcpJT5g)

---

Hello everyone,

This summer, I had the opportunity to contribute to [Robotics Academy](https://jderobot.github.io/RoboticsAcademy/) through the Google Summer of Code 2025 program. My project focused on upgrading the Robotics-Academy’s Docker-based framework by porting exercises to native ROS2 with direct topic integration. My project proposal can be found [here](https://drive.google.com/file/d/1dFJHO139j73nkt_5qDKmCxGMMtfub-CU/view?usp=sharing).

### About me

I hold a Bachelor’s degree in Computer Science Engineering from MVJ College of Engineering, India. My interests span software engineering, AI/ML, and robotics, with a strong focus on building practical systems that bridge theory and real-world applications.

While I had some exposure to open source prior to GSoC, this program marks my first major contribution to the open-source community, and it has been an incredibly rewarding learning experience.

### About the Project

JdeRobot’s Robotics-Academy provides exercises to learn robotics and AI while abstracting students from the complexities of the framework. The dockerized containers and web templates offer cross-platform functionality, simplifying the setup process. This allows beginners to focus on coding and testing their algorithms without dealing with extensive software installation.

Currently, Robotics-Academy uses custom Hardware Abstraction Layer (HAL) and GUI components to facilitate interaction and programming of the exercises. My goal was to port these exercises to native ROS2, enabling users to leverage the full capabilities of ROS2, including its powerful communication and middleware features.

---

### Contribution Summary

#### Step 1 : Refactoring the Existing Framework
Robotics Academy consists of three main repositories: [Robotics Academy](https://github.com/JdeRobot/RoboticsAcademy), [Robotics Application Manager](https://github.com/JdeRobot/RoboticsApplicationManager), and [Robotics Infrastructure](https://github.com/JdeRobot/RoboticsInfrastructure). To effectively port the exercises to ROS 2, I first needed to thoroughly understand the existing framework. This involved studying the current implementation, including the custom HAL and GUI components, and identifying the key areas that required modification. The HAL provides a set of APIs that allow users to interact with the exercises without needing to understand the underlying ROS2 architecture. The goal of this project is to provide an alternative interface for users to interact with the exercises using ROS2.

Once I understood the framework, I began refactoring the existing codebase to incorporate ROS 2 Native support. This involved replacing the custom HAL components with their ROS 2 equivalents and updating the Robotics Application Manager to ensure seamless integration within the existing framework.

#### Step 2 : Porting Follow line exercise for ROS2 Native support 

Upon refactoring the existing framework, I began porting the Follow Line exercise to ROS 2. 
The refactoring was done in such a way that all exercises now have partial ROS 2 native support. To achieve full support, only the GUI needed to be ported.
I then worked on porting the WebGUI to ensure ROS 2 native compatibility. The WebGUI now supports two modes:
- Automatic mode, which launches a topic for seamless ROS 2 native integration
- Manual mode, which uses the HAL implementation

I also updated the documentation to reflect ROS 2 native support for the exercise and added a working ROS 2 solution.

![Follow line exercise ROS Native implementation](assets/lib/week_5_fl.gif)  
<sub><i>Follow line exercise ROS Native implementation</i></sub>

#### Step 3 : Porting Vacuum Cleaner exercise for ROS2 Native support

After completing the Follow Line exercise, I began working on the Vacuum Cleaner exercise. This involved similar steps: replacing custom HAL components with their ROS 2 equivalents. Thanks to the groundwork done in Step 2, this process was relatively straightforward and required minimal changes.

I updated the WebGUI in the same way as for the Follow Line exercise, implementing two modes. Now, the map updates in real-time, and the user can see the vacuum cleaner's position on the map as it moves. A working ROS 2 solution for the Vacuum Cleaner exercise was also implemented.

![Vacuum Cleaner exercise ROS Native implementation](assets/lib/week_8.gif)  
<sub><i>Vacuum Cleaner exercise ROS Native implementation </i></sub>

#### Step 4 : Testing , Documentation and production ready  

After implementing the exercises, I focused on testing and ensuring everything worked as expected. This involved running the exercises in various scenarios, identifying and fixing bugs, and keeping the documentation up to date.

I also worked on making the exercises production-ready by ensuring they were well-documented, user-friendly, and robust.

Once the code was production-ready, I created Pull Requests for the changes to be merged into the main production branch. The community can now benefit from ROS 2 native support in these exercises, and the upcoming release will include these enhancements.

---

### Demo Video

Here's a demonstration of the ROS2 native support implementation for both Follow Line and Vacuum Cleaner exercises:

{% include embed/youtube.html id='Ymt8XVFyciY' %}
<sub><i>ROS Native implementation Demo Video</i></sub>

---

### GitHub Contributions

Over the summer, I submitted a total of 21 pull requests across 3 repositories. These pull requests addressed 15 issues, and my contributions will be incorporated into the upcoming releases of JdeRobot’s Robotics-Academy.

| Pull Request | Solves Issue | Description | More |
|:------------:|:------------:|:-----------:|:----:|
|[Robotics Academy](https://github.com/JdeRobot/RoboticsAcademy)  |
| [#3150](https://github.com/JdeRobot/RoboticsAcademy/pull/3150)         | [#3148](https://github.com/JdeRobot/RoboticsAcademy/pull/3148)          | Follow Line Exercise docs update with <br> ROS 2 topics & new modules info | [Week 4 Blog](https://theroboticsclub.github.io/gsoc2025-Ashish_Ramesh/posts/Week-4/) |
| [#3157](https://github.com/JdeRobot/RoboticsAcademy/pull/3157)         | [#3156](https://github.com/JdeRobot/RoboticsAcademy/pull/3156)          | Vacuum Cleaner Exercise docs update with <br> ROS 2 topics & new modules info | [Week 5 Blog](https://theroboticsclub.github.io/gsoc2025-Ashish_Ramesh/posts/Week-5/) |
| [#3168](https://github.com/JdeRobot/RoboticsAcademy/pull/3168)         | [#3167](https://github.com/JdeRobot/RoboticsAcademy/pull/3167)          | Update GUI to support publishing of images <br> (Ros Native Follow Line) | [Week 6 Blog](https://theroboticsclub.github.io/gsoc2025-Ashish_Ramesh/posts/Week-6/) |
| [#3188](https://github.com/JdeRobot/RoboticsAcademy/pull/3188)         | [#3187](https://github.com/JdeRobot/RoboticsAcademy/pull/3187)          | Update GUI to support real time <br> update of map  (Ros Native Vacuum Cleaner) | [Week 7 Blog](https://theroboticsclub.github.io/gsoc2025-Ashish_Ramesh/posts/Week-7/), <br> [Week 8 Blog](https://theroboticsclub.github.io/gsoc2025-Ashish_Ramesh/posts/Week-8/) |
| [#3192](https://github.com/JdeRobot/RoboticsAcademy/pull/3192), [#3196](https://github.com/JdeRobot/RoboticsAcademy/pull/3196)         | [#3193](https://github.com/JdeRobot/RoboticsAcademy/issues/3193)          | Fix GUI import method for ros native <br> and update docs | [Week 9 Blog](https://theroboticsclub.github.io/gsoc2025-Ashish_Ramesh/posts/Week-9/) |
| [#3155](https://github.com/JdeRobot/RoboticsAcademy/pull/3155), [#3197](https://github.com/JdeRobot/RoboticsAcademy/pull/3197), [#3198](https://github.com/JdeRobot/RoboticsAcademy/pull/3198)         | [#3189](https://github.com/JdeRobot/RoboticsAcademy/issues/3189)          | Branch Sync and PR for production branch  | [Week 5 Blog](https://theroboticsclub.github.io/gsoc2025-Ashish_Ramesh/posts/Week-5/), <br> [Week 9 Blog](https://theroboticsclub.github.io/gsoc2025-Ashish_Ramesh/posts/Week-9/) |
| [Robotics Application Manager](https://github.com/JdeRobot/RoboticsApplicationManager)  |
| [#216](https://github.com/JdeRobot/RoboticsApplicationManager/pull/216)        | [#217](https://github.com/JdeRobot/RoboticsApplicationManager/issues/217)          | ROS 2 spin() support to user code| [Week 2 Blog](https://theroboticsclub.github.io/gsoc2025-Ashish_Ramesh/posts/week-2/) |
| [#221](https://github.com/JdeRobot/RoboticsApplicationManager/pull/221)        | [#218](https://github.com/JdeRobot/RoboticsApplicationManager/issues/218)          | Support for rclpy.spin_once()| [Week 3 Blog](https://theroboticsclub.github.io/gsoc2025-Ashish_Ramesh/posts/Week-3/) |
| [#228](https://github.com/JdeRobot/RoboticsApplicationManager/pull/228)        | [#227](https://github.com/JdeRobot/RoboticsApplicationManager/issues/227)          | Frequency control using rate| [Week 4 Blog](https://theroboticsclub.github.io/gsoc2025-Ashish_Ramesh/posts/Week-4/) |
| [#216](https://github.com/JdeRobot/RoboticsApplicationManager/pull/216), [#230](https://github.com/JdeRobot/RoboticsApplicationManager/pull/230)        | [#239](https://github.com/JdeRobot/RoboticsApplicationManager/issues/239)          | Branch Sync and PR for production branch | [Week 5 Blog](https://theroboticsclub.github.io/gsoc2025-Ashish_Ramesh/posts/Week-5/), <br> [Week 9 Blog](https://theroboticsclub.github.io/gsoc2025-Ashish_Ramesh/posts/Week-9/) |
| [Robotics Academy Solutions <br> (This is a private repo)](https://github.com/JdeRobot/RoboticsAcademy-solutions) |
| [#100](https://github.com/JdeRobot/RoboticsAcademy-solutions/pull/100), [#103](https://github.com/JdeRobot/RoboticsAcademy-solutions/pull/103)         | [#98](https://github.com/JdeRobot/RoboticsAcademy-solutions/issues/98), [#102](https://github.com/JdeRobot/RoboticsAcademy-solutions/issues/102)          | Follow line ROS Native Solution | [Week 5 Blog](https://theroboticsclub.github.io/gsoc2025-Ashish_Ramesh/posts/Week-5/), <br> [Week 6 Blog](https://theroboticsclub.github.io/gsoc2025-Ashish_Ramesh/posts/Week-6/) |
| [#105](https://github.com/JdeRobot/RoboticsAcademy-solutions/pull/105), [#111](https://github.com/JdeRobot/RoboticsAcademy-solutions/pull/111)         | [#104](https://github.com/JdeRobot/RoboticsAcademy-solutions/issues/104), [#108](https://github.com/JdeRobot/RoboticsAcademy-solutions/issues/108)          | Vacuum Cleaner ROS Native Solution | [Week 7 Blog](https://theroboticsclub.github.io/gsoc2025-Ashish_Ramesh/posts/Week-7/), <br> [Week 8 Blog](https://theroboticsclub.github.io/gsoc2025-Ashish_Ramesh/posts/Week-8/) |
| [#99](https://github.com/JdeRobot/RoboticsAcademy-solutions/pull/99), [#114](https://github.com/JdeRobot/RoboticsAcademy-solutions/pull/114), [#115](https://github.com/JdeRobot/RoboticsAcademy-solutions/pull/115), [#116](https://github.com/JdeRobot/RoboticsAcademy-solutions/pull/116)         | [#109](https://github.com/JdeRobot/RoboticsAcademy-solutions/issues/109)          | Branch Sync and PR for production branch | [Week 9 Blog](https://theroboticsclub.github.io/gsoc2025-Ashish_Ramesh/posts/Week-9/) |

---

### Future Work

The refactoring carried out during this project has been designed with scalability in mind, enabling ROS 2 native support for all exercises in the Robotics Academy framework. This foundation opens the door for future contributions, where additional exercises can be seamlessly ported to ROS 2 with minimal effort. I look forward to continuing my involvement by extending ROS 2 native support to more exercises in the future.

Another important area for improvement is addressing the current limitation with the get_logger function, which does not display logs on the VNC console. Fixing this will significantly enhance the user experience by providing clearer runtime feedback during exercise execution. The open issue for this can be found [here](https://github.com/JdeRobot/RoboticsApplicationManager/issues/222).

---

### Conclusion

Participating in Google Summer of Code 2025 has been an incredibly rewarding journey. This project not only strengthened my technical expertise in ROS 2 and large-scale software integration but also gave me the opportunity to contribute meaningfully to open-source.

Collaborating with the JdeRobot community has been a highlight of this experience. I gained valuable insights into open-source workflows, collaborative development, and designing solutions that scale for real users.

I would like to express my gratitude to Prof. José María Cañas and the JdeRobot admins for providing this opportunity. A special thanks to my mentors Pedro Arias Pérez, Pawan Wadhwani, Apoorv Garg, and Prajyot Jadhav for their continuous guidance, thoughtful feedback, and encouragement throughout the project. Their support has been instrumental in shaping the success of this work.

---

Thanks for following along with my GSoC journey! It’s been an incredible experience sharing weekly updates and progress throughout the summer. I’m grateful for the guidance, support, and feedback I’ve received along the way.

With this final post, I’ll be signing off but I’m excited to see how these contributions evolve and continue to benefit the community.

With gratitude, signing off — 


_Ashish_
