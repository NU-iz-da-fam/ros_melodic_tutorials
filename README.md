# ROS MELODIC TUTORIALS

This tutorial is used when you have already installed ros and want to get used to with ros environment. I will leave a link to install ros below in case you haven't installed yet.

Here is the link: http://wiki.ros.org/melodic/Installation/Ubuntu

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

## Create and launch nodes
1. Create .cpp file that contains node you want to run.
2. Create launch file which will run your .cpp file.
3. Add executable script to CMakeList.txt file.

After that, run codes below:
```
cd [workspace name]
source  [workspace name]/devel/setup.bash
catkin_make
roslauch [folder containing launch file] [launch file name].lauch
```
