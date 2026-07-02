# 1.1.1 Introduction to Operating System (OS)

---

# Introduction

An **Operating System (OS)** is the most important system software in a computer.

It acts as an interface between the **User**, **Application Programs**, and the **Computer Hardware**.

Without an Operating System, a computer cannot function properly because the hardware cannot communicate directly with the user or application software.

Examples of Operating Systems:

- Microsoft Windows
- Linux
- UNIX
- macOS
- Android
- iOS

> According to the PDF, the Operating System is responsible for managing computer hardware resources and providing services to application programs.

---

# What is an Operating System?

## Definition

An **Operating System (OS)** is system software that manages computer hardware and software resources and provides a platform for running application programs.

It acts as a bridge between the user and the computer hardware.

```text
User
   │
Application Software
   │
Operating System
   │
Hardware
```

---

# Components of a Computer System

According to the PDF, a computer system consists of four major components.

## 1. Hardware

Hardware includes all physical components of the computer.

Examples:

- CPU
- RAM
- Hard Disk / SSD
- Keyboard
- Mouse
- Monitor
- Printer

---

## 2. Operating System

The Operating System controls all hardware resources and provides an environment for application software.

Examples:

- Windows
- Linux
- UNIX
- macOS

---

## 3. Application Programs

Application software helps users perform specific tasks.

Examples:

- Google Chrome
- Microsoft Word
- VLC Media Player
- Visual Studio Code
- Photoshop

Applications never communicate directly with hardware.

They always communicate through the Operating System.

---

## 4. User

The person who uses the computer system is called the User.

Examples:

- Student
- Software Developer
- Teacher
- System Administrator

---

# Working of Operating System

The communication process inside a computer is:

```text
User
   │
Application
   │
Operating System
   │
Hardware
```

Example:

```text
You
↓
Google Chrome
↓
Ubuntu Linux
↓
CPU
RAM
SSD
```

The browser never directly accesses the hardware.

The Operating System performs all hardware operations.

---

# Why Operating System is Required?

Without an Operating System:

- Applications cannot run.
- Hardware cannot be managed.
- Memory cannot be allocated.
- Files cannot be stored.
- Multiple programs cannot run simultaneously.

The Operating System solves these problems.

---

# Functions of Operating System

The Operating System performs many important functions.

---

## 1. Process Management

A process is a program that is currently running.

The Operating System:

- Creates processes
- Executes processes
- Terminates processes
- Schedules CPU time
- Manages multiple processes

### Example

```text
Chrome
VS Code
Spotify

↓

Operating System

↓

CPU Scheduling
```

---

## 2. Memory Management

Memory Management controls the usage of RAM.

Responsibilities:

- Allocate memory
- Deallocate memory
- Protect memory
- Manage Virtual Memory

Example:

```text
Chrome
2 GB RAM

VS Code
700 MB

Ubuntu
System Memory
```

---

## 3. File Management

The Operating System manages all files and directories.

Functions include:

- Create files
- Delete files
- Rename files
- Copy files
- Move files
- Store files
- Retrieve files

---

## 4. Device Management

The Operating System controls all hardware devices.

Examples:

- Keyboard
- Mouse
- Printer
- Monitor
- Hard Disk
- USB Drive

The Operating System communicates with these devices using **Device Drivers**.

---

## 5. Security and Protection

The Operating System provides security through:

- User Login
- Password Protection
- File Permissions
- Access Control

This prevents unauthorized access.

---

# Device Driver

## Definition

A **Device Driver** is a software program that allows the Operating System to communicate with hardware devices.

It converts Operating System commands into hardware-specific instructions.

### Example

```text
Application
        │
Operating System
        │
Device Driver
        │
Printer
```

Examples of Drivers:

- Printer Driver
- Graphics Driver
- Sound Driver
- Wi-Fi Driver
- Bluetooth Driver

---

# Kernel

The **Kernel** is the core part of the Operating System.

It is the first software loaded into memory when the computer starts.

The Kernel is responsible for:

- Process Management
- Memory Management
- Device Management
- File System Management
- CPU Scheduling

```text
Applications
      │
Operating System
      │
Kernel
      │
Hardware
```

---

# Operating System Examples

