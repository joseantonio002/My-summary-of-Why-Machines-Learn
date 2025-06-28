## Chapter 10

### Previous concepts

- Chain rule

### How do we train multi-layer neural networks?

- There was a problem because no one knew how to train multi-layer perceptrons
- Rossenblat was the first to introduce the concept of backpropagation, where the output value for an input minus the real expected value (the error) propagates back to change the weights
- Before training the network we have to initialize the weights, if we initialize them all with the same value, then the changes in each weight will be the same. So we have to initialize each weight to a random value so it breaks symmetry
- Conceptually, the backpropagation algorithm consists in calculating the error for an input (output - expected value). This error is a function of all the weights of the network, How do you minimize the error? Well, you can do gradient descent. Find the gradient of the error (as a function of the weights, meaning the input of the function are the weights and bias and everything else is fixed)
and take a small step in the opposite direction by updating each weight by a tiny amount
- The problem with this is that the shape of the function you’re descending is not necessarily convex, meaning its possible that the gradient descent algorithm gets stuck in some local minima

### The basics 

- To update the parameters of a neural network using the error made by the network we need a loss function. Then we find the gradient of this loss function w.r.t all the weights and bias of the network, and with the gradient we can update the parameters by going in the opposite direction of the gradient (gradient descend)
- However, with just a single layer of neurons, we cannot solve problems that are not linearly independent.

### Nonlinearity added to the mix

- A single neuron essentially finds a line/hyperplane (see Chapter 2). If it's linear regression, it finds a line that fits the data—we don’t use an activation function. If it’s classification, it finds a line that separates the data—we do use an activation function...
- Adding more neurons in the same layer only results in finding different lines, but they do not combine; each one is independent, as if the others didn’t exist—each neuron handles its own part.
- To combine the lines from one layer, we need an additional layer. However, the more layers we add, the more parameters there are, and therefore more partial derivatives to compute. This becomes unsustainable. This is where backpropagation comes in.

### Backpropagation algorithm 

- In the forward pass, the network computes each dimension of the gradient using calculus tricks (chain rule, etc.).
- To do this, at the end of the forward pass, it must remember the outputs of each neuron and all the weights and biases (they’re used to compute the gradient without taking derivatives from scratch).
- Training eventually comes down to this: Provide the network with some set of inputs, figure out what the expected output should be (either because we humans have annotated the data and know what the output should be or because, in types of learning called self-supervised, the expected output is some known variation of the input itself), calculate the loss, calculate the gradient of the loss, update the weights/biases, rinse and repeat

