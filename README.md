## Introduction 
This project aims to create an interactive digital twin of industrial robotic arms for maintenance monitoring and virtual commisioning. The project is currently in the early stages of development and has only interfaced with Universal Robot arm and OnRobot gripper.

This project uses a number of tools:
- ROS & Moveit: backbone for interfacing and controlling robot hardware
- Unity: design GUI and control physics-based behaviors to virtual robot
- Mongodb: data storing and processing
- WISE-PaaS IoTSuite: monitoring dashboard

*This repo contains packages for using in ROS only. Follow the instruction to install other related repos from Telepatia

## Demo
### Setup for ROS
- Create catkin workspace: `mkdir -p catkin_ws/src && cd catkin_ws`

- Follow Moveit setup tutorial: [Moveit Getting Started](http://ros-planning.github.io/moveit_tutorials/doc/getting_started/getting_started.html "Moveit Getting Started") and [Moveit MoveGroup Demo](https://ros-planning.github.io/moveit_tutorials/doc/move_group_python_interface/move_group_python_interface_tutorial.html "Moveit MoveGroup Demo")

- Install driver for Universal Robot and follow [driver setup](https://github.com/UniversalRobots/Universal_Robots_ROS_Driver "driver setup") tutorial: `git clone https://github.com/UniversalRobots/Universal_Robots_ROS_Driver.git src/Universal_Robots_ROS_Driver`

- Install driver for OnRobot Gripper and follow [driver setup](https://github.com/Osaka-University-Harada-Laboratory/onrobot.git "driver setup") tutorial: `git clone https://github.com/Osaka-University-Harada-Laboratory/onrobot.git src/onrobot`

- Install Universal Robot description: `git clone -b melodic-devel https://github.com/ros-industrial/universal_robot.git src/universal_robot`

- Install ROS-TCP-Endpoint (for connecting to Unity): `git clone https://github.com/Unity-Technologies/ROS-TCP-Endpoint src/ros_tcp_endpoint`

- Clone this repo: `git clone https://github.com/Takikoi/telepatia_digitwin.git src/telepatia_digitwin`

- Build & activate the packages: `catkin_make && source devel/setup.bash`

### Setup for Unity
- Clone digital twin unity repo outside catkin workspace: `git clone https://github.com/Takikoi/Telepatia_Unity_Digitwin.git`
- Open UnityHub, add and open this unity project.

### Reference
- [Unity Robotic Hub](https://github.com/Unity-Technologies/Unity-Robotics-Hub "Unity Robotic Hub")