| Operating System | Developed By |
|-----------------|--------------|
| Windows | Microsoft |
| Linux | Community / GNU |
| UNIX | AT&T Bell Labs |
| macOS | Apple |
| Android | Google |

---

# Practical (Ubuntu VirtualBox)

Open Terminal:

```bash
Ctrl + Alt + T
```

Display Kernel Name

```bash
uname
```

Expected Output

```text
Linux
```

---

Display Complete System Information

```bash
uname -a
```

---

Display Operating System Details

```bash
hostnamectl
```

or

```bash
cat /etc/os-release
```

Expected Output

```text
Ubuntu
Version
Kernel
Architecture
```

---

# Common Beginner Mistakes

❌ Typing command incorrectly

```bash
Unmae
```

✅ Correct

```bash
uname
```

---

❌ Writing commands in uppercase

```bash
UNAME
```

✅ Correct

```bash
uname
```

Linux commands are case-sensitive.

---

# Real World Applications

Software Engineers use Operating Systems for:

- Software Development
- Programming
- Testing

Backend Developers use Linux servers to run:

- Node.js
- Java
- Python
- PHP

DevOps Engineers use Linux for:

- Docker
- Kubernetes
- Jenkins
- CI/CD Pipelines

Cloud Engineers use Linux in:

- AWS EC2
- Azure Virtual Machines
- Google Cloud Compute Engine

Most web servers run Linux because it is stable, secure, and efficient.

---

# Advantages of Operating System

- Easy interaction between user and hardware
- Efficient resource management
- Supports multitasking
- Improves system security
- Simplifies file management
- Better hardware utilization

---

# Disadvantages of Operating System

- System failure affects all applications.
- Some Operating Systems are expensive.
- Malware can affect the Operating System.
- Requires regular updates and maintenance.

---

# Quick Revision

- Operating System is system software.
- It acts as an interface between User and Hardware.
- It manages CPU, Memory, Files, and Devices.
- Kernel is the core of the Operating System.
- Device Drivers help communicate with hardware.
- Applications access hardware through the Operating System.

---

# Important Keywords

- Operating System
- Kernel
- Hardware
- Software
- User
- Application Program
- Process Management
- Memory Management
- File Management
- Device Management
- Device Driver
- CPU Scheduling
- Security

---

# Frequently Asked Questions

## Q1. What is an Operating System?

Operating System is system software that acts as an interface between the user and computer hardware.

---

## Q2. What are the main functions of an Operating System?

- Process Management
- Memory Management
- File Management
- Device Management
- Security

---

## Q3. What is a Kernel?

Kernel is the core component of an Operating System responsible for managing system resources.

---

## Q4. What is a Device Driver?

A Device Driver is software that enables communication between the Operating System and hardware devices.

---

# 2 Marks Questions

1. Define Operating System.
2. What is Kernel?
3. What is Device Driver?
4. Name any four Operating Systems.
5. What is Process Management?

---

# 5 Marks Questions

1. Explain Operating System.
2. Explain the functions of Operating System.
3. Explain the components of a computer system.
4. Explain Device Drivers with examples.

---

# Long Answer Questions

1. Explain Operating System with a neat diagram.
2. Explain the functions of Operating System in detail.
3. Explain Kernel and Device Driver with suitable examples.

---

# Practical Questions

1. Display Linux Kernel Name.

```bash
uname
```

2. Display Complete Kernel Information.

```bash
uname -a
```

3. Display Operating System Information.

```bash
hostnamectl
```

4. Display Ubuntu Version.

```bash
cat /etc/os-release
```

---

# University Exam Tips

If the question is:

**"Explain Operating System."**

Write your answer in the following order:

1. Definition
2. Diagram
3. Components of Computer System
4. Functions of Operating System
5. Kernel
6. Device Driver
7. Examples
8. Conclusion

This structure helps in scoring maximum marks.

---

# Summary

- Operating System is the most important system software.
- It acts as a bridge between the user and computer hardware.
- It manages processes, memory, files, devices, and security.
- Kernel is the heart of the Operating System.
- Device Drivers enable communication with hardware.
- Linux, Windows, UNIX, and macOS are common Operating Systems.
