## Chapter 9

### Multilayer/Deep neural networks (Multilayer perceptron)

- This chapter explains the most basic architecture of a neural network, the multilayer perceptron. Because is the easiest one to understand
- A multilayer neural network consists of three types of layers, input layer, hidden layers and output layer
- The input layer is simply the input data, for example if we want a network to classify images of cats and dogs, the input layer will be the numerical value of the pixels of the image we want to classify
- The hidden and output layers are perceptrons (weight, bias and activation function) stacked
- Each perceptron in a layer receives as input the output of all the perceptrons in the previous layer
- The input and output layers are mandatory. You can put 0 hidden layers if you want (that would be a single-layer neural network, we could train it with Rossenblat's algorithm)
- If the network has one or more hidden layers, we can say its a deep neural network:\
  ![deepnn](imgs/deepnn.png)




### Explaining how a deep neural networks can approximate any function
