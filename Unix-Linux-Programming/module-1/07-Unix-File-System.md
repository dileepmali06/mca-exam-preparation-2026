# 1.2.1 UNIX File System (Part 1)

> **Module:** Module 1 - Introduction
>
> **Topic:** 1.2.1 UNIX File System
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

- Understand what a File System is.
- Explain why a File System is required.
- Differentiate between File and Directory.
- Understand the UNIX Hierarchical File System.
- Explain Root Directory.
- Understand Parent and Child Directories.
- Understand Current Working Directory.
- Navigate through the UNIX File System using commands.

---

# Introduction

Every operating system stores thousands or even millions of files.

These files include:

- Documents
- Images
- Videos
- Programs
- Operating System Files
- Configuration Files

If all these files were stored randomly, it would become almost impossible to locate and manage them.

To solve this problem, UNIX uses a **File System**.

A File System organizes files and directories in a structured way, making storage, searching, and retrieval fast and efficient.

---

# Why Do We Need a File System?

Imagine a library containing 50,000 books.

If the books are placed randomly, finding one specific book will take hours.

Therefore, books are arranged using:

- Rooms
- Shelves
- Book Numbers

Similarly, a computer also requires a proper system to organize files.

The File System performs this task.

---

# What is a File System?

## Definition

A **File System** is a method used by the operating system to organize, store, manage, and retrieve files and directories on a storage device.

It keeps track of:

- File Names
- File Locations
- File Size
- Permissions
- Owner
- File Type

Without a File System, an operating system cannot locate or access stored data.

---

# Everything is a File

One of the most famous UNIX philosophies is:

> **Everything is a File**

Unlike many operating systems, UNIX treats almost everything as a file.

Examples include:

- Text Files
- Directories
- Hard Disks
- USB Drives
- Printers
- Keyboard
- Mouse
- Network Devices

This design makes UNIX simple, flexible, and powerful.

---

# What is a File?

## Definition

A **File** is a collection of related information stored on secondary storage.

A file stores actual data.

Examples:

```text
notes.txt

resume.pdf

photo.jpg

video.mp4

program.c

index.html
```

Each file has:

- Name
- Size
- Owner
- Permissions
- Creation Time
- Modification Time

---

# What is a Directory?

## Definition

A **Directory** is a special type of file that stores references to other files and directories.

A directory helps organize files into logical groups.

Windows calls it a **Folder**.

Linux calls it a **Directory**.

---

# File vs Directory

| File | Directory |
|------|-----------|
| Stores Data | Stores Files and Directories |
| Has Content | Organizes Content |
| Cannot Contain Other Files | Can Contain Multiple Files |
| Example: notes.txt | Example: Documents |

---

# Hierarchical Tree Structure

UNIX organizes files in a **Tree Structure**.

```text
                /

         (Root Directory)

      /      |      |      \

   home     etc    usr     var

     |

   dilip

     |

 Documents

     |

 Linux
```

Every directory can contain:

- Files
- Subdirectories

This makes navigation simple and organized.

---

# Root Directory

The Root Directory is represented by:

```text
/
```

It is the top-most directory of the UNIX File System.

Every file and directory exists under the Root Directory.

Example:

```text
/

├── bin

├── boot

├── dev

├── etc

├── home

├── usr

├── var
```

Unlike Windows, UNIX has only one Root Directory.

---

# Parent and Child Directory

Example

```text
/home

   |

dilip

   |

Documents

   |

Linux
```

Here,

- Parent of **dilip** is **home**
- Parent of **Documents** is **dilip**
- Parent of **Linux** is **Documents**

Each directory can have:

- One Parent
- Multiple Child Directories

---

# Current Working Directory (CWD)

Whenever a Terminal is opened, it always starts inside a directory.

This directory is called the **Current Working Directory**.

To display the Current Working Directory:

```bash
pwd
```

Example Output

```text
/home/dilip
```

---

# File System Navigation

Move to Root Directory

```bash
cd /
```

Display Current Directory

