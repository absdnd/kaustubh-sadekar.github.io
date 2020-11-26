---
title: "Handwritten content binarization using Deep CNN"
excerpt: "A deep convolutional neural network to segment hand written content from a given page<br/><img src='/images/pgNet.gif'>"
collection: portfolio
---

Project in brief
================

*Manuscript in process*

A large amount of information about our past is handwritten. Hence it is a common practice to understand the content in such handwritten documents.
Constant attempts have been made to understand the content in such handwritten documents using computer vision and deep learning.
It is observed that these pages have different types of ruled lines and textures. These attributes act as noise to deep learning models used to understand content written in the documents. Thus, researchers have made several attempts to segment only the written content and eliminate the page lines and texture. This model is inspired by [1]

Some key points of the project are as follows:

* CNN based model trained from scratch.
* Model can segment the handwritten content from different types of pages.
* Next attempt is to improve the model performance on various public datasets.

<p align="center">
  <img src='/images/pgNet.gif'>
</p>

It is interesting to observe how the model can perform well even for very crumpled pages and curved pages. Test images for the results shown above were directly taken from the internet to evaluate the model performance. Links to the original pictures are:

* [Link 1](https://www.google.com/url?sa=i&url=https%3A%2F%2Fwww.bbc.com%2Fnews%2Fworld-asia-india-49631186&psig=AOvVaw3ubr50bb9z0C4unEwWxXmc&ust=1606506187863000&source=images&cd=vfe&ved=0CAIQjRxqFwoTCPiHl-_8oO0CFQAAAAAdAAAAABAc)
* [Link 2](https://www.google.com/url?sa=i&url=https%3A%2F%2Fwww.nytimes.com%2F2020%2F05%2F16%2Fus%2FAP-exams-test-glitch-virus.html&psig=AOvVaw0k6l69RIknM5klw9POZiqK&ust=1606506267025000&source=images&cd=vfe&ved=0CAIQjRxqFwoTCJiD75eDoe0CFQAAAAAdAAAAABAM)
* [Link 3](https://www.google.com/url?sa=i&url=https%3A%2F%2Fwww.pinterest.ca%2Fpin%2F147281850293176668%2F&psig=AOvVaw2t2P89Fw2sKnr1nNze_QKp&ust=1606507404351000&source=images&cd=vfe&ved=0CAIQjRxqFwoTCPjt64CGoe0CFQAAAAAdAAAAABAD)
* [Link 4](https://www.google.com/url?sa=i&url=https%3A%2F%2Fwww.pinterest.com%2Fpin%2F369084131942387580%2F&psig=AOvVaw2t2P89Fw2sKnr1nNze_QKp&ust=1606507404351000&source=images&cd=vfe&ved=0CAIQjRxqFwoTCOCH44GGoe0CFQAAAAAdAAAAABAD)

**References**

[1] A. K. Bhunia, A. K. Bhunia, A. Sain and P. P. Roy, "Improving Document Binarization Via Adversarial Noise-Texture Augmentation," 2019 IEEE International Conference on Image Processing (ICIP), Taipei, Taiwan, 2019, pp. 2721-2725, doi: 10.1109/ICIP.2019.8803348.
