# Support Vector Machine
SVM (Support Vector Machine) is a supervised machine learning technique that can be used to solve classification and regression problems. It is, however, mostly employed to solve categorization difficulties. Each data item is plotted as a point in n-dimensional space (where n is the number of features you have), with the value of each feature being the value of a certain coordinate in the SVM algorithm. Then we accomplish classification by locating the hyper-plane that clearly distinguishes the two classes.



<B><center>
## Methods
</center>
</B>

- ### <B><U>fit(X,k=3,iter=100)</u></B>

>Compute kmeans clustering for thr input dataset X. where k denotes the number of centroids and iteration
>
>| Parameters | Description     |
>| :------------ |:---------------:|
>|    X {dtype:list/numpy_ndarray,shape:(n_samples,n_features)} | array like matrix denoting the input array for clustering | 
>|    k {dtype: int } | Number of centroids for clustering  |  
>|    iter{dtype:int ,default value: 10}  | number of iterations we want our model to update its centroids |  
