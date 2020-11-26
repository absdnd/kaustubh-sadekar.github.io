---
title: "Fall detection using pose estimation"
excerpt: "Robust fall detection using pose estimation.<br/><img src='/images/FallDetection2.gif'>"
collection: portfolio
---

Project in brief
================

The project aims to detect any scenario where a person is falling on the floor. There are so many scenarios where this can be very useful. In this research project, we plan to create a robust and real-time fall detection algorithm. Our first set of experiments
is focused on testing pre-trained models for pose estimation for fall scenarios. Some of the key points of the projects are as follows:

* Literature survey for selecting a model for pose estimation.
* Testing the [Real-time 2D Multi-Person Pose Estimation on CPU: Lightweight OpenPose](https://arxiv.org/pdf/1811.12004.pdf) on the following datasets
  * [UR Fall detection dataset](http://fenix.univ.rzeszow.pl/~mkepski/ds/uf.html)
  * [Multiple Cameras Fall Dataset](http://www.iro.umontreal.ca/~labimage/Dataset/)
  * [Fall detection Dataset](http://www.falldataset.com/)
* Testing [OpenPose](https://github.com/CMU-Perceptual-Computing-Lab/openpose)

Some of the results are shown below.

<p align="center">
  <img src='/images/FallDetection.gif'>
</p>
<p align="center">
  Test on a sample from UR Fall detection dataset
</p>

<p align="center">
  <img src='/images/FallDetection2.gif'>
</p>
<p align="center">
  Test on a sample from Multi-cameras fall dataset
</p>

<p align="center">
  <img src='/images/FallDetection3.gif'>
</p>
<p align="center">
  Test on a sample from Fall detection dataset
</p>


