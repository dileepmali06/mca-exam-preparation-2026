# 3.2.5 Copying Files, Moving Files, Renaming Files and Deleting Files (`cp`, `mv`, `rm`)

> **Module:** Module 3 – Unix/Linux Commands
>
> **Topic:** Copying Files, Moving Files, Renaming Files and Deleting Files (`cp`, `mv`, `rm`)
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

- Copy files and directories using the `cp` command.
- Move files and directories using the `mv` command.
- Rename files and directories.
- Delete files and directories using the `rm` command.
- Understand recursive and force deletion.
- Perform practical file management tasks in Ubuntu Linux.

---

# Introduction

Linux provides powerful commands for file management.

The three most commonly used commands are:

- `cp` – Copy files and directories.
- `mv` – Move or rename files and directories.
- `rm` – Remove files and directories.

These commands are essential for developers, Linux administrators, and DevOps engineers.

---

# The `cp` Command

## Definition

The **`cp` (Copy)** command is used to copy files or directories from one location to another.

The original file remains unchanged.

---

# Syntax

```bash
cp source destination
```

---

# Example 1 – Copy a File

```bash
cp notes.txt backup.txt
```

Result

```text
notes.txt

backup.txt
```

Both files now exist.

---

# Example 2 – Copy a File to Another Directory

```bash
cp notes.txt Documents/
```

The file is copied to the **Documents** directory.

---

# Example 3 – Copy Multiple Files

```bash
cp file1.txt file2.txt Documents/
```

Both files are copied to the destination directory.

---

# Copy an Entire Directory

Use the `-r` (recursive) option.

```bash
cp -r Projects Backup
```

This copies the complete **Projects** directory into **Backup**.

---

# Features of `cp`

- Copies files.
- Copies directories.
- Supports multiple files.
- Keeps the original file unchanged.

---

# The `mv` Command

## Definition

The **`mv` (Move)** command is used to move or rename files and directories.

---

# Syntax

```bash
mv source destination
```

---

# Example 1 – Move a File

```bash
mv notes.txt Documents/
```

The file is moved to the **Documents** directory.

---

# Example 2 – Rename a File

```bash
mv notes.txt linux_notes.txt
```

The file name changes while the content remains the same.

---

# Example 3 – Rename a Directory

```bash
mv Project Projects
```

The directory name changes from **Project** to **Projects**.

---

# Features of `mv`

- Moves files.
- Moves directories.
- Renames files.
- Renames directories.

---

# The `rm` Command

## Definition

The **`rm` (Remove)** command is used to permanently delete files and directories.

> **Warning:** Files deleted using `rm` are generally not moved to the Recycle Bin.

---

# Syntax

```bash
rm filename
```

---

# Example 1 – Delete a File

```bash
rm notes.txt
```

The file is permanently removed.

---

# Example 2 – Delete Multiple Files

```bash
rm file1.txt file2.txt file3.txt
```

All specified files are deleted.

---

# Delete a Directory

Use the recursive option.

```bash
rm -r Projects
```

The directory and all its contents are removed.

---

# Force Delete

```bash
rm -f notes.txt
```

Deletes the file without asking for confirmation.

---

# Recursive Force Delete

```bash
rm -rf Projects
```

Deletes the directory and all its contents without confirmation.

> **Warning:** Use `rm -rf` carefully because deleted data cannot normally be recovered.

---

# Difference Between `cp`, `mv`, and `rm`

| Command | Purpose |
|----------|---------|
| `cp` | Copy files and directories |
| `mv` | Move or rename files and directories |
| `rm` | Delete files and directories |

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

Create Files.

```bash
touch notes.txt
```

```bash
touch data.txt
```

---

## Step 3

Copy a File.

```bash
cp notes.txt backup.txt
```

---

## Step 4

Verify Files.

```bash
ls
```

---

## Step 5

Rename a File.

```bash
mv backup.txt backup_notes.txt
```

---

## Step 6

Move the File.

```bash
mv backup_notes.txt Documents/
```

---

## Step 7

Create a Directory.

```bash
mkdir Linux
```

---

## Step 8

Copy the Directory.

```bash
cp -r Linux LinuxBackup
```

---

## Step 9

Delete a File.

```bash
rm notes.txt
```

---

## Step 10

Delete a Directory.

```bash
rm -r LinuxBackup
```

---

# Expected Output

```text
$ touch notes.txt
```

---

```text
$ cp notes.txt backup.txt
```

---

```text
$ ls

backup.txt

notes.txt
```

---

```text
$ mv backup.txt backup_notes.txt
```

---

```text
$ mv backup_notes.txt Documents/
```

---

```text
$ rm notes.txt
```

---

```text
$ rm -r LinuxBackup
```

---

# Real World Applications

## Software Developers

