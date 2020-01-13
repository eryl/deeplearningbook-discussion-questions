Chapter 7 Regularization for deep learning
    7.0 (1) What are the tradeoffs considered in regularizing an estimator?
    7.0 (2) In what sense are the three regimes of model family vs. data-generating process an idealized perspective?
Chapter 7.1 Parameter Norm Penalties
    7.1 (1) Why is it often undesirable to put a weight penalty on the biases of the affine transformations used in neural networks and linear models?
    7.1 (2) Should you use the same regularization coefficient for all weights?
    7.1 (3) Why is L2 regularization often referred to as weight decay in the neural networks community?
    7.1 (4) How does L2 regularization encourage weights to change in relation to the eigenvectors of the Hessian in the quadratic loss example?
    7.1 (5) What does it mean that L2 regularization causes the learning algorithm to “perceive” the input X as having higher variance?
    7.1 (6) What is the main qualitative difference between L1 and L2 regularization?
    7.1 (7) From a Maximum A Posteriori point of view, what prior distribution on the weights does L2 respectively L1 weight penalties correspond to? 
Chapter 7.2 Norm Penalties as Constrained Optimization
    7.2 (1) What are the benefits of explicit constraints implemented with reprojections compared to implicit constraints implemented with norm penalties?
    7.2 (2) What is an alternative to constraining the Frobenius norm of weight matrices?
Chapter 7.3 Regularization and Under-Constrained Problems
    7.3 (1) What are reasons the matrix XTX might be singular?
    7.3 (2) Why is the matrix XTX + 𝛼I guaranteed to be invertible? 
    7.3 (3) What could be a problem for e.g. unregularized logistic regression trained with stochastic gradient descent when the two classes are linearly separable?
7.4  - Dataset augmentation
    7.4 (1). How would you define noise in the input in the context of machine learning?
    7.4 (2). What would you say the relationship between data augmentation and the factors of variation of the data generating process are?
    7.4 (3). Would you agree with the statement that dataset augmentation is about adding noise to the data?
7.5 - Noise robustness
    7.5 (1). In what way is adding noise to the weights not a Baysian approach to learning the weights?
    7.5 (2). How is adding noise to weights connected to flat minima of the loss function?
    7.5 (3). Why is hard targets an issue when training a classification model using softmax and maximum likelihood learning?
    7.5 (4). How does label smoothing help against softmax learning being driven towards larger and larger weights?
7.6 - Semi-supervised learning
    7.6 (1) What is the general idea behind semi-supervised learning and why is it included in the regularization chapter?
7.7 - Multitask Learning
    7.7 (1). Is an intermediate representation (h(shared)) required for multitask learning to work (e.g would it work with some shallow method like linear regression or decision trees directly on the raw data )? 
    7.7 (2). Can you suggest how to use multitask learning with learning algorithms other than neural networks (e.g. by combining algorithms)?
    7.7 (3). Explain what is meant by task-specific vs. generic parameters in multi-task learning.
    7.7 (4). What assumptions does multitask learning rely on in: a) general, and b) in deep learning?
    7.7 (5). [Advanced topic, transfer learning has not yet been covered] Explain the relationship (if any) between multi-task learning and transfer learning.

7.8
    7.8 (1) Early stopping leads to overfitting. Do you agree with this statement?
    7.8 (2) In what way is the number of training iterations similar to other hyperparameters (such as learning rate or weight decay coefficient)?
    7.8 (3) In what way is the number of training iterations different from other hyperparameters?
    7.8 (4) What are some issues with the two strategies (retrain with all training data vs. continue training but add the validation set to the training set) described in the book for training with the full training dataset after the early stopping training is done?
    7.8 (5) Under certain assumptions, there is a close connection between early stopping and L2 regularization. Given these assumptions, what are some important differences between the two?
    7.8 (6) Is there a point in combining early stopping with weight decay when training neural networks?

7.9
    7.9 (1) The book uses an example of two models A and B and suggest how a parameter norm penalty could be used to keep their weights close to each other. What is the difference if instead model B was initialized with the weights of model A, and then trained using early stopping?
    7.9 (2) What statistical property of images does weight sharing in Convolutional Neural Networks assume?

7.10
    7.10 (1) In regards to factors of variation, why is representational sparsity desirable?
    7.10 (2) The section on representational sparsity doesn’t explain how it acts as a regularizer, only how to implement it. Do you have any intuition about what effect it has on the function we learn?

7.11
    7.11 (1) When discussing the expected prediction error and expected squared error (just after equation 7.51) , when are the errors perfectly correlation vs. perfectly uncorrelated?
    7.11 (2) In regards to the Bias-Variance decomposition of the mean squared error (see chapter 5.4.4), which of the terms does model averaging help to reduce the most?
    7.11 (3) Bagging relies on the bootstrap resample method. The simple bootstrap works by taking a sample with replacement from the dataset. Why is it important to do the resample with replacement?
7.12
    7.12 (1) Why is dropout approximating an exponential number of neural networks?
    7.12 (2) Consider a radial basis function (see chapter 6.3.3), where the activation of a unit is proportional to f(x) = exp(-||x - w||2). How would you need to modify the elements of x so as to achieve the effect of dropout (on x, not the output f(x))?
    7.12 (3) In what way is a mini-batch used in stochastic gradient descent typically different from a bootstrap sample?
    7.12 (4) In what way does dropout training differ from bagging?
    7.12 (5) Why is applying the noise to hidden unit activations more powerful than applying it to the input data?
7.13
    7.13 (1) What kind of function does adversarial training locally encourage the network to learn?
    7.13 (2) What is the idea behind semi-supervised adversarial learning?

7.14
    7.14 (1) The methods described relies on ideas from the manifold hypothesis of machine learning (chapter 5.11), what key assumptions of this hypothesis do they rely on?
    7.14 (2) What are tangent vectors to a manifold for a point x, and why are they important in the context of the manifold hypothesis?
    7.14 (3) Why would it make sense to use the distance between the manifolds M1 and M2 as nearest neighbor distance between points x1 and x2 in them?
    7.14 (4) What is the main difference between tangent propagation and dataset augmentation, and what are the pros and cons of both methods?
    7.14 (5) When it comes to invariance to local changes, what are the differences between adversarial training and the tangent methods described here?

Comments:
7.12 The authors say that for very large datasets, regularization confers little reduction in generalization error, but this should be understood in terms of fixed model complexity. The deep learning field has shown that we never have enough data. The more data we have, the bigger we make the models. In the field of Natural Language Processing, the complexity of models are increased as larger amounts of computational resources and data become available. The need to regularize the models remains, for example the currently most successful models for NLP (based on the so called Transformer architecture) uses dropout even though they are trained on tens of gigabytes of text data.
