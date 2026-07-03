# 1.1.5 UNIX Layered Architecture

> **Module:** Module 1 - Introduction
>
> **Topic:** 1.1.5 UNIX Layered Architecture
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

- Understand UNIX Layered Architecture.
- Explain the four layers of UNIX.
- Understand the role of Hardware, Kernel, Utilities, and User.
- Explain the functions of the Kernel.
- Understand Process Management, CPU Scheduling, Memory Management, and File Management.
- Understand the role of Shell in UNIX.

---

# Introduction

UNIX follows a **Layered Architecture**, where each layer has a specific responsibility.

Instead of allowing the user to communicate directly with hardware, UNIX divides the system into different layers.

This architecture makes UNIX:

- More Secure
- More Stable
- Easier to Maintain
- Easier to Upgrade
- More Reliable

Each layer communicates only with the layer directly above or below it.

---

# Why Layered Architecture?

Imagine a company.

```text
CEO
 │
Managers
 │
Employees
 │
Machines
```

The CEO never operates the machines directly.

Managers communicate with employees, and employees operate the machines.

Similarly, in UNIX:

```text
User
 │
Utilities / Shell
 │
Kernel
 │
Hardware
```

Each layer performs its own responsibility.

---

# UNIX Layered Architecture

The UNIX operating system consists of **four layers**.

```text
+-----------------------------+
|            User             |
+-----------------------------+

+-----------------------------+
| Utilities / Applications    |
| (Shell, Commands, Programs) |
+-----------------------------+

+-----------------------------+
|           Kernel            |
+-----------------------------+

+-----------------------------+
|          Hardware           |
+-----------------------------+
```

---

# Layer 1 – Hardware

## Definition

The Hardware layer is the lowest layer of UNIX.

It contains all the physical components of the computer.

Examples:

- CPU
- RAM
- Hard Disk / SSD
- Keyboard
- Mouse
- Monitor
- Printer
- Network Card

Hardware cannot perform any task on its own.

It requires instructions from the Kernel.

---

## Responsibilities

- Execute machine instructions.
- Store data.
- Accept input.
- Produce output.

---

# Layer 2 – Kernel

## Definition

The **Kernel** is the core (heart) of the UNIX Operating System.

It directly communicates with the hardware.

The Kernel is loaded into memory when the computer starts and remains in memory until the system shuts down.

---

# Responsibilities of Kernel

The Kernel performs several important tasks.

## 1. Process Management

A process is a program currently running in memory.

The Kernel:

- Creates processes
- Schedules processes
- Terminates processes
- Synchronizes processes

Example

```text
Chrome

VS Code

Terminal

↓

Kernel

↓

CPU
```

---

## 2. CPU Scheduling

The CPU can execute only one instruction at a time.

The Kernel decides:

- Which process gets CPU time.
- How long it runs.
- Which process runs next.

This is called **CPU Scheduling**.

Traditional UNIX scheduling is:

- Preemptive
- Time Sharing
- Priority Based

---

## 3. Memory Management

The Kernel manages RAM.

Functions include:

- Memory Allocation
- Memory Deallocation
- Virtual Memory
- Swap Area
- Demand Paging

Example

```text
Chrome → 2 GB

VS Code → 800 MB

Terminal → 150 MB
```

The Kernel allocates memory according to requirements.

---

## 4. Device Management

The Kernel controls all hardware devices.

Examples:

- Keyboard
- Mouse
- Printer
- USB Drive
- Network Adapter

Communication with hardware is performed through **Device Drivers**.

---

## 5. File Management

The Kernel manages the file system.

Responsibilities include:

- Creating files
- Deleting files
- Reading files
- Writing files
- File Permissions
- Directory Management

---

## 6. Inter Process Communication (IPC)

The Kernel allows different processes to communicate with each other.

Examples:

- Pipes
- Signals
- Shared Memory
- Message Queues

---

# Layer 3 – Utilities / Application Programs

## Definition

Utilities are programs that help users perform different tasks.

Examples:

```bash
ls
pwd
mkdir
cp
mv
rm
cat
grep
sort
```

These utilities do not communicate directly with hardware.

Instead, they request services from the Kernel.

---

## Working Example

Command

```bash
mkdir Project
```

Execution

```text
User

↓

Shell

↓

mkdir Utility

↓

Kernel

↓

Hard Disk

↓

Directory Created
```

---

# Layer 4 – User

The User is the top-most layer.

The user interacts with the operating system using:

- Shell
- Terminal
- GUI Applications

Examples:

- Student
- Developer
- Administrator

The User never communicates directly with the hardware.

---

# Role of Shell

The Shell acts as an interface between the User and the Kernel.

Responsibilities:

- Read user commands
- Validate commands
- Execute programs
- Display output
- Run shell scripts
- Manage environment variables

Flow:

```text
User

↓

Shell

↓

Kernel

↓

Hardware
```

---

# Complete Command Execution Flow

Suppose the user executes:

```bash
mkdir Linux
```

Internal Execution

```text
User

↓

Shell

↓

mkdir Utility

↓

Kernel

↓

File System

↓

Directory Created

↓

Output Displayed
```

---

# Process Management

## Definition

A Process is a program that is currently executing.

The Kernel is responsible for:

- Creating Processes
- Scheduling Processes
- Terminating Processes

### Practical

Display running processes.

```bash
ps
```

---

Display live processes.

```bash
top
```

Press **q** to exit.

---

# CPU Scheduling

