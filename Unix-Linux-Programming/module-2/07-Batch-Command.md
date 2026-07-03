# 2.3.2 The `batch` Command

> **Module:** Module 2 – Processes
>
> **Topic:** The `batch` Command
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

- Understand the purpose of the `batch` command.
- Schedule commands to run when the system load is low.
- Understand the relationship between `batch` and `at`.
- Display and remove scheduled jobs.
- Perform practical demonstrations in Ubuntu Linux.
- Differentiate between `batch` and `at`.

---

# Introduction

Linux provides several utilities to schedule commands.

Sometimes we want a command to execute immediately.

Sometimes we want it to execute at a particular time.

Sometimes we want it to execute **only when the system becomes less busy**.

For this purpose, Linux provides the **`batch` command**.

The `batch` command schedules commands to run automatically when the system load becomes sufficiently low.

---

# Why Do We Need the `batch` Command?

Some commands consume a large amount of CPU or memory.

Examples include:

- Large Backup
- Database Export
- Video Conversion
- File Compression
- Log Analysis

Running these commands immediately may slow down the system.

The `batch` command waits until the system becomes less busy before executing them.

---

# Definition

The **`batch` command** schedules commands for execution when the system load becomes sufficiently low.

Unlike normal commands, execution does not begin immediately.

---

# Working of the `batch` Command

```text
User

↓

batch Command

↓

Job Queue

↓

System Load Checked

↓

Low System Load

↓

Command Executes
```

---

# Syntax

```bash
batch
```

After pressing Enter, the terminal displays:

```text
at>
```

Now type one or more commands.

Finish by pressing:

```text
Ctrl + D
```

The job is then scheduled for execution.

---

# Example 1 – Simple Batch Job

Run:

```bash
batch
```

Type:

```bash
echo "Hello Linux"
```

Press:

```text
Ctrl + D
```

Example Output

```text
job 1 at Tue Jul 01 11:30:00 2026
```

The command will execute automatically when the system load becomes low.

---

# Example 2 – Multiple Commands

Run:

```bash
batch
```

Type:

```bash
pwd
date
whoami
ls
```

Finish using:

```text
Ctrl + D
```

All commands become part of the same batch job.

---

# How Does `batch` Decide When to Execute?

The `batch` command checks the **system load**.

If the system is busy:

- The job waits in the queue.

When the CPU load decreases:

- Linux automatically executes the job.

---

# The `atd` Daemon

The `batch` command works through the **`atd` daemon**.

The daemon continuously checks:

- Scheduled jobs
- Current system load

If `atd` is not running, scheduled batch jobs will not execute.

---

# Installing the `batch` Command (Ubuntu)

Modern Ubuntu versions may not have the `batch` command installed.

Install it using:

```bash
sudo apt update
```

```bash
sudo apt install at
```

---

# Enable the Daemon

```bash
sudo systemctl enable atd
```

---

# Start the Daemon

```bash
sudo systemctl start atd
```

---

# Check Daemon Status

```bash
systemctl status atd
```

Expected Output

```text
active (running)
```

---

# Display Scheduled Jobs

The `atq` command displays all scheduled `at` and `batch` jobs.

## Syntax

```bash
atq
```

Example Output

```text
1 Tue Jul 01 11:30
```

---

# Remove a Scheduled Job

The `atrm` command removes a scheduled job.

## Syntax

```bash
atrm JOB_NUMBER
```

Example

```bash
atrm 1
```

The selected job is removed from the queue.

---

# Difference Between `batch` and `at`

| `batch` | `at` |
|----------|------|
| Executes when system load is low | Executes at a specified time |
| No fixed execution time | Fixed execution time |
| Load-dependent | Time-dependent |
| Used for heavy jobs | Used for scheduled jobs |

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

Check whether `batch` is available.

```bash
batch
```

If the command is not found:

```bash
sudo apt update
```

```bash
sudo apt install at
```

---

## Step 3

Enable the daemon.

```bash
sudo systemctl enable atd
```

---

## Step 4

Start the daemon.

```bash
sudo systemctl start atd
```

---

## Step 5

Create a Batch Job.

```bash
batch
```

Enter:

```bash
date
pwd
whoami
```

Press:

```text
Ctrl + D
```

---

## Step 6

View Scheduled Jobs.

```bash
atq
```

---

## Step 7

Remove the Job.

```bash
atrm 1
```

Replace `1` with the actual Job Number.

---

# Expected Output

```text
$ batch

at>

date

pwd

whoami

<Ctrl + D>

job 1 at Tue Jul 01 11:30:00 2026
```

---

```text
$ atq

1 Tue Jul 01 11:30
```

