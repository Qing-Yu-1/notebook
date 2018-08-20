```
hw12 = '%s %s %d' % (hello, world, 12)  # sprintf style string formatting
print (hw12)  # prints "hello world 12"
```
#### list（列表）
If you want access to the index of each element within the body of a loop, use the built-in `enumerate` function:
```
animals = ['cat', 'dog', 'monkey']
for idx, animal in enumerate(animals):
    print ('#%d: %s' % (idx + 1, animal))
```
#1: cat<Br/>
#2: dog<Br/>
#3: monkey<Br/>

#### Dictionaries（字典）
It is easy to iterate over the keys in a dictionary:(迭代ｋｅｙ)
```
d = {'person': 2, 'cat': 4, 'spider': 8}
for animal in d:
    legs = d[animal]
    print ('A %s has %d legs' % (animal, legs))
```
A person has 2 legs<Br/>
A cat has 4 legs<Br/>
A spider has 8 legs<Br/>

If you want access to keys and their corresponding values, use the iteritems method:<Br/>
```
d = {'person': 2, 'cat': 4, 'spider': 8}
for animal, legs in d.iteritems():
    print 'A %s has %d legs' % (animal, legs)
```
A person has 2 legs<Br/>
A spider has 8 legs<Br/>
A cat has 4 legs<Br/>

Dictionary comprehensions: These are similar to list comprehensions, but allow you to easily construct dictionaries. For example:
```nums = [0, 1, 2, 3, 4]
even_num_to_square = {x: x ** 2 for x in nums if x % 2 == 0}
print (even_num_to_square)
```
{0: 0, 2: 4, 4: 16}

#### Sets（集合）
A set is an unordered collection of distinct elements. As a simple example, consider the following:
```
animals = {'cat', 'dog'}
print ('cat' in animals)   # Check if an element is in a set; prints "True"
print ('fish' in animals)  # prints "False"
```
True<Br/>
False<Br/>

```
animals.add('fish')      # Add an element to a set
print ('fish' in animals)
print (len(animals))       # Number of elements in a set;
```
True<Br/>
3<Br/>

```
animals.add('cat')       # Adding an element that is already in the set does nothing
print len(animals)       
animals.remove('cat')    # Remove an element from a set
print len(animals)  
```
3<Br/>
2<Br/>

Set comprehensions: Like lists and dictionaries, we can easily construct sets using set comprehensions:
```
from math import sqrt
print ({int(sqrt(x)) for x in range(30)})
```
{0, 1, 2, 3, 4, 5}<Br/>

#### Tuples(元组）
A tuple is an (immutable) ordered list of values. A tuple is in many ways similar to a list; one of the most important differences is that tuples can be used as keys in dictionaries and as elements of sets, while lists cannot. Here is a trivial example:
```
d = {(x, x + 1): x for x in range(10)}  # Create a dictionary with tuple keys
t = (5, 6)       # Create a tuple
print (type(t))
print (d[t])       
print (d[(1, 2)])
```
<class 'tuple'><Br/>
5<Br/>
1<Br/>
```
print(d)
```
```
{(0, 1): 0, (1, 2): 1, (2, 3): 2, (3, 4): 3, (4, 5): 4, (5, 6): 5, (6, 7): 6, (7, 8): 7, (8, 9): 8, (9, 10): 9}
```

