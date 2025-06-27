## Chapter 10

### Previous concepts

### First paragraph

- There was a problem because no one knew how to train multi-layer perceptrons
- Rossenblat was the first to introduce the concept of backpropagation, where the output value for an input minus the real expected value (the error) propagates back to change the weights
- Before training the network we have to initialize the weights, if we initialize them all with the same value, then the changes in each weight will be the same. So we have to initialize each weight to a random value so it breaks symmetry
- Conceptually, the backpropagation algorithm consists in calculating the error for an input (output - expected value). This error is a function of all the weights of the network, How do you minimize the error? Well, you can do gradient descent. Find the gradient of the error (as a function of the weights, meaning the input of the function are the weights and bias and everything else is fixed)
and take a small step in the opposite direction by updating each weight by a tiny amount
- The problem with this is that the shape of the function you’re descending is not necessarily convex, meaning its possible that the gradient descent algorithm gets stuck in some local minima

### Second paragraph

- Te explica como entrenar una neurona usando la función de error y gradient descend, pero claro esto no sirve para multilayer, porque el error de una capa oculta no es el error final ¿no?
- Bueno también te explica que haciendolo así no te va a servir para datos que no sean linealmente separables, explica porque en el siguiente párrafo

### Third paragraph

- Una única neurona lo que hace es encontrar una línea/hiperplano (revisar capítulo 2). Si es regresión lineal una línea que pase por los datos, no usamos función de activación, si es clasificación una línea que separe los datos, usamos función de activación...
- Añadir más neuronas en la misma capa lo único que hace es encontrar líneas diferentes, pero no combina las líneas, cada una es independiente, como si las demas no existieran cada una se ocupa de lo suyo
- 
