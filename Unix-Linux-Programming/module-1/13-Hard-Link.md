# 1.2.4 Hard Link

> **Module:** Module 1 - UNIX File System
>
> **Topic:** Hard Link
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

- Understand what a Hard Link is.
- Explain why Hard Links are used.
- Understand the relationship between Hard Links and Inodes.
- Create Hard Links using Linux commands.
- Explain Link Count.
- Understand what happens when the original file is deleted.
- Differentiate Hard Links from normal file copies.

---

# Introduction

In Linux, multiple filenames can point to the same file.

Instead of creating another copy of the data, Linux allows multiple directory entries to point to the same inode.

This concept is called a **Hard Link**.

Hard Links save disk space because they do not duplicate file data.

---

# Why Do We Need Hard Links?

Imagine a book kept inside a library.

The same book is listed in two different catalogs.

```text
Catalog A

↓

Linux Programming

↓

Book No. 101

Catalog B

↓

Operating Systems

↓

Book No. 101
```

Although there are two catalog entries, there is only **one physical book**.

Hard Links work in the same way.

Multiple filenames refer to the same file.

---

# Definition

A **Hard Link** is another directory entry that points to the **same inode** as the original file.

Both the original file and the Hard Link share:

- Same Inode Number
- Same Metadata
- Same Data Blocks

Linux treats both names as equal.

There is no concept of an "original" file internally.

---

# Hard Link Architecture

```text
notes.txt
      │
      │
      ▼
+----------------+
| Inode #530461  |
+----------------+
| Permissions    |
| Owner          |
| Size           |
| Time Stamps    |
| Data Block Ptr |
+----------------+
        │
        ▼
+----------------+
| Hello Linux    |
+----------------+
        ▲
        │
hardlink.txt
```

Both filenames point to the **same inode**.

---

# Characteristics of Hard Links

- Share the same inode.
- Share the same data blocks.
- Share the same metadata.
- Save disk space.
- Increase the link count.
- Cannot normally be created for directories.
- Cannot span different file systems.

---

# Creating a Hard Link

## Syntax

```bash
ln source_file hardlink_name
```

---

## Example

Create a file.

```bash
touch notes.txt
```

Add data.

```bash
echo "Hello Linux" > notes.txt
```

Create Hard Link.

```bash
ln notes.txt hardlink.txt
```

---

# Verify Inode Numbers

Run:

```bash
ls -li
```

Example Output

```text
530461 notes.txt

530461 hardlink.txt
```

Notice that both files have the **same inode number**.

---

# Understanding Link Count

Run:

```bash
ls -l
```

Example

```text
-rw-r--r-- 2 dilip dilip 12 notes.txt

-rw-r--r-- 2 dilip dilip 12 hardlink.txt
```

The number **2** represents the **Link Count**.

It means there are two filenames pointing to the same inode.

---

# Working of a Hard Link

```text
Directory

↓

notes.txt

↓

Inode #530461

↓

Data Block

↓

Hello Linux

↑

hardlink.txt
```

Both filenames access the same data.

---

# Editing Through Hard Link

Suppose you modify:

```bash
nano hardlink.txt
```

Add:

```text
Linux is Powerful
```

Now display:

```bash
cat notes.txt
```

Output

```text
Hello Linux

Linux is Powerful
```

Since both filenames refer to the same inode, changes appear through both names.

---

# Deleting the Original File

Delete:

```bash
rm notes.txt
```

Now list files.

```bash
ls
```

Output

```text
hardlink.txt
```

The data still exists because the inode still has one link.

Display the file.

```bash
cat hardlink.txt
```

Output

```text
Hello Linux
```

The data is still available.

---

# When is the Data Deleted?

Linux removes the actual data only when:

- Link Count becomes zero.

Example

```bash
rm hardlink.txt
```

Now:

- Link Count = 0
- Inode is released.
- Data Blocks are freed.

---

# Advantages

- Saves storage space.
- Faster than copying files.
- Same data accessible through multiple names.
- Reliable backup within the same file system.

---

# Limitations

- Cannot link across different file systems.
- Cannot normally create hard links for directories.
- Confusing for beginners if multiple filenames point to the same data.

---

# Practical (Ubuntu VirtualBox)

Create a file.

