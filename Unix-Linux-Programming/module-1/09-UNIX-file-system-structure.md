# UNIX File System Structure

---

# Introduction

A UNIX File System is not just a collection of files.

Internally, the disk is divided into different logical blocks.

Each block has a specific responsibility.

These blocks help UNIX:

- Boot the Operating System
- Manage Storage
- Store File Information
- Store Actual File Data

The UNIX File System consists of four major blocks:

1. Boot Block
2. Super Block
3. Inode Block
4. Data Block

---

# UNIX File System Structure Diagram

```text
+------------------------------------------------------+
|                    Hard Disk                         |
+------------------------------------------------------+

+------------------------------------------------------+
|                  Boot Block                          |
+------------------------------------------------------+

+------------------------------------------------------+
|                 Super Block                          |
+------------------------------------------------------+

+------------------------------------------------------+
|                 Inode Block                          |
+------------------------------------------------------+

+------------------------------------------------------+
|                  Data Block                          |
+------------------------------------------------------+
```

---

# 1. Boot Block

## Definition

The **Boot Block** is the first block of the UNIX File System.

It contains the bootstrap program that helps start the operating system.

Without the Boot Block, the operating system cannot boot.

---

## Responsibilities

- Starts the boot process.
- Loads the boot loader.
- Helps load the operating system into memory.

---

## Boot Process

```text
Power ON

↓

BIOS / UEFI

↓

Boot Block

↓

Boot Loader

↓

Kernel

↓

Operating System Starts
```

---

## Practical

Display boot directory

```bash
ls /boot
```

Example Output

```text
config
grub
initrd.img
vmlinuz
```

---

# 2. Super Block

## Definition

The **Super Block** stores information about the entire file system.

Whenever a file is created, deleted, or modified, the Super Block is updated.

It is one of the most important structures in the UNIX File System.

---

## Information Stored in Super Block

- File System Size
- Total Number of Blocks
- Free Blocks
- Free Inodes
- Block Size
- Status of File System

---

## Why Super Block is Important?

Before creating a new file, UNIX checks the Super Block to determine:

- Is there enough free space?
- Is a free inode available?

Only then is the file created.

---

# 3. Inode Block

## Definition

An **Inode (Index Node)** is a special data structure that stores information (metadata) about a file.

Every file in UNIX has its own unique inode number.

---

# Metadata Stored in Inode

The Inode stores:

- File Type
- File Size
- File Permissions
- Owner ID
- Group ID
- Number of Links
- Access Time
- Modification Time
- Change Time
- Address of Data Blocks

---

## Important Exam Point ⭐

The **Inode does NOT store the File Name.**

The filename is stored inside the directory.

The directory maps:

```text
Filename

↓

Inode Number

↓

Inode

↓

Data Block
```

---

## Practical

Display inode number

```bash
ls -li
```

Example Output

```text
348291 notes.txt
```

Display complete metadata

```bash
stat notes.txt
```

Example Output

```text
Size

Permissions

Owner

Modify Time

Inode Number
```

---

# 4. Data Block

## Definition

The **Data Block** stores the actual contents of the file.

This is where user data is stored.

---

## Example

Suppose

```text
notes.txt
```

contains

```text
Hello Linux
```

The text:

```text
Hello Linux
```

is stored inside the **Data Block**.

---

## Complete Working

```text
notes.txt

↓

Directory

↓

Inode Number

↓

Inode

↓

Data Block

↓

Actual File Contents
```

---

# Complete UNIX File System Flow

```text
Hard Disk

│

├── Boot Block

│      ↓

│   Starts Operating System

│

├── Super Block

│      ↓

│  File System Information

│

├── Inode Block

│      ↓

│  File Metadata

│

└── Data Block

       ↓

 Actual File Data
```

---

# Practical (Ubuntu VirtualBox)

Open Terminal

```bash
Ctrl + Alt + T
```

Display Boot Files

```bash
ls /boot
```

Display Disk Usage

```bash
df -h
```

Display Inode Number

```bash
ls -li
```

Display Metadata

```bash
stat notes.txt
```

Display File System Information

```bash
df -T
```

---

# Common Beginner Mistakes

### Mistake 1

