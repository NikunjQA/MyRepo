# MyRepo
Vectors using Numpy
What is Numpy?
             NumPy is the fundamental package for scientific computing in Python. It is a Python library that provides a multidimensional array object, various derived objects (such as masked arrays and matrices), and an assortment of routines for fast operations on arrays, including mathematical, logical, shape manipulation, sorting, selecting, I/O, discrete Fourier transforms, basic linear algebra, basic statistical operations, random simulation and much more.

There are several important differences between NumPy arrays and the standard Python sequences(lists):

-  NumPy arrays have a fixed size at creation, unlike Python lists (which can grow dynamically). Changing the size of an ndarray will create a new array and delete the original.
-   The elements in a NumPy array are all required to be of the same data type, and thus will be the same size in memory. The exception: one can have arrays of (Python, including NumPy) objects, thereby allowing for arrays of different sized elements.
-   NumPy arrays facilitate advanced mathematical and other types of operations on large numbers of data. Typically, such operations are executed more efficiently and with less code than is possible using Python’s built-in sequences.
-   A growing plethora of scientific and mathematical Python-based packages are using NumPy arrays; though these typically support Python-sequence input, they convert such input to NumPy arrays prior to processing, and they often output NumPy arrays. 


# Lets Import Numpy
import numpy as np

# TASK: Define Numpy arrays with names: n1, n2
# Reference: https://numpy.org/doc/stable/user/quickstart.html#array-creation
# Your Code:

n1 = np.array([1, 2, 3, 4, 5])
n2 = np.array([6, 7, 8, 9, 10])

print(n1)
print(n2)

[1 2 3 4 5]
[ 6  7  8  9 10]

# TASK: Redefine n1 as a vector/array with the values 22,33,44 and order of the vector as 1x3
# Your Code:

n1 = np.array([22,33,44])

print(n1)

[22 33 44]


Addition:

# Adding numpy vectors is as simple as performing regular addition in Python.

# TASK: Add vector [2, 2, 2] with n1 from earlier
# Your Code:

n2 = np.array([2,2,2])
result = n1+n2
print(result)


# Expected output: [24, 35, 46]
[24 35 46]


Subtraction

#Subtracting numpy vectors is also as simple as performing regular subtraction in Python

# TASK: Subtract vector [2, 3, 4] with n1 from earlier

# Your Code:

n2 = np.array([2,3,4])
result = n1-n2
print(result)


# Expected output: [20, 30, 40]
[20 30 40]

#Scalar Multiplication/ Element-wise multiplication

This is also very easy to perform. Regular Python is enough or numpy also comes with functions to perform the same

https://numpy.org/doc/stable/reference/generated/numpy.multiply.html#numpy-multiply

# TASK: Multiply n1 with 25

# Your Code:
result=n1*25
print(result)

# Expected output: [550,  825, 1100]
[ 550  825 1100]

# TASK: perform element-wise multiplication of n1 and [11, 12, 13]. Use numpy's multiply function

# Your Code:
result = np.multiply(n1, [11, 12, 13])

print(result)

# Expected output: [242, 396, 572]
[242 396 572]

Vector Multiplication
Vector multiplication, or also called dot product of vectors/matrices. Numpy has functions to perform the same

https://numpy.org/doc/stable/reference/generated/numpy.dot.html#numpy-dot https://numpy.org/doc/stable/reference/generated/numpy.reshape.html#numpy-reshape

note: numpy functions also carry additional features for certain scenarios of inputs. The reference mentions all of them, we will be looking only at our required case here.

# TASK: perform vector multiplication of n1 (use numpy reshape:- set order as 3 x 1) and a vector of only 3's, and of order/dimension 1 x 4

# Your Code:
n1 = n1.reshape(3, 1)
n2 = np.array([[3, 3, 3, 3]])

result = np.matmul(n1, n2)

print(result)

# Expected Output:
# [[ 66,  66,  66,  66],
#  [ 99,  99,  99,  99],
#  [132, 132, 132, 132]]
[[ 66  66  66  66]
 [ 99  99  99  99]
 [132 132 132 132]]
	
# TASK: perform vector multiplication of n1 and transpose of n1. Use numpy techniques for transpose

# Your Code:

n1 = np.array([22, 33, 44])

result = np.matmul(n1, n1.T)

print(result)


# Expected output: 3059 - It is incorrect 
3509  - Correct output


# TASK: Initialize a vector (v1) with prime numbers 1 to 23, with order 3x3. Initialize a vector (v2) as inverse of v1.
# Perform vector multiplication of both and get identityu matrix. Use numpy rounding methods if needed
# https://numpy.org/doc/stable/reference/generated/numpy.linalg.inv.html#numpy-linalg-inv
# https://numpy.org/doc/stable/reference/generated/numpy.round.html#numpy-round

# Your Code:

import numpy as np
v1 = np.array([[2, 3, 5],
    [7, 11, 13],
    [17, 19, 23]
])

v2 = np.linalg.inv(v1)
result = np.matmul(v1, v2)

# Round the result
result = np.round(result)

print(result)

# Expected output (with or without signs both is ok):
# [[ 1., -0.,  0.],
#  [ 0.,  1.,  0.],
#  [-0., -0.,  1.]]
[[ 1.  0. -0.]
 [ 0.  1.  0.]
 [ 0.  0.  1.]]

Go Through Documentation
https://numpy.org/doc/stable/user/quickstart.html#the-basics

# TASK: Study and perform 3 different universal functions on v1
v1 = np.array([
    [2, 3, 5],
    [7, 11, 13],
    [17, 19, 23]
])

# 1. Square root
print(np.sqrt(v1))

# 2. Square of each element
print(np.square(v1))

# 3. Exponential (e^x)
print(np.exp(v1))

[[1.41421356  1.73205081  2.23606798]
 [2.64575131  3.31662479  3.60555128]
 [4.12310563  4.35889894 4.79583152]]

[[  4   9  25]
 [ 49 121 169]
 [289 361 529]]

[[7.38905610e+00 2.00855369e+01 1.48413159e+02]
 [1.09663316e+03 5.98741417e+04 4.42413392e+05]
 [2.41549528e+07 1.78482301e+08 9.74480345e+09]]




