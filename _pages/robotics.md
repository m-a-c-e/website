---
layout: archive
title: "Computer Vision"
permalink: /robotics/
author_profile: true
redirect_from:
  - /resume
---

{% include base_path %}
### Object Tracking and Obstacle Avoidance
The goal of this project was to use lidar and camera input to navigate a maze. Two main algorithms leading up to it are shown below in object tracking and obstacle avoidance. The major steps involved were as follows:
- For object tracking, read the image from the camera and get the centre of the image
- Turn the robot based on the pixel disparity between the centre of the camera and image centre using PID control
- For obstacle avoidance, once the obstacle is detected, using the lidar measurements in front of the robot, make the robot parallel to the wall.
- Next, move the robot parallel to the wall using PID control untill the obstacle is cleared
- Once the obstacle is cleared, re-oreient the robot to towards the goal using in-built IMU

<p float="left">
  <img src="http://m-a-c-e.github.io/website/files/object_tracking.gif" width="100" />
  <img src="http://m-a-c-e.github.io/website/files/obstacle_avoidance.gif" width="100" /> 
</p>

![Alt Text](http://m-a-c-e.github.io/website/files/object_tracking.gif)

![Alt Text](http://m-a-c-e.github.io/website/files/obstacle_avoidance.gif)

![Alt Text](http://m-a-c-e.github.io/website/files/control.gif)


