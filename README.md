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
def BinarySearch(arr, k, low, high):
    # Write your code here for binary search using recursive method
    if high >= low:
        mid = low + (high - low)//2
        if arr[mid] == k:
            return mid
        elif arr[mid] > k:
            return BinarySearch(arr, k, low, mid-1)
        else:
            return BinarySearch(arr, k, mid + 1, high)
    else:
        return -1
arr = eval(input())
#sort the array
arr.sort()
k = eval(input()) # k is the element to be searched for

result = BinarySearch(arr, k, 0, len(arr)-1)# use the binary search function to find the result
# use if-else to print sorted array and "Element not found" if the item is not present in the list otherwise print sorted array and "Element found at index: ", result
if(result == -1):
    print(arr)
    print("Element not found")
else:
    print(arr)
    print("Element found at index: ", result)
    
```
ii)	# Find the element in a list using Binary Search(Iterative Method).
```
def binarySearchIter(array, k, low, high):
    # Write your code here to find the middle value and check if the desired item is above or below the middle value
    while low <= high:
        mid = low + (high - low)//2
        if array[mid] == k:
            return mid
        elif array[mid] < k:
            low = mid + 1
        else:
            high = mid - 1
    return -1
array = eval(input())
array.sort()
# sort the array
k = eval(input()) #k-item to be searched
result = binarySearchIter(array,k, 0, len(array)-1)
if (result == -1):
    print(array)
    print("Element not found")
else:
    print(array)
    print("Element found at index: ", result)

# use the binary search function to find the item in the list

# use if-else to print sorted array and "Element not found" if the item is not present in the list otherwise print sorted array and "Element found at index: ", result

```
iii)	# Find the element in a list using Binary Search (recursive Method).
```
def BinarySearch(arr, k, low, high):
    # Write your code here for binary search using recursive method
    if high >= low:
        mid = low + (high - low)//2
        if arr[mid] == k:
            return mid
        elif arr[mid] > k:
            return BinarySearch(arr, k, low, mid-1)
        else:
            return BinarySearch(arr, k, mid + 1, high)
    else:
        return -1
arr = eval(input())
#sort the array
arr.sort()
k = eval(input()) # k is the element to be searched for

result = BinarySearch(arr, k, 0, len(arr)-1)# use the binary search function to find the result
# use if-else to print sorted array and "Element not found" if the item is not present in the list otherwise print sorted array and "Element found at index: ", result
if(result == -1):
    print(arr)
    print("Element not found")
else:
    print(arr)
    print("Element found at index: ", result)
    
```
## Sample Input and Output
1.
![Screenshot_8-12-2024_20237_lms2 ai saveetha in](https://github.com/user-attachments/assets/b4140570-b850-40c3-a89f-4e0081300863)


2.
![image](https://github.com/user-attachments/assets/06415273-d191-4142-8b82-33be8b57ecab)


3.
![Screenshot_8-12-2024_202414_lms2 ai saveetha in](https://github.com/user-attachments/assets/47d1f0dd-c883-49b6-b074-9af76e4b6a3b)





## Result
Thus the linear search and binary search algorithm is implemented using python programming.
