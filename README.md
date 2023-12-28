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
i)	#Use a linear search method to match the item in a list.
```
''' 
Program for linear search method to match the item in a list
Developed by:MOHAMED SULTHAN A
RegisterNumber: 23004839
'''
def linearSearch(array,n,k):
    for i in range (n):
        if array[i]==k:
            return i
    return -1
array = eval(input())
array.sort()
k = eval(input())
n=len(array)
print(array)
result = linearSearch(array,n,k)
if result==-1:
    print("Element not found")
else:
     print("Element found at index: ",result)
```



```
ii)	# Find the element in a list using Binary Search(Iterative Method).
```
''' 
Program to find the element in a list using Binary Search(Iterative Method)..
Developed by:MOHAMED SULTHAN A
RegisterNumber: 23004839
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
k = eval(input())
print(array)
result=binarySearchIter(array,k,0,len(array)-1)
if result==-1:
    print("Element not found")
else:
    print("Element found at index: ",result)
```





```
iii)	# Find the element in a list using Binary Search (recursive Method).
```
''' 
Program to find the element in a list using Binary Search (recursive Method).
Developed by: your name MOHAMED SULTHAN A
RegisterNumber: 23004839
'''
def BinarySearch(arr,low, high,x):
    if high>=low:
        mid=(high+low)//2
        if arr[mid]==x:
            return mid
        elif arr [mid]>x:
            return BinarySearch(arr,low,mid-1,x)
        else:
            return BinarySearch(arr,mid+1,high,x)
    else:
        return -1
    
arr = eval(input())
arr=sorted(arr)
x=eval(input())
result=BinarySearch(arr,0,len(arr)-1,x)
if result!=-1:
    print(arr)
    print("Element found at index: ",str(result))
else:
    print(arr)
    print("Element not found")
```





```
## Output:
![Screenshot 2023-12-28 172908](https://github.com/Sulthan06042007/Search-Algorithm/assets/144980103/ac0354e1-6c72-4996-bca0-5b2c4946733f)
![Screenshot 2023-12-28 172950](https://github.com/Sulthan06042007/Search-Algorithm/assets/144980103/e339f4f3-aa7a-4873-aed7-0a202596d1f3)
![Screenshot 2023-12-28 173020](https://github.com/Sulthan06042007/Search-Algorithm/assets/144980103/6e72b569-bc22-4046-8dd1-84b3e5adb0bd)











## Result
Thus the linear search and binary search algorithm is implemented using python programming.
