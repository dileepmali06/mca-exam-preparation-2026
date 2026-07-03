# 2.1.1 Process State and Transitions

> **Module:** Module 2 – Processes
>
> **Topic:** Process State and Transitions
>
> **Subject:** Unix/Linux Programming
>
> **Level:** Beginner → Advanced
>
> **University:** MCA Semester III
>
> **Based On:** Amity University PDF
>
> **Author:** Dilip
>
> **Maintained By:** Dilip

---

# Learning Objectives

After studying this topic, you will be able to:

- Understand what a Process is.
- Differentiate between Program and Process.
- Understand Process ID (PID).
- Explain Process States.
- Understand Process State Transitions.
- Draw the Process State Diagram.
- Perform basic process-related practicals in Ubuntu Linux.

---

# Introduction

Whenever we execute a program in Linux, it becomes a **Process**.

Linux manages every running task as a process.

Examples of processes include:

- Terminal
- Firefox
- Google Chrome
- VS Code
- Music Player
- Calculator

Every running application is treated as an independent process.

---

# Why Do We Need Processes?

Suppose your computer is performing the following tasks simultaneously:

- Listening to music
- Browsing the Internet
- Downloading files
- Editing a document

All these tasks run independently.

Linux achieves this by creating separate processes for each task.

Without processes, multitasking would not be possible.

---

# Program vs Process

Many students think Program and Process are the same.

Actually, they are completely different.

## Program

A Program is a collection of instructions stored on secondary storage (Hard Disk / SSD).

A Program is passive because it is not executing.

Example

```text
Google Chrome (Installed)

↓

Stored in SSD
```

---

## Process

A Process is a Program that is currently executing.

It is loaded into RAM and uses CPU resources.

Example

```text
Google Chrome

↓

Double Click

↓

Loaded into RAM

↓

Running

↓

Process
```

---

# Difference Between Program and Process

| Program | Process |
|----------|----------|
| Collection of Instructions | Program in Execution |
| Stored on Disk | Loaded in RAM |
| Passive Entity | Active Entity |
| No CPU Usage | Uses CPU |
| Static | Dynamic |

---

# What is a Process?

## Definition

A **Process** is a program that is currently executing.

It is the basic unit of execution in Linux.

Each process has its own:

- Process ID (PID)
- Memory
- Registers
- Stack
- Heap
- Program Counter

---

# Process ID (PID)

Every process in Linux is assigned a unique number called the **Process ID (PID)**.

Linux uses the PID to identify and manage processes.

Example

```text
Firefox

↓

PID 2201

------------------

Terminal

↓

PID 1840

------------------

VS Code

↓

PID 3250
```

Every running process has a different PID.

---

# Characteristics of a Process

A Process:

- Executes instructions.
- Uses CPU.
- Occupies memory.
- Has its own PID.
- Has its own execution state.
- Can communicate with other processes.

---

# Process States

During execution, a process does not remain in one state.

It changes from one state to another.

The major process states are:

- New
- Ready
- Running
- Waiting (Blocked)
- Terminated

These states together form the **Process Life Cycle**.

---

# 1. New State

A process enters the **New** state immediately after it is created.

At this stage:

- Linux creates the process.
- Required resources are allocated.
- Process has not yet started execution.

Example

```text
Double Click Firefox

↓

Process Created

↓

New State
```

---

# 2. Ready State

After creation,

the process enters the **Ready** state.

The process is ready to execute but is waiting for CPU allocation.

Example

```text
Firefox

↓

Waiting for CPU

↓

Ready State
```

---

# 3. Running State

When the CPU scheduler selects the process,

it enters the **Running** state.

Now the CPU executes its instructions.

Example

```text
Firefox

↓

CPU Allocated

↓

Running
```

---

# 4. Waiting (Blocked) State

Sometimes a process cannot continue execution because it is waiting for an event.

Examples:

- Waiting for keyboard input.
- Waiting for a file.
- Waiting for Internet response.
- Waiting for printer.

During this period, the CPU executes another process.

Example

```text
Firefox

↓

Waiting for Internet

↓

Waiting State
```

---

# 5. Terminated State

After completing its execution,

the process enters the **Terminated** state.

Linux releases all resources used by the process.

Example

```text
User Closes Firefox

↓

Execution Finished

↓

Terminated
```

---

# Process State Diagram

```text
                +-----------+
                |   New     |
                +-----------+
                      |
                      ▼
                +-----------+
                |   Ready   |
                +-----------+
                      |
                CPU Allocated
                      |
                      ▼
                +-----------+
                | Running   |
                +-----------+
                 ▲      │
                 │      │
      I/O Done   │      │ I/O Request
                 │      ▼
            +-----------+
            | Waiting   |
            +-----------+
                      |
                      ▼
                +-----------+
                |   Ready   |
                +-----------+

Running
   │
   ▼
Terminated
```

