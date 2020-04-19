---
title: "SPARK a robotic sketching arm"
excerpt: "A 3DOF robotic arm capable of sketching images using ROS and OpenCV <br/><img src='/images/500x300.png'>"
collection: portfolio
---

SPARK is a 3DOF ROS based robotic arm capable of sketching any image given to it as input. The robot takes an input image, converts it to binary format, uses the binary image to decide where to draw the pixels and ultimately it creates a sketch of the input image!!


Motivation
==========

I liked sketching in childhood but I was never so good at it. Although drawing is fun as a hobby but when we have to draw accurate engineering figures using so many tools with hand .... I never enjoyed that. That's when the idea for SPARK came to my mind. I thought of making a robot that could do all these complicated drawings for me while I did some other productive work.


Project in brief
================

ROS based project consisting of three major nodes.
* Vision node uses **OpenCV** to convert the input image to binary image and states points to be sketched.
* **Inverse kinematics** node to determine angles of the robot joints.
* Embedded node that controls the servo motors to move the robotic arm.


Update Version 2.0
==================

Closed loop control using vision based feedback system integrated with ROS
* Vision based feedback node, using AruCo marker, publishes realtime robot joint pose.
* Closed loop control node publishes the motor angles, which are subscribed by the embedded node.

<p align='center'>
  <img src='/images/spark-pid1.gif'>
</p>
<p align='center'>
    Results for P controller
</p>

<p align='center'>
  <img src='/images/2.gif'>
</p>
<p align='center'>
    Results for PD controller
</p>