### Functions
Python functions are defined using the `def` keyword. For example:
```
def sign(x):
    if x > 0:
        return 'positive'
    elif x < 0:
        return 'negative'
    else:
        return 'zero'

for x in [-1, 0, 1]:
    print sign(x)
```
```
negative
zero
positive
```
We will often define functions to take optional keyword arguments, like this:
```
def hello(name, loud=False):
    if loud:
        print 'HELLO, %s' % name.upper()
    else:
        print 'Hello, %s!' % name

hello('Bob')
hello('Fred', loud=True)
```
```
Hello, Bob!
HELLO, FRED
```
### Classes
The syntax for defining classes in Python is straightforward:
```
class Greeter:

    # Constructor
    def __init__(self, name):
        self.name = name  # Create an instance variable

    # Instance method
    def greet(self, loud=False):
        if loud:
            print 'HELLO, %s!' % self.name.upper()
        else:
            print 'Hello, %s' % self.name

g = Greeter('Fred')  # Construct an instance of the Greeter class
g.greet()            # Call an instance method; prints "Hello, Fred"
g.greet(loud=True)   # Call an instance method; prints "HELLO, FRED!"
```
```
Hello, Fred
HELLO, FRED!
```
## Numpy
Numpy is the core library for scientific computing in Python. It provides a high-performance multidimensional array object, and tools for working with these arrays. If you are already familiar with MATLAB, you might find this [tutorial](http://wiki.scipy.org/NumPy_for_Matlab_Users) useful to get started with Numpy.<Br/>
To use Numpy, we first need to import the `numpy` package:
```
import numpy as np
```
### Arrays
A numpy array is a grid of values, all of the same type, and is indexed by a tuple of nonnegative integers. The number of dimensions is the rank of the array; the shape of an array is a tuple of integers giving the size of the array along each dimension.<Br/>
We can initialize numpy arrays from nested（嵌入的） Python lists, and access elements using square brackets(方括号）:<Br/>
```
a = np.array([1, 2, 3])  # Create a rank 1 array
print type(a), a.shape, a[0], a[1], a[2]
a[0] = 5                 # Change an element of the array
print a                  
```
```
<type 'numpy.ndarray'> (3,) 1 2 3
[5 2 3]
```
```
b = np.array([[1,2,3],[4,5,6]])   # Create a rank 2 array
print (b)
```
```
[[1 2 3]
 [4 5 6]]
 ```
 ```
 print (b.shape)                   
print (b[0, 0], b[0, 1], b[1, 0])
```
```
(2, 3)
1 2 4
```
```
a = np.zeros((2,2))  # Create an array of all zeros
print (a)
```
```
[[ 0.  0.]
 [ 0.  0.]]
 ```
```
b = np.ones((1,2))   # Create an array of all ones
print b
```
```
[[1. 1.]]
```
```
c = np.full((2,2), 7) # Create a constant array
print c 
```
```
[[ 7.  7.]
 [ 7.  7.]]
 ```
```
d = np.eye(2)        # Create a 2x2 identity matrix
print d
```
```
[[ 1.  0.]
 [ 0.  1.]]
 ```
```
e = np.random.random((2,2)) # Create an array filled with random values
print (e)
```
```
[[ 0.09477679  0.79267634]
 [ 0.78291274  0.38962829]]
 ```
### Array indexing
Numpy offers several ways to index into arrays.<Br/>
Slicing: Similar to Python lists, numpy arrays can be sliced. Since arrays may be multidimensional, you must specify a slice for each dimension of the array:<br/>
```
import numpy as np

# Create the following rank 2 array with shape (3, 4)
# [[ 1  2  3  4]
#  [ 5  6  7  8]
#  [ 9 10 11 12]]
a = np.array([[1,2,3,4], [5,6,7,8], [9,10,11,12]])

# Use slicing to pull out the subarray consisting of the first 2 rows
# and columns 1 and 2; b is the following array of shape (2, 2):
# [[2 3]
#  [6 7]]
b = a[:2, 1:3]#切片的方法＝结果是同维度的　 a[2, 1:3]＝降一个维度
print (b)
```
```
[[2 3]
 [6 7]]
 ```
 A slice of an array is a view into the same data, so modifying it will modify the original array.
 ```
 print (a[0, 1])  
b[0, 0] = 77    # b[0, 0] is the same piece of data as a[0, 1]
print (a[0, 1])
```
```
2
77
```
You can also mix integer indexing with slice indexing. However, doing so will yield an array of lower rank（降维度） than the original array. Note that this is quite different from the way that MATLAB handles array slicing:
```
# Create the following rank 2 array with shape (3, 4)
a = np.array([[1,2,3,4], [5,6,7,8], [9,10,11,12]])
print (a)
```
```
[[ 1  2  3  4]
 [ 5  6  7  8]
 [ 9 10 11 12]]
 ```
 Two ways of accessing the data in the middle row of the array. Mixing integer indexing with slices yields an array of lower rank, while using only slices yields an array of the same rank as the original array:
 ```
 row_r1 = a[1, :]    # Rank 1 view of the second row of a  
row_r2 = a[1:2, :]  # Rank 2 view of the second row of a
row_r3 = a[[1], :]  # Rank 2 view of the second row of a
print (row_r1, row_r1.shape)
print (row_r2, row_r2.shape)
print (row_r3, row_r3.shape)
```
```
[5 6 7 8] (4,)#　降一个维度
[[5 6 7 8]] (1, 4)
[[5 6 7 8]] (1, 4)
```
```
# We can make the same distinction when accessing columns of an array:
col_r1 = a[:, 1]
col_r2 = a[:, 1:2]
print (col_r1, col_r1.shape)
print()
print (col_r2, col_r2.shape)
```
```
[ 2  6 10] (3,)

[[ 2]
 [ 6]
 [10]] (3, 1)
 ```
 Integer array indexing: When you index into numpy arrays using slicing, the resulting array view will always be a subarray （子数组）of the original array. In contrast, integer array indexing allows you to construct arbitrary(任意的） arrays using the data from another array. Here is an example:
```
a = np.array([[1,2], [3, 4], [5, 6]])# 使用列表构建数组　[[1,2], [3, 4], [5, 6]]　是一个列表

# An example of integer array indexing.
# The returned array will have shape (3,) and 
print (a[[0, 1, 2], [0, 1, 0]])　＃[[0, 1, 2], [0, 1, 0]]是一个列表　这里代表一个数组索引

# The above example of integer array indexing is equivalent to this:
print (np.array([a[0, 0], a[1, 1], a[2, 0]]))　＃[a[0, 0], a[1, 1], a[2, 0]]是一个列表　然后通过np.array转换为数组
```
```
[1 4 5]
[1 4 5]
```
One useful trick with integer array indexing is selecting or mutating one element from each row of a matrix:
```
# Create a new array from which we will select elements
a = np.array([[1,2,3], [4,5,6], [7,8,9], [10, 11, 12]])
print (a)
```
```
[[ 1  2  3]
 [ 4  5  6]
 [ 7  8  9]
 [10 11 12]]
 ```
```
# Create an array of indices
b = np.array([0, 2, 0, 1])
# Select one element from each row of a using the indices in b
print (a[np.arange(4), b])  # Prints "[ 1  6  7 11]"
```
```
[ 1  6  7 11]
```
```
[np.arange(4),b]
```
### Datatypes
Every numpy array is a grid of elements of the same type. Numpy provides a large set of numeric datatypes that you can use to construct arrays. Numpy tries to guess a datatype when you create an array, but functions that construct arrays usually also include an optional argument to explicitly specify the datatype. Here is an example:
```
x = np.array([1, 2])  # Let numpy choose the datatype
y = np.array([1.0, 2.0])  # Let numpy choose the datatype
z = np.array([1, 2], dtype=np.int64)  # Force a particular datatype

print x.dtype, y.dtype, z.dtype
```
```
int64 float64 int64
```
### Array math
Note that unlike MATLAB, * is elementwise multiplication, not matrix multiplication. We instead use the dot function to compute inner products of vectors, to multiply a vector by a matrix, and to multiply matrices. dot is available both as a function in the numpy module and as an instance method of array objects:
```
x = np.array([[1,2],[3,4]])
y = np.array([[5,6],[7,8]])

v = np.array([9,10])
w = np.array([11, 12])

# Inner product of vectors; both produce 219
print (v.dot(w))
print (np.dot(v, w))
```
```
219
219
```
```
# Matrix / vector product; both produce the rank 1 array [29 67]
print x.dot(v)
print np.dot(x, v)
```
```
[29 67]
[29 67]
```
```
# Matrix / matrix product; both produce the rank 2 array
# [[19 22]
#  [43 50]]
print x.dot(y)
print np.dot(x, y)
```
```
[[19 22]
 [43 50]]
[[19 22]
 [43 50]]
 ```
 Numpy provides many useful functions for performing computations on arrays; one of the most useful is `sum`:
 ```
 x = np.array([[1,2],[3,4]])

print np.sum(x) # Compute sum of all elements; prints "10"
print np.sum(x, axis=0)  # Compute sum of each column; prints "[4 6]"
#[1 2]
#[3 4]

#[4 6]

#prints "[4 6]"

print np.sum(x, axis=1)  # Compute sum of each row; prints "[3 7]"
#[1 2]
#[3 4]

#[3]
#[7]

#prints "[3 7]"
```
```
10
[4 6]
[3 7]
```
Apart from computing mathematical functions using arrays, we frequently need to reshape or otherwise manipulate data in arrays. The simplest example of this type of operation is transposing a matrix; to transpose a matrix, simply use the T attribute of an array object:
```
print x
print x.T
```
```
[[1 2]
 [3 4]]
[[1 3]
 [2 4]]
 ```
```
v = np.array([[1,2,3]])
print v 
print v.T
```
```
[1 2 3]
[1 2 3]
```
### Broadcasting
Broadcasting is a powerful mechanism that allows numpy to work with arrays of different shapes when performing arithmetic operations. Frequently we have a smaller array and a larger array, and we want to use the smaller array multiple times to perform some operation on the larger array.<br/>

For example, suppose that we want to add a constant vector to each row of a matrix. We could do it like this:

```
# We will add the vector v to each row of the matrix x,
# storing the result in the matrix y
x = np.array([[1,2,3], [4,5,6], [7,8,9], [10, 11, 12]])
v = np.array([1, 0, 1])
y = np.empty_like(x)   # Create an empty matrix with the same shape as x

# Add the vector v to each row of the matrix x with an explicit loop
for i in range(4):
    y[i, :] = x[i, :] + v

print y
```
```
[[ 2  2  4]
 [ 5  5  7]
 [ 8  8 10]
 [11 11 13]]
 ```
This works; however when the matrix x is very large, computing an explicit loop in Python could be slow. Note that adding the vector v to each row of the matrix x is equivalent to forming a matrix vv by stacking multiple copies of v vertically, then performing elementwise summation of x and vv. We could implement this approach like this:

```
vv = np.tile(v, (4, 1))  # Stack 4 copies of v on top of each other
print vv                 # Prints "[[1 0 1]
                         #          [1 0 1]
                         #          [1 0 1]
                         #          [1 0 1]]"
```
```
[[1 0 1]
 [1 0 1]
 [1 0 1]
 [1 0 1]]
```
```
y = x + vv  # Add x and vv elementwise
print y
[[ 2  2  4]
 [ 5  5  7]
 [ 8  8 10]
 [11 11 13]]
 ```
Numpy broadcasting allows us to perform this computation without actually creating multiple copies of v. Consider this version, using broadcasting:

```
import numpy as np

# We will add the vector v to each row of the matrix x,
# storing the result in the matrix y
x = np.array([[1,2,3], [4,5,6], [7,8,9], [10, 11, 12]])
v = np.array([1, 0, 1])
y = x + v  # Add v to each row of x using broadcasting
print y
```
```
[[ 2  2  4]
 [ 5  5  7]
 [ 8  8 10]
 [11 11 13]]
```

The line `y = x + v` works even though x has shape (4, 3) and v has shape (3,) due to broadcasting; this line works as if v actually had shape (4, 3), where each row was a copy of v, and the sum was performed elementwise.

Broadcasting two arrays together follows these rules:

If the arrays do not have the same rank, prepend the shape of the lower rank array with 1s until both shapes have the same length.
The two arrays are said to be compatible in a dimension if they have the same size in the dimension, or if one of the arrays has size 1 in that dimension.
The arrays can be broadcast together if they are compatible in all dimensions.
After broadcasting, each array behaves as if it had shape equal to the elementwise maximum of shapes of the two input arrays.
In any dimension where one array had size 1 and the other array had size greater than 1, the first array behaves as if it were copied along that dimension
If this explanation does not make sense, try reading the explanation from the documentation or this explanation.

Functions that support broadcasting are known as universal functions. You can find the list of all universal functions in the documentation.

Here are some applications of broadcasting:

```
# Compute outer product of vectors
v = np.array([1,2,3])  # v has shape (3,)
w = np.array([4,5])    # w has shape (2,)
# To compute an outer product, we first reshape v to be a column
# vector of shape (3, 1); we can then broadcast it against w to yield
# an output of shape (3, 2), which is the outer product of v and w:

print (np.reshape(v, (3, 1)) * w)
print((np.reshape(v, (3, 1))).shape)
```
```
[[ 4  5]
 [ 8 10]
 [12 15]]
(3, 1)
```
```
# Add a vector to each row of a matrix
x = np.array([[1,2,3], [4,5,6]])
# x has shape (2, 3) and v has shape (3,) so they broadcast to (2, 3),
# giving the following matrix:

print x + v
```
```
[[2 4 6]
 [5 7 9]]
```
```
# Add a vector to each column of a matrix
# x has shape (2, 3) and w has shape (2,).
# If we transpose x then it has shape (3, 2) and can be broadcast
# against w to yield a result of shape (3, 2); transposing this result
# yields the final result of shape (2, 3) which is the matrix x with
# the vector w added to each column. Gives the following matrix:

print (x.T + w).T
```
```
[[ 5  6  7]
 [ 9 10 11]]
```
```
# Another solution is to reshape w to be a row vector of shape (2, 1);
# we can then broadcast it directly against x to produce the same
# output.
print x + np.reshape(w, (2, 1))
```
```
[[ 5  6  7]
 [ 9 10 11]]
```
```
# Multiply a matrix by a constant:
# x has shape (2, 3). Numpy treats scalars as arrays of shape ();
# these can be broadcast together to shape (2, 3), producing the
# following array:
print x * 2
```
```
[[ 2  4  6]
 [ 8 10 12]]
```

Broadcasting typically makes your code more concise and faster, so you should strive to use it where possible.<br/>
This brief overview has touched on many of the important things that you need to know about numpy, but is far from complete. Check out the numpy reference to find out much more about numpy.
## Matplotlib
Matplotlib is a plotting library. In this section give a brief introduction to the matplotlib.pyplot module, which provides a plotting system similar to that of MATLAB.
```
import matplotlib.pyplot as plt
import numpy as np
```
By running this special iPython command, we will be displaying plots inline:
```
%matplotlib inline
```
### Plotting
The most important function in matplotlib is plot, which allows you to plot 2D data. Here is a simple example:

```
# Compute the x and y coordinates for points on a sine curve
x = np.arange(0, 3 * np.pi, 0.1)
y = np.sin(x)

# Plot the points using matplotlib
plt.plot(x, y)
```




 



 
 


 
 





 
 









 

































