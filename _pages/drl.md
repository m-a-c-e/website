---
layout: archive
title: ""
permalink: /drl/
author_profile: true
redirect_from:
  - /resume
---

{% include base_path %}
### Control Policy Using Deep Reinforcement Learning (in progress)
This is my robotics capstone project, where the goal is to build a control policy for tracking a wall at a desired distance. Since I like to work on algorithms from the ground up, I have chosen this relatively simple task, but in exchange, I get a fine grained idea on how to deploy algorithms from scratch. The only libraries used are ROS and gazebo packages, pytorch and numpy.

- The control policy is a three layer MLP with a tanh activation
- The input to the control policy are the 360 degree lidar measurements from the robot sensor
- The only action that the robot is allowed to take is setting its angular velocity between -1 and 1 rad/s, and hence the tanh activation function. The linear velocity is set to a constant of 0.1 m/s
- The loss for a given episode is a summation of future expected rewards at each time step, calcualted using temporal difference learning.
- The simulation is run in gazebo with turtlebot3 and custom world files

<p align="middle">
  <img src="http://m-a-c-e.github.io/website/files/right_turns.gif" width="400" />
  <img src="http://m-a-c-e.github.io/website/files/left_turns.gif" width="400" />
  <figcaption align="middle"> The training (left) and testing (right) environments in gazebo. The robot was trained only for 20 percent of the track (left) but is still able to complete it while making 90 degree left and right turns. While never trained on the track on the right, it still manages to complete it without colliding with the wall.</figcaption>
</p>
