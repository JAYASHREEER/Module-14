Exp No: 36  
Circular Queue 

AIM  
To write a Python program with a function to insert string values into a Circular Queue.

ALGORITHM
Start.
Initialize a circular queue of fixed size (say max_size).
Initialize two pointers:
front = -1
rear = -1
Define a function enqueue(value) to insert a string into the circular queue.

In the enqueue function:
Check if the queue is full:
If (rear + 1) % max_size == front then the queue is full.
Print "Queue is full, cannot insert."
Return from the function.

If the queue is empty (i.e., front == -1):
Set front = 0.

Increment rear using circular increment:
rear = (rear + 1) % max_size.
Insert the given value at queue[rear].
End function.

In the main program, call the enqueue function with string inputs as required.
End.

PROGRAM
```

# Queue simply works in FIFO
class Queue:
    def __init__(self, size):
        self.items = [0] * size
        self.max_size = size
        self.head, self.tail, self.size = 0, 0, 0

    def enqueue(self, item):
        if self.is_list_full():
            print(f'Queue is full')
            return

        #print(f'Inserting {item}')
        self.items[self.tail] = item
        self.tail = (self.tail + 1) % self.max_size
        self.size += 1

    def dequeue(self):
        item = self.items[self.head]
        self.head = (self.head + 1) % self.max_size
        self.size -= 1

        return item

    def is_list_full(self):
        if self.size == self.max_size:
            return True
        return False

    def is_empty(self):
        if self.size == 0:
            return True
        return False

size=int(input())
queue = Queue(size)
str=input()
str1=input()
str2=input()
queue.enqueue(str)
queue.enqueue(str1)
queue.enqueue(str2)

    
print(queue.items)
#print(queue.head)
#print(queue.tail)



```

OUTPUT
![image](https://github.com/user-attachments/assets/b6fea67e-1078-48b4-905a-773aa1b6890b)

RESULT
Thus, Python program with a function to insert string values into a Circular Queue was successfully and verfied.