- Backup source code.
- Rename project files.
- Organize project folders.

---

## Backend Developers

- Move configuration files.
- Copy environment files.
- Remove temporary files.

---

## DevOps Engineers

- Backup deployment folders.
- Move release packages.
- Delete old log files.

---

## Linux System Administrators

- Organize user data.
- Backup important directories.
- Remove unwanted files.

---

# Common Beginner Mistakes

### Mistake 1

Trying to copy a directory without `-r`.

**Correct:**

```bash
cp -r Folder Backup
```

---

### Mistake 2

Thinking `mv` only moves files.

**Correct:** It also renames files and directories.

---

### Mistake 3

Using `rm -rf` without verifying the path.

**Correct:** Always check the directory using:

```bash
pwd
```

before running destructive commands.

---

# Advantages

## `cp`

- Keeps the original file safe.
- Supports copying multiple files.
- Can copy complete directories.

---

## `mv`

- Moves files quickly.
- Renames files and directories.
- Does not duplicate data.

---

## `rm`

- Removes unwanted files.
- Deletes directories recursively.
- Supports force deletion.

---

# Quick Revision

- `cp` copies files.
- `cp -r` copies directories.
- `mv` moves files.
- `mv` also renames files and directories.
- `rm` deletes files.
- `rm -r` deletes directories.
- `rm -f` force deletes files.
- `rm -rf` recursively force deletes directories.

---

# Important Keywords

- `cp`
- `mv`
- `rm`
- Recursive Copy
- Recursive Delete
- Force Delete
- Rename
- File Management

---

# Frequently Asked Questions

## What is the `cp` command?

It copies files and directories.

---

## What is the `mv` command?

It moves or renames files and directories.

---

## What is the `rm` command?

It permanently deletes files and directories.

---

## Which option copies directories?

```bash
cp -r
```

---

## Which option deletes directories recursively?

```bash
rm -r
```

---

# MCQ Questions

### Q1.

Which command copies a file?

A. `mv`

B. `cp`

C. `rm`

D. `ls`

**Answer:** B

---

### Q2.

Which command renames a file?

A. `cp`

B. `mv`

C. `rm`

D. `pwd`

**Answer:** B

---

### Q3.

Which option copies directories?

A. `-f`

B. `-p`

C. `-r`

D. `-a`

**Answer:** C

---

### Q4.

Which command deletes a directory recursively?

A. `rm`

B. `rm -r`

C. `cp -r`

D. `mv`

**Answer:** B

---

### Q5.

Which command force deletes a file?

A. `rm -f`

B. `cp -f`

C. `mv -f`

D. `ls -f`

**Answer:** A

---

# Interview Questions

- What is the purpose of the `cp` command?
- Explain the `mv` command with examples.
- What is the difference between moving and copying a file?
- Explain `rm -r` and `rm -rf`.
- Which command is used to rename a file?

---

# Viva Questions

1. What is the `cp` command?
2. What is the `mv` command?
3. What is the `rm` command?
4. What does `cp -r` do?
5. What does `rm -rf` do?

---

# 2 Marks Questions

1. Define the `cp` command.
2. Define the `mv` command.
3. Define the `rm` command.
4. What is the purpose of `cp -r`?

---

# 5 Marks Questions

1. Explain the `cp` command with examples.
2. Explain the `mv` command with examples.
3. Explain the `rm` command with examples.

---

# Long Answer Questions

1. Explain file management using the `cp`, `mv`, and `rm` commands.
2. Explain copying, moving, renaming, and deleting files in Linux with suitable examples.
3. Compare the `cp`, `mv`, and `rm` commands.

---

# Command Cheat Sheet

| Command | Purpose |
|----------|---------|
| `cp source destination` | Copy a file |
| `cp -r source destination` | Copy a directory |
| `mv source destination` | Move a file or directory |
| `mv old new` | Rename a file or directory |
| `rm file` | Delete a file |
| `rm -r directory` | Delete a directory |
| `rm -f file` | Force delete a file |
| `rm -rf directory` | Force delete a directory |

---

# Previous Year Exam Focus

⭐⭐⭐⭐⭐ Very Important

- `cp` Command
- `mv` Command
- `rm` Command
- `cp -r`
- `rm -r`
- `rm -rf`
- File Renaming
- Directory Copying

---

# Summary

- The `cp` command is used to copy files and directories while keeping the original unchanged.
- The `mv` command is used to move or rename files and directories.
- The `rm` command permanently removes files and directories.
- The `-r` option enables recursive operations on directories, while the `-f` option forces deletion without confirmation.
- These commands are essential for Linux file management and are widely used in development, system administration, and DevOps.

---

# Related Topics

⬅️ Previous Topic

**06-LS-Command.md**

➡️ Next Topic

**08-File-Viewing-Commands.md**