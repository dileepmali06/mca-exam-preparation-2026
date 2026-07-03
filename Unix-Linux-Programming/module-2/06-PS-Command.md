# 2.3.1 The `ps` Command

> **Module:** Module 2 – Processes
>
> **Topic:** The `ps` Command
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

- Understand the purpose of the `ps` command.
- Display currently running processes.
- Interpret the output of the `ps` command.
- Use common options such as `-e`, `-f`, `-ef`, and `aux`.
- Find Process IDs (PID) for process management.
- Monitor Linux processes using practical commands.

---

# Introduction

Linux is a multitasking operating system.

Many processes run simultaneously, including:

- Terminal
- Browser
- File Manager
- Music Player
- Background Services
- System Processes

To display information about these running processes, Linux provides the **`ps` (Process Status)** command.

It is one of the most commonly used commands by Linux users, system administrators, developers, and DevOps engineers.

---

# Why Do We Need the `ps` Command?

The `ps` command is used to:

- View running processes.
- Find Process IDs (PID).
- Monitor active programs.
- Check Parent Process IDs (PPID).
- Verify whether an application is running.
- Identify processes before terminating them.

---

# Definition

The **`ps` (Process Status)** command displays information about the currently running processes in a Linux system.

It provides details such as Process ID, Terminal, CPU Time, Parent Process ID, and Command Name.

---

# Basic Syntax

```bash
ps
```

---

# Basic `ps` Command

Run:

```bash
ps
```

Example Output

```text
PID TTY          TIME CMD
2480 pts/0    00:00:00 bash
2650 pts/0    00:00:00 ps
```

---

# Explanation of Output

| Column | Meaning |
|---------|----------|
| PID | Process ID |
| TTY | Terminal Name |
| TIME | CPU Time Used |
| CMD | Executed Command |

---

# PID (Process ID)

Every running process has a unique Process ID.

Example

```text
2480
```

The PID is used to identify and manage processes.

---

# TTY

TTY stands for **Teletype Terminal**.

It indicates the terminal from which the process is running.

Example

```text
pts/0
```

---

# TIME

Displays the amount of CPU time consumed by the process.

Example

```text
00:00:01
```

---

# CMD

Displays the command or program that started the process.

Example

```text
bash
```

---

# `ps -e`

The `-e` option displays **all running processes** in the system.

## Syntax

```bash
ps -e
```

Example Output

```text
PID TTY TIME CMD

1 ? 00:00:03 systemd

850 ? 00:00:00 NetworkManager

2400 pts/0 00:00:00 bash
```

---

# `ps -f`

The `-f` option displays process information in **Full Format**.

## Syntax

```bash
ps -f
```

Example Output

```text
UID PID PPID C STIME TTY TIME CMD
```

---

# Meaning of New Columns

| Column | Meaning |
|----------|---------|
| UID | User ID |
| PID | Process ID |
| PPID | Parent Process ID |
| C | CPU Usage |
| STIME | Start Time |
| TTY | Terminal |
| TIME | CPU Time |
| CMD | Command Name |

---

# Parent Process ID (PPID)

PPID stands for **Parent Process ID**.

Every process (except the first system process) is created by another process.

Example

```text
Terminal

↓

bash

↓

sleep
```

Here,

- `bash` is the Parent Process.
- `sleep` is the Child Process.

---

# `ps -ef`

The `-ef` option displays **all running processes** in **Full Format**.

## Syntax

```bash
ps -ef
```

This is one of the most commonly used Linux commands.

It shows:

- User
- PID
- PPID
- Start Time
- Command
- Terminal

---

# `ps aux`

The `aux` option displays detailed information about all running processes.

## Syntax

```bash
ps aux
```

Example Output

```text
USER PID %CPU %MEM VSZ RSS TTY STAT START TIME COMMAND
```

---

# Meaning of Important Columns

| Column | Meaning |
|----------|---------|
| USER | Owner of the Process |
| PID | Process ID |
| %CPU | CPU Usage |
| %MEM | Memory Usage |
| VSZ | Virtual Memory Size |
| RSS | Physical Memory Usage |
| STAT | Process State |
| START | Start Time |
| TIME | CPU Time |
| COMMAND | Executed Command |

---

# Difference Between `ps` Options

| Command | Description |
|----------|-------------|
| `ps` | Shows processes running in the current terminal |
| `ps -e` | Displays all running processes |
| `ps -f` | Displays processes in full format |
| `ps -ef` | Displays all processes with full details |
| `ps aux` | Displays detailed CPU and Memory usage |

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

Display Current Terminal Processes

```bash
ps
```

---

## Step 3

Display All Running Processes

```bash
ps -e
```

---

## Step 4

Display Full Process Information

```bash
ps -f
```

---

## Step 5

Display All Processes with Full Information

```bash
ps -ef
```

---

## Step 6

Display CPU and Memory Usage

```bash
ps aux
```

---

# Expected Output

```text
$ ps

PID TTY TIME CMD

2480 pts/0 00:00:00 bash

2650 pts/0 00:00:00 ps
```

---