The CPU cannot execute all programs simultaneously.

The Kernel rapidly switches CPU time between processes.

Example

```text
Chrome

↓

VS Code

↓

Terminal

↓

Music Player
```

This rapid switching creates the illusion that all applications are running together.

---

# Memory Management

The Kernel keeps track of RAM usage.

It ensures:

- No process accesses another process's memory.
- Memory is allocated efficiently.
- Unused memory is released.

---

# File Management

UNIX stores files in a hierarchical structure.

```text
/

├── home

├── etc

├── usr

├── var

├── bin
```

The Kernel manages all file operations.

---

# Practical (Ubuntu VirtualBox)

Open Terminal

```bash
Ctrl + Alt + T
```

---

## Display Kernel Version

```bash
uname -r
```

---

## Display Complete Kernel Information

```bash
uname -a
```

---

## Display System Information

```bash
hostnamectl
```

---

## Display Running Processes

```bash
ps
```

---

## Display Live Processes

```bash
top
```

Exit:

```text
q
```

---

# Common Beginner Mistakes

### Mistake 1

Thinking Shell and Kernel are the same.

Correct:

- Shell = Command Interpreter
- Kernel = Core of Operating System

---

### Mistake 2

Thinking Hardware communicates with User.

Correct:

Hardware communicates only through the Kernel.

---

### Mistake 3

Thinking Utilities communicate directly with Hardware.

Correct:

Utilities communicate with the Kernel.

---

# Real World Applications

## Software Developers

- Run programs
- Debug applications
- Compile source code

---

## Backend Developers

- Linux Servers
- Node.js
- Java
- Python

---

## DevOps Engineers

- Docker
- Kubernetes
- Bash
- Jenkins

---

## Cloud Engineers

Cloud platforms like:

- AWS
- Azure
- Google Cloud

are built on Linux Kernel concepts.

---

# Advantages of Layered Architecture

- Better Security
- Easier Maintenance
- Better Resource Management
- Improved Stability
- Modular Design
- Easy Troubleshooting

---

# Limitations

- Communication between layers may introduce slight overhead.
- More abstraction can make debugging lower layers difficult.

---

# Quick Revision

- UNIX consists of four layers.
- Hardware is the lowest layer.
- Kernel is the core of UNIX.
- Utilities provide user commands.
- User is the top-most layer.
- Shell acts as an interface between User and Kernel.
- Kernel manages processes, memory, CPU, devices, and files.

---

# Important Keywords

- UNIX Layered Architecture
- Hardware
- Kernel
- Utilities
- Shell
- User
- Process Management
- CPU Scheduling
- Memory Management
- Device Management
- File Management
- IPC

---

# MCQ Questions

## Q1.

How many layers are present in UNIX Layered Architecture?

- A. 2
- B. 3
- C. 4
- D. 5

**Answer:** C

---

## Q2.

Which layer is the core of UNIX?

- A. User
- B. Hardware
- C. Kernel
- D. Utility

**Answer:** C

---

## Q3.

Which layer directly communicates with hardware?

- A. User
- B. Shell
- C. Kernel
- D. Utility

**Answer:** C

---

## Q4.

Which command displays running processes?

- A. ls
- B. pwd
- C. ps
- D. cat

**Answer:** C

---

## Q5.

Which command displays live running processes?

- A. ps
- B. top
- C. ls
- D. pwd

**Answer:** B

---

## Q6.

Which layer is present at the top?

- A. Hardware
- B. Kernel
- C. User
- D. Utility

**Answer:** C

---

## Q7.

Which component manages memory?

- A. User
- B. Shell
- C. Kernel
- D. Utility

**Answer:** C

---

## Q8.

Which component executes user commands?

- A. Hardware
- B. Shell
- C. CPU
- D. RAM

**Answer:** B

---

# 2 Marks Questions

1. Define Kernel.
2. Define Process.
3. What is CPU Scheduling?
4. What is UNIX Layered Architecture?
5. What is the role of Shell?

---

# 5 Marks Questions

1. Explain UNIX Layered Architecture.
2. Explain the functions of Kernel.
3. Explain Process Management.
4. Explain Memory Management.

---

# Long Answer Questions

1. Explain UNIX Layered Architecture with a neat diagram.
2. Explain the functions of the Kernel in detail.
3. Explain command execution flow in UNIX.

---

# Viva Questions

- What is the difference between Shell and Kernel?
- Why is Kernel called the heart of UNIX?
- Why can't users directly access hardware?
- What is the purpose of CPU Scheduling?

---

# Command Cheat Sheet

| Command | Purpose |
|----------|---------|
| `uname -r` | Display Kernel Version |
| `uname -a` | Display Complete Kernel Information |
| `hostnamectl` | Display System Information |
| `ps` | Display Running Processes |
| `top` | Display Live Running Processes |

---

# Previous Year Exam Focus

⭐ Very Important

- UNIX Layered Architecture Diagram
- Functions of Kernel
- Process Management
- CPU Scheduling

---

# Summary

- UNIX follows a four-layer architecture.
- Hardware forms the base layer.
- Kernel is the core component responsible for managing system resources.
- Utilities provide commands and applications for users.
- Shell acts as an interface between the user and the kernel.
- Layered architecture makes UNIX secure, modular, and easy to maintain.

---

# Related Topics

⬅️ Previous Topic

**1.1.4 UNIX Features**

➡️ Next Topic

**1.1.6 Types of Shell (Bourne, Bash, Korn, C Shell)**