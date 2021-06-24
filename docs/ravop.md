<div align="center">
 <h1> RavOP </h1>
</div>

[Github](https://github.com/ravenprotocol/ravop.git)

Ravop is the Raven Distribution framework’s (RDF) operation library . Ops are a fundamental unit of RDF. Ravop Library contains the main object data types `Tensor` and `Scalar` upon which we can perform the various arithmetic and mathematical operations available in the ravop library in a distributed and decentralized manner . 


Ravop in RDF
-
Ravop is responsible for creation of ops and retrieving ops from ravcom and ravsock. 

Setup and Installation
-

Create a virtual environment
    
    virtualenv ravop -p python3
    
Activate the virtual environment
    
    source ravop/bin/activate

Install RavOp

    pip install https://github.com/ravenprotocol/ravop.git


Initializing Tensors , Scalars and Graphs
    
`Tensors`:Raven Tensors are data type objects which are multidimensional arrays

`Scalars`:Raven data type object for `int` or `float` type.

`Graph`: For evaluating all the ops after creating it in a computational graph.

These data types can be initialized as follows: 
```python
import ravop.core as R
a=R.Tensor([1,2,3])
b=R.Scalar(10)
```


Example
-
We can use raven ops to operate on these Tensors. Let's consider adding two Tensors .
Adding two tensors can be achieved using the R.add() operation

 

```python
import ravop.core as R

#inittializing Tensors
a=R.Tensor([1,2,3])
b=R.Tensor([2,3,4])
    
#using add operation from ravop.core
c=R.add(a,b)
```

Raven supports Unary and Binary ops :

`unary ops`

```python
import ravop.core as R

#inittializing Tensor
a=R.Tensor([1,2,3])

#using min operation from ravop.core
c=R.min(a)
```

`Binary ops` :

```python
import ravop.core as R

#inittializing Tensors
a=R.Tensor([1,2,3])
b=R.Tensor([2,3,4])

#using multiply operation from ravop.core
c=R.multiply(a,b)
```


Arithmetic Ops
-

Op name |
|---|
|add|
|mul|
|sub|
|pos|
|neg|
|exp|
|natlog|
|pow|
|square|
|cube|
|square_root|
|cube_root|
|abs|


---
add
-

```python
a=R.Tensor([1,2,3])
b=R.Tensor([3,4,5])
c=R.add(a,b)
print(c.output)
```
`Parameters:`

**a (R.Tensor| Dtype:Ravop Tensor) :** The first input Tensor

**b (R.Tensor| Dtype: Ravop Tensor) :** The second input Tensor 

`Returns:`

R.Tensor()

---
mul
-
**Description:** Returns the elementwise multiplication between two tensors a and b

```python
a=R.Tensor([2,2])
b=R.Tensor([1,2])
R.mul(a,b)
```
`Parameters:`

**a (R.Tensor| Dtype:Ravop Tensor) :** The first input Tensor

**b (R.Tensor| Dtype: Ravop Tensor) :** The second input Tensor 

`Returns:`

R.Tensor()

---
sub
-
**Description:** Returns the elementwise subtraction between two tensors a and b

```python
a=R.Tensor([1,2,3])
b=R.Tensor([1,1,1])
R.sub(a,b)
```
`Parameters:`

**a (R.Tensor| Dtype:Ravop Tensor) :** The first input Tensor

**b (R.Tensor| Dtype: Ravop Tensor) :** The second input Tensor 

`Returns:`

R.Tensor()

---
pos
-
**Description:**

```python
a=R.Tensor([1,2,-3])
R.pos(a,b)
```
`Parameters:`

**a (R.Tensor| Dtype:Ravop Tensor) :** The first input Tensor

`Returns:`

R.Tensor()

---
neg
-
**Description:** Returns negative value of the tensor

```python
a=R.Tensor([1,-2,-3])
b=R.neg(a)
print(b.output)
```
    Output: array([-1,2,3])
`Parameters:`

**a (R.Tensor| Dtype:Ravop Tensor) :** The  input Tensor

`Returns:`

R.Tensor()

---
exp
-
**Description:** Returns exponential of input tensor

```python
a=R.Tensor([1,2,3])
b=R.exp(a)
print(b.output)
```

    Output: array([2.7182817459106445, 7.389056205749512, 20.08553695678711])
`Parameters:`

**a (R.Tensor| Dtype:Ravop Tensor) :** The first input Tensor

`Returns:`

R.Tensor()

---
natlog
-
**Description:** Returns natural log of input tensor

```python
a=R.Tensor([1,2,3])
b=R.natlog(a)
print(b.output)
```
    Output: array([0, 0.6931471824645996, 1.0986123085021973])
`Parameters:`

**a (R.Tensor| Dtype:Ravop Tensor) :** The first input Tensor

**b (R.Tensor| Dtype: Ravop Tensor) :** The second input Tensor 

`Returns:`

R.Tensor()

---
pow
-
**Description:** Returns a tensor element wise raised to the power of input tensor

```python
a=R.Tensor([1,2,3])
b=R.Tensor([1,2,3])
c=R.pow(a,b)
print(c.output)
```
    Output: array([1,4,27])
`Parameters:`

**a (R.Tensor| Dtype:Ravop Tensor) :** The first input Tensor

**b (R.Tensor| Dtype: Ravop Tensor) :** The second input Tensor 

`Returns:`

R.Tensor()

---
square
-
**Description:** Returns square of a tensor

```python
a=R.Tensor([1,2,3])
b=R.square(a)
print(b.output)
```
    Output: array([1,4,9])
`Parameters:`

**a (R.Tensor| Dtype:Ravop Tensor) :** The first input Tensor

`Returns:`

R.Tensor()

---
cube
-

**Description:** Returns cube of a tensor

```python
a=R.Tensor([1,2,3])
b=R.cube(a)
print(b.output)
```
    Output: array([1,8,27])
`Parameters:`

**a (R.Tensor| Dtype:Ravop Tensor) :** The first input Tensor

`Returns:`

R.Tensor()

---
square_root
-

**Description:** Returns square root of a tensor

```python
a=R.Tensor([16,4,9])
b=R.square(a)
print(b.output)
```
    Output: array([4,2,3])
`Parameters:`

**a (R.Tensor| Dtype:Ravop Tensor) :** The first input Tensor

`Returns:`

R.Tensor()

---
cube_root
-

**Description:** Returns cube root of a tensor

```python
a=R.Tensor([27,64,729])
b=R.cube_root(a)
print(b.output)
```
    Output: array([3,4,9])
`Parameters:`

**a (R.Tensor| Dtype:Ravop Tensor) :** The first input Tensor

`Returns:`

R.Tensor()

---
abs
-

**Description:** Returns absolute value of elements of a tensor

```python
a=R.Tensor([1,-2,-3])
b=R.square(a)
print(b.output)
```
    Output: array([1,2,3])
`Parameters:`

**a (R.Tensor| Dtype:Ravop Tensor) :** The first input Tensor

`Returns:`

R.Tensor()

---





Comparision Ops
-

Op name |
|---|
|greater|
|greater_equal|
|less|
|less_equal|
|equal|
|not_equal|


greater
-
**Description:** Returns truth value of (a>b) element-wise for two ravop Tensors a and b .
```python
a=R.Tensor([1,2,3])
b=R.Tensor([3,1,3])
c=R.greater(a,b)
print(c.output)
```
    Output: array([0,1,0])
    

`Parameters:`

**a (R.Tensor| Dtype:Ravop Tensor) :** The first input Tensor

**b (R.Tensor| Dtype: Ravop Tensor) :** The second input Tensor 

`Returns:`

R.Tensor()

---



greater_equal
-
**Description:** Returns truth value of (a >= b) element-wise for two ravop Tensors a and b .
```python
a=R.Tensor([1,2,3])
b=R.Tensor([3,1,3])
c=R.greater_equal(a,b)
print(c.output)
```

    Output: array([0,1,1])
`Parameters:`

**a (R.Tensor| Dtype:Ravop Tensor) :** The first input Tensor

**b (R.Tensor| Dtype: Ravop Tensor) :** The second input Tensor 

`Returns:`

R.Tensor()

---


less
-
**Description:** Returns truth value of (a < b) element-wise for two ravop Tensors a and b .
```python
a=R.Tensor([1,2,3])
b=R.Tensor([3,1,3])
c=R.less(a,b)
print(c.output)
```
    Output: array([1,0,0])

`Parameters:`

**a (R.Tensor| Dtype:Ravop Tensor) :** The first input Tensor

**b (R.Tensor| Dtype: Ravop Tensor) :** The second input Tensor 

`Returns:`

R.Tensor()





less_equal
-
**Description:** Returns truth value of (a <= b) element-wise for two ravop Tensors a and b .


```python
a=R.Tensor([1,2,3])
b=R.Tensor([3,4,3])
c=R.less_equal(a,b)
print(c.output)
```

    Output: array([1,0,1])


`Parameters:`

**a (R.Tensor| Dtype:Ravop Tensor) :** The first input Tensor

**b (R.Tensor| Dtype: Ravop Tensor) :** The second input Tensor 

`Returns:`

R.Tensor()

---
    
equal
-
**Description:** Returns truth value of (a == b) element-wise for two ravop Tensors a and b .


```python
a=R.Tensor([1,2,3])
b=R.Tensor([3,2,3])
R.equal(a,b)
```

    Output: array([0,1,1])
`Parameters:`

**a (R.Tensor| Dtype:Ravop Tensor) :** The first input Tensor

**b (R.Tensor| Dtype: Ravop Tensor) :** The second input Tensor 

`Returns:`

R.Tensor()

---

not_equal
-
**Description:** Returns truth value of (a != b) element-wise for two ravop Tensors a and b .


```python
a=R.Tensor([1,2,3])
b=R.Tensor([2,2,2])
c=R.not_equal(a,b)
print(c.output)
```

    Output: array([1,0,1])
`Parameters:`

**a (R.Tensor| Dtype:Ravop Tensor) :** The first input Tensor

**b (R.Tensor| Dtype: Ravop Tensor) :** The second input Tensor 

`Returns:`

R.Tensor()

---


Logical Operations
-

Op name |
|---|
|logical_and|
|logical_or|
|logical_not|
|logical_xor|

---

logical_and
-
**Description:** Returns truth values of 'logical and' operation between two tensors a and b.
```python
a=R.Tensor([True,True,False,False])
b=R.Tensor([True,False,True,False])
c=R.logical_and(a,b)
print(c.output)
```
    Output: array([1,0,0,0])
`Parameters:`

**a (R.Tensor| Dtype:Ravop Tensor) :** The first input Tensor

**b (R.Tensor| Dtype: Ravop Tensor) :** The second input Tensor 

`Returns:`

R.Tensor()

---


logical_or
-
**Description:** Returns truth values of 'logical or' operation between two tensors a and b.


```python
a=R.Tensor([True,True,False,False])
b=R.Tensor([True,False,True,False])
c=R.logical_or(a,b)
print(c.output)
```
`Parameters:`

**a (R.Tensor| Dtype:Ravop Tensor) :** The first input Tensor

**b (R.Tensor| Dtype: Ravop Tensor) :** The second input Tensor 

`Returns:`

R.Tensor()

---

logical_not
-
**Description:** Returns truth values of 'logical not' operation for a tensor a.

```python
a=R.Tensor([True,True,False])
c=R.logical_not(a)
print(c.output)
```
    Output: array([False,False,True])
`Parameters:`

**a (R.Tensor| Dtype:Ravop Tensor) :** The input Tensor

`Returns:`

R.Tensor()


---
logical_xor
-
**Description:** Returns truth values of 'logical xor' operation between two tensors a and b.

```python
a=R.Tensor([True,True,False,False])
b=R.Tensor([True,False,True,False])
c=R.logical_xor(a,b)
print(c.output)
```
    Output: array([])

`Parameters:`

**a (R.Tensor| Dtype:Ravop Tensor) :** The first input Tensor

**b (R.Tensor| Dtype: Ravop Tensor) :** The second input Tensor 

`Returns:`

R.Tensor()

---

Statistical Ops
-

Op name |
|---|
|mean|
|average|
|mode|
|median|
|variance|
|std|
|percentile|

---
mean
-
**Description:** Computes mean along the dimension of a ravop tensor.

```python
a=R.Tensor([[1,2],[2,4],[3,5]])
c1=R.mean(a,axis=0)
c2=R.mean(a,axis=1)
print(c1.output)
print(c2.output)
```
    Output: array([[2 , 3.66666675]])
            array([[1.5] , [3. ], [4. ]])

`Parameters:`

**a (R.Tensor| Dtype:Ravop Tensor) :** The  input Tensor

**axis (R.Scalar,int ) :** The axis along which to calculate the mean

`Returns:`

R.Tensor()


---
mode
-

**Description:** Computes mode along the dimension of a ravop tensor.


```python
a=R.Tensor([1,1,1,2,3,4])
c=R.mode(a ,axis=0)
print(c.output)
```
    Output: array([1])

`Parameters:`

**a (R.Tensor| Dtype:Ravop Tensor) :** The first input Tensor

**axis (R.Scalar, int ) :** The axis along which to calculate the mode

`Returns:`

R.Tensor()

---
median
-

**Description:** Computes median along the dimension of a ravop tensor.


```python
a=R.Tensor([1,1,1,2,3,4])
c=R.median(a ,axis=0)
print(c.output)
```
    Output: array([1.5])

`Parameters:`

**a (R.Tensor| Dtype:Ravop Tensor) :** The  input Tensor

**axis (R.Scalar, int ) :** The axis along which to calculate the median


`Returns:`

R.Tensor()

---
variance
-
**Description:** Computes variance along the dimension of a ravop tensor.

```python
a=R.Tensor([1,1,1,2,3,4])
c=R.median(a ,axis=0)
print(c.output)
```
    Output: array([1.6])

`Parameters:`

**a (R.Tensor| Dtype:Ravop Tensor) :** The first input Tensor

**axis (R.Scalar, int ) :** The axis along which to calculate the variance

`Returns:`

R.Tensor()

---
std
-
**Description:** Computes standard deviation along the dimension of a ravop tensor.

```python
a=R.Tensor([1,1,1,2,3,4])
c=R.median(a ,axis=0)
print(c.output)
```
    Output: 1.1547005383792515

`Parameters:`

**a (R.Tensor| Dtype:Ravop Tensor) :** The first input Tensor.

**axis (R.Scalar, int ) :** The axis along which to calculate the standard deviation.

`Returns:`

R.Tensor()

---
percentile
-

**Description:** Calculate percentile of a tensor.


```python
a=R.Tensor([1,2,3,4,5,6])
R.percentile(a ,value=1)
print(a.output)
```
    Output: 0.3333333334
`Parameters:`

**a (R.Tensor| Dtype:Ravop Tensor) :** The input Tensor

`Returns:`

R.Tensor()

---



Other Ops
-

Op name |
|---|
|random|
|bincount|
|where|
|sign|
|foreach|
|one_hot_encoding|
|matmul|
|multiply|
|dot|
|transpose|
|sum|
|sort|
|split|
|reshape|
|concat|
|min|
|max|
|unique|
|argmax|
|argmin|
|expand_dims|
|inv|
|gather|
|reverse|
|stack|
|tile|
|slice|
|find_indices|
|shape|


random
-
**Description:** generates a random tensor by randomly picking values from a input ravop tensor.

```python
a=R.Tensor([1,2,3,4,5,6])
c=R.random(a,size=3)
print(c.output)
```
    Output: [6,1,4]
`Parameters:`

**a (R.Tensor| Dtype:Ravop Tensor) :** The input Tensor

**size (int,R.Scalar) :** size of output tensor

`Returns:`

R.Tensor()

---

bincount
-
**Description:** : 

```python
a=R.Tensor([1,2,3])

```
`Parameters:`

**a (R.Tensor| Dtype:Ravop Tensor) :** The first input Tensor

**minlength (R.Scalar,int) :** 

**weights (array) :** 

`Returns:`

R.Tensor()

---

where
-
**Description:** Returns elements from a or b depending on the condition.

```python
a=R.Tensor([1,2,3])
b=R.Tensor([-6,-7,-8])
cond=[True,True,False]
c=R.where(a,b,condition=cond)
print(c.output)
```
    Output: array([1,2,-8])
`Parameters:`

**a (R.Tensor| Dtype:Ravop Tensor) :** The first input Tensor

**b (R.Tensor| Dtype: Ravop Tensor) :** The second input Tensor 

**b (ndarray, list) :** condition ,if true choose from a ,else choose from b.

`Returns:`

R.Tensor()

---

sign
-
**Description:** Returns an element-wise indication of the sign of a number.



```python
a=R.Tensor([0,1,-2,-1.4])
b=R.sign(a)
print(b.output)
```
    Output: array([0,1,-1,-1])
`Parameters:`

**a (R.Tensor| Dtype:Ravop Tensor) :** The  input Tensor

`Returns:`

R.Tensor()

---

foreach
-
**Description:** Apply a function from tenserflow.js to every element of the tensor

```python
a=R.Tensor([[1,2,3],[4,5,6],[6,7,8]])
b=R.foreach(a, operation='sum')
print(b.output)
```
    Output: array([6,15,21])
`Parameters:`

**a (R.Tensor| Dtype:Ravop Tensor) :** The input Tensor

**operation (str) :** name of the tfjs operation.

`Returns:`

R.Tensor()

---

one_hot_encoding
-
**Description:** creates a one hot ravop Tensor.

**Description:**
```python
a=R.Tensor([1,3,2])
b=R.one_hot_encoding(a ,depth=4)
print(b.output)
```
    Output: array([0,1,0,0]
                [0,0,0,1]
                [0,0,1,0])
`Parameters:`

**a (R.Tensor| Dtype:Ravop Tensor) :** The input Tensor

**depth (R.Tensor| Dtype: Ravop Tensor) :** depth of the one hot representation

`Returns:`

R.Tensor()

---

matmul
-
**Description:** Computes the dot product of two ravop tensors a and b.
```python
a=R.Tensor([[1,2],[3,6]])
b=R.Tensor([[3,4],[5,4]])
R.multiply(a,b)
```
    Output: array([[13,12],[39,36]])
`Parameters:`

**a (R.Tensor| Dtype:Ravop Tensor) :** The first input Tensor

**b (R.Tensor| Dtype: Ravop Tensor) :** The second input Tensor 

`Returns:`

R.Tensor()


---

multiply
-
**Description:** Computes the matrix multiplication of two ravop tensors a and b.
```python
a=R.Tensor([[1,2],[3,6]])
b=R.Tensor([[3,4],[5,4]])
R.multiply(a,b)
```
    Output: array([[3,8],[15,24]])
`Parameters:`

**a (R.Tensor| Dtype:Ravop Tensor) :** The first input Tensor

**b (R.Tensor| Dtype: Ravop Tensor) :** The second input Tensor 

`Returns:`

R.Tensor()

---

dot
-
**Description:** Computes the dot product of two ravop tensors a and b.
```python
a=R.Tensor([[1,2],[3,6]])
b=R.Tensor([[3,4],[5,4]])
R.dot(a,b)
```
    Output: array([[13,12],[39,36]])

`Parameters:`

**a (R.Tensor| Dtype:Ravop Tensor) :** The first input Tensor

**b (R.Tensor| Dtype: Ravop Tensor) :** The second input Tensor

`Returns:`

R.Tensor()

---

transpose
-
**Description:** Outputs transpose of a tensor matrix.
```python
a=R.Tensor([[1,2],[3,4]])
b=R.transpose(a)
print(b.output)
```
    Output: array([1,3]
                [2,4])


`Parameters:`

**a (R.Tensor| Dtype:Ravop Tensor) :** The input Tensor


`Returns:`

R.Tensor()

---

sum
-
**Description:** Outputs sum of elements in a tensor along a axis.
```python
a=R.Tensor([[1,2],[3,4]])
b=R.sum(a,axis=1)
print(b.output)
```
    Output: array([3,7])

`Parameters:`

**a (R.Tensor| Dtype:Ravop Tensor) :** The first input Tensor.

**axis (int) :** axis along which to calculate the sum of tensor.

`Returns:`

R.Tensor()

---
sort
-

**Description:** Sort a Tensor in ascending order.
```python
a=R.Tensor([[7,2,1,4]])
b=R.sort(a)
print(b)
```
    Output: array([1,2,4,7])

`Parameters:`

**a (R.Tensor| Dtype:Ravop Tensor) :** The first input Tensor.

`Returns:`

R.Tensor()

---

split
-

```python
a=R.Tensor([[1,2,3,4],[5,6,7,8]])
R.split(a)
```
`Parameters:`

**a (R.Tensor| Dtype:Ravop Tensor) :** The input Tensor

**numOrSizeSplits (int):** number of splits to be made.

**axis (int):** axis along which to be split.
 
`Returns:`

R.Tensor()

---

reshape
-
**Description:** Reshape a tensor into the given shape
```python
a=R.Tensor([[1,2],[3,4]])
b=R.reshape(a,shape=[4])
print(b.output)
```
    Output:array([1,2,3,4])
`Parameters:`

**a (R.Tensor| Dtype:Ravop Tensor) :** The first input Tensor

**shape (array,list) :** list denoting the shape of the output tensor 

`Returns:`

R.Tensor()

---

concat
-
**Description:** Concatenate a list of tensors along a axis
```python
a=R.Tensor([[1,2],[3,4]])
b=R.Tensor([[6,5],[7,8]])
c=R.concat(a,b,axis=1)
print(c.output)
```
    Output: array([1, 2, 6, 5]
            [3, 4, 7, 8])

`Parameters:`

**a (R.Tensor| Dtype:Ravop Tensor) :** The first input Tensor

**b (R.Tensor| Dtype: Ravop Tensor) :** The second input Tensor 

**axis(int):** axis along which to concatenate.

`Returns:`

R.Tensor()

---

min
-
**Description:** return minimum element in a Tensor
```python
a=R.Tensor([1,2,3,4,5])
b=R.min(a)
print(b.output)
```
    Output: 1

`Parameters:`

**a (R.Tensor| Dtype:Ravop Tensor) :** The input Tensor


`Returns:`

R.Tensor()

---

max
-
**Description:** Return maximum element in a Tensor

```python
a=R.Tensor([1,2,3,4,5])
b=R.max(a)
print(b.output)
```
    Output: 5

`Parameters:`

**a (R.Tensor| Dtype:Ravop Tensor) :** The input Tensor

`Returns:`

R.Tensor()

---
unique
-
**Description:** return unique elements in a Tensor

```python
a=R.Tensor([1,1,1,2,2,3,4,4,4])
b=R.unique(a)
print(b.output)
```
    Output: array([1,2,3,4])
`Parameters:`

**a (R.Tensor| Dtype:Ravop Tensor) :** The input Tensor

`Returns:`

R.Tensor()

---

argmax
-
**Description:** returns indices of maximum value in the tensor.

```python
a=R.Tensor([[1,2,3],[2,1,1]])
b=R.argmax(a,axis=1)
print(b.output)
```
    Output:array([2,0])
`Parameters:`

**a (R.Tensor| Dtype:Ravop Tensor) :** The input Tensor

**axis (int):** axis along which to find argmax

`Returns:`

R.Tensor()

---

argmin
-
**Description:** returns indices of minimum value in the tensor.

```python
a=R.Tensor([[1,2,3],[2,1,1]])
b=R.argmin(a,axis=1)
print(b.output)
```
    Output:array([2,0])


`Parameters:`

**a (R.Tensor| Dtype:Ravop Tensor) :** The input Tensor

**axis (int) :** axis along which to find argmax


`Returns:`

R.Tensor()

---

expand_dims
-
**Description:** increase the dimension of a tensor by 1. 
```python
a=R.Tensor([1,2,3])
b=R.expand_dims(a)
print(b.output)
```
    Output:array([[1,2,3]])

`Parameters:`

**a ( R.Tensor | Dtype:Ravop Tensor) :** The first input Tensor

**axis (int) :** axis along which to expand dimension

`Returns:`

R.Tensor()

---

inv
-
**Description:** outputs the inverse of a matrix tensor

```python
a=R.Tensor([[1,2],[3,4]])
b=R.inv(a)
print(b.output)
```
    Output: array([[-2 , 1 ],[1.5,-0.5]])


`Parameters:`

**a (R.Tensor| Dtype:Ravop Tensor) :** The input Tensor

`Returns:`

R.Tensor()

---

gather
-
**Description:** Get the elements of a Tensor by indices

```python
a=R.Tensor([1,2,3,4,5,6])
b=R.Tensor([1,3])
c=R.gather(a,b)
print(c.output)
```
    Output: array([2,4])


`Parameters:`

**a (R.Tensor| Dtype:Ravop Tensor) :** The input Tensor

**b (R.Tensor| Dtype: Ravop Tensor) :** The indices Tensor 

`Returns:`

R.Tensor()

---

reverse
-
**Description:** returns the tensor in reverse order.

```python
a=R.Tensor([1,2,3])
b=R.reverse(a)
print(b.output)
```
    Output: array([3,2,1])

`Parameters:`

**a (R.Tensor| Dtype:Ravop Tensor) :** The  input Tensor


`Returns:`

R.Tensor()

---

stack
-
**Description:**

```python
a=R.Tensor([[1,2,3],[3,4,5]])
R.stack(a,b)
```
`Parameters:`

**a (R.Tensor| Dtype:Ravop Tensor) :** The first input Tensor

**b (R.Tensor| Dtype: Ravop Tensor) :** The second input Tensor 

`Returns:`

R.Tensor()

---

slice
-

```python
a=R.Tensor([1,2,3,4,5,6])
b=R.slice(a,begin=2,size=2)
print(b.output)
```
`Parameters:`

**a (R.Tensor| Dtype:Ravop Tensor) :** The first input Tensor

**begin (int) :** which index to begin the slice from

**size (int) :** size of the output tensor.

`Returns:`

R.Tensor()

---

find_indices
-
**Description:** Get the indices of values in a tensor.

```python
a=R.Tensor([1,2,2,3,6,6,6,7])
b=R.find_indices(a,R.Tensor([1,6]))
print(b.output)
```
    Output: array([[0],[4,5,6]])

`Parameters:`

**a (R.Tensor| Dtype:Ravop Tensor) :** The  input Tensor

**b (R.Tensor| Dtype: Ravop Tensor) :** The Tensor denoting indices of elements we want

`Returns:`

R.Tensor()

---
shape
-
**Description:** Get the shape of a Tensor.

```python
a=R.Tensor([[1,2,3],[4,5,6]])
b=R.shape(a)
```
    Output: array([2,3])

`Parameters:`

**a (R.Tensor| Dtype:Ravop Tensor) :** The input Tensor


`Returns:`

R.Tensor()

---

