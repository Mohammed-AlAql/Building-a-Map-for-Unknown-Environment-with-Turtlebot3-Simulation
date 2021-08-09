# Building-a-Map-for-Unknown-Environment-with-Turtlebot3-Simulation

Building a map for unkown environment with SLAM using ROS, Simultaneous localization and mapping (SLAM) concerns the problem of a robot building or updating a map of an unknown environment while simultaneously keeping track its location in that environment. it was executed using Ubuntu 16.04.6 LTS and ROS kinetic

Install the SLAM module

* sudo apt install ros-kinetic-slam-gmapping
Building a map of environment for testing SLAM
Start Gazebo in a new terminal window, This will lanuch an environment for testing SLAM

* roslaunch turtlebot3_gazebo turtlebot3_world.launch
Start SLAM in a new terminal tab

* roslaunch turtlebot3_slam turtlebot3_slam.launch slam_methods:=gmapping
in order to build the map of the environment you need to navigate through the entire environment, you can do this by either starting autonomous navigation or manually using keyboard

Start autonomous navigation in a new terminal tab

* roslaunch turtlebot3_gazebo turtlebot3_simulation.launch
or launch key teleop

* roslaunch turtlebot3_teleop turtlebot3_teleop_key.launch
When you draw the entire environment save it using the map_server package, it will be stored in HOME, the last part is responsable for the location of save

* rosrun map_server map_saver -f ~/map

![87581626-ecbd6d80-c6e1-11ea-94be-2606220f037a](https://user-images.githubusercontent.com/85512336/128723272-f4a48f1d-bcc0-47f5-b3ac-4fa88e29c00c.gif)

# Building a map of a house environment
All the steps above are same except lanuch house environment

* roslaunch turtlebot3_gazebo turtlebot3_house.launch
![87581706-0f4f8680-c6e2-11ea-85cb-47aeaa5667e6](https://user-images.githubusercontent.com/85512336/128723345-39fc1bfd-702b-4ee1-a9cf-4693cd3ad61f.png)

