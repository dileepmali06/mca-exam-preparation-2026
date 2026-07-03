# 3.2.2 Moving Around by Path (`cd`) and Creating New Directories (`mkdir`)

> **Module:** Module 3 – Unix/Linux Commands
>
> **Topic:** Moving Around by Path (`cd`) and Creating New Directories (`mkdir`)
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

- Understand directory navigation in Linux.
- Use the `cd` command to move between directories.
- Understand Absolute and Relative Paths.
- Understand special directory symbols (`.`, `..`, `~`, `/`, `-`).
- Create new directories using the `mkdir` command.
- Create nested directories using the `-p` option.
- Perform practical directory operations in Ubuntu Linux.

---

# Introduction

Linux organizes files and folders in a hierarchical directory structure.

To work efficiently with files and folders, users must know how to:

- Move from one directory to another.
- Create new directories.
- Navigate using different types of paths.

Linux provides two important commands for these tasks:

- `cd` (Change Directory)
- `mkdir` (Make Directory)

---

# The `cd` Command

## Definition

The **`cd` (Change Directory)** command is used to change the current working directory.

It allows users to move from one directory to another within the Linux file system.

---

# Syntax

```bash
cd directory_name
```

---

# Example 1 – Move to a Directory

Current Directory

```text
/home/dilip
```

Command

```bash
cd Documents
```

Current Directory becomes

```text
/home/dilip/Documents
```

Verify using:

```bash
pwd
```

Output

```text
/home/dilip/Documents
```

---

# Example 2 – Move to Home Directory

```bash
cd
```

or

```bash
cd ~
```

Output

```text
/home/dilip
```

---

# Example 3 – Move to Parent Directory

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

---

# Example 4 – Move to Root Directory

```bash
cd /
```

Output

```text
/
```

---

# Example 5 – Move to Previous Directory

```bash
cd -
```

Example

```text
/home/dilip

↓

cd Documents

↓

/home/dilip/Documents

↓

cd -

↓

/home/dilip
```

---

# Special Symbols Used with `cd`

| Symbol | Meaning |
|---------|---------|
| `.` | Current Directory |
| `..` | Parent Directory |
| `~` | Home Directory |
| `/` | Root Directory |
| `-` | Previous Directory |

---

# Absolute Path

An **Absolute Path** specifies the complete path from the Root Directory.

Example

```bash
cd /home/dilip/Documents
```

Advantages:

- Independent of the current location.
- Always points to the same directory.

---

# Relative Path

A **Relative Path** is interpreted with respect to the Current Working Directory.

Example

Current Directory

```text
/home/dilip
```

Command

```bash
cd Documents
```

Advantages:

- Shorter and easier to type.
- Useful when working within nearby directories.

---

# Difference Between Absolute and Relative Path

| Absolute Path | Relative Path |
|---------------|---------------|
| Starts from Root (`/`) | Starts from Current Directory |
| Complete path | Short path |
| Independent of current location | Depends on current location |
| Longer | Shorter |

---

# The `mkdir` Command

## Definition

The **`mkdir` (Make Directory)** command is used to create new directories in Linux.

---

# Syntax

```bash
mkdir directory_name
```

---

# Example 1 – Create a Single Directory

```bash
mkdir LinuxNotes
```

This creates a directory named **LinuxNotes**.

---

# Example 2 – Create Multiple Directories

```bash
mkdir HTML CSS JavaScript
```

This creates three directories:

```text
HTML

CSS

JavaScript
```

---

# Example 3 – Create Nested Directories

```bash
mkdir -p College/MCA/Sem3/Linux
```

Result

```text
College

└── MCA

     └── Sem3

          └── Linux
```

The `-p` option automatically creates missing parent directories.

---

# Without `-p`

Command

```bash
mkdir College/MCA/Linux
```

If the parent directory does not exist, Linux displays:

```text
mkdir: cannot create directory 'College/MCA/Linux': No such file or directory
```

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

Display the Current Working Directory.

```bash
pwd
```

---

## Step 3

Move to the Documents directory.

```bash
cd Documents
```

---

## Step 4

Verify the Current Directory.

```bash
pwd
```

---

## Step 5

Return to the Home Directory.

```bash
cd ~
```

---

## Step 6

Move to the Parent Directory.

```bash
cd ..
```

---

## Step 7

Create a New Directory.

```bash
mkdir LinuxNotes
```

---

## Step 8

Create Multiple Directories.

```bash
mkdir HTML CSS JavaScript
```

---

## Step 9

Create Nested Directories.

```bash
mkdir -p Projects/MERN/Backend
```

---

## Step 10

Display the Created Directories.

```bash
ls
```

---

# Expected Output

```text
$ pwd

/home/dilip
```

---

```text
$ cd Documents
```

---

```text
$ pwd

/home/dilip/Documents
```

---

```text
$ mkdir LinuxNotes
```

---

```text
$ ls

Desktop

Documents

Downloads

LinuxNotes
```

---

# Real World Applications

## Software Developers

- Navigate project directories.
- Create folders for frontend and backend projects.
- Organize source code.

---

