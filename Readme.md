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

## **3\. Autonomous navigation**

`>sudo apt install ros-foxy-robot-localization`

`>sudo apt install ros-foxy-slam-toolbox`

`>sudo apt install ros-foxy-navigation2`

`>sudo apt install ros-foxy-nav2-bringup`


**SLAM**

`ros2 launch hcr_nav nav_office_world.launch.py`

After setting up hospital world you can run `nav_office_world.launch.py`

`ros2 launch slam_toolbox online_async_launch.py`

`ros2 launch nav2_bringup navigation_launch.py`

**Setting up hospital world**
Clone the aws_hospital world in to your ros workspace. Make sure to add the required model paths before running hospital world. For more please go through [2] 

**TODO**
- [ ] FIne tuning for efficient resource utilization
- [ ] FIne tuning for improving performance accuracy


**Reference**
1. [ROS2 Navigation](https://navigation.ros.org/getting_started/index.html)
2. [AWS hospital world](https://github.com/aws-robotics/aws-robomaker-hospital-world/tree/ros2)

**Bugs and Fixes**

1. An error I faced while setting up gazebo hospital world . Can be solved by sourcing gazebo path.
```
[gzclient   -2] gzclient: /usr/include/boost/smart_ptr/shared_ptr.hpp:734: typename boost::detail::sp_member_access<T>::type boost::shared_ptr<T>::operator->() const [with T = gazebo::rendering::Camera; typename boost::detail::sp_member_access<T>::type = gazebo::rendering::Camera*]: Assertion `px != 0' failed.
```

Solution
`. /usr/share/gazebo/setup.sh` 
