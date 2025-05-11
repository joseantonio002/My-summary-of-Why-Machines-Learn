## Chapter 4

### Previous concepts

1. [Bayes theorem](https://www.youtube.com/watch?v=HZGCoVF3YvM&ab_channel=3Blue1Brown)
2. Basics of probability theory (experiment, random variable, [CDF, PDF, PMF](https://www.youtube.com/watch?v=YXLVjCKVP7U&t=17s&ab_channel=zedstatistics), famous distributions (Bernoulli, normal...), [Expected value](https://en.wikipedia.org/wiki/Expected_value), variance, standar deviation)
3. [marginal, conditional](https://www.youtube.com/watch?v=xu-HhF3SpbE&ab_channel=DataMListic) and [joint](https://www.youtube.com/watch?v=CQS4xxz-2s4&ab_channel=IntelligentSystemsLab) probabilities

### Underlying distribution

- In machine learning, we start with data. The distribution of the data we have in hand is representative of some underlying distribution of the data
- Whether it’s a probability mass function for a discrete random variable or a probability density function for a continuous random variable, some well-known and analytically well-understood functions, with characteristic parameters, can be used to describe the probability distributions of the data
- The parameters of a probability distribution model that distribution (p in bernoulli, mean and variance in normal...)

### Estimating the underlying distribution of the data and its parameters in supervised learning

- In supervised learning we are given some labeled data, X. Each instance of X is a d-dimensional vector, meaning it has d components. So, X is a matrix, where each row of the matrix is one instance of the data. Associated with each instance of X is a label, y
- If we knew the underlying probability distribution of P(X, y) we could calculate the probabilite for one class of y given an instance of X, this is called the Bayes optimal classifier
- Bayes optimal classifier it's the best an ML algorithm can do because it has access to the underlying distribution, wich in practice is almost impossible to know. So, the task of probabilistic ML algorithms, one can say, comes down to estimating the distribution from data
- Since finding the real underlying distribution is very difficult, we assume its type. Then given this assumed distribution there are two main ways of finding its parameters so its adjust to the data.
- MLE (maximum likelihood estimation)
- MAP (maximum a posteriori)
- 
