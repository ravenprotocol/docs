<div align="center">
 <h1> RavOP </h1>
</div>

[Github](https://github.com/ravenprotocol/ravop.git)

Ravop is the Raven Distribution framework’s (RDF) operation library . Ops are a fundamental unit of RDF. Ravop Library contains the main object data types `Tensor` and `Scalar` upon which we can perform the various arithmetic and mathematical operations available in the ravop library in a distributed and decentralized manner . 


###Ravop in RDF
Ravop is responsible for creation of ops and retrieving ops from ravcom and ravsock. 
### Setup and Installation

Create a virtual environment
    
    virtualenv ravop -p python3
    
Activate the virtual environment
    
    source ravop/bin/activate

Install RavOp

    pip install https://github.com/ravenprotocol/ravop.git


### Initializing Tensors , Scalars and Graphs
    
`Tensors`:Raven Tensors are data type objects which are multidimensional arrays

`Scalars`:Raven data type object for `int` or `float` type.

`Graph`: For evaluating all the ops after creating it in a computational graph.

These data types can be initialized as follows: 

    import ravop.core as R

    a=R.Tensor([1,2,3])

    b=R.Scalar(10)



###Example
We can use raven ops to operate on these Tensors. Let's consider adding two Tensors .
Adding two tensors can be achieved using the R.add() operation

 

    import ravop.core as R
    #inittializing Tensors
    a=R.Tensor([1,2,3])
    b=R.Tensor([2,3,4])
    
    #using add operation from ravop.core
    c=R.add(a,b)

Raven supports Unary and Binary ops :

`unary ops`

    import ravop.core as R
    #inittializing Tensor
    a=R.Tensor([1,2,3])
    #using min operation from ravop.core
    c=R.min(a)


`Binary ops` :

    import ravop.core as R
    #inittializing Tensors
    a=R.Tensor([1,2,3])
    b=R.Tensor([2,3,4])
    #using multiply operation from ravop.core
    c=R.multiply(a,b)
##Supported Ops
Arithmetic Ops 

Op name |parameters|
|---|---|
|lin|
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

Comparision Opa

Op name |parameters|
|---|---|
|greater|
|greater_equal|
|less|
|less_equal|
|equal|
|not_equal|

Logical Operations

Op name |parameters|
|---|---|
|logical_and|
|logical_or|
|logical_not|
|logical_xor|

Statistical Ops

Op name |parameters|
|---|---|
|mean|
|average|
|mode|
|median|
|variance|
|std|
|percentile|

Tensor Ops

Op name |parameters|
|---|---|
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








##### This step will automatically install the dependencies