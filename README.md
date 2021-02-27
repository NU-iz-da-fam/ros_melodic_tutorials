# ROS MELODIC TUTORIALS

This tutorial is used when you have already installed ros and want to get used to with ros environment.
## Create workspace in ros-melodic
```
mkdir [workspace name]
cd [workspace name]
source /opt/ros/melodic/setup.bash
mkdir src
catkin_make
```

## Create package in workspace
Imagine that you are in workspace created above.
```
cd src
source [workspace name]/devel/setup.bash
catkin_create_pkg [package name] roscpp rospy std_msgs
```
If package is created correctly, you will have CMakeList file, include, package and src folder. You can add more dependencies (roscpp, rospy, ...) when creating package.
