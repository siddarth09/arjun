# ARJUN robot
Arjun is a basic robot with camera and laser scanner similar to hardware based robot configuration, this can be used for educational, experimental learning of ROS


![ARJUN](https://user-images.githubusercontent.com/60263608/130914758-250ca2b8-dc53-48ce-a078-837f06960a6d.png)

## Installation

```bash
cd ~/catkin_ws/src
git clone https://github.com/siddarth09/arjun.git
git clone https://github.com/siddarth09/arjunamr_description.git
cd ..
catkin_make
```
Note:
> Please change the catkin_ws to your custom rosworkspace name 

## TELE-OPERATION
The teleop keys are customised according to the robot configuration ie; the hardware bot, you can make changes to the friction between wheels or increase the max speed so the wheels of your bo motors can move faster

```bash
roslaunch arjun teleop_key.launch
```

The above command can be used to run the teleop node in your pc 

## WORLD SIMULATION

This robot world can be simulated in Gazebo for testing various problems, the house contains three rooms with one narrow passage to check robot navigation in such conditions

To run the house simulation 
```bash
roslaunch arjun amr_house.launch
```
To run maze_1 simulation
```bash
roslaunch arjun arjun_maze_1.launch
```
## SLAM 
Simultaneous localization and mapping (SLAM) is the computational problem of constructing or updating a map of an unknown environment while simultaneously keeping track of an agent's location within it. Here we are using frontier mapping, gmapping, Hector-slam packages to map the given environment for navigation purposes

To run Gmapping package
``` bash
roslaunch arjun arjun_gmapping.launch
```

## NAVIGATION STACK

Navigation stack is an important for autonomous navigation, ROS has builtin packages which helps you setup the entire navigation stack very easily and fine tune the
path planning algorithms accordingly. 

- GLOBAL COSTMAP:
  In the global costmap is everything the robot knows from previous visits and stored knowledge e.g. the map
  
- LOCAL COSTMAP:
 In the local costmap is everything that can be known from the current position with the sensors right know
 
Here ROS comes with default DWA or **DYNAMIC WINDOW APPROACH** which uses Dijkastra's algorithm to find the shortest path to the given X,Y coordinates

To run the navigation stack 

```bash
roslaunch arjun arjun_navigation.launch
```
#### MAKE SURE YOU HAVE MAPPED YOU ENVIRONMENT PROPERLY
