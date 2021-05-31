# RavML
Raven Distribution Framework's Machine Learning Library

RavML is the machine learning library based on RavOp. It contains implementations of various machine learning algorithms like ordinary least squares, linear regression, logistic regression, KNN, Kmeans, Mini batch Kmeans, Decision Tree classifier, and Naive Bayes classifier


[Github](https://github.com/ravenprotocol/ravml.git)

## Installation

Create a virtual environment
    
    virtualenv ravml -p python3
    
Activate the virtual environment
    
    source ravml/bin/activate

Install Dependencies

    pip install git+https://github.com/ravenprotocol/ravml.git

Install Ravml

    python3 setup.py install
###### use `python3 setup --help` for argument details

## Available Algorithms

### K-Nearest Neighbours
K-Nearest Neighbors (KNN) is a simple machine learning technique for regression and classification problems. KNN algorithms take data and apply similarity metrics to classify fresh data points (e.g. distance function). A majority vote of its neighbours is used to classify it. The information is assigned to the class with the most neighbours. As the number of nearest neighbours grows, so does the value of k, and so does the accuracy.

### Naive Bayes Classifier
It's a classification method based on Bayes' Theorem and the assumption of predictor independence. A Naive Bayes classifier, in simple terms, assumes that the existence of one feature in a class is unrelated to the presence of any other feature. The Naive Bayes model is simple to construct and is especially good for huge data sets. Naive Bayes is renowned to outperform even the most advanced classification systems due to its simplicity.

### Support Vector Machine
SVM (Support Vector Machine) is a supervised machine learning technique that can be used to solve classification and regression problems. It is, however, mostly employed to solve categorization difficulties. Each data item is plotted as a point in n-dimensional space (where n is the number of features you have), with the value of each feature being the value of a certain coordinate in the SVM algorithm. Then we accomplish classification by locating the hyper-plane that clearly distinguishes the two classes.
### K-Means
### Linear Regression
### Logistic Regression
### Multi-Layer Perceptron
### Decision Trees
