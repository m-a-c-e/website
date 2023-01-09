---
layout: archive
title: ""
permalink: /drl/
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

<p align="middle">
  <img src="http://m-a-c-e.github.io/website/files/object_tracking.gif" width="400" />
  <img src="http://m-a-c-e.github.io/website/files/obstacle_avoidance.gif" width="400" />
  <figcaption align="middle"> Object tracking (left) and Obstacle aovidance (right) </figcaption>
</p>

### Line Follower Robot
<p>
  <img style="float: right;" src="http://m-a-c-e.github.io/website/files/control.gif" width="200" height="400"/>
</p>
The goal of this project was to build a line follower robot using infrared sensors which can detect bright white color. The gif below shows the demo from the final competition wherein the robot has to follow the line and complete the track in minimal amount of time. We used PID control and placed 4th in the competition.



