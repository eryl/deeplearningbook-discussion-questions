# Chapter 9
## Chapter 9.1
9.1.1. Why does w(t) need to be a valid probability density function for the output to be a weighted average?
9.1.2. Why is the output of a convolution in the neural networks community referred to as a feature map?
9.1.3. Why is it not as important to flip the kernel for convolutions in neural networks?
9.1.4. In many machine learning libraries, the convolution operator is actually implemented as cross-correlation. When could this be an issue?
9.1.5. Let x be a 4x4 matrix and w a 2x2 kernel. Write down the matrix W which implements the convolution x*w using the matrix multiplication xW. 

## Chapter 9.2
9.2.1. Convolutional layers are agnostic of input size (i.e. the width and height of input images to a convolutional layer can vary), but convolutional networks typically have a fixed input size. What is the reason for this?
9.2.2. Lets say we have an greyscale input image of dimension 28*28. Is this statement true or false: The fully connected layer with size 128 (number of neurons) is equvivalent to the convolutional layer with 128 kernels of size 28*28 (assume only valid convolution, no padding).
9.2.3. What assumptions about the important patterns in the input does the following ideas depend on:
  1. Sparse connections?
  2. Parameter sharing?
  3. eqivariance

## Chapter 9.3
9.3.1. Pooling is sometimes referred to as introducing invariance to small translations into convolutional networks. Exactly what is it that we want to allow small translations of?

9.3.2. Figure 9.9 show en example of how pooling over different feaure maps could learn rotational invariance. Would you have to know beforehand what kind of invariance you want to learn when implementing pooling over feature maps?

9.3.3. What adverse effects can pooling have on what a convnet learnse?

### Comment on chapter 9.3
Pooling layers are no longer as common as they were when the book was written. Convolutional layers used to be presented as in figure 9.7, where the pooling stage was always used after the nonlinearity. In contemporary  architectures like Residual Networks, pooling is only used as infrequent downsampling stages.

## Chapter 9.4
9.4.1. What is the relationship between the amounts of data required and the strenght of a prior, assuming that the prior is a good one? For example, assume we can smoothly interpolate between a convolutional network (strong prior) to the corresponding fully connected network without weight sharing and sparse connections (weak prior). How does this prior affect the amount of data needed to learn a good model?
