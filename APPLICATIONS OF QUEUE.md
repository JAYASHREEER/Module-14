Exp.No:40  
APPLICATIONS OF QUEUE

AIM  
To write a Python program to implement FCFS Process Scheduling using a queue.

ALGORITHM  
1.Start
2.Get the number of processes n from the user.
3.Create an empty queue or list to store burst times of each process.
4.For each process i from 1 to n:
Get the burst time and append it to the queue.
5.Initialize:
waiting_time[0] = 0 (first process has no waiting time)
6.For each process i from 1 to n-1:
waiting_time[i] = waiting_time[i-1] + burst_time[i-1]
7.For each process i from 0 to n-1:
turnaround_time[i] = waiting_time[i] + burst_time[i]
8.Display:
Process ID, Burst Time, Waiting Time, and Turnaround Time for each process.
9.Calculate and display:
Average Waiting Time
Average Turnaround Time
10.End

PROGRAM  
# Python3 program for implementation
# of FCFS scheduling

# Function to find the waiting
# time for all processes
def findWaitingTime(processes, n,
					bt, wt):

	# waiting time for
	# first process is 0
	wt[0] = 0

	# calculating waiting time
	for i in range(1, n ):
		wt[i] = bt[i - 1] + wt[i - 1]

# Function to calculate turn
# around time
def findTurnAroundTime(processes, n,
					bt, wt, tat):

	# calculating turnaround
	# time by adding bt[i] + wt[i]
	for i in range(n):
		tat[i] = bt[i] + wt[i]

# Function to calculate
# average time
def findavgTime( processes, n, bt):

	wt = [0] * n
	tat = [0] * n
	total_wt = 0
	total_tat = 0

	# Function to find waiting
	# time of all processes
	findWaitingTime(processes, n, bt, wt)

	# Function to find turn around
	# time for all processes
	findTurnAroundTime(processes, n,
					bt, wt, tat)

	# Display processes along
	# with all details
	print( "Processes Burst time " +
				" Waiting time " +
				" Turn around time")

	# Calculate total waiting time
	# and total turn around time
	for i in range(n):
	
		total_wt = total_wt + wt[i]
		total_tat = total_tat + tat[i]
		print(" " + str(i + 1) + "   " +
					str(bt[i]) + "  " +
					str(wt[i]) + "    " +
					str(tat[i]))

	print( "Average waiting time = "+
				str(total_wt / n))
	print("Average turn around time = "+
					str(total_tat / n))

# Driver code
if __name__ =="__main__":
	
	# process id's
	processes = [ 1, 2, 3]
	n = len(processes)

	# Burst time of all processes
	t0=int(input())
	t1=int(input())
	t2=int(input())
	burst_time = [t0,t1,t2]

	findavgTime(processes, n, burst_time)

OUTPUT
![image](https://github.com/user-attachments/assets/cffb3f43-0385-483c-8dfa-69b7730d7fd5)

RESULT
Thus, the Python program to implement FCFS Process Scheduling using a queue was succesfully implemented and verified.

