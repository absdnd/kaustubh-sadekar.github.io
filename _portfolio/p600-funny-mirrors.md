---
title: "Air Drums using OpenCV"
excerpt: "Used color based segmentation to create a fun application of air drums<br/><img src='/images/air-drums.gif'>"
collection: portfolio
---

Augmented reality drums based on concepts of computer vision and image processing. A fun application created to enable users to play virtual drums anywhere simply by using colour tags.

Project in brief
================

I created this project as a fun application of the HSV based color segmentation method. Some key steps of the project are mentioned as follows:
* Used blue color detection with OpenCV.
* Performed blue color detection only in a specific ROI to improve real time performance.
* If a blue color object is detected inside this ROI then sound of drums is played using pygames.

| Image showing ROI | Air drums interface with augment drums |
| :---: | :---: |
| ![](/images/verbose.jpg) | ![](/images/air-drums.png) |
