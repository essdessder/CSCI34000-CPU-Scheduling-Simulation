# CSCI34000-CPU-Scheduling-Simulation

The main home project for CSCI34000 Operating Systems course at Hunter College (Spring 2020)

Professor: Pavel Shostak

Final Score: 100/100

Goal: To build an executable file to simulate operating system scheduling based on the below specifications 

The project is due to May 12 (11:59 pm).

 

The program should be submitted ONLY via BlackBoard.

No late submissions.

The project is meant for individual work only. My “questions about the project” policy is still in place.

The program must compile and run on Linux Lab computers (0 points if it doesn't).

If you submit more than 5 files, please pack them into archive.

If your program requires compilation with some specific command, please create a make-file or README.txt file with this specific compilation command in it. There is no need to send me the already-compiled executable files.

The project can be done in one of the following programming languages: C++ , Python , Java .

All your source-files should start with a comment with your name in it.

 

I will subtract points for poor programming practices, including but not limited to:

goto operator
non-constant global variables
variable-length arrays in C++
lack of classes and poor program structure
bad variable naming
extreme inefficiencies
 

You should write a program that simulates some aspects of operating systems. There is no real system programming involved. The whole simulation is based on the text inputs that the program receives from user.

 

CPU scheduling: your program should implement the following CPU scheduling scheme:

 

there are two levels of a ready-queue: one for RT-processes and one for common processes.
on each level you practice round-robin.
you run common processes only if there is no RT-processes waiting.
if RT-process arrives while common process is running, common process gets preemptied and sent to the head of the common processes ready-queue.
 

All I/O-queues are FCFS.

 

Memory: your program should simulate contiguous memory management with “first-fit” approach. You are not allowed to separately represent each byte of memory in your simulation.

 

 

At the start, your program asks the user three questions:

How much RAM memory is there on the simulated computer? Your program receives the number in bytes (no kilobytes or words). I can enter any number up to 4000000000 (4 billions).
How many hard disks does the simulated computer have? The enumeration of the hard disks starts with 0.
 

After that, the simulation begins. Your program constantly listens for the user inputs. You should NOT ask for a confirmation to enter another input. The user inputs signal some system events. Your program simulates the corresponding system behaviour. The possible inputs are:

 

A   size     ‘A’ input means that a new common process has been created. When the new process arrives, your program should create its PCB and place the process in the ready-queue or the CPU. The requested amount of memory should be allocated for the new process. When choosing a PID for the new process start from 1 and go up. Do NOT reuse PIDs of the terminated processes. For example, the command A 1000 means that a new common process has been created and it requires 1000 bytes of memory.

 

AR   size   the same as ‘A’ but the new process is an RT-process. 

 

Q   means that the time slice has ended for the currently running process.

 

t   currently running process terminates 


d number       The process that currently uses the CPU requests the hard disk #number.

 

D number   The hard disk #number has finished the work for one process.

  

S r     Shows what process is currently using the CPU and what processes are waiting on both levels of the ready-queue.

 

S i      Shows what processes are currently using the hard disks and what processes are waiting to use them. For each busy hard disk show the process that uses it and show its I/O-queue. The enumeration of hard disks starts from 0.

 

S m   Shows the state of memory. Show the range of memory addresses used by each process in the system.

 

 

Comments:

User input can come with any number of whitespaces in any position. Your program is responsible for correct input parsing.
 

 

Good Luck!
