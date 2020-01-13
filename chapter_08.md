Chapter 8.1
    8.1 (1) The book mentions that the true measure we actually want to optimize might not be feasible because it might be non-differentiable. Apart from the 0-1 loss they mention, can you give some other example of such a measure?
    8.1 (2) Consider a neural network with a logistic sigmoid output (a binary classification output). Explain the difference between when the 0-1 loss vs the negative log likelihood loss is minimized on the training set for this model (i.e. what output values of the sigmoid would cause the respective losses to have minimal values)? 
    8.1 (3) Imagine you are monitoring both accuracy and negative log likelihood on a validation set for early stopping. When should you do early stopping, when the accuracy stops increasing or when the negative log likelihood stops decreasing?
    8.1 (4) How does the variance of the estimate of the gradient of the maximum likelihood estimation change with the size of a minibatch?
    8.1 (5) What does it mean that stochastic gradient descent (SGD) follows the gradient of the true generalization error?
    8.1 (6) What can you say about the bias of the estimator of the gradient of the generalization error in these three cases: single example SGD, mini-batch SGD and batch gradient descent (on the full training set)?
    8.1 (7) Can you overfit if you only use the examples in the training set once?

Chapter 8.2
    8.2 (1) In what ways are neural networks not identifiable?
    8.2 (2) Why is it wrong to think of minima in neural networks as the lowest point of a bowl?
    8.2 (3) Summarize the idea of how the kind of critical points a random function has changes in high dimensions.
    8.2 (4) What is the difference between first order (gradient descent) and second order (e.g. unmodified Newton's method) methods in relation to saddle points?
    8.2 (5) What is the main determination whether gradients explode or vanish in the example given by equation 8.11?
    8.2 (6) Which is most problematic: vanishing or exploding gradients?
    8.2 (7) How is the choice of initialization points related to the issue of poor correspondence between local and global structure?

Comments
Chapter 8.1: Remember that the condition number (for a square matrix like the Hessian) is the absolute value of the ratio between the largest and smallest eigenvalue. Take for example the multiplication Hv. If the condition number of H is 1, then the largest and smallest eigenvalue are the same, so they will uniformly scale the magnitude of any v. If the condition number is large, the magnitude of Hv will be very much dependent on the direction of v, in particular, they will magnify the components of v which are parallel to the largest eigenvector much more than along the smallest, leading to an uneven expansion/contraction of the space. Imagine we have an approximate v, then error will be magnified in the direction of the largest eigenvalue.
Large condition numbers are also a big problem when inverting H for similar reasons. Here is an article which also covers momentum in depth, it’s well worth a read if you want more details: https://distill.pub/2017/momentum/

Chapter 8.3
Is large datasets problematic for Stochastic Gradient Descent?
8.4
What does it mean that an example is “lost in the null space” of forward propagation?
Describe how large weight values could cause saturation and what effect this has on backpropagation.
8.5
Why can the delta-bar-delta rule only be applied to full batch optimization? 
Consider a linear regressions  model ( f(x) = Wx + beta). Assume there is a single global optima of and that the loss surface is convex. In terms of the solutions found by momentum compared to AdaGrad, how does the solutions found change as we rotate x and W in arbitrary ways?


Chapter 8.6
    8.6 (1) Describe how negative eigenvalues of the Hessian can cause Newton's method to take update steps in the wrong direction.
    8.6 (2) Why does Levenberg-Marquardt  algorithm converge to gradient descent when the alphas become large?
    8.6 (3) How does the method of steepest descent on quadratic functions undo progress from the previous iteration?
    8.6 (4) What is the connection between conjugate gradient descent and momentum gradient descent?

Chapter 8.7
    8.7 (1) There has been much criticism of the original Batch Normalization paper about unsubstantiated claims it made, particularly regarding what they call internal covariate shift. Do you think Goodfellow et. al. perpetuate these unsubstantiated claims, or are they more in line what can be correctly claimed in regards to batch norm? 
    8.7 (2) In what way could coordinate descent be used for parallelizing training of neural networks?
    8.7 (3) How is Polyak averaging and momentum connected?
    8.7 (4) What is the difference between greedy supervised pretraining and multitask learning (chapter 7.7)?
    8.7 (5) What could be some  drawbacks with what the representations are encouraged to encode in greedy supervised pretraining? 
    8.7 (6) What assumption about the loss landscape does  the following statement rely on: “modern neural networks have been designed so that their local gradient information corresponds reasonably well to moving toward a distant solution”?
    8.7 (7) Describe how skip connections are related to adding “auxiliary heads” as in GoogLeNet.
    8.7 (8) How are “auxiliary heads” related to multitask learning?
    8.7 (9) Explain how curriculum learning can be framed as a continuation method.
 


