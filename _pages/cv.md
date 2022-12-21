---
layout: archive
title: ""
permalink: /cv/
author_profile: true
redirect_from:
  - /resume
---

{% include base_path %}

### Depth from Stereo
The goal of this project was to detect people wearing safety vest around a track loader using cameras. We developed a custom depth from stereo pipeline using two mounted orlaco cameras which streamed images synchronously. The steps in the pipeline were as follows:
- Get the camera calibration and transformation matrices
- Filter the image for safety vest colors using hsv color space in OpenCV
- Detect the centres of the blobs generated - keypoints
- Build SIFT descriptors at these keypoints
- Perform one-to-one matching between keypoints in left and right images - generating pair of keypoints (left and right image)
- Perform triangulaiton using direct linear transform in OpenCV using the pairs of keypoints

<p align="centre">
  <img src="http://m-a-c-e.github.io/website/files/orlaco2.gif"/>
  <img src="http://m-a-c-e.github.io/website/files/orlaco1.gif"/>
  <figcaption align="middle"> The pipeline outputs the distance in meters to the track loader. Left (outdoor) right (indoor) </figcaption>
</p>
