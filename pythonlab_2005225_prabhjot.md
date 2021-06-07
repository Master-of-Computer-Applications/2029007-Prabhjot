******Python program to print the elements of an array ******

Initialize array  
arr = [0,1, 2, 3, 4, 5]; 
print("Elements of given array: "); 
print("Access all items individually");
print"1st element:",arr[0];
print"2nd element:",arr[1];
print"3rd element:",arr[2];
print"4th element:",arr[3];
print"5th element:",arr[4];
print"6th element:",arr[5];
output:- ![Screenshot from 2021-06-07 18-57-23](https://user-images.githubusercontent.com/82701181/121027582-b63e8480-c7c4-11eb-9d3c-a116488a839d.png)

******
********Write a python program to reverse the order of the items in the array.******

#The original array
arr = [11, 22, 33, 44, 55]
print("Before reversal Array is :",arr)

arr.reverse() #reversing using reverse()
print("After reversing Array:",arr)
output:- ![Screenshot from 2021-06-07 19-14-02](https://user-images.githubusercontent.com/82701181/121027946-fe5da700-c7c4-11eb-9e31-21bad631be94.png)

********

********Write a Python program to append a new item to the end of the array.******

my_input = ['Engineering', 'Medical'] 
my_input.append('Science') 
print(my_input)
output:-![Screenshot from 2021-06-07 19-22-21](https://user-images.githubusercontent.com/82701181/121028793-bab76d00-c7c5-11eb-9863-b6f1ca39f3c1.png)

********
********write a python program to remove a specified item using the index from an array.********

#original array
arr= [1,2,3,4,5,6]
#Remove element with index= 1
arr.remove(1)
#Printing the array
print(arr)
#Remove element with index = 4
arr.remove(4)
#Printing the array
print(arr)
Output:- ![Screenshot from 2021-06-07 19-30-19](https://user-images.githubusercontent.com/82701181/121030331-00c10080-c7c7-11eb-8e2c-d50ccb0af4eb.png)

********
********Write a Python program to get the length of an array.********

import array 
arr = [1,2,3,4,'PYTHON']
print("Array elements: ",arr)
print("Length of array:",len(arr))
Output:- ![Screenshot from 2021-06-07 19-43-56](https://user-images.githubusercontent.com/82701181/121032260-be98be80-c7c8-11eb-8e5e-9e607b37d973.png)

********
********Write a program for binary search.**********

def binary_search(arr, low, high, x):
 
    # Check base case
    if high >= low:
 
        mid = (high + low) // 2
 
        # If element is present at the middle itself
        if arr[mid] == x:
            return mid
 
        # If element is smaller than mid, then it can only
        # be present in left subarray
        elif arr[mid] > x:
            return binary_search(arr, low, mid - 1, x)
 
        # Else the element can only be present in right subarray
        else:
            return binary_search(arr, mid + 1, high, x)
 
    else:
        # Element is not present in the array
        return -1
 
# Test array
arr = [ 2, 3, 4, 10, 40 ]
x = 10
 
# Function call
result = binary_search(arr, 0, len(arr)-1, x)
 
if result != -1:
    print("Element is present at index", str(result))
else:
    print("Element is not present in array")
    output:- ![Screenshot from 2021-06-07 19-52-12](https://user-images.githubusercontent.com/82701181/121033521-e6d4ed00-c7c9-11eb-8f00-fb820fc84404.png)
    ********
    ********Write a program for sequential or linear search.********
    
    def linearsearch(arr, x):
   for i in range(len(arr)):
      if arr[i] == x:
         return i
   return -1
arr = ['t','u','t','o','r','i','a','l']
x = 'a'
print("element found at index "+str(linearsearch(arr,x)))
output:-![Screenshot from 2021-06-07 19-57-42](https://user-images.githubusercontent.com/82701181/121034651-ca858000-c7ca-11eb-9852-9be695b31beb.png)
************

********Write a program to sort a list of elements using the bubble sort algorithm.********

def bubbleSort(nlist):
    for passnum in range(len(nlist)-1,0,-1):
        for i in range(passnum):
            if nlist[i]>nlist[i+1]:
                temp = nlist[i]
                nlist[i] = nlist[i+1]
                nlist[i+1] = temp

nlist = [14,46,43,27,57,41,45,21,70]
bubbleSort(nlist)
print(nlist)
output:- ![Screenshot from 2021-06-07 19-46-47](https://user-images.githubusercontent.com/82701181/121032678-20592880-c7c9-11eb-86c0-79aed01376dc.png)
**********
*********Write a program to sort a list of elements using the selection sort.**********

def selectionSort( itemsList ):
    n = len( itemsList )
    for i in range( n - 1 ):
        minValueIndex = i

        for j in range( i + 1, n ):
            if itemsList[j] < itemsList[minValueIndex] :
                minValueIndex = j

        if minValueIndex != i :
            temp = itemsList[i]
            itemsList[i] = itemsList[minValueIndex]
            itemsList[minValueIndex] = temp

    return itemsList


el = [21,6,9,33,3]

print(selectionSort(el))
output:- ![Screenshot from 2021-05-27 16-55-03](https://user-images.githubusercontent.com/82701181/120997252-ab73f780-c7a4-11eb-9d7f-25b64b2b878b.png)
*********
***********Write a program to sort a list of elements using insertion sort.*************

arr = [12, 11, 13, 5, 6]
insertionSort(arr)
print ("Sorted array is:")
for i in range(len(arr)):
    print ("%d" %arr[i])
output:- !![Screenshot from 2021-05-27 17-02-17](https://user-images.githubusercontent.com/82701181/120998030-51276680-c7a5-11eb-9f25-16b9cb3236d0.png)
**********
************Write a program to sort a list of elements using the quick sort.************

def quicksort(x):
    if len(x) == 1 or len(x) == 0:
        return x
    else:
        pivot = x[0]
        i = 0
        for j in range(len(x)-1):
            if x[j+1] < pivot:
                x[j+1],x[i+1] = x[i+1], x[j+1]
                i += 1
        x[0],x[i] = x[i],x[0]
        first_part = quicksort(x[:i])
        second_part = quicksort(x[i+1:])
        first_part.append(x[i])
        return first_part + second_part

alist = [54,26,93,17,77,31,44,55,20]
quicksort(alist)
print(alist)
output:- ![Screenshot from 2021-05-27 17-12-33](https://user-images.githubusercontent.com/82701181/120999057-50db9b00-c7a6-11eb-9e50-6e430d706b15.png)
**********
********Write a program to create a singly linked list, append some items & iterate through the list.***********
class Node:
    def _init_(self, data=None):
        self.data = data
        self.next = None
class singly_linked_list:
    def _init_(self):
        self.tail = None
        self.head = None
        self.count = 0

    def iterate_item(self):
        current_item = self.tail
        while current_item:
            val = current_item.data
            current_item = current_item.next
            yield val

    def append_item(self, data):
        node = Node(data)
        if self.head:
            self.head.next = node
            self.head = node
        else:
            self.tail = node
            self.head = node
        self.count += 1

items = singly_linked_list()
items.append_item('PHP')
items.append_item('Python')
items.append_item('C#')
items.append_item('C++')
items.append_item('Java')

for val in items.iterate_item():
    print(val)
output:- ![Exp12](https://user-images.githubusercontent.com/82701181/120999947-51286600-c7a7-11eb-8d27-39d630b6e7c7.png)
********Write a program to find the size of a singly linked list.***********

class Node:
    # Singly linked node
    def __init__(self, data=None):
        self.data = data
        self.next = None
class singly_linked_list:
    def __init__(self):
        # Createe an empty list
        self.tail = None
        self.head = None
        self.count = 0
	
    def append_item(self, data):
        #Append items on the list
        node = Node(data)
        if self.head:
            self.head.next = node
            self.head = node
        else:
            self.tail = node
            self.head = node
        self.count += 1
    
    def iterate_item(self):
        # Iterate the list.
        current_item = self.tail
        while current_item:
            val = current_item.data
            current_item = current_item.next
            yield val

items = singly_linked_list()
items.append_item('PHP')
items.append_item('Python')
items.append_item('C#')
items.append_item('C++')
items.append_item('Java')

print("Original list:")
for val in items.iterate_item():
    print(val)

print("\nSize of the list:",items.count)
output:- ![Exp13](https://user-images.githubusercontent.com/82701181/121001490-f98afa00-c7a8-11eb-9cfa-e2d8dcd3c683.png)
**********
**********Write a program to search a specific item in a singly list and return true if the item is found otherwise return false.***********

class Node:
    # Singly linked node
    def __init__(self, data=None):
        self.data = data
        self.next = None
class singly_linked_list:
    def __init__(self):
        # Createe an empty list
        self.tail = None
        self.head = None
        self.count = 0

    def append_item(self, data):
        #Append items on the list
        node = Node(data)
        if self.head:
            self.head.next = node
            self.head = node
        else:
            self.tail = node
            self.head = node
        self.count += 1

    def iterate_item(self):
        # Iterate the list.
        current_item = self.tail
        while current_item:
            val = current_item.data
            current_item = current_item.next
            yield val

    def search_item(self, val):
         # Search the list
         for node in self.iterate_item():
             if val == node:
                 return True
         return False

items = singly_linked_list()
items.append_item('PHP')
items.append_item('Python')
items.append_item('C#')
items.append_item('C++')
items.append_item('Java')

if items.search_item('SQL'):
    print("True")
else:
    print("False")

if items.search_item('C++'):
    print("True")
else:
    print("False")
output:- ![Exp14](https://user-images.githubusercontent.com/82701181/121002118-a1082c80-c7a9-11eb-93d7-183558dfb1cf.png)
**********
***********Write a program to delete the first item from a singly linked list.************
class Node:
    # Singly linked node
    def __init__(self, data=None):
        self.data = data
        self.next = None
class singly_linked_list:
    def __init__(self):
        # Createe an empty list
        self.tail = None
        self.head = None
        self.count = 0

    def append_item(self, data):
        #Append items on the list
        node = Node(data)
        if self.head:
            self.head.next = node
            self.head = node
        else:
            self.tail = node
            self.head = node
        self.count += 1

    def delete_item(self, data):
        # Delete an item from the list
        current = self.tail
        prev = self.tail
        while current:
            if current.data == data:
                if current == self.tail:
                    self.tail = current.next
                else:
                    prev.next = current.next
                self.count -= 1
                return
            prev = current
            current = current.next
    def iterate_item(self):
        # Iterate the list.
        current_item = self.tail
        while current_item:
            val = current_item.data
            current_item = current_item.next
            yield val

items = singly_linked_list()
items.append_item('PHP')
items.append_item('Python')
items.append_item('C#')
items.append_item('C++')
items.append_item('Java')

print("Original list:")
for val in items.iterate_item():
    print(val)

print("\nAfter removing the first item from the list:")
items.delete_item('PHP')
for val in items.iterate_item():
    print(val)
 output:-![Exp15](https://user-images.githubusercontent.com/82701181/121002569-1d9b0b00-c7aa-11eb-9c2e-9c4d96734de1.png)
 ***********
************Write a program to create circular single linked lists.************
class Node:
     
    # Constructor to create  a new node
    def _init_(self, data):
        self.data = data
        self.next = None
 
class CircularLinkedList:
     
    # Constructor to create a empty circular linked list
    def _init_(self):
        self.head = None
 
    # Function to insert a node at the beginning of a
    # circular linked list
    def push(self, data):
        ptr1 = Node(data)
        temp = self.head
         
        ptr1.next = self.head
 
        # If linked list is not None then set the next of
        # last node
        if self.head is not None:
            while(temp.next != self.head):
                temp = temp.next
            temp.next = ptr1
 
        else:
            ptr1.next = ptr1 # For the first node
 
        self.head = ptr1
 
    # Function to print nodes in a given circular linked list
    def printList(self):
        temp = self.head
        if self.head is not None:
            while(True):
                print "%d" %(temp.data),
                temp = temp.next
                if (temp == self.head):
                    break
 
 
# Driver program to test above function
 
# Initialize list as empty
cllist = CircularLinkedList()
 
# Created linked list will be 11->2->56->12
cllist.push(12)
cllist.push(56)
cllist.push(2)
cllist.push(11)
 
print "Contents of circular Linked List"
cllist.printList()
output:-![WhatsApp Image 2021-06-07 at 19 33 06](https://user-images.githubusercontent.com/82701181/121037121-d4a87e00-c7cc-11eb-8ae2-17814de4c6da.jpeg)
************
********Write a program to implement stack and its operation using list.***********
stack = []
 
# append() function to push
# element in the stack
stack.append('a')
stack.append('b')
stack.append('c')
 
print('Initial stack')
print(stack)
 
# pop() fucntion to pop
# element from stack in
# LIFO order
print('\nElements poped from stack:')
print(stack.pop())
print(stack.pop())
print(stack.pop())
 
print('\nStack after elements are poped:')
print(stack)
output:-![Screenshot from 2021-06-07 20-23-21](https://user-images.githubusercontent.com/82701181/121038877-40d7b180-c7ce-11eb-8a52-3f2a7d332de4.png)
***************
*********Write program to implement queue and its operations using list.************

 Initializing a queue
queue = []

#Adding elements to the queue
queue.append('a')
queue.append('b')
queue.append('c')

print("Initial queue")
print(queue)

#Removing elements from the queue
print("\nElements dequeued from queue")
print(queue.pop(0))
print(queue.pop(0))
print(queue.pop(0))

print("\nQueue after removing elements")
print(queue)
#Uncommenting print(queue.pop(0))
#will raise and IndexError
#as the queue is now empty
output:- ![Expe18](https://user-images.githubusercontent.com/82701181/121039449-b6dc1880-c7ce-11eb-824b-3d9692481d5d.png)
************
********Write program to create a BST using an array elements where elements are sorted in ascending order.********

class TreeNode(object):
    def _init_(self, x):
        self.val = x
        self.left = None
        self.right = None

def sorted_array_to_bst(nums):
    
    if not nums:
        return None
    mid_val = len(nums)//2
    node = TreeNode(nums[mid_val])
    node.left = sorted_array_to_bst(nums[:mid_val])
    node.right = sorted_array_to_bst(nums[mid_val+1:])
    return node

def preOrder(node): 
    if not node: 
        return      
    print(node.val)
    preOrder(node.left) 
    preOrder(node.right)   
    
result = sorted_array_to_bst([1, 2, 3, 4, 5, 6, 7])
preOrder(result)
output:-![WhatsApp Image 2021-06-07 at 19 52 20](https://user-images.githubusercontent.com/82701181/121040583-a37d7d00-c7cf-11eb-9c37-95b6c3e9f528.jpeg)
************
********Write a Program to find the kth smallest element in a given array.********

class TreeNode(object):
    def _init_(self, x):
        self.val = x
        self.left = None
        self.right = None

def sorted_array_to_bst(nums):
    
    if not nums:
        return None
    mid_val = len(nums)//2
    node = TreeNode(nums[mid_val])
    node.left = sorted_array_to_bst(nums[:mid_val])
    node.right = sorted_array_to_bst(nums[mid_val+1:])
    return node

def preOrder(node): 
    if not node: 
        return      
    print(node.val)
    preOrder(node.left) 
    preOrder(node.right)   
    
result = sorted_array_to_bst([1, 2, 3, 4, 5, 6, 7])
preOrder(result)
output:-![WhatsApp Image 2021-06-07 at 19 57 50](https://user-images.githubusercontent.com/82701181/121041217-2e5e7780-c7d0-11eb-89f6-f0075dc0c8a2.jpeg)