---

```text
$ atrm 1
```

---

# Real World Applications

## Software Developers

- Source code compilation
- Build automation
- Large project builds

---

## Backend Developers

- Database export
- Cache cleanup
- Large file processing

---

## DevOps Engineers

- Backup jobs
- Maintenance scripts
- Log cleanup
- Server optimization tasks

---

## Linux Administrators

- Disk cleanup
- Report generation
- File indexing
- System maintenance

---

# Common Beginner Mistakes

### Mistake 1

Thinking `batch` executes commands immediately.

**Correct:** It waits until the system load becomes low.

---

### Mistake 2

Thinking `batch` and `at` are identical.

**Correct:**

- `batch` → Executes when the system load is low.
- `at` → Executes at a specified time.

---

### Mistake 3

Forgetting to start the `atd` daemon.

**Correct:** Without the `atd` service, `batch` jobs will never execute.

---

# Advantages

- Reduces system load.
- Suitable for CPU-intensive tasks.
- Automatic execution.
- Easy scheduling.

---

# Limitations

- No exact execution time.
- Depends on current system load.
- Requires the `atd` daemon.

---

# Quick Revision

- `batch` schedules commands.
- Executes when system load is low.
- Uses the `atd` daemon.
- `atq` displays scheduled jobs.
- `atrm` removes scheduled jobs.

---

# Important Keywords

- batch
- at
- atd
- atq
- atrm
- Job Queue
- System Load

---

# Frequently Asked Questions

## What is the `batch` command?

The `batch` command schedules commands to execute when the system load becomes low.

---

## Which package provides the `batch` command?

The `at` package.

---

## Which daemon executes batch jobs?

`atd`

---

## Which command displays scheduled jobs?

```bash
atq
```

---

## Which command removes a scheduled job?

```bash
atrm JOB_NUMBER
```

---

# MCQ Questions

### Q1.

The `batch` command executes jobs:

A. Immediately

B. At shutdown

C. When system load becomes low

D. At login

**Answer:** C

---

### Q2.

The `batch` command belongs to which package?

A. bash

B. cron

C. at

D. ps

**Answer:** C

---

### Q3.

Which daemon executes `batch` jobs?

A. sshd

B. systemd

C. atd

D. cron

**Answer:** C

---

### Q4.

Which command displays scheduled jobs?

A. jobs

B. ps

C. atq

D. fg

**Answer:** C

---

### Q5.

Which command removes a scheduled job?

A. rm

B. kill

C. atrm

D. bg

**Answer:** C

---

# Interview Questions

- What is the purpose of the `batch` command?
- Explain the working of the `batch` command.
- Explain the difference between `batch` and `at`.
- What is the role of the `atd` daemon?
- Explain `atq` and `atrm`.

---

# Viva Questions

1. Define the `batch` command.
2. What is the purpose of the `atd` daemon?
3. What is the use of `atq`?
4. What is the use of `atrm`?
5. Differentiate between `batch` and `at`.

---

# 2 Marks Questions

1. Define the `batch` command.
2. What is `atq`?
3. What is `atrm`?
4. What is the `atd` daemon?

---

# 5 Marks Questions

1. Explain the `batch` command with syntax.
2. Explain the working of the `batch` command.
3. Differentiate between `batch` and `at`.

---

# Long Answer Questions

1. Explain the `batch` command with practical examples.
2. Explain the execution flow of the `batch` command.
3. Explain the `batch` command and related utilities (`atq`, `atrm`, `atd`).

---

# Command Cheat Sheet

| Command | Purpose |
|----------|---------|
| `batch` | Schedule a batch job |
| `atq` | Display scheduled jobs |
| `atrm JOB_NUMBER` | Remove a scheduled job |
| `sudo apt install at` | Install the `at` package |
| `sudo systemctl enable atd` | Enable the `atd` daemon |
| `sudo systemctl start atd` | Start the `atd` daemon |
| `systemctl status atd` | Check daemon status |

---

# Previous Year Exam Focus

⭐⭐⭐⭐⭐ Very Important

- `batch` Command
- `atd` Daemon
- `atq`
- `atrm`
- Difference between `batch` and `at`
- Practical Commands

---

# Summary

- The `batch` command schedules commands to execute when the system load becomes low.
- It is part of the `at` package and requires the `atd` daemon.
- Multiple commands can be added to a single batch job.
- The `atq` command displays scheduled jobs, while `atrm` removes them.
- The `batch` command is useful for executing resource-intensive tasks without affecting current system performance.

---

# Related Topics

⬅️ Previous Topic

**06-PS-Command.md**

➡️ Next Topic

**08-AT-Command.md**