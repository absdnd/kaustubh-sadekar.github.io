---
title: "Low-Cost Custom Stereo Camera From USB Webcams"
excerpt: "Using two USB webcams a low cost stereo camera can be developed for depth perception<br/><img src='/images/pgNet.gif'>"
collection: portfolio
---

Project in brief
================

Stereo cameras are a standard solution for depth perception. Most of the industrial-grade stereo cameras come with well written APIs and SDKs to make it easy for the developers to get the depth data from the camera with just a few code lines. However, these cameras are quite expensive compared to the regular USB cameras.

I learned the fundamental concepts of stereo vision from CS 763 - Computer Vision at IIT Bombay (sit through - without credits). This motivated me to develop my low-cost stereo camera from two USB cameras and write my software to get the setup's depth information. The software is written in Python as well as C++. 

Design and Fabrication
----------------------

A 3D printed box was used to ensure that the cameras do not move and give it a nice look! My childhood friend and neighbor [**Mandar Kadwekar**]() designed the
 3d box.

<p align="center">
  <img src='/images/cameraDesign.gif'>
</p>
<p align="center">
  Stages of StereoCam setup
</p>

Stereo Calibration
------------------

I created a **custom stereo calibration grid using ArUco markers**. It is easier to detect compared to the checkerboard pattern. The marker corner detection is done using 
ArUco class in OpenCV.

<p align="center">
  <img src='/images/calibration.gif'>
</p>
<p align="center">
  Capturing images for calibration using the custom calibration grid
</p>


Depth Estimation and 2.5 D Projection
-------------------------------------

Using the depth map and the calibrated camera parameters, each pixel's depth is estimated, and a 3D point cloud is generated. This is usually called a 2.5 D projection.
StereoSGBM method is used to estimate the disparity map, and the WLS filter is used to refine the disparity map. The disparity map information and intrinsic camera parameters 
are used to get the 2.5 D representation.

The point cloud generated in the above process is displayed using Open3D.

<p align="center">
  <img src='/images/stereo3D.gif'>
</p>
<p align="center">
  Live pointcloud displayed using Open3D
</p>




