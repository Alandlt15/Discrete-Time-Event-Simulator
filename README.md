# Discrete-Time Event Simulator

### Project Overview:
This project is a representation of a queuing system with an Event Queue, a Ready Queue and processes. At runtime, the system generates arrival time and service time for each process. The average arrival rate follows a Poisson Distribution (hence exponential inter-arrival times). Service times follow an Exponential Distribution. The simulation stops after 10,000 processes have been executed.

### Break Down:
Events (e.g., process arrival, process departure) that occur causes the simulator to update its current state (e.g., cpu busy/idle, contents of the Ready queue). Events are kept in a priority queue called Event Queue that describes the future events and is kept sorted by the time of each event. The simulator keeps a clock variable the represents the current time which initially takes the time of the first event in the Event Queue. As the simulator runs and events are handled, additional future events may be added to the Event Queue. 

For example, when a process gets serviced by the CPU and completes, another process can
start executing (if one is waiting in the Ready queue) and under FCFS, we know exactly when this process would finish (since FCFS is non-preemptive), so we can schedule a departure event in the future and place it in the Event queue.

### Metrics:
After the program is done executing, it outputs the following metrics:

- Average Turnaround Time of Processes

- Total Throughput (number of processes done per unit time)

- CPU Utilization

- Average Number of Processes in the Ready Queue

### How to Run the Project:
The easiest and simples way to run the program is by downloading/copying the main.cpp file and pasting it in your IDE of choice. 

It takes 2 inputs:

1. Average Arrival Rate (Lambda):

    (eg. 10) for an average of 10 processes per second

3. Average Service Time:
   
    (eg. 04) for an average service time of .04 seconds

## Acknowlegdments
Special thanks to Dr. Guirguis as this was a cool project for his course Computing Systems Fundamentals (CS3360) @ Texas State University.

October, 2024.
