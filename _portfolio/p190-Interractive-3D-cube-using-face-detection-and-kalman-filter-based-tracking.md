---
title: "Interractive 3D cube using face detection and kalman filter based tracking"
excerpt: "Created an interractive 3D cube using only OpenCV and numpy. Rendering was also done using oply OpenCV and not using OpenGL<br/><img src='/images/pixocube.gif'>"
collection: portfolio
---

PixoCube is a digital version of photo cubes that people usually gift others. It is basically a 3D cube with different images consisting of different sides of the cube. The interesting part of this project is 
I used concepts of camera projection and only opencv functions to render the cube. Moreover the camera view point is rendered such that it shifts based on the movement of users face.  

Project in brief
================

I created this project as a fun application of various fundamental concepts that I have learnt . I have mentioned how I have used these concepts to develop
various parts of this project.
* Understanding all the components of a **camera projection matrix.**
* Developing a virtual camera using a **self defined virtual camera class.**
* Calculating pixel coordinates of vertices of a **3D cube when projected into the virtual camera**.
* Using the projected pixel coordinates and perspective transform, **rendering sides of the cube** with different images.
* Using dlib based face detection method and controling camera position coordinates as the user moves her/his face, giving the 3D effect.
* Created a python wrapper for the C++ based code.

| **Projected points of 3D cube in virtual camera** | **Rendered faces using the projected points** |
| :--------------------------------------------: | :----------------------------------------: |
|![](https://github.com/kaustubh-sadekar/PixoCube/blob/master/proj1.gif) | ![](https://github.com/kaustubh-sadekar/PixoCube/blob/master/proj2.gif) |

<p align='center'>
  **Rendering images on the cube**
</p>
|![](https://github.com/kaustubh-sadekar/PixoCube/blob/master/min1.png) | ![](https://github.com/kaustubh-sadekar/PixoCube/blob/master/min2.png)|
| :------------------------------------------------------------------: | :----------------------------------: |




