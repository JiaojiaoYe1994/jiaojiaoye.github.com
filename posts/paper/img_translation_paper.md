## Image-to-Image translation


In this blog, I summarize some recent papers from CVPR. ECCV related to topic image translation, Domain adaption. The content is based on my personal understanding, so for sure there maybe some misunderstanding or mistakes. Any feedbacks are welcome.


 
### High-Resolution Image Synthesis and Semantic Manipulation with Conditional GANs
[paper](https://arxiv.org/pdf/1711.11585.pdf) | [GitHub](https://github.com/NVIDIA/pix2pixHD)

This paper is the collabrative work from Nvidia and University of Berkely, published in CVPR 2018.

* Idea
1. Image synthesis
2. Image manipulation by adding additional feature maps

perform Autoencoder and KMeans Cluster to encode diffenerent features of style. At test time, randomly choose one cluster as style feature and concatenat with semantic label maps as input to generator.  

* Network

There are multiple tricks of network architecture design in this paper to generate photorealistic and high resolution network

1. Global and Local Generator Coarse-to-fine generator
 <p align='center'>    
	<img src='./imgs/gen.png' width='440'/>
<p/>
2. Multiscale Discriminator
 <p align='center'>    
	<img src='./imgs/dis.png' width='340' height="550" />
<p/>


* Loss function


The loss function consists of two parts:

1. Adeversarial loss
 <p align='center'>    
	<img src='./imgs/adversial_loss.png' width='440'/>
<p/>

2. Feature matching loss
 <p align='center'>    
	<img src='./imgs/fm_loss.png' width='440'/>
<p/>


The total loss is like the following
 <p align='center'>    
	<img src='./imgs/total_loss.png' width='440'/>
<p/>



* Summary

 - High Resolution Image Synthesis
 - instance level image appearance manipulation, but discrete chooose
 - user interactive image manipulation 
 - require instance map to improve image quality
 - supervised learning
 - almost realtime inference(20-30 ms on GTX 1080Ti)



### Multimodal Unsupervised Image-to-Image Translation

[paper](https://arxiv.org/abs/1804.04732) | [GitHub](https://github.com/NVlabs/MUNIT) 

* Idea

synthesize diverse, realistic images

using domain-invariant loss

content: underlying spatial structure
style: rendering of the structure

* Network


* Summary
 - Multimodal, continues style space
 - unsupervised learning
 - example-guided translation is possible.
 - disentangled representation of content and style???


### Unsupervised Image-to-Image Translation 
[paper](https://arxiv.org/pdf/1703.00848.pdf) | [GitHub](https://github.com/mingyuliutw/UNIT)

In their new work MUNIT, they also contain implementation of UNIT, so I would like to suggest to check out in their Pytorch implementation of MUNIT(https://github.com/NVlabs/MUNIT)

### Toward Multimodal Image-to-Image Translation
[paper](https://arxiv.org/pdf/1711.11586.pdf) 


This paper is the collabrative work from Adobe and University of Berkely, 

Bicycle

NIPs 2017




👉[Jiaojiao Ye web](https://jiaojiaoye1994.github.io/jiaojiaoye.github.com/)
