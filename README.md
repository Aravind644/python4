# python4
ARRAYS


1.Write a function to add integer values of an array

import array as arr

numbers = arr.array('i', [1, 2, 3])

numbers.append(4)
print(numbers)     # Output: array('i', [1, 2, 3, 4])

# extend() appends iterable to the end of the array
numbers.extend([5, 6, 7])
print(numbers)   


2.Write a function to calculate the average value of an array of integers

# Example to find avearge of list
from numpy import mean
number_list = [45, 34, 10, 36, 12, 6, 80]
avg = mean(number_list)
print("The average is ", round(avg,2))


3.Write a program to find the index of an array element

import numpy as np

# Create a numpy array from a list of numbers
arr = np.array([11, 12, 13, 14, 15, 16, 17, 18, 19, 20, 21])

result = np.where(arr == 19)

print('Tuple of arrays returned : ', result)
print("Elements with value 19 exists at following indices", result[0], sep='\n')


4.Write a function to test if array contains a specific value

import numpy as np
  
# creating a Numpy array
n_array = np.array([[2, 3, 0],
                    [4, 1, 6]])
  
print("Given array:")
print(n_array)
  
# Checking whether specific values
# are present in "n_array" or not
print(2 in n_array)
print(0 in n_array)
print(6 in n_array)
print(50 in n_array)
print(10 in n_array)


5.Write a function to remove a specific element from an array

from array import *

# Declare an array of 8 numbers
num_array = array('i', range(11, 19))

# Printing the array before deletion of elements
print("num_array before deletion: {}".format(num_array))

# Remove 11 from the array
num_array.remove(11)
print("Array.remove() to remove 11: {}".format(num_array))



6.Write a function to copy an array to another array

import numpy as np

arr = np.array([1, 2, 3, 4, 5])
x = arr.copy()
arr[0] = 42

print(arr)
print(x)


7.Write a function to insert an element at a specific position in the array

my_input = [1, 2, 3, 4, 5]

print(f'Current Numbers List {my_input}')

number = int(input("Please enter a number to be added:\n"))

index = int(input(f'Enter the index between 0 and {len(my_input) - 1} to add the given number:\n'))

my_input.insert(index, number)

print(f'Updated List {my_input}')


8.Write a function to find the minimum and maximum value of an array

# import numpy library
import numpy
  
# creating a numpy array of integers
arr = numpy.array([1, 5, 4, 8, 3, 7])
  
# finding the maximum and 
# minimum element in the array
max_element = numpy.max(arr)
min_element = numpy.min(arr)
  
# printing the result
print('maximum element in the array is: ', 
      max_element)
print('minimum element in the array is: ',
      min_element)
      
      

9.Write a function to reverse an array of integer values

mport numpy as np

orgarr = np.array([15, 20, 50, 40, 78, 99, 248])
print("Original Numeric Numpy Array Items = ", orgarr)

revarr = orgarr[::-1]
print("After Reversing Numeric Numpy Array = ", revarr)


10.Write a function to find the duplicate values of an array

def findRepeating(arr, size):
     
    # Hash map to store the
    # frequency of elements
    frequency = {}
     
    # Loop to store the frequency of
    # elements of array
    for i in range (0, size):
        frequency[arr[i]] = \
        frequency.get(arr[i], 0) + 1
    return frequency
     
# Driver Code
if __name__ == "__main__":
    arr = [4, 4, 5, 5, 6]
    arr_size = len(arr)
    frequency = findRepeating(arr, arr_size)
    print("Below is the frequency\
    of repeated elements -")
    for i in frequency:
        if frequency[i] > 1:
            print(i, " --> ", frequency[i])
            
            


11.Write a program to find the common values between two arrays

import numpy as np
  
  
# create 2 arrays
a = np.array([2, 4, 7, 1, 4])
b = np.array([7, 2, 9, 0, 5])
  
# Display the arrays
print("Original arrays", a, ' ', b)
  
# use the np.intersect1d method
c = np.intersect1d(a, b)
  
# Display result
print("Common values", c)


12.Write a method to remove duplicate elements from an array

print("Enter Array Elements:")     #using set()
l=list(map(int,input().split()))
l=set(l)
l=list(l)
for i in range(len(l)):
    print(l[i],end=" ")
    
    
13.Write a method to find the second largest number in an array

import array
arr = []
n = int(input("enter size of array : "))
for x in range(n):
    x=int(input("enter element of array : "))
    arr.append(x)
 
sorted_array = sorted(array.array('i', arr))
for i in range(len(arr)-1, 0, -1):
    if sorted_array[i]!=sorted_array[i-1]:
        print(f"second largest element is {sorted_array[i-1]}")
        break 
        
        
        
14.14. Write a method to find the second largest number in an array


import array
arr = []
n = int(input("enter size of array : "))
for x in range(n):
    x=int(input("enter element of array : "))
    arr.append(x)
 
sorted_array = sorted(array.array('i', arr))
for i in range(len(arr)-1, 0, -1):
    if sorted_array[i]!=sorted_array[i-1]:
        print(f"second largest element is {sorted_array[i-1]}")
        break 
        
        
        
        
15.Write a method to find number of even number and odd numbers in an array

import numpy as np

evenOddArr = np.array([10, 99, 22, 50, 77, 22, 112, 19])
print("The List of Numbers in evenOddArr Array = ", evenOddArr)

evenArrCount = 0
oddArrCount = 0

for i in range(len(evenOddArr)):
    if (evenOddArr[i] % 2 == 0):
        evenArrCount = evenArrCount + 1
    else:
        oddArrCount = oddArrCount + 1

print("The Count of Even Numbers in evenOddArr Array = ", evenArrCount)
print("The Count of Odd Numbers in evenOddArr Array  = ", oddArrCount)



16.Write a function to get the difference of largest and smallest value

print("Input an integer created by 8 numbers from 0 to 9.:")
num = list(input())
print("Difference between the largest and the smallest integer from the given integer:")
print(int("".join(sorted(num,reverse=True))) - int("".join(sorted(num))))


17.Write a method to verify if the array contains two specified elements(12,23)


product_id = [12,23]
products = np.array([[1,23],
                [12, 20]])
if product_id in products:
    print(True)
else:
    print(False)
    
    
18. Write a program to remove the duplicate elements and return the new array

 
 import array as arr
def test(nums):
    return sorted(set(nums),key=nums.index)

array_num = arr.array('i', [1, 3, 5, 1, 3, 7, 9])
print("Original array:")
for i in range(len(array_num)):    
    print(array_num[i], end=' ')
print("\nAfter removing duplicate elements from the said array:")
result = arr.array('i', test(array_num))
for i in range(len(result)):    
    print(result[i], end=' ')
    
    
