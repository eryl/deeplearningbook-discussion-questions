# Chapter 9
## Chapter 9.1
1. Why does w(t) need to be a valid probability density function for the output to be a weighted average?
2. Why is the output of a convolution in the neural networks community referred to as a feature map?
3. Why is it not as important to flip the kernel for convolutions in neural networks?
4. In many machine learning libraries, the convolution operator is actually implemented as cross-correlation. When could this be an issue?
5. Let x be a 4x4 matrix and w a 2x2 kernel. Write down the matrix W which implements the convolution x*w using the matrix multiplication xW. 

## Chapter 9.2
1. Convolutional layers are agnostic of input size (i.e. the width and height of input images to a convolutional layer can vary), but convolutional networks typically have a fixed input size. What is the reason for this?
2. Lets say we have an gray scale input image of dimension 28*28. Is this statement true or false: The fully connected layer with size 128 (number of neurons) is equivalent to the convolutional layer with 128 kernels of size 28*28 (assume only valid convolution, no padding).
3. What assumptions about the important patterns in the input does the following ideas depend on:
    1. Sparse connections?
    2. Parameter sharing?
    3. eqivariance

## Chapter 9.3
1. Pooling is sometimes referred to as introducing invariance to small translations into convolutional networks. Exactly what is it that we want to allow small translations of?

2. Figure 9.9 show en example of how pooling over different feature maps could learn rotational invariance. Would you have to know beforehand what kind of invariance you want to learn when implementing pooling over feature maps?

3. What adverse effects can pooling have on what a convnet learns?

### Comment on chapter 9.3
Pooling layers are no longer as common as they were when the book was written. Convolutional layers used to be presented as in figure 9.7, where the pooling stage was always used after the non-linearity. In contemporary  architectures like Residual Networks, pooling is only used as infrequent down sampling stages.

## Chapter 9.4
1. What is the relationship between the amounts of data required and the strength of a prior, assuming that the prior is a good one? For example, assume we can smoothly interpolate between a convolutional network (strong prior) to the corresponding fully connected network without weight sharing and sparse connections (weak prior). How does this prior affect the amount of data needed to learn a good model?

2.  With the same example as in the previous question, in practice, could the two layers (convolutional vs. fully connected) learn the same function (that is, perform the same mapping for any input in the domain)? If yes, how? If no, why not?

## Chapter 9.5
1. What will be the width of a resulting feature map when we convolve a kernel with size k, using stride s over an image of width m, assuming valid convolution (write down the algebraic expression)?

2. What prior assumptions are still assumed when we go from regular convolutions to unshared convolutions?

3. Aside from storage, what other efficiency are we giving up when using unshared convolutions?

## Chapter 9.6
1. The authors describe a recurrent convolutional architecture for gradual refinement of segmentation masks (pixel labeling). Why would you want to solve the problem like they describe instead of adding more layers?

## Chapter 9.7
1. Table 9.1 shows examples of different kinds of data for convolutions are useful. Consider multi-channel 2-D data and single channel 3-D data. Both are 3-D tensors, but what is the difference, if any, in how the convolution is applied?

## Chapter 9.8
1. Consider a 2-dimensional kernel whose elements correspond to the identity matrix. Is this kernel separable?

## Chapter 9.9
1. Coates et al. (2011) use k-means clustering on small image patches to learn convolutional kernels. Compared to learning the kernels using a supervised task, is there a difference in learning to recognize:
    a. Rare patterns (e.g. leopard spots in a large dataset of natural images)?
    b. Composite patterns (e.g. a cross)?


## Chapter 9.10
1. The authors list some differences between the vision system and convolutional networks. What is another key difference in a convolutional layer and the layers described as simple-complex cell?

### Comments for chapter 9.10
- The authors mention that feedback is very common in the brain, but that feedback has not yet show to offer compelling improvements in neural network models. This statement likely refer to feedback we implemented using recurrent connections. However, training neural networks rely on a very important feedback, the error backpropagation. There are hypothesis that the feedback connections in the brain could be used to implement some similar error propagation protocol, but that is mostly speculation at this time.

