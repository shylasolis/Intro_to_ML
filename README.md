# Most Important Aspect to Machine Learning

After watching a Cornell University lecture, I learned the biggest key to learn is how to choose a machine learning algorithm and leverage its assumptions. 

* First analyze, ask myself, "What are the properties of this data set?"
* What assumptions can I make? Do these assumptions hold?
* What algorithm leverages these assumptions and makes the prediction?
* If you dont know anything about the data, instead you can just use lots of different algorithms and create different models and compare the training and test validation sets


The simplest algorithm is K-Nearest Neighbor from 1967
* Binary Classification Problem
* Makes the assumption that data points that are simliar, have similar labels
* This algortihm is only as good as it's distance metric. This means if the the distance metric is showing similrity in labels (most common is the Minkowski Distance) (distance can also be learned) When p=1, Manhatten; When p=2, Euclideon; When p=infinity, Max.
* Knn will not work for high dimensional data (mathematically, as d goes to infinity, the probability of the point landing between 0 and 1 to the power of d is zero. ) https://www.youtube.com/watch?v=BbYV8UfMJSA&t=546s 
* Your data has to lie in a low dimensional subspace or it lies in a low dimensional submanifold which is low dimension. (reduce the dimensionality during preprocessing e.g. PCA is a dimentionality reduction algorithm)
* Must consider "Curse of dimensionality"; When there are too many dimensions, all neighbors are close. 
* If n becomes really really large it becomes a really good classifier, but it also becomes really slow!


* Advantages Versus Disadvantages
* *Disadvantages: You have to sift through all training data points to calculate the distances for each test point. The complexity for testing is O(nd)

* First, grab a new data point, ask, is it a cross or a zero?
* Look at the test point, x, from the dataset D. Then look at the K-Nearest Neighbors from the training points(usually k is an odd number)

