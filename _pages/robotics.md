---
layout: archive
title: ""
permalink: /robotics/
author_profile: true
redirect_from:
  - /resume
---

{% include base_path %}
### 3DOF Manipulator Dynamics and Control (Georgia Tech - Spring 2023)
The goal of this project was to design a controller for a simplified PUMA robot (3-DOF) so that it can achieve a reference task space trajectory. The procedure for designing the controller was as follows:
- Use lagranges equation to find the torque required at each joint to compensate for gravitational force
- Determine the error, derivative of error and integral of error between the reference and measured end effector position
- Scale these error with PID gains to find the froce exerted by an imaginary reciprocal wrench (Force exerted will be zero when the error is zero)
- Compute the jacobian matrix (3x3) as a function of joint angles
- Compute the reciprocal wrench Torque = J' * F
- Tune the gains so that the end point is stable throughout the trajectory
- See below for results for reference and reproduced trajectory

<p align="middle">
  <img src="http://m-a-c-e.github.io/website/files/puma_circles.gif" width="400" />
  <img src="http://m-a-c-e.github.io/website/files/2_reproduced_trajectory.png" width="400" />
  <figcaption align="middle"> Robot (left) executing the input trajectory (right) </figcaption>
</p>


<p align="middle">
  <img src="http://m-a-c-e.github.io/website/files/puma_robots.gif" width="400" />
  <img src="http://m-a-c-e.github.io/website/files/produced_trajectory_3(1).png" width="400" />
  <figcaption align="middle"> Robot (left) executing the input trajectory (right) </figcaption>
</p>


### Object Tracking and Obstacle Avoidance (Georgia Tech - Fall 2021)
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

### Line Follower Robot (Purdue - Fall 2019)
<p>
  <img style="float: right;" src="http://m-a-c-e.github.io/website/files/control.gif" width="200" height="400"/>
</p>
The goal of this project was to build a line follower robot using infrared sensors which can detect bright white color. The gif below shows the demo from the final competition wherein the robot has to follow the line and complete the track in minimal amount of time. We used PID control and placed 4th in the competition.



