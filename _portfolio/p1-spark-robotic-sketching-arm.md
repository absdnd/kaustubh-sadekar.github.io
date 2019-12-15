---
title: "SPARK a robotic sketching arm"
excerpt: "A 3DOF robotic arm capable of sketching images using ROS and OpenCV <br/><img src='/images/500x300.png'>"
collection: portfolio
---

SPARK is a 3DOF robotic arm capable of sketching any image given to it as input. The robot takes an input image, converts it to binary format, uses the binary image to decide where to draw the pixels and ultimately it creates a sketch of the input image!!


Motivation
==========

I liked sketching in childhood but I was never so good at it. Although drawing is fun as a hobby but when we have to draw accurate engineering figures using so many tools with hand .... I never enjoyed that. That's when the idea for SPARK came to my mind. I thought of making a robot that could do all these complicated drawings for me while I did some other productive work.


Project in brief
================

I used OpenCV to convert the input image into a binary format which helps the robot to understand *what/where* to draw. Using inverse kinematics of the robot angles for the servo motors were deterined for the movement of the robot. The software was written using the ROS framework in python language. Initially MATLAB was used to understand the dynamics of the robot before fabricating it. The diagram below explains the software design based on ROS framework for SPARK.

