---
title: "Analysis of visual SLAM methods"
excerpt: "Study and analysis of LSD-SLAM, CUBEMAP SLAM and ORB-SLAM for omnidirectional cameras<br/><img src='/images/SLAM.gif'>"
collection: portfolio
---

This is a small portion of my work as a research associate at IIT Bombay. Due to institution policy, I am unable to share more details and 
results as I am supposed to keep it confidential. 

Project in brief
================

The main problem statement was to develop a SLAM algorithm for a manually operated robot. The robot dynamics posed a huge challenge for the existing SLAM algorithms to perform well without any modifications. Moreover, an omnidirectional camera was used in the robot.
The following are some key points of what we did as an attempt to solve the problem statement.

* Studied and tested LSD SLAM algorithm for Narrow FOV cameras and Omnidirectional Cameras after using undistortion.
* Studied and tested the CubeMap SLAM algorithm for wide-angle lens cameras.
* Improved the existing official CubeMap SLAM repository code with the following contributions:
  * Made the code ROS compatible.
  * Created a GUI to determine the parameters corresponding to the omnidirectional camera used in the robot.
  * Created an efficient library to convert video streams from the omnidirectional camera to CubeMap in real-time for online operation. The original repository needs all the frame sequences to be stored before starting the mapping process, making it only useful for offline mapping.
  * Created a conversion code that enables us to test Cubemap SLAM for horizontally placed cameras. The original repository does not provide any facility to perform mapping using a camera in horizontal (parallel to the ground and facing the ceiling) orientation.

<p align='center'>
  <img src="/images/CmapSLAM.gif">
</p>
<p align='center'>
  Sample output of CubeMap SLAM for horizontally placed camera
</p>

<p align='center'>
  <img src="/images/SLAM.gif">
</p>
<p align='center'>
  Sample output of LSD SLAM for rpi camera
</p>



