# LIDAR-Obstacle-Avoidance
Robot obstacle avoidance system using LIDAR module on a Turtlebot3 Simulator

# Introduction
This program is an algorithm implementation of LIDAR (Light Detection and Ranging) sensor for Turtlebot3 on a simulator. The simulator will show how LIDAR is used to avoid obstacle. LIDAR works similarly like SONAR, but uses laser. The laser will spread from LIDAR module and any object that is hit by the laser will bounce back to the LIDAR sensor and LIDAR will detect the range of the object. The range is then processed within robot's ROS node. If the object's range is less than certain value, then the robot will execute a maneuver to avoid hitting the detected object.

The simulator is provided ROBOTIS-GIT project. This program is only the algorithmic implementation of the navigation and obstacle avoidance system using the data from LIDAR sensor.

<br>

# Installation and Program Execution

The program was developed using ROS Noetic and Ubuntu 20.04 LTS. Try to use these versions. Follow below instruction to run the program

```
$ git clone https://github.com/farrel-a/LIDAR-Obstacle-Avoidance.git
$ cd LIDAR-Obstacle-Avoidance
$ cd lidar_ws/src
$ git clone https://github.com/ROBOTIS-GIT/turtlebot3_msgs.git -b noetic-devel
$ git clone https://github.com/ROBOTIS-GIT/turtlebot3.git -b noetic-devel
$ cd .. && catkin_make
$ cd src
$ git clone https://github.com/ROBOTIS-GIT/turtlebot3_simulations.git 
$ cd .. && catkin_make
$ source devel/setup.bash       #for bash
# or
$ source devel/setup.zsh        #for zsh
$ export TURTLEBOT3_MODEL=waffle
$ roslaunch turtlebot3_movement move_robot.launch
```
# Result

![](https://i.ibb.co/rQj6T2r/Screenshot-from-2022-01-20-12-32-29.png)
