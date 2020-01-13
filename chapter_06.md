## Chapter 6 introduction
1. If described as a graph of function compositions, what kind of graph is
  a. a feedforward neural network,
  b. a recurrent neural network?
2. What is the difference between the output layer and the hidden layers?
3. What is meant by the width of a layer?
4. Explain how linear functions are defective in regards to interaction between variables.
5. What are the three approaches to choose feature mapping 𝜙 according to Goodfellow et. al?
6. What are some important design decisions in regards to feedforward neural networks?

## Chapter 6.1 Example: Learning XOR
1. Why is the XOR function often used as an example in introductions to neural networks?

##  Chapter 6.2 - Gradient-based Learning
1. What is meant by “Stochastic Gradient Descent applied to nonconvex loss functions [...] is sensitive to the values of the initial parameters.”?
2. What training paradigm are neural networks mostly trained under?
3. Under maximum likelihood training, what cost function correspond to the model choice of conditionally normal distribution [that is the model assumption: p_model(y | x) = N(y; f(x; theta), I)]?
4. What is meant by a cost function saturating and when is it a problem?
5. In what way does the choice of minimizing negative log likelihood help with the problem of cost saturation?
6. What is the difference between learning a probability distribution p(y |x; theta) and learning a conditional statistic?
7. What type of output layer should you use if you model your conditional distribution p_model(y | x) as Gaussian and you want to parameterize the mean using a neural network?
8. What type of output layer should you use if you model your conditional distribution p_model(y | x) as Bernoulli and you want to parameterize the probability of the positive class?
9. What’s the issue with using P(y=1 |x) = max{0, min{1, w^Th + b}} as output for parameterizing a Bernoulli distribution?
10. What is meant by a logit?
11. What are two ways the softmax function is used in neural networks?
12. When using logistic units or softmax as outputs, which loss function is best to use, Mean Squared Error or Negative Log-Likelihood? Why?
13. Where does the name softmax come from?
14. Brain teaser:  Consider using a softmax to model a k-way conditionally categorical distribution p_model(y | x). Let’s assume that the entropy of the true conditional distribution is 0 (that is, for every possible x, a single value of the categorical distribution P( y | x) has all the probability mass). Given the softmax form softmax(z)_i = exp(z_i)/sum_j exp(z_j), how many dimensions does z need to have, to perfectly model the true conditional distribution?
15. What is meant by a heteroscedastic model?
16. What is the advantage of using precision instead of variance or standard deviation when parameterizing a Gaussian with a neural network trained using negative log-likelihood?
17. What activation function is useful when parameterizing the diagonal values of the precision matrix?
18. What is the idea behind a mixture density network (of Gaussians), and what three different types of output units does it have?

## Chapter 6.3 - Hidden units
1. What could be considered the default choice for activation functions of hidden layers in feedforward networks?
2. How do software for training neural networks deal with point where the derivative is undefined?
3. What are three generalizations of rectified linear units?
4. What is the general idea behind maxout units?
5. What is the relationship between the logistic sigmoid and hyperbolic tangent functions?
6. Why is training a network with tanh units easier than training one with logistic ones?
7. What is the result of using multiple linear layers (without activation function in between) and why would it be a good idea?
8. What is the idea behind using softmax units as hidden activation units inside a network?

## Chapter 6.4 - Architecture design
1. What does the universal approximation theorem for neural networks state?
2. What are two ways in which the learning of approximating a function can fail?
3. Can you think of any other machine learning model which has the property of being a universal function approximator?
4. Why does the universal function approximation theorem matter?
5. What is the result from circuits of logic gates regarding shallow vs. deep circuits which is used to motivate deep neural networks?
6. How does the number of linear regions a deep rectifier network can learn relate to the depth of the network?
7. From a representation learning point of view, what kind of prior belief about the learning problem does a deep architecture imply?
8. What are skip connections in feedforward networks?

## Chapter 6.5.1-6.5.2 - Back-propagation and Other Differentiation Algorithms
1. Why is the jacobian (𝜕y/𝜕x) in equation 6.46 a matrix?
2. Draw a picture which shows the relation between equation 6.45 and 6.46

