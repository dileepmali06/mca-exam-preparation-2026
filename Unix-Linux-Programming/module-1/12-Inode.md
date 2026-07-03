# 1.2.4 Inode

> **Module:** Module 1 - UNIX File System
>
> **Topic:** 1.2.4 Inode
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

- Understand what an Inode is.
- Explain why Linux uses Inodes.
- Understand Metadata.
- Understand Inode Numbers.
- Understand the Inode Table.
- Explain how Linux locates a file.
- Use Linux commands to display inode information.
- Understand the importance of Inodes in Linux.

---

# Introduction

In UNIX/Linux, every file is associated with a special data structure called an **Inode** (Index Node).

The operating system does not directly use the filename to access a file.

Instead, it first finds the inode associated with the filename and then uses the inode to locate the actual file data.

This design makes file access fast, efficient, and reliable.

---

# Why Do We Need Inodes?

Imagine a library containing thousands of books.

Each book has:

- Book Name
- Book Number

When a librarian wants to find a book, they usually search using the **Book Number**, not by reading every book title.

Similarly, Linux uses **Inode Numbers** internally to identify files.

The filename is only for users.

Linux actually works with inode numbers.

---

# What is an Inode?

## Definition

An **Inode (Index Node)** is a special data structure that stores metadata (information about a file) but **does not store the filename**.

Every file and directory has its own unique inode.

---

# Full Form

**Inode = Index Node**

---

# What is Metadata?

Metadata means:

> **Data about Data**

Example

Suppose there is a file:

```text
notes.txt
```

Metadata includes:

- File Size
- File Type
- Owner
- Group
- Permissions
- Creation Time
- Modification Time
- Access Time
- Link Count

This information is stored inside the Inode.

---

# Information Stored in an Inode

An Inode stores:

- File Type
- File Permissions
- Owner (UID)
- Group (GID)
- File Size
- Number of Links
- Access Time (atime)
- Modification Time (mtime)
- Change Time (ctime)
- Address of Data Blocks

---

# Information NOT Stored in an Inode

The following information is **not** stored inside an inode:

- File Name
- Directory Name

The filename is stored inside the directory.

---

# Inode Number

Every file has a unique identification number called the **Inode Number**.

Example

```text
notes.txt

↓

Inode Number

↓

530461
```

Linux internally identifies the file using this inode number.

---

# Inode Table

The file system maintains a table containing all inodes.

This table is called the **Inode Table**.

Whenever a file is created, Linux allocates:

- One Inode
- Required Data Blocks

---

# Working of an Inode

When a user opens a file, Linux follows these steps:

```text
User

↓

Directory

↓

Filename

↓

Inode Number

↓

Inode

↓

Metadata

↓

Data Block

↓

Actual File Content
```

The filename is first searched in the directory.

The directory returns the inode number.

Linux reads the inode.

The inode tells Linux where the actual data is stored.

Finally, Linux reads the data block.

---

# Inode Diagram

```text
Directory

↓

notes.txt

↓

Inode Number

↓

530461

↓

Inode

↓

Metadata

↓

Data Block

↓

Actual File Data
```

---

# Linux Commands Related to Inodes

## Display Inode Number

```bash
ls -i filename
```

Example

```bash
ls -i notes.txt
```

---

## Display Detailed File Information

```bash
stat notes.txt
```

This command displays:

- Inode Number
- File Size
- Permissions
- Owner
- Group
- Access Time
- Modify Time

---

## Display Inode Number Only

```bash
stat --format=%i notes.txt
```

---

## Display Detailed List with Inodes

```bash
ls -il
```

---

## Display Filesystem Inodes

```bash
df -i
```

This command shows:

- Total Inodes
- Used Inodes
- Free Inodes

---

# Practical (Ubuntu VirtualBox)

## Step 1

Open Terminal

```text
Ctrl + Alt + T
```

---

## Step 2

Create a File

```bash
touch notes.txt
```

---

## Step 3

Write Data

```bash
echo "Hello Linux" > notes.txt
```

---

## Step 4

Display Inode Number

```bash
ls -i notes.txt
```

Example Output

```text
530461 notes.txt
```

---

## Step 5

Display Complete Metadata

```bash
stat notes.txt
```

---

## Step 6

Display Only Inode Number

```bash
stat --format=%i notes.txt
```

---

## Step 7

Display Filesystem Inodes

