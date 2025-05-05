## Chapter 3

### Previous concepts:

1. [Limits](https://www.youtube.com/watch?v=pYVVPqphPS0&ab_channel=ElTraductordeIngenier%C3%ADa)
2. [Slope of a line](https://youtu.be/lz8zVJxRFX8?si=C2LQjSdEETm9PGwQ)
3. [Derivates](https://youtu.be/_6-zwdrqD3U?si=PyqmzsqCEmlCYy3v)
4. [Partial Derivates](https://en.wikipedia.org/wiki/Partial_derivative)
5. [Expected value](https://en.wikipedia.org/wiki/Expected_value)

### Gradient descent or method of steepest descent

- [Gradient descent](https://en.wikipedia.org/wiki/Gradient_descent)
- It's an algorithm used to find the local minimum of a function.
- The gradient is a vector whose value at a point p gives the direction and the rate of fastest increase (in other words, the "slope" when we have more than one variable)
- The algorithm works by starting at a point of the function (for example if the function is f(x) = x^2 we start at x = 8) and updating the position by going in the opposite direction of the gradient until we reach a point where the gradient is 0 or close to 0 (local minima)
- To calculate the gradient we need partial derivatives (in case of multiple variables)
- We multiply the gradient by a step size (a small number, for example 0.1), so when we get closer to the minima the jumps in the direction of the gradient are smaller
- The function needs to be derivable



