# Experiment-2-ECE-2112
### Intended learning outcomes:
1. To identify the codes and functions incorporated in the Numpy library
2. To be able to apply and use the different codes and functions in creating a Python program using a
Numpy library

## Problem 1: Normalization problem:
### Step-by-Step Process:
In beginning the code, the NumPy library must first be imported to be able to access its functionalities, hence the first line of code is:

- import numpy as np

Afterwards, I needed a 5x5 array with random values which leads to as follow:

- X = np.random.random((5,5))

To get the mean and standard deviation, I assigned them to variables a and b respectively and used their corresponding NumPy functions:

- a = np.mean(X)
- b = np.std(X)

For the normalized array of X, the following formula was used and implemented to the code:

- normalized_X = (X-a)/b

Lastly, the output was saved in a .npy format using the function np.save, implemented as:

- np.save('X_normalized', normalized_X)

Just in case the .npy file was loaded in the same program using the code:

- c = np.load('X_normalized.npy)
- c

## Problem 2: Divisible by 3 problem:
### Step-by-Step Process:

In this problem, I needed a 100x100 array that contains the squares of the numbers 1 to 100. 

To achieve this, I first defined an array containing the values from 1 to 100 using the following line of code:

- Y = np.arange(1,101,1)

Next, I resized the array into a 10x10 array using the .resize function, implemented as:

- Y.resize(10,10)

To complete the array, I needed to get the squares of the value so I had a few options. Two that stood out most to me is to use the exponentiation operator ** or multiply it to itself. The code implemented was the latter:

- Y = Y*Y

Now that I have a 10x10 array containing the squares of the numbers 1 to 100, I needed a variable that could hold the number of times the program will encounter a number in the array that is divisible by 3.

Using the following code, I was able to get an array that retains the values that are divisible by 3.

- f = Y[Y%3 == 0]

Finally, I saved the result (f) in a .npy format using the following line of code:

- np.save('div_by_3',f)

And loaded it for extra measure with the code:

- np.load('div_by_3.npy')
