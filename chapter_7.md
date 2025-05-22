## Chapter 7

### Previous concepts

### Overview of Vapnik's algorithm for finding an optimal separating hyperplane

- Remembering: a separating hyperplane is a lineal boundary between two regions in the coordinate space (it divides the space in two)
- To separate data into two clusters using a hyperplane, the data must be linearly separable
- Rosenblatt's perceptron finds a hyperplane that divides the labeled data, however is a random one and, hence, not the best possible
- Vapnik's algorithm finds the OPTIMAL SEPARATING HYPERPLANE, meaning the one that minimizes prediction error. To do this it finds the hyperplane
that maximizes the margins between the two clusters of data, using the closest data points for each cluster as margin. The hyperplane is the line that goes through the middle of the path. \
![optimal_separating_hyperplane](imgs/optimal_separating_hyperplane.png)\
By definition, the data is linearly separable, so this margin data points always exists. And the hyperplane is placed in the middle of "no-mans land".
- Maybe for some data this is not the best hyperplane, maybe the best one would be near the margin of some cluster, however this optimal hyperplane works best in most cases, and it allows us to have a defined method to find it. It's after all still probabilistic
- The number of margin data points for each cluster/class of data can be anything (greater than zero of course)
- The optimal hyperplane is characterized by the vector w (perperdicular to the hyperplane) and the bias b, its offset from the origin
- The weight vector that maximizes the separation between points on either side of the hyperplane can be found by minimizing the function |w|^2/2, where |w| is the magnitude of the weight vector, while simultaneously satisfying this equation for every data point xi (a vector) and its associated label, yi (a scalar, equal to -1 or +1): yi(w.xi + b) ≥ 1 (margin rule)
- This is a constrained optimization problem, where we cannot just simply optimize |w|^2/2, we have to satisfy certain condition, the margin rule. To do this we use Lagrange multipliers

### Lagrange Multipliers


