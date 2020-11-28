---
title: "Interactive 3D cube using face detection and Kalman filter based tracking"
excerpt: "Created an interactive 3D cube using only OpenCV and NumPy. Rendering was also done using only OpenCV and not using OpenGL<br/><img src='/images/pixocube.gif'>"
collection: portfolio
---

PixoCube is a digital version of photo cubes that people usually gift to others. It is a 3D cube with different images consisting of different sides of the cube. This project's exciting part is that I used camera projection concepts and only OpenCV functions to render the cube. Moreover, the camera viewpoint is rendered such that it shifts based on the movement of the user's face.  

Project in brief
================

I created this project as a fun application of various fundamental concepts that I have learned. I have mentioned how I have used these concepts to develop
multiple parts of this project.
* Understanding all the components of a **camera projection matrix.**
* Developing a virtual camera using a ** self-defined virtual camera class.**
* Calculating pixel coordinates of vertices of a **3D cube when projected into the virtual camera**.
* Using the projected pixel coordinates and perspective transform, **rendering sides of the cube** with different images.
* Using **dlib based face detection** method and controlling camera position coordinates as the user moves her/his face, giving the 3D effect.
* Applying **Kalman Filter for tracking** the face.
* Created a **python wrapper for the C++** based code.

Creating a 3D cube
==================
A cube is initialized with a center at origin and side = 1meter. I created two different classes -one to handle and define the 3D cube and the other for the virtual camera. The cube is initialized when the object for the 3D cube is created. The cube is represented here by its eight vertices.

Creating the virtual camera
===========================
To define a virtual camera, we define a set of matrices representing different properties of a camera. We use the following matrices to describe different properties of the virtual camera : 
* Translation matrix (T): To represent the translation of the camera in the real world.
* Rotation matrix (R) : To represent the camera's rotations about the x, y and z axis.
* Camera matrix (K): To represent the properties of the virtual camera like focal length (f), apparent pixel size (sx), apparent center of the image in pixel coordinates. 
* Using the above matrices, we define the camera projection matrix (P).

Deriving projection of 3D cube vertices in the virtual camera
=============================================================
The camera projection matrix (P) mentioned in the above section is used to find the 3D cube vertices' projection in the camera frame, which means given the camera and cube's position and orientation, we can find the image coordinates for each vertex of the 3D cube. Thus driving the projection is simply a matrix operation that finds the 2d pixel coordinates in the image frame for given 3D coordinates of each cube's vertex. These projected pixel coordinates of the cube vertices are used to render the cube.


| **Projected points of 3D cube in virtual camera** | **Rendered faces using the projected points** |
| :--------------------------------------------: | :----------------------------------------: |
|![](/images/proj1.gif) | ![](/images/proj2.gif) |


Rendering of the 3D cube
========================

We use the image pixel coordinates derived previously to render the final cube. The process of generating the cube consists of the following steps:

* Storing the projected 2d coordinates of vertices for each face of the cube is a list.
* Finding the distance of the center of each face from the camera.
* Selecting and importing images for each face of the cube.
* Rendering faces of the cube by applying perspective warping using image dimensions as source points and the derived 2D coordinates of corners of the cube faces as destination points. The order of rendering is such that the face farthest from the camera is rendered first.

The last step in the process of rendering is performed to ensure the opaque nature of the object. Many advanced algorithms in graphics processing literature perform this task better, but for our case, distance-based sorting works.

**Rendering images on the cube**


| **Rendered cube sample 1** | **Rendered cube sample 2** |
| :------------------------: | :-----------------------: |
|![](/images/min1.png) | ![](/images/min2.png) |


Face tracking for controlling the camera viewpoint
===================================================

Face tracking for controlling the camera viewpoint
The camera viewpoint is changed using face tracking to generate an effect where the rendered cube would feel like a real cube as it will change the perspective with respect to the user's position. Process of updating the camera viewpoint using face tracking consists of the following steps :

* Detecting the face of the user. I am doing this using the face detection method available in dlib. This method returns a list of coordinates of bounding boxes for each face detected by the algorithm.
* Since the application can only support a single user, we index the bounding box coordinates related to the first face detected.
* We use the bounding box values to calculate the center of the bounding box further.
* We use the center's coordinates to map the user's movement and the virtual camera to generate the 3D perspective effect.
* The width of the bounding box is used to control the z coordinates of the virtual camera.
Kalman Filter is used to tracking the face. The software's real-time performance is improved by using Kalman Filter to predict the bounding box position and width, and face detection is used for only 20 percent of the frames to enhance/update the estimates. Some results of face detection and tracking are shown below.

| **Face tracking disabled** | **Face tracking enabled** |
| :------------------------: | :-----------------------: |
|![](/images/gif1.gif) | ![](/images/gif3.gif) |



