[2.2 Optimization Algorithms](https://app.capacities.io/da1727b3-702c-4ccb-80e6-6bd0f97632ed/18d59297-fd12-449f-958a-edb9afa8c18b)
## ôn tập
[[ZAN.canvas|ZAN]]
What is the primary difference between classification and regression tasks?

- [ ] a) Classification predicts a continuous-valued output, while regression predicts discrete values.
    
- [x] b) Classification predicts discrete values, while regression predicts a continuous-valued output.
    
- [ ] c) Classification is a supervised learning task, while regression is unsupervised.
    
- [ ] d) Classification deals with numerical data, while regression deals with categorical data.
    

Binary classification is a supervised learning algorithm that classifies input data into how many categories or classes?

- [x] a) One.
    
- [ ] b) Two.
    
- [ ] c) Three or more.
    
- [ ] d) Any number.
    

Which of the following is an example of a binary classification problem?

- [x] a) Predicting the price of a house.
    
- [ ] b) Distinguishing cats from dogs in images...
    
- [ ] c) Forecasting demand for retail sales.
    
- [ ] d) Predicting the length of stay for hospital patients.
    

Binary classification problems can be solved using which algorithm?

- [ ] a) Linear Regression.
    
- [x] b) Logistic Regression.
    
- [ ] c) K-means clustering.
    
- [ ] d) Principal Component Analysis.
    

In binary classification, the output of the algorithm is typically a binary decision, such as:

- [ ] a) A continuous number.
    
- [ ] b) A probability distribution over multiple classes.
    
- [x] c) Yes or no, true or false, 1 or 0.
    
- [ ] d) A ranking of options.
    

---

---

**According to one source, classifying an email as spam or not spam is an example of what type of problem?**

- [ ] a) Regression.
    
- [x] b) Binary classification.
    
- [ ] c) Clustering.
    
- [ ] d) Dimensionality reduction.
    

---

**Another example of a binary classification problem mentioned is recognizing whether an image contains what?**

- [ ] a) A specific object from a large set.
    
- [x] b) A cat or not.
    
- [ ] c) Multiple distinct objects.
    
- [ ] d) A handwritten digit.
    

---

**In machine learning terminology, what refers to problems where we are interested only in hard assignments of examples to categories?**

- [ ] a) Soft assignments.
    
- [x] b) Regression.
    
- [ ] c) Classification.
    
- [ ] d) Ranking.
    

---

**What is the other subtly different problem that machine learning practitioners colloquially overload the word "classification" to describe, besides hard assignments?**

- [ ] a) Ranking items.
    
- [ ] b) Predicting continuous values.
    
- [x] c) Making soft assignments, i.e., assessing the probability of each category.
    
- [ ] d) Clustering data points.
    

---

**Even when the primary interest is in hard assignments in classification, models that make soft assignments are often used. Why does one source say this distinction tends to get blurred?**

- [ ] a) Because soft assignments are always more accurate.
    
- [ ] b) Because hard assignments are computationally cheaper.
    
- [x] c) Because often, even when caring about hard assignments, models making soft assignments are used.
    
- [ ] d) Because the output is always interpreted as a probability.
    

---

### Logistic Regression

**Logistic Regression is an algorithm used to solve what type of problems?**

- [ ] a) Continuous prediction problems.
    
- [x] b) Binary classification problems.
    
- [ ] c) Unsupervised learning problems.
    
- [ ] d) Dimensionality reduction problems.
    

---

**Logistic Regression is closely related to which other machine learning concept/algorithm?**

- [ ] a) K-means clustering.
    
- [ ] b) Principal Component Analysis.
    
- [x] c) Support Vector Machines.
    
- [ ] d) Decision Trees.
    

---

**In the context of neural networks, Logistic Regression can be represented as a single neuron neural network with what type of activation function?**

- [ ] a) [Rectified Linear Unit](https://app.capacities.io/da1727b3-702c-4ccb-80e6-6bd0f97632ed/35c319d2-ce83-4f56-9331-b2ad6dbed925) (ReLU).
    
- [ ] b) Hyperbolic Tangent (tanh).
    
- [ ] c) Binary-step activation function.
    
- [x] d) Sigmoid activation function.
    

---

**One source states that Logistic Regression is actually used more in which types of problems?**

- [ ] a) Regression.
    
- [x] b) Classification.
    
- [ ] c) Clustering.
    
- [ ] d) Feature selection.
    

---

**What is the name commonly referred to when popular perspectives on the softmax and margin perceptrons are discussed?**

- [ ] a) Linear Regression and Naive Bayes.
    
- [x] b) Support Vector Machines and Logistic Regression.
    
- [ ] c) K-means and Spectral Clustering.
    
- [ ] d) Decision Trees and Random Forests.
    

---

 **Logistic regression boundary created by the algorithm has what form?**
    
- [ ] a) Non-linear.
    
- [ ] b) Piecewise linear.
    
- [x] c) Linear.
    
- [ ] d) Polynomial.
    

---

 **According to one source, Logistic Regression corresponds to a conditional probability model of the form p(y|x,w) = Ber(y|σ(wTx)) in the binary case. What does σ represent here?**
    
- [ ] a) A linear function.
    
- [ ] b) The softmax function.
    
- [x] c) The sigmoid (logistic) function.
    
- [ ] d) The ReLU function.
    

---

**Multinomial logistic regression is a discriminative classification model used when there are more than two classes. What function is typically used in the output layer of multinomial logistic regression to produce a probability distribution over classes?**
    
- [ ] a) Sigmoid.
    
- [ ] b) ReLU.
    
- [x] c) Softmax.
    
- [ ] d) Tanh.
    

---

**What classification model results from applying maximum likelihood estimation with a Bernoulli distribution and a sigmoid activation function?**
    
- [ ] a) It is the same as linear regression.
    
- [x] b) It is called Logistic Regression.
    
- [ ] c) It is a form of support vector machine.
    
- [ ] d) It is an unsupervised method.
    

---

 **Logistic Regression can be seen as a linear model that computes what kind of decision boundaries in the input space?**
    
- [ ] a) Curved.
    
- [ ] b) Nonlinear.
    
- [x] c) Linear.
    
- [ ] d) Arbitrary.
    

---

### Logistic Regression Cost Function

 **What is a common loss function used for Logistic Regression, especially when interpreting outputs as probabilities?**
    
- [ ] a) Mean Squared Error (MSE).
    
- [x] b) Cross-entropy.
    
- [ ] c) Hinge loss.
    
- [ ] d) Absolute error.
    

---

 **According to one source, cross-entropy calculates what?**
    
- [ ] a) The difference between predicted and true values.
    
- [ ] b) The mean squared error of the predictions.
    
- [x] c) The negative log-likelihood of the predicted probability assigned to the true label.
    
- [ ] d) The hinge loss of the model.
    

---

 **What is a common name for the softmax perceptron cost function used with fixed feature mapped input?**
    
- [ ] a) Mean Squared Error.
    
- [ ] b) Hinge Loss.
    
- [ ] c) Logistic Regression.
    
- [x] d) Support Vector Machine.
    

---

 **If the loss function of Logistic Regression was written as (J(w)=∑i=1N​(yi​−zi​)2), what difficulty would occur?**
    
- [ ] a) The function would be convex and easy to optimize.
    
- [x] b) The function would be non-convex and challenging to optimize.
    
- [ ] c) This is the standard loss function for Logistic Regression.
    
- [ ] d) The gradients would vanish.
    

---

**In the context of Logistic Regression, minimizing the negative log likelihood is a standard approach for what?**

- [ ] a) Parameter initialization.
    
- [ ] b) Cross-validation.
    
- [x] c) Maximum likelihood estimation.
    
- [ ] d) Feature selection.
    

---

 **The negative log-likelihood for the linear regression model can be written in terms of a squared error. What does this correspond to in the context of the Gaussian likelihood?**
    
- [ ] a) Maximizing the prior probability.
    
- [ ] b) Minimizing the cross-entropy.
    
- [x] c) Maximizing the likelihood.
    
- [ ] d) Minimizing the hinge loss.
    

---

**One source mentions that Logistic Regression with softmax activation function can be trained using what type of loss function?**
    
- [ ] a) Mean Squared Error.
    
- [ ] b) Hinge loss.
    
- [x] c) Cross-entropy loss function.
    
- [ ] d) L2 regularization loss.
    

---

**The log likelihood can be written as the negative cross entropy in which model?**
    
- [ ] a) Linear Regression.
    
- [x] b) Multinomial logistic regression.
    
- [ ] c) Support Vector Machine.
    
- [ ] d) Naive Bayes.
    

---

**For a classification problem using Logistic Regression, the final layer often has linear activations, and the outputs are interpreted as what?**
    
- [x] a) Probabilities.
    
- [ ] b) Labels.
    
- [ ] c) Scores or logits.
    
- [ ] d) Feature vectors.
    

---

**When using the cross-entropy loss with softmax, how does its derivative relate to the derivative of squared error, according to one source?**

- [ ] a) They are completely different.
    
- [x] b) They behave very similarly, by taking the difference between expected and predicted behavior.
    
- [ ] c) The cross-entropy derivative is always larger.
    
- [ ] d) The squared error derivative is always larger.
    

---

### Gradient Descent

 **What is the most common method for optimizing multilayer neural networks?**
    
- [ ] a) Newton's Method.
    
- [x] b) Gradient Descent (GD).
    
- [ ] c) Analytical solution.
    
- [ ] d) Grid Search.
    

---

**Gradient descent is a widely used numerical method for what?**

- [ ] a) Parameter initialization.
    
- [ ] b) Data visualization.
    
- [x] c) Optimization.
    
- [ ] d) Feature scaling.
    

---

**To apply Gradient Descent, what needs to be calculated?**

- [ ] a) The mean of the data.
    
- [ ] b) The variance of the data.
    
- [x] c) The derivative of the loss function according to parameters.
    
- [ ] d) The analytical solution.
    

---

 **Stochastic gradient descent is a variation of gradient descent that updates parameters using how much data at each step?**
    
- [ ] a) The entire dataset.
    
- [ ] b) A random subset (minibatch) of the data.
    
- [x] c) A single data point.
    
- [ ] d) A fixed, non-random subset.
    

---

 **What is one benefit of using stochastic gradient descent compared to standard gradient descent on large datasets?**
    
- [ ] a) It guarantees finding the global minimum.
    
- [x] b) It is typically faster.
    
- [ ] c) It requires less memory to store the entire dataset.
    
- [ ] d) It is not affected by local minima.
    

---
**What is a minibatch in the context of stochastic gradient descent?**
    
- [ ] a) The entire training dataset.
    
- [ ] b) A single training example.
    
- [x] c) A small, random subset of the training examples.
    
- [ ] d) The validation set.
    

---

 **What is the purpose of gradient clipping in training recurrent neural networks (RNNs)?**
    
- [ ] a) To increase the learning rate.
    
- [x] b) To prevent exploding gradients.
    
- [ ] c) To introduce random noise.
    
- [ ] d) To reduce the number of parameters.
    

---

 **According to one source, optimization is the engine that powers which machine learning concepts?**
    
- [x] a) Predictive learning, feature design, and function approximation.
    
- [ ] b) Data collection and preprocessing.
    
- [ ] c) Model evaluation and interpretation.
    
- [ ] d) Clustering and dimensionality reduction.
    

---

 **In optimization, a loss function is often referred to as what?**
    
- [ ] a) The validation metric.
    
- [ ] b) The accuracy score.
    
- [x] c) The objective function.
    
- [ ] d) The regularization term.
    

---

**What happens if a poor choice of initialization or activation function is made, potentially affecting gradient descent convergence?**
    
- [ ] a) The optimization algorithm will always converge faster.
    
- [ ] b) The model will not be able to perform classification.
    
- [x] c) Exploding or vanishing gradients might be encountered.
    
- [ ] d) The dataset will need to be normalized.
    

---

### Derivatives

**What is the study of how functions behave under small changes called?**
    
- [ ] a) Linear algebra.
    
- [ ] b) Probability and statistics.
    
- [x] c) Differential calculus.
    
- [ ] d) Discrete mathematics.
    

---

**In the context of machine learning optimization, gradients are used to find what?**
    
- [ ] a) The data variance.
    
- [x] b) The maximum/minimum of functions.
    
- [ ] c) The dimensions of matrices.
    
- [ ] d) The probability distribution of data.
    

---

**What mathematical rule is fundamental for computing gradients in neural networks with multiple layers?**
    
- [ ] a) Bayes' Rule.
    
- [ ] b) Sum Rule.
    
- [ ] c) Product Rule.
    
- [x] d) Chain Rule.
    

---
## tom tat
---

**What is the gradient of a scalar function (f) with respect to a matrix (X)?**

- [ ] a) A scalar.
    
- [ ] b) A vector.
    
- [ ] c) A matrix with the same dimensionality as (X).
    
- [ ] d) A tensor of higher order.
    

---

**What process relies on the chain rule for transforming random variables and is used in generative models?**

- [ ] a) Gradient Descent.
    
- [ ] b) Normalizing flows.
    
- [ ] c) Principal Component Analysis.
    
- [ ] d) K-means clustering.
    

---

**In numerical optimization, what is a descent direction?**

- [ ] a) A direction in which the function value increases.
    
- [ ] b) A direction in which the function value decreases.
    
- [ ] c) A direction orthogonal to the gradient.
    
- [ ] d) A direction parallel to the Hessian.
    

---

**What is the Hessian matrix?**

- [ ] a) A vector of first derivatives.
    
- [ ] b) A matrix of second derivatives.
    
- [ ] c) A scalar representing the magnitude of the gradient.
    
- [ ] d) A matrix of input features.
    

---

**What is automatic differentiation?**

- [ ] a) Manually computing derivatives for all parameters.
    
- [ ] b) Using numerical approximation to estimate derivatives.
    
- [ ] c) Algorithms that compute derivatives automatically.
    
- [ ] d) Ignoring derivatives and using a different optimization method.
    

---

**What is the derivative of the Logistic Sigmoid function, according to one source?**

- [ ] a) It is always 0.
    
- [ ] b) It is always 1.
    
- [ ] c) It vanishes for large positive and negative arguments.
    
- [ ] d) It is a constant value.
    

---

**What are Newton's method and gradient descent methods for?**

- [ ] a) Finding analytical solutions to optimization problems.
    
- [ ] b) Numerical optimization.
    
- [ ] c) Generating random data.
    
- [ ] d) Calculating the mean and variance of data.
    

---

### Computation Graph

**What is a computation graph?**

- [ ] a) A table of numerical data.
    
- [ ] b) A directed structure where nodes are operations and edges represent data.
    
- [ ] c) A plot of the loss function over iterations.
    
- [ ] d) A matrix of weights and biases.
    

---

**What do the nodes and edges represent in a computation graph?**

- [ ] a) Nodes are parameters, edges are data.
    
- [ ] b) Nodes are data, edges are operations.
    
- [ ] c) Nodes are primitive operations, edges represent numeric data.
    
- [ ] d) Nodes are layers, edges are activation functions.
    

---

**A deep neural network can be expressed as a computation graph, where the nodes are primitive operations like matrix multiplication, and edges represent what?**

- [ ] a) Layers.
    
- [ ] b) Parameters.
    
- [ ] c) Numeric data in the form of vectors, matrices, or tensors.
    
- [ ] d) Activation functions.
    

---

**What is one of the benefits of modeling a deep architecture as a computation graph?**

- [ ] a) It makes the model intrinsically linear.
    
- [ ] b) It is not possible to derive a global loss function.
    
- [ ] c) It is possible to derive a global loss function that can be optimized.
    
- [ ] d) It hides the relationship between layers.
    

---

**According to one source, TensorFlow models a deep architecture using what concept?**

- [ ] a) Sequential layers only.
    
- [ ] b) A directed structure called a computational graph.
    
- [ ] c) Analytical equations.
    
- [ ] d) Only linear operations.
    

---

**In a computation graph, what does a linear layer followed by an elementwise nonlinearity correspond to?**

- [ ] a) A single primitive operation.
    
- [ ] b) A sequence of nodes and edges.
    
- [ ] c) A loop or cycle.
    
- [ ] d) A parameter node.
    

---

**Drawing the computation graph for a model can help visualize what?**

- [ ] a) The input data distribution.
    
- [ ] b) The dependencies between variables and operations.
    
- [ ] c) The optimal learning rate.
    
- [ ] d) The convergence speed of gradient descent.
    

---

**What happens to the computational graph if you want to compute second derivatives?**

- [ ] a) It becomes simpler.
    
- [ ] b) It requires a completely different graph.
    
- [ ] c) It generally becomes larger.
    
- [ ] d) It depends only on the input dimension.
    

---

**What is the memory footprint for training a neural network?**

- [ ] a) It is only determined by the number of parameters.
    
- [ ] b) It is determined by the parameters and intermediate variables stored during the forward pass.
    
- [ ] c) It is independent of the model architecture.
    
- [ ] d) It is always smaller than the memory needed for prediction.
    

---

**If a computational graph is too large for a single GPU, how might it be handled?**

- [ ] a) It cannot be trained.
    
- [ ] b) It can be partitioned over more than one GPU.
    
- [ ] c) Only smaller models can be trained.
    
- [ ] d) Training must be done on a CPU.
    

---

### Derivatives with a Computation Graph

**What algorithm uses the computation graph to efficiently calculate the gradient of a function defined on the graph?**

- [ ] a) Gradient Descent.
    
- [ ] b) Newton's Method.
    
- [ ] c) Backpropagation.
    
- [ ] d) Grid Search.
    

---

**Backpropagation calculates gradients by applying what mathematical rule repeatedly?**

- [ ] a) Bayes' Rule.
    
- [ ] b) The Sum Rule.
    
- [ ] c) The Chain Rule.
    
- [ ] d) The Product Rule.
    

---

**What is the purpose of calculating gradients using backpropagation?**

- [ ] a) To evaluate the model's accuracy.
    
- [ ] b) To update the model's parameters using optimization algorithms like gradient descent.
    
- [ ] c) To visualize the data distribution.
    
- [ ] d) To select the optimal hyperparameters.
    

---

**What does "forward propagation" or "forward pass" refer to in a neural network?**

- [ ] a) Calculating gradients.
    
- [ ] b) Updating parameters.
    
- [ ] c) Calculating and storing intermediate variables (including outputs) from input to output layer.
    
- [ ] d) Splitting the data into batches.
    

---

**Backpropagation is often called "backward propagation" because it computes gradients in what direction through the computation graph?**

- [ ] a) From input to output.
    
- [ ] b) From output to input.
    
- [ ] c) Randomly through the graph.
    
- [ ] d) Only within a single layer.
    

---

**What needs to be stored during the forward pass to enable the backward pass (backpropagation)?**

- [ ] a) The final output only.
    
- [ ] b) The initial input only.
    
- [ ] c) Intermediate variables, including inputs and outputs of each operation.
    
- [ ] d) The gradient values.
    

---

**What is the dimensionality of the gradient of a scalar function (f) with respect to an input matrix (X) of size (n×m)?**

- [ ] a) (1×1).
    
- [ ] b) (n×m).
    
- [ ] c) (m×n).
    
- [ ] d) (n×1).
    

---

**How does TensorFlow compute the gradients of an output tensor with respect to any previous connected layer in the computation graph?**

- [ ] a) Manually.
    
- [ ] b) Using symbolic differentiation.
    
- [ ] c) Using automatic differentiation, enabling standard back-propagation.
    
- [ ] d) By approximating the gradient with finite differences.
    

---

**What is the primary concept that makes backpropagation efficient for training deep neural networks?**

- [ ] a) Calculating gradients independently for each parameter.
    
- [ ] b) Reusing intermediate calculations during the backward pass via the chain rule.
    
- [ ] c) Avoiding the computation of derivatives.
    
- [ ] d) Using a fixed learning rate.
    

---

**In backpropagation through time for RNNs, gradients are backpropagated through how many layers along the time steps?**

- [ ] a) A fixed number, independent of sequence length.
    
- [ ] b) O(T), where T is the sequence length.
    
- [ ] c) Only through the current time step's layers.
    
- [ ] d) Only through the input layer.
    

---

### Logistic Regression Gradient Descent

**What method can be used to optimize the loss function of Logistic Regression?**

- [ ] a) Analytical solution.
    
- [ ] b) Gradient Descent.
    
- [ ] c) Grid Search.
    
- [ ] d) Random Search.
    

---

**According to one source, what optimization algorithm is used to learn the parameters of the softmax classifier?**

- [ ] a) Analytical Solution.
    
- [ ] b) Newton's Method.
    
- [ ] c) Gradient Descent.
    
- [ ] d) Linear Regression.
    

---

**For a Logistic Regression model represented as a single neuron with a sigmoid activation, what function needs to be calculated to apply gradient descent?**

- [ ] a) The mean of the data.
    
- [ ] b) The derivative of the loss function with respect to the weights and biases.
    
- [ ] c) The variance of the data.
    
- [ ] d) The principal components.
    

---

**If the loss function for Logistic Regression is cross-entropy, how does the gradient calculation relate to the difference between the expected and predicted behavior?**

- [ ] a) It is unrelated.
    
- [ ] b) It behaves very similarly, like the derivative of squared error.
    
- [ ] c) It only depends on the input features.
    
- [ ] d) It only depends on the true labels.
    

---

**One source mentions computing the gradient of the loss function for Logistic Regression with respect to each variable. What rule is typically used for this?**

- [ ] a) Product Rule.
    
- [ ] b) Sum Rule.
    
- [ ] c) Chain Rule.
    
- [ ] d) Bayes' Rule.
    

---

**What is one challenge when minimizing the non-convex cost function when using neural network features for classification?**

- [ ] a) It can always be solved in closed form.
    
- [ ] b) Gradient descent will always find the global minimum.
    
- [ ] c) Multiple runs of gradient descent are typically made to ensure convergence to a good local minimum.
    
- [ ] d) The loss function is always convex.
    

---

**What techniques can help numerical optimization techniques avoid poor stationary points of non-convex cost functions, according to one source?**

- [ ] a) Using a fixed learning rate.
    
- [ ] b) Using the hinge loss function.
    
- [ ] c) Using L2 regularizer.
    
- [ ] d) Using an analytical solution.
    

---

**For Logistic Regression with a basis of single hidden layer neural network features, the corresponding Least Squares problem cannot be solved in closed form due to what?**

- [ ] a) The problem is always linearly separable.
    
- [ ] b) The objective function is always convex.
    
- [ ] c) The internal parameters are related in a nonlinear fashion with the basis weights.
    
- [ ] d) The number of data points is too large.
    

---

**In the case of Logistic Regression and Support Vector Machines, due to the similarity of their cost functions, they perform similarly well in practice and can be extended using "kernels" and "feed-forward neural networks" to perform what?**

- [ ] a) Linear regression.
    
- [ ] b) Unsupervised learning.
    
- [ ] c) Nonlinear classification.
    
- [ ] d) Dimensionality reduction.
    

---

**According to one source, Logistic Regression is one of the most famous linear classifiers, based on the principle of maximizing what?**

- [ ] a) The hinge loss.
    
- [ ] b) The error rate.
    
- [ ] c) The probability of a sample belonging to the right class.
    
- [ ] d) The distance between classes.
    

---

### Gradient Descent on m examples

**Training neural networks often uses optimization algorithms on minibatches of data. What is this approach called?**

- [ ] a) Batch Gradient Descent.
    
- [ ] b) Stochastic Gradient Descent (SGD).
    
- [ ] c) Mini-batch Gradient Descent.
    
- [ ] d) Analytical Solution.
    

---

**In mini-batch gradient descent, the gradient is computed using a small number of examples ((m)) sampled from the training set. How does this compare to batch gradient descent?**

- [ ] a) Mini-batch uses the entire dataset, batch uses a subset.
    
- [ ] b) Mini-batch uses a subset, batch uses the entire dataset.
    
- [ ] c) Mini-batch is only used for linear models, batch is for neural networks.
    
- [ ] d) Mini-batch does not use gradients.
    

---

**What is one advantage of using mini-batch gradient descent compared to stochastic gradient descent with a single example?**

- [ ] a) It is slower but more accurate.
    
- [ ] b) It can be more computationally efficient due to vectorization.
    
- [ ] c) It guarantees finding the global minimum.
    
- [ ] d) It does not require calculating gradients.
    

---

**What is one potential disadvantage of using mini-batch gradient descent compared to batch gradient descent?**

- [ ] a) It converges faster.
    
- [ ] b) It can be more computationally expensive per update.
    
- [ ] c) The updates are noisier due to using a subset of data.
    
- [ ] d) It requires more memory.
    

---

**For mini-batch gradient descent, how is the batch size typically chosen?**

- [ ] a) It is fixed to 1.
    
- [ ] b) It is equal to the total number of training examples.
    
- [ ] c) It is a hyperparameter that needs to be tuned.
    
- [ ] d) It is determined by the input dimension.
    

---

**How does mini-batch gradient descent leverage vectorization?**

- [ ] a) It avoids all vector operations.
    
- [ ] b) It applies operations element-wise only.
    
- [ ] c) It performs matrix operations over the minibatch of examples.
    
- [ ] d) It requires manually looping over each example.
    

---

**What happens to the gradient calculation when using mini-batches?**

- [ ] a) It is the same as calculating the gradient for the entire dataset.
    
- [ ] b) It is an approximation of the full gradient.
    
- [ ] c) It is always zero.
    
- [ ] d) It is always infinite.
    

---

**What is a common approach for handling large datasets that do not fit into memory during training?**

- [ ] a) Using batch gradient descent.
    
- [ ] b) Using mini-batch gradient descent or stochastic gradient descent.
    
- [ ] c) Using an analytical solution.
    
- [ ] d) Reducing the number of parameters to zero.
    

---

**What might happen if the batch size is too small in mini-batch gradient descent?**

- [ ] a) The updates are less noisy.
    
- [ ] b) Training can be unstable.
    
- [ ] c) It will always converge to the global optimum.
    
- [ ] d) Vectorization benefits are maximized.
    

---

**What might happen if the batch size is too large in mini-batch gradient descent?**

- [ ] a) Training converges faster.
    
- [ ] b) It requires more memory and computation per update.
    
- [ ] c) The updates are more noisy.
    
- [ ] d) It is equivalent to stochastic gradient descent with a single example.
    

---

### Vectorization

**What is vectorization in the context of machine learning and numerical computation?**

- [ ] a) Using loops to process data element by element.
    
- [ ] b) Performing operations on entire arrays or matrices at once.
    
- [ ] c) Converting numerical data to categorical data.
    
- [ ] d) Reducing the dimensionality of data.
    

---

**Why is vectorization important for machine learning algorithms, especially deep learning?**

- [ ] a) It reduces the number of parameters.
    
- [ ] b) It avoids the need for gradients.
    
- [ ] c) It allows for more efficient computation on hardware like GPUs.
    
- [ ] d) It guarantees better model accuracy.
    

---

**Modern deep learning frameworks leverage hardware like GPUs to accelerate numerical computation. What property of the tensor class (ndarray in NumPy, Tensor in PyTorch/TensorFlow) facilitates this?**

- [ ] a) Automatic differentiation support.
    
- [ ] b) The ability to leverage GPUs.
    
- [ ] c) The ability to store categorical data.
    
- [ ] d) Its resemblance to NumPy's ndarray.
    

---

**What are tensors?**

- [ ] a) Only 1-dimensional arrays.
    
- [ ] b) N-dimensional arrays used to store and manipulate data.
    
- [ ] c) Mathematical functions.
    
- [ ] d) Optimization algorithms.
    

---

**Operations like matrix multiplication and addition can be vectorized. How does this benefit processing multiple examples in a batch?**

- [ ] a) It makes processing each example independent.
    
- [ ] b) It allows processing the entire batch using efficient matrix operations.
    
- [ ] c) It requires manually looping over each example.
    
- [ ] d) It only works for single examples.
    

---

**What is the computational cost of transforming (d) inputs into (q) outputs in a fully connected layer without using techniques like structural matrix approximations?**

- [ ] a) O(d + q).
    
- [ ] b) O(d * q).
    
- [ ] c) O(log(d*q)).
    
- [ ] d) Independent of d and q.
    

---

**Techniques like permutations, Fourier transforms, and scaling can reduce the computational cost of a fully connected layer from quadratic to what?**

- [ ] a) Exponential.
    
- [ ] b) Log-linear.
    
- [ ] c) Linear.
    
- [ ] d) Constant.
    

---

**What kind of decompositions can be used to reduce the cost of a fully connected layer to O((dq/n)) for a compression factor (n)?**

- [ ] a) Singular Value Decomposition (SVD).
    
- [ ] b) Quaternion-like decompositions.
    
- [ ] c) LU decomposition.
    
- [ ] d) Cholesky decomposition.
    

---

**Why are vectorization and efficient implementations on modern hardware like GPUs crucial for machine learning practitioners?**

- [ ] a) They improve model interpretability.
    
- [ ] b) They make models easier to design.
    
- [ ] c) They allow models to be executed more efficiently.
    
- [ ] d) They reduce the need for training data.
    

---

**In the context of deep learning frameworks, what does vectorization enable when processing minibatches?**

- [ ] a) Element-wise operations only.
    
- [ ] b) Efficient processing using matrix operations over the minibatch.
    
- [ ] c) Processing one example at a time.
    
- [ ] d) Reducing the number of layers.
    

---

### Vectorizing Logistic Regression

**How can Logistic Regression be represented to facilitate vectorized computations, particularly when processing multiple examples simultaneously?**

- [ ] a) As separate equations for each example.
    
- [ ] b) In matrix form, using operations like matrix multiplication and vector addition.
    
- [ ] c) By avoiding all numerical operations.
    
- [ ] d) By converting all data to categorical format.
    

---

**When processing a minibatch of input data (X) for Logistic Regression, represented as a matrix where each row is an example, how can the linear combination (Wx + b) be computed efficiently?**

- [ ] a) By looping through each example's vector and applying (wTx+b).
    
- [ ] b) By performing a single matrix multiplication (XWT) (or (XW) depending on convention) and adding the bias vector (b) appropriately.
    
- [ ] c) By computing the mean of the input matrix.
    
- [ ] d) By applying an activation function directly to (X).
    

---

**The softmax function, commonly used in multinomial Logistic Regression, is not an element-wise function because it uses all components of the input vector. How is it typically applied in a vectorized implementation for a batch of examples?**

- [ ] a) Element-wise to the entire input matrix.
    
- [ ] b) By looping through each row (example) of the input matrix and applying the softmax function.
    
- [ ] c) By applying a single softmax operation to the entire input matrix.
    
- [ ] d) It cannot be vectorized.
    

---

**How is the bias term (b) handled in vectorized implementations of linear layers like those in Logistic Regression?**

- [ ] a) It is ignored.
    
- [ ] b) It is added element-wise to the result of the matrix multiplication for each example in the batch.
    
- [ ] c) It is multiplied by the input matrix.
    
- [ ] d) It is applied after the activation function.
    

---

**What is the purpose of representing Logistic Regression (and other linear models) as simple neural networks where inputs are directly wired to the output(s)?**

- [ ] a) To make the model intrinsically non-linear.
    
- [ ] b) To avoid using parameters.
    
- [ ] c) To introduce most of the components required for training more complex models (parametric forms, differentiable objectives, optimization, evaluation).
    
- [ ] d) To restrict the model's expressive power.
    

---

**In a vectorized implementation for a batch of size (n) with (d) input features and (q) output classes (e.g., for softmax regression), what are the typical dimensions of the input matrix (X), weight matrix (W), bias vector (b), and output matrix (O)?**

- [ ] a) (X∈Rd×n), (W∈Rd×q), (b∈Rq), (O∈Rq×n).
    
- [ ] b) (X∈Rn×d), (W∈Rd×q), (b∈Rq) (or broadcast), (O∈Rn×q).
    
- [ ] c) (X∈Rn×d), (W∈Rq×d), (b∈Rn), (O∈Rn×q).
    
- [ ] d) (X∈Rd×n), (W∈Rq×d), (b∈Rn), (O∈Rq×n).
    

---

**When computing the output (O = XW + b) for a batch, how is the bias (b) (which is a vector of size (q)) typically added to the result of (XW) (which is a matrix of size (n×q))?**

- [ ] a) Manually looping and adding the vector (b) to each row of (XW).
    
- [ ] b) Using a mechanism that adds the vector (b) to each row of (XW), often referred to as broadcasting.
    
- [ ] c) By multiplying (b) by a matrix of ones.
    
- [ ] d) By ignoring (b) during the vectorized operation.
    

---

**Why is it more efficient to use vectorized matrix operations for Logistic Regression on a batch of data compared to looping through each example?**

- [ ] a) It uses less memory.
    
- [ ] b) Modern hardware and libraries are optimized for matrix operations.
    
- [ ] c) It simplifies the mathematical derivation.
    
- [ ] d) It avoids the need for an activation function.
    

---

**What is the purpose of the softmax function in the vectorized output layer of multinomial Logistic Regression?**

- [ ] a) To make the output linear.
    
- [ ] b) To produce a probability distribution over the classes for each example in the batch.
    
- [ ] c) To reduce the dimensionality of the output.
    
- [ ] d) To act as a regularizer.
    

---

**In the vectorized implementation of Logistic Regression, the inputs (X) are typically organized as a matrix where each what corresponds to a different data point (example)?**

- [ ] a) Column.
    
- [ ] b) Row.
    
- [ ] c) Element.
    
- [ ] d) Slice.
    

---

### Vectorizing Logistic Regression’s Gradient Output

**When training Logistic Regression using gradient descent on a batch of (n) examples, what is the target of the gradient calculation?**

- [ ] a) The input matrix (X).
    
- [ ] b) The true labels (y).
    
- [ ] c) The parameters (weights (W) and bias (b)).
    
- [ ] d) The output probabilities.
    

---

**In a vectorized implementation, the loss function for the entire batch is often computed. What is this loss based on?**

