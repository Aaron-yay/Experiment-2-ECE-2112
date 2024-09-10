## Experiment-2-ECE-2112
# Intended learning outcomes:
1. To identify the codes and functions incorporated in the Numpy library
2. To be able to apply and use the different codes and functions in creating a Python program using a
Numpy library

# Problem 1: Normalization problem:
for this problem, I used the np.random.random function to automatically generate an array without having to manually input its values and dimensions allowing me to follow with the instruction of generating a random array, hence the code:
X = np.random.random((5,5))

next, I used the mean and standard deviation functions in np to quickly and conveniently get 2 values that will take forever to get if manually solved for, which leads to the appearance of both: a = np.mean(X), b = np.std(X)

finally, I divided the variable a to variable b to obtain the normalized value of the array and stored it in the variable named normalized_X

to store the value of normalized_X, I used the np.save function to save the array, whose format is np.save('name_of_npy_file',name_of_variable).
for double-checking, I used the np.load function to make sure that the value is actually saved

p.s. maiiba ung value ng normalized x pag nirun ulet ung code sa array soo ayun lng hehe

# Problem 2: Divisible by 3 problem:
for this problem I first had to initialize an array that contained the elements from 1 to 100.
I achieved this by using the np.arange (single r) function and inputting the 1st and last element, along with the interval or increment:

np.arange(1, 101, 1)

the next step was to turn it into a 10x10 array so I used the resize function which produced the output of a desirable 10x10 array:

np.resize(10,10)

next, I needed to get the square of all the elements of the array, so I just multiplied it to itself to make sure the operation is as simple as possible:

Y = Y*Y

before starting the code, I printed out the entire array again to make sure its still in the square form of the numbers from 1 to 100:

Y

finally, I declared a new variable, f, to act as my counter for finding the number of numbers divisible by 3:

f = 0

with a bit of googling, experimenting, and note-referencing, I was able to make a nested for loop that will iterate over the entire array and increase the value of the variable f by 1 whenever it encounters a number divisible by 3.

for y in Y:
    for x in y:
        if x % 3 == 0:
            f = f+1
        else:
            pass      

to top it all off, I saved the result acquired (which is 33) and saved it as div_by_3.npy using the same function np.save
np.save('div_by_3',f)
