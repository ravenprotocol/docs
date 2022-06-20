<center><b>
<h1>

# Loss functions
</h1>
</center></b>

### loss functions in ravml written using the ravop library compute the different loss values.

<center>

# mean_absolute_error

</center>

Mean absolute error regression loss.
<u>

`Parameters:`<br></u>
><b><i>y_true</i></b>: array-like of shape (n_samples,) or (n_samples, n_outputs)
Ground truth (correct) target values.

><i><b>y_pred</b></i> : array-like of shape (n_samples,) or (n_samples, n_outputs)
Estimated target values.


<u>

### Returns:<br></u>
>Ravop Tensor Object.

<br>
<center>
<img src=files/mean_abs_e.png width=250 height= 85>
</center>

Usage:
 ```python
from ravml.losses import mean_absolute_error
''' y_true and y_pred '''

loss_val = mean_absolute_error(y_true,y_pred)
''' returns a ravop tensor object ''' 
 ```


<center>

# mean_squared_error
</center>


<center>
<img src=files/meansquarederror.png width=250 height= 75>
</center>
<u>

`Parameters:`<br></u>
><b><i>y_true</i></b>: array-like of shape (n_samples,) or (n_samples, n_outputs)
Ground truth (correct) target values.

><i><b>y_pred</b></i> : array-like of shape (n_samples,) or (n_samples, n_outputs)
Estimated target values.

### Returns:<br></u>
>Ravop Tensor Object.

<br>    

 ```python
from ravml.losses import mean_squared_error
'''
y_true and y_pred
'''

loss_val = mean_squared_error(y_true,y_pred)
''' returns a ravop tensor object ''' 
 ```


<br><br>







<center>

# root_mean_squared_error
</center>


    description of rmse
<center>
<img src=files/rootmeansquarederror.png width=250 height= 85>
</center>
<u>

`Parameters:`<br></u>
><b><i>y_true</i></b>: array-like of shape (n_samples,) or (n_samples, n_outputs)
Ground truth (correct) target values.

><i><b>y_pred</b></i> : array-like of shape (n_samples,) or (n_samples, n_outputs)
Estimated target values.
    
### Returns:<br></u>
>Ravop Tensor Object.


 ```python
from ravml.losses import root_mean_squared_error
'''
y_true and y_pred
'''

loss_val = root_mean_squared_error(y_true,y_pred)
''' returns a ravop tensor object ''' 
 ```


<br><br>









<center>

# mean_squared_log_error
</center>
    

<center>
<img src=files/rmsle.png width=250 height= 85>
</center>
<u>

`Parameters:`<br></u>
><b><i>y_true</i></b>: array-like of shape (n_samples,) or (n_samples, n_outputs)
Ground truth (correct) target values.

><i><b>y_pred</b></i> : array-like of shape (n_samples,) or (n_samples, n_outputs)
Estimated target values.

### Returns:<br></u>
>Ravop Tensor Object.

 ```python
from ravml.losses import mean_squared_log_error
'''
y_true and y_pred
'''

loss_val = mean_squared_log_error(y_true,y_pred)
''' returns a ravop tensor object ''' 
 ```






<br><br>

<center>

# log_loss
</center>

    description of log loss
<center>
<img src=files/mean_abs_e.png width=250 height= 85>
</center>
<u>
`Parameters:` <br></u>
><b><i>y_true</i></b>: array-like of shape (n_samples,) or (n_samples, n_outputs)
Ground truth (correct) target values.

><i><b>y_pred</b></i> : array-like of shape (n_samples,) or (n_samples, n_outputs)

### Returns:<br></u>
>Ravop Tensor Object.


<br><br>





<center>

# one_hot_cross_entropy
</center>

    description of  one hot cross entropy

<center>
<img src=files/mean_abs_e.png width=250 height= 85>
</center>
<u>

### Parameters:<br></u>
><b><i>y_true</i></b>: array-like of shape (n_samples,) or (n_samples, n_outputs)
Ground truth (correct) target values.

><i><b>y_pred</b></i> : array-like of shape (n_samples,) or (n_samples, n_outputs)
Estimated target values.


### Returns:<br></u>
>Ravop Tensor Object.

<br><br>






<center>

# sparse_cross_entropy
</center>
    description of 

<center>
<img src=files/mean_abs_e.png width=250 height= 85>
</center>

<u>

### Parameters:<br></u>
><b><i>y_true</i></b>: array-like of shape (n_samples,) or (n_samples, n_outputs)
Ground truth (correct) target values.

><i><b>y_pred</b></i> : array-like of shape (n_samples,) or (n_samples, n_outputs)
Estimated target values.

### Returns:<br></u>
>Ravop Tensor Object.

<br><br>








<center>

# categorical_hinge
</center>

<center>
<img src=files/mean_abs_e.png width=250 height= 85>
</center>
<u>

### Parameters:<br></u>
><b><i>y_true</i></b>: array-like of shape (n_samples,) or (n_samples, n_outputs)
Ground truth (correct) target values.

><i><b>y_pred</b></i> : array-like of shape (n_samples,) or (n_samples, n_outputs)
Estimated target values.
    description of mse

### Returns:<br></u>
>Ravop Tensor Object.

<br><br>



<h1>

# Huber loss

</h1>

<center>
<img src=files/mean_abs_e.png width=250 height= 85>
</center>

<u>

`Parameters:`<br></u>



><b><i>y_true</i></b>: array-like of shape (n_samples,) or (n_samples, n_outputs)
Ground truth (correct) target values.

><i><b>y_pred</b></i> : array-like of shape (n_samples,) or (n_samples, n_outputs)
Estimated target values.
    description of mse


### Returns:<br></u>
>Ravop Tensor Object.

<br><br>



<h1>

# KL_div_loss
</h1>
    description of 


<u>

### Parameters:<br></u>
><b><i>y_true</i></b>: array-like of shape (n_samples,) or (n_samples, n_outputs)
Ground truth (correct) target values.

><i><b>y_pred</b></i> : array-like of shape (n_samples,) or (n_samples, n_outputs)
Estimated target values.

### Returns:<br>
>Ravop Tensor Object.

<br><br>



<h1>

# Poisson_loss
</h1>



<u>

`Parameters:`<br></u>
><b><i>y_true</i></b>: array-like of shape (n_samples,) or (n_samples, n_outputs)
Ground truth (correct) target values.

><i><b>y_pred</b></i> : array-like of shape (n_samples,) or (n_samples, n_outputs)
Estimated target values.

### Returns:<br></u>
>Ravop Tensor Object.

<br><br>


<u>
<h1>

# Logcosh </u></h1>





`Parameters:`<br>
><b><i>y_true</i></b>: array-like of shape (n_samples,) or (n_samples, n_outputs)
Ground truth (correct) target values.

><i><b>y_pred</b></i> : array-like of shape (n_samples,) or (n_samples, n_outputs)
Estimated target values.
 
### Returns:<br></u>
>Ravop Tensor Object.

<br><br>
