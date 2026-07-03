# 2.3.3 The `at` Command

> **Module:** Module 2 – Processes
>
> **Topic:** The `at` Command
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

- Understand the purpose of the `at` command.
- Schedule commands to execute at a specific future date and time.
- Display and remove scheduled jobs.
- Understand the working of the `atd` daemon.
- Differentiate between `at`, `batch`, and `cron`.
- Perform practical demonstrations in Ubuntu Linux.

---

# Introduction

Linux provides various scheduling utilities for automating tasks.

Sometimes a task needs to be executed immediately.

Sometimes it needs to run when the system load is low.

Sometimes it must execute at a specific date and time.

For one-time scheduled execution, Linux provides the **`at` command**.

The `at` command allows users to schedule commands or scripts for future execution.

---

# Why Do We Need the `at` Command?

There are many situations where commands need to execute automatically at a future time.

Examples include:

- Database Backup
- System Shutdown
- Running Shell Scripts
- File Cleanup
- Sending Reports
- Log Rotation

Instead of manually executing commands, the `at` command performs them automatically.

---

# Definition

The **`at` command** is used to schedule a command or script for one-time execution at a specified future date and time.

---

# Working of the `at` Command

```text
User

↓

at Command

↓

Specify Date & Time

↓

Job Queue

↓

Specified Time Arrives

↓

Command Executes Automatically
```

---

# Syntax

```bash
at TIME
```

Example

```bash
at 5:00 PM
```

The terminal displays:

```text
at>
```

Now enter one or more commands.

Finish by pressing:

```text
Ctrl + D
```

The job is stored and scheduled for execution.

---

# Time Formats Supported

## Specific Time

```bash
at 10:30 AM
```

---

## Noon

```bash
at noon
```

---

## Midnight

```bash
at midnight
```

---

## Tomorrow

```bash
at 8:00 AM tomorrow
```

---

## Relative Time

```bash
at now + 30 minutes
```

```bash
at now + 2 hours
```

```bash
at now + 3 days
```

---

## Specific Date

```bash
at 7:00 PM Jul 10
```

---

# Example 1 – Schedule a Simple Command

Run:

```bash
at now + 1 minute
```

Enter:

```bash
date
```

Press:

```text
Ctrl + D
```

After one minute, Linux automatically executes the command.

---

# Example 2 – Schedule Multiple Commands

Run:

```bash
at 6:00 PM
```

Enter:

```bash
pwd
whoami
ls
```

Press:

```text
Ctrl + D
```

All commands will execute at 6:00 PM.

---

# Example 3 – Schedule a Shell Script

Run:

```bash
at 9:00 PM
```

Enter:

```bash
/home/dilip/backup.sh
```

Press:

```text
Ctrl + D
```

The shell script will execute automatically at the scheduled time.

---

# Display Scheduled Jobs

The `atq` command displays all scheduled jobs.

## Syntax

```bash
atq
```

Example Output

```text
2 Tue Jul 01 17:00
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
atrm 2
```

---

# The `atd` Daemon

The `at` command works through the **`atd` daemon**.

The daemon continuously checks the job queue.

When the scheduled time arrives, it executes the job automatically.

---

# Installing the `at` Package

If the `at` command is unavailable, install it using:

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

# Difference Between `at`, `batch`, and `cron`

| Feature | `at` | `batch` | `cron` |
|---------|------|---------|--------|
| Execution | At a specified time | When system load is low | Repeated schedule |
| Frequency | One-time | One-time | Repeated |
| User specifies execution time | Yes | No | Yes |
| Depends on system load | No | Yes | No |
| Best Use | Future one-time task | Heavy tasks | Daily/Weekly automation |

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

Install the package (if required).

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

Create a Job.

```bash
at now + 2 minutes
```

Type:

```bash
date
```

Press:

```text
Ctrl + D
```

---

## Step 6

Display Scheduled Jobs.

```bash
atq
```

---

## Step 7

Remove the Job.

```bash
atrm 1
```

Replace **1** with the actual Job Number.

---

# Expected Output

```text
$ at now + 2 minutes

warning: commands will be executed using /bin/sh

at>

date

<Ctrl + D>

job 1 at Tue Jul 01 17:00:00 2026
```

---

```text
$ atq

1 Tue Jul 01 17:00
```

---

```text
$ atrm 1
```

---

# Real World Applications

## Software Developers

- Schedule build scripts.
- Run testing scripts.

---

## Backend Developers

- Schedule database backups.
- Schedule report generation.

---

## DevOps Engineers

