# 1.2.3 Relative Path

> **Module:** Module 1 - UNIX File System
>
> **Topic:** 1.2.3 Relative Path
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

- Understand what a Relative Path is.
- Explain why Relative Paths are used.
- Understand the role of the Current Working Directory (CWD).
- Use `.` (Current Directory) and `..` (Parent Directory).
- Navigate directories using Relative Paths.
- Differentiate between Absolute Path and Relative Path.

---

# Introduction

In UNIX/Linux, every file and directory can be accessed using a **Path**.

A Path specifies the location of a file or directory.

There are two types of paths:

1. Absolute Path
2. Relative Path

Unlike an Absolute Path, a **Relative Path** starts from the **Current Working Directory (CWD)** instead of the Root Directory.

---

# Why Do We Need a Relative Path?

Suppose you are inside your college library.

If someone asks you where the Computer Lab is, you don't need to tell the complete address of the college.

You simply say:

```text
Go straight

↓

Take the right turn

↓

Computer Lab
```

Since both of you are already inside the college, the complete address is unnecessary.

Similarly, in Linux, if you are already inside a directory, you do not always need to write the complete path.

This shorter path is called a **Relative Path**.

---

# Definition

A **Relative Path** is the path of a file or directory relative to the **Current Working Directory (CWD)**.

It does **not** start with the Root Directory (`/`).

Instead, it starts from the directory in which the user is currently working.

---

# Characteristics of Relative Path

- Starts from the Current Working Directory.
- Does not begin with `/`.
- Shorter than an Absolute Path.
- Depends on the Current Working Directory.
- Commonly used inside projects and shell scripts.

---

# Structure of a Relative Path

Suppose the Current Working Directory is:

```text
/home/dilip
```

Directory Structure

```text
/home

   └── dilip

         ├── Documents

         │      └── notes.txt

         ├── Downloads

         └── Projects
```

Relative Path to Documents

```text
Documents
```

Relative Path to notes.txt

```text
Documents/notes.txt
```

Absolute Path to notes.txt

```text
/home/dilip/Documents/notes.txt
```

---

# Current Working Directory (CWD)

The Current Working Directory is the directory in which the user is currently working.

Display the Current Working Directory:

```bash
pwd
```

Example Output

```text
/home/dilip
```

The Current Working Directory acts as the starting point for all Relative Paths.

---

# Special Symbols Used in Relative Paths

## 1. Current Directory (`.`)

The symbol `.` represents the Current Directory.

Example

```bash
cd .
```

This command keeps you in the same directory.

---

## 2. Parent Directory (`..`)

The symbol `..` represents the Parent Directory.

Example

Current Directory

```text
/home/dilip/Documents
```

Command

```bash
cd ..
```

Output

```text
/home/dilip
```

The command moves one level up.

---

## Moving Multiple Levels

Suppose the Current Directory is:

```text
/home/dilip/Documents/Linux
```

Command

```bash
cd ../..
```

Output

```text
/home/dilip
```

Explanation:

- First `..` → Documents
- Second `..` → dilip

---

# Practical (Ubuntu VirtualBox)

## Step 1

Open Terminal.

Shortcut

```text
Ctrl + Alt + T
```

---

## Step 2

Check Current Working Directory.

```bash
pwd
```

---

## Step 3

Create Directories.

```bash
mkdir -p Linux/Notes
```

---

## Step 4

Move to Linux Directory.

```bash
cd Linux
```

---

## Step 5

Move to Notes Directory.

```bash
cd Notes
```

---

## Step 6

Go One Level Up.

```bash
cd ..
```

---

## Step 7

Go One More Level Up.

```bash
cd ..
```

---

## Step 8

Verify the Current Directory.

```bash
pwd
```

---

# Absolute Path vs Relative Path

| Absolute Path | Relative Path |
|---------------|---------------|
| Starts with `/` | Does not start with `/` |
| Complete Path | Partial Path |
| Independent of CWD | Depends on CWD |
| Longer | Shorter |
| Suitable for Scripts | Suitable for Local Navigation |

---

# Advantages