- [ ] a) The loss for a single example.
    
- [ ] b) The sum or average of the loss over all examples in the batch.
    
- [ ] c) Only the first example's loss.
    
- [ ] d) A randomly selected example's loss.
    

---

**How is the gradient of the total loss (sum/average over the batch) with respect to the weight matrix (W) calculated efficiently in a vectorized implementation?**

- [ ] a) By looping through each example and summing individual gradients.
    
- [ ] b) Using a single matrix operation involving the input matrix (X) and the error signals for the batch.
    
- [ ] c) By only considering the first example's gradient.
    
- [ ] d) By taking the derivative of the activation function.
    

---

**The error signal for a batch of examples, which is crucial for calculating vectorized gradients, is often represented as a matrix. What does each row of this matrix correspond to?**

- [ ] a) The error for a single parameter.
    
- [ ] b) The error for a single example.
    
- [ ] c) The error for a single class.
    
- [ ] d) The error for a single layer.
    

---

**When calculating the gradient of the loss with respect to the bias vector (b) in a vectorized implementation, what operation is typically performed on the error signal matrix?**

- [ ] a) Matrix multiplication.
    
- [ ] b) Element-wise product.
    
- [ ] c) Summation across the example dimension (rows).
    
- [ ] d) Summation across the output dimension (columns).
    

---

**The gradients computed in a vectorized manner for a batch are used to update the model parameters. How are these parameters typically updated in gradient descent?**

- [ ] a) By adding the gradient.
    
- [ ] b) By multiplying by the gradient.
    
- [ ] c) By subtracting the gradient scaled by the learning rate.
    
- [ ] d) By dividing by the gradient.
    

---

**What is the benefit of calculating gradients for the entire batch at once using vectorized operations compared to doing it one example at a time?**

- [ ] a) It uses less memory.
    
- [ ] b) It is computationally faster due to optimized hardware and libraries.
    
- [ ] c) It avoids the need for backpropagation.
    
- [ ] d) It results in a more accurate gradient for a single example.
    

---

**According to one source, representing gradients in matrix form allows for efficient computation using what?**

- [ ] a) Manual loops.
    
- [ ] b) Component-wise product.
    
- [ ] c) Linear algebra operations.
    
- [ ] d) Scalar arithmetic.
    

---

**The vectorization across multiple examples (batching) allows for more efficient computation of forward and backward passes. What type of operations are heavily utilized?**

- [ ] a) Scalar operations.
    
- [ ] b) Matrix operations.
    
- [ ] c) Boolean operations.
    
- [ ] d) String operations.
    

---

**In the context of vectorized gradient computation for Logistic Regression, the true labels for a batch are often represented using what encoding?**

- [ ] a) Binary encoding.
    
- [ ] b) One-hot encoding.
    
- [ ] c) Ordinal encoding.
    
- [ ] d) Label encoding.
    

---

### Broadcasting in Python

**(Based on source context) In deep learning frameworks like PyTorch and TensorFlow, vector operations on tensors are common. What is a tensor?**

- [ ] a) A scalar value.
    
- [ ] b) A 1-dimensional array.
    
- [ ] c) An N-dimensional array.
    
- [ ] d) A mathematical function.
    

---

**(Based on source context) What type of operations on tensors do modern deep learning frameworks leverage GPUs for?**

- [ ] a) File I/O operations.
    
- [ ] b) Numerical computation, such as matrix operations.
    
- [ ] c) String manipulation.
    
- [ ] d) User interface rendering.
    

---

**(Based on source context) When adding a vector (like a bias term) to each row of a matrix (like the result of a linear transformation for a batch), deep learning frameworks often use an implicit mechanism. What is this mechanism related to?**

- [ ] a) Explicit looping.
    
- [ ] b) Matrix inversion.
    
- [ ] c) Duplicating the vector to match the matrix dimensions.
    
- [ ] d) Element-wise operations.
    

---

**(Based on source context) What is the primary benefit of using vectorization and batching in deep learning implementations?**

- [ ] a) It reduces the total number of training examples.
    
- [ ] b) It allows for faster computation on parallel hardware.
    
- [ ] c) It eliminates the need for activation functions.
    
- [ ] d) It simplifies the model architecture.
    

---

**(Based on source context) When implementing algorithms from scratch using libraries like NumPy or the tensor functionalities of PyTorch/TensorFlow, what is a common way to apply a vector operation (like adding a bias) across multiple dimensions of a higher-dimensional tensor?**

- [ ] a) Explicitly write nested loops.
    
- [ ] b) Rely on implicit mechanisms provided by the library for dimension matching.
    
- [ ] c) Convert the tensors to scalars first.
    
- [ ] d) Only perform operations on 1-dimensional tensors.
    

---

**(Based on source context) What property of tensors in deep learning frameworks, resembling NumPy's ndarray, makes neural networks easy to code and fast to run?**

- [ ] a) They only run on CPUs.
    
- [ ] b) They only support integer values.
    
- [ ] c) They support automatic differentiation and leverage GPUs.
    
- [ ] d) They can only store 1-dimensional data.
    

---

**(Based on source context) In a vectorized implementation, if you have a matrix of input features for a batch and a weight matrix, how is the linear combination calculated for all examples simultaneously?**

- [ ] a) Using nested loops and scalar multiplication.
    
- [ ] b) Using a single matrix multiplication operation.
    
- [ ] c) Using element-wise addition.
    
- [ ] d) Using the mean of each matrix.
    

---

**(Based on source context) What is an example of a vectorized operation that can be applied to a matrix?**

- [ ] a) Adding a scalar to each element.
    
- [ ] b) Applying a sigmoid function element-wise.
    
- [ ] c) Multiplying two matrices.
    
- [ ] d) All of the above.
    

---

**(Based on source context) Vectorization is crucial for efficiently computing the output of a neural network layer for a batch of inputs. What does this involve?**

- [ ] a) Looping through each neuron.
    
- [ ] b) Performing matrix multiplications and additions.
    
- [ ] c) Skipping the activation function.
    
- [ ] d) Ignoring the bias term.
    

---

**(Based on source context) When computing gradients using backpropagation on a batch, vectorized operations are used. What do these operations involve?**

- [ ] a) Scalar arithmetic only.
    
- [ ] b) Matrix operations involving the input data, error signals, and weights.
    
- [ ] c) Only operations on 1-dimensional vectors.
    
- [ ] d) Avoiding all multiplication operations.
    

---

### Explanation of Logistic Regression Cost Function (Optional)

**The cross-entropy loss function is commonly used for Logistic Regression. What is its relationship to the negative log-likelihood?**

- [ ] a) It is unrelated.
    
- [ ] b) It calculates the negative log-likelihood of the predicted probability assigned to the true label.
    
- [ ] c) It calculates the mean squared error.
    
- [ ] d) It calculates the hinge loss.
    

---

**For multinomial Logistic Regression with softmax output, the log likelihood can be written as what?**

- [ ] a) The sum of squared errors.
    
- [ ] b) The negative cross entropy.
    
- [ ] c) The product of predicted probabilities.
    
- [ ] d) The hinge loss.
    

---

**What is one reason the cross-entropy loss is suitable for classification problems where the output is interpreted as probabilities?**

- [ ] a) It only works for binary classification.
    
- [ ] b) It penalizes confident wrong predictions more heavily.
    
- [ ] c) It is always a convex function.
    
- [ ] d) It leads to a closed-form solution for parameter estimation.
    

---

**In the context of multinomial Logistic Regression, the softmax function converts the logits into what?**

- [ ] a) Integer labels.
    
- [ ] b) Continuous values.
    
- [ ] c) A probability distribution over the classes.
    
- [ ] d) Binary outputs.
    

---

**Why might minimizing the squared error loss ((∑i=1N​(yi​−zi​)2)) for Logistic Regression with binary labels (0 or 1) be problematic?**

- [ ] a) It is always a convex problem.
    
- [ ] b) It leads to exploding gradients.
    
- [ ] c) The function becomes non-convex and difficult to optimize.
    
- [ ] d) It only works for continuous outputs.
    

---

**What is the goal of minimizing the loss function (like cross-entropy) for Logistic Regression during training?**

- [ ] a) To find parameters that maximize the error.
    
- [ ] b) To find parameters that minimize the difference between predicted probabilities and true labels.
    
- [ ] c) To reduce the number of input features.
    
- [ ] d) To increase the complexity of the model.
    

---

**When calculating the cross-entropy loss in a vectorized way for a batch, what is used to efficiently select the probabilities corresponding to the true labels?**

- [ ] a) Random sampling.
    
- [ ] b) Indexing using the true labels (e.g., one-hot encoding).
    
- [ ] c) Looping through each example.
    
- [ ] d) Matrix multiplication.
    

---

**What is the value of the cross-entropy loss when the predicted probability assigned to the true label is close to 1?**

- [ ] a) Large.
    
- [ ] b) Small (close to 0).
    
- [ ] c) Negative.
    
- [ ] d) Infinite.
    

---

**What is the value of the cross-entropy loss when the predicted probability assigned to the true label is close to 0?**

- [ ] a) Small (close to 0).
    
- [ ] b) Large.
    
- [ ] c) Negative.
    
- [ ] d) Exactly 0.5.
    

---

**According to one source, the derivative of the cross-entropy loss for softmax is very similar to the derivative of squared error. How is this similarity described?**

- [ ] a) Both involve taking the difference between expected and predicted behavior.
    
- [ ] b) Both involve taking the derivative of an exponential function.
    
- [ ] c) Both involve the log of the input.
    
- [ ] d) Both involve only linear operations.
    

---

### Neural Networks Overview

**What is a Neural Network (or Artificial Neural Network)?**

- [ ] a) A type of optimization algorithm.
    
- [ ] b) A directed structure connecting an input layer with an output layer.
    
- [ ] c) A method for dimensionality reduction.
    
- [ ] d) A statistical test.
    

---

**What are the two key elements from which the adjective "neural" comes in Artificial Neural Networks?**

- [ ] a) Biological neurons and synapses.
    
- [ ] b) Input and output layers.
    
- [ ] c) Weights and biases.
    
- [ ] d) Loss functions and optimization algorithms.
    

---

**In the context of neural networks, what is a neuron or basic computational unit?**

- [ ] a) An input feature.
    
- [ ] b) A mathematical function.
    
- [ ] c) A unit that calculates a weighted sum of inputs, adds a bias, and filters the result through an activation function.
    
- [ ] d) A layer in the network.
    

---

**What are the connections between neurons called, each characterized by a synaptic weight?**

- [ ] a) Layers.
    
- [ ] b) Inputs.
    
- [ ] c) Channels.
    
- [ ] d) Synaptic weights/connections.
    

---

**What is added to the weighted sum of inputs in an artificial neuron?**

- [ ] a) Another input feature.
    
- [ ] b) A non-linear function.
    
- [ ] c) A bias term.
    
- [ ] d) The error signal.
    

---

**The result of the weighted sum plus bias in an artificial neuron is filtered by what?**

- [ ] a) The input layer.
    
- [ ] b) The output layer.
    
- [ ] c) An activation function.
    
- [ ] d) A loss function.
    

---

**What property do the operations in a neural network typically have to enable optimization using gradient-based methods?**

- [ ] a) Linearity.
    
- [ ] b) Non-linearity.
    
- [ ] c) Differentiability.
    
- [ ] d) Convexity.
    

---

**What is the name for the parameters that control how well a neural network model explains the data, typically found by optimizing an objective function?**

- [ ] a) Hyperparameters.
    
- [ ] b) Input features.
    
- [ ] c) Model parameters (weights and biases).
    
- [ ] d) Activation functions.
    

---

**What is the goal of training a neural network using numerical optimization methods?**

- [ ] a) To achieve perfect accuracy on the training data.
    
- [ ] b) To estimate parameters so the model performs well on data not used for training.
    
- [ ] c) To reduce the number of layers.
    
- [ ] d) To find an analytical solution.
    

---

**What does "deep learning" refer to?**

- [ ] a) Any machine learning algorithm.
    
- [ ] b) Machine learning concerned with models based on many-layered neural networks.
    
- [ ] c) Unsupervised learning algorithms.
    
- [ ] d) Algorithms that learn only one layer of transformation.
    

---

### Neural Network Representation

**A Multilayer Perceptron (MLP) is one of the simplest kinds of neural networks. It consists of a series of what?**

- [ ] a) Unconnected neurons.
    
- [ ] b) Linear layers combined with elementwise nonlinearities.
    
- [ ] c) Only input and output layers.
    
- [ ] d) Convolutional layers.
    

---

**In an MLP, what are the layers between the input and output layers called?**

- [ ] a) Linear layers.
    
- [ ] b) Activation layers.
    
- [ ] c) Hidden layers.
    
- [ ] d) Convolutional layers.
    

---

**What connects the neurons in one layer of an MLP to the neurons in the next layer?**

- [ ] a) Only non-linear functions.
    
- [ ] b) Weighted connections (weights and biases).
    
- [ ] c) Activation functions directly.
    
- [ ] d) Loss functions.
    

---

**What are the parameters of a neural network layer?**

- [ ] a) Input features.
    
- [ ] b) Output values.
    
- [ ] c) Weights and biases.
    
- [ ] d) Activation functions.
    

---

**How is the output of a neuron typically computed?**

- [ ] a) Only by applying an activation function to the input.
    
- [ ] b) By a weighted sum of its inputs plus a bias, filtered by an activation function.
    
- [ ] c) Only by the sum of its inputs.
    
- [ ] d) By the product of its inputs.
    

---

**In the representation of a neural network with multiple layers, the output of one layer serves as what for the next layer?**

- [ ] a) The parameters.
    
- [ ] b) The loss function.
    
- [ ] c) The input.
    
- [ ] d) The activation function.
    

---

**What does a single neuron map a set of inputs into?**

- [ ] a) A set of outputs.
    
- [ ] b) A single output number.
    
- [ ] c) A probability distribution.
    
- [ ] d) A binary decision.
    

---

**What is the term for layers where each neuron receives all output values from the previous layer?**

- [ ] a) Convolutional layers.
    
- [ ] b) Pooling layers.
    
- [ ] c) Fully connected layers (or dense layers).
    
- [ ] d) Activation layers.
    

---

**In a diagram of a neural network, what typically represents the connections between neurons?**

- [ ] a) Boxes.
    
- [ ] b) Lines or edges.
    
- [ ] c) Circles.
    
- [ ] d) Text labels.
    

---

**What do convolutional layers typically operate on?**

- [ ] a) 1D vectors.
    
- [ ] b) 2D inputs like images.
    
- [ ] c) Categorical data.
    
- [ ] d) Text sequences.
    

---

### Computing a Neural Network’s Output

**To compute a neural network's output, what is the process called where calculations proceed from the input layer to the output layer?**

- [ ] a) Backpropagation.
    
- [ ] b) Gradient Descent.
    
- [ ] c) Forward Propagation (or forward pass).
    
- [ ] d) Optimization.
    

---

**In a single neuron, the output is calculated as (y=φ(wTx+b)). What is the term (wTx+b)?**

- [ ] a) The activation function.
    
- [ ] b) The input vector.
    
- [ ] c) The weighted sum plus bias.
    
- [ ] d) The output value.
    

---

**For a layer with D units transforming an input vector x, what is the output vector y calculated as in a linear layer?**

- [ ] a) (y=φ(x)).
    
- [ ] b) (y=Wx+b).
    
- [ ] c) (y=wTx+b).
    
- [ ] d) (y=x+b).
    

---

**In a multilayer network, the output of each layer is typically computed by first performing a linear transformation (matrix multiplication and bias addition) followed by what?**

- [ ] a) Another linear transformation.
    
- [ ] b) An elementwise nonlinear activation function.
    
- [ ] c) A loss function.
    
- [ ] d) A gradient calculation.
    

---

**When processing a batch of inputs (X) with a linear layer defined by weights (W) and bias (b), the vectorized output (Y) is computed using what matrix operation?**

- [ ] a) (Y=XW+b) (with appropriate broadcasting/dimensions).
    
- [ ] b) (Y=WX+b).
    
- [ ] c) (Y=X+W+b).
    
- [ ] d) (Y=X∗W∗b) (element-wise).
    

---

**What converts the linear combination of inputs into the final output of a neuron or layer, introducing non-linearity?**

- [ ] a) The weight matrix.
    
- [ ] b) The bias vector.
    
- [ ] c) The activation function.
    
- [ ] d) The input features.
    

---

**For a classification problem, the output layer often uses the softmax function. What is the result of applying softmax to the final layer's linear outputs (logits)?**

- [ ] a) A single label.
    
- [ ] b) A continuous score.
    
- [ ] c) A probability distribution over the classes.
    
- [ ] d) A binary decision.
    

---

**In a feedforward neural network, what is the flow of information?**

- [ ] a) From output to input.
    
- [ ] b) Only within hidden layers.
    
- [ ] c) From input layer, through hidden layers, to the output layer.
    
- [ ] d) Back and forth between layers.
    

---

**What operation is performed elementwise after a linear transformation in many neural network layers?**

- [ ] a) Matrix multiplication.
    
- [ ] b) Adding a bias.
    
- [ ] c) Applying an activation function.
    
- [ ] d) Calculating the gradient.
    

---

**How does the computation of a neural network's output relate to its computational graph representation?**

- [ ] a) The output cannot be computed from the graph.
    
- [ ] b) The computation follows the directed structure of the graph from inputs to outputs.
    
- [ ] c) The computation requires reversing the graph's direction.
    
- [ ] d) The computation involves random traversal of the graph.
    

---

### Vectorizing across multiple examples

**When processing a batch of multiple examples in a neural network, how are the inputs typically organized?**

- [ ] a) As individual vectors processed one by one.
    
- [ ] b) As a single matrix where each row (or column) is an example.
    
- [ ] c) As a list of tensors.
    
- [ ] d) As a scalar value representing the batch size.
    

---

**Why is vectorizing across multiple examples important for training neural networks on modern hardware?**

- [ ] a) It reduces the number of parameters.
    
- [ ] b) It allows for parallel computation on GPUs and other accelerators.
    
- [ ] c) It simplifies the model architecture.
    
- [ ] d) It avoids the need for a loss function.
    

---

**In a vectorized implementation, a linear layer transformation (y=Wx+b) for a single example becomes a matrix operation for a batch of examples. If (X) is the input matrix for a batch and (Y) is the output matrix, what is the form?**

- [ ] a) (Y=XW+b) (with appropriate dimensions).
    
- [ ] b) (Y=WX+b).
    
- [ ] c) (Y=X+W+b).
    
- [ ] d) (Y=X∗W∗b).
    

---

**What does vectorizing across multiple examples enable during the forward pass?**

- [ ] a) Computing each example's output independently and sequentially.
    
- [ ] b) Performing the same operation on all examples simultaneously using matrix operations.
    
- [ ] c) Skipping certain layers for some examples.
    
- [ ] d) Reducing the batch size.
    

---

**What is a key benefit of processing data in batches using vectorization?**

- [ ] a) It reduces the amount of training data needed.
    
- [ ] b) It reduces overfitting.
    
- [ ] c) It allows for more efficient utilization of hardware designed for parallel matrix operations.
    
- [ ] d) It simplifies the mathematical derivation of gradients.
    

---

**When vectorizing across multiple examples, the parameters of the neural network (weights and biases) are shared across all examples within the batch. What does this imply?**

- [ ] a) Each example has its own set of parameters.
    
- [ ] b) The same parameters are used for the entire batch.
    
- [ ] c) Parameters change for each example in the batch.
    
- [ ] d) Parameters are not used when processing a batch.
    

---

**The outputs of a layer for a batch of examples are collected into a matrix. What does each row (or column, depending on convention) of this matrix represent?**

- [ ] a) The parameters of the layer.
    
- [ ] b) The input features for the next layer.
    
- [ ] c) The output of the layer for a single example in the batch.
    
- [ ] d) The activation function values.
    

---

**What enables efficient training of neural networks with stochastic gradient descent by processing subsets of data simultaneously?**

- [ ] a) Random initialization.
    
- [ ] b) Vectorization across multiple examples (batching).
    
- [ ] c) Using non-linear activation functions.
    
- [ ] d) Manual gradient calculation.
    

---

**When using vectorization, what is the dimension of the input data for a batch of (n) examples, each with (d) features?**

- [ ] a) (n×d) or (d×n) matrix.
    
- [ ] b) A vector of size (n).
    
- [ ] c) A vector of size (d).
    
- [ ] d) A scalar value.
    

---

**What is the primary goal of vectorizing computations in deep learning frameworks?**

- [ ] a) To reduce memory usage.
    
- [ ] b) To maximize computational speed and efficiency.
    
- [ ] c) To simplify the model architecture.
    
- [ ] d) To guarantee finding the global minimum.
    

---

### Explanation for vectorized implementation

**Vectorization enables efficient computation by utilizing hardware like GPUs that are optimized for what types of operations?**

- [ ] a) Scalar arithmetic.
    
- [ ] b) Matrix and vector operations.
    
- [ ] c) String processing.
    
- [ ] d) Conditional logic.
    

---

**Why are matrix operations computationally faster than explicit loops for the same calculation on modern processors?**

- [ ] a) Because they require less memory.
    
- [ ] b) Because they can utilize parallel processing units efficiently.
    
- [ ] c) Because they avoid multiplication operations.
    
- [ ] d) Because they simplify the mathematical expression.
    

---

**What does vectorization mean in the context of a neural network layer processing a batch of data?**

- [ ] a) Applying the operation to one example at a time.
    
- [ ] b) Applying the layer's operation to the entire batch of examples using matrix operations.
    
- [ ] c) Converting the batch into a single vector.
    
- [ ] d) Ignoring the batch structure and processing randomly.
    

---

**How does vectorization simplify the implementation of gradient calculations for a batch?**

- [ ] a) It requires looping through each example's gradient.
    
- [ ] b) It allows computing gradients for the entire batch using a few matrix operations.
    
- [ ] c) It avoids the need for derivatives.
    
- [ ] d) It requires calculating the gradient for the entire dataset.
    

---

**What is the role of libraries like NumPy, PyTorch, and TensorFlow in vectorized implementations?**

- [ ] a) They perform manual gradient calculation.
    
- [ ] b) They provide highly optimized tensor (N-dimensional array) operations.
    
- [ ] c) They visualize the data.
    
- [ ] d) They automatically select the best model architecture.
    

---

**When using a vectorized implementation for a layer, the computation for each neuron's output across the entire batch is often combined into a single operation. What kind of operation?**

- [ ] a) Element-wise addition.
    
- [ ] b) Scalar multiplication.
    
- [ ] c) Matrix multiplication.
    
- [ ] d) Activation function.
    

---

**What allows for efficient parallel processing of matrix operations on GPUs?**

- [ ] a) Their limited number of processing cores.
    
- [ ] b) Their architecture is designed for linear algebra.
    
- [ ] c) They are optimized for sequential processing.
    
- [ ] d) They do not support floating-point numbers.
    

---

**How does vectorization benefit the calculation of the loss function for a batch of data?**

- [ ] a) The loss must be calculated separately for each example.
    
- [ ] b) The loss for the entire batch (e.g., sum or mean) can be computed efficiently using vectorized operations.
    
- [ ] c) Vectorization avoids the need for a loss function.
    
- [ ] d) The loss calculation becomes less accurate.
    

---

**What is the relationship between vectorization and the concept of mini-batches in gradient descent?**

- [ ] a) Vectorization is only used with batch gradient descent, not mini-batches.
    
- [ ] b) Vectorization is crucial for efficiently processing mini-batches.
    
- [ ] c) Mini-batches are used to avoid vectorization.
    
- [ ] d) Vectorization is only applicable to single data points.
    

---

**What does an N-dimensional array (tensor) resemble in classical scientific computing libraries like NumPy?**

- [ ] a) A list or vector.
    
- [ ] b) A scalar.
    
- [ ] c) An ndarray.
    
- [ ] d) A function.
    

---

### Activation Functions

**What is the purpose of an activation function in a neural network?**

- [ ] a) To perform a linear transformation.
    
- [ ] b) To decide whether a neuron should be activated or not, filtering the weighted sum and bias.
    
- [ ] c) To calculate the loss function.
    
- [ ] d) To add a bias term.
    

---

**What kind of operators are activation functions typically?**

- [ ] a) Linear operators.
    
- [ ] b) Differentiable operators for transforming input signals to outputs.
    
- [ ] c) Non-differentiable operators.
    
- [ ] d) Optimization algorithms.
    

---

**Most activation functions add what property to the transformation from input to output?**

- [ ] a) Linearity.
    
- [ ] b) Differentiability.
    
- [ ] c) Convexity.
    
- [ ] d) Non-linearity.
    

---

**What is considered the most popular choice for an activation function in practice due to its simplicity and performance?**

- [ ] a) Sigmoid.
    
- [ ] b) Tanh.
    
- [ ] c) Rectified Linear Unit (ReLU).
    
- [ ] d) Softmax.
    

---

**What is the definition of the Rectified Linear Unit (ReLU) function for an element (x)?**

- [ ] a) (max(x,0)).
    
- [ ] b) (1/(1+e−x)).
    
- [ ] c) ((ex−e−x)/(ex+e−x)).
    
- [ ] d) (log(1+ex)).
    

---

**What activation function is still widely used on output units when interpreting outputs as probabilities for binary classification?**

- [ ] a) ReLU.
    
- [ ] b) Tanh.
    
- [ ] c) Sigmoid.
    
- [ ] d) Softplus.
    

---

**The sigmoid function can pose challenges for optimization because its gradient vanishes for large positive and negative arguments. What can this lead to?**

- [ ] a) Faster convergence.
    
- [ ] b) Plateaus that are difficult to escape from.
    
- [ ] c) Increased model accuracy.
    
- [ ] d) Simplified parameter initialization.
    

---

**What activation function is a smooth, differentiable approximation to a thresholding unit?**

- [ ] a) ReLU.
    
- [ ] b) Softmax.
    
- [ ] c) Sigmoid.
    
- [ ] d) GELU.
    

---

**The softmax function is often used in the output layer for what type of problems?**

- [ ] a) Binary classification.
    
- [ ] b) Regression.
    
- [ ] c) Multiclass classification.
    
- [ ] d) Clustering.

---
## Luyện tập

What activation function is defined as  $\max(a, 0) + \alpha \cdot \min(a, 0)$ ?

- [ ] a) ReLU.
    
- [x] b) Leaky ReLU.
    
- [ ] c) ELU.
    
- [ ] d) Swish.

**1. What is the main learning objective when studying the basic building blocks of ResNets?**

- [ ] a) Training a state-of-the-art neural network for image classification.
    
- [x] b) Implementing the basic building blocks of ResNets in a deep neural network using Keras.
    
- [ ] c) Preprocessing and augmenting data using the Keras Sequential API.
    
- [ ] d) Fine-tuning the final layers of a classifier to improve accuracy.
    

**2. Why is it useful to review case studies of neural networks in computer vision research?**

- [ ] a) They provide ready-made solutions for all computer vision tasks.
    
- [ ] b) They help create new datasets from a directory.
    
- [x] c) They provide useful insights and ideas for the learner's own work.
    
- [ ] d) They allow for fine-tuning the final layers of a classifier.
    

**3. Which classic neural networks have been successful in computer vision and are used as models or starting points?**

- [ ] a) MobileNet, EfficientNet, Transformer.
    
- [x] b) LeNet-5, AlexNet, VGG, ResNet, and Inception.
    
- [ ] c) GANs, Autoencoders, Reinforcement Learning.
    
- [ ] d) Only LeNet-5 and AlexNet.
    

**4. What input image size was the LeNet-5 architecture designed to handle?**

- [ ] a) 28x28x1.
    
- [x] b) 32x32x1.
    
- [ ] c) 14x14x6.
    
- [ ] d) 10x10x16.
    

**5. Who proposed the VGG-16 network in 2014?**

- [ ] a) Christian Szegedy at Google.
    
- [ ] b) Andrew G. Howard and colleagues at Google.
    
- [x] c) Karen Simonyan and Andrew Zisserman of the Visual Geometry Group Lab at the University of Oxford.
    
- [ ] d) Mingxing Tan and Quoc V. Le at Google.
    

**6. How many total layers does VGG-16 consist of?**

- [x] a) 13 convolutional layers and 3 fully connected layers.
    
- [ ] b) 16 layers, including 13 convolutional layers, 5 max-pooling layers, and 3 fully connected layers.
    
- [ ] c) 5 max-pooling layers and 3 fully connected layers.
    
- [ ] d) 13 convolutional layers and 5 max-pooling layers.
    

**7. How did VGG-16 perform in the ImageNet Large Scale Visual Recognition Challenge?**

- [ ] a) Average performance.
    
- [ ] b) Poor performance.
    
- [x] c) State-of-the-art performance.
    
- [ ] d) Performance only acceptable for simple images.
    

**8. What is the purpose of a 1x1 convolution?**

- [ ] a) To increase the spatial dimensions of the input image.
    
- [ ] b) To reduce the number of channels in an input volume.
    
- [ ] c) To apply a non-linear function without changing dimensions.
    
- [x] d) Both b and c.
    

**9. Is the 1x1 convolution operation non-linear?**

- [ ] a) Yes, and this allows it to learn a more complex function of the input volume.
    
- [x] b) No, it is just a linear transformation.
    
- [ ] c) Only when used in an Inception network.
    
- [ ] d) It depends on the size of the output channels.
    

**10. For what purpose was the MobileNet convolutional neural network architecture designed?**

- [ ] a) Efficient processing on mobile devices and embedded systems.
    
- [ ] b) Achieving the highest accuracy on large datasets.
    
- [ ] c) Natural language processing.
    
- [x] d) Real-time object detection on cloud servers.
    

**11. What type of convolution does MobileNet use to reduce the number of computations and parameters?**

- [ ] a) Normal convolution.
    
- [x] b) Depthwise separable convolutions.
    
- [ ] c) Transposed convolution.
    
- [ ] d) 3D convolution.
    

**12. The computational cost of a normal convolution is proportional to which factors?**

- [ ] a) The number of parameters of the filter.
    
- [ ] b) The number of filter positions.
    
- [ ] c) The number of filters.
    
- [x] d) All of the above.
    

**13. Depthwise separable convolution can be used as a building block for which network architecture?**

- [ ] a) LeNet.
    
- [ ] b) VGG.
    
- [x] c) MobileNet.
    
- [ ] d) AlexNet.
    

**14. When performing a convolution on an RGB image, what happens with the filters and the output volume?**

- [ ] a) Only one filter is used for the entire image.
    
- [x] b) Different filters are used to detect different features in the image, and the outputs of each filter can be stacked to form a 3D volume.
    
- [ ] c) The convolution is only applied to the red channel.
    
- [ ] d) The output volume is always 1x1.
    

**15. In a layer of a convolutional neural network, which formula represents the forward propagation?**

- [x] a) Z = W * X + b
    
- [ ] b) Z = Wa + b
    
- [ ] c) a = g(X)
    
- [ ] d) a = Z
    

**16. If you have 10 filters of size 3x3x3 in one layer of a convolutional neural network, how many parameters does this layer have?**

- [ ] a) 27 parameters.
    
- [ ] b) 28 parameters (27 filter parameters + 1 bias).
    
- [x] c) 280 parameters (28 * 10 filters).
    
- [ ] d) 10 parameters.
    

**17. What are the main types of layers in a convolutional network?**

- [ ] a) Input, Hidden, Output.
    
- [x] b) Convolution, Pooling, Fully connected.
    
- [ ] c) Encoder, Decoder, Attention.
    
- [ ] d) Recurrent, LSTM, GRU.
    

**18. What is the main function of the pooling layer in a CNN?**

- [ ] a) To increase the size of the representation.
    
- [x] b) To reduce the size of the representation and speed up computation.
    
- [ ] c) To add fully connected layers.
    
- [ ] d) To apply non-linear activation functions.
    

**19. What is the advantage of a Pooling layer?**

- [ ] a) Reduces data dimensionality and computational cost.
    
- [ ] b) Prevents overfitting.
    
- [ ] c) Helps achieve translation invariance.
    
- [x] d) All of the above.
    

**20. What is the disadvantage of a Pooling layer?**

- [ ] a) Information loss.
    
- [ ] b) Can cause over-smoothing.
    
- [ ] c) Introduces hyperparameters that need tuning.
    
- [x] d) All of the above.
    

**21. What is convolution used to detect in an image?**

- [ ] a) Only general features.
    
- [ ] b) Only specific features.
    
- [x] c) Edges in the image.
    
- [ ] d) None of the above.
    

**22. What is the goal of Transpose Convolution?**

- [ ] a) To reduce the input size.
    
- [x] b) To upsample a small input into a larger output, often used in semantic segmentation.
    
- [ ] c) To only apply a filter on the input regardless of position.
    
- [ ] d) To perform a simple matrix multiplication.
    

**23. What is the key feature of One-shot learning in face recognition?**

- [ ] a) It requires many images for each new person.
    
- [x] b) It recognizes a person from a single image.
    
- [ ] c) It uses the Euclidean distance function to compare faces.
    
- [ ] d) It does not require retraining the network when adding a new person to the database.
    

**24. How do Siamese networks solve the one-shot learning problem in face recognition?**

- [ ] a) By learning a direct classification function.
    
- [x] b) By learning a similarity function to measure the difference between images.
    
- [ ] c) By learning a cryptographic hash function.
    
- [ ] d) By learning a set of fully connected layers.
    

**25. What loss function is used to define the objective function in a Siamese network?**

- [ ] a) Cross-entropy loss.
    
- [ ] b) Mean squared error.
    
- [x] c) Triplet loss.
    
- [ ] d) Softmax loss.
    

### **II. Deep Neural Networks (DNNs) and Related Concepts**

**26. What is the main goal of initializing neural network weights randomly with small values?**

- [ ] a) To ensure all hidden units compute the same function.
    
- [x] b) To speed up the learning process by breaking symmetry.
    
