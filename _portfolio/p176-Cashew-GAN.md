---
title: "Cashew GAN - A Generative Adversarial Network to generate different types of casews"
excerpt: "A generative adversarial network, to generate different kinds of cashews, designed and trained from scratch<br/><img src='/images/CashewGAN.gif'>"
collection: portfolio
---

Project in brief
================

I find it quite interesting to solve various vision related problems in the domain of food and manufacturing industry. One of the hobby proect
I am working on is to sort good and poor quality cashews. While sorting the broken and full cashews is an easy task, there are several grades of
cashews. Specifically developing a model that can differentiate between cashew splits and full cashews or good and burnt cashew can be challenging. 
Us
It is sometimes difficult to get enough samples for each kind of cashew. I have learnt a lot about GANs but never had a chance of 
making one from scratch. I planned to create my own dataset and developing a GAN to generate new images of cashews. So far the results are 
not very crisp but we can say that they look fair enough. Through this project I have learnt a lot of practical concepts that on needs to know
while creating a GAN from scratch. Some important points that helped me in creating a stable GAN are as follows:

* Normalizing input
* Using batchnorm
* Instead of 1 and 0 for real and fake using soft lables random number between 0-0.2 and 0.8-1.1 respectively.
* Randomly flip the lables for real and fake images
* ADAM optimizer worked better than SGD
* Decaying learning rate

<p align='center'>
  <img src='/images/CashewGAN.gif'>
</p>
