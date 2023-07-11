---
title: Image segmentation
date: 2023-07-10 20:14 +0000
categories: [image]
tags: [blog, jekyll]
author: ishandandekar
---

Image segmentation in simple terms is highlighting the area where the object is. It is a little different from object detection. Object detection just finds the four coordinates of the bounding box within which the object might be present. Instead, image segmentation is a task that generates a sort-of mask that shows the complete area where the object is.  
One of the applications where image segmentation is used is, to blur the background in an image.

![segmentation](https://media5.datahacker.rs/2021/11/image-16-768x305.png)
_Semantic segmentation_

So, essentially we divide the image into 'segments'. These segments can be leveraged individually to highlight or use for various tasks. Image segmentation is also used in autonomous driving to identify other cars, persons as well as road. The most essential thing to keep in mind when developing algorithms for image segmentation is **output image has the size as the input image**.

## Different types of Image segmentation

There are various types of image segmentation techniques but these two main ones are:

1. Semantic segmentation: This technique assigns semantic labels (e.g. person, car, tree) to each pixel in the image, creating a dense pixel-wise classification. It is commonly used in autonomous driving.
2. Instance segmentation: Instance segmentation goes a step further by differentiating between individual instances of objects. It assigns unique labels to each object instance in an image. For better a analogy, just like how object detection identifies all the faces in an image of a crowd, instance segmentation highlights all the 'instances' of that class.
   ![types of image segmentation](https://av-eks-blogoptimized.s3.amazonaws.com/Screenshot-from-2019-03-28-12-08-09.jpg)
   _semantic vs instance_

## U-Net[^arXiv]

U-Net is a neural network architecture that is often used for image segmentation. This architecture was first built for bio-medical image segmentation. This architecture is composed of convolutions, residual connections and most importantly _transpose convolutions_.

[^arXiv]: https://arxiv.org/abs/1505.04597