## Backend Developers

- Create API and configuration directories.
- Manage project structures.

---

## DevOps Engineers

- Create deployment folders.
- Organize application releases.
- Manage backup directories.

---

## Linux System Administrators

- Create user directories.
- Organize system folders.
- Maintain server directory structures.

---

# Common Beginner Mistakes

### Mistake 1

Trying to enter a directory that does not exist.

**Correct:**

Check available directories using:

```bash
ls
```

---

### Mistake 2

Confusing `.` and `..`.

**Correct:**

- `.` → Current Directory
- `..` → Parent Directory

---

### Mistake 3

Creating nested directories without using `-p`.

**Correct:**

```bash
mkdir -p Parent/Child
```

---

### Mistake 4

Using Relative Paths from the wrong directory.

**Correct:**

Use:

```bash
pwd
```

before navigating.

---

# Advantages

## `cd`

- Easy directory navigation.
- Supports Absolute and Relative Paths.
- Quick access to Home and Parent directories.

---

## `mkdir`

- Creates new directories easily.
- Supports multiple directory creation.
- Creates nested directory structures using `-p`.

---

# Quick Revision

- `cd` changes the current directory.
- `cd ~` moves to the Home Directory.
- `cd ..` moves to the Parent Directory.
- `cd /` moves to the Root Directory.
- `cd -` returns to the Previous Directory.
- `mkdir` creates new directories.
- `mkdir -p` creates nested directories.

---

# Important Keywords

- Change Directory
- Make Directory
- Absolute Path
- Relative Path
- Parent Directory
- Home Directory
- Root Directory
- Current Directory

---

# Frequently Asked Questions

## What is the `cd` command?

It is used to change the current working directory.

---

## What is the `mkdir` command?

It is used to create new directories.

---

## Which command moves to the Parent Directory?

```bash
cd ..
```

---

## Which command moves to the Home Directory?

```bash
cd ~
```

or

```bash
cd
```

---

## Which option creates nested directories?

```bash
mkdir -p
```

---

# MCQ Questions

### Q1.

Which command changes the current directory?

A. `pwd`

B. `cd`

C. `ls`

D. `mkdir`

**Answer:** B

---

### Q2.

Which command creates a new directory?

A. `touch`

B. `mkdir`

C. `cp`

D. `mv`

**Answer:** B

---

### Q3.

Which command moves to the Parent Directory?

A. `cd .`

B. `cd ..`

C. `cd ~`

D. `cd /`

**Answer:** B

---

### Q4.

Which symbol represents the Home Directory?

A. `.`

B. `..`

C. `~`

D. `/`

**Answer:** C

---

### Q5.

Which option creates nested directories?

A. `mkdir -r`

B. `mkdir -n`

C. `mkdir -p`

D. `mkdir -a`

**Answer:** C

---

# Interview Questions

- What is the purpose of the `cd` command?
- What is the purpose of the `mkdir` command?
- Explain Absolute and Relative Paths.
- What is the difference between `cd ~` and `cd ..`?
- Explain the `mkdir -p` option.

---

# Viva Questions

1. What is the `cd` command?
2. What is the `mkdir` command?
3. What does `cd ..` do?
4. What does `cd ~` do?
5. What is the purpose of `mkdir -p`?

---

# 2 Marks Questions

1. Define the `cd` command.
2. Define the `mkdir` command.
3. What is an Absolute Path?
4. What is a Relative Path?

---

# 5 Marks Questions

1. Explain the `cd` command with examples.
2. Explain the `mkdir` command with examples.
3. Differentiate between Absolute and Relative Paths.

---

# Long Answer Questions

1. Explain directory navigation using the `cd` command.
2. Explain directory creation using the `mkdir` command.
3. Explain Absolute Path and Relative Path with suitable examples.

---

# Command Cheat Sheet

| Command | Purpose |
|----------|---------|
| `cd directory_name` | Change directory |
| `cd ~` | Move to Home Directory |
| `cd ..` | Move to Parent Directory |
| `cd /` | Move to Root Directory |
| `cd -` | Move to Previous Directory |
| `mkdir folder_name` | Create a new directory |
| `mkdir dir1 dir2` | Create multiple directories |
| `mkdir -p path` | Create nested directories |

---

# Previous Year Exam Focus

⭐⭐⭐⭐⭐ Very Important

- `cd` Command
- `mkdir` Command
- `cd ..`
- `cd ~`
- `cd /`
- `mkdir -p`
- Absolute Path
- Relative Path

---

# Summary

- The `cd` command is used to change the current working directory in Linux.
- It supports navigation using Absolute Paths, Relative Paths, Home Directory (`~`), Parent Directory (`..`), Root Directory (`/`), and Previous Directory (`-`).
- The `mkdir` command is used to create new directories.
- Multiple directories can be created in a single command, and nested directories can be created using the `-p` option.
- These commands form the foundation of Linux file system navigation and directory management.

---

# Related Topics

⬅️ Previous Topic

**03-Current-Working-Directory-and-Home-Directory.md**

➡️ Next Topic

**05-Touch-and-CAT-Commands.md**