```text
$ ps -e

PID TTY TIME CMD

1 ? 00:00:03 systemd

850 ? 00:00:00 NetworkManager

2400 pts/0 00:00:00 bash
```

---

```text
$ ps -ef

UID PID PPID C STIME TTY TIME CMD

root 1 0 0 10:20 ? 00:00:03 systemd
```

---

# Real World Applications

## Software Developers

- Verify whether an application is running.
- Find the PID before stopping a process.
- Debug application execution.

---

## Backend Developers

- Monitor Node.js, Java, or Python servers.
- Identify running API services.

---

## DevOps Engineers

- Monitor production services.
- Identify high CPU and memory usage.
- Troubleshoot server issues.

---

## Linux Administrators

- Monitor all system processes.
- Detect zombie or orphan processes.
- Manage running services.

---

# Common Beginner Mistakes

### Mistake 1

Thinking `ps` displays all system processes.

**Correct:**

The basic `ps` command shows only the processes associated with the current terminal.

---

### Mistake 2

Confusing PID with PPID.

**Correct:**

- PID → Current Process ID
- PPID → Parent Process ID

---

### Mistake 3

Thinking `ps` continuously updates.

**Correct:**

The `ps` command displays a snapshot of the current processes.

For live monitoring, use:

```bash
top
```

or

```bash
htop
```

---

# Advantages

- Easy to use.
- Displays running processes.
- Helps identify Process IDs.
- Useful for process management.
- Supports multiple display formats.

---

# Limitations

- Shows only a snapshot of running processes.
- Does not continuously update.
- Large systems may produce lengthy output.

---

# Quick Revision

- `ps` stands for **Process Status**.
- Displays running process information.
- `ps -e` shows all processes.
- `ps -f` displays full process details.
- `ps -ef` displays all processes in full format.
- `ps aux` displays CPU and memory usage.

---

# Important Keywords

- Process Status
- PID
- PPID
- UID
- TTY
- CPU Usage
- Memory Usage
- Command

---

# Frequently Asked Questions

## What is the `ps` command?

The `ps` command displays information about running processes.

---

## What does PID mean?

PID stands for **Process ID**.

---

## Which command displays all running processes?

```bash
ps -e
```

---

## Which command displays all processes with full information?

```bash
ps -ef
```

---

## Which command displays CPU and memory usage?

```bash
ps aux
```

---

# MCQ Questions

### Q1.

The `ps` command stands for:

A. Process Start

B. Process Status

C. Program Status

D. Process Stop

**Answer:** B

---

### Q2.

Which option displays all running processes?

A. `ps -a`

B. `ps -e`

C. `ps -d`

D. `ps -x`

**Answer:** B

---

### Q3.

PPID stands for:

A. Primary Process ID

B. Parent Process ID

C. Program Process ID

D. Process Program ID

**Answer:** B

---

### Q4.

Which command displays detailed CPU and memory information?

A. `ps`

B. `ps -f`

C. `ps aux`

D. `pwd`

**Answer:** C

---

### Q5.

Which command displays all processes in full format?

A. `ps -ef`

B. `ps -l`

C. `ps -d`

D. `ps -r`

**Answer:** A

---

# Interview Questions

- What is the purpose of the `ps` command?
- Explain the difference between `ps` and `ps -ef`.
- What is the difference between PID and PPID?
- Explain the output of the `ps` command.
- Why is the `ps` command important in Linux?

---

# Viva Questions

1. What is the `ps` command?
2. What is PID?
3. What is PPID?
4. What is the use of `ps -e`?
5. What is the use of `ps aux`?

---

# 2 Marks Questions

1. Define the `ps` command.
2. What is PID?
3. What is PPID?
4. What is the purpose of `ps -e`?

---

# 5 Marks Questions

1. Explain the `ps` command with examples.
2. Explain the options of the `ps` command.
3. Explain PID and PPID.

---

# Long Answer Questions

1. Explain the `ps` command and its options with suitable examples.
2. Explain the output of the `ps` command.
3. Explain the practical applications of the `ps` command.

---

# Command Cheat Sheet

| Command | Purpose |
|----------|---------|
| `ps` | Display current terminal processes |
| `ps -e` | Display all running processes |
| `ps -f` | Display full process information |
| `ps -ef` | Display all processes with full details |
| `ps aux` | Display CPU and memory usage |

---

# Previous Year Exam Focus

⭐⭐⭐⭐⭐ Very Important

- `ps` Command
- Process Status
- PID
- PPID
- `ps -e`
- `ps -f`
- `ps -ef`
- `ps aux`

---

# Summary

- The `ps` command is used to display information about running processes.
- It provides details such as PID, PPID, TTY, CPU Time, and Command Name.
- `ps -e` shows all processes, while `ps -f` displays detailed information.
- `ps -ef` combines all processes with full details, and `ps aux` provides CPU and memory usage information.
- The `ps` command is an essential tool for Linux users, developers, system administrators, and DevOps engineers.

---

# Related Topics

⬅️ Previous Topic

**05-Suspend-Interrupt-and-Kill-a-Process.md**

➡️ Next Topic

**07-Batch-Command.md**