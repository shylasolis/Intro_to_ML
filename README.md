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

* First, grab a new data point, ask, is it a cross or a zero?
* Look at the test point, x, from the dataset D. Then look at the K-Nearest Neighbors (usually k is an odd number)
