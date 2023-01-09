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

- For object tracking, read the image from the camera and get the centre of the image
- Turn the robot based on the pixel disparity between the centre of the camera and image centre using PID control
- For obstacle avoidance, once the obstacle is detected, using the lidar measurements in front of the robot, make the robot parallel to the wall.
- Next, move the robot parallel to the wall using PID control untill the obstacle is cleared
- Once the obstacle is cleared, re-oreient the robot to towards the goal using in-built IMU

<p align="middle">
  <img src="http://m-a-c-e.github.io/website/files/right_turns.gif" width="400" />
  <img src="http://m-a-c-e.github.io/website/files/left_turns.gif" width="400" />
  <figcaption align="middle"> Object tracking (left) and Obstacle aovidance (right) </figcaption>
</p>