Thinking Boot Block stores user data.

Correct:

Boot Block only helps start the operating system.

---

### Mistake 2

Thinking Inode stores the filename.

Correct:

The filename is stored in the directory.

The Inode stores metadata.

---

### Mistake 3

Thinking Data Block stores permissions.

Correct:

Permissions are stored in the Inode.

The Data Block stores only the actual contents.

---

# Real World Applications

## Software Developers

Every source code file has its own inode.

Whenever the file is modified, metadata changes.

---

## Backend Developers

Linux servers use inode information to manage millions of files efficiently.

---

## DevOps Engineers

Commands like:

```bash
stat
```

and

```bash
ls -li
```

are commonly used for debugging file-related issues.

---

## Cloud Engineers

Linux file systems used in AWS, Azure, and Google Cloud rely on:

- Super Block
- Inode
- Data Block

for efficient storage management.

---

# Advantages of UNIX File System Structure

- Fast File Access
- Efficient Storage Management
- Better Security
- Reliable Data Organization
- Easy File Recovery
- High Performance

---

# Quick Revision

- Boot Block starts the operating system.
- Super Block stores file system information.
- Inode stores metadata.
- Data Block stores actual file contents.
- Every file has a unique inode number.
- The filename is stored in the directory, not in the inode.

---

# Important Keywords

- Boot Block
- Super Block
- Inode
- Metadata
- Data Block
- File System
- Inode Number

---

# Frequently Asked Questions

## Q1. What is the Boot Block?

The Boot Block contains the bootstrap program used to start the operating system.

---

## Q2. What is the Super Block?

The Super Block stores information about the entire file system.

---

## Q3. What is an Inode?

An Inode is a data structure that stores metadata about a file.

---

## Q4. Does an Inode store the filename?

No.

The filename is stored in the directory.

---

## Q5. Where is the actual file content stored?

Inside the Data Block.

---

# MCQ Questions

### Q1.

The first block of a UNIX File System is:

- A. Super Block
- B. Inode Block
- C. Boot Block
- D. Data Block

**Answer:** C

---

### Q2.

Which block stores file system information?

- A. Boot Block
- B. Super Block
- C. Data Block
- D. Directory

**Answer:** B

---

### Q3.

Which block stores metadata?

- A. Boot Block
- B. Data Block
- C. Inode Block
- D. Root Directory

**Answer:** C

---

### Q4.

Where is the actual file content stored?

- A. Boot Block
- B. Super Block
- C. Inode
- D. Data Block

**Answer:** D

---

### Q5.

Which command displays the inode number?

- A. pwd
- B. ls -li
- C. mkdir
- D. cd

**Answer:** B

---

### Q6. ⭐ Very Important

Which of the following is **NOT** stored in an Inode?

- A. File Size
- B. Owner
- C. File Name
- D. Permissions

**Answer:** C

---

# Interview Questions

- What is an Inode?
- Why does UNIX use Inodes?
- Explain Boot Block and Super Block.
- Why is the filename not stored in the Inode?

---

# Viva Questions

1. What is Boot Block?
2. What is Super Block?
3. What is Metadata?
4. What is an Inode?
5. What is a Data Block?

---

# Command Cheat Sheet

| Command | Purpose |
|----------|---------|
| `ls /boot` | Display Boot Files |
| `df -h` | Display Disk Usage |
| `df -T` | Display File System Type |
| `ls -li` | Display Inode Number |
| `stat filename` | Display File Metadata |

---

# Previous Year Exam Focus

⭐⭐⭐⭐⭐ Very Important

- UNIX File System Structure
- Boot Block
- Super Block
- Inode
- Data Block
- Inode vs File Name
- Diagram of UNIX File System Structure

---

# Summary

- UNIX File System is divided into Boot Block, Super Block, Inode Block, and Data Block.
- Boot Block starts the operating system.
- Super Block manages the entire file system.
- Inode stores metadata of files.
- Data Block stores the actual contents of files.
- Every file has a unique inode number.
- The filename is stored in the directory, while the inode stores information about the file.

---

# Related Topics

⬅️ Previous Topic

**1.2.1 UNIX File System**

➡️ Next Topic

**1.2.2 Absolute Path**