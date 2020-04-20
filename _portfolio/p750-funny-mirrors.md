---
title: "Fun mirrors using OpenCV"
excerpt: "Used color based segmentation to create a fun application of air drums<br/><img src='/images/FunMirrors2.gif'>"
collection: portfolio
---

FunMirrors is another hobby project that I did where I applied my fundamental knowledge of **camera projection matrix, geometry of image formation
and mesh based warping.** 

Project in brief
================

After studying fundamental concepts of image formation and camera projection matrix, while learning about multi-view geometry,
I created this project. Some of the key points of the project are as follows :
* Created a python package `vcam` which is now **availabe on pip**.
  * The package is written in OOP way and contains a **class for virtual camera** and a **class for generating 3D surfaces.**
* A funny mirror can be generated using the meshGen class of the package.
* A virtual camera can be created using the vcam class of the package.
* Using the created camera object we capture the generated 3D surface.
* We finally use these projected 2D points for mesh based warping to generate different funny mirrors effect.

<p align='center'>
  Some examples of funny mirrors
</p>

<p align='center'>
  <img src="/images/FunMirrors2.gif">
</p>

<p align='center'>
  <img src="/images/FunMirrors.gif">
</p>