- Deploy applications at night.
- Schedule server maintenance.
- Restart services automatically.

---

## Linux Administrators

- Automatic shutdown.
- Cleanup temporary files.
- Generate daily reports.

---

# Common Beginner Mistakes

### Mistake 1

Thinking `at` executes commands immediately.

**Correct:** It executes commands only at the scheduled time.

---

### Mistake 2

Forgetting to press `Ctrl + D`.

**Correct:** The job is saved only after pressing `Ctrl + D`.

---

### Mistake 3

Thinking `at` repeats tasks automatically.

**Correct:** `at` executes a job only once.

Use `cron` for recurring jobs.

---

# Advantages

- Easy one-time scheduling.
- Supports multiple commands.
- Executes automatically.
- Useful for future tasks.

---

# Limitations

- Executes only once.
- Requires the `atd` daemon.
- Not suitable for recurring jobs.

---

# Quick Revision

- `at` schedules one-time tasks.
- Executes commands at a specific date and time.
- Uses the `atd` daemon.
- `atq` displays scheduled jobs.
- `atrm` removes scheduled jobs.
- `Ctrl + D` saves the job.

---

# Important Keywords

- at
- atd
- atq
- atrm
- Job Scheduling
- One-Time Scheduling

---

# Frequently Asked Questions

## What is the `at` command?

The `at` command schedules commands for one-time execution at a specified future time.

---

## Which daemon executes `at` jobs?

`atd`

---

## Which command displays scheduled jobs?

```bash
atq
```

---

## Which command removes scheduled jobs?

```bash
atrm JOB_NUMBER
```

---

## Does `at` execute jobs repeatedly?

No.

It executes a job only once.

---

# MCQ Questions

### Q1.

The `at` command is used for:

A. File Compression

B. One-Time Scheduling

C. Process Monitoring

D. User Management

**Answer:** B

---

### Q2.

Which daemon executes `at` jobs?

A. sshd

B. cron

C. atd

D. systemd

**Answer:** C

---

### Q3.

Which command displays scheduled jobs?

A. jobs

B. ps

C. atq

D. top

**Answer:** C

---

### Q4.

Which command removes a scheduled job?

A. kill

B. atrm

C. rm

D. bg

**Answer:** B

---

### Q5.

Which scheduling utility is used for recurring tasks?

A. at

B. batch

C. cron

D. ps

**Answer:** C

---

# Interview Questions

- What is the purpose of the `at` command?
- Explain the working of the `at` command.
- Differentiate between `at`, `batch`, and `cron`.
- What is the purpose of the `atd` daemon?
- Explain the `atq` and `atrm` commands.

---

# Viva Questions

1. What is the `at` command?
2. What is the `atd` daemon?
3. What is `atq`?
4. What is `atrm`?
5. What is the difference between `at` and `cron`?

---

# 2 Marks Questions

1. Define the `at` command.
2. What is `atq`?
3. What is `atrm`?
4. What is the `atd` daemon?

---

# 5 Marks Questions

1. Explain the `at` command with syntax.
2. Explain the working of the `at` command.
3. Differentiate between `at` and `batch`.

---

# Long Answer Questions

1. Explain the `at` command with suitable examples.
2. Explain the working of the `at` command with practical commands.
3. Compare `at`, `batch`, and `cron`.

---

# Command Cheat Sheet

| Command | Purpose |
|----------|---------|
| `at TIME` | Schedule a one-time job |
| `atq` | Display scheduled jobs |
| `atrm JOB_NUMBER` | Remove a scheduled job |
| `sudo apt install at` | Install the `at` package |
| `sudo systemctl enable atd` | Enable the `atd` daemon |
| `sudo systemctl start atd` | Start the `atd` daemon |
| `systemctl status atd` | Check daemon status |

---

# Previous Year Exam Focus

⭐⭐⭐⭐⭐ Very Important

- `at` Command
- `atd` Daemon
- `atq`
- `atrm`
- Difference between `at`, `batch`, and `cron`
- Practical Commands

---

# Summary

- The `at` command is used to schedule one-time tasks at a specified future date and time.
- It works with the `atd` daemon, which executes scheduled jobs automatically.
- Users can create jobs using `at`, view them with `atq`, and remove them using `atrm`.
- Unlike `batch`, which depends on system load, `at` executes jobs at a fixed time.
- For recurring tasks, Linux provides the `cron` scheduling utility.

---

# Related Topics

⬅️ Previous Topic

**07-Batch-Command.md**

➡️ Next Module

**Module 3 – File System and File Management**