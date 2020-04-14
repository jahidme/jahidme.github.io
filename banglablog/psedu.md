---
layout: post
title: Introduction to Machine Learning
author: Md. Jahid Hasan
date: '2020-04-12 01:05:23 +0600'
category: guides
summary: 𝐓𝐡𝐞 𝐌𝐚𝐜𝐡𝐢𝐧𝐞 𝐋𝐞𝐚𝐫𝐧𝐢𝐧𝐠 𝐋𝐚𝐧𝐝𝐬𝐜𝐚𝐩𝐞
---





Topic : convolutional neural network

A convolutional neural network (CNN) is a type of artificial neural network used in image recognition and processing that is specifically designed to process pixel data.

CNNs are powerful image processing, artificial intelligence (AI) tools that use deep learning to perform both generative and descriptive tasks, often using machine vison that includes image and video recognition, along with recommender systems and natural language processing (NLP).  

Application of CNN :
-Image recognition and OCR
-Object detection for self-driving cars
-Face recognition on social media
-Image analysis in healthcare  

In a convolutional network (ConvNet), there are basically three types of layers:
1.Convolution layer
2.Pooling layer
3.Fully connected layer


1.Convolution part : Parameters of each convolved  layer ,,,,,,,,
-Stride
-Padding
-Number of filter (depth of next layer)
-Size of the filter

>Stride : The amount of filter shift in the image. The bigger the stride, the smaller the feature map output.
example :1
 7 x 7 Input Volume and value of stride is 1
then Output volume is 5 x 5
example :2
  7 x 7 Input Volume and value of stride is 2
then Output volume is 3 x 3

>>Padding :We have seen that convolving an input of 6 X 6 dimension with a 3 X 3 filter results in 4 X 4 output. We can generalize it and say that if the input is n X n and the filter size is f X f, then the output size will be (n-f+1) X (n-f+1):
-Input: n X n
-Filter size: f X f
-Output: (n-f+1) X (n-f+1)
with Padding
-Input: n X n
-Padding: p
-Filter size: f X f
-Output: (n+2p-f+1) X (n+2p-f+1)

>>>Number of filter :
Example: 6x6x3 image with four 3x3 filter.
After convolving, will get 4x4xn, n is depends on the number of filter you use.In this case, n will be 4.

2.The Pooling Layer :
Pooling reduces the dimensionality of each feature map and retains the most important information of an image. Spatial Pooling can be of different types: Max, Average, Sum etc.
Max pooling being the most popular. This basically takes a filter (example: size 2x2) and a stride of the same length(which is 2). It then applies it to the input volume and outputs the maximum number in every sub-region that the filter convolves around.

3.Fully connected layer :
 Fully connected layers are an essential component of Convolutional Neural Networks (CNNs), which have been proven very successful in recognizing and classifying images for computer vision. The CNN process begins with convolution and pooling, breaking down the image into features, and analyzing them independently. The result of this process feeds into a fully connected neural network structure that drives the final classification decision