```bash
df -i
```

---

# Real World Applications

## Software Developers

Understand file metadata while developing applications.

---

## Backend Developers

Manage configuration files and file permissions.

---

## DevOps Engineers

Monitor inode usage to avoid server issues.

---

## Cloud Engineers

Linux servers in AWS, Azure, and Google Cloud rely heavily on inode structures.

---

# Common Beginner Mistakes

### Mistake 1

Thinking the filename is stored inside the inode.

Correct:

The filename is stored in the directory.

---

### Mistake 2

Thinking metadata is actual file data.

Correct:

Metadata only describes the file.

---

### Mistake 3

Thinking every file shares the same inode.

Correct:

Every file has its own unique inode number.

---

# Advantages of Inodes

- Fast file lookup.
- Efficient file management.
- Better storage organization.
- Improved file security.
- Easy metadata management.

---

# Limitations

- Number of inodes is fixed when the file system is created.
- If all inodes are used, new files cannot be created even if disk space is available.

---

# Quick Revision

- Inode = Index Node.
- Stores metadata.
- Does not store the filename.
- Every file has a unique inode number.
- Linux accesses files using inode numbers.

---

# Important Keywords

- Inode
- Index Node
- Metadata
- Inode Number
- Inode Table
- Data Block
- Directory
- File System

---

# Frequently Asked Questions

## What is an Inode?

An Inode is a data structure that stores metadata about a file.

---

## Does an Inode store the filename?

No.

The filename is stored inside the directory.

---

## What is Metadata?

Metadata is information about a file such as size, owner, permissions, and timestamps.

---

## Which command displays the inode number?

```bash
ls -i
```

---

## Which command displays detailed inode information?

```bash
stat
```

---

# MCQ Questions

### Q1.

The full form of Inode is:

A. Internal Node

B. Index Node

C. Information Node

D. Input Node

**Answer:** B

---

### Q2.

An Inode stores:

A. File Name

B. Metadata

C. Folder Name

D. Password

**Answer:** B

---

### Q3.

Which command displays the inode number?

A. pwd

B. ls -i

C. mkdir

D. rm

**Answer:** B

---

### Q4.

Which command displays complete metadata?

A. stat

B. ls

C. pwd

D. cat

**Answer:** A

---

### Q5.

The filename is stored inside:

A. Inode

B. Directory

C. Boot Block

D. Data Block

**Answer:** B

---

# Interview Questions

- What is an Inode?
- Why are Inodes important?
- What information is stored in an Inode?
- Why is the filename not stored inside an Inode?
- Explain the working of an Inode.

---

# Viva Questions

1. What is an Inode?
2. What is Metadata?
3. What is an Inode Number?
4. Which command displays inode information?
5. Why does Linux use Inodes?

---

# 2 Marks Questions

1. Define Inode.
2. What is Metadata?
3. What is an Inode Number?
4. Define Inode Table.
5. Write the syntax of the `stat` command.

---

# 5 Marks Questions

1. Explain the Inode structure in UNIX.
2. Explain Metadata with examples.
3. Explain the working of an Inode.

---

# Long Answer Questions

1. Explain the concept of Inodes in UNIX/Linux with a suitable diagram.
2. Explain the working of an Inode with commands and examples.

---

# Command Cheat Sheet

| Command | Purpose |
|----------|---------|
| `ls -i` | Display Inode Number |
| `ls -il` | Display Detailed List with Inodes |
| `stat filename` | Display Metadata |
| `stat --format=%i filename` | Display Only Inode Number |
| `df -i` | Display Filesystem Inodes |

---

# Previous Year Exam Focus

⭐⭐⭐⭐⭐ Very Important

- Definition of Inode
- Metadata
- Inode Number
- Inode Table
- Working of Inode
- Commands (`ls -i`, `stat`, `df -i`)

---

# Summary

- An Inode is a data structure used by UNIX/Linux to store metadata about a file.
- Every file has a unique inode number.
- The filename is stored in the directory, not in the inode.
- Linux accesses files using inode numbers instead of filenames.
- Commands like `ls -i`, `stat`, and `df -i` help inspect inode information.

---

# Related Topics

⬅️ Previous Topic

**09-Relative-Path.md**

➡️ Next Topics

- **11-Hard-Link.md**
- **12-Soft-Link.md**
- **13-Hard-Link-vs-Soft-Link.md**