- Easy to write.
- Short and readable.
- Convenient for project directories.
- Faster navigation.

---

# Limitations

- Depends on the Current Working Directory.
- Commands may fail if executed from another directory.
- Less suitable for automation scripts.

---

# Real World Applications

## Software Developers

Access nearby project files.

Example

```text
src/components
```

---

## Backend Developers

Navigate inside project directories.

---

## DevOps Engineers

Relative Paths are frequently used in deployment scripts executed inside project folders.

---

## Cloud Engineers

Applications often use Relative Paths for internal resources.

---

# Common Beginner Mistakes

### Mistake 1

Starting a Relative Path with `/`.

Wrong

```text
/home/dilip/Documents
```

Correct

```text
Documents
```

---

### Mistake 2

Confusing `.` and `..`.

Correct

- `.` → Current Directory
- `..` → Parent Directory

---

### Mistake 3

Using Relative Paths without checking the Current Working Directory.

Always verify using:

```bash
pwd
```

---

# Quick Revision

- Relative Path starts from the Current Working Directory.
- It never starts with `/`.
- `.` represents the Current Directory.
- `..` represents the Parent Directory.
- Relative Paths are shorter and easier to use.

---

# Important Keywords

- Relative Path
- Current Working Directory (CWD)
- Parent Directory
- Current Directory
- Dot (`.`)
- Double Dot (`..`)

---

# Frequently Asked Questions

## Q1. What is a Relative Path?

A Relative Path is the path of a file or directory relative to the Current Working Directory.

---

## Q2. Does a Relative Path start with `/`?

No.

---

## Q3. What does `.` represent?

The Current Directory.

---

## Q4. What does `..` represent?

The Parent Directory.

---

## Q5. Which command displays the Current Working Directory?

```bash
pwd
```

---

# MCQ Questions

### Q1.

Relative Path depends on:

- A. Root Directory
- B. Current Working Directory
- C. Kernel
- D. Shell

**Answer:** B

---

### Q2.

Which symbol represents the Current Directory?

- A. `..`
- B. `.`
- C. `/`
- D. `~`

**Answer:** B

---

### Q3.

Which symbol represents the Parent Directory?

- A. `.`
- B. `..`
- C. `/`
- D. `~`

**Answer:** B

---

### Q4.

Which command moves one level up?

- A. `cd .`
- B. `cd ..`
- C. `pwd`
- D. `ls`

**Answer:** B

---

### Q5.

Which of the following is a Relative Path?

- A. `/home/dilip/Documents`
- B. `/etc/passwd`
- C. `Documents/notes.txt`
- D. `/usr/bin`

**Answer:** C

---

# Interview Questions

- What is a Relative Path?
- What is the difference between Absolute and Relative Paths?
- What do `.` and `..` represent?
- Why do Relative Paths depend on the Current Working Directory?

---

# Viva Questions

1. Define Relative Path.
2. What is the Current Working Directory?
3. What is the purpose of `.`?
4. What is the purpose of `..`?
5. Differentiate between Absolute Path and Relative Path.

---

# Command Cheat Sheet

| Command | Purpose |
|----------|---------|
| `pwd` | Display Current Working Directory |
| `cd DirectoryName` | Move to a Subdirectory |
| `cd .` | Stay in the Current Directory |
| `cd ..` | Move to the Parent Directory |
| `cd ../..` | Move Two Levels Up |

---

# Previous Year Exam Focus

⭐⭐⭐⭐ Very Important

- Relative Path Definition
- Current Working Directory
- `.` and `..`
- Difference between Absolute and Relative Path
- Practical Commands

---

# Summary

- A Relative Path specifies the location of a file or directory relative to the Current Working Directory.
- It does not start with the Root Directory (`/`).
- The symbols `.` and `..` are used to represent the Current Directory and Parent Directory respectively.
- Relative Paths are shorter and more convenient for local navigation.
- They are widely used in software development, shell scripting, and Linux system administration.

---

# Related Topics

⬅️ Previous Topic

**1.2.2 Absolute Path**

➡️ Next Topic

**1.2.4 Inode**