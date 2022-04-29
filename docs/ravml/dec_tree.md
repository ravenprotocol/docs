
<center>

# <B>  De </B>
</center>

Decision Tree is a supervised learning technique that may be used to solve both classification and regression problems, however, it is most commonly employed to solve classification issues. Internal nodes represent dataset attributes, branches represent decision rules, and each leaf node provides the conclusion in this tree-structured classifier. The Decision Node and the Leaf Node are the two nodes of a Decision tree. Leaf nodes are the output of those decisions and do not contain any more branches, whereas Decision nodes are used to make any decision and have several branches. The decisions or tests are made based on the characteristics of the given dataset.

```python
from ravml.tree import DecisionTreeClassifier

obj = DecisionTreeClassifier(max_depth=3)
obj.fit(X_train[:30], y_train[:30])
pr = obj.predict(X_test)
print(f1_score(y_test, pr, average='weighted'))

```


<B><center>
## Methods
</center>
</B>

- ### <B><U>fit(X,y)</u></B>

>
>
>| Parameters | Description     |
>| :------------ |:---------------:|
>|    X {dtype:list/numpy_ndarray) | array like matrix that is the training input array  | 
>|    y {dtype:list/numpy_ndarray) | array like matrix that is the input array  |


- ### <U><B>predict(X)</B><br></U>

> For the decision tree classification model, the predicted class for each sample in X is returned. For a regression model
>
>| Parameters | Description     |
>| :------------: |:---------------:|
>|    X {shape:(n_samples,n_features)} |New data to predict  | 





You can view the implementation of Decision Tree [*here*](https://github.com/ravenprotocol/ravml/blob/main/ravml/tree/decision_tree.py).

