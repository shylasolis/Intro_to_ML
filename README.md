# Most Important Aspect to Machine Learning

After watching a Cornell University lecture, I learned the biggest key to learn is how to choose a machine learning algorithm and leverage its assumptions. 

* First analyze, ask myself, "What are the properties of this data set?"
* What assumptions can I make? Do these assumptions hold?
* What algorithm leverages these assumptions and makes the prediction?
* If you dont know anything about the data, instead you can just use lots of different algorithms and create different models and compare the training and test validation sets

The Perceptron (1957) by Rosenblatt 
* An algorithm for supervised learning of binary classifiers
* Makes the assumption that there must be a hyper plane that seperates one class from the other "There exists a hyperplane such that all the points from one class lay on one side of the hyperplane, while all the points from the other class lay on the other side of the hyperplane" Note: This does not hold for low dimensional spaces, but it most likely will work for high dimensions
* Assumes the data is linearly separable
* Works in high dimensional spaces
* Does not work for all data sets (Need a hyperplane that divides the set dependent on the classes)
* During training this algorithm will find a hyperplane if it exists
* Defining the hyperplane: H={x: w^(T)x+b=0} (it's one dimension, but the data is in two dimensions)
* During testing, take the sign of the computed hyperplane: sign(w^(T)x+b) If >0 its on one side of the hyperplane, if <0 its on the other side, if =0 lands on the hyperplane. If t lands on the hyperplane, you get out a coin and flip it, if its heads its here and if it's tails its the other side. Assign y={-1,+1} (like O and X). Must learn 2 things, W and b. However, instead of finding two things we can reduce the number of things we need to find by using the dot product against [xi, 1] with [W, b], this makes H={x: W^Tx=0, using W bar and X bar}
* You start off with the W vector being zero, yi are either +1 or -1, set a variable m to count for the number of points miss classified. while no points are missclasified, then for all points in the data set, if yw^(T)x <=0 then w becomes w+yx, also increase m, the counter, to be m=m+1. Outside the for loop, check, if m=0 then your done. If there exist suh a hyperplane then the algorithm will converge.  

The simplest algorithm is K-Nearest Neighbor from 1967
* Binary Classification Problem
* Makes the assumption that data points that are simliar, have similar labels
* Works on data sets even if they are not linearly separable
* This algortihm is only as good as it's distance metric. This means if the the distance metric is showing similrity in labels (most common is the Minkowski Distance) (distance can also be learned) When p=1, Manhatten; When p=2, Euclideon; When p=infinity, Max.
* Knn will not work for high dimensional data (mathematically, as d goes to infinity, the probability of the point landing between 0 and 1 to the power of d is zero. ) https://www.youtube.com/watch?v=BbYV8UfMJSA&t=546s 
* Your data has to lie in a low dimensional subspace or it lies in a low dimensional submanifold which is low dimension. (reduce the dimensionality during preprocessing e.g. PCA is a dimentionality reduction algorithm)
* Must consider "Curse of dimensionality"; When there are too many dimensions, all neighbors are close. Note: You want to use knn in low dimensional space because curse of dimentionality doesn't kick you and because it will be alot faster with less dimensions (you have to compute lots of distances)
* If n becomes really really large it becomes a really good classifier, but it also becomes really slow!


* Advantages Versus Disadvantages
* *Disadvantages: You have to sift through all training data points to calculate the distances for each test point. The complexity for testing is O(nd)

* First, grab a new data point, ask, is it a cross or a zero?
* Look at the test point, x, from the dataset D. Then look at the K-Nearest Neighbors from the training points(usually k is an odd number)