---

# Process Transitions

A Process Transition means moving from one state to another.

Examples:

### New → Ready

Process is created successfully.

---

### Ready → Running

CPU is assigned to the process.

---

### Running → Waiting

Process requests an I/O operation.

---

### Waiting → Ready

I/O operation completes.

---

### Running → Terminated

Execution completes.

---

# Practical (Ubuntu VirtualBox)

## Step 1

Open Terminal.

Shortcut:

```text
Ctrl + Alt + T
```

---

## Step 2

Display Running Processes

```bash
ps
```

---

## Step 3

Display Current Shell PID

```bash
echo $$
```

---

## Step 4

Display Live Running Processes

```bash
top
```

Exit

```text
Press q
```

---

## Step 5

If installed

```bash
htop
```

This displays an advanced process monitor.

---

# Expected Output

```text
PID TTY TIME CMD

1840 pts/0

bash

2121 pts/0

ps
```

---

# Real World Applications

## Software Developers

Monitor application execution.

---

## Backend Developers

Manage Node.js servers.

---

## DevOps Engineers

Monitor running services.

Restart failed processes.

---

## Linux Administrators

Manage user processes.

Kill unnecessary processes.

---

## Cloud Engineers

Monitor Linux virtual machines on AWS, Azure and Google Cloud.

---

# Common Beginner Mistakes

### Mistake 1

Thinking Program and Process are the same.

Correct:

Program = Stored Code

Process = Running Program

---

### Mistake 2

Thinking every process has the same PID.

Correct:

Each process has its own unique PID.

---

### Mistake 3

Thinking a process remains in Running state forever.

Correct:

Processes continuously change states.

---

# Quick Revision

- Program = Passive.
- Process = Active.
- Process = Running Program.
- Every process has a unique PID.
- Process States:
  - New
  - Ready
  - Running
  - Waiting
  - Terminated

---

# Important Keywords

- Process
- Program
- PID
- Process State
- Process Transition
- Ready Queue
- Running
- Waiting
- Terminated

---

# Frequently Asked Questions

## What is a Process?

A Process is a program that is currently executing.

---

## What is PID?

PID stands for Process ID.

It uniquely identifies every process.

---

## How many major process states are there?

Five.

- New
- Ready
- Running
- Waiting
- Terminated

---

## What is the difference between Program and Process?

A Program is stored code.

A Process is a running program.

---

# MCQ Questions

### Q1.

A Process is:

A. Stored File

B. Running Program

C. Folder

D. CPU

**Answer:** B

---

### Q2.

PID stands for:

A. Process Identification

B. Program ID

C. Process ID

D. Primary ID

**Answer:** C

---

### Q3.

Which state waits for CPU allocation?

A. Running

B. Waiting

C. Ready

D. New

**Answer:** C

---

### Q4.

Which state occurs after process completion?

A. Waiting

B. Running

C. Terminated

D. Ready

**Answer:** C

---

### Q5.

Which command displays running processes?

A. ls

B. ps

C. pwd

D. cd

**Answer:** B

---

# Interview Questions

- What is a Process?
- What is the difference between Program and Process?
- What is PID?
- Explain Process States.
- Draw the Process State Diagram.

---

# Viva Questions

1. Define Process.
2. Define Program.
3. What is PID?
4. List the Process States.
5. Explain the Running State.
6. Explain the Waiting State.

---

# 2 Marks Questions

1. Define Process.
2. Define Program.
3. What is PID?
4. What is Process Transition?

---

# 5 Marks Questions

1. Explain Process States.
2. Differentiate between Program and Process.
3. Explain Process State Transitions.

---

# Long Answer Questions

1. Explain Process State and Transition with a neat diagram.
2. Explain the Process Life Cycle in Linux.
3. Explain Program vs Process with suitable examples.

---

# Command Cheat Sheet

| Command | Purpose |
|----------|---------|
| `ps` | Display Running Processes |
| `top` | Live Process Monitor |
| `htop` | Advanced Process Monitor |
| `echo $$` | Display Current Shell PID |

---

# Previous Year Exam Focus

⭐⭐⭐⭐⭐ Very Important

- Process Definition
- Program vs Process
- PID
- Process States
- Process State Diagram
- Process Transitions
- ps Command

---

# Summary

- A Process is a program in execution.
- Every process has a unique Process ID (PID).
- Linux manages every running task as a process.
- A process moves through five major states: New, Ready, Running, Waiting, and Terminated.
- The movement between states is called a Process Transition.
- Commands like `ps`, `top`, and `htop` help monitor processes in Linux.

---

# Related Topics

⬅️ Previous Module

**Module 1 – Linux Fundamentals**

➡️ Next Topic

**02-Process-Context.md**