---
title: "Air Drums using OpenCV"
excerpt: "Used color based segmentation to create a fun application of air drums<br/><img src='/images/air-drums.gif'>"
collection: portfolio
---

I created this project to play virtual drums anywhere simply by using color tags using OpenCV.

Project in brief
================

I created this project as a fun application of the HSV based color segmentation method. Some key steps of the project are mentioned as follows:
* Used blue color detection with OpenCV.
* Performed blue color detection only in a specific ROI to improve real-time performance.
* If a blue color object is detected inside this ROI, drums' sound is played using pygames.

| Image showing ROI | Air drums interface with augment drums |
| :---: | :---: |
| ![](/images/verbose.jpg) | ![](/images/air-drums.png) |