```bash
touch notes.txt
```

Write data.

```bash
echo "Hello Linux" > notes.txt
```

Check inode.

```bash
ls -li
```

Create Hard Link.

```bash
ln notes.txt hardlink.txt
```

Check inode again.

```bash
ls -li
```

Display Link Count.

```bash
ls -l
```

Delete original.

```bash
rm notes.txt
```

Read Hard Link.

```bash
cat hardlink.txt
```

---

# Real World Applications

## Software Developers

Maintain multiple filenames for the same file.

---

## Linux Administrators

Manage important system files efficiently.

---

## DevOps Engineers

Share configuration files without duplicating data.

---

## Cloud Engineers

Use Hard Links to reduce storage usage on Linux servers.

---

# Common Beginner Mistakes

### Mistake 1

Thinking Hard Link is a copy.

Correct:

A Hard Link is **not** a copy.

---

### Mistake 2

Thinking deleting the original file deletes the data.

Correct:

Data remains until the last Hard Link is removed.

---

### Mistake 3

Thinking Hard Links have different inode numbers.

Correct:

All Hard Links share the same inode.

---

# Quick Revision

- Hard Link shares the same inode.
- Same inode means same data.
- Created using `ln`.
- Increases Link Count.
- Original file deletion does not remove data immediately.
- Data is deleted only when Link Count becomes zero.

---

# Important Keywords

- Hard Link
- Link Count
- Inode
- Directory Entry
- Data Block

---

# Frequently Asked Questions

## What is a Hard Link?

A Hard Link is another filename pointing to the same inode.

---

## Do Hard Links have different inode numbers?

No.

They share the same inode.

---

## Which command creates a Hard Link?

```bash
ln
```

---

## What happens if the original file is deleted?

The Hard Link continues to work.

---

# MCQ Questions

### Q1.

Hard Link shares:

A. Different Data

B. Different Inode

C. Same Inode

D. Same Directory

**Answer:** C

---

### Q2.

Which command creates a Hard Link?

A. cp

B. mv

C. ln

D. mkdir

**Answer:** C

---

### Q3.

Deleting the original file:

A. Deletes the Hard Link

B. Deletes the data immediately

C. Does not affect the Hard Link

D. Deletes the inode instantly

**Answer:** C

---

### Q4.

Hard Links can be created across different file systems.

A. True

B. False

**Answer:** B

---

### Q5.

Hard Links increase:

A. File Size

B. Link Count

C. Disk Size

D. Memory

**Answer:** B

---

# Interview Questions

- What is a Hard Link?
- Why does Linux use Hard Links?
- Explain Link Count.
- What happens when the original file is deleted?
- Can Hard Links be created across different file systems?

---

# Viva Questions

1. Define Hard Link.
2. Which command creates a Hard Link?
3. What is Link Count?
4. Why do Hard Links share the same inode?
5. Can Hard Links be created for directories?

---

# 2 Marks Questions

1. Define Hard Link.
2. What is Link Count?
3. Which command creates a Hard Link?
4. What happens when a Hard Link is deleted?

---

# 5 Marks Questions

1. Explain Hard Link with a suitable example.
2. Explain the working of Hard Links.

---

# Long Answer Questions

1. Explain Hard Links in UNIX/Linux with diagram and practical example.
2. Explain the relationship between Hard Links and Inodes.

---

# Command Cheat Sheet

| Command | Purpose |
|----------|---------|
| `ln source target` | Create Hard Link |
| `ls -li` | Display Inode Numbers |
| `ls -l` | Display Link Count |
| `cat filename` | Read File |
| `rm filename` | Delete File |

---

# Previous Year Exam Focus

⭐⭐⭐⭐⭐ Very Important

- Definition of Hard Link
- Working of Hard Link
- Link Count
- Same Inode Concept
- Deleting Original File
- Practical Commands

---

# Summary

- A Hard Link is another filename pointing to the same inode.
- Both filenames share the same data and metadata.
- Hard Links are created using the `ln` command.
- Deleting one filename does not delete the file data.
- The file is permanently deleted only when the last Hard Link is removed.

---

# Related Topics

⬅️ Previous Topic

**10-Inode.md**

➡️ Next Topic

**12-Soft-Link.md**