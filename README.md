Merge 2 sorted arrays
In this article we will see a python program to Merge 2 sorted arrays. We will given two array namely array1 and array2 of length n1 and n2. Without using any extra list or set or container, we need to merge both the array in such a way that after sorting no element is more then once in the list. And the initial n1 elements of this array after merging is required to be stored in array1 and rest in array2.

merge two sorted array without using extra space in python

Algorithm
Step 1: Create array1 and assign values
Step 2: Create array2 and assign values
Step 3: Call the function find
Algorithm for function find
Step 1 : Append the element of array2 in array1.
Step 2: Sort array1. Now array 1 have all the elements that we have got after merging both array.
Step 3: Add n2 elements in array2 from last.
Step 4: Let array1 have initial n1 elements
Step 5: Print both the array.
merge two sorted array without using extra space using python
Python Code
Run
# Merge 2 sorted arrays without using Extra space.

def find(array1, array2, n1, n2):
    # append array2 to array1
    for i in array2:
        array1.append(i)
    array1 = list(set(sorted(array1)))

    array2 = array1[len(array1) - n2:]
    array1 = array1[:len(array1) - n2]

    print("After")
    print("Array1: ", array1, "\nArray2: ", array2)


array1 = [1, 2, 3, 5, 8, 9, 10, 13, 15, 20]
array2 = [2, 3, 8, 13]

print("Before: ")
print("Array1: ", array1)
print("Array2: ", array2)

find(array1, array2, len(array1), len(array2))
Output
Before: 
Array1: [1, 2, 3, 5, 8, 9, 10, 13, 15, 20]
Array2: [2, 3, 8, 13]
After
Array1: [1, 2, 3, 5, 8, 9] 
Array2: [10, 13, 15, 20]