- [ ] c) To reduce the computational cost of the network.
    
- [ ] d) To prevent the exploding gradients phenomenon.
    

**27. The progress of neural network learning has been driven by recent improvements in which factors?**

- [x] a) Computational power and data availability.
    
- [ ] b) Only the development of new algorithms.
    
- [ ] c) Only the increase in unlabeled data.
    
- [ ] d) The size of the test datasets.
    

**28. Which of the following best describes what happens during forward propagation in a deep neural network?**

- [ ] a) Calculating derivatives and updating weights.
    
- [x] b) The network computes outputs layer by layer using weighted sums and nonlinear activation functions.
    
- [ ] c) Only involves applying a non-linear activation function.
    
- [ ] d) Only involves updating weights.
    

**29. What does the term 'm' represent in the formulas for the matrix sizes W, b, dW, db, Z, A, dZ, dA?**

- [ ] a) The number of layers in the network.
    
- [ ] b) The size of the output.
    
- [x] c) The number of training examples.
    
- [ ] d) The number of parameters.
    

**30. What is the main advantage of using a deep architecture (many layers) over a shallow one (few layers) in deep learning?**

- [ ] a) They are always easier to train.
    
- [x] b) They can compute more complex functions more efficiently by representing them with exponentially fewer hidden units.
    
- [ ] c) They require less training data.
    
- [ ] d) They minimize the risk of overfitting.
    

**31. What does the overall process of training a neural network involve?**

- [ ] a) Propagating outputs through the network only..
    
- [ ] b)Computing gradients without using model predictions.
    
- [x] c) Computing predictions and updating weights based on the loss.
    
- [ ] d)Manually tuning layer parameters after each epoch.
    

**32. Why do deep neural networks work surprisingly well?**

- [ ] a) They only require a few lines of code to work.
    
- [x] b) They are fed a large amount of data and learn from it using hidden layers.
    
- [ ] c) They are manually tuned.
    
- [ ] d) They always use a small number of parameters.
    

**33. What does selecting the right hyperparameters help with?**

- [ ] a) Increase training time.
    
- [ ] b) Decrease accuracy.
    
- [x] c) Make the model more effective.
    
- [ ] d) No significant impact.
    

**34. Why is applying deep learning a very empirical process?**

- [ ] a) There is always a fixed method for choosing hyperparameters.
    
- [x] b) It requires trying different values to see what works best for a specific application.
    
- [ ] c) Only experienced researchers can tune hyperparameters.
    
- [ ] d) There is no need to tune hyperparameters.
    

**35. When will initializing neural network weights to zero lead to symmetry and slow learning?**

- [ ] a) With shallow neural networks.
    
- [ ] b) With deep neural networks with many hidden units.
    
- [ ] c) When hidden units compute the same function.
    
- [ ] d) With any neural network.
    

**36. In which fields has deep learning been successfully applied?**

- [ ] a) Only computer vision.
    
- [ ] b) Computer vision, natural language processing, speech recognition, online advertising, and logistics.
    
- [ ] c) Only tasks with small datasets.
    
- [ ] d) Only tasks that do not require model training.
    

**37. What is the main goal of initializing neural network weights randomly?**

- [ ] a) To ensure hidden units compute the same function.
    
- [ ] b) To enhance the randomness of the output.
    
- [ ] c) To break the symmetry in the hidden units, helping the network learn more effectively.
    
- [ ] d) To reduce the number of parameters in the network.
    

**38. In a neural network representation, what is a hidden layer?**

- [ ] a) The input layer of the network.
    
- [ ] b) The output layer of the network.
    
- [ ] c) Its values are not observed in the training set.
    
- [ ] d) The last layer before making a prediction.
    

**39. How does Batch Gradient Descent update the model parameters in one epoch?**

- [ ] a) Each training sample is used to perform one update.
    
- [ ] b) A single time using the entire training dataset.
    
- [ ] c) Using a subset of the training data for each iteration.
    
- [ ] d) It does not update the parameters.
    

**40. How does Mini-batch Gradient Descent speed up the deep learning training process on large datasets?**

- [ ] a) By processing the entire dataset at once.
    
- [ ] b) By only using backpropagation to update weights.
    
- [ ] c) By processing smaller subsets, or mini-batches, at a time, performing forward and backward propagation on each mini-batch.
    
- [ ] d) By skipping the gradient calculation.
    

**41. What does one epoch in deep learning training mean?**

- [ ] a) One iteration of the gradient descent algorithm.
    
- [ ] b) Each sample of the training set has passed through the network once to update the parameters.
    
- [ ] c) The number of weight updates.
    
- [ ] d) The size of the mini-batch.
    

**42. In Mini-batch Gradient Descent, how many iterations does one epoch correspond to?**

- [ ] a) A single iteration.
    
- [ ] b) n iterations, where n is the number of training samples.
    
- [ ] c) n/b iterations, where b is the size of the mini-batch.
    
- [ ] d) An arbitrary number of iterations.
    

**43. When can gradient descent with momentum be used to reach a global minimum faster?**

- [ ] a) When using a smaller learning rate.
    
- [ ] b) When a larger learning rate leads to larger update steps, and a faster learning rate in the horizontal direction.
    
- [ ] c) When there are only small oscillations in the vertical direction.
    
- [ ] d) When β (momentum) is 0.
    

**44. What is the learning rate decay technique?**

- [ ] a) A technique to gradually increase the learning rate during training.
    
- [ ] b) A technique used to gradually decrease the learning rate α over time during the training of a neural network.
    
- [ ] c) A technique used only in the initial stage of training.
    
- [ ] d) A technique to keep the learning rate constant.
    

**45. Why is learning rate decay important?**

- [ ] a) To avoid getting stuck in local minima.
    
- [ ] b) To speed up convergence and reduce oscillations around the global minimum.
    
- [ ] c) To prevent overfitting.
    
- [ ] d) To ensure the gradient calculation is always large.
    

**46. In deep neural networks, what are the issues with local minima?**

- [ ] a) It is a major problem in modern deep learning.
    
- [ ] b) Most non-gradient points in the cost function are not local minima but saddle points.
    
- [ ] c) It is easy to get stuck.
    
- [ ] d) It only occurs in convex functions.
    

**47. Which hyperparameter is considered the most important when tuning a deep neural network?**

- [ ] a) Adam’s hyperparameters (β1, β2, ε).
    
- [ ] b) The number of hidden layers.
    
- [ ] c) The learning rate (α).
    
- [ ] d) The mini-batch size.
    

**48. Which method is recommended for searching for effective hyperparameters?**

- [ ] a) Random sampling.
    
- [ ] b) Grid search.
    
- [ ] c) Sequential search.
    
- [ ] d) A 5x5 grid search.
    

**49. When choosing values for hyperparameters like the learning rate (alpha) or beta in exponential weighted averaging, what is a more effective approach?**

- [ ] a) Choosing values from a uniform distribution.
    
- [ ] b) Sampling on a logarithmic scale.
    
- [ ] c) Only choosing large values.
    
- [ ] d) Only choosing small values.
    

**50. Who developed Batch Normalization?**

- [ ] a) Andrew Ng.
    
- [ ] b) Sergey Ioffe and Christian Szegedy.
    
- [ ] c) Geoffrey Hinton.
    
- [ ] d) Yann LeCun.
    

**51. What is the purpose of Batch Normalization?**

- [ ] a) To make deep neural networks learn slower.
    
- [ ] b) To normalize the mean and variance of the hidden unit values, enhancing training efficiency and the robustness of the neural network.
    
- [ ] c) To reduce the number of parameters in the network.
    
- [ ] d) To cause larger oscillations during training.
    

**52. For what type of classification problem is Softmax regression used?**

- [ ] a) Binary classification.
    
- [ ] b) Multi-class classification (more than two classes).
    
- [ ] c) Linear regression.
    
- [ ] d) Problems with no hidden layers.
    

**53. In multi-class classification, how many units does the output layer of Softmax regression have?**

- [ ] a) One unit.
    
- [ ] b) Two units.
    
- [ ] c) The number of units corresponds to the total number of classes.
    
- [ ] d) The number of units equals the number of hidden layers.
    

**54. Which deep learning frameworks are mentioned as popular?**

- [ ] a) Caffe/Caffe2, CNTK, DL4J, Keras, Lasagne, mxnet, PaddlePaddle, TensorFlow, Theano, Torch.
    
- [ ] b) PyTorch, JAX, Scikit-learn.
    
- [ ] c) MATLAB, R, SAS.
    
- [ ] d) Only TensorFlow and Keras.
    

**55. What is TensorFlow?**

- [ ] a) An open-source machine learning library developed by the Google Brain team.
    
- [ ] b) A proprietary framework from Microsoft.
    
- [ ] c) A programming language for deep learning.
    
- [ ] d) A large dataset.
    

**56. What happens when you implement a minimization function in TensorFlow?**

- [ ] a) You must implement both forward and backward propagation.
    
- [ ] b) TensorFlow will automatically perform backpropagation.
    
- [ ] c) You only need to define the loss function.
    
- [ ] d) It only works with custom optimization algorithms.
    

**57. When should you consider training and testing on different data distributions?**

- [ ] a) Always.
    
- [ ] b) When the training set is significantly larger than the dev/test set, and the data sources are different.
    
- [ ] c) When the data comes from the same distribution.
    
- [ ] d) Never, as it leads to poor accuracy.
    

**58. What methods do deep learning researchers and practitioners often use instead of a priori guarantees?**

- [ ] a) Only linear models.
    
- [ ] b) Methods that have generalized well on similar problems in the past and post hoc generalization certification through empirical evaluations.
    
- [ ] c) Methods that only work on the training set.
    
- [ ] d) Methods based on a small number of parameters.
    

**59. How do deep networks tend to be over-parameterized compared to classical linear models?**

- [ ] a) Fewer parameters.
    
- [ ] b) More parameters than the number of examples.
    
- [ ] c) The same number of parameters.
    
- [ ] d) No parameters.
    

**60. In the Transformer architecture, why is multi-head self-attention effective?**

- [ ] a) It reduces the number of parameters.
    
- [ ] b) It allows for parallel computation, making it efficient and suitable for large-scale deep learning models.
    
- [ ] c) It only works with RNNs.
    
- [ ] d) It only computes a single set of attention weights.
    

**61. In what forms have Transformers been pre-trained?**

- [ ] a) Encoder only.
    
- [ ] b) Encoder-decoder.
    
- [ ] c) Decoder only.
    
- [ ] d) All of the above.
    

**62. What factors benefit the performance of Transformers?**

- [ ] a) Smaller models.
    
- [ ] b) Less training data.
    
- [ ] c) Larger models, more training data, and more computational resources.
    
- [ ] d) Only using text data.
    

**63. What challenges does optimization in deep learning often face?**

- [ ] a) Only encountering local minima.
    
- [ ] b) High computational cost, handling gradients, hyperparameter optimization.
    
- [ ] c) Always converging quickly.
    
- [ ] d) Easily finding the global optimum.
    

**64. What is the main goal of optimization in deep learning?**

- [ ] a) To make the model more complex.
    
- [ ] b) To minimize the model's loss function.
    
- [ ] c) To increase the number of parameters.
    
- [ ] d) To reduce the number of training epochs.
    

**65. In the context of deep learning, what is the significance of the asymmetry between random access memory and the growth of data and computational power?**

- [ ] a) Statistical models need to become more memory-efficient.
    
- [ ] b) More machine cycles can be spent on parameter optimization.
    
- [ ] c) The sweet spot in machine learning has shifted from linear models to deep neural networks.
    
- [ ] d) All of the above.
    

**66. What differentiates deep learning from traditional methods?**

- [ ] a) Deep learning only learns one layer of transformation.
    
- [ ] b) The operations are learned in multiple layers of representation that are learned jointly from data in deep learning.
    
- [ ] c) Deep learning requires manual feature engineering.
    
- [ ] d) Deep learning cannot handle low-level sensory data.
    

**67. In what types of problems has deep learning succeeded where traditional methods have struggled?**

- [ ] a) Only simple classification problems.
    
- [ ] b) Learning from raw audio signals, raw pixel values of images, or mapping between sentences of arbitrary length to other languages.
    
- [ ] c) Only problems requiring manual feature engineering.
    
- [ ] d) Problems with only small labeled datasets.
    

**68. What conveniences do modern deep learning frameworks like Theano, DistBelief, and Caffe provide?**

- [ ] a) Only support the Lisp programming language.
    
- [ ] b) Automatic differentiation and the convenience of Python.
    
- [ ] c) Only allow manual implementation of gradient-based algorithms.
    
- [ ] d) Do not provide optimized library functions.
    

**69. How does the size of the training dataset affect overfitting?**

- [ ] a) Smaller datasets increase the likelihood of overfitting.
    
- [ ] b) Larger datasets increase the likelihood of overfitting.
    
- [ ] c) Dataset size does not affect overfitting.
    
- [ ] d) It only affects linear models.
    

**70. What is the main goal of training word2vec?**

- [ ] a) Text classification.
    
- [ ] b) Embedding words into a vector space to capture semantic relationships.
    
- [ ] c) Language translation.
    
- [ ] d) Object detection in images.
    

**71. What is the main problem with the softmax classification method?**

- [ ] a) High computational cost when the vocabulary is large.
    
- [ ] b) Difficulty in sampling the context c.
    
- [ ] c) Both a and b.
    
- [ ] d) No issues.
    

**72. How does negative sampling create a supervised learning problem?**

- [ ] a) The task is to predict a random dictionary word.
    
- [ ] b) The task is to predict whether a pair of words is a context-target pair.
    
- [ ] c) The task is to generate negative examples.
    
- [ ] d) The task is to predict the context.
    

**73. How does the computational cost of the negative sampling algorithm compare to the large Softmax model?**

- [ ] a) Much higher.
    
- [ ] b) Much lower.
    
- [ ] c) The same.
    
- [ ] d) Higher only when K is large.
    

**74. What is recommended for sampling negative examples?**

- [ ] a) Sampling from the empirical frequencies.
    
- [ ] b) Uniform random sampling from the dictionary.
    
- [ ] c) A heuristic value proportional to the frequency of a word to the power of three-quarters.
    
- [ ] d) None of the above.
    

**75. What is sentiment classification in NLP?**

- [ ] a) A problem that only analyzes positive opinions.
    
- [ ] b) Analyzing text to determine positive or negative opinions.
    
- [ ] c) A problem that does not require word embeddings.
    
- [ ] d) A problem with no labeled data.
    

**76. How have word embeddings been used to mitigate the problem of limited labeled training data in sentiment classification?**

- [ ] a) By introducing new hyperparameters.
    
- [ ] b) By allowing learning from a much larger text corpus.
    
- [ ] c) By reducing the size of the vocabulary.
    
- [ ] d) By using one-hot encoding directly.
    

**77. What biases can word embeddings inherit from the training data?**

- [ ] a) Only biases related to sentence structure.
    
- [ ] b) Biases such as gender stereotypes.
    
- [ ] c) Bias in the learning rate.
    
- [ ] d) No biases.
    

**78. What is the main goal of the attention mechanism in sequence models?**

- [ ] a) To allow the model to focus on different parts of the input sequence at different times.
    
- [ ] b) To only reduce the size of the input sequence.
    
- [ ] c) To only speed up computation.
    
- [ ] d) To generate word representations independently.
    

**79. What applications does the attention model have besides translation?**

- [ ] a) Only speech recognition.
    
- [ ] b) Image captioning.
    
- [ ] c) Text classification.
    
- [ ] d) None.
    

**80. What is the definition of 'mismatched training and dev/test data'?**

- [ ] a) The training, dev, and test data come from the same distribution.
    
- [ ] b) The training and test sets come from different distributions.
    
- [ ] c) The training data is randomly shuffled.
    
- [ ] d) All data is labeled.
    

**81. Why can having a training set from a different distribution than the dev and test sets affect the learning algorithm?**

- [ ] a) It will make your learning algorithm perform better.
    
- [ ] b) It will make your learning algorithm perform worse.
    
- [ ] c) No significant impact.
    
- [ ] d) It only affects small models.
    

**82. When is Transfer learning a useful technique?**

- [ ] a) When you have a large amount of data for the target task.
    
- [ ] b) When you have little data for the target task but a lot of data for the source task.
    
- [ ] c) When the source task and target task are completely different.
    
- [ ] d) When you want to train the model from scratch.
    

**83. What is Multi-task learning?**

- [ ] a) A version of learning from multiple different tasks simultaneously.
    
- [ ] b) A technique only used in natural language processing.
    
- [ ] c) A technique that helps improve performance when there is little data.
    
- [ ] d) A method to reduce computational cost.
    

**84. What is true about multi-task learning compared to transfer learning?**

- [ ] a) Transfer learning is used more often than multi-task learning today.
    
- [ ] b) Multi-task learning is always better.
    
- [ ] c) Transfer learning is only for small networks.
    
- [ ] d) Multi-task learning is only for computer vision.
    

**85. What is end-to-end deep learning?**

- [ ] a) A technique that replaces multiple processing stages with a single neural network.
    
- [ ] b) A technique that requires manual feature engineering.
    
- [ ] c) A technique that only works with a small amount of data.
    
- [ ] d) A technique that requires many intermediate steps.
    

**86. What is the advantage of end-to-end deep learning?**

- [ ] a) It needs less data.
    
- [ ] b) The data "speaks for itself" and there is less need for manual component design.
    
- [ ] c) It excludes useful manually designed components.
    
- [ ] d) It is more complex to implement.
    

**87. What is the disadvantage of end-to-end deep learning?**

- [ ] a) It is always more efficient.
    
- [ ] b) It may require a large amount of data and excludes potentially useful manually designed components.
    
- [ ] c) It simplifies the workflow.
    
- [ ] d) The data can "speak" more easily.
    

**88. When deciding whether to use end-to-end deep learning or other methods, what should be considered?**

- [ ] a) Only the complexity of the problem.
    
- [ ] b) Only the availability of data.
    
- [ ] c) The complexity of the problem and the availability of data.
    
- [ ] d) Nothing needs to be considered.
    

**89. How are neural network weights initialized in Random Initialization to avoid symmetry?**

- [ ] a) All to 0.
    
- [ ] b) Randomly with large values.
    
- [ ] c) Randomly with small values.
    
- [ ] d) With constants greater than 0.01.
    

**90. For a deep neural network, how do you ensure that each hyperparameter has a clear and understandable effect?**

- [ ] a) By tuning them randomly.
    
- [ ] b) By defining a specific set of hyperparameters to be tuned.
    
- [ ] c) By ensuring each hyperparameter has a clear and understandable function (orthogonalization).
    
- [ ] d) By only focusing on hyperparameters related to the optimization algorithm.
    

**91. Why is a machine learning strategy important?**

- [ ] a) To waste time and effort.
    
- [ ] b) To identify the most promising ideas and accelerate the building and deployment of deep learning products.
    
- [ ] c) To only use slow strategies.
    
- [ ] d) To maintain traditional methods.
    

**92. What is defining a single-number evaluation metric for your team to optimize?**

- [ ] a) It's a trade-off between precision and recall.
    
- [ ] b) It's a better and faster way to establish a single-number evaluation metric for your project before starting.
    
- [ ] c) It's a confusion matrix.
    
- [ ] d) It's a strategy to identify key priorities.
    

**93. How large should the dev and test sets be?**

- [ ] a) 100 examples are sufficient.
    
- [ ] b) The dev set should be large enough to detect differences between the algorithms you are trying. A dev set size of 1,000 to 10,000 examples is common.
    
- [ ] c) The test set should always be smaller than the dev set.
    
- [ ] d) The size is not important.
    

**94. In modern deep learning, is the traditional 70/30 or 60/20/20 data split still appropriate?**

- [ ] a) Yes, always.
    
- [ ] b) No, because dataset sizes are much larger.
    
- [ ] c) Only for small datasets.
    
- [ ] d) Only for linear models.
    

**95. What does the difference between the training error and the dev error tell us?**

- [ ] a) The Bayes error.
    
- [ ] b) The amount of avoidable bias.
    
- [ ] c) The amount of variance.
    
- [ ] d) The overall accuracy.
    

**96. When did comparing to human-level performance become more common?**

- [ ] a) When machine learning was still trying to catch up with humans.
    
- [ ] b) When machines had already surpassed humans in certain tasks.
    
- [ ] c) When there was no data to train the model.
    
- [ ] d) When the model's accuracy was perfect.
    

**97. What problem can training a larger model help solve in reducing bias and variance?**

- [ ] a) Reduce training error and reduce variance.
    
- [ ] b) Reduce training error.
    
- [ ] c) Reduce dev error.
    
- [ ] d) Reduce bias and reduce variance.
    

**98. What is a way to reduce training error in deep learning?**

- [ ] a) Use less data.
    
- [ ] b) Train a larger model or use neural network architecture/hyperparameter search.
    
- [ ] c) Apply regularization.
    
- [ ] d) Reduce training time.
    

**99. What is a way to reduce dev error in deep learning?**

- [ ] a) Train a smaller model.
    
- [ ] b) Add more data and apply regularization.
    
- [ ] c) Only search for hyperparameters.
    
- [ ] d) Reduce the model's complexity.
    

**100. When does machine learning outperform humans in natural perception tasks like speech recognition, computer vision, and natural language processing?**

- [ ] a) Always.
    
- [ ] b) When there is a large amount of data.
    
- [ ] c) This is difficult, but machine learning outperforms humans in structured data tasks.
    
- [ ] d) Never.
    

### **III. Recurrent Neural Networks (RNNs)**

**101. What is the limitation of standard neural networks in processing sequences of varying lengths?**

- [ ] a) They cannot share features learned across text positions.
    
- [ ] b) They can only handle fixed-length inputs.
    
- [ ] c) They cannot use backpropagation.
    
- [ ] d) They cannot capture information from previous time steps.
    

**102. How do RNNs address the limitations of standard neural networks in processing sequences of varying lengths?**

- [ ] a) By using a recurrent structure.
    
- [ ] b) By only using past information.
    
- [ ] c) By ignoring previous activations.
    
- [ ] d) By only processing the current input.
    

**103. What does Backpropagation Through Time (BPTT) require?**

- [ ] a) Only maintaining hidden states for the first time step.
    
- [ ] b) Maintaining hidden states for each time step during the forward pass.
    
- [ ] c) Ignoring the problems of vanishing or exploding gradients.
    
- [ ] d) Only using the basic RNN architecture.
    

**104. What are vanishing and exploding gradients a problem for in training RNNs?**

- [ ] a) Insignificant.
    
- [ ] b) May require additional techniques such as gradient clipping or more advanced RNN architectures (e.g., LSTM or GRU).
    
- [ ] c) Do not affect model performance.
    
- [ ] d) Only occur in forward propagation.
    

**105. What specific purposes do different RNN architectures serve?**

- [ ] a) Only machine translation.
    
- [ ] b) One-to-one, one-to-many, many-to-one, and many-to-many.
    
- [ ] c) Only music generation.
    
- [ ] d) None of the above.
    

**106. What does a Language model do?**

- [ ] a) Only predicts the next word in a sequence.
    
- [ ] b) Predicts the probability of a sequence of words and is crucial in tasks like speech recognition and machine translation.
    
- [ ] c) Only encodes text.
    
- [ ] d) Only generates random text.
    

**107. What does training a language model involve?**

- [ ] a) Only mapping words to indices.
    
- [ ] b) Tokenizing a text corpus, mapping words to vectors or indices, and the RNN predicting the next word.
    
- [ ] c) Only predicting the next word from left to right.
    
- [ ] d) Only using a cost function to measure the difference during training.
    

**108. During the sampling of a new sequence, how does the language model perform?**

- [ ] a) Always generates the same sequence.
    
- [ ] b) Samples the first word, passes it to the next steps, and repeats until the sequence is complete.
    
- [ ] c) Only uses the learned keywords.
    
- [ ] d) Ignores unknown word tokens.
    

**109. What training challenges do powerful models like GRUs and LSTMs address?**

- [ ] a) Vanishing gradients.
    
- [ ] b) Exploding gradients.
    
- [ ] c) Both a and b.
    
- [ ] d) Only Word-level models.
    

**110. In training deep neural networks, what does the vanishing gradient problem hinder?**

- [ ] a) Forward propagation.
    
- [ ] b) Backpropagation, especially in RNNs where forward propagation is from left to right and backpropagation is from right to left.
    
- [ ] c) Computational power.
    
- [ ] d) The model's ability to capture long-range dependencies.
    

**111. How do advanced RNN models like GRUs and LSTMs address the vanishing gradient problem?**

- [ ] a) By using new activation functions.
    
- [ ] b) By allowing the capture of long-range dependencies.
    
- [ ] c) By reducing the number of layers.
    
- [ ] d) By speeding up the training.
    

**112. In which NLP tasks have word embeddings enabled significant improvements?**

- [ ] a) Only text classification.
    
- [ ] b) Language translation, sentiment analysis, and text classification.
    
- [ ] c) Only speech recognition.
    
- [ ] d) Only tasks requiring one-hot encoding.
    

**113. What is the benefit of using word embeddings for transfer learning?**

- [ ] a) It always requires a larger dataset.
    
- [ ] b) Knowledge learned from a larger dataset can be applied to a smaller, related task.
    
- [ ] c) It can only represent words with one-dimensional feature vectors.
    
- [ ] d) It is less useful for language modeling and machine translation when there is a large dataset.
    

**114. What is the Word2Vec algorithm?**

- [ ] a) A complex and inefficient algorithm for learning types of word embeddings.
    
- [ ] b) A simpler and more efficient algorithm for learning these types of word embeddings.
    
- [ ] c) An algorithm only for word classification.
    
- [ ] d) An algorithm that only uses the skip-gram model.
    

**115. What is the goal of the skip-gram model?**

- [ ] a) To predict a context word based on a target word.
    
- [ ] b) To predict a target word in a window by choosing a context word.
    
- [ ] c) To only learn bad word embeddings.
    
- [ ] d) To calculate the negative log likelihood.
    

**116. Where does the computational speed problem in skip-gram with softmax arise from?**

- [ ] a) The need to compute a sum over the entire vocabulary during probability evaluation.
    
- [ ] b) Only from the size of the context window.
    
- [ ] c) Only from the use of one-hot encoding.
    
- [ ] d) From using too few parameters.
    

**117. What is the solution to the computational speed problem in skip-gram with softmax?**

- [ ] a) Using a hierarchical softmax classifier.
    
- [ ] b) Reducing the size of the vocabulary.
    
- [ ] c) Increasing the size of the context window.
    
- [ ] d) Only using the forward propagation algorithm.
    

**118. What do RNNs do with sequence data?**

- [ ] a) Ignore it.
    
- [ ] b) Maintain hidden states to capture information across time steps.
    
- [ ] c) Only process the input.
    
- [ ] d) Only use a single hidden layer.
    

**119. What is the effect of Backpropagation Through Time in RNNs?**

- [ ] a) It only makes the model learn slower.
    
- [ ] b) It trains RNNs by unrolling them through time.
    
- [ ] c) It is not related to parameter updates.
    
- [x] d) It cannot solve the vanishing gradients problem.
    

**120. What mechanism does a GRU use to mitigate the vanishing gradients problem in RNNs?**

- [ ] a) Gating mechanisms.
    
- [ ] b) Increasing the number of layers.
    
- [ ] c) Reducing the number of parameters.
    
- [ ] d) Only using a linear activation function.
    

**121. What does an LSTM incorporate to capture long-range dependencies?**

- [ ] a) Memory cells.
    
- [ ] b) Convolutional layers.
    
- [ ] c) Fully connected layers.
    
- [ ] d) Feed-forward only layers.
    

**122. In which direction do Bi-directional RNNs process a sequence?**

- [ ] a) Only one direction.
    
- [ ] b) Both directions.
    
- [ ] c) Randomly.
    
- [ ] d) From end to beginning.
    

**123. Why do deep RNNs stack multiple layers?**

- [ ] a) To reduce model complexity.
    
- [ ] b) To learn complex patterns.
    
- [ ] c) To reduce computational cost.
    
- [ ] d) To only process non-sequential data.
    

**124. What limitations of traditional sequence-to-sequence models motivated Transformers?**

- [ ] a) Inability to process data in parallel.
    
- [ ] b) Inability to capture long-range dependencies in the input sequence due to the vanishing gradient problem.
    
- [ ] c) Being limited only by vocabulary size.
    
- [ ] d) Inability to use a self-attention mechanism.
    

**125. Why is the Transformer architecture popular in NLP?**

- [ ] a) It is a simple architecture.
    
- [ ] b) It allows parallel processing of the entire sequence.
    
- [ ] c) It only processes one word or token at a time.
    
- [ ] d) It relies only on RNNs.
    

**126. What is the main innovation of the Transformer architecture?**

- [ ] a) The use of RNNs.
    
- [ ] b) The combination of attention-based representations and CNN-style processing.
    
- [ ] c) Only using fully connected layers.
    
- [ ] d) Only solving the vanishing gradient problem.
    

**127. How does the self-attention mechanism allow for parallel computation of representations?**

- [ ] a) By sequentially processing each word.
    
- [ ] b) By using matrix multiplication to calculate attention values.
    
- [ ] c) By only focusing on context words.
    
- [ ] d) By ignoring irrelevant words.
    

**128. The Transformer model has an encoder and a decoder block, each with multiple layers. What mechanism does the encoder use to create a contextual embedding for each word?**

- [ ] a) Only feed-forward networks.
    
- [ ] b) Self-attention and feed-forward networks.
    
- [ ] c) Recurrent networks.
    
- [ ] d) Only positional encoding.
    

**129. Overall, how does the Transformer excel in NLP?**

- [ ] a) By surpassing RNNs and CNNs due to its parallelization capability and handling of long-range dependencies.
    
- [ ] b) Only by using self-attention.
    
- [ ] c) By reducing model complexity.
    
- [ ] d) By eliminating the encoder-decoder layers.
    

**130. Beam search is a decoding algorithm used in machine translation and other sequence generation tasks for what purpose?**

- [ ] a) To simplify the search.
    
- [ ] b) To expand multiple possible sequences simultaneously, narrowing the search space.
    
- [ ] c) To only find the single optimal sequence.
    
- [ ] d) To always choose the word with the highest probability.
    

**131. Why is beam search used instead of exhaustive enumeration to find the most likely sentence in machine translation?**

- [ ] a) It always finds the optimal translation.
    
- [ ] b) The exponentially large space of all possible sentences in a language.
    
- [ ] c) Greedy search selects the most likely word at each step.
    
- [ ] d) Both b and c.
    

**132. What is the first step in selecting the most likely sentence with Beam search?**

- [ ] a) Only considering the second word.
    
- [ ] b) Selecting the first word of the English translation and using a network segment with an encoder and decoder.
    
- [ ] c) Selecting the third word.
    
- [ ] d) Ignoring the first word.
    

**133. If the beam width is set to 1, what does beam search become?**

- [ ] a) A complete search.
    
- [ ] b) A greedy search.
    
- [ ] c) An optimal search.
    
- [ ] d) A random search.
    

**134. How does the BLEU score evaluate the quality of machine translation?**

- [ ] a) By comparing n-grams.
    
- [ ] b) By comparing single words.
    
- [ ] c) By only evaluating grammar.
    
- [ ] d) By evaluating meaning.
    

**135. For speech recognition, what can end-to-end deep learning models do?**

- [ ] a) Only accept spectrograms as input.
    
- [ ] b) Can input raw audio and directly output the transcript.
    
- [ ] c) Require a separate trigger word detection system.
    
- [ ] d) Cannot use an attention model.
    

**136. With what type of dataset can a trigger word detection system be built?**

- [ ] a) A large dataset.
    
- [ ] b) A smaller dataset than required for complete speech recognition.
    
- [ ] c) A dataset with only audio.
    
- [ ] d) A dataset with only text.
    

**137. What are hyperparameters in deep learning?**

- [ ] a) Parameters learned during training.
    
- [x] b) Parameters that are not learned during training but affect the model's performance.
    
- [ ] c) Only parameters related to the loss function.
    
- [ ] d) Only parameters related to the input.
    

**138. Why can tuning hyperparameters lead to a large improvement in model performance?**

- [ ] a) Because they are learned automatically.
    
- [ ] b) Because they directly affect the model's position on the leaderboard.
    
- [ ] c) Because they are only related to the model architecture.
    
- [ ] d) Because they are always fixed values.
    

**139. What is one of the most important hyperparameters?**

- [ ] a) The number of hidden layers.
    
- [ ] b) The learning rate.
    
- [ ] c) The mini-batch size.
    
- [ ] d) Momentum.
    

**140. How is the frequency of a specific hyperparameter explored?**

- [ ] a) By sampling points in a grid.
    
- [ ] b) By randomly exploring its values.
    
- [ ] c) By systematic search.
    
- [ ] d) Both a and b.
    

**141. In image classification, an input RGB image has a size of 39x39x3. The first layer uses 3 filters of 3x3 with a stride of 1 and no padding. What is the output size?**

- [ ] a) 37 x 37 x 10.
    
- [ ] b) 39 x 39 x 3.
    
- [ ] c) 17 x 17 x 20.
    
- [ ] d) 7 x 7 x 40.
    

**142. What are the two main changes in the MobileNet v2 architecture compared to previous architectures?**

- [ ] a) Adding a residual connection and an expansion layer before the depthwise convolution.
    
- [ ] b) Removing the pooling layers.
    
- [ ] c) Reducing the overall number of parameters.
    
- [ ] d) Increasing the filter size.
    

**143. What operation does the bottleneck block in MobileNet v2 use?**

- [ ] a) Only depthwise convolution.
    
- [ ] b) An expansion operation to increase the representation size within the bottleneck block.
    
- [ ] c) A reduction operation to decrease memory requirements.
    
- [ ] d) Pointwise convolution.
    

**144. EfficientNet is a convolutional neural network architecture designed for what?**

- [ ] a) Only to reduce computational cost.
    
