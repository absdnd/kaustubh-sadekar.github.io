---
title: "Study-and-implementation-of-various-omnidirectional-camera-models"
excerpt: "Developed virtual camera classes for various omnidirectional camera models<br/><img src='/images/e2feye.gif'>"
collection: portfolio
---

Project in brief
================

As one of my key area of interest is related to perception algorithms related to omnidirectional camera models, I studied the following camera models and 
created a GUI for each model which helps the user to play with various intrinsic and extrinsic camera parameters.
* Pinhole Camera Model
* Brown–Conrady model
* Unified Camera Model
* Extended Unified Camera Model
* Kannala-Brandt Camera Model
* Field-of-View Camera Model
* Double Sphere Camera Model

The idea here was to use the inverse projection function (Unprojection function) to determine the real world coordinate direction, get corresponding spheric coordinates for 
a unit sphere and sample the pixel values from a given 360&deg; image (in equirectangular format).

<p align='center'>
  <img src='/images/distCoeff.gif'>
</p>
<p align='center'>
  GUI for pinhole camera with Brown–Conrady model
</p>

<p align='center'>
  <img src='/images/e2feye.gif'>
</p>
<p align='center'>
  GUI for unified camera model
</p>

