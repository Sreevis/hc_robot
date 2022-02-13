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

**ie. Do this in every terminal you opens**

`>source /opt/ros/foxy/setup.bash`

`>source install/setup.bash`

To display the robot in rviz

`>ros2 launch hcr_description display.launch.py`

Launch empty world in gazebo

`>ros2 launch hcr_gazebo hcr_world.launch.py`

To run the robot in teleop mode:

`>ros2 run teleop_twist_keyboard teleop_twist_keyboard`
Press 'i' to move forward ..

