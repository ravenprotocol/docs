# Naive Bayes Classifier
It's a classification method based on Bayes' Theorem and the assumption of predictor independence. A Naive Bayes classifier, in simple terms, assumes that the existence of one feature in a class is unrelated to the presence of any other feature. The Naive Bayes model is simple to construct and is especially good for huge data sets. Naive Bayes is renowned to outperform even the most advanced classification systems due to its simplicity.


<B><center>
## Methods
</center>
</B>

- ### <B><U>fit(X,k=3,iter=100)</u></B>

>Compute kmeans clustering for thr input dataset X. where k denotes the number of centroids and iteration
>
>| Parameters | Description     |
>| :------------ |:---------------:|
>|    X {dtype:list/numpy_ndarray)} | array like matrix (input array) | 
 >|    Y {dtype:list/numpy_ndarray} | array like matrix (input array) | 
  





- ### <B><U>predict(X_test)</u></B>

>predict function for naive bayes classifier which predicts the output  
>
>| Parameters | Description     |
>| :------------ |:---------------:|
>|    X {dtype:list/numpy_ndarray)} | array like matrix (input array) | 
>|    Y {dtype:list/numpy_ndarray} | array like matrix (input array) 


```python
from ravml.linear_model.naive_bayes import NaiveBayesClassifier

model = NaiveBayesClassifier()

model.fit(X_train, y_train)
y_preds = model.predict(X_test)

calc_preds = []
for y_pred in y_preds:
    keys = list(y_pred.keys())
    calc_pred = {key: y_pred[key]() for key in keys}
    calc_preds.append(calc_pred)

MAPs = []
for pred in calc_preds:
    MAP = max(pred, key= pred.get)
    MAPs.append(MAP)

print("NaiveBayesClassifier accuracy: {0:.3f}".format(model.accuracy(y_test, MAPs)))
```



You can view a sample implementation of Naive Bayes on ravml [here](https://github.com/ravenprotocol/ravml/blob/main/examples/naive_bayes_classifier.py)