- [ ] b) To achieve state-of-the-art performance on image classification tasks while minimizing the number of parameters and computational resources required.
    
- [ ] c) To increase model complexity.
    
- [ ] d) To work only on mobile devices.
    

**145. What method does EfficientNet use to scale the neural network?**

- [ ] a) Only changing the depth.
    
- [ ] b) Compound scaling, which simultaneously adjusts the image resolution, depth, and width of the neural network.
    
- [ ] c) Only changing the width.
    
- [ ] d) Only changing the filter size.
    

**146. Transfer learning is a technique in computer vision that allows for what?**

- [ ] a) Slower progress.
    
- [ ] b) Faster progress by using pre-trained neural network models as a starting point.
    
- [ ] c) Always requiring training the model from scratch.
    
- [ ] d) Only working with small datasets.
    

**147. Which pre-trained models are mentioned as being freely available and trained on large datasets like ImageNet, MS COCO, and Pascal?**

- [ ] a) LeNet, VGG.
    
- [ ] b) ResNet, AlexNet.
    
- [ ] c) None of them are available.
    
- [ ] d) All are available.
    

**148. What is usually done to the early layers of a pre-trained model in transfer learning?**

- [ ] a) Fine-tuned for the specific problem.
    
- [ ] b) Frozen.
    
- [ ] c) Removed.
    
- [ ] d) Replaced.
    

**149. What is usually done to the later layers of a pre-trained model in transfer learning?**

- [ ] a) Frozen.
    
- [ ] b) Fine-tuned for the specific problem.
    
- [ ] c) Removed.
    
- [ ] d) Replaced.
    

**150. What is the overall advantage of transfer learning?**

- [ ] a) Only saving time.
    
- [ ] b) A powerful technique that can save time and improve performance in computer vision applications.
    
- [ ] c) Only improving performance.
    
- [ ] d) No significant advantages.
    

Suppose you have $n_x$ input features per example. Recall that $X = [x^{(1)}\ x^{(2)}\ \ldots\ x^{(m)}]$. What is the dimension of the matrix $X$?
- [ ] A. (1, m)
    
- [ ] B. (m, 1)
    
- [ ] C. (m, $n_x$)
    
- [x] D. ($n_x$ , m)
    

Consider the following code snippet. How do you vectorize this?

```python
# a.shape = (3, 4)
# b.shape = (4, 1)
for i in range(3):
    for j in range(4):
        c[i][j] = a[i][j] + b[j]
```

- [x] A. $c = a + b^T$
    
- [ ] B. $c = a^T + b^T$
    
- [ ] C. $c = a + b$
    
- [ ] D. $c = a^T + b$
    
What does the analogy "Al is the new electricity" refer to? 
- [ ] Through the "smart grid", Al is delivering a new wave of electricity. 

- [x] Similar to electricity starting about 100 years ago, Al is transforming multiple industries. 

- [ ] Al is powering personal devices in our homes and offices, similar to electricity. 

- [ ] Al runs on computers and is thus powered by electricity, but it is letting computers do things not possible before.

Which of these are reasons for Deep Learning recently taking off? (Check the three options that apply.) 
- [ ] Neural Networks are a brand new field. 

- [x] Deep learning has resulted in significant improvements in important applications such as online advertising, speech recognition, and image recognition. 

- [x] We have access to a lot more computational power. 

- [x] We have access to a lot more data.

Recall the diagram of iterating over different ML ideas. Which of the stages shown in the diagram was improved with the use of a better GPU/CPU? 
- [ ] Some algorithms are specifically designed to run experiments faster. 

- [ ] Without better hardware, there is no way to train models faster. 
	
- [ ] With larger datasets, the iteration process is faster. 

- [x] Experiments finish faster, producing better ideas through increased iteration tempo.

- When building a neural network to predict housing price from features like size, the number of bedrooms, zip code, and wealth, it is necessary to come up with other features in between input and output like family size and school quality. True/False? 
- [x]  False
- [ ]  True

- Images for cat recognition is an example of "structured" data, because it is represented as a structured array in a computer. True/False? True False
- [x]  False
- [ ]  True

- A demographic dataset with statistics on different cities' population, GDP per capita, and economic growth is an example of "unstructured" data because it contains data coming from different sources. True/False? True False
- [x]  False
- [ ]  True

- RNNs (Recurrent Neural Networks) are good for data with a temporal component. True/False? True False
- [ ]  False
- [x]  True

Suppose the information given in the diagram is accurate. We can deduce that when using large training sets, for a model to keep improving as the amount of data for training grows, the size of the neural network must grow. True/False?
- [ ]  False
- [x]  True

Suppose you have a 10000 word vocabulary, and are learning 500-dimensional word  
embeddings. The word2vec model uses the following softmax function:  
  
$$
P(w_o | w_I) = \frac{\exp\left(v_{w_o}'^\top v_{w_I}\right)}{\sum_{w=1}^{W} \exp\left(v_{w}'^\top v_{w_I}\right)}
$$

  
Which of these statements are correct? Check all that apply.  
- [ ] A: θt and ${\mathbf{e}}_c$  are both 500 dimensional vectors.  
- [ ] B: θt and ${\mathbf{e}}_c$ are both 10000 dimensional vectors.  
- [x] C: θt and ${\mathbf{e}}_c$ are both trained with an optimization algorithm such as Adam or gradient descent.  
- [ ] D: After training, we should expect θt to be very close to ${\mathbf{e}}_c$ when t and c are the same word.

You have trained word embeddings using a text dataset of m1? words. You are considering using these word embeddings for a language task, for which you have a separate labeled dataset of m2? words. Keeping in mind that using word embeddings is a form of transfer learning, under which of these circumstances would you expect the word embeddings to be helpful?
- [x] m1>>m2
- [ ] m1<< m2

Suppose you are building a speech recognition system, which uses an RNN model to map from audio clip x to a text transcript y. Your algorithm uses beam search to try to find the value of y that maximizes $P(y∣x)$. On a dev set example, given an input audio clip, your algorithm outputs the transcript $\hat{y}$= "I'm building an A Eye system in Silly con Valley", whereas a human gives a much superior transcript $y^∗$= "I'm building an AI system in Silicon Valley".  
According to your model,  

$P(\hat{y} \mid x) = 1.09 \times 10^{-7}$

$P(y^* \mid x) = 7.21 \times 10^{-8}$

Would you expect increasing the beam width B to help correct this example?

- [x] No, because $P(y^* \mid x) < P(\hat{y} \mid x)$ indicates the error should be attributed to the RNN rather than to the search algorithm.

- [ ] No, because $P(y^* \mid x) < P(\hat{y} \mid x)$ indicates the error should be attributed to the search algorithm rather than to the RNN.

- [ ] Yes, because $P(y^* \mid x) < P(\hat{y} \mid x)$ indicates the error should be attributed to the RNN rather than to the search algorithm.

- [ ] Yes, because $P(y^* \mid x) < P(\hat{y} \mid x)$ indicates the error should be attributed to the search algorithm rather than to the RNN.

Attention(WQiQ,WKiK,WViV)

  
i here represents the computed attention weight matrix associated with the ith head (sequence)

$$Attention(W_i^QQ, W_i^KK, W_i^VV)$$
i here represents the computed attention weight matrix associated with the ith head (sequence)]
- [ ]  False
- [x]  True


Following is the architecture within a Transformer Network
What is NOT necessary for the Decoder's second block of Multi-Head Attention?
![[Pasted image 20250718224526.png]]
- [x] All of the below are necessary for the Decoder's second block.
- [ ] V
- [ ] Q
- [ ] K

Which of the following are common reasons for using open-source implementations of ConvNets (both the model and/or weights)? Check all that apply.  
- [ ] A: A model trained for one computer vision task can usually be used to perform data augmentation even for a different computer vision task.  
- [ ] B: It is a convenient way to get working an implementation of a complex ConvNet architecture.  
- [ ] C: The same techniques for winning computer vision competitions, such as using multiple crops at test time, are widely used in practical deployments (or production system deployments) of ConvNets.  
- [ ] D: Parameters trained for one computer vision task are often useful as pretraining for other computer vision tasks.

If you think ß (hyperparameter for momentum) is between on 0.9 and 0.99, which of the following is the recommended way to sample a value for beta?


- [ ] r = np.random.rand()  beta = r*0.09 + 0.9

- [x] r = np.random.rand()  beta = 1-10**(-r-1)

- [ ] r = np.random.rand()  beta = 1-10**(-r+1)

- [ ] r = np.random.rand()  beta = r*0.9 + 0.09






## FE
### Bài kiểm tra trắc nghiệm: Mạng Nơ-ron Nông và Sâu

**Chọn câu trả lời đúng nhất cho mỗi câu hỏi.**

#### Phần 1: Mạng Nơ-ron Nông (Shallow Neural Networks)

1. **Một mạng nơ-ron "nông" (shallow) được định nghĩa là mạng có:** a) Không có lớp ẩn nào. b) Một lớp ẩn. c) Hai lớp ẩn. d) Nhiều hơn hai lớp ẩn.
    
2. **Tại sao các lớp ẩn (hidden layers) lại được gọi là "ẩn"?** a) Vì chúng rất khó để lập trình. b) Vì các giá trị kích hoạt của chúng không được quan sát trực tiếp trong tập dữ liệu. c) Vì chúng thực hiện các phép tính bí mật. d) Vì chúng luôn sử dụng hàm kích hoạt Sigmoid.
    
3. **Tại sao việc sử dụng các hàm kích hoạt phi tuyến (non-linear) trong các lớp ẩn lại quan trọng?** a) Vì chúng giúp tính toán nhanh hơn. b) Vì nếu không có chúng, việc xếp chồng nhiều lớp cũng chỉ tương đương với một mô hình tuyến tính duy nhất. c) Vì chúng luôn cho ra kết quả trong khoảng [0, 1]. d) Vì chúng giúp giảm số lượng tham số.
    
4. **Hàm kích hoạt nào thường được coi là lựa chọn mặc định tốt nhất cho các lớp ẩn hiện nay?** a) Sigmoid b) Tanh c) ReLU (Rectified Linear Unit) d) Linear
    
5. **Hàm kích hoạt Tanh có ưu điểm gì so với Sigmoid trong các lớp ẩn?** a) Nó tính toán nhanh hơn. b) Nó cho ra giá trị trung bình của các kích hoạt gần 0, giúp việc học ở lớp sau dễ dàng hơn. c) Nó không bao giờ bị bão hòa. d) Nó chỉ hoạt động với số nguyên.
    
6. **Nếu đầu vào `z = -5`, đầu ra của hàm ReLU là bao nhiêu?** a) -5 b) 0 c) 1 d) 0.01
    
7. **Đạo hàm của hàm ReLU tại `z = 10` là bao nhiêu?** a) 0 b) 1 c) 10 d) Không xác định.
    
8. **Mục đích của việc khởi tạo trọng số ngẫu nhiên (Random Initialization) là gì?** a) Để làm cho mô hình chạy nhanh hơn. b) Để "phá vỡ tính đối xứng" (break symmetry), đảm bảo các nơ-ron trong cùng một lớp học các đặc trưng khác nhau. c) Để đảm bảo hàm chi phí luôn giảm. d) Để giảm số lượng tham số cần học.
    
9. **Điều gì sẽ xảy ra nếu tất cả các trọng số trong một mạng nơ-ron được khởi tạo bằng 0?** a) Mô hình sẽ hội tụ rất nhanh. b) Tất cả các nơ-ron trong cùng một lớp sẽ học cùng một đặc trưng, khiến mạng không thể học được gì hữu ích. c) Hàm chi phí sẽ ngay lập tức bằng 0. d) Mô hình sẽ hoạt động tốt hơn.
    
10. **Trong một mạng nơ-ron 2 lớp (1 lớp ẩn, 1 lớp đầu ra), `a[1]` đại diện cho cái gì?** a) Các đặc trưng đầu vào. b) Các kích hoạt (đầu ra) của lớp ẩn. c) Dự đoán cuối cùng của mạng. d) Các trọng số của lớp ẩn.
    
11. **Quá trình tính toán các đạo hàm `dW` và `db` được gọi là gì?** a) Lan truyền xuôi (Forward Propagation) b) Khởi tạo ngẫu nhiên (Random Initialization) c) Lan truyền ngược (Backpropagation) d) Vector hóa (Vectorization)
    
12. **Trong công thức `Z[1] = W[1]X + b[1]`, `X` đại diện cho cái gì?** a) Ma trận trọng số. b) Ma trận chứa tất cả các mẫu dữ liệu đầu vào. c) Vector độ lệch. d) Ma trận chứa các kích hoạt của lớp ẩn.
    
13. **Đâu là một biến thể của ReLU giúp giải quyết vấn đề "nơ-ron chết" (dying ReLU)?** a) Sigmoid b) Tanh c) Leaky ReLU d) Softmax
    
14. **Đạo hàm của hàm Sigmoid `σ(z)` là gì?** a) `σ(z)` b) `1 - σ(z)²` c) `σ(z) * (1 - σ(z))` d) `1`
    
15. **Một mạng nơ-ron có lớp đầu vào 10 nơ-ron, lớp ẩn có 5 nơ-ron và lớp đầu ra có 1 nơ-ron. Ma trận trọng số `W[1]` sẽ có kích thước là bao nhiêu?** a) (10, 5) b) (5, 10) c) (5, 1) d) (1, 5)
    

#### Phần 2: Mạng Nơ-ron Sâu (Deep Neural Networks)

16. **Một mạng nơ-ron được coi là "sâu" (deep) khi nào?** a) Khi nó có nhiều hơn 1000 nơ-ron. b) Khi nó có nhiều hơn một lớp ẩn. c) Khi nó sử dụng hàm kích hoạt ReLU. d) Khi nó được huấn luyện trên một tập dữ liệu lớn.
    
17. **Lợi ích chính của việc sử dụng các kiến trúc sâu là gì?** a) Chúng luôn chạy nhanh hơn các mạng nông. b) Chúng có ít siêu tham số hơn. c) Chúng có khả năng học các biểu diễn đặc trưng theo cấp bậc (hierarchical features), từ đơn giản đến phức tạp. d) Chúng không bao giờ bị overfitting.
    
18. **Trong một mạng nơ-ron sâu `L` lớp, `a[L]` đại diện cho cái gì?** a) Kích hoạt của lớp ẩn đầu tiên. b) Kích hoạt của lớp ẩn cuối cùng. c) Dự đoán cuối cùng của mạng (`ŷ`). d) Dữ liệu đầu vào `X`.
    
19. **Trong lan truyền xuôi của một mạng sâu, đầu vào của lớp `l` là gì?** a) Dữ liệu gốc `X`. b) Kích hoạt của lớp `l+1` (`a[l+1]`). c) Kích hoạt của lớp `l-1` (`a[l-1]`). d) Trọng số của lớp `l` (`W[l]`).
    
20. **Đâu là một ví dụ về "siêu tham số" (hyperparameter)?** a) Trọng số `W`. b) Độ lệch `b`. c) Tốc độ học `α`. d) Kích hoạt `a`.
    
21. **Sự khác biệt chính giữa "tham số" (parameters) và "siêu tham số" (hyperparameters) là gì?** a) Tham số được học từ dữ liệu, siêu tham số được người dùng thiết lập trước. b) Siêu tham số được học từ dữ liệu, tham số được người dùng thiết lập trước. c) Không có sự khác biệt. d) Tham số chỉ có trong mạng nông, siêu tham số chỉ có trong mạng sâu.
    
22. **Trong một mạng có `L=4` lớp, ma trận trọng số `W[3]` sẽ kết nối giữa hai lớp nào?** a) Lớp 2 và lớp 3. b) Lớp 3 và lớp 4. c) Lớp 1 và lớp 2. d) Lớp 3 và lớp đầu vào.
    
23. **Tại sao việc kiểm tra kích thước của các ma trận (`W`, `b`, `Z`, `A`) lại là một công cụ gỡ lỗi hữu ích?** a) Vì nó giúp mô hình hội tụ nhanh hơn. b) Vì nó đảm bảo các phép toán nhân ma trận được thực hiện đúng cách và giúp phát hiện lỗi trong quá trình lập trình. c) Vì nó giúp giảm overfitting. d) Vì nó giúp chọn đúng hàm kích hoạt.
    
24. **Trong bài toán nhận dạng khuôn mặt, lớp đầu tiên của một mạng nơ-ron sâu có khả năng học được đặc trưng gì?** a) Các khuôn mặt hoàn chỉnh. b) Các bộ phận như mắt, mũi, miệng. c) Các cạnh và góc đơn giản. d) Tên của người trong ảnh.
    
25. **"Cache" trong quá trình lan truyền xuôi được sử dụng để làm gì?** a) Để lưu trữ dự đoán cuối cùng. b) Để tăng tốc độ lan truyền xuôi. c) Để lưu trữ các giá trị trung gian (như `Z`) nhằm tái sử dụng trong quá trình lan truyền ngược. d) Để lưu trữ các siêu tham số.
    
26. **Câu khẳng định nào sau đây là đúng về mối quan hệ giữa mạng nơ-ron và bộ não?** a) Mạng nơ-ron là một bản sao chính xác của bộ não. b) Các nhà khoa học thần kinh đã chứng minh bộ não sử dụng thuật toán lan truyền ngược. c) Mạng nơ-ron chỉ được lấy cảm hứng một cách lỏng lẻo từ bộ não và sự tương đồng này không hoàn toàn chính xác. d) Mạng nơ-ron hoạt động hiệu quả hơn bộ não trong mọi tác vụ.
    
27. **Một mạng nơ-ron có `n[l-1]` nơ-ron ở lớp trước và `n[l]` nơ-ron ở lớp hiện tại. Kích thước của ma trận trọng số `W[l]` là:** a) (`n[l-1]`, `n[l]`) b) (`n[l]`, `n[l-1]`) c) (`n[l]`, 1) d) (`n[l-1]`, 1)
    
28. **Nếu bạn đang xây dựng một mạng nơ-ron và không chắc chắn về số lớp ẩn, một chiến lược tốt để bắt đầu là gì?** a) Bắt đầu với một mạng rất sâu (ví dụ: 50 lớp). b) Bắt đầu với một mô hình đơn giản (như Hồi quy Logistic hoặc mạng 1 lớp ẩn) và tăng dần độ sâu nếu cần. c) Chọn một số ngẫu nhiên từ 1 đến 100. d) Luôn sử dụng 5 lớp ẩn.
    
29. **Trong lan truyền ngược của một mạng sâu, `da[l-1]` được tính toán dựa trên giá trị nào?** a) `da[l-2]` b) `dz[l]` c) `a[l]` d) `W[l-1]`
    
30. **Lý thuyết mạch (Circuit theory) gợi ý rằng mạng sâu có thể hiệu quả hơn mạng nông vì:** a) Mạng sâu có thể tính toán một số hàm phức tạp với số lượng nơ-ron ít hơn theo cấp số mũ so với mạng nông. b) Mạng sâu luôn cần nhiều dữ liệu hơn. c) Mạng sâu dễ lập trình hơn. d) Mạng sâu không cần hàm kích hoạt.
    

#### Phần 3: Câu hỏi lý thuyết bổ sung

31. **Trong một mạng nơ-ron, "activation" (kích hoạt) của một nơ-ron là gì?** a) Giá trị đầu vào của nơ-ron đó. b) Giá trị đầu ra của nơ-ron đó sau khi đi qua hàm kích hoạt. c) Trọng số kết nối đến nơ-ron đó. d) Độ lệch của nơ-ron đó.
    
32. **Quá trình lặp lại việc thực hiện lan truyền xuôi và lan truyền ngược được gọi là gì?** a) Một epoch. b) Một bước của Gradient Descent. c) Một lần dự đoán. d) Khởi tạo.
    
33. **Đâu là một nhược điểm của hàm Sigmoid và Tanh?** a) Chúng không phải là hàm phi tuyến. b) Chúng có thể gặp vấn đề "gradient biến mất" (vanishing gradient) khi đầu vào quá lớn hoặc quá nhỏ. c) Chúng chỉ có thể được sử dụng ở lớp đầu ra. d) Chúng rất khó để tính đạo hàm.
    
34. **Tại sao ReLU lại giúp giảm bớt vấn đề "gradient biến mất"?** a) Vì đạo hàm của nó luôn bằng 1 đối với các đầu vào dương, giúp gradient không bị suy giảm khi lan truyền ngược. b) Vì nó là một hàm tuyến tính. c) Vì nó giới hạn đầu ra trong khoảng [0, 1]. d) Vì nó có đạo hàm bằng 0 đối với các đầu vào âm.
    
35. **Ký hiệu `n[0]` thường dùng để chỉ điều gì?** a) Số nơ-ron ở lớp đầu ra. b) Số nơ-ron ở lớp ẩn đầu tiên. c) Số đặc trưng đầu vào (`nₓ`). d) Luôn bằng 0.
    
36. **Trong các công thức lan truyền ngược, `g'(Z)` đại diện cho cái gì?** a) Giá trị của hàm kích hoạt. b) Đạo hàm của hàm kích hoạt theo `Z`. c) Đầu vào của hàm kích hoạt. d) Một hằng số.
    
37. **Nếu bạn tăng số lượng lớp ẩn trong một mạng nơ-ron, điều gì có khả năng xảy ra?** a) Khả năng của mạng để học các hàm phức tạp sẽ tăng lên. b) Nguy cơ overfitting có thể tăng lên. c) Thời gian huấn luyện sẽ tăng lên. d) Tất cả các câu trên đều đúng.
    
38. **"Forward propagation" và "Inference" (suy luận) có liên quan như thế nào?** a) Chúng hoàn toàn không liên quan. b) Inference chính là quá trình thực hiện forward propagation trên dữ liệu mới để đưa ra dự đoán (sau khi mô hình đã được huấn luyện). c) Forward propagation là một phần của inference, nhưng không phải ngược lại. d) Inference là tên gọi khác của backpropagation.
    
39. **Việc chọn kiến trúc mạng (số lớp, số nơ-ron mỗi lớp) thuộc về quá trình nào?** a) Tối ưu hóa tham số. b) Tinh chỉnh siêu tham số. c) Lan truyền ngược. d) Xử lý dữ liệu.
    
40. **Trong một mạng nơ-ron được huấn luyện tốt, các trọng số `W` thường có giá trị như thế nào?** a) Rất lớn. b) Rất nhỏ, gần 0. c) Các giá trị được phân bổ hợp lý, không quá lớn cũng không quá nhỏ. d) Luôn bằng 1.
    
41. **Một mạng nơ-ron có 3 lớp ẩn sẽ được gọi là mạng mấy lớp?** a) 3 lớp. b) 4 lớp (3 ẩn + 1 đầu ra). c) 5 lớp (1 đầu vào + 3 ẩn + 1 đầu ra). d) Tùy thuộc vào cách đếm.
    
42. **Mục đích của vector `b` (bias) trong một nơ-ron là gì?** a) Để làm cho phép tính phức tạp hơn. b) Cung cấp thêm một mức độ linh hoạt, cho phép đường biên quyết định dịch chuyển lên/xuống. c) Để chuẩn hóa đầu vào. d) Để ngăn chặn overfitting.
    
43. **Đâu không phải là một hàm kích hoạt?** a) ReLU b) Tanh c) Sigmoid d) Gradient Descent
    
44. **Quá trình tính toán `Z = W*A + b` là một phép biến đổi:** a) Tuyến tính. b) Phi tuyến. c) Ngẫu nhiên. d) Logarit.
    
45. **Trong công thức `db[l] = (1/m) * np.sum(dZ[l], axis=1, keepdims=True)`, `np.sum` được sử dụng để làm gì?** a) Tính tổng các sai số trên tất cả các mẫu trong mini-batch để có được đạo hàm của bias. b) Tính tổng các trọng số. c) Tính tổng các kích hoạt. d) Chuẩn hóa dữ liệu.
    
46. **Sự khác biệt chính giữa một mạng nơ-ron nông và một mạng sâu nằm ở:** a) Số lượng tham số. b) Tốc độ huấn luyện. c) Độ sâu, tức là số lượng lớp ẩn. d) Loại dữ liệu chúng có thể xử lý.
    
47. **Nếu bạn có một mạng nơ-ron rất sâu, bạn có thể gặp phải vấn đề gì trong quá trình huấn luyện?** a) Gradient biến mất hoặc bùng nổ (Vanishing/Exploding Gradients). b) Overfitting. c) Thời gian huấn luyện lâu. d) Tất cả các câu trên.
    
48. **Việc vector hóa giúp tăng tốc độ tính toán chủ yếu là do:** a) Python vốn dĩ rất nhanh. b) Các thư viện như NumPy sử dụng các đoạn mã C/Fortran được tối ưu hóa cao và tận dụng tính toán song song của phần cứng. c) Nó làm giảm số lượng phép tính cần thực hiện. d) Nó làm giảm độ phức tạp của thuật toán.
    
49. **Trong một mạng nơ-ron, thông tin được truyền đi như thế nào?** a) Từ lớp đầu ra đến lớp đầu vào. b) Giữa các nơ-ron trong cùng một lớp. c) Từ lớp này sang lớp tiếp theo, theo một chiều từ đầu vào đến đầu ra. d) Một cách ngẫu nhiên.
    
50. **Đâu là bước đầu tiên trong quá trình lan truyền ngược (backpropagation)?** a) Cập nhật trọng số của lớp đầu tiên. b) Tính toán sai số giữa dự đoán và nhãn thật ở lớp đầu ra. c) Tính toán kích hoạt của lớp ẩn đầu tiên. d) Khởi tạo lại tất cả các trọng số.
    

### **Đáp án**

<details> <summary>Nhấn vào đây để xem đáp án</summary>

1. b | 2. b | 3. b | 4. c | 5. b
    
2. b | 7. b | 8. b | 9. b | 10. b
    
3. c | 12. b | 13. c | 14. c | 15. b
    
4. b | 17. c | 18. c | 19. c | 20. c
    
5. a | 22. a | 23. b | 24. c | 25. c
    
6. c | 27. b | 28. b | 29. b | 30. a
    
7. b | 32. b | 33. b | 34. a | 35. c
    
8. b | 37. d | 38. b | 39. b | 40. c
    
9. b | 42. b | 43. d | 44. a | 45. a
    
10. c | 47. d | 48. b | 49. c | 50. b
    

</details>


### Bài kiểm tra trắc nghiệm: Các khía cạnh thực tế của Học sâu

**Chọn câu trả lời đúng nhất cho mỗi câu hỏi.**

#### Phần 1: Thiết lập Ứng dụng Học máy (Train/Dev/Test, Bias/Variance)

1. **Mục đích chính của tập phát triển (dev set) là gì?** a) Để huấn luyện mô hình. b) Để đưa ra đánh giá cuối cùng, không thiên vị về hiệu suất của mô hình. c) Để tinh chỉnh các siêu tham số và đánh giá các ý tưởng khác nhau. d) Không có mục đích cụ thể.
    
2. **Trong thời đại Dữ liệu lớn (Big Data), tỷ lệ phân chia Train/Dev/Test nào sau đây là hợp lý nhất cho một tập dữ liệu có 1,000,000 mẫu?** a) 60% / 20% / 20% b) 70% / 30% / 0% c) 98% / 1% / 1% d) 34% / 33% / 33%
    
3. **"High Bias" (Độ chệch cao) có nghĩa là gì?** a) Mô hình bị overfitting. b) Mô hình quá phức tạp. c) Mô hình quá đơn giản và không khớp tốt với cả tập huấn luyện (underfitting). d) Mô hình hoạt động tốt trên tập huấn luyện nhưng kém trên tập dev.
    
4. **Nếu lỗi trên tập huấn luyện (Train error) là 1% và lỗi trên tập phát triển (Dev error) là 11%, mô hình của bạn đang gặp vấn đề gì?** a) High Bias (Độ chệch cao) b) High Variance (Phương sai cao) c) Cả High Bias và High Variance d) Low Bias và Low Variance
    
5. **Nếu Train error là 14% và Dev error là 15% (giả sử lỗi tối ưu là ~0%), mô hình của bạn đang gặp vấn đề gì?** a) High Bias (Độ chệch cao) b) High Variance (Phương sai cao) c) Cả High Bias và High Variance d) Low Bias và Low Variance
    
6. **Để giải quyết vấn đề High Variance, bạn nên thử phương pháp nào đầu tiên?** a) Huấn luyện một mạng lớn hơn. b) Thêm dữ liệu hoặc sử dụng điều chuẩn hóa (regularization). c) Huấn luyện lâu hơn. d) Thử một thuật toán tối ưu hóa khác.
    
7. **Để giải quyết vấn đề High Bias, bạn nên thử phương pháp nào?** a) Thêm dữ liệu. b) Sử dụng Dropout. c) Huấn luyện một mạng lớn hơn hoặc huấn luyện lâu hơn. d) Sử dụng L2 regularization.
    
8. **Tại sao tập dev và tập test nên đến từ cùng một phân phối dữ liệu?** a) Để quá trình huấn luyện nhanh hơn. b) Để đảm bảo rằng việc tối ưu hóa trên tập dev sẽ dẫn đến hiệu suất tốt trên dữ liệu thực tế mà tập test đại diện. c) Đó chỉ là một quy ước không bắt buộc. d) Để giảm bộ nhớ sử dụng.
    
9. **Quy trình làm việc trong học máy có tính chất gì?** a) Tuyến tính, làm một lần là xong. b) Lặp đi lặp lại (iterative): Lên ý tưởng -> Viết code -> Thử nghiệm -> Tinh chỉnh. c) Hoàn toàn ngẫu nhiên. d) Chỉ phụ thuộc vào việc viết code.
    
10. **Trong "công thức" cơ bản cho học máy, bước đầu tiên sau khi huấn luyện mô hình là gì?** a) Kiểm tra xem mô hình có bị High Variance không. b) Triển khai mô hình ngay lập tức. c) Kiểm tra xem mô hình có bị High Bias không. d) Thu thập thêm dữ liệu.
    

#### Phần 2: Điều chuẩn hóa (Regularization)

11. **Mục đích chính của các kỹ thuật điều chuẩn hóa (regularization) là gì?** a) Để giải quyết vấn đề High Bias (underfitting). b) Để tăng tốc độ huấn luyện. c) Để giải quyết vấn đề High Variance (overfitting). d) Để giảm số lượng lớp ẩn.
    
12. **L2 Regularization hoạt động bằng cách nào?** a) Thêm một thành phần vào hàm chi phí để phạt các trọng số có giá trị lớn. b) Loại bỏ ngẫu nhiên các nơ-ron trong quá trình huấn luyện. c) Dừng quá trình huấn luyện sớm. d) Chuẩn hóa các đặc trưng đầu vào.
    
13. **Điều gì xảy ra với các trọng số `W` khi bạn tăng siêu tham số `λ` (lambda) trong L2 Regularization?** a) Các trọng số sẽ trở nên lớn hơn. b) Các trọng số sẽ bị đẩy về gần 0. c) Các trọng số sẽ không thay đổi. d) Một nửa số trọng số sẽ bằng 0.
    
14. **Dropout Regularization hoạt động bằng cách nào?** a) Thêm nhiễu vào dữ liệu đầu vào. b) Loại bỏ ngẫu nhiên một số nơ-ron và các kết nối của chúng trong mỗi lần lặp của quá trình huấn luyện. c) Giảm tốc độ học theo thời gian. d) Chỉ sử dụng một phần nhỏ của tập dữ liệu.
    
15. **Kỹ thuật "Inverted Dropout" thực hiện điều gì để giữ cho giá trị kỳ vọng của các kích hoạt không đổi?** a) Chia các kích hoạt của các nơ-ron còn lại cho `keep_prob`. b) Nhân các kích hoạt của các nơ-ron còn lại với `keep_prob`. c) Thêm một giá trị bias mới. d) Không làm gì cả.
    
16. **Khi nào thì Dropout được áp dụng?** a) Chỉ trong quá trình huấn luyện. b) Chỉ trong quá trình kiểm thử (test time). c) Cả trong quá trình huấn luyện và kiểm thử. d) Không bao giờ được áp dụng ở lớp đầu ra.
    
17. **Một trong những nhược điểm của Dropout là gì?** a) Nó làm tăng High Bias. b) Nó làm cho hàm chi phí `J` không còn được định nghĩa rõ ràng, gây khó khăn cho việc gỡ lỗi. c) Nó chỉ hoạt động với hàm kích hoạt Sigmoid. d) Nó yêu cầu một lượng lớn bộ nhớ.
    
18. **"Data Augmentation" (Tăng cường dữ liệu) là một kỹ thuật điều chuẩn hóa bằng cách:** a) Mua thêm dữ liệu từ bên ngoài. b) Tạo ra các mẫu huấn luyện mới bằng cách biến đổi các mẫu hiện có (ví dụ: lật ảnh, xoay ảnh). c) Lặp lại các mẫu dữ liệu hiện có nhiều lần. d) Giảm số lượng đặc trưng.
    
19. **"Early Stopping" (Dừng sớm) hoạt động dựa trên nguyên tắc nào?** a) Dừng huấn luyện sau một số lần lặp cố định. b) Dừng huấn luyện khi lỗi trên tập huấn luyện bắt đầu tăng. c) Dừng huấn luyện khi lỗi trên tập phát triển (dev set) ngừng giảm và bắt đầu tăng. d) Dừng huấn luyện khi độ chính xác đạt 100%.
    
20. **Đâu là một nhược điểm của Early Stopping?** a) Nó không hiệu quả trong việc giảm overfitting. b) Nó kết hợp hai nhiệm vụ: tối ưu hóa hàm chi phí và chống overfitting, làm cho việc tìm kiếm siêu tham số trở nên phức tạp hơn. c) Nó yêu cầu một mạng nơ-ron rất sâu. d) Nó chỉ hoạt động với L2 regularization.
    

#### Phần 3: Tối ưu hóa Quá trình Huấn luyện

