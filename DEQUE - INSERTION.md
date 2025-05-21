Exp.No:39  
DEQUE - INSERTION

AIM  
To write a Python program to insert elements at REAR END of deque using a collection built-in function.

ALGORITHM  
1.Start.
2.Import deque class from the collections module.
3.Initialize an empty deque or a deque with some initial elements.
4.Define a list or take input elements that need to be inserted at the rear end.
5.For each element in the input list:
6.Use the append() method of deque to insert the element at the rear (right end).
7.After all insertions, print or display the updated deque.
8.End.

PROGRAM 
import collections
  
n1=input()
n2=input()
n3=input()
# initializing deque
de = collections.deque([n1,n2,n3])

# inserts 14,15 at the end of deque


de.append('h')
de.append('o')
de.append('n')
# printing modified deque
print ("The deque after appending at right is : ")
print (de)


### OUTPUT
![image](https://github.com/user-attachments/assets/f6bffd42-edc9-4ddd-839c-87423babb9b6)

### RESULT
Thus, the Python program to insert elements at REAR END of deque using a collection built-in function was successfully implemented and verified.
