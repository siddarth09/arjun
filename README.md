# ARJUN robot
Arjun is a basic robot with camera and laser scanner similar to hardware based robot configuration, this can be used for educational, experimental learning of ROS

![ARJUN](https://user-images.githubusercontent.com/60263608/130731680-80f58b82-b660-4e2c-ad12-5d184d78cf09.png)


## Installation

```bash
cd ~/catkin_ws/src
git clone https://github.com/siddarth09/arjun.git
cd ..
catkin_make
```
Note:
> Please change the catkin_ws to your custom rosworkspace name 

## TELE-OPERATION
The teleop keys are customised according to the robot configuration ie; the hardware bot, you can make changes to the friction between wheels or increase the max speed so the wheels of your bo motors can move faster

`roslaunch arjun teleop_key.launch`

The above command can be used to run the teleop node in your pc 

## HOUSE SIMULATION

This robot world can be simulated in Gazebo for testing various problems, the house contains three rooms with one narrow passage to check robot navigation in such conditions

To run the house simulation 
`roslaunch arjun amr_house.launch`

## SLAM 
Simultaneous localization and mapping (SLAM) is the computational problem of constructing or updating a map of an unknown environment while simultaneously keeping track of an agent's location within it. Here we are using frontier mapping, gmapping, Hector-slam packages to map the given environment for navigation purposes

To run Gmapping package
`roslaunch arjun arjun_gmapping.launch`