```bash
pwd
```

List Files

```bash
ls
```

Move to Home Directory

```bash
cd /home
```

---

# Practical (Ubuntu VirtualBox)

Open Terminal

```bash
Ctrl + Alt + T
```

Display Current Directory

```bash
pwd
```

Move to Root Directory

```bash
cd /
```

Display Current Directory Again

```bash
pwd
```

List Root Directories

```bash
ls
```

Move Back to Home

```bash
cd /home
```

---

# Expected Output

```text
/

bin

boot

dev

etc

home

usr

var
```

---

# Common Beginner Mistakes

### Mistake 1

Thinking Folder and Directory are different.

Correct:

Windows → Folder

Linux → Directory

---

### Mistake 2

Confusing Root Directory with Root User.

Correct:

Root Directory

```text
/
```

Root User

Administrator Account

---

### Mistake 3

Forgetting Current Working Directory.

Always check using:

```bash
pwd
```

---

# Real World Applications

## Software Developers

Organize projects into directories.

Example

```text
Project

├── src

├── controllers

├── routes

├── models

└── config
```

---

## Backend Developers

Store APIs, database models, and configuration files in separate directories.

---

## DevOps Engineers

Daily work with directories like:

```text
/etc

/var

/usr

/home
```

---

## Cloud Engineers

Cloud servers on AWS, Azure, and Google Cloud use the UNIX File System.

---

# Quick Revision

- File System organizes files.
- UNIX follows a Hierarchical Tree Structure.
- Everything in UNIX is treated as a File.
- Root Directory is represented by `/`.
- Directory organizes files.
- `pwd` displays the Current Working Directory.
- `cd` changes the directory.
- `ls` lists files and directories.

---

# Important Keywords

- File System
- Root Directory
- Directory
- File
- Hierarchical Structure
- Parent Directory
- Child Directory
- Current Working Directory (CWD)

---

# Frequently Asked Questions

## Q1. What is a File System?

A File System is a method used to organize and manage files and directories.

---

## Q2. What is the Root Directory?

The Root Directory is the top-most directory represented by `/`.

---

## Q3. What is the Current Working Directory?

The directory in which the user is currently working.

---

## Q4. Which command displays the Current Working Directory?

```bash
pwd
```

---

# MCQ Questions

### Q1.

UNIX File System follows:

- A. Linear Structure
- B. Circular Structure
- C. Hierarchical Tree Structure
- D. Random Structure

**Answer:** C

---

### Q2.

The Root Directory is represented by:

- A. C:\
- B. \
- C. /
- D. Root

**Answer:** C

---

### Q3.

Which command displays the Current Working Directory?

- A. ls
- B. pwd
- C. mkdir
- D. cp

**Answer:** B

---

### Q4.

A Directory stores:

- A. CPU
- B. RAM
- C. Files and Directories
- D. Programs Only

**Answer:** C

---

# 2 Marks Questions

1. Define File System.
2. Define Directory.
3. What is Root Directory?
4. What is Current Working Directory?
5. What is Hierarchical File Structure?

---

# 5 Marks Questions

1. Explain UNIX File System.
2. Explain Root Directory.
3. Explain Hierarchical Tree Structure.

---

# Long Answer Questions

1. Explain UNIX File System with suitable diagram.
2. Explain File System hierarchy with examples.

---

# Viva Questions

- What is a File System?
- Why is Root Directory important?
- What is the difference between File and Directory?
- Which command displays the Current Working Directory?

---

# Command Cheat Sheet

| Command | Purpose |
|----------|---------|
| `pwd` | Display Current Working Directory |
| `ls` | List Files and Directories |
| `cd` | Change Directory |
| `cd /` | Move to Root Directory |
| `cd /home` | Move to Home Directory |

---

# Previous Year Exam Focus

⭐ Very Important

- UNIX File System
- Root Directory
- Hierarchical Tree Structure
- Current Working Directory

---

## Continue Reading

➡️ **Part 2 – Types of Files**