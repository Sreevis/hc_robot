# **Health Care Robot**

Health care robot with autonomous navigation feature

## **Core features:**

- Fully Autonomous (using ROS2 navigation Stack).
- Gazebo simulation environment.

## **Tested on:**

Ubuntu 20.04 (ROS2 foxy)

## 1\. Installation

1.  Install ROS2 foxy - [ROS Foxy Debian Installation](https://docs.ros.org/en/foxy/Installation/Ubuntu-Install-Debians.html)
2.  Set up hcr packages

`>mkdir -p hcr_ws/src`

`>cd hcr_ws/src`

`>git clone https://github.com/Sreevis/hc_robot.git`

`>cd ..`

`>source /opt/ros/foxy/setup.bash`

`>colcon build --symlink-install`

## **2\. Quick Start**

**Important: Always remember to source the path while opening each terminals**

**ie. Do this for each terminal**

`>source /opt/ros/foxy/setup.bash`

`>source install/setup.bash`

To display the robot in rviz

`>ros2 launch hcr_description display.launch.py`

Launch empty world in gazebo

`>ros2 launch hcr_gazebo hcr_world.launch.py`
