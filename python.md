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

 
 


 
 





 
 









 

