21. **Mục đích của việc chuẩn hóa các đặc trưng đầu vào (Normalizing inputs) là gì?** a) Để làm cho dữ liệu khó hiểu hơn. b) Để làm cho hàm chi phí có dạng đối xứng hơn (giống hình cái bát tròn), giúp Gradient Descent hội tụ nhanh hơn. c) Để tăng số lượng đặc trưng. d) Để loại bỏ các giá trị ngoại lai.
    
22. **Hai bước chính trong việc chuẩn hóa đầu vào là gì?** a) Trừ đi giá trị lớn nhất và chia cho giá trị nhỏ nhất. b) Trừ đi trung bình và chia cho phương sai (hoặc độ lệch chuẩn). c) Lấy logarit và sau đó lấy căn bậc hai. d) Thêm một hằng số và nhân với một hằng số.
    
23. **"Vanishing Gradients" (Gradient biến mất) là hiện tượng gì?** a) Gradient trở nên rất lớn, gây ra sự bất ổn trong quá trình huấn luyện. b) Gradient trở nên rất nhỏ (gần bằng 0) khi lan truyền ngược qua nhiều lớp, khiến việc học ở các lớp đầu tiên diễn ra rất chậm. c) Gradient biến mất khỏi bộ nhớ máy tính. d) Gradient luôn bằng 1.
    
24. **"Exploding Gradients" (Gradient bùng nổ) là hiện tượng gì?** a) Gradient trở nên rất lớn khi lan truyền ngược, gây ra các bước cập nhật quá lớn và làm cho mô hình phân kỳ. b) Gradient trở nên rất nhỏ. c) Gradient chỉ xuất hiện ở lớp cuối cùng. d) Gradient được lưu vào một file riêng.
    
25. **Phương pháp khởi tạo trọng số nào được đề xuất để sử dụng với hàm kích hoạt ReLU?** a) Khởi tạo bằng 0. b) Khởi tạo Xavier/Glorot. c) Khởi tạo He. d) Khởi tạo bằng 1.
    
26. **Công thức khởi tạo He cho trọng số `W[l]` sử dụng phương sai là bao nhiêu? (với `n[l-1]` là số nơ-ron ở lớp trước)** a) `1 / n[l-1]` b) `2 / n[l-1]` c) `1 / n[l]` d) `2 / n[l]`
    
27. **Tại sao việc khởi tạo tất cả các trọng số bằng 0 lại là một ý tưởng tồi?** a) Vì nó gây ra lỗi chia cho 0. b) Vì nó tạo ra vấn đề "đối xứng", khiến tất cả các nơ-ron trong một lớp học cùng một thứ. c) Vì nó làm cho quá trình huấn luyện quá nhanh. d) Vì nó chỉ hoạt động với mạng nông.
    
28. **Nếu bạn sử dụng hàm kích hoạt `tanh`, phương pháp khởi tạo trọng số nào thường được khuyên dùng?** a) Khởi tạo He b) Khởi tạo bằng 0 c) Khởi tạo Xavier d) Khởi tạo bằng 1
    
29. **Việc chuẩn hóa đầu vào có thể giúp giảm thiểu vấn đề gradient biến mất/bùng nổ không?** a) Có, vì nó giúp giữ cho các giá trị đầu vào ở một quy mô hợp lý. b) Không, nó hoàn toàn không liên quan. c) Nó chỉ làm cho vấn đề tồi tệ hơn. d) Nó chỉ giải quyết được vấn đề gradient biến mất.
    
30. **Việc lựa chọn phương pháp khởi tạo trọng số phù hợp phụ thuộc chủ yếu vào yếu tố nào?** a) Số lượng lớp trong mạng. b) Kích thước của tập dữ liệu. c) Loại hàm kích hoạt được sử dụng. d) Tốc độ học.
    

#### Phần 4: Gỡ lỗi và Câu hỏi lý thuyết bổ sung

31. **"Gradient Checking" là một kỹ thuật được sử dụng để làm gì?** a) Để tăng tốc độ của Gradient Descent. b) Để kiểm tra xem việc triển khai thuật toán lan truyền ngược (backpropagation) có đúng hay không. c) Để tự động chọn tốc độ học. d) Để điều chuẩn hóa mô hình.
    
32. **Gradient Checking hoạt động bằng cách nào?** a) So sánh gradient tính bằng lan truyền ngược với gradient được ước tính bằng phương pháp số (xấp xỉ hai phía). b) Chạy Gradient Descent hai lần và so sánh kết quả. c) Kiểm tra xem hàm chi phí có giảm sau mỗi lần lặp hay không. d) So sánh các trọng số trước và sau khi cập nhật.
    
33. **Bạn có nên sử dụng Gradient Checking trong quá trình huấn luyện không?** a) Có, trong mỗi lần lặp. b) Không, nó chỉ nên được sử dụng để gỡ lỗi và sau đó tắt đi vì nó rất chậm về mặt tính toán. c) Chỉ khi mô hình bị overfitting. d) Chỉ khi mô hình bị underfitting.
    
34. **Gradient Checking có hoạt động với Dropout không?** a) Có, nó hoạt động hoàn hảo. b) Không, vì Dropout đưa vào tính ngẫu nhiên, làm cho hàm chi phí thay đổi trong mỗi lần chạy, khiến việc kiểm tra gradient trở nên khó khăn. c) Chỉ hoạt động với `keep_prob` = 1. d) Chỉ hoạt động với `keep_prob` = 0.5.
    
35. **Nếu kết quả của Gradient Checking cho ra một sự khác biệt lớn (ví dụ: `10⁻²`), điều đó có nghĩa là gì?** a) Việc triển khai lan truyền ngược của bạn có khả năng cao là đúng. b) Việc triển khai lan truyền ngược của bạn có khả năng cao là sai. c) Tốc độ học của bạn quá lớn. d) Mô hình của bạn đang học rất tốt.
    
36. **"Bias" và "Variance" có mối quan hệ "trade-off" (đánh đổi) trong học máy cổ điển. Điều này có còn đúng trong học sâu không?** a) Có, hoàn toàn đúng. b) Không hẳn, trong học sâu, việc tăng kích thước mạng và thêm dữ liệu thường có thể giảm cả bias và variance (hoặc giảm một cái mà không làm tăng cái kia nhiều). c) Trong học sâu chỉ có bias, không có variance. d) Trong học sâu chỉ có variance, không có bias.
    
37. **Đâu không phải là một phương pháp điều chuẩn hóa?** a) L2 Regularization b) Dropout c) Gradient Descent d) Data Augmentation
    
38. **Việc thêm điều chuẩn hóa L2 vào hàm chi phí tương đương với việc đặt một prior (tiên nghiệm) nào lên các trọng số?** a) Prior phân phối Laplace. b) Prior phân phối Gaussian với trung bình 0. c) Prior phân phối đều. d) Không tương đương với bất kỳ prior nào.
    
39. **Tại sao Dropout có thể được coi là một dạng của L2 regularization?** a) Vì nó buộc các nơ-ron phải học các trọng số nhỏ hơn và phân tán hơn, không phụ thuộc vào bất kỳ đặc trưng nào. b) Vì công thức toán học của chúng giống hệt nhau. c) Vì chúng đều làm cho quá trình huấn luyện chậm lại. d) Chúng không liên quan đến nhau.
    
40. **Việc chuẩn hóa đầu vào sử dụng trung bình và phương sai được tính từ tập dữ liệu nào?** a) Chỉ từ tập test. b) Chỉ từ tập dev. c) Chỉ từ tập huấn luyện (train set). d) Từ toàn bộ dữ liệu (train + dev + test).
    
41. **Khi áp dụng chuẩn hóa cho tập dev/test, bạn nên làm gì?** a) Tính lại trung bình và phương sai mới từ tập dev/test. b) Sử dụng cùng một giá trị trung bình và phương sai đã được tính từ tập huấn luyện. c) Không cần chuẩn hóa tập dev/test. d) Trộn tập train và dev/test lại rồi tính trung bình và phương sai.
    
42. **Trong thực tế, khi nào bạn nên lo lắng về vấn đề High Bias?** a) Khi lỗi trên tập dev rất cao. b) Khi lỗi trên tập huấn luyện cao hơn đáng kể so với hiệu suất của con người (hoặc lỗi Bayes). c) Khi lỗi trên tập huấn luyện thấp nhưng lỗi trên tập dev cao. d) Khi mô hình huấn luyện rất nhanh.
    
43. **"Orthogonalization" (Trực giao hóa) trong học máy là ý tưởng về việc:** a) Sử dụng các vector trực giao để khởi tạo trọng số. b) Đảm bảo rằng mỗi "nút vặn" (kỹ thuật) bạn sử dụng chỉ ảnh hưởng đến một khía cạnh duy nhất của hiệu suất mô hình (ví dụ: một nút cho bias, một nút khác cho variance). c) Làm cho các lớp trong mạng nơ-ron độc lập với nhau. d) Luôn sử dụng ma trận vuông.
    
44. **Nếu mô hình của bạn có High Variance, nhưng bạn không thể thu thập thêm dữ liệu, lựa chọn tốt nhất tiếp theo là gì?** a) Tăng kích thước mạng. b) Tăng cường các kỹ thuật điều chuẩn hóa (tăng `λ`, giảm `keep_prob`). c) Huấn luyện lâu hơn nữa. d) Giảm tốc độ học.
    
45. **Trong "inverted dropout", tại sao chúng ta không cần phải làm gì thêm ở bước kiểm thử (test time)?** a) Vì ở bước kiểm thử chúng ta cũng áp dụng dropout. b) Vì việc chia cho `keep_prob` trong quá trình huấn luyện đã đảm bảo rằng đầu ra ở bước kiểm thử không cần phải thay đổi tỷ lệ. c) Vì bước kiểm thử không quan trọng. d) Vì chúng ta nhân với `keep_prob` ở bước kiểm thử.
    
46. **Kỹ thuật nào giúp giải quyết vấn đề "internal covariate shift" (sự thay đổi hiệp phương sai nội bộ)?** a) L2 Regularization b) Dropout c) Batch Normalization (Sẽ học ở bài sau, nhưng là một khái niệm liên quan) d) Chuẩn hóa đầu vào (Input Normalization).
    
47. **Nếu bạn đang gỡ lỗi cho việc triển khai backpropagation, bạn nên kiểm tra thành phần nào trước tiên?** a) Đạo hàm của hàm chi phí. b) Đạo hàm của hàm kích hoạt. c) Phép nhân ma trận. d) Tất cả các thành phần, bắt đầu từ lớp cuối cùng và đi ngược lại.
    
48. **Việc huấn luyện một mạng nơ-ron là một quá trình có tính chất gì?** a) Có thể dự đoán chính xác kết quả ngay từ đầu. b) Mang tính thực nghiệm cao, đòi hỏi nhiều lần thử và sai. c) Luôn luôn hội tụ đến điểm tối ưu toàn cục. d) Chỉ cần một lần lặp là đủ.
    
49. **L1 regularization khác L2 regularization ở điểm nào?** a) L1 có xu hướng đẩy các trọng số về 0, tạo ra các mô hình thưa (sparse), trong khi L2 chỉ làm chúng nhỏ lại. b) L2 có xu hướng đẩy các trọng số về 0, tạo ra các mô hình thưa (sparse), trong khi L1 chỉ làm chúng nhỏ lại. c) L1 chỉ dùng cho mạng nông, L2 chỉ dùng cho mạng sâu. d) Không có sự khác biệt.
    
50. **Đâu là lý do chính khiến các mạng nơ-ron sâu dễ bị overfitting hơn các mô hình đơn giản?** a) Vì chúng có ít tham số hơn. b) Vì chúng có rất nhiều tham số, cho phép chúng học được cả nhiễu trong dữ liệu huấn luyện. c) Vì chúng huấn luyện chậm hơn. d) Vì chúng không thể sử dụng các kỹ thuật điều chuẩn hóa.
    

### **Đáp án**

<details> <summary>Nhấn vào đây để xem đáp án</summary>

1. c | 2. c | 3. c | 4. b | 5. a
    
2. b | 7. c | 8. b | 9. b | 10. c
    
3. c | 12. a | 13. b | 14. b | 15. a
    
4. a | 17. b | 18. b | 19. c | 20. b
    
5. b | 22. b | 23. b | 24. a | 25. c
    
6. b | 27. b | 28. c | 29. a | 30. c
    
7. b | 32. a | 33. b | 34. b | 35. b
    
8. b | 37. c | 38. b | 39. a | 40. c
    
9. b | 42. b | 43. b | 44. b | 45. b
    
10. d | 47. d | 48. b | 49. a | 50. b
    

</details>


### Bài kiểm tra trắc nghiệm: Tối ưu hóa và Tinh chỉnh Siêu tham số

**Chọn câu trả lời đúng nhất cho mỗi câu hỏi.**

#### Phần 1: Các thuật toán Tối ưu hóa (Optimization Algorithms)

1. **Sự khác biệt chính giữa Batch Gradient Descent và Mini-batch Gradient Descent là gì?** a) Batch GD nhanh hơn Mini-batch GD. b) Batch GD cập nhật tham số sau mỗi mẫu dữ liệu, còn Mini-batch GD cập nhật sau mỗi lô nhỏ. c) Batch GD cập nhật tham số sau khi xử lý toàn bộ tập huấn luyện, còn Mini-batch GD cập nhật sau mỗi lô nhỏ (subset). d) Mini-batch GD luôn hội tụ tốt hơn.
    
2. **Một "epoch" có nghĩa là gì?** a) Một lần cập nhật các tham số. b) Một lần thuật toán đi qua toàn bộ tập dữ liệu huấn luyện. c) Kích thước của một mini-batch. d) Số lượng lớp trong mạng nơ-ron.
    
3. **Nếu bạn có 5,000,000 mẫu huấn luyện và kích thước mini-batch là 1000, có bao nhiêu lần lặp (iterations) trong một epoch?** a) 1000 b) 5,000,000 c) 5000 d) 1
    
4. **Ưu điểm của Mini-batch Gradient Descent so với Stochastic Gradient Descent (SGD) là gì?** a) Mini-batch GD ít "nhiễu" hơn và có thể tận dụng lợi thế của vector hóa để tính toán nhanh hơn. b) Mini-batch GD luôn tìm ra điểm tối ưu toàn cục tốt hơn. c) Mini-batch GD không cần thiết lập tốc độ học. d) SGD luôn nhanh hơn Mini-batch GD.
    
5. **Trong công thức tính Trung bình trọng số mũ (EWA), `Vt = β * Vt-1 + (1-β) * θt`, nếu `β` được đặt gần bằng 1 (ví dụ: 0.98), đường cong trung bình sẽ như thế nào?** a) Rất nhiễu và bám sát vào các điểm dữ liệu. b) Mượt hơn và phản ứng chậm hơn với sự thay đổi. c) Gần như là một đường thẳng. d) Luôn đi qua điểm dữ liệu đầu tiên.
    
6. **Mục đích của "Bias correction" trong EWA là gì?** a) Để làm cho thuật toán chạy nhanh hơn. b) Để hiệu chỉnh ước tính ban đầu, vốn bị chệch về phía 0, đặc biệt là trong giai đoạn đầu. c) Để ngăn chặn overfitting. d) Để tăng giá trị của `β`.
    
7. **Gradient Descent with Momentum được thiết kế để giải quyết vấn đề gì?** a) Giảm thiểu dao động theo chiều dọc và tăng tốc độ hội tụ theo chiều ngang trong các hàm chi phí có dạng "thung lũng hẹp". b) Chỉ để làm cho code phức tạp hơn. c) Giảm thiểu High Bias. d) Tự động tìm kích thước mini-batch tốt nhất.
    
8. **Thuật toán RMSprop (Root Mean Square prop) điều chỉnh tốc độ học cho mỗi tham số bằng cách nào?** a) Dựa trên tổng của các gradient. b) Dựa trên trung bình trọng số mũ của các gradient. c) Dựa trên trung bình trọng số mũ của bình phương các gradient. d) Dựa trên một giá trị ngẫu nhiên.
    
9. **Thuật toán Adam (Adaptive Moment Estimation) là sự kết hợp của hai thuật toán nào?** a) Batch GD và Stochastic GD. b) Momentum và RMSprop. c) L2 Regularization và Dropout. d) EWA và Bias Correction.
    
10. **Mục đích của việc sử dụng "Learning Rate Decay" là gì?** a) Để tăng tốc độ học khi quá trình huấn luyện diễn ra. b) Để giảm dần tốc độ học khi tiến gần đến điểm tối ưu, giúp mô hình hội tụ một cách tinh vi hơn và tránh dao động quanh điểm tối ưu. c) Để giữ cho tốc độ học không đổi trong suốt quá trình huấn luyện. d) Để ngăn chặn gradient biến mất.
    
11. **Trong các mạng nơ-ron sâu và không gian nhiều chiều, hầu hết các điểm có gradient bằng 0 là gì?** a) Điểm cực tiểu toàn cục (Global optima). b) Điểm cực tiểu cục bộ (Local optima). c) Điểm yên ngựa (Saddle points). d) Điểm cực đại (Maxima).
    
12. **Hiện tượng "plateau" (vùng phẳng) trong hàm chi phí gây ra vấn đề gì?** a) Làm cho quá trình học bị chậm lại đáng kể vì gradient rất gần 0. b) Gây ra hiện tượng gradient bùng nổ. c) Khiến mô hình bị overfitting. d) Làm cho bộ nhớ bị đầy.
    
13. **Giá trị `β₁` trong thuật toán Adam thường được đặt mặc định là bao nhiêu và nó kiểm soát thành phần nào?** a) 0.999, kiểm soát RMSprop. b) 0.9, kiểm soát Momentum. c) 0.5, kiểm soát tốc độ học. d) 10⁻⁸, kiểm soát epsilon.
    
14. **Khi chọn kích thước mini-batch, tại sao các con số lũy thừa của 2 (ví dụ: 64, 128, 512) lại được ưa chuộng?** a) Vì chúng là các số đẹp. b) Vì chúng phù hợp với cách tổ chức bộ nhớ của CPU/GPU, giúp tính toán hiệu quả hơn. c) Vì chúng giúp giảm overfitting. d) Đây chỉ là một quy ước ngẫu nhiên.
    
15. **Nếu bạn có một tập dữ liệu nhỏ (ví dụ: < 2000 mẫu), bạn nên chọn kích thước mini-batch là bao nhiêu?** a) 1 (Stochastic GD). b) 64. c) Bằng kích thước của toàn bộ tập dữ liệu (Batch GD). d) 128.
    

#### Phần 2: Tinh chỉnh Siêu tham số và Batch Normalization

16. **Đâu là siêu tham số (hyperparameter) thường được coi là quan trọng nhất cần tinh chỉnh?** a) Số lớp ẩn. b) Tốc độ học `α`. c) `β` trong Momentum. d) Kích thước mini-batch.
    
17. **Tại sao tìm kiếm ngẫu nhiên (Random Search) thường hiệu quả hơn tìm kiếm theo lưới (Grid Search) để tinh chỉnh siêu tham số?** a) Vì nó luôn nhanh hơn. b) Vì nó cho phép khám phá nhiều giá trị hơn cho các siêu tham số quan trọng, trong khi một số siêu tham số khác có thể ít ảnh hưởng hơn. c) Vì nó dễ lập trình hơn. d) Vì nó đảm bảo tìm ra điểm tối ưu toàn cục.
    
18. **Khi tinh chỉnh tốc độ học `α`, tại sao nên sử dụng thang đo logarit (logarithmic scale)?** a) Vì tốc độ học luôn là một số dương. b) Vì sự thay đổi từ 0.001 đến 0.01 có tác động lớn hơn nhiều so với sự thay đổi từ 0.9 đến 0.91. Thang đo logarit giúp khám phá các khoảng giá trị nhỏ hiệu quả hơn. c) Để làm cho biểu đồ đẹp hơn. d) Vì `α` không thể lớn hơn 1.
    
19. **Chiến lược "Caviar" trong tinh chỉnh siêu tham số ám chỉ điều gì?** a) Huấn luyện một mô hình duy nhất và theo dõi, tinh chỉnh nó một cách cẩn thận. b) Huấn luyện song song nhiều mô hình với các bộ siêu tham số khác nhau và chọn ra mô hình tốt nhất. c) Chỉ sử dụng các siêu tham số mặc định. d) Sử dụng các thuật toán di truyền để tìm siêu tham số.
    
20. **Batch Normalization (Batch Norm) thực hiện việc chuẩn hóa trên cái gì?** a) Dữ liệu đầu vào `X`. b) Các giá trị kích hoạt `A` hoặc các giá trị tiền kích hoạt `Z` của các lớp ẩn. c) Các trọng số `W`. d) Các nhãn `Y`.
    
21. **Hai tham số có thể học được trong Batch Norm, `γ` (gamma) và `β` (beta), có vai trò gì?** a) Chúng là tốc độ học và momentum. b) Chúng cho phép mạng học một giá trị trung bình và phương sai tối ưu cho các kích hoạt, thay vì bị ép buộc phải có trung bình 0 và phương sai 1. c) Chúng là các tham số điều chuẩn hóa. d) Chúng được dùng để khởi tạo trọng số.
    
22. **Một trong những lợi ích chính của Batch Norm là gì?** a) Nó làm cho mạng nơ-ron trở nên sâu hơn. b) Nó cho phép sử dụng tốc độ học cao hơn và làm cho quá trình huấn luyện ổn định hơn, ít nhạy cảm với việc khởi tạo trọng số. c) Nó loại bỏ hoàn toàn nhu cầu về các hàm kích hoạt. d) Nó chỉ hoạt động với bài toán hồi quy.
    
23. **Batch Norm có tác dụng điều chuẩn hóa (regularization) nhẹ vì:** a) Nó thêm một thành phần phạt vào hàm chi phí. b) Nó loại bỏ các nơ-ron một cách ngẫu nhiên. c) Trung bình và phương sai được tính trên từng mini-batch mang một chút nhiễu, và nhiễu này được đưa vào các kích hoạt của lớp ẩn. d) Nó làm cho các trọng số nhỏ hơn.
    
24. **Trong quá trình dự đoán (test time), trung bình và phương sai cho Batch Norm được tính như thế nào?** a) Chúng được tính lại trên từng mẫu dữ liệu test. b) Chúng được tính trên toàn bộ tập test. c) Một ước tính (ví dụ: trung bình trọng số mũ) của trung bình và phương sai từ các mini-batch trong quá trình huấn luyện được sử dụng. d) Luôn được đặt bằng 0 và 1.
    
25. **Hàm kích hoạt Softmax thường được sử dụng ở lớp đầu ra cho loại bài toán nào?** a) Hồi quy. b) Phân loại nhị phân. c) Phân loại nhiều lớp (Multi-class classification). d) Phân cụm.
    
26. **Đầu ra của lớp Softmax có đặc điểm gì?** a) Là một vector chứa các số thực bất kỳ. b) Là một số duy nhất trong khoảng (0, 1). c) Là một vector các xác suất có tổng bằng 1. d) Là một vector các số nguyên.
    
27. **Nếu lớp đầu ra của một mạng Softmax có 4 nơ-ron, điều đó có nghĩa là gì?** a) Mạng có 4 lớp ẩn. b) Bài toán có 4 đặc trưng đầu vào. c) Bài toán phân loại có 4 lớp. d) Kích thước mini-batch là 4.
    
28. **TensorFlow là gì?** a) Một ngôn ngữ lập trình. b) Một hệ điều hành. c) Một framework mã nguồn mở cho học máy và học sâu. d) Một thuật toán tối ưu hóa.
    
29. **Trong TensorFlow, "placeholder" (trước TF 2.x) hoặc `tf.function` với `input_signature` được dùng để làm gì?** a) Để lưu trữ các trọng số đã được huấn luyện. b) Để định nghĩa một biến sẽ được cung cấp dữ liệu sau (ví dụ: dữ liệu đầu vào từ mini-batch). c) Để tính toán hàm chi phí. d) Để khởi tạo các biến.
    
30. **Một ưu điểm lớn của việc sử dụng các framework học sâu như TensorFlow là gì?** a) Bạn phải tự viết code cho lan truyền ngược. b) Chúng tự động tính toán các đạo hàm cho lan truyền ngược, bạn chỉ cần định nghĩa lan truyền xuôi. c) Chúng chỉ chạy được trên CPU. d) Chúng không yêu cầu dữ liệu.
    

#### Phần 3: Câu hỏi lý thuyết bổ sung

31. **Tại sao Mini-batch GD thường được ưa chuộng hơn Batch GD trong thực tế?** a) Vì nó hội tụ mượt mà hơn. b) Vì việc tính toán gradient trên toàn bộ tập dữ liệu (đặc biệt là dữ liệu lớn) rất tốn kém và chậm chạp. c) Vì nó yêu cầu bộ nhớ ít hơn Batch GD. d) Cả b và c đều đúng.
    
32. **Giá trị `β` trong EWA xấp xỉ trung bình trên bao nhiêu ngày?** a) `1 / β` b) `1 / (1 - β)` c) `β / (1 - β)` d) `1 - β`
    
33. **Thuật toán Momentum giúp "tích lũy đà" theo hướng có gradient nhất quán, điều này có ý nghĩa gì?** a) Nó làm cho thuật toán di chuyển nhanh hơn theo các hướng mà gradient liên tục chỉ về một phía. b) Nó làm cho thuật toán dừng lại. c) Nó chỉ hoạt động trên các hàm lồi. d) Nó làm giảm tốc độ học.
    
34. **Tại sao thuật toán Adam lại được gọi là "thích ứng" (Adaptive)?** a) Vì nó thích ứng với kích thước của tập dữ liệu. b) Vì nó tính toán một tốc độ học riêng biệt, thích ứng cho từng tham số. c) Vì nó có thể thay đổi kiến trúc mạng. d) Vì nó chỉ hoạt động trên CPU.
    
35. **Đâu không phải là một phương pháp learning rate decay?** a) Exponential decay. b) Step decay. c) Random decay. d) `1 / (1 + decay_rate * epoch_num)`.
    
36. **Trong không gian nhiều chiều, tại sao các điểm yên ngựa (saddle points) lại phổ biến hơn các điểm cực tiểu cục bộ (local optima)?** a) Vì để là một điểm cực tiểu cục bộ, hàm chi phí phải cong lên ở tất cả các chiều, một điều kiện rất khó xảy ra. b) Vì các thuật toán tối ưu hóa có xu hướng tránh các điểm cực tiểu cục bộ. c) Vì các hàm chi phí trong học sâu luôn là hàm lồi. d) Đây là một nhận định sai.
    
37. **Đâu là một siêu tham số của thuật toán Adam?** a) `keep_prob` b) `λ` (lambda) c) `β₁`, `β₂`, `ε` d) Số lượng epoch.
    
38. **Việc tinh chỉnh siêu tham số là một quá trình mang tính:** a) Lý thuyết và có thể tính toán chính xác. b) Thực nghiệm, đòi hỏi nhiều lần thử và sai. c) Tự động hoàn toàn. d) Chỉ cần thực hiện một lần duy nhất.
    
39. **Batch Norm giúp giải quyết vấn đề "Internal Covariate Shift". Vấn đề này là gì?** a) Sự thay đổi trong phân phối của dữ liệu đầu vào. b) Sự thay đổi trong phân phối của các kích hoạt ở các lớp ẩn khi các lớp trước đó cập nhật tham số. c) Sự khác biệt giữa tập train và tập test. d) Sự thay đổi trong tốc độ học.
    
40. **Bạn nên đặt lớp Batch Norm ở đâu trong một tầng của mạng nơ-ron?** a) Trước phép tính tuyến tính (`Z`). b) Giữa phép tính tuyến tính (`Z`) và hàm kích hoạt (`A`). c) Sau hàm kích hoạt (`A`). d) Chỉ ở lớp đầu ra.
    
41. **Nếu bạn sử dụng Batch Norm, tham số `b` (bias) trong phép tính `Z = W*A + b` có còn cần thiết không?** a) Có, nó rất quan trọng. b) Không, vì tác dụng của nó sẽ bị loại bỏ bởi bước trừ đi trung bình trong Batch Norm. c) Chỉ cần thiết ở lớp đầu ra. d) Chỉ cần thiết nếu không dùng hàm kích hoạt.
    
42. **Softmax là một dạng tổng quát hóa của hàm nào cho trường hợp nhiều lớp?** a) ReLU b) Tanh c) Sigmoid d) Linear
    
43. **Nếu một trong các giá trị đầu vào của Softmax rất lớn so với các giá trị khác, xác suất đầu ra tương ứng sẽ như thế nào?** a) Gần 0. b) Gần 0.5. c) Gần 1. d) Không thể xác định.
    
44. **"Tuning process" (Quá trình tinh chỉnh) trong học sâu thường bắt đầu bằng việc:** a) Thử nghiệm với một kiến trúc mạng rất phức tạp. b) Tìm ra tốc độ học tốt nhất trước tiên, vì nó là siêu tham số quan trọng nhất. c) Thu thập càng nhiều dữ liệu càng tốt. d) Chọn một thuật toán tối ưu hóa ngẫu nhiên.
    
45. **Tại sao việc theo dõi đường cong học tập (learning curve - cost theo số lần lặp) lại quan trọng?** a) Để đảm bảo code không có lỗi cú pháp. b) Để chẩn đoán các vấn đề như tốc độ học quá lớn/quá nhỏ, hoặc mô hình có đang học hay không. c) Để tính toán số lượng tham số. d) Chỉ để tạo ra các biểu đồ đẹp.
    
46. **So với Batch GD, đường cong chi phí của Mini-batch GD có đặc điểm gì?** a) Mượt mà và luôn đi xuống. b) Có nhiều "nhiễu" (dao động) nhưng có xu hướng chung là đi xuống. c) Luôn đi lên. d) Là một đường thẳng.
    
47. **Trong công thức của Momentum, `β` thường được đặt giá trị là bao nhiêu?** a) 0.9 b) 0.999 c) 0.5 d) 1.0
    
48. **Việc sử dụng các framework như TensorFlow/PyTorch giúp các nhà nghiên cứu và kỹ sư tập trung vào đâu?** a) Tối ưu hóa các phép toán ma trận ở mức độ thấp. b) Xây dựng kiến trúc mô hình và thử nghiệm các ý tưởng mới. c) Viết driver cho GPU. d) Quản lý bộ nhớ.
    
49. **Trong bài toán phân loại có 3 lớp (A, B, C), nếu đầu ra của lớp Softmax là `[0.1, 0.8, 0.1]`, dự đoán của mô hình là gì?** a) Lớp A b) Lớp B c) Lớp C d) Không thể xác định.
    
50. **Đâu là một lý do khiến Batch Norm có thể làm cho mạng nơ-ron ít nhạy cảm hơn với việc khởi tạo trọng số?** a) Vì nó chuẩn hóa các kích hoạt, giảm bớt ảnh hưởng của các trọng số ban đầu không tốt. b) Vì nó tự động khởi tạo các trọng số. c) Vì nó loại bỏ một nửa số trọng số. d) Vì nó làm cho tất cả các trọng số bằng nhau.
    

### **Đáp án**

<details> <summary>Nhấn vào đây để xem đáp án</summary>

1. c | 2. b | 3. c | 4. a | 5. b
    
2. b | 7. a | 8. c | 9. b | 10. b
    
3. c | 12. a | 13. b | 14. b | 15. c
    
4. b | 17. b | 18. b | 19. b | 20. b
    
5. b | 22. b | 23. c | 24. c | 25. c
    
6. c | 27. c | 28. c | 29. b | 30. b
    
7. d | 32. b | 33. a | 34. b | 35. c
    
8. a | 37. c | 38. b | 39. b | 40. b
    
9. b | 42. c | 43. c | 44. b | 45. b
    
10. b | 47. a | 48. b | 49. b | 50. a
    

</details>

### Bài kiểm tra trắc nghiệm: Mạng Nơ-ron Tích chập (CNN)

**Chọn câu trả lời đúng nhất cho mỗi câu hỏi.**

#### Phần 1: Nền tảng về CNN

1. **Tại sao mạng nơ-ron truyền thẳng (fully-connected) thông thường không phù hợp với các hình ảnh có kích thước lớn?** a) Vì chúng không thể học được các đặc trưng phức tạp. b) Vì số lượng tham số sẽ trở nên cực kỳ lớn, dễ gây overfitting và tốn kém về mặt tính toán. c) Vì chúng chỉ hoạt động với ảnh xám. d) Vì chúng yêu cầu phải có lớp pooling.
    
2. **Hai ưu điểm chính của Mạng Nơ-ron Tích chập (CNN) so với mạng nơ-ron thông thường là gì?** a) Vector hóa và Tốc độ học cao. b) Chia sẻ tham số (Parameter sharing) và Kết nối thưa (Sparsity of connections). c) Lớp ẩn và Lớp đầu ra. d) Điều chuẩn hóa L2 và Dropout.
    
3. **"Parameter sharing" (Chia sẻ tham số) trong CNN có nghĩa là gì?** a) Mỗi nơ-ron trong một lớp có một bộ trọng số riêng. b) Một bộ lọc (filter) với cùng một bộ trọng số được sử dụng để quét qua các vùng khác nhau của ảnh. c) Các lớp khác nhau chia sẻ cùng một bộ trọng số. d) Giảm số lượng tham số bằng cách chia sẻ chúng với một mô hình khác.
    
4. **"Sparsity of connections" (Kết nối thưa) trong CNN có nghĩa là gì?** a) Mỗi nơ-ron đầu ra chỉ kết nối với tất cả các nơ-ron đầu vào. b) Mỗi nơ-ron đầu ra chỉ phụ thuộc vào một vùng nhỏ (local region) của các nơ-ron đầu vào. c) Một số kết nối bị loại bỏ ngẫu nhiên. d) Mạng có rất ít lớp.
    
