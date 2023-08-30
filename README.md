# Bumpybot Simulation in Gazebo

## Launch Robot in Gazebo

In order to spawn BumpyBot in turtlebot3 house, run the following command:
```
roslaunch trikey_gazebo turtle_house.launch
```

### Launch Arguments
- `<arg name="teleop" default="true">` : Launches keyboard teleoperation node
- `<arg name="roller" default="false"` : Spawns the robot with rollers. Note: Omnidirectional sliding movement is not yet implemented. The robot uses `planar_move` plugin instead.
- `<arg name="vel_topic" default="/trikey/base_controller/cmd_vel" />` : cmd_vel topic name
- `<arg name="icp_odom" default="false" />` : Use ICP odometry source. It cannot be used with `planar_move` plugin.


## Robot Navigation in Gazebo
```
roslaunch trikey_gazebo gazebo_slam_stack.launch
```

This launches following:
- `trikey_gazebo turtle_house.launch`
- `bumpybot_navigation slam_toolbox.launch`
- `bumpybot_navigation move_base.launch`
- `Rviz`

The robot spawns in the turtlebot3 house and starts SLAM. You can set a target pose in Rviz using Move Goal to both explored and unexlplored areas. The robot will navigate to the target pose while avoiding obstacles.



<!-- 
### What is this repository for? ###

Run a simulation of Trikey/Bumpybot on Gazebo.

### How do I get set up? ###

For now, follow the instructions provided on 
[this](https://carlosgonzalez-hcrl.atlassian.net/wiki/spaces/TRIKEY/pages/33007/Running+Trikey+Simulation) 
confluence page. -->

