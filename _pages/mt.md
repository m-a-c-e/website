---
layout: archive
title: ""
permalink: /mt/
author_profile: true
redirect_from:
  - /resume
---

{% include base_path %}
### Multi-threading
This is a simulation generated in OpenGL using multi-threading.
- The physics of the sphere is such that the UAVs are attracted to the surface of the sphere
- The UAVs perform random motion while also colliding with each other
- The velocities and acceleration of each UAV is controlled by its own thread
- Incoroporated thread-saftey and collision detection across threads

<p align="middle">
  <img src="http://m-a-c-e.github.io/website/files/buzzy.gif" width="700" height="400"/>
  <figcaption align="middle"> Rendering using OpenGL and multi-threading using std::threads in C++ </figcaption>
</p>