5. **Mục đích chính của phép tích chập (convolution operation) trong CNN là gì?** a) Để giảm kích thước của ảnh. b) Để tăng độ sáng của ảnh. c) Để trích xuất các đặc trưng (features) từ ảnh, chẳng hạn như các cạnh, góc, hoặc các hoa văn. d) Để phân loại ảnh.
    
6. **Trong một phép tích chập, "filter" (bộ lọc) hay "kernel" là gì?** a) Là ảnh đầu ra sau khi tích chập. b) Là một ma trận các trọng số nhỏ được học để phát hiện một đặc trưng cụ thể. c) Là kích thước của ảnh đầu vào. d) Là một hàm kích hoạt.
    
7. **Lớp đầu tiên của một CNN thường học được các đặc trưng ở cấp độ nào?** a) Các đối tượng hoàn chỉnh như khuôn mặt, xe hơi. b) Các bộ phận của đối tượng như mắt, bánh xe. c) Các đặc trưng đơn giản như các cạnh, góc, và màu sắc. d) Các câu văn hoàn chỉnh.
    
8. **Đầu ra của một phép tích chập được gọi là gì?** a) Vector trọng số. b) Lớp ẩn. c) Bản đồ đặc trưng (Feature Map) hoặc Bản đồ kích hoạt (Activation Map). d) Lớp pooling.
    
9. **Một bộ lọc `[[1, 0, -1], [1, 0, -1], [1, 0, -1]]` được thiết kế để phát hiện loại đặc trưng nào?** a) Các cạnh ngang. b) Các cạnh dọc. c) Các góc. d) Các vùng màu đỏ.
    
10. **Các giá trị trong các bộ lọc của CNN được xác định như thế nào?** a) Chúng được thiết lập thủ công bởi người lập trình. b) Chúng được học tự động thông qua quá trình huấn luyện (sử dụng backpropagation). c) Chúng luôn là các số 0 và 1. d) Chúng được lấy ngẫu nhiên và không thay đổi.
    

#### Phần 2: Các thành phần kiến trúc CNN

11. **"Padding" trong CNN được sử dụng để giải quyết vấn đề gì?** a) Làm cho ảnh đầu vào lớn hơn. b) Giảm số lượng kênh màu. c) Ngăn chặn việc kích thước đầu ra bị thu nhỏ và mất thông tin ở các cạnh của ảnh. d) Tăng tốc độ tính toán.
    
12. **"Valid Padding" có nghĩa là gì?** a) Thêm padding để kích thước đầu ra bằng kích thước đầu vào. b) Không sử dụng padding (`p=0`). c) Chỉ thêm padding ở các cạnh hợp lệ. d) Thêm padding bằng các giá trị ngẫu nhiên.
    
13. **"Same Padding" có nghĩa là gì?** a) Không sử dụng padding. b) Thêm một lượng padding sao cho kích thước chiều cao và chiều rộng của đầu ra bằng với đầu vào. c) Sử dụng cùng một giá trị padding cho tất cả các lớp. d) Sử dụng cùng một bộ lọc cho tất cả các lớp.
    
14. **"Stride" (bước nhảy) trong phép tích chập là gì?** a) Kích thước của bộ lọc. b) Số lượng pixel mà bộ lọc dịch chuyển qua ảnh trong mỗi bước. c) Số lượng lớp trong mạng. d) Kích thước của padding.
    
15. **Nếu bạn thực hiện tích chập trên một ảnh màu RGB (có 3 kênh), chiều sâu (số kênh) của bộ lọc phải là bao nhiêu?** a) 1 b) 3 c) Tùy ý. d) Bằng kích thước của bộ lọc (ví dụ: 3x3 thì chiều sâu là 3).
    
16. **Nếu bạn áp dụng 16 bộ lọc khác nhau vào một ảnh đầu vào, chiều sâu (số kênh) của bản đồ đặc trưng đầu ra sẽ là bao nhiêu?** a) 1 b) 3 c) 16 d) Bằng chiều sâu của ảnh đầu vào.
    
17. **Mục đích chính của lớp Pooling là gì?** a) Để tăng độ phân giải của bản đồ đặc trưng. b) Để giảm kích thước không gian (chiều cao và rộng) của bản đồ đặc trưng, giúp giảm tính toán và kiểm soát overfitting. c) Để thêm các đặc trưng mới. d) Để học các bộ lọc.
    
18. **Max Pooling hoạt động như thế nào?** a) Lấy giá trị trung bình của các pixel trong một vùng. b) Lấy giá trị lớn nhất của các pixel trong một vùng. c) Lấy giá trị nhỏ nhất của các pixel trong một vùng. d) Tính tổng các pixel trong một vùng.
    
19. **Lớp Pooling có các tham số cần học (như trọng số) không?** a) Có, nó có cả trọng số và độ lệch. b) Chỉ có trọng số. c) Không, nó không có tham số nào để học. d) Chỉ có độ lệch.
    
20. **Đâu là các siêu tham số của một lớp Pooling?** a) Kích thước bộ lọc (`f`) và bước nhảy (`s`). b) Tốc độ học và momentum. c) Số lượng lớp và số nơ-ron. d) Hàm kích hoạt và hàm chi phí.
    

#### Phần 3: Xây dựng và Vận dụng CNN

21. **Ba loại lớp phổ biến nhất trong một kiến trúc CNN điển hình là gì?** a) Input, Hidden, Output. b) Convolutional, Pooling, Fully Connected. c) ReLU, Sigmoid, Tanh. d) Adam, RMSprop, Momentum.
    
22. **Lớp Fully Connected (FC) thường được đặt ở đâu trong một CNN và có vai trò gì?** a) Ở đầu mạng, để tiền xử lý ảnh. b) Ở giữa các lớp CONV, để tăng tính phi tuyến. c) Ở cuối mạng, để thực hiện việc phân loại cuối cùng dựa trên các đặc trưng đã được trích xuất. d) Nó không được sử dụng trong CNN.
    
23. **Khi đi sâu hơn vào một mạng CNN, kích thước không gian (chiều cao, rộng) và chiều sâu (số kênh) của các bản đồ đặc trưng thường thay đổi như thế nào?** a) Kích thước không gian tăng, chiều sâu giảm. b) Kích thước không gian giảm, chiều sâu tăng. c) Cả hai đều tăng. d) Cả hai đều giảm.
    
24. **Một lớp CONV có 10 bộ lọc, mỗi bộ lọc có kích thước 3x3x3. Lớp này có bao nhiêu tham số (chỉ tính trọng số, không tính bias)?** a) 90 b) 27 c) 270 d) 30
    
25. **Tiếp câu 24, nếu mỗi bộ lọc có thêm 1 tham số bias, tổng số tham số có thể học được trong lớp đó là bao nhiêu?** a) 280 b) 271 c) 100 d) 37
    
26. **Cho ảnh đầu vào 7x7, bộ lọc 3x3, padding `p=0`, stride `s=1`. Kích thước đầu ra là bao nhiêu?** a) 7x7 b) 6x6 c) 5x5 d) 4x4
    
27. **Cho ảnh đầu vào 7x7, bộ lọc 3x3, padding `p=0`, stride `s=2`. Kích thước đầu ra là bao nhiêu?** a) 3x3 b) 4x4 c) 2x2 d) 5x5
    
28. **Cho ảnh đầu vào 10x10, bộ lọc 5x5, stride `s=1`. Cần padding `p` bằng bao nhiêu để có "Same Padding"?** a) 0 b) 1 c) 2 d) 3
    
29. **Một bản đồ đặc trưng 4x4 được đưa vào một lớp Max Pooling 2x2 với stride `s=2`. Kích thước đầu ra là bao nhiêu?** a) 4x4 b) 3x3 c) 2x2 d) 1x1
    
30. **Một lớp CONV có đầu vào là 14x14x6, sử dụng 16 bộ lọc 5x5 với stride `s=1` và padding `p=0`. Kích thước đầu ra là bao nhiêu?** a) 10x10x16 b) 14x14x16 c) 10x10x6 d) 9x9x16
    

#### Phần 4: Câu hỏi lý thuyết bổ sung

31. **Tại sao CNN có khả năng bất biến với sự dịch chuyển (translation invariance) ở một mức độ nào đó?** a) Vì nó sử dụng hàm kích hoạt ReLU. b) Vì các đặc trưng được phát hiện bởi một bộ lọc không phụ thuộc vào vị trí của chúng trên ảnh, và lớp pooling giúp làm mờ đi các khác biệt nhỏ về vị trí. c) Vì nó luôn chuẩn hóa dữ liệu đầu vào. d) Vì nó có các lớp fully connected.
    
32. **Trong các thư viện học sâu, phép toán "convolution" thực chất thường là phép toán nào trong xử lý tín hiệu?** a) Tích chập (Convolution). b) Tương quan chéo (Cross-correlation). c) Biến đổi Fourier. d) Phép cộng.
    
33. **Lớp tích chập 1x1 (1x1 Convolution) thường được sử dụng để làm gì?** a) Để phát hiện các cạnh. b) Chỉ để giảm chiều cao và rộng. c) Để thay đổi số lượng kênh (chiều sâu) của bản đồ đặc trưng một cách hiệu quả về mặt tính toán. d) Nó không có tác dụng gì.
    
34. **Hàm kích hoạt (ví dụ: ReLU) được đặt ở đâu trong một lớp CONV?** a) Trước phép tích chập. b) Sau phép tích chập và sau khi cộng bias. c) Chỉ ở lớp cuối cùng. d) Thay thế cho lớp pooling.
    
35. **Đâu là một nhược điểm của lớp Pooling?** a) Tăng số lượng tham số. b) Gây mất mát thông tin không gian. c) Làm cho quá trình huấn luyện chậm lại. d) Không tương thích với lớp CONV.
    
36. **Tại sao việc xếp chồng nhiều lớp với bộ lọc nhỏ (ví dụ: hai lớp 3x3) thường tốt hơn một lớp với bộ lọc lớn (ví dụ: một lớp 5x5)?** a) Nó có ít tham số hơn và có thể học được các hàm phức tạp hơn do có nhiều lớp phi tuyến hơn. b) Nó có nhiều tham số hơn. c) Nó chạy nhanh hơn. d) Nó dễ lập trình hơn.
    
37. **"Flattening" một lớp trong CNN có nghĩa là gì?** a) Làm cho các giá trị trong lớp bằng 0. b) Chuyển đổi một bản đồ đặc trưng đa chiều (ví dụ: 7x7x40) thành một vector phẳng (1D) để đưa vào lớp Fully Connected. c) Áp dụng một bộ lọc làm mờ. d) Giảm số lượng kênh.
    
38. **Ngoài phân loại ảnh, CNN còn có thể được sử dụng cho tác vụ nào khác?** a) Phát hiện vật thể (Object Detection). b) Phân đoạn ảnh (Image Segmentation). c) Xử lý ngôn ngữ tự nhiên (trên dữ liệu văn bản 1D). d) Tất cả các câu trên.
    
39. **Mối quan hệ giữa kích thước bộ lọc, padding, stride và kích thước đầu ra được mô tả bằng công thức nào?** a) `output_size = (n + 2p - f) / s + 1` b) `output_size = (n - 2p + f) / s + 1` c) `output_size = (n + p - f) / s` d) `output_size = n - f + 1`
    
40. **Sự khác biệt chính giữa Max Pooling và Average Pooling là gì?** a) Max Pooling giữ lại đặc trưng nổi bật nhất (mạnh nhất), trong khi Average Pooling giữ lại thông tin trung bình của đặc trưng. b) Max Pooling nhanh hơn Average Pooling. c) Average Pooling có các tham số cần học. d) Không có sự khác biệt đáng kể.
    
41. **Nếu bạn tăng số lượng bộ lọc trong một lớp CONV, điều gì sẽ xảy ra?** a) Số lượng tham số trong lớp đó sẽ tăng. b) Chiều sâu của bản đồ đặc trưng đầu ra sẽ tăng. c) Khả năng của lớp đó để học nhiều loại đặc trưng khác nhau sẽ tăng. d) Tất cả các câu trên đều đúng.
    
42. **Lớp cuối cùng của một CNN cho bài toán phân loại 10 chữ số (0-9) thường là gì?** a) Một lớp CONV với 10 bộ lọc. b) Một lớp Max Pooling. c) Một lớp Fully Connected với 10 nơ-ron và hàm kích hoạt Softmax. d) Một lớp Fully Connected với 1 nơ-ron và hàm kích hoạt Sigmoid.
    
43. **Tại sao CNN lại đặc biệt phù hợp với dữ liệu hình ảnh?** a) Vì ảnh có thể được biểu diễn dưới dạng số. b) Vì CNN có khả năng bảo toàn và tận dụng các mối quan hệ không gian giữa các pixel (tính cục bộ). c) Vì CNN luôn cho độ chính xác 100%. d) Vì CNN yêu cầu ít dữ liệu hơn các mô hình khác.
    
44. **Trong một kiến trúc CNN, lớp nào chịu trách nhiệm chính cho việc học các đặc trưng?** a) Lớp Pooling. b) Lớp Fully Connected. c) Lớp Convolutional. d) Lớp Input.
    
45. **Trong một kiến trúc CNN, lớp nào chịu trách nhiệm chính cho việc giảm kích thước?** a) Lớp Pooling và các lớp CONV có stride > 1. b) Lớp Fully Connected. c) Lớp Convolutional có stride = 1. d) Lớp Input.
    
46. **"Receptive field" (trường tiếp nhận) của một nơ-ron trong CNN là gì?** a) Toàn bộ ảnh đầu vào. b) Vùng trên ảnh đầu vào mà nơ-ron đó "nhìn thấy" hoặc bị ảnh hưởng bởi. c) Kích thước của bộ lọc. d) Số lượng nơ-ron trong lớp.
    
47. **Nếu bạn xếp chồng hai lớp CONV 3x3 (stride 1), trường tiếp nhận của một nơ-ron ở lớp thứ hai sẽ có kích thước bao nhiêu trên đầu vào của lớp đầu tiên?** a) 3x3 b) 4x4 c) 5x5 d) 6x6
    
48. **Đâu không phải là một siêu tham số của một lớp CONV?** a) Kích thước bộ lọc (`f`). b) Số lượng bộ lọc (`nC`). c) Bước nhảy (`s`). d) Ma trận trọng số (`W`).
    
49. **Trong TensorFlow Keras, lớp nào được sử dụng để tạo một lớp tích chập 2D?** a) `tf.keras.layers.Dense` b) `tf.keras.layers.Conv2D` c) `tf.keras.layers.MaxPooling2D` d) `tf.keras.layers.Flatten`
    
50. **Đâu là một kiến trúc CNN nổi tiếng?** a) Logistic Regression b) Support Vector Machine c) LeNet-5, AlexNet, VGG d) K-Means
    

### **Đáp án**

<details> <summary>Nhấn vào đây để xem đáp án</summary>

1. b | 2. b | 3. b | 4. b | 5. c
    
2. b | 7. c | 8. c | 9. b | 10. b
    
3. c | 12. b | 13. b | 14. b | 15. b
    
4. c | 17. b | 18. b | 19. c | 20. a
    
5. b | 22. c | 23. b | 24. c | 25. a
    
6. c (`(7-3+1)=5`) | 27. a (`floor((7-3)/2)+1=3`) | 28. c (`p=(5-1)/2=2`) | 29. c | 30. a (`(14-5+1)=10`)
    
7. b | 32. b | 33. c | 34. b | 35. b
    
8. a | 37. b | 38. d | 39. a | 40. a
    
9. d | 42. c | 43. b | 44. c | 45. a
    
10. b | 47. c | 48. d | 49. b | 50. c
    

</details>

### Bài kiểm tra trắc nghiệm: Các Kiến trúc CNN kinh điển và Kỹ thuật Nâng cao

**Chọn câu trả lời đúng nhất cho mỗi câu hỏi.**

#### Phần 1: Các Mạng Kinh điển (LeNet-5, AlexNet, VGG)

1. **Kiến trúc LeNet-5 ban đầu được thiết kế cho tác vụ chính nào?** a) Nhận dạng vật thể trong ảnh màu. b) Nhận dạng chữ số viết tay. c) Phân đoạn ảnh y tế. d) Dịch máy.
    
2. **Đặc điểm nào sau đây không phải của LeNet-5?** a) Sử dụng các lớp tích chập và pooling xen kẽ. b) Có khoảng 60,000 tham số. c) Sử dụng hàm kích hoạt ReLU trong tất cả các lớp. d) Chiều cao và rộng của ảnh giảm dần khi đi sâu vào mạng.
    
3. **AlexNet đã mang lại cải tiến đột phá nào so với các kiến trúc trước đó?** a) Sử dụng hàm kích hoạt Sigmoid/tanh. b) Là mạng nơ-ron nông đầu tiên. c) Sử dụng hàm kích hoạt ReLU và kỹ thuật Dropout để chống overfitting. d) Có ít tham số hơn LeNet-5.
    
4. **Kiến trúc VGG-16 nổi tiếng với đặc điểm nào?** a) Sử dụng nhiều kích thước bộ lọc khác nhau trong cùng một lớp. b) Rất nông nhưng có nhiều tham số. c) Sử dụng các kết nối tắt (skip connections). d) Sử dụng một kiến trúc rất đồng nhất, chủ yếu là các lớp tích chập 3x3 được xếp chồng lên nhau.
    
5. **Tại sao việc xếp chồng hai lớp CONV 3x3 lại được ưa chuộng trong VGG thay vì một lớp CONV 5x5?** a) Nó có nhiều tham số hơn, giúp học tốt hơn. b) Nó có ít tham số hơn và tăng độ sâu phi tuyến của mạng. c) Nó chỉ hoạt động với ảnh xám. d) Nó tính toán nhanh hơn đáng kể.
    
6. **Số lượng tham số của AlexNet so với LeNet-5 như thế nào?** a) Ít hơn đáng kể. b) Tương đương nhau. c) Nhiều hơn đáng kể (khoảng 60 triệu so với 60 nghìn). d) Gấp đôi.
    
7. **Trong AlexNet, Dropout được sử dụng ở các lớp nào?** a) Các lớp tích chập. b) Các lớp pooling. c) Các lớp fully-connected. d) Lớp đầu vào.
    
8. **Thứ tự các loại lớp trong LeNet-5 là gì?** a) CONV -> CONV -> POOL -> POOL -> FC -> FC b) CONV -> POOL -> CONV -> POOL -> FC -> FC c) FC -> FC -> CONV -> POOL -> CONV -> POOL d) CONV -> FC -> POOL -> CONV -> FC -> POOL
    
9. **VGG-16 có bao nhiêu lớp có trọng số (convolutional và fully-connected)?** a) 8 b) 16 c) 19 d) 22
    
10. **Điểm chung của LeNet-5, AlexNet, và VGG là gì?** a) Tất cả đều sử dụng kết nối tắt (skip connections). b) Cấu trúc chung là các lớp CONV/POOL xếp chồng lên nhau, theo sau là các lớp FC để phân loại. c) Tất cả đều được thiết kế cho các thiết bị di động. d) Tất cả đều có ít hơn 1 triệu tham số.
    

#### Phần 2: Các Kiến trúc Hiện đại (ResNet, Inception, MobileNet)

11. **Vấn đề chính mà Mạng Residual (ResNet) được thiết kế để giải quyết là gì?** a) Tốc độ tính toán chậm. b) Vấn đề gradient biến mất (vanishing gradients) trong các mạng rất sâu. c) Overfitting trong các mạng nông. d) Thiếu dữ liệu huấn luyện.
    
12. **Cơ chế cốt lõi của một khối Residual (Residual Block) là gì?** a) Sử dụng các bộ lọc 1x1. b) Sử dụng một kết nối tắt (skip connection) để cộng đầu vào của khối với đầu ra của nó. c) Loại bỏ ngẫu nhiên các nơ-ron. d) Sử dụng nhiều kích thước bộ lọc song song.
    
13. **Tại sao ResNet có thể huấn luyện các mạng cực kỳ sâu (hơn 100 lớp) mà không làm tăng lỗi huấn luyện?** a) Vì nó có ít tham số hơn. b) Vì kết nối tắt giúp các lớp dễ dàng học một hàm đồng nhất (identity function), đảm bảo việc thêm lớp mới không làm giảm hiệu suất. c) Vì nó chỉ sử dụng các bộ lọc 1x1. d) Vì nó không sử dụng backpropagation.
    
14. **Mục đích của việc sử dụng các lớp tích chập 1x1 trong kiến trúc "Network in Network" và Inception là gì?** a) Để tăng kích thước không gian của bản đồ đặc trưng. b) Để giảm số lượng kênh (chiều sâu) một cách hiệu quả, hoạt động như một "bottleneck" để giảm chi phí tính toán. c) Chỉ để phát hiện các cạnh dọc. d) Để thay thế hoàn toàn các lớp pooling.
    
15. **Ý tưởng chính đằng sau mạng Inception là gì?** a) Chỉ sử dụng các lớp 3x3 để đơn giản hóa kiến trúc. b) Xếp chồng các khối residual lên nhau. c) Thực hiện song song nhiều phép tích chập với các kích thước bộ lọc khác nhau (1x1, 3x3, 5x5) và cả pooling trong cùng một module, sau đó ghép kết quả lại. d) Sử dụng một mạng rất nông để tăng tốc độ.
    
16. **Mạng MobileNet được thiết kế để tối ưu cho môi trường nào?** a) Các siêu máy tính. b) Các thiết bị di động và nhúng có tài nguyên tính toán hạn chế. c) Chỉ cho các bài toán xử lý văn bản. d) Các máy chủ đám mây với GPU mạnh mẽ.
    
17. **Kỹ thuật cốt lõi được sử dụng trong MobileNet để giảm chi phí tính toán là gì?** a) Kết nối tắt (Skip connections). b) Tích chập tách biệt theo chiều sâu (Depthwise Separable Convolutions). c) Dropout. d) Data Augmentation.
    
18. **Một phép tích chập tách biệt theo chiều sâu bao gồm hai bước nào?** a) Depthwise Convolution và 1x1 Pointwise Convolution. b) Max Pooling và Average Pooling. c) Convolution và Deconvolution. d) Forward Propagation và Backward Propagation.
    
19. **Kiến trúc MobileNetV2 đã cải tiến MobileNetV1 bằng cách thêm vào yếu tố nào?** a) Các bộ lọc 7x7. b) Các khối bottleneck ngược với kết nối residual. c) Loại bỏ tất cả các lớp 1x1. d) Chỉ sử dụng hàm kích hoạt Sigmoid.
    
20. **Ý tưởng chính của EfficientNet là gì?** a) Chỉ tăng độ sâu của mạng. b) Chỉ tăng độ rộng của mạng. c) Sử dụng một phương pháp "compound scaling" để cân bằng và tăng đồng thời cả độ sâu, độ rộng và độ phân giải của mạng. d) Sử dụng một kiến trúc hoàn toàn khác so với các CNN trước đó.
    

#### Phần 3: Các Kỹ thuật Nâng cao (Transfer Learning, Data Augmentation)

21. **"Transfer Learning" (Học chuyển giao) là kỹ thuật gì?** a) Huấn luyện một mô hình từ đầu trên một tập dữ liệu mới. b) Sử dụng kiến thức (các trọng số đã được huấn luyện) từ một mô hình đã được huấn luyện trên một tác vụ lớn để áp dụng cho một tác vụ mới, thường có ít dữ liệu hơn. c) Chuyển đổi một mô hình từ TensorFlow sang PyTorch. d) Chỉ sử dụng các lớp cuối cùng của một mạng đã được huấn luyện.
    
22. **Khi nào thì Transfer Learning có khả năng hoạt động hiệu quả nhất?** a) Khi tác vụ nguồn có ít dữ liệu hơn tác vụ đích. b) Khi hai tác vụ có cùng một đầu vào (ví dụ: cùng là ảnh) và tác vụ nguồn có lượng dữ liệu lớn hơn nhiều. c) Khi hai tác vụ hoàn toàn không liên quan đến nhau. d) Khi bạn không có GPU.
    
23. **Trong Transfer Learning, "fine-tuning" (tinh chỉnh) có nghĩa là gì?** a) Chỉ huấn luyện lớp đầu ra mới và giữ nguyên tất cả các lớp khác. b) Huấn luyện lại toàn bộ mạng với tốc độ học rất lớn. c) "Rã đông" (unfreeze) một vài lớp cuối của mô hình đã được huấn luyện trước và tiếp tục huấn luyện chúng với tốc độ học nhỏ trên dữ liệu mới. d) Thay đổi kiến trúc của mô hình.
    
24. **"Data Augmentation" (Tăng cường dữ liệu) được sử dụng để làm gì?** a) Để giảm số lượng dữ liệu huấn luyện. b) Để tăng tốc độ huấn luyện. c) Để tạo ra các mẫu dữ liệu huấn luyện mới một cách nhân tạo, giúp mô hình khái quát hóa tốt hơn và giảm overfitting. d) Để gán nhãn cho dữ liệu.
    
25. **Đâu là một kỹ thuật Data Augmentation phổ biến cho dữ liệu hình ảnh?** a) Lật ảnh theo chiều ngang (Mirroring). b) Cắt xén ngẫu nhiên (Random Cropping). c) Thay đổi màu sắc (Color shifting). d) Tất cả các câu trên.
    
26. **"Ensembling" là kỹ thuật gì để cải thiện hiệu suất?** a) Sử dụng một mô hình duy nhất nhưng rất sâu. b) Huấn luyện nhiều mô hình độc lập và lấy trung bình kết quả dự đoán của chúng. c) Tăng cường dữ liệu huấn luyện. d) Sử dụng một thuật toán tối ưu hóa khác.
    
27. **"Multi-crop at test time" là gì?** a) Áp dụng data augmentation cho tập test (ví dụ: tạo nhiều phiên bản cắt xén của ảnh test) và lấy trung bình dự đoán để có kết quả cuối cùng ổn định hơn. b) Chỉ huấn luyện mô hình trên các ảnh đã được cắt xén. c) Cắt bỏ các phần không quan trọng của ảnh test. d) Sử dụng nhiều tập test khác nhau.
    
28. **Khi bạn có một tập dữ liệu rất nhỏ cho tác vụ của mình, chiến lược nào sau đây là hiệu quả nhất?** a) Huấn luyện một mạng rất lớn từ đầu. b) Sử dụng Transfer Learning từ một mô hình đã được huấn luyện trước (pre-trained model). c) Chỉ sử dụng các mô hình tuyến tính. d) Không sử dụng lớp ẩn nào.
    
29. **Tại sao Data Augmentation lại giúp chống overfitting?** a) Vì nó làm cho mô hình trở nên phức tạp hơn. b) Vì nó làm cho tập dữ liệu huấn luyện trở nên đa dạng hơn, buộc mô hình phải học các đặc trưng bất biến và khái quát hơn. c) Vì nó giảm số lượng tham số. d) Vì nó làm giảm tốc độ học.
    
30. **Khi thực hiện Transfer Learning, bạn thường thay thế phần nào của mạng đã được huấn luyện trước?** a) Các lớp tích chập đầu tiên. b) Lớp đầu ra (ví dụ: lớp Softmax). c) Các lớp pooling. d) Tất cả các lớp.
    

#### Phần 4: Câu hỏi lý thuyết bổ sung

31. **Tại sao việc nghiên cứu các "case studies" (các kiến trúc đã thành công) lại quan trọng?** a) Để sao chép y hệt code của người khác. b) Để có được những ý tưởng và trực giác về cách kết hợp các khối xây dựng (CONV, POOL, FC) một cách hiệu quả. c) Vì không có cách nào khác để xây dựng một mạng nơ-ron. d) Chỉ để biết về lịch sử của học sâu.
    
32. **Đặc điểm chung của các kiến trúc CNN hiện đại (VGG, ResNet, Inception) là gì?** a) Chúng rất nông. b) Chúng có xu hướng ngày càng sâu hơn. c) Chúng không sử dụng lớp fully-connected. d) Chúng chỉ hoạt động trên ảnh xám.
    
33. **Trong một khối residual, nếu kích thước của đầu vào và đầu ra khác nhau, bạn cần làm gì với kết nối tắt?** a) Không thể sử dụng kết nối tắt. b) Thêm một lớp tích chập 1x1 (hoặc một phép chiếu tuyến tính) vào kết nối tắt để làm cho kích thước khớp nhau. c) Thêm padding vào đầu vào. d) Sử dụng Average Pooling.
    
34. **Trong MobileNet, "pointwise convolution" thực chất là loại tích chập nào?** a) Tích chập 3x3. b) Tích chập 5x5. c) Tích chập 1x1. d) Max Pooling.
    
35. **"Depthwise convolution" khác với tích chập tiêu chuẩn như thế nào?** a) Nó áp dụng một bộ lọc duy nhất cho tất cả các kênh đầu vào. b) Nó áp dụng một bộ lọc riêng cho từng kênh đầu vào một cách độc lập. c) Nó không có trọng số. d) Nó chỉ hoạt động trên dữ liệu 1D.
    
36. **Trong các tác vụ Thị giác máy tính (Computer Vision), nguồn kiến thức của một thuật toán học máy đến từ đâu?** a) Chỉ từ dữ liệu được gán nhãn. b) Chỉ từ các đặc trưng được thiết kế thủ công. c) Cả từ dữ liệu được gán nhãn và từ các kiến trúc/thành phần được thiết kế thủ công. d) Từ các siêu tham số.
    
37. **Khi lượng dữ liệu có sẵn rất lớn, xu hướng trong thiết kế mô hình là gì?** a) Dựa nhiều hơn vào các đặc trưng được thiết kế thủ công. b) Sử dụng các kiến trúc đơn giản hơn và để "dữ liệu tự lên tiếng". c) Sử dụng các mô hình nhỏ hơn. d) Giảm số lượng lớp.
    
38. **Đâu là một lý do khiến MobileNet hiệu quả hơn về mặt tính toán so với một CNN tiêu chuẩn?** a) Nó sâu hơn. b) Tích chập tách biệt theo chiều sâu tách một phép tích chập lớn thành hai phép tích chập nhỏ hơn, làm giảm đáng kể tổng số phép tính. c) Nó sử dụng nhiều lớp fully-connected hơn. d) Nó không sử dụng hàm kích hoạt.
    
39. **Kiến trúc nào giới thiệu khái niệm "bottleneck layer" sử dụng tích chập 1x1 để giảm chiều dữ liệu trước khi thực hiện các phép tích chập tốn kém hơn?** a) LeNet-5 b) AlexNet c) Inception d) VGG
    
40. **"Fine-tuning" một mô hình thường hiệu quả hơn huấn luyện từ đầu khi nào?** a) Khi bạn có một tập dữ liệu cực lớn. b) Khi bạn có một tập dữ liệu nhỏ và tác vụ của bạn tương tự như tác vụ mà mô hình đã được huấn luyện trước đó. c) Khi bạn có rất nhiều tài nguyên tính toán. d) Khi bạn muốn tạo ra một kiến trúc hoàn toàn mới.
    
41. **Trong kiến trúc ResNet, hàm kích hoạt ReLU thường được đặt ở đâu trong một khối residual?** a) Chỉ ở đầu khối. b) Chỉ ở cuối khối. c) Sau mỗi lớp tích chập và sau phép cộng của kết nối tắt. d) Không sử dụng ReLU.
    
42. **Tại sao các mô hình CNN hiện đại thường loại bỏ hoặc giảm thiểu số lượng các lớp fully-connected lớn ở cuối?** a) Vì các lớp FC không thể học được gì. b) Vì các lớp FC chứa một lượng lớn tham số, dễ gây overfitting và làm tăng kích thước mô hình. c) Vì các lớp CONV có thể thực hiện việc phân loại. d) Vì các lớp FC quá nhanh.
    
43. **Đâu là một ví dụ về việc "cross-fertilizing" ý tưởng trong học sâu?** a) Chỉ sử dụng các ý tưởng từ lĩnh vực thị giác máy tính cho các bài toán thị giác máy tính. b) Áp dụng các ý tưởng từ kiến trúc CNN (như ResNet) cho các mô hình trong xử lý ngôn ngữ tự nhiên (như Transformer). c) Chỉ sử dụng một kiến trúc duy nhất cho mọi bài toán. d) Luôn huấn luyện mô hình từ đầu.
    
44. **Khi thực hiện data augmentation, điều quan trọng cần đảm bảo là gì?** a) Các phép biến đổi phải làm thay đổi hoàn toàn đối tượng trong ảnh. b) Các phép biến đổi phải giữ nguyên nhãn của ảnh (ví dụ: lật ảnh một con mèo vẫn phải là một con mèo). c) Chỉ áp dụng một loại biến đổi duy nhất. d) Áp dụng các phép biến đổi cho cả tập train và tập test.
    
45. **Trong MobileNetV2, lớp "expansion" có vai trò gì?** a) Giảm số lượng kênh. b) Tăng số lượng kênh bằng tích chập 1x1 trước khi thực hiện depthwise convolution. c) Thực hiện max pooling. d) Thay thế hàm kích hoạt.
    
46. **Đâu là một thách thức khi so sánh hiệu suất của các kiến trúc CNN khác nhau?** a) Số lượng tham số. b) Tốc độ suy luận (inference speed). c) Độ chính xác trên một tập dữ liệu chuẩn. d) Tất cả các yếu tố trên đều cần được xem xét.
    
47. **Tên gọi "Inception" được lấy cảm hứng từ đâu?** a) Tên của nhà khoa học đã phát minh ra nó. b) Một bộ phim khoa học viễn tưởng. c) Một thuật ngữ toán học. d) Tên của một công ty.
    
48. **Việc sử dụng các mô hình đã được huấn luyện trước (pre-trained models) từ các kho mã nguồn mở có lợi ích gì?** a) Tiết kiệm thời gian và tài nguyên tính toán. b) Tận dụng được các kiến trúc đã được chứng minh là hiệu quả. c) Cung cấp một điểm khởi đầu tốt cho các tác vụ với dữ liệu hạn chế. d) Tất cả các câu trên.
    
