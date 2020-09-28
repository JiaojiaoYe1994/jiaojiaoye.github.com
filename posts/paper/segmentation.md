# Segmentation



In this blog, I will a brief introduction to Image segmentation with Deep Learning.



## Table of Contents : 



- [Definition](#Definition)
- [Network](#Network)
- [Evaluation methods](#Evaluation)
- [Paper and Project](# Paper and Project)
- [Blogs](Blogs)





## Definition

Different from classification and object detection, segmentation describes the process of classifying each pixels to a certain class. Essentially, segmentation is pixel-level classification. According to fidelity of classification, it can be divided into the following areas: 



### Semantic segmentation

The goal of semantic image segmentation is to label *each pixel* of an image with a corresponding ***class*** of what is being represented. It doesn't different across different instances of the same object.



### Instance segmentation

Instance segmentation gives a unique label to every instance of a particle object in the image. For example, for dog1 in one image, it will will label it as dog1, dog2, dog3 , while semantic segmentation classifies it as one label dog.



### Panoptic segmentation

It was first introduced in  by Kaiming He, cooperated FAIR and Heidelberg University  in 2018 . Panoptic segmentation will give every pixel a label and instance ID.





## Network 

* LinkNet CVPR 2017 
* SegNet (2017)
* pspNet (2017)
* DeepLab V1, DeepLab V2, DeepLab V3, DeepLab V3+
* FCNet (2014)
*  UNet 
*  Fast SCNN (2019)
*  ICNet(2018)



## Evaluation

The performance of segmentation models can be evaluated in three aspects.



### 1. **Execution time**

Execution or speed is a key indicator for application, especially during inference time in the period of model deployment. Execution time is an indicator for algorithm efficiency and complexity. On the other hand, execution time is also effect by the hardware.



### 2. **Memory footprint**

Memory cost is an important consideration for real time application. For example, for a self driving car, there are a fixed number of GPUs allocated in one car, which is responsible for processing all modules, including perception, prediction, decision making, control. Obviously, the memory footprint should be limited.



### 3. Accuracy

Other than previous two criterion, there are several other metrics for evaluating segmentation performance.

 

* PA (Pixel Accuracy)

  the percent of pixels in the image which were correctly classified. 

  $$ accuracy = \frac{TP + TN }{ TP + TN + FP + FN} $$

  

* PC (Per-Class)

   accuracy measures the proportion of correctly labelled pixels for each class and then averages over the classes

* MIoU (Mean Intersection over Union) / Jaccard Index 

  https://en.wikipedia.org/wiki/Jaccard_index

  measures the intersection over the union of the labelled segments for each class and reports the average

  The `Jaccard index`_, also known as Intersection over Union and the Jaccard similarity coefficient.
  $$ a =q $$

* **IoU class:** Intersection over Union for each class 

  $$IoU=TP/(TP+FP+FN)

* **iIoU class** ( Instance Intersection over Union ) 

  $$iIoU=iTP/(iTP+FP+iFN)$$

* **IoU category** (Intersection over Union for each category) 

  $$IoU=TP/(TP+FP+FN)$$

* **iIoU category** (Instance Intersection over Union for each category) 

  $$ iIoU=iTP/(iTP+FP+iFN) $$



## 
