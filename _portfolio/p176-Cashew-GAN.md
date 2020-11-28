---
title: "Cashew GAN - A Generative Adversarial Network to generate different types of cashews"
excerpt: "A generative adversarial network, to generate different kinds of cashews, designed and trained from scratch<br/><img src='/images/CashewGAN.gif'>"
collection: portfolio
---

Project in brief
================

I find it quite interesting to solve various vision-related problems in the food and manufacturing industry domain. One of the hobby projects
I am working on is to sort good and poor quality cashews. While sorting the broken and full cashews is an easy task, there are several grades of
cashews. Specifically, developing a model that can differentiate between cashew splits and whole cashews or good and burnt cashew can be challenging. 

It is sometimes difficult to get enough samples for each kind of cashew. I have learned a lot about GANs but never had a chance to make one from scratch. I planned to create my dataset and developing a GAN to generate new images of cashews. So far, the results are not very realistic, but we can say that they look fair enough. Through this project, I have learned many practical concepts that one needs to know
while creating a GAN from scratch. Some crucial points that helped me in making a stable GAN are as follows:

* Normalizing input
* Using batch normalization 
* Instead of 1 and 0 for real and fake using soft labels random number between 0-0.2 and 0.8-1.1 respectively.
* Randomly flip the labels for real and fake images
* ADAM optimizer worked better than SGD
* Decaying learning rate

<p align='center'>
  <img src='/images/CashewGAN.gif'>
</p>
