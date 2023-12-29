# Linear Search and Binary search
## Aim:
To write a program to perform linear search and binary search using python programming.
## Equipment’s required:
1.	Hardware – PCs
2.	Anaconda – Python 3.7 Installation / Moodle-Code Runner
## Algorithm:
## Linear Search:
1.	Start from the leftmost element of array[] and compare k with each element of array[] one by one.
2.	If k matches with an element in array[] , return the index.
3.	If k doesn’t match with any of elements in array[], return -1 or element not found.
## Binary Search:
1.	Set two pointers low and high at the lowest and the highest positions respectively.
2.	Find the middle element mid of the array ie. arr[(low + high)/2]
3.	If x == mid, then return mid.Else, compare the element to be searched with m.
4.	If x > mid, compare x with the middle element of the elements on the right side of mid. This is done by setting low to low = mid + 1.
5.	Else, compare x with the middle element of the elements on the left side of mid. This is done by setting high to high = mid - 1.
6.	Repeat steps 2 to 5 until low meets high
## Program:
(i)Use a linear search method to match the item in a list.
```python
''' 
Program for linear search method to match the item in a list
Developed by: Guumurthy S
RegisterNumber: 23013514
'''
def linearSearch(array,n,k):
    for i in range(n):
        if k==array[i]:
            return i
    return -1
array = eval(input())
array.sort()
print(array)
k = eval(input())
n=len(array)
result= linearSearch(array,n,k)
if result == -1:
    print("Element not found")
else:
    print("Element found at index: ",result)

```
(ii)Find the element in a list using Binary Search(Iterative Method).
```python
''' 
Program to find the element in a list using Binary Search(Iterative Method)..
Developed by: Gurumurthy S
RegisterNumber: 23013514
'''
def binarySearchIter(array, k, low, high):
    while low<=high:
        mid=low+(high-low)//2
        if array[mid]==k:
            return mid
        elif array[mid]<k:
            low=mid+1
        else:
            high=mid-1
   
    return -1
    
    
array = eval(input())
array.sort()
print(array)
k = eval(input())
n=len(array)
t=binarySearchIter(array,k,0,n-1)
if t==-1:
    print("Element not found")
else:
    print("Element found at index: ",t)

```
(iii)Find the element in a list using Binary Search (recursive Method).
```python
''' 
Program to find the element in a list using Binary Search (recursive Method).
Developed by: your name
RegisterNumber: 
'''
def BinarySearch(arr, k, low, high):
    if low<=high:
        mid = low+(high-low)//2
        if arr[mid]==k:
            return mid
        elif arr[mid]<k:
            return BinarySearch(arr,k,mid+1,high)
        else:
            return BinarySearch(arr,k,low,mid-1)
    else:
        return -1
arr = eval(input())
arr.sort()
print(arr)
k = eval(input())
result = BinarySearch(arr,k,0,len(arr)-1)
if result ==-1:
    print("Element not found")
else:
    print("Element found at index: ",result)
    
```
## Sample Input and Output
![index_found](https://github.com/GURUMUR/Search-Algorithm/assets/144895197/0b176d97-ac0f-4938-9824-d4712f88d2ef)
![iteration_method](https://github.com/GURUMUR/Search-Algorithm/assets/144895197/0fb0d5c5-9175-42c1-bde8-7c71f5e6c17f)
![recurive_method](https://github.com/GURUMUR/Search-Algorithm/assets/144895197/0a321796-d119-465c-a5e3-8a59ed5ab778)


## Result
Thus the linear search and binary search algorithm is implemented using python programming.