49. **Kiến trúc nào sau đây không sử dụng kết nối tắt (skip connection)?** a) ResNet b) MobileNetV2 c) VGG-16 d) EfficientNet
    
50. **Xu hướng chung trong các kiến trúc CNN từ LeNet đến EfficientNet là gì?** a) Mạng ngày càng nông và rộng hơn. b) Mạng ngày càng sâu hơn, phức tạp hơn nhưng cũng hiệu quả hơn về mặt tính toán. c) Mạng ngày càng có nhiều lớp fully-connected hơn. d) Mạng ngày càng ít sử dụng các lớp tích chập hơn.
    

### **Đáp án**

<details> <summary>Nhấn vào đây để xem đáp án</summary>

1. b | 2. c | 3. c | 4. d | 5. b
    
2. c | 7. c | 8. b | 9. b | 10. b
    
3. b | 12. b | 13. b | 14. b | 15. c
    
4. b | 17. b | 18. a | 19. b | 20. c
    
5. b | 22. c | 23. c | 24. c | 25. d
    
6. b | 27. a | 28. b | 29. c | 30. b
    
7. b | 32. b | 33. b | 34. c | 35. b
    
8. c | 37. b | 38. b | 39. c | 40. b
    
9. c | 42. b | 43. b | 44. b | 45. b
    
10. d | 47. b | 48. d | 49. c | 50. b
    

</details>

### Bài kiểm tra trắc nghiệm: Các ứng dụng CNN Nâng cao

**Chọn câu trả lời đúng nhất cho mỗi câu hỏi.**

#### Phần 1: Các khái niệm cơ bản về Phát hiện Vật thể (Object Detection)

1. **Sự khác biệt chính giữa "Image Classification" và "Classification with Localization" là gì?** a) Classification chỉ cho biết có đối tượng hay không, còn Localization cho biết có bao nhiêu đối tượng. b) Classification chỉ dự đoán lớp của đối tượng, còn Localization còn dự đoán thêm một hộp giới hạn (bounding box) xung quanh đối tượng. c) Localization nhanh hơn Classification. d) Chúng là hai tên gọi khác nhau cho cùng một bài toán.
    
2. **Một hộp giới hạn (bounding box) thường được tham số hóa bởi những giá trị nào?** a) Tọa độ góc trên bên trái (x1, y1) và góc dưới bên phải (x2, y2). b) Tọa độ điểm trung tâm (bx, by), chiều cao (bh), và chiều rộng (bw). c) Chỉ chiều cao và chiều rộng. d) Tên của đối tượng bên trong hộp.
    
3. **"Landmark detection" (Phát hiện điểm mốc) là bài toán gì?** a) Phát hiện các địa danh nổi tiếng trong ảnh. b) Xác định các điểm chính, quan trọng trên một đối tượng (ví dụ: các góc mắt, chóp mũi trên khuôn mặt). c) Vẽ một hộp giới hạn xung quanh đối tượng. d) Phân loại đối tượng.
    
4. **Thuật toán "Sliding Windows Detection" hoạt động như thế nào?** a) Phóng to các cửa sổ trong ảnh để xem chi tiết. b) Trượt một cửa sổ (vùng chữ nhật) qua toàn bộ ảnh và dùng một bộ phân loại để xác định xem có đối tượng trong cửa sổ đó không. c) Chỉ nhìn vào trung tâm của ảnh. d) Chia ảnh thành các vùng ngẫu nhiên.
    
5. **Nhược điểm chính của thuật toán Sliding Windows truyền thống là gì?** a) Độ chính xác thấp. b) Chi phí tính toán rất cao do phải chạy bộ phân loại trên rất nhiều cửa sổ. c) Chỉ hoạt động với ảnh xám. d) Không thể phát hiện các đối tượng nhỏ.
    
6. **Làm thế nào để biến một lớp Fully Connected (FC) thành một lớp Tích chập (CONV)?** a) Không thể làm được. b) Bằng cách sử dụng một bộ lọc có cùng kích thước với đầu vào của lớp FC đó (ví dụ: đầu vào 5x5x16 thì dùng bộ lọc 5x5x16). c) Bằng cách sử dụng một bộ lọc 1x1. d) Bằng cách thêm một lớp pooling.
    
7. **Ưu điểm của việc triển khai Sliding Windows bằng phép tích chập là gì?** a) Tăng độ chính xác của hộp giới hạn. b) Cho phép chia sẻ một lượng lớn các phép tính giữa các cửa sổ chồng chéo, giúp tăng tốc độ đáng kể. c) Giảm số lượng lớp trong mạng. d) Không cần dữ liệu huấn luyện.
    
8. **"Intersection over Union" (IoU) được sử dụng để làm gì?** a) Để đo lường tốc độ của thuật toán. b) Để đo lường mức độ chồng chéo giữa hai hộp giới hạn (thường là hộp dự đoán và hộp thực tế). c) Để tính toán hàm chi phí. d) Để chọn kích thước của anchor box.
    
9. **Nếu IoU giữa hộp dự đoán và hộp thực tế là 0.9, điều đó có nghĩa là gì?** a) Hai hộp hầu như không chồng lên nhau. b) Hộp dự đoán hoàn toàn sai. c) Hộp dự đoán có độ trùng khớp rất cao với hộp thực tế. d) Không thể kết luận.
    
10. **Mục đích của "Non-max Suppression" (NMS) là gì?** a) Để tăng số lượng hộp giới hạn được dự đoán. b) Để loại bỏ các hộp giới hạn dư thừa, chồng chéo cho cùng một đối tượng và chỉ giữ lại hộp tốt nhất. c) Để tăng tốc độ lan truyền ngược. d) Để chọn ra các đặc trưng quan trọng nhất.
    

#### Phần 2: Các thuật toán (YOLO, U-Net)

11. **YOLO là viết tắt của cụm từ gì?** a) You Only Learn Once b) You Only Look Once c) You Observe Local Objects d) You Omit Lots of Objects
    
12. **Ý tưởng cốt lõi của thuật toán YOLO là gì?** a) Chia ảnh thành một lưới (grid), và mỗi ô lưới (grid cell) chịu trách nhiệm dự đoán đối tượng có tâm nằm trong ô đó. b) Chạy thuật toán sliding windows trên toàn bộ ảnh. c) Chỉ nhìn vào các góc của ảnh. d) Sử dụng nhiều mạng nơ-ron khác nhau cho mỗi đối tượng.
    
13. **"Anchor boxes" được sử dụng để giải quyết vấn đề gì trong YOLO?** a) Giúp mỗi ô lưới có thể phát hiện nhiều đối tượng có hình dạng khác nhau và chồng chéo lên nhau. b) Giảm chi phí tính toán. c) Cố định kích thước của các hộp giới hạn. d) Tăng số lượng lớp trong mạng.
    
14. **Trong YOLO, nếu một đối tượng có tâm nằm trong ô lưới (i, j), ô lưới nào sẽ chịu trách nhiệm dự đoán đối tượng đó?** a) Tất cả các ô lưới. b) Chỉ ô lưới (i, j). c) Các ô lưới lân cận của (i, j). d) Một ô lưới được chọn ngẫu nhiên.
    
15. **Đâu không phải là một thành phần trong vector đầu ra của một ô lưới trong YOLO?** a) `Pc` (xác suất có đối tượng). b) `bx, by, bh, bw` (tọa độ hộp giới hạn). c) `c1, c2, c3,...` (xác suất các lớp). d) `IoU` (giá trị Intersection over Union).
    
16. **"Semantic Segmentation" (Phân đoạn theo ngữ nghĩa) khác với Object Detection như thế nào?** a) Semantic Segmentation nhanh hơn. b) Semantic Segmentation chỉ hoạt động với ảnh y tế. c) Thay vì chỉ vẽ một hộp giới hạn, Semantic Segmentation phân loại cho từng pixel trong ảnh. d) Object Detection chính xác hơn.
    
17. **Kiến trúc U-Net được đặt tên như vậy vì lý do gì?** a) Nó được phát minh bởi một người tên U. b) Sơ đồ kiến trúc của nó có hình dạng giống chữ U. c) Nó là viết tắt của "Ultimate Network". d) Nó chỉ có thể phân loại chữ U.
    
18. **Thành phần nào trong U-Net được sử dụng để tăng kích thước (upsample) của bản đồ đặc trưng ở nhánh giải mã (decoder)?** a) Max Pooling b) Tích chập chuyển vị (Transpose Convolution). c) Lớp Fully Connected. d) Anchor Box.
    
19. **Các "skip connections" trong kiến trúc U-Net có vai trò gì?** a) Để làm cho mạng sâu hơn. b) Để kết hợp thông tin đặc trưng chi tiết từ nhánh mã hóa (encoder) với thông tin ngữ cảnh từ nhánh giải mã, giúp việc định vị chính xác hơn. c) Để giảm số lượng tham số. d) Để tăng tốc độ huấn luyện.
    
20. **Đâu là một ứng dụng phổ biến của U-Net?** a) Dịch máy. b) Phân đoạn ảnh y tế (ví dụ: xác định khối u). c) Nhận dạng giọng nói. d) Dự báo giá cổ phiếu.
    

#### Phần 3: Nhận dạng Khuôn mặt (Face Recognition)

21. **Sự khác biệt giữa "Face Verification" (Xác minh khuôn mặt) và "Face Recognition" (Nhận dạng khuôn mặt) là gì?** a) Verification là bài toán 1:1 ("Đây có phải là người X không?"), còn Recognition là bài toán 1:N ("Đây là ai trong số N người?"). b) Recognition là bài toán 1:1, còn Verification là bài toán 1:N. c) Chúng là hai tên gọi cho cùng một bài toán. d) Verification chỉ hoạt động với ảnh tĩnh, Recognition hoạt động với video.
    
22. **"One-shot learning" trong nhận dạng khuôn mặt là vấn đề gì?** a) Chỉ cần một lần lặp để huấn luyện mô hình. b) Mô hình phải có khả năng nhận dạng một người chỉ từ một hình ảnh duy nhất của người đó. c) Chỉ có một người trong cơ sở dữ liệu. d) Mô hình chỉ đưa ra một dự đoán duy nhất.
    
23. **Tại sao việc huấn luyện một mạng Softmax tiêu chuẩn không hiệu quả cho bài toán one-shot learning?** a) Vì Softmax không thể xử lý ảnh. b) Vì tập huấn luyện cho mỗi người quá nhỏ (chỉ 1 ảnh) và việc thêm người mới đòi hỏi phải huấn luyện lại toàn bộ mạng. c) Vì Softmax quá chậm. d) Vì Softmax chỉ hoạt động với bài toán nhị phân.
    
24. **Kiến trúc Siamese Network hoạt động dựa trên nguyên tắc nào?** a) Sử dụng hai mạng nơ-ron giống hệt nhau để học một hàm "đo độ tương tự" (similarity function) giữa hai ảnh đầu vào. b) Sử dụng một mạng duy nhất để phân loại nhiều người. c) Kết hợp nhiều mô hình khác nhau. d) Chỉ sử dụng các lớp fully-connected.
    
25. **Mục tiêu của việc huấn luyện Siamese Network là gì?** a) Tối đa hóa khoảng cách giữa các embedding của cùng một người. b) Tối thiểu hóa khoảng cách giữa các embedding của những người khác nhau. c) Học một hàm embedding sao cho khoảng cách giữa các ảnh của cùng một người thì nhỏ, và khoảng cách giữa các ảnh của những người khác nhau thì lớn. d) Phân loại ảnh thành các nhóm.
    
26. **Hàm mất mát Triplet Loss yêu cầu một bộ ba (triplet) gồm những ảnh nào?** a) Ba ảnh của cùng một người. b) Ba ảnh của ba người khác nhau. c) Một ảnh mỏ neo (Anchor), một ảnh dương tính (Positive - cùng người với anchor), và một ảnh âm tính (Negative - khác người với anchor). d) Một ảnh gốc, một ảnh đã qua augmentation, và một ảnh nhiễu.
    
27. **Công thức của Triplet Loss, `max(||f(A)-f(P)||² - ||f(A)-f(N)||² + α, 0)`, nhằm mục đích gì?** a) Đảm bảo khoảng cách từ Anchor đến Negative lớn hơn khoảng cách từ Anchor đến Positive ít nhất một khoảng `α`. b) Đảm bảo khoảng cách từ Anchor đến Positive lớn hơn khoảng cách từ Anchor đến Negative. c) Làm cho tất cả các khoảng cách bằng nhau. d) Tối đa hóa tổng các khoảng cách.
    
28. **Tham số `α` (alpha) trong Triplet Loss được gọi là gì?** a) Tốc độ học. b) Tham số điều chuẩn hóa. c) Lề (Margin). d) Ngưỡng (Threshold).
    
29. **Tại sao việc chọn các "hard triplets" lại quan trọng trong quá trình huấn luyện?** a) Vì chúng dễ học nhất. b) Vì việc học trên các triplet quá dễ không giúp mô hình cải thiện, nên cần chọn các triplet mà mô hình dễ bị nhầm lẫn để tập trung học. c) Để làm cho quá trình huấn luyện chậm lại. d) Vì chúng chiếm phần lớn trong tập dữ liệu.
    
30. **Một cách tiếp cận khác để giải quyết bài toán Face Verification là coi nó như một bài toán:** a) Hồi quy. b) Phân loại nhị phân (dự đoán 2 ảnh có phải cùng một người hay không). c) Phân cụm. d) One-shot learning.
    

#### Phần 4: Chuyển đổi Phong cách và Các khái niệm khác

31. **"Neural Style Transfer" (Chuyển đổi phong cách bằng mạng nơ-ron) là kỹ thuật gì?** a) Sao chép phong cách của một người và áp dụng cho người khác. b) Kết hợp "nội dung" của một ảnh với "phong cách" của một ảnh khác để tạo ra một ảnh mới. c) Chuyển đổi một mạng nơ-ron từ TensorFlow sang PyTorch. d) Dạy cho mạng nơ-ron vẽ tranh.
    
32. **Trong Neural Style Transfer, hàm chi phí tổng hợp `J(G)` bao gồm hai thành phần nào?** a) Chi phí huấn luyện và chi phí kiểm thử. b) Chi phí nội dung (Content cost) và Chi phí phong cách (Style cost). c) Chi phí L1 và chi phí L2. d) Chi phí của ảnh gốc và chi phí của ảnh phong cách.
    
33. **Chi phí nội dung `J_content(C, G)` được tính như thế nào?** a) Bằng cách so sánh trực tiếp các pixel của ảnh nội dung (C) và ảnh được tạo ra (G). b) Bằng cách so sánh các kích hoạt của một lớp ẩn sâu trong một mạng CNN đã được huấn luyện trước cho cả hai ảnh C và G. c) Bằng cách đo độ tương phản của hai ảnh. d) Bằng cách so sánh biểu đồ màu của hai ảnh.
    
34. **Tại sao lại sử dụng một lớp ẩn sâu để đo lường "nội dung"?** a) Vì các lớp sâu nắm bắt được các đặc trưng ngữ nghĩa, cấp cao của đối tượng trong ảnh. b) Vì các lớp nông tính toán nhanh hơn. c) Vì các lớp sâu có ít nơ-ron hơn. d) Đây là một lựa chọn ngẫu nhiên.
    
35. **"Phong cách" của một ảnh trong Neural Style Transfer được định nghĩa là gì?** a) Bảng màu được sử dụng trong ảnh. b) Mức độ tương quan giữa các kích hoạt trên các kênh khác nhau trong một lớp của CNN. c) Các đối tượng có trong ảnh. d) Độ phân giải của ảnh.
    
36. **Ma trận phong cách (Style Matrix), hay ma trận Gram, đo lường điều gì?** a) Giá trị trung bình của các kích hoạt. b) Mức độ mà các đặc trưng cấp thấp (như màu sắc, hoa văn) có xu hướng xuất hiện cùng nhau. c) Kích thước của ảnh. d) Số lượng đối tượng trong ảnh.
    
37. **Tại sao lại sử dụng nhiều lớp (cả nông và sâu) để tính toán chi phí phong cách?** a) Để làm cho việc tính toán phức tạp hơn. b) Để nắm bắt được các đặc trưng phong cách ở nhiều quy mô khác nhau, từ các hoa văn nhỏ đến các cấu trúc lớn hơn. c) Vì không thể sử dụng một lớp duy nhất. d) Để giảm thời gian huấn luyện.
    
38. **Quá trình tạo ra ảnh trong Neural Style Transfer hoạt động như thế nào?** a) Huấn luyện một mạng nơ-ron mới từ đầu. b) Bắt đầu với một ảnh nhiễu ngẫu nhiên và sử dụng Gradient Descent để cập nhật các pixel của ảnh đó nhằm tối thiểu hóa hàm chi phí tổng hợp. c) Trộn lẫn các pixel của ảnh nội dung và ảnh phong cách. d) Tìm một ảnh tương tự trên internet.
    
39. **Mạng nơ-ron tích chập có thể được tổng quát hóa cho dữ liệu 1D không?** a) Không, nó chỉ hoạt động với dữ liệu 2D (ảnh). b) Có, bằng cách sử dụng các bộ lọc 1D, nó có thể được áp dụng cho dữ liệu chuỗi thời gian hoặc văn bản. c) Chỉ có thể tổng quát hóa cho dữ liệu 3D. d) Chỉ khi dữ liệu 1D được chuyển đổi thành ảnh.
    
40. **Đâu là một ví dụ về dữ liệu 3D mà CNN có thể được áp dụng?** a) Một đoạn văn bản. b) Dữ liệu quét y tế (như CT scan) hoặc video. c) Một tín hiệu âm thanh. d) Một bức ảnh đen trắng.
    
41. **Trong thuật toán YOLO, nếu hai anchor box khác nhau trong cùng một ô lưới đều có IoU cao với cùng một đối tượng, đối tượng đó sẽ được gán cho anchor box nào?** a) Cả hai. b) Anchor box có IoU cao hơn. c) Một anchor box được chọn ngẫu nhiên. d) Không gán cho cái nào.
    
42. **Trong Non-max Suppression, nếu hai hộp giới hạn có IoU cao hơn một ngưỡng nhất định, hộp nào sẽ bị loại bỏ?** a) Hộp có xác suất `Pc` cao hơn. b) Hộp có xác suất `Pc` thấp hơn. c) Cả hai. d) Hộp có kích thước lớn hơn.
    
43. **"Face encoding" hay "face embedding" là gì?** a) Là ảnh gốc của khuôn mặt. b) Là một vector số (thường là 128 chiều) biểu diễn các đặc trưng của một khuôn mặt, được tạo ra bởi một mạng nơ-ron. c) Là tên của người đó. d) Là một hộp giới hạn quanh khuôn mặt.
    
44. **Thuật toán R-CNN (Regions with CNN) hoạt động như thế nào?** a) Chạy một mạng CNN trên toàn bộ ảnh một lần. b) Đầu tiên đề xuất các "vùng có khả năng chứa đối tượng", sau đó chạy một bộ phân loại CNN trên từng vùng đó. c) Chia ảnh thành một lưới cố định. d) Chỉ phân đoạn ảnh.
    
45. **Tại sao các thuật toán như Fast R-CNN và Faster R-CNN lại nhanh hơn R-CNN?** a) Vì chúng sử dụng mạng nông hơn. b) Vì chúng sử dụng các kỹ thuật tích chập để chia sẻ tính toán giữa các vùng đề xuất, thay vì chạy CNN trên từng vùng một cách độc lập. c) Vì chúng sử dụng ít dữ liệu hơn. d) Vì chúng không cần gán nhãn dữ liệu.
    
46. **Trong Neural Style Transfer, chúng ta tối ưu hóa cái gì?** a) Các trọng số của mạng nơ-ron. b) Các siêu tham số. c) Các pixel của ảnh được tạo ra (G). d) Các pixel của ảnh nội dung (C).
    
47. **Để huấn luyện một hệ thống nhận dạng khuôn mặt, bạn cần một tập dữ liệu như thế nào?** a) Một vài ảnh của một người duy nhất. b) Nhiều ảnh của nhiều người khác nhau. c) Chỉ cần các ảnh không có khuôn mặt. d) Các ảnh đã được chuyển đổi phong cách.
    
48. **Đâu là một thách thức của bài toán "one-shot learning"?** a) Mô hình rất dễ bị overfitting vào một ví dụ duy nhất. b) Cần rất nhiều dữ liệu. c) Thời gian huấn luyện rất lâu. d) Không thể sử dụng GPU.
    
49. **Trong U-Net, nhánh bên trái (nhánh đi xuống) có vai trò gì?** a) Tăng kích thước ảnh. b) Hoạt động như một bộ mã hóa (encoder), trích xuất các đặc trưng ngữ nghĩa và giảm kích thước không gian. c) Phân loại các pixel. d) Chỉ để sao chép dữ liệu.
    
50. **Đâu là một ứng dụng mà CNN 1D có thể hữu ích?** a) Phân tích tín hiệu EKG (điện tâm đồ). b) Phân loại văn bản. c) Nhận dạng giọng nói. d) Tất cả các câu trên.
    

### **Đáp án**

<details> <summary>Nhấn vào đây để xem đáp án</summary>

1. b | 2. b | 3. b | 4. b | 5. b
    
2. b | 7. b | 8. b | 9. c | 10. b
    
3. b | 12. a | 13. a | 14. b | 15. d
    
4. c | 17. b | 18. b | 19. b | 20. b
    
5. a | 22. b | 23. b | 24. a | 25. c
    
6. c | 27. a | 28. c | 29. b | 30. b
    
7. b | 32. b | 33. b | 34. a | 35. b
    
8. b | 37. b | 38. b | 39. b | 40. b
    
9. b | 42. b | 43. b | 44. b | 45. b
    
10. c | 47. b | 48. a | 49. b | 50. d
    

</details>

### Bài kiểm tra trắc nghiệm: Mạng Nơ-ron Hồi quy (RNN)

**Chọn câu trả lời đúng nhất cho mỗi câu hỏi.**

#### Phần 1: Các khái niệm cơ bản về Mô hình Chuỗi và RNN

1. **Tại sao các mạng nơ-ron tiêu chuẩn (không phải RNN) không phù hợp cho các bài toán xử lý chuỗi (sequence tasks)?** a) Vì chúng không thể xử lý các đầu vào và đầu ra có độ dài thay đổi. b) Vì chúng không chia sẻ các đặc trưng đã học được qua các vị trí khác nhau trong chuỗi. c) Cả A và B đều đúng. d) Vì chúng quá chậm.
    
2. **Trong ký hiệu của mô hình chuỗi, `x<t>` đại diện cho điều gì?** a) Toàn bộ chuỗi đầu vào. b) Đầu vào tại bước thời gian (time step) thứ `t`. c) Mẫu dữ liệu huấn luyện thứ `t`. d) Lớp thứ `t` của mạng.
    
3. **Đặc điểm kiến trúc cốt lõi của một Mạng Nơ-ron Hồi quy (RNN) là gì?** a) Nó có nhiều lớp ẩn hơn các mạng khác. b) Nó có một vòng lặp, cho phép thông tin (trạng thái kích hoạt) từ bước thời gian trước được truyền đến bước thời gian hiện tại. c) Nó chỉ sử dụng hàm kích hoạt tuyến tính. d) Nó không có tham số trọng số.
    
4. **Trong một RNN cơ bản, các tham số trọng số (`W_aa`, `W_ax`, `W_ya`) có đặc điểm gì?** a) Chúng thay đổi ở mỗi bước thời gian. b) Chúng được chia sẻ (sử dụng chung) qua tất cả các bước thời gian. c) Chúng chỉ được sử dụng ở bước thời gian cuối cùng. d) Chúng được khởi tạo bằng 0.
    
5. **Trong bài toán Nhận dạng Thực thể có tên (Named-Entity Recognition), nếu đầu vào và đầu ra đều có cùng độ dài (`Tx = Ty`), đây là loại kiến trúc RNN nào?** a) Many-to-one b) One-to-many c) Many-to-many d) One-to-one
    
6. **Phân tích cảm xúc (sentiment classification) của một câu văn (ví dụ: đánh giá phim) là một ví dụ của loại kiến trúc RNN nào?** a) Many-to-one b) One-to-many c) Many-to-many (`Tx = Ty`) d) Many-to-many (`Tx != Ty`)
    
7. **Tạo ra một bản nhạc (music generation) từ một nốt nhạc đầu vào là một ví dụ của loại kiến trúc RNN nào?** a) Many-to-one b) One-to-many c) Many-to-many d) One-to-one
    
8. **Trong công thức tính kích hoạt của RNN, `a<t> = g(W_aa * a<t-1> + W_ax * x<t> + b_a)`, thành phần `a<t-1>` đại diện cho điều gì?** a) Đầu vào hiện tại. b) "Bộ nhớ" hay thông tin từ bước thời gian trước đó. c) Dự đoán của bước thời gian trước. d) Nhãn đúng của bước thời gian trước.
    
9. **Để biểu diễn một từ trong một câu cho máy tính, phương pháp phổ biến là gì?** a) Sử dụng chính chuỗi ký tự đó. b) Sử dụng một số nguyên duy nhất. c) Sử dụng mã hóa one-hot dựa trên một bộ từ điển (vocabulary). d) Sử dụng mã ASCII của từ đó.
    
10. **Token `<UNK>` được sử dụng để làm gì trong mô hình ngôn ngữ?** a) Để biểu thị sự kết thúc của một câu. b) Để biểu thị một từ không có trong từ điển. c) Để biểu thị một từ là tên riêng. d) Để bắt đầu một câu mới.
    

#### Phần 2: Huấn luyện RNN và các Biến thể

11. **Thuật toán được sử dụng để huấn luyện RNN được gọi là gì?** a) Gradient Descent b) Adam c) Backpropagation d) Backpropagation Through Time (BPTT)
    
12. **Tại sao thuật toán huấn luyện RNN lại có tên "Through Time" (Xuyên thời gian)?** a) Vì nó mất rất nhiều thời gian để huấn luyện. b) Vì quá trình lan truyền ngược lỗi diễn ra từ bước thời gian cuối cùng ngược về các bước thời gian đầu tiên. c) Vì nó có thể dự đoán tương lai. d) Vì nó chỉ hoạt động với dữ liệu chuỗi thời gian.
    
13. **Mục tiêu của một mô hình ngôn ngữ (language model) là gì?** a) Dịch một câu từ ngôn ngữ này sang ngôn ngữ khác. b) Đếm số từ trong một câu. c) Ước tính xác suất của một chuỗi các từ. d) Phân loại cảm xúc của một câu.
    
14. **Khi tạo ra một chuỗi mới (ví dụ: văn bản) bằng RNN, đầu vào cho bước thời gian `t` là gì?** a) Một từ được chọn ngẫu nhiên từ từ điển. b) Đầu ra (từ được dự đoán) của bước thời gian `t-1`. c) Luôn là một vector zero. d) Toàn bộ câu đã được tạo ra trước đó.
    
15. **Sự khác biệt chính giữa mô hình ngôn ngữ cấp độ từ (word-level) và cấp độ ký tự (character-level) là gì?** a) Mô hình cấp độ ký tự không bao giờ gặp phải từ không xác định (`<UNK>`). b) Mô hình cấp độ từ thường tạo ra các chuỗi dài hơn. c) Mô hình cấp độ ký tự yêu cầu một từ điển lớn hơn. d) Mô hình cấp độ từ luôn chính xác hơn.
    
16. **Trong BPTT, hàm chi phí tổng hợp (`L`) cho toàn bộ chuỗi được tính như thế nào?** a) Là giá trị chi phí ở bước thời gian cuối cùng. b) Là giá trị chi phí trung bình của tất cả các bước thời gian. c) Là tổng của các hàm chi phí tại mỗi bước thời gian. d) Là giá trị chi phí lớn nhất trong tất cả các bước thời gian.
    
17. **Trong một RNN cơ bản, dự đoán `ŷ<t>` tại một bước thời gian phụ thuộc vào những thông tin nào?** a) Chỉ đầu vào `x<t>`. b) Chỉ kích hoạt `a<t-1>`. c) Cả đầu vào `x<t>` và tất cả các đầu vào trước đó (`x<1>`, ..., `x<t-1>`) thông qua `a<t-1>`. d) Chỉ các đầu vào trong tương lai.
    
18. **Dịch máy từ một câu có độ dài `Tx` sang một câu có độ dài `Ty` (với `Tx != Ty`) là một ví dụ của loại kiến trúc RNN nào?** a) Many-to-one b) One-to-many c) Many-to-many (`Tx = Ty`) d) Many-to-many (`Tx != Ty`), thường sử dụng kiến trúc Encoder-Decoder.
    
19. **Nhược điểm của mô hình ngôn ngữ cấp độ ký tự là gì?** a) Nó không thể học được cấu trúc ngữ pháp. b) Nó có xu hướng tạo ra các chuỗi rất dài và khó nắm bắt các phụ thuộc xa. c) Nó không thể xử lý dấu câu. d) Nó yêu cầu một GPU rất mạnh.
    
20. **Trong quá trình "sampling" một chuỗi mới, điều gì quyết định từ/ký tự nào sẽ được chọn ở mỗi bước?** a) Luôn chọn từ có xác suất cao nhất. b) Lấy mẫu từ phân phối xác suất được tạo ra bởi lớp softmax. c) Chọn một từ ngẫu nhiên. d) Cả A và B đều là các chiến lược có thể sử dụng.
    

#### Phần 3: Các Vấn đề và Giải pháp trong RNN (Gradients, GRU, LSTM)

21. **Vấn đề "Vanishing Gradients" (Gradient biến mất) trong RNN gây ra khó khăn gì?** a) Làm cho mô hình học quá nhanh. b) Khiến cho lỗi từ các bước thời gian sau khó lan truyền ngược lại để cập nhật các trọng số ở các bước thời gian đầu, làm cho RNN khó học các phụ thuộc xa (long-range dependencies). c) Gây ra hiện tượng overfitting. d) Chỉ xảy ra với các chuỗi ngắn.
    
22. **Vấn đề "Exploding Gradients" (Gradient bùng nổ) là gì?** a) Gradient trở nên rất nhỏ. b) Gradient trở nên cực kỳ lớn, gây ra các bước cập nhật không ổn định và dẫn đến giá trị `NaN`. c) Hàm chi phí không bao giờ giảm. d) Mô hình dự đoán cùng một giá trị cho mọi đầu vào.
    
23. **Kỹ thuật nào thường được sử dụng để giải quyết vấn đề Exploding Gradients?** a) Dropout b) Gradient Clipping (Xén Gradient). c) Batch Normalization d) Khởi tạo He.
    
24. **Mục đích chính của các đơn vị GRU (Gated Recurrent Unit) và LSTM (Long Short-Term Memory) là gì?** a) Để làm cho RNN chạy nhanh hơn. b) Để giải quyết vấn đề gradient biến mất và giúp RNN học các phụ thuộc xa tốt hơn. c) Để giảm số lượng tham số. d) Để chỉ hoạt động với dữ liệu hình ảnh.
    
25. **Thành phần nào trong GRU và LSTM hoạt động như một "bộ nhớ" để lưu trữ thông tin qua các bước thời gian?** a) Trạng thái kích hoạt (activation state) `a<t>`. b) Trạng thái ô nhớ (memory cell) `c<t>`. c) Các cổng (gates). d) Vector đầu vào `x<t>`.
    
26. **"Cổng" (gate) trong GRU/LSTM có vai trò gì?** a) Nó là một mạng nơ-ron nhỏ (thường có hàm kích hoạt sigmoid) quyết định lượng thông tin nào được phép đi qua. b) Nó là một hằng số cố định. c) Nó chỉ cho phép thông tin đi qua nếu giá trị lớn hơn 1. d) Nó chặn tất cả thông tin.
    
27. **GRU có bao nhiêu cổng?** a) 1 (Update gate) b) 2 (Update gate và Relevance gate) c) 3 (Update gate, Forget gate, và Output gate) d) 4
    
28. **LSTM có bao nhiêu cổng?** a) 1 b) 2 c) 3 (Update gate, Forget gate, và Output gate) d) 4
    
29. **Cổng nào trong LSTM có nhiệm vụ quyết định thông tin nào từ ô nhớ cũ (`c<t-1>`) cần được loại bỏ?** a) Update gate b) Relevance gate c) Output gate d) Forget gate
    
30. **So với LSTM, GRU có ưu điểm gì?** a) Nó luôn chính xác hơn. b) Nó có kiến trúc đơn giản hơn và ít tham số hơn, giúp tính toán nhanh hơn và dễ dàng xây dựng các mô hình lớn hơn. c) Nó có nhiều cổng hơn. d) Nó không bao giờ gặp vấn đề gradient biến mất.
    

#### Phần 4: Các Kiến trúc Nâng cao và Ứng dụng

31. **Tại sao một RNN đơn hướng (unidirectional) lại có hạn chế?** a) Vì nó không thể xử lý các chuỗi dài. b) Vì tại một bước thời gian `t`, dự đoán chỉ có thể sử dụng thông tin từ các bước trước đó (`1` đến `t-1`), không sử dụng được thông tin từ tương lai. c) Vì nó quá phức tạp. d) Vì nó chỉ có thể được huấn luyện bằng BPTT.
    
32. **Mạng RNN hai chiều (Bidirectional RNN - BRNN) giải quyết hạn chế của RNN đơn hướng bằng cách nào?** a) Bằng cách thêm nhiều lớp ẩn hơn. b) Bằng cách xử lý chuỗi theo cả hai hướng (từ trái sang phải và từ phải sang trái) và kết hợp kết quả. c) Bằng cách sử dụng một tốc độ học lớn hơn. d) Bằng cách loại bỏ các kết nối hồi quy.
    
