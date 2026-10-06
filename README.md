# Task Scheduler

A simple **round-robin task scheduler** implemented as a personal embedded systems project.

The scheduler runs **four tasks** alternately using a **1-second time slice**. The project is written in a low-level style and does **not use the HAL library**, providing direct experience with task scheduling, CPU context management, and interrupts.

## Features

- Round-robin task scheduling
- Four independent tasks
- 1-second time slice for each task
- Context switching between tasks
- CPU register/context management
- Interrupt-based scheduling
- Low-level implementation without HAL libraries

## What I Learned

Through this project, I gained hands-on experience with:

- Task scheduling algorithms
- Round-robin scheduling
- CPU register management
- Context switching
- Interrupt and exception handling
- Low-level embedded programming

## Example Output

```text
Hello from task 4
Hello from task 4
Hello from task 4
Hello from task 4

Task 1 will be executed
An exception occurred!

Hello from task 1
Hello from task 1
Hello from task 1
Hello from task 1

Task 2 will be executed
An exception occurred!

Hello from task 2
Hello from task 2
Hello from task 2
Hello from task 2

Task 3 will be executed
An exception occurred!

Hello from task 3
Hello from task 3
Hello from task 3
Hello from task 3

Task 4 will be executed
An exception occurred!

Hello from task 4
Hello from task 4
Hello from task 4
Hello from task 4
```

The output demonstrates the scheduler switching execution sequentially between the four tasks.

## Demo

<img width="1440" height="750" alt="Task Scheduler Demo" src="https://github.com/user-attachments/assets/e2cfdb48-e7a0-40ad-aa2d-68ddb9dab374" />

## Scheduling Flow

```text
Task 1
  ↓
Task 2
  ↓
Task 3
  ↓
Task 4
  ↓
Task 1
  ↓
 ...
```

Each task receives approximately **1 second of CPU execution time** before the scheduler switches to the next task.
