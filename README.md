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
    if high>=low:
        mid=low+(high-low)//2
        if arr[mid]==k:
            return mid
        elif arr[mid]>k:
            return BinarySearch(arr,k,low,mid-1)
        else:
            return BinarySearch (arr,k,mid+1,high)
    else:
        return -1
        
arr=eval(input())
arr.sort()
k=eval(input())

result=BinarySearch(arr,k,0,len(arr)-1)
if (result==-1):
    print(arr)
    print("Element not found")
else:
    print(arr)
    print("Element found at index: ",result)



```
ii)	# Find the element in a list using Binary Search(Iterative Method).
```
def binarySearchIter(array, k, low, high):
    while(low<=high):
        mid=low+(high-low)//2
        if array[mid]==k:
            return mid
        elif array[mid]<k:
            low=mid+1
        else:
            high=mid+1
    return -1
array=eval(input())
#sort the array
array.sort()
print(array)
#k-item to be searched
k=eval(input()) 
low=0
high= len(array)-1
# use the binary search function to find the item in the list
result=binarySearchIter(array, k, low, high)
# use if-else to print sorted array and "Element not found" if the item is not present in the list otherwise print sorted array and "Element found at index: ", result
if result>=0:
    print("Element found at index: ",result)
else:
    print("Element not found")




```
iii)	# Find the element in a list using Binary Search (recursive Method).
```
def BinarySearch(arr, k, low, high):
    if high>=low:
        mid=low+(high-low)//2
        if arr[mid]==k:
            return mid
        elif arr[mid]>k:
            return BinarySearch(arr,k,low,mid-1)
        else:
            return BinarySearch (arr,k,mid+1,high)
    else:
        return -1
        
arr=eval(input())
arr.sort()
k=eval(input())

result=BinarySearch(arr,k,0,len(arr)-1)
if (result==-1):
    print(arr)
    print("Element not found")
else:
    print(arr)
    print("Element found at index: ",result)




```
## Sample Input and Output
![Screenshot (36)](https://user-images.githubusercontent.com/94828604/154986038-0af94018-1073-49a4-a1e2-6fc72e8c39a9.png)
![Screenshot (38)](https://user-images.githubusercontent.com/94828604/154986248-2b30f680-2840-478c-afda-f30890af8734.png)
![Screenshot (40)](https://user-images.githubusercontent.com/94828604/154986505-d74048f5-7e49-46cd-9625-5f5dbf4dc368.png)






## Result
Thus the linear search and binary search algorithm is implemented using python programming.