33. **BRNN đặc biệt hữu ích cho các tác vụ nào?** a) Các tác vụ mà việc dự đoán tại một điểm cần ngữ cảnh từ cả quá khứ và tương lai, ví dụ như Named-Entity Recognition. b) Các tác vụ tạo văn bản thời gian thực. c) Các tác vụ có chuỗi đầu vào rất ngắn. d) Các tác vụ không yêu cầu bộ nhớ.
    
34. **Một nhược điểm của BRNN là gì?** a) Nó chậm hơn RNN đơn hướng. b) Nó yêu cầu toàn bộ chuỗi đầu vào phải có sẵn trước khi có thể đưa ra dự đoán. c) Nó có nhiều khả năng bị overfitting hơn. d) Nó khó triển khai hơn.
    
35. **Một Mạng RNN sâu (Deep RNN) được tạo ra bằng cách nào?** a) Tăng số lượng bước thời gian. b) Xếp chồng nhiều lớp RNN lên nhau, trong đó đầu ra của lớp `l` tại thời điểm `t` là đầu vào cho lớp `l+1` tại cùng thời điểm `t`. c) Sử dụng một vector kích hoạt có kích thước lớn hơn. d) Kết hợp RNN với CNN.
    
36. **Lợi ích của việc sử dụng Deep RNN là gì?** a) Cho phép học các đặc trưng phức tạp hơn ở mỗi bước thời gian. b) Luôn chạy nhanh hơn RNN nông. c) Không bao giờ gặp vấn đề gradient biến mất. d) Yêu cầu ít dữ liệu hơn.
    
37. **Trong một Deep RNN 3 lớp, đầu vào của lớp thứ 2 tại bước thời gian `t` (`a[2]<t>`) là gì?** a) `x<t>` b) `a[1]<t>` c) `a[2]<t-1>` d) `a[3]<t>`
    
38. **Trong thực tế, các kiến trúc RNN sâu thường có bao nhiêu lớp?** a) Hàng trăm lớp. b) Thường không quá sâu (ví dụ, 3 lớp đã được coi là khá sâu) do chi phí tính toán. c) Luôn chỉ có 1 lớp. d) Hàng nghìn lớp.
    
39. **Bạn có thể xây dựng một Deep Bidirectional RNN không?** a) Không, hai kiến trúc này không tương thích. b) Có, bằng cách xếp chồng các lớp BRNN lên nhau. c) Chỉ khi sử dụng GRU. d) Chỉ khi sử dụng LSTM.
    
40. **Trong các ứng dụng thực tế, loại đơn vị hồi quy nào thường được sử dụng làm lựa chọn mặc định?** a) RNN cơ bản. b) GRU. c) LSTM. d) Cả GRU và LSTM đều là những lựa chọn mạnh mẽ.
    

#### Phần 5: Câu hỏi lý thuyết bổ sung

41. **Trong RNN, "trạng thái ẩn" (hidden state) là gì?** a) Là đầu ra cuối cùng của mạng. b) Là một vector mang thông tin tóm tắt về những gì đã xảy ra trong chuỗi cho đến bước thời gian hiện tại. c) Là các trọng số của mạng. d) Là một siêu tham số.
    
42. **Tại sao việc chia sẻ tham số lại quan trọng trong RNN?** a) Nó làm giảm đáng kể tổng số tham số cần học. b) Nó cho phép mô hình áp dụng cùng một quy tắc/đặc trưng đã học cho các phần khác nhau của chuỗi. c) Cả A và B đều đúng. d) Nó làm cho mô hình phức tạp hơn.
    
43. **"Unfolding" một RNN có nghĩa là gì?** a) Biến đổi kiến trúc vòng lặp của RNN thành một mạng truyền thẳng rất sâu, trong đó mỗi bước thời gian là một lớp. b) Làm phẳng vector đầu ra. c) Giảm số lượng lớp. d) Tăng tốc độ học.
    
44. **Cổng cập nhật (update gate) trong GRU có chức năng tương tự như sự kết hợp của hai cổng nào trong LSTM?** a) Cổng quên và cổng đầu ra. b) Cổng quên và cổng cập nhật (đầu vào). c) Cổng cập nhật và cổng đầu ra. d) Không có sự tương đồng.
    
45. **Trong công thức của LSTM, `c<t> = Γu * c̃<t> + Γf * c<t-1>`, `Γf` là đầu ra của cổng nào?** a) Cổng cập nhật (Update gate). b) Cổng quên (Forget gate). c) Cổng đầu ra (Output gate). d) Cổng liên quan (Relevance gate).
    
46. **Đâu là một ví dụ về dữ liệu chuỗi (sequence data)?** a) Giá cổ phiếu theo thời gian. b) Một câu văn. c) Một đoạn âm thanh. d) Tất cả các câu trên.
    
47. **Nếu bạn đang xây dựng một hệ thống nhận dạng giọng nói, tại sao BRNN lại hữu ích?** a) Vì việc nhận dạng một âm vị có thể phụ thuộc vào các âm vị đứng cả trước và sau nó. b) Vì giọng nói luôn được xử lý từ trái sang phải. c) Vì BRNN yêu cầu ít dữ liệu hơn. d) Vì BRNN không bị ảnh hưởng bởi nhiễu.
    
48. **Trong một Deep RNN, các kết nối được hình thành như thế nào?** a) Chỉ theo chiều ngang (qua thời gian). b) Chỉ theo chiều dọc (qua các lớp). c) Cả theo chiều ngang (qua thời gian) và chiều dọc (qua các lớp). d) Một cách ngẫu nhiên.
    
49. **Peephole connection là một biến thể của kiến trúc nào?** a) GRU b) RNN cơ bản c) LSTM d) BRNN
    
50. **Đâu không phải là một ứng dụng của mô hình chuỗi?** a) Nhận dạng hoạt động trong video. b) Phân loại ảnh tĩnh (ví dụ: ảnh mèo và chó). c) Phân tích chuỗi DNA. d) Dịch máy.
    

### **Đáp án**

<details> <summary>Nhấn vào đây để xem đáp án</summary>

1. c | 2. b | 3. b | 4. b | 5. c
    
2. a | 7. b | 8. b | 9. c | 10. b
    
3. d | 12. b | 13. c | 14. b | 15. a
    
4. c | 17. c | 18. d | 19. b | 20. d
    
5. b | 22. b | 23. b | 24. b | 25. b
    
6. a | 27. b | 28. c | 29. d | 30. b
    
7. b | 32. b | 33. a | 34. b | 35. b
    
8. a | 37. b | 38. b | 39. b | 40. d
    
9. b | 42. c | 43. a | 44. b | 45. b
    
10. d | 47. a | 48. c | 49. c | 50. b
    

</details>
### Bài kiểm tra trắc nghiệm: NLP, Mô hình Chuỗi, Attention và Transformer

**Chọn câu trả lời đúng nhất cho mỗi câu hỏi.**

#### Phần 1: Biểu diễn Từ và Word Embeddings

1. **Ưu điểm chính của Word Embeddings so với biểu diễn One-hot là gì?** a) Word Embeddings yêu cầu ít bộ nhớ hơn cho mỗi vector. b) Word Embeddings cho phép mô hình khái quát hóa mối quan hệ giữa các từ (ví dụ: "cam" và "táo" đều là trái cây). c) One-hot luôn tốt hơn cho các bài toán NLP. d) Word Embeddings dễ tính toán hơn.
    
2. **Trong bài toán loại suy "Man is to Woman as King is to ___", word embeddings giải quyết bằng cách nào?** a) Tìm kiếm trên Google. b) Tìm từ `w` sao cho vector `e_w` gần nhất với `e_king - e_man + e_woman`. c) So sánh độ dài của các từ. d) Sử dụng một mạng nơ-ron riêng để giải bài toán loại suy.
    
3. **Hàm tương tự Cosine (Cosine Similarity) được dùng để làm gì?** a) Để đo khoảng cách Euclid giữa hai vector từ. b) Để đo góc giữa hai vector từ, qua đó xác định mức độ tương đồng về ngữ nghĩa. c) Để tính toán hàm chi phí. d) Để chuẩn hóa các vector từ.
    
4. **Trong mô hình Word2Vec Skip-gram, nhiệm vụ học có giám sát được tạo ra là gì?** a) Từ một từ mục tiêu (target), dự đoán các từ ngữ cảnh (context) xung quanh nó. b) Từ các từ ngữ cảnh, dự đoán một từ mục tiêu ở giữa. c) Phân loại cảm xúc của một câu. d) Dịch một câu.
    
5. **Kỹ thuật "Negative Sampling" được phát triển để giải quyết vấn đề gì trong Word2Vec?** a) Vấn đề từ không có trong từ điển. b) Chi phí tính toán rất cao của lớp Softmax trên toàn bộ từ điển. c) Vấn đề thiên vị giới tính trong word embeddings. d) Vấn đề gradient biến mất.
    
6. **Thuật toán GloVe (Global Vectors for Word Representation) học word embeddings dựa trên thông tin nào?** a) Chỉ dựa vào các cặp từ ngữ cảnh-mục tiêu cục bộ. b) Dựa trên ma trận đồng xuất hiện (co-occurrence matrix) của các từ trên toàn bộ kho văn bản. c) Dựa trên cảm xúc của câu. d) Dựa trên một mạng nơ-ron sâu.
    
7. **Một phương pháp đơn giản để phân loại cảm xúc của một câu sử dụng word embeddings là gì?** a) Chỉ sử dụng embedding của từ cuối cùng. b) Lấy trung bình hoặc tổng các vector embedding của tất cả các từ trong câu và đưa vào một bộ phân loại Softmax. c) Đếm số lượng từ tích cực và tiêu cực. d) Sử dụng one-hot encoding.
    
8. **Tại sao word embeddings có thể chứa đựng các thiên vị (bias) xã hội?** a) Do lỗi trong thuật toán. b) Vì chúng học từ các kho văn bản lớn do con người tạo ra, vốn đã chứa đựng các thiên vị đó. c) Do khởi tạo ngẫu nhiên. d) Do hàm chi phí không phù hợp.
    
9. **Một trong các bước để giảm thiểu thiên vị (debiasing) trong word embeddings là gì?** a) Huấn luyện lại mô hình với dữ liệu ít hơn. b) Xác định "chiều thiên vị" (ví dụ: chiều giới tính) và chiếu các từ không mang tính định nghĩa ra khỏi chiều đó. c) Tăng kích thước của vector embedding. d) Chỉ sử dụng các từ trung tính.
    
10. **Trong mô hình Word2Vec CBOW (Continuous Bag-of-Words), nhiệm vụ học là gì?** a) Từ một từ mục tiêu, dự đoán các từ ngữ cảnh. b) Từ các từ ngữ cảnh xung quanh, dự đoán từ mục tiêu ở giữa. c) Dự đoán từ tiếp theo trong câu. d) Dịch từ sang ngôn ngữ khác.
    
11. **Ma trận embedding `E` thường có kích thước là bao nhiêu?** a) (số chiều embedding, số chiều embedding) b) (kích thước từ điển, số lượng câu) c) (số chiều embedding, kích thước từ điển) d) (kích thước từ điển, số chiều embedding)
    
12. **"Transfer learning" trong NLP thường được thực hiện như thế nào?** a) Huấn luyện một mô hình từ đầu cho mọi tác vụ. b) Sử dụng một mô hình đã huấn luyện trên tác vụ A để huấn luyện cho tác vụ B. c) Tải về một bộ word embeddings đã được huấn luyện trước trên một kho văn bản lớn và sử dụng nó cho tác vụ của mình. d) Chia sẻ các siêu tham số giữa các mô hình.
    
13. **Đâu không phải là một ứng dụng của word embeddings?** a) Nhận dạng thực thể có tên (Named Entity Recognition). b) Phân loại cảm xúc. c) Tóm tắt văn bản. d) Phân đoạn ảnh.
    
14. **Khi tạo các cặp (context, target) trong Word2Vec, "window size" (kích thước cửa sổ) có ý nghĩa gì?** a) Kích thước của toàn bộ câu. b) Số lượng từ ngữ cảnh được xem xét ở bên trái và bên phải của từ mục tiêu. c) Số chiều của vector embedding. d) Số lượng ví dụ âm (negative examples).
    
15. **Trong Negative Sampling, tại sao chúng ta không lấy mẫu các từ âm một cách ngẫu nhiên đều?** a) Vì làm vậy quá chậm. b) Vì các từ phổ biến (như "the", "a") sẽ được chọn quá thường xuyên. Thay vào đó, một heuristic được sử dụng để cân bằng giữa các từ phổ biến và ít phổ biến. c) Vì làm vậy sẽ khiến mô hình không hội tụ. d) Vì các từ âm không quan trọng.
    

#### Phần 2: Mô hình Chuỗi và Cơ chế Chú ý (Attention)

16. **Kiến trúc Encoder-Decoder trong các mô hình sequence-to-sequence có vai trò gì?** a) Encoder nén chuỗi đầu vào thành một vector biểu diễn, Decoder tạo ra chuỗi đầu ra từ vector đó. b) Encoder tạo ra chuỗi đầu ra, Decoder nén chuỗi đầu vào. c) Cả hai đều cùng tạo ra chuỗi đầu ra. d) Chúng được dùng để phân loại từ.
    
17. **Một nhược điểm lớn của kiến trúc Encoder-Decoder cơ bản khi xử lý các câu dài là gì?** a) Nó quá nhanh. b) Nó phải nén toàn bộ thông tin của câu dài vào một vector ngữ cảnh có kích thước cố định, gây ra hiện tượng "thắt cổ chai thông tin". c) Nó chỉ hoạt động với các câu ngắn. d) Nó yêu cầu quá nhiều bộ nhớ.
    
18. **Thuật toán tìm kiếm nào chọn ra từ có xác suất cao nhất ở mỗi bước để tạo ra câu dịch?** a) Beam Search b) Breadth-First Search c) Greedy Search d) Depth-First Search
    
19. **Tại sao Greedy Search thường không phải là thuật toán tốt nhất để dịch máy?** a) Vì nó quá chậm. b) Vì việc chọn từ tốt nhất ở mỗi bước có thể dẫn đến một câu hoàn chỉnh không tối ưu về mặt tổng thể. c) Vì nó không thể xử lý các từ không có trong từ điển. d) Vì nó yêu cầu beam width lớn.
    
20. **Beam Search với beam width `B=1` tương đương với thuật toán nào?** a) Random Search b) Greedy Search c) Breadth-First Search d) Không có thuật toán nào.
    
21. **Trong Beam Search, tham số `B` (beam width) có ý nghĩa gì?** a) Số lượng câu dịch cuối cùng được tạo ra. b) Số lượng giả thuyết (lựa chọn) tốt nhất được giữ lại ở mỗi bước. c) Kích thước tối đa của câu dịch. d) Tốc độ học.
    
22. **Mục đích của việc chuẩn hóa độ dài (Length Normalization) trong Beam Search là gì?** a) Để ưu tiên các câu dịch ngắn hơn, vốn có tích các xác suất cao hơn. b) Để phạt các câu dịch quá dài bằng cách chia log của xác suất cho độ dài câu. c) Để đảm bảo tất cả các câu dịch có cùng độ dài. d) Để tăng tốc độ tìm kiếm.
    
23. **Chỉ số BLEU (Bilingual Evaluation Understudy) được dùng để làm gì?** a) Để đo tốc độ của một mô hình dịch máy. b) Để đánh giá chất lượng của một câu dịch máy bằng cách so sánh nó với một hoặc nhiều câu dịch tham khảo của con người. c) Để tính toán hàm chi phí trong quá trình huấn luyện. d) Để chọn ra beam width tốt nhất.
    
24. **Cơ chế chú ý (Attention Mechanism) giải quyết vấn đề câu dài của mô hình Encoder-Decoder bằng cách nào?** a) Bằng cách tăng kích thước của vector ngữ cảnh. b) Cho phép Decoder ở mỗi bước tạo từ, "nhìn lại" và tập trung vào các phần khác nhau, phù hợp của câu đầu vào. c) Bằng cách sử dụng một mạng nơ-ron lớn hơn. d) Bằng cách cắt các câu dài thành nhiều câu ngắn.
    
25. **Trong mô hình Attention, trọng số chú ý `α<t, t'>` cho biết điều gì?** a) Mức độ quan trọng của từ đầu vào thứ `t` đối với từ đầu ra thứ `t'`. b) Mức độ quan trọng của từ đầu ra thứ `t` đối với từ đầu vào thứ `t'`. c) Mức độ quan trọng của từ đầu vào thứ `t'` khi tạo ra từ đầu ra thứ `t`. d) Xác suất của từ đầu ra thứ `t`.
    
26. **Trong bài toán chú thích ảnh (Image Captioning), vai trò của Encoder thường được đảm nhiệm bởi kiến trúc nào?** a) Một mạng RNN. b) Một mạng Transformer. c) Một mạng CNN đã được huấn luyện trước (ví dụ: VGG, ResNet). d) Một mô hình tuyến tính.
    
27. **Hàm chi phí CTC (Connectionist Temporal Classification) hữu ích cho bài toán nào?** a) Dịch máy. b) Phân loại cảm xúc. c) Nhận dạng giọng nói, nơi không có sự căn chỉnh chính xác giữa chuỗi âm thanh đầu vào và chuỗi văn bản đầu ra. d) Tạo văn bản.
    
28. **Trong một hệ thống phát hiện từ kích hoạt (trigger word detection), nhãn của dữ liệu thường được gán như thế nào?** a) Gán nhãn 1 cho toàn bộ đoạn âm thanh nếu có từ kích hoạt. b) Gán nhãn 1 cho các khung thời gian ngay sau khi từ kích hoạt được nói xong. c) Gán nhãn 1 cho các khung thời gian trước khi từ kích hoạt được nói. d) Không cần gán nhãn.
    
29. **Nếu lỗi dịch máy của bạn chủ yếu là do Beam Search, bạn nên làm gì? (dựa trên phân tích lỗi)** a) Tăng beam width `B`. b) Huấn luyện lại mô hình RNN. c) Thu thập thêm dữ liệu. d) Giảm beam width `B`.
    
30. **Nếu lỗi dịch máy của bạn chủ yếu là do mô hình RNN, bạn nên làm gì?** a) Tăng beam width `B`. b) Thử một kiến trúc RNN khác, thêm điều chuẩn hóa, hoặc thu thập thêm dữ liệu. c) Giảm beam width `B`. d) Chỉ cần chạy lại Beam Search.
    

#### Phần 3: Kiến trúc Transformer

31. **Động lực chính đằng sau việc phát minh ra kiến trúc Transformer là gì?** a) Để tạo ra một mô hình có ít tham số hơn RNN. b) Để khắc phục hạn chế về xử lý tuần tự của RNN và cho phép xử lý song song toàn bộ chuỗi, giúp nắm bắt các phụ thuộc xa tốt hơn. c) Để chuyên biệt hóa cho các bài toán thị giác máy tính. d) Để sử dụng ít dữ liệu hơn.
    
32. **Cơ chế cốt lõi của Transformer là gì?** a) Các kết nối hồi quy. b) Các lớp tích chập. c) Tự chú ý (Self-Attention). d) Các cổng (gates) như trong LSTM.
    
33. **Trong Self-Attention, ba vector Query (Q), Key (K), và Value (V) được tạo ra từ đâu?** a) Từ ba nguồn dữ liệu khác nhau. b) Chúng được tạo ra bằng cách nhân vector embedding của cùng một từ đầu vào với ba ma trận trọng số khác nhau (`W_Q`, `W_K`, `W_V`). c) Chúng là các hằng số cố định. d) Chúng được lấy ngẫu nhiên.
    
34. **Vai trò của Query, Key, và Value trong Self-Attention là gì?** a) Query hỏi, Key trả lời, Value cung cấp thông tin. b) Query đại diện cho từ hiện tại, nó so khớp với tất cả các Key (đại diện cho các từ khác) để tìm ra trọng số chú ý, sau đó các trọng số này được dùng để tính tổng có trọng số của các Value. c) Chúng không có vai trò cụ thể. d) Cả ba đều được dùng để tính toán hàm chi phí.
    
35. **Mục đích của "Multi-Head Attention" là gì?** a) Để làm cho mô hình phức tạp hơn một cách không cần thiết. b) Cho phép mô hình cùng lúc chú ý đến các thông tin từ các không gian con biểu diễn khác nhau (ví dụ: một "đầu" có thể tập trung vào quan hệ cú pháp, một "đầu" khác tập trung vào quan hệ ngữ nghĩa). c) Để xử lý nhiều ngôn ngữ cùng lúc. d) Để giảm số lượng tham số.
    
36. **Tại sao Transformer cần "Positional Encoding" (Mã hóa vị trí)?** a) Vì cơ chế self-attention không có tính tuần tự, nó xử lý tất cả các từ như một tập hợp. Positional Encoding được thêm vào để cung cấp thông tin về vị trí của các từ trong chuỗi. b) Để tăng số chiều của vector embedding. c) Để giảm số chiều của vector embedding. d) Nó không thực sự cần thiết.
    
37. **Trong khối Decoder của Transformer, "Masked Multi-Head Attention" có tác dụng gì?** a) Che đi một số từ ngẫu nhiên để điều chuẩn hóa. b) Ngăn chặn việc một vị trí có thể "nhìn thấy" các vị trí trong tương lai của chuỗi đầu ra, đảm bảo rằng dự đoán tại bước `t` chỉ phụ thuộc vào các đầu ra đã biết trước đó. c) Che đi các từ không quan trọng trong câu đầu vào. d) Chỉ được sử dụng trong quá trình inference.
    
38. **Thành phần "Add & Norm" trong Transformer bao gồm những gì?** a) Phép cộng và phép nhân. b) Một kết nối tắt (residual connection) và một lớp chuẩn hóa lớp (Layer Normalization). c) Data augmentation và chuẩn hóa dữ liệu. d) Phép cộng và hàm Softmax.
    
39. **Đâu là một mô hình nổi tiếng được xây dựng dựa trên kiến trúc Transformer?** a) Word2Vec b) GloVe c) LSTM d) BERT, GPT
    
40. **So với RNN, Transformer có ưu điểm gì về mặt tính toán?** a) Nó luôn yêu cầu ít bộ nhớ hơn. b) Các phép tính trong nó có thể được song song hóa cao độ, giúp tận dụng tốt GPU và huấn luyện nhanh hơn trên các chuỗi dài. c) Nó không cần backpropagation. d) Nó có ít tham số hơn.
    

#### Phần 4: Câu hỏi lý thuyết bổ sung và Tổng hợp

41. **Trong mô hình Encoder-Decoder với Attention, vector ngữ cảnh `c<t>` được tính như thế nào?** a) Là trạng thái ẩn cuối cùng của Encoder. b) Là tổng có trọng số của các trạng thái ẩn của Encoder, với trọng số là các trọng số chú ý. c) Là trạng thái ẩn đầu tiên của Encoder. d) Là trung bình của tất cả các trạng thái ẩn của Encoder.
    
42. **Trong Self-Attention, tại sao lại chia cho `sqrt(d_k)` trong công thức `softmax(QKᵀ / sqrt(d_k))`?** a) Để làm cho kết quả là số nguyên. b) Để ổn định gradient, ngăn chặn việc tích vô hướng trở nên quá lớn khi số chiều `d_k` lớn. c) Đây là một tham số có thể học được. d) Để chuẩn hóa độ dài của vector.
    
43. **Kiến trúc Transformer có các kết nối hồi quy (recurrent connections) không?** a) Có, giống hệt như RNN. b) Không, nó hoàn toàn dựa vào cơ chế self-attention. c) Chỉ có ở khối Encoder. d) Chỉ có ở khối Decoder.
    
44. **"Fine-tuning" một mô hình Transformer đã được huấn luyện trước (như BERT) cho một tác vụ cụ thể (như NER) thường bao gồm bước nào?** a) Huấn luyện lại toàn bộ mô hình từ đầu trên dữ liệu mới. b) Giữ nguyên phần lớn mô hình và chỉ thêm/huấn luyện một vài lớp phân loại ở trên cùng. c) Chỉ sử dụng các positional encodings. d) Loại bỏ cơ chế attention.
    
45. **Trong bài toán Question Answering (QA), mô hình Transformer thường được huấn luyện để làm gì?** a) Tạo ra một câu trả lời hoàn toàn mới. b) Dự đoán vị trí bắt đầu và kết thúc của câu trả lời trong một đoạn văn bản cho trước. c) Dịch câu hỏi sang một ngôn ngữ khác. d) Tóm tắt đoạn văn bản.
    
46. **Sự khác biệt chính giữa khối Encoder và Decoder trong Transformer là gì?** a) Encoder không có self-attention. b) Decoder có thêm một lớp "Masked Multi-Head Attention" và một lớp multi-head attention thứ hai để chú ý đến đầu ra của Encoder. c) Decoder không có lớp Feed Forward. d) Không có sự khác biệt nào.
    
47. **Đâu là một nhược điểm của Transformer so với RNN?** a) Khó nắm bắt các phụ thuộc xa. b) Chi phí tính toán và bộ nhớ tăng theo bậc hai với độ dài chuỗi. c) Không thể xử lý song song. d) Không thể áp dụng cho các bài toán NLP.
    
48. **"Positional Encoding" trong Transformer thường được tạo ra bằng cách nào?** a) Bằng một mạng nơ-ron nhỏ. b) Bằng cách sử dụng các hàm sin và cos ở các tần số khác nhau. c) Là các vector có thể học được. d) Bằng cách gán một số nguyên cho mỗi vị trí.
    
49. **Trong Word2Vec, tại sao Negative Sampling lại hiệu quả hơn Hierarchical Softmax?** a) Về mặt lý thuyết, Hierarchical Softmax tốt hơn. b) Trong thực tế, Negative Sampling đơn giản hóa bài toán thành nhiều bài toán phân loại nhị phân độc lập, thường cho kết quả tốt hơn và dễ triển khai hơn. c) Negative Sampling yêu cầu ít dữ liệu hơn. d) Hierarchical Softmax không thể học được các từ hiếm.
    
50. **Mô hình nào sau đây không phải là mô hình sequence-to-sequence?** a) Dịch máy. b) Tóm tắt văn bản. c) Phân loại cảm xúc (sử dụng RNN many-to-one). d) Tạo chú thích ảnh.
    

#### Phần 5: Câu hỏi lý thuyết bổ sung

51. **Trong BLEU score, "brevity penalty" (phạt độ ngắn) được dùng để làm gì?** a) Để phạt các câu dịch máy quá dài so với câu tham khảo. b) Để phạt các câu dịch máy quá ngắn so với câu tham khảo, tránh trường hợp mô hình chỉ dịch một từ đúng để có precision cao. c) Để thưởng cho các câu dịch ngắn. d) Để đo lường tốc độ dịch.
    
52. **Lớp "Feed Forward Network" trong mỗi khối của Transformer có đặc điểm gì?** a) Nó là một mạng RNN. b) Nó là một mạng tích chập (CNN). c) Nó là một mạng nơ-ron truyền thẳng (fully-connected) đơn giản, được áp dụng độc lập cho từng vị trí. d) Nó chia sẻ trọng số giữa tất cả các vị trí.
    
53. **Trong bài toán Question Answering, fine-tuning mô hình Transformer thường yêu cầu đầu vào là gì?** a) Chỉ câu hỏi. b) Chỉ đoạn văn. c) Cặp (câu hỏi, đoạn văn). d) Chỉ câu trả lời.
    
54. **"Scaled Dot-Product Attention" là tên gọi của cơ chế nào?** a) Toàn bộ kiến trúc Transformer. b) Cơ chế self-attention cụ thể được sử dụng trong Transformer. c) Lớp Feed Forward Network. d) Lớp Positional Encoding.
    
55. **Kiến trúc Transformer được giới thiệu lần đầu tiên trong bài báo nào?** a) "Deep Residual Learning for Image Recognition" b) "GloVe: Global Vectors for Word Representation" c) "Attention Is All You Need" d) "BERT: Pre-training of Deep Bidirectional Transformers for Language Understanding"
    
56. **Tại sao Attention có thể được xem là một cơ chế "mềm" (soft)?** a) Vì nó dễ lập trình. b) Vì nó gán một trọng số (một giá trị mềm) cho mỗi từ đầu vào, thay vì chọn "cứng" một từ duy nhất để tập trung vào. c) Vì nó không yêu cầu nhiều bộ nhớ. d) Vì nó sử dụng hàm kích hoạt Softmax.
    
57. **Trong khối Decoder của Transformer, lớp Multi-Head Attention thứ hai nhận Key (K) và Value (V) từ đâu?** a) Từ lớp Masked Multi-Head Attention ngay trước đó. b) Từ đầu ra của khối Encoder. c) Từ các positional encodings. d) Từ dữ liệu đầu vào gốc.
    
58. **Đâu là một hạn chế của chỉ số BLEU?** a) Nó không xem xét đến ý nghĩa hoặc cấu trúc ngữ pháp của câu. b) Nó quá chậm để tính toán. c) Nó yêu cầu nhiều GPU. d) Nó chỉ hoạt động với các câu ngắn.
    
59. **"Extractive Question Answering" có nghĩa là gì?** a) Mô hình tự tạo ra câu trả lời. b) Mô hình trích xuất một đoạn văn bản từ ngữ cảnh cho trước để làm câu trả lời. c) Mô hình chỉ trả lời "có" hoặc "không". d) Mô hình dịch câu hỏi.
    
60. **So với RNN, Transformer có khả năng nắm bắt các phụ thuộc xa tốt hơn là do:** a) Nó có nhiều lớp hơn. b) Đường đi trực tiếp giữa hai từ bất kỳ trong cơ chế self-attention có độ dài là O(1), không phụ thuộc vào khoảng cách giữa chúng trong chuỗi. c) Nó sử dụng hàm kích hoạt ReLU. d) Nó có kết nối hồi quy.
    

### **Đáp án**

<details> <summary>Nhấn vào đây để xem đáp án</summary>

1. b | 2. b | 3. b | 4. a | 5. b
    
2. b | 7. b | 8. b | 9. b | 10. b
    
3. d | 12. c | 13. d | 14. b | 15. b
    
4. a | 17. b | 18. c | 19. b | 20. b
    
5. b | 22. b | 23. b | 24. b | 25. c
    
6. c | 27. c | 28. b | 29. a | 30. b
    
7. b | 32. c | 33. b | 34. b | 35. b
    
8. a | 37. b | 38. b | 39. d | 40. b
    
9. b | 42. b | 43. b | 44. b | 45. b
    
10. b | 47. b | 48. b | 49. b | 50. c
    
11. b | 52. c | 53. c | 54. b | 55. c
    
12. b | 57. b | 58. a | 59. b | 60. b
    

</details>



If you have 10,000 examples, how would you split the train/dev/test set? Choose the best option.

33% train. 33% dev. 33% test.

60% train. 20% dev. 20% test.

98% train. 1% dev. 1% test.

Correct

Yes. This might be considered a small data set, not in the range of big data. Thus a more classical (old) best practice should be used.

1 / 1 point

### 2.

Question 2

In a personal experiment, an M.L. student decides to not use a test set, only train-dev sets. In this case which of the following is true?

He might be overfitting to the dev set.

He won't be able to measure the variance of the model.

He won't be able to measure the bias of the model.

Not having a test set is unacceptable under any circumstance.

Incorrect

No. Although not recommended if a more accurate measure of the performance is not necessary, it is ok to not use a test set. However, this might cause an overfit to the dev set.

1 point

### 3.

Question 3

If your Neural Network model seems to have high variance, what of the following would be promising things to try?

Make the Neural Network deeper

Get more training data

Correct

Add regularization

Correct

Increase the number of units in each hidden layer

Get more test data

1 / 1 point

### 4.

Question 4

You are working on an automated check-out kiosk for a supermarket and are building a classifier for apples, bananas, and oranges.

Suppose your classifier obtains a training set error of 19% and a development set error of 21%.

**Which of the following is the most promising strategy to improve your classifier?** (Assume the human error is approximately 0%)

Get more training data.

Increase the regularization parameter lambda.

Use a bigger network.

Correct

A larger network can reduce bias by enabling the model to learn more complex patterns.

1 / 1 point

### 5.

Question 5

In every case it is a good practice to use dropout when training a deep neural network because it can help to prevent overfitting. True/False?

False

True

Correct

Correct. In most cases, it is recommended to not use dropout if there is no overfit. Although in computer vision, due to the nature of the data, it is the default practice.

1 / 1 point

### 6.

Question 6

**True or False:** To reduce high variance, the regularization hyperparameter lambda must be increased.

True

False

Correct

Correct. By increasing the regularization parameter the magnitude of the weight parameters is reduced. This helps reduce the variance.

1 / 1 point

### 7.

Question 7

Which of the following are true about dropout?

In practice, it eliminates units of each layer with a probability of 1- keep_prob.

Correct

Correct. The probability that dropout doesn't eliminate a neuron is keep_prob.

It helps to reduce overfitting.

Correct

Correct. The dropout is a regularization technique and thus helps to reduce the overfit.

In practice, it eliminates units of each layer with a probability of keep_prob.

It helps to reduce the bias of a model.

1 / 1 point

### 8.

Question 8

Increasing the parameter keep_prob from (say) 0.5 to 0.6 will likely cause the following: (Check the two that apply)

Increasing the regularization effect

Reducing the regularization effect

Correct

Causing the neural network to end up with a higher training set error

Causing the neural network to end up with a lower training set error

Correct

1 / 1 point

### 9.

Question 9

Which of these techniques are useful for reducing variance (reducing overfitting)? (Check all that apply.)

Dropout

Correct

Xavier initialization

L2 regularization

Correct

Exploding gradient

Data augmentation

Correct

Vanishing gradient

Gradient Checking

1 / 1 point

### 10.

Question 10

Suppose that a model uses, as one feature, the total number of kilometers walked by a person during a year, and another feature is the height of the person in meters. What is the most likely effect of normalization of the input data?

It won't have any positive or negative effects.

It will make the data easier to visualize.

It will make the training faster.

It will increase the variance of the model.