## Chapter 6

### Previous concepts

1. Matrix multiplication (rows of the first matrix by columns of the second matrix)
2. Symmetric matrix
3. [Correlation](https://en.wikipedia.org/wiki/Correlation), [covariance](https://en.wikipedia.org/wiki/Covariance)
4. Centering data

### Intuitive description of PCA

- Principal Component Analysis (PCA) is a method to reduce the dimensionality of data
- You try to find the dimensions that capture most of the variation in the data 

### Eigenvectors and Eigenvalues

- Multiplying a matrix with a vector results in a new vector (like if we transformed the original vector to a new one)
- If we want the resulting vector to preserve the dimensions of the original, the matrix must be square, with the number of rows/columns equal to the number of elements in the vector. Then we will change the original vector in magnitude and direction.
- But there are some orientations associated with each square matrix that are special, or characteristic (hence, the notion of “eigen”)
- The special orientations of a square matrix are represented by vectors called eigenvectors. When you multiply a vector with a square matrix, if the vector belongs in the same direction of one of its eigenvectors, then the vector will keep its direction and will only change in magnitude, like when you multiply a vector with a scalar; Each eigenvector has a eigenvalue, a value that could be seen as that scalar.
- The number of eigenvectors of a square matrix is its number of rows/columns
- Formally: Ax = λx, where A is a matrix and x is an eigenvector and λ is an eigenvalue. That’s saying that multiplying the vector x by the matrix A results in a vector that equals x multiplied by a scalar value λ.
- In a square symmetric matrix, the eigenvector are orthogonals

### Covariance matrix

- Given X, a matrix with our data, where the columns are features and the rows are instances of the data, if we center X and we multiply the transpose of X with itself we get the covariance matrix
- The covariance matrix is a square symmetric matrix where the diagonal is the variance of each feature, and the off-diagonal elements are the covariance of each pair of features

### PCA is made from the covariance matrix

- The eigenvectors of a covariance matrix are the principal components of the original matrix X. Each eigenvector of the covariance matrix yields a primary dimension along which the original data vary, and the associated eigenvalue tells you how much variance there is in the data along that direction
- So, in order to find the dimensions that capture most of the variance in the data we take the eigenvectors with greater eigenvalues, and project the data onto that eigenvalues
- PCA is powerful for capturing major patterns in data, but it can miss rare yet crucial features (firetruck example).

### Intro to unsupervised learning

- Up until know, our datasets where labeled, and thus we were doing supervised learning. However when we don't have this labels it's called unsupervised learning
- One of the problems in unsupervised learning is clustering, trying to find the missing labels for our data
- One of the main algorithms for clustering is K-means
