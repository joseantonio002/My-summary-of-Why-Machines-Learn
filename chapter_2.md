## Chapter 2

### Previous concepts:
1. sen, cos, tan
2. Vectors ([basics](https://www.youtube.com/watch?v=KBSCMTYaH1s&ab_channel=ProfessorDaveExplains))
3. [Dot product](https://www.youtube.com/watch?v=h0NJK4mEIJU&t=52s&ab_channel=PhysicsVideosbyEugeneKhutoryansky)
4. Matrix ([transpose](https://www.youtube.com/watch?v=TZrKrNVhbjI&ab_channel=KhanAcademy), multiplication)

### Perceptron as a Vector Function

- Perceptron output:  
  - Outputs `1` if the weighted sum of inputs plus bias > 0  
  - Outputs `-1` otherwise  
- Inputs and weights and bias can be represented as vectors.
- The weighted sum becomes a **dot product** of the input vector and weight vector.

### Geometry of the Perceptron

- In 2D:
  - Data points: `(x1, x2)`  
  - Weights: `(w1, w2)` → vector **w**
- A **hyperplane** separates the space into two regions.
  - In 2D: a line
  - In 3D: a plane
  - In higher dimensions: a hyperplane
- **w** is orthogonal (perpendicular) to the hyperplane.
- Changing **w** changes the orientation of the hyperplane.
- The **bias** moves the hyperplane without changing its orientation.

- Dot product `w · x`:
  - Positive → point on one side of the hyperplane
  - Negative → point on the other side
  - Zero → point lies **on** the hyperplane
- If **w** is a unit vector:
  - Dot product equals the **projection** of a point onto **w**.
  - This projection measures the signed distance from the hyperplane.
- Dot products with **w** tell:
  - Which side of the hyperplane a point lies
  - How far it is from the hyperplane

### Multiple Hyperplanes

- If data is linearly separable, infinitely many hyperplanes can divide them.
- The perceptron will find one separating hyperplane, not necessarily the best.
- The "best" hyperplane relates to **future prediction accuracy**, which is a more complex problem.


 ### Training algorithm for Rosenblatt's perceptron

- Step 1. Initialize the weight vector to zero: set w = 0

- Step 2. For each data point x in the training dataset, do the following:

 - Step 2a if ywTx ≤0:

    the weight vector is wrong, so update it:

    wnew= wold + yx

- Step 3. If there were no updates to the weight vector in Step 2, terminate; otherwise, go to Step 2 and iterate over all the data points once again.

Basically, it finds the hyperplane by checking if every training point is on the side of the hyperplane its suposed to be. 
If not, it moves the weight vector in a way that that point is closer to the correct side of the hyperplane

### Limitations of the Rosenblatt's perceptron

- Data has to be linearly separable if we want to solve the problem with one perceptron (XOR problem)
- The training algorithm does not work with multiple layers of perceptrons
