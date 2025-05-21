Exp.No:37  
PRIORITY QUEUE

AIM  
To write a Python program for simple implementation of Priority Queue using Queue.

ALGORITHM
Start.

Initialize an empty list to represent the priority queue. Each element will be a tuple: (priority, data).

Define a function enqueue(data, priority) to insert elements:

Append (priority, data) tuple to the list.

Define a function dequeue() to remove and return the element with the highest priority (lowest priority number):

If the queue is empty, print "Queue is empty" and return None.

Otherwise, search through the list to find the element with the minimum priority value.

Remove that element from the list and return its data.

In the main program, call enqueue to add elements with priorities.

Call dequeue to remove elements in priority order.

End.

PROGRAM
```
# A simple implementation of Priority Queue
# using Queue.
class PriorityQueue(object):
	def __init__(self):
		self.queue = []

	def __str__(self):
		return ' '.join([str(i) for i in self.queue])

	# for checking if the queue is empty
	def isEmpty(self):
		return len(self.queue) == 0

	# for inserting an element in the queue
	def insert(self, data):
		self.queue.append(data)

	# for popping an element based on Priority
	def delete(self):
		try:
			max_val = 0
			for i in range(len(self.queue)):
				if self.queue[i] > self.queue[max_val]:
					max_val = i
			item = self.queue[max_val]
			del self.queue[max_val]
			return item
		except IndexError:
			print()
			exit()


myQueue = PriorityQueue()
n=int(input())	
for i in range(0, n):
    ele = int(input())
    myQueue.insert(ele)
	
print(myQueue)		
while not myQueue.isEmpty():
	print(myQueue.delete())

```

OUTPUT
![image](https://github.com/user-attachments/assets/7adff00e-0f12-40f4-b2b6-414a221cf6d1)

RESULT
Thus,  Python program for simple implementation of Priority Queue using Queue was successfully implemented and verified.
