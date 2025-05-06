## Chapter 3

### Previous concepts:

1. [Limits](https://www.youtube.com/watch?v=pYVVPqphPS0&ab_channel=ElTraductordeIngenier%C3%ADa)
2. [Slope of a line](https://youtu.be/lz8zVJxRFX8?si=C2LQjSdEETm9PGwQ)
3. [Derivates](https://youtu.be/_6-zwdrqD3U?si=PyqmzsqCEmlCYy3v)
4. [Partial Derivates](https://en.wikipedia.org/wiki/Partial_derivative)
5. [Expected value](https://en.wikipedia.org/wiki/Expected_value)

### Gradient descent or method of steepest descent

- [Gradient descent](https://en.wikipedia.org/wiki/Gradient_descent)
- It's an algorithm used to find the local minimum of a function
- The gradient is a vector whose value at a point p gives the direction and the rate of fastest increase (in other words, the "slope" when we have more than one variable)
- The algorithm works by starting at a point of the function (for example if the function is f(x) = x^2 we start at x = 8) and updating the position by going in the opposite direction of the gradient until we reach a point where the gradient is 0 or close to 0 (local minima)
- To calculate the gradient we need partial derivatives (in case of multiple variables)
- We multiply the gradient by a step size (a small number, for example 0.1), so when we get closer to the minima the jumps in the direction of the gradient are smaller
- The function needs to be derivable

### First approximation to minimizing the error in order to optimize parameters

- This chapter uses an adaptative filter as an example. This filter takes an input (xn) each time step, that can be seconds, minutes, months... and filters the noise from the input. The catch is that the noise is different each time we use the filter, so it has to be adaptative, meaning it has to learn the characteristics of the noise each time, like a neuron has to learn the patterns in the data:\
![filter](img/filter.PNG)
- If we have an input xn (xn0, xn1, xn2...), an output yn, calculated using weights; yn = xn.w (where . is the dot product); And a desired output dn; we can calculate the error en = dn - w.xn for each input
- A way to update the parameters w so the filter learns the noise is by minimizing the error. To do this we calculate the function of the error by squaring each error and taking the expected value of that: J = E((dn - w.xn)^2). Because we dont have probabilities, the expected value E is simply the sample average. E(xn) = 1/n SUM from n = 1 to n(xn)
- We square the errors because they can be negative and cancel each other, it punishes big errors more, and makes the error function differentiable everywhere (MSE)
- There are two main ways of minimizing this function, setting the derivative with respect to w to 0 and solve the equation, or use gradient descent. However, both ways are computationally expensive. That's why the LMS algorithm was invented (next paragraph)


