# Multilayer-Perceptron
MLP in Python

https://github.com/jorgesleonel/Multilayer-Perceptron/blob/master/Basic%20Multi-Layer%20Perceptron.ipynb


The Perceptron, that neural network whose name evokes how the future looked from the perspective of the 1950s, 
is a simple algorithm intended to perform binary classification; i.e. it predicts whether input belongs to a certain 
category of interest or not (ex: fraud/ not-fraud).

The perceptron is a linear classifier — an algorithm that classifies input by separating two categories with a straight
line. Input is typically a feature vector xmultiplied by weights w and added to a bias b: y = w * x + b.

Perceptrons produce a single output based on several real-valued inputs by forming a linear combination using input
weights (and sometimes passing the output through a non-linear activation function). 

Rosenblatt built a single-layer perceptron ; it did not include multiple layers, which allow neural networks to model 
a feature hierarchy. It was, therefore, a shallow neural network, which ended up preventing his perceptron from performing
non-linear classification, such as the classic logic XOR function (an XOR operator trigger when input exhibits either one
trait or another, but not both; it stands for “exclusive OR”).

Fast forward to 1986, when Hinton, Rumelhart, and Williams published a paper “Learning representations by back-propagating
errors”, introducing backpropagation and hidden layers concepts — therefore so to speak giving birth to Multilayer 
Perceptrons (MLPs):

* Backpropagation, a procedure to repeatedly adjust the weights so as to minimize the difference between actual output
and desired output
* Hidden Layers, which are neuron nodes stacked in between inputs and outputs, allowing neural networks to learn more
complicated features (such as XOR logic)

An MLP can be thought of, therefore, as a deep artificial neural network. It is composed of more than one perceptron. 
They are composed of an input layer to receive the signal, an output layer that makes a decision or prediction about 
the input, and in between those two, an arbitrary number of hidden layers that are the true computational engine of the MLP.

Multilayer perceptrons train on a set of input-output pairs and learn to model the correlation (or dependencies) between
those inputs and outputs. Training involves adjusting the parameters, or the weights and biases, of the model in order
to minimize error. Backpropagation is used to make those weigh and bias adjustments relative to the error, and the error
itself can be measured in a variety of ways, including by root mean squared error (RMSE).

Feedforward networks such as MLPs are just like ping-pong: they are mainly involved in two motions, a constant back and
forth (forward and backward passes):

. In the forward pass, the signal flow moves from the input layer through the hidden layers to the output layer, and
the decision of the output layer is measured against the ground truth labels;

. In the backward pass, using backpropagation and the chain rule of calculus, partial derivatives of the error function
regarding the various weights and biases are back-propagated through the MLP. That act of differentiation gives us a 
gradient, or a landscape of error, along which the parameters may be adjusted as they move the MLP one step closer to
the error minimum. (this can be done with any gradient-based optimization algorithm such as stochastic gradient descent).

The network keeps playing that game of ping-pong until the error can go no lower. This state is known as convergence.

![MLP](https://www.researchgate.net/profile/Mohamed_Zahran6/publication/303875065/figure/fig4/AS:371118507610123@1465492955561/A-hypothetical-example-of-Multilayer-Perceptron-Network.png)

