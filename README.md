# What is this?
This repository is made for the assignment of CSE316 (Operating Systems) as a part of CA3, for 4th Semester.   

The following two are the problems which were assigned:
- The Sleeping-Barber Problem. A barbershop consists of a waiting room with n chairs
and a barber room with one barber chair. If there are no customers to be served the barber
goes to sleep. If a customer enters the barbershop and all chairs are occupied then the
customer leaves the shop. If the barber is busy but chairs are available, then the customer sits in one of the free chairs. If the barber is asleep, the customer wakes up the barber.
Write a program to coordinate the barber and the customers.

- Write a program to implement priority scheduling algorithm with context switching time.
Prompt to user to enter the number of processes and then enter their priority, burst time and
arrival time also. Now whenever operating system preempts a process and shifts cpu’s control to some another process of higher priority assume that it takes 2 seconds for context
switching(dispatcher latency).Form a scenario, where we can give the processes are assigned
with priority where the lower integer number is higher priority and then context switch .. as the process waits the priority of the process increase at rate of one per 2 time units of wait.
Calculate waiting time and turnaround time for each process.

#### The Sleeping barber problem:
 The Sleeping Barber Problem: The problem involves the use of locks and semaphores to avoid deadlock in the processes. In the solution, we make use of three semaphores. First is for the customer which counts the number of customers present in the waiting room (customer in the barber chair is not included because he is not waiting). Second, the barber 0 or 1 is used to tell whether the barber is idle or is working, And the third mutex is used to provide the mutual exclusion which is required for the process to execute. In the solution, the customer has the record of the number of customers waiting in the waiting room if the number of customers is equal to the number of chairs in the waiting room then the upcoming customer leaves the barbershop.
 When the barber shows up in the morning, he executes the procedure barber, causing him to block on the semaphore customers because it is initially 0. Then the barber goes to sleep until the first customer comes up.   
 To run: Open the file in a terminal and type ```gcc -pthread sleepingBarber.c```

#### Priority Scheduling Algorithm:
 Priority scheduling is a non-preemptive algorithm and one of the most common scheduling algorithms in batch systems. Each process is assigned a priority. Process with the highest priority is to be executed first and so on. Processes with the same priority are executed on first come first served basis. Priority can be decided based on memory requirements, time requirements or any other resource requirement.   
To run: Open the file in a terminal and type ```python3 prorityScheduling.py```
