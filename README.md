# Semantic Segmentation
[//]: # (Image References)
[image1]: ./writeup_imgs/fcn-arch.png "Simplified Representation of FCN Architecture"
[image2]: ./writeup_imgs/um_000000.png "A typical result from the trained network"
[image3]: ./writeup_imgs/um_000003.png "Another typical result from the trained network"
[image4]: ./writeup_imgs/um_000087.png "The trained network had some issues dealing with shadows or high-contrast situations"

In this project, I labeled the pixels of a road in images using a Fully Convolutional Network (FCN). The architecture used was based on FCN-8, with more information on FCN-8 available [here](https://people.eecs.berkeley.edu/~jonlong/long_shelhamer_fcn.pdf).

## About
- The [Kitti Road dataset](http://www.cvlibs.net/datasets/kitti/eval_road.php) was used to train the and evaluate the network.
- This FCN uses the VGG16 network as the encoder, and a decoder with 3 layers and 2 skip connections. A simplified representation of the network is shown below, with the image taken from Udacity's classroom
![image1]
- The network was trained over 50 epochs with a loss of approximately 8-9%.

## Results
Below are some typical results from the trained FCN. For the most part, it identifies most of the road surface and excludes other vehicles on the road. It does have some issues in dealing with shadows or high contrast situations, as illustrated in the last image. 

A typical result from the trained FCN:
![image2]

Another typical result from the trained FCN:
![image3]

The FCN is shown having trouble with a high-contrast situation:
![image4]

## Limitations of this Specific Project
- The network had to be trained on CPUs rather than GPUs, due to insufficient GPU memory
- Augmenting the training data would help generalize this method more, perhaps also improving the analysis with shadows
- The performance of the trained network could be improved by using the techniques learned in the "Inference Performance" module of the Udacity classroom

