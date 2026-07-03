# Hard Link vs Soft Link (Symbolic Link)

> **Module:** Module 1 - UNIX File System
>
> **Topic:** Hard Link vs Soft Link
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

- Differentiate between Hard Link and Soft Link.
- Understand their working.
- Understand the role of Inodes.
- Perform practical demonstrations.
- Answer comparison questions in university exams.

---

# Introduction

Linux provides two different ways to create links between files:

1. Hard Link
2. Soft Link (Symbolic Link)

Although both are used to access the same file, their working principles are completely different.

Understanding the difference between them is one of the most important topics in UNIX/Linux Programming.

---

# What is a Hard Link?

A **Hard Link** is another filename that points directly to the **same inode** as the original file.

Both filenames are treated equally by Linux.

They share:

- Same Inode
- Same Data
- Same Metadata

---

# What is a Soft Link?

A **Soft Link (Symbolic Link)** is a special file that stores the **path of another file or directory**.

It behaves like a shortcut.

It has its own inode.

---

# Architecture Comparison

## Hard Link

```text
notes.txt
      │
      ▼
+----------------+
| Inode #530461  |
+----------------+
| Metadata       |
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

Both filenames point to the same inode.

---

## Soft Link

```text
shortcut.txt

↓

Own Inode

↓

Stores Path

↓

notes.txt

↓

Inode #530461

↓

Data
```

The Soft Link does not point directly to the inode.

It first stores the file path.

---

# Difference Between Hard Link and Soft Link

| Hard Link | Soft Link |
|------------|-----------|
| Shares the same inode | Has a different inode |
| Points directly to data | Points to file path |
| Created using `ln` | Created using `ln -s` |
| Original file can be deleted safely | Original file deletion creates a Broken Link |
| Cannot span different file systems | Can span different file systems |
| Cannot normally link directories | Can link directories |
| Faster | Slightly slower |
| Link Count increases | Link Count does not increase |

---

# Inode Comparison

## Hard Link

```text
notes.txt

↓

Inode #530461

↑

hardlink.txt
```

Same inode.

---

## Soft Link

```text
notes.txt

↓

530461

↑

Data

shortcut.txt

↓

530500

↓

Path
```

Different inode.

---

# Deleting the Original File

## Hard Link

Delete

```bash
rm notes.txt
```

Result

```text
hardlink.txt

↓

Still Works
```

The file remains available.

---

## Soft Link

Delete

```bash
rm notes.txt
```

Result

```text
shortcut.txt

↓

Broken Link
```

The shortcut can no longer access the file.

---

# Commands

## Hard Link

```bash
ln notes.txt hardlink.txt
```

---

## Soft Link

```bash
ln -s notes.txt shortcut.txt
```

---

# Practical Demonstration

Create a file.

```bash
touch notes.txt
```

Write data.

```bash
echo "Hello Linux" > notes.txt
```

Create Hard Link.

```bash
ln notes.txt hardlink.txt
```

Create Soft Link.

```bash
ln -s notes.txt shortcut.txt
```

Display inode numbers.

```bash
ls -li
```

Display links.

```bash
ls -l
```

Delete original file.

```bash
rm notes.txt
```

Try reading both files.

```bash
cat hardlink.txt

cat shortcut.txt
```

Observation:

- Hard Link works.
- Soft Link becomes Broken.

---

# Real World Applications

## Hard Link

- Backup files
- Shared data
- Efficient storage

---

## Soft Link

- Desktop shortcuts
- Configuration links
- Deployment folders
- Shared libraries

---

# Advantages

## Hard Link

- Saves storage.
- Same data.
- Faster access.
- Survives deletion of one filename.

---

## Soft Link

- Can link directories.
- Works across different file systems.
- Easy to manage.
- Very flexible.

---

# Limitations

## Hard Link

- Cannot link directories.
- Cannot cross file systems.

---

## Soft Link

- Broken if original file is deleted.
- Depends on the file path.

---

# Memory Trick

## Hard Link

Think:

> **Same House, Two Names**

Two names.

One house.

One inode.

---

## Soft Link

Think:

> **Google Chrome Desktop Shortcut**

Shortcut only.

Original software is somewhere else.

---

# Exam Tip

### If the question is:

**Differentiate between Hard Link and Soft Link.**

Always answer in **table format**.

Tables score higher marks than paragraph explanations.

---

# Quick Revision

## Hard Link

- Same Inode
- Same Data
- Same Metadata
- `ln`
- Link Count increases

---

## Soft Link

- Different Inode
- Stores Path
- `ln -s`
- Broken Link possible
- Can link directories

---

# Important Keywords

- Hard Link
- Soft Link
- Symbolic Link
- Inode
- Link Count
- Broken Link
- File System

---

# Frequently Asked Questions

## Q1. Which link shares the same inode?

Hard Link.

---

## Q2. Which link acts as a shortcut?

Soft Link.

---

## Q3. Which command creates a Hard Link?

```bash
ln
```

---

## Q4. Which command creates a Soft Link?

```bash
ln -s
```

---

## Q5. Which link becomes broken when the original file is deleted?

Soft Link.

---

# MCQ Questions

### Q1.

Hard Link shares:

- A. Different Inode
- B. Same Inode
- C. Different Path
- D. None

**Answer:** B

---

### Q2.

Soft Link stores:

- A. Data
- B. Metadata
- C. Path
- D. Permissions

**Answer:** C

---

### Q3.

Which command creates a Soft Link?

- A. cp
- B. mv
- C. ln
- D. ln -s

**Answer:** D

---

### Q4.

Which link survives deletion of the original file?

- A. Hard Link
- B. Soft Link

**Answer:** A

---

### Q5.

Which link can cross file systems?

- A. Hard Link
- B. Soft Link

**Answer:** B

---

# Interview Questions

- Explain Hard Link and Soft Link.
- Why does Hard Link share the same inode?
- What is a Broken Link?
- Which link is faster and why?
- Can Hard Links be created across different file systems?

---

# Viva Questions

1. Define Hard Link.
2. Define Soft Link.
3. What is a Broken Link?
4. Which command creates a Hard Link?
5. Which command creates a Soft Link?
6. Which link shares the same inode?

---

# 2 Marks Questions

1. Define Hard Link.
2. Define Soft Link.
3. What is a Broken Link?
4. Write the command to create a Hard Link.
5. Write the command to create a Soft Link.

---

# 5 Marks Questions

1. Differentiate between Hard Link and Soft Link.
2. Explain Hard Link with an example.
3. Explain Soft Link with an example.

---

# Long Answer Questions

1. Explain Hard Link and Soft Link with suitable diagrams.
2. Compare Hard Link and Soft Link with practical examples.

---

# Command Cheat Sheet

| Command | Purpose |
|----------|---------|
| `ln source target` | Create Hard Link |
| `ln -s source target` | Create Soft Link |
| `ls -li` | Display Inode Numbers |
| `ls -l` | Display Link Details |
| `rm filename` | Delete File |
| `cat filename` | Display File Contents |

---

# Previous Year Exam Focus

⭐⭐⭐⭐⭐ Very Important

- Hard Link vs Soft Link
- Same Inode Concept
- Broken Link
- Link Count
- ln Command
- ln -s Command

---

# Summary

- Hard Link points directly to the same inode as the original file.
- Soft Link stores the path of the original file.
- Hard Links survive deletion of one filename.
- Soft Links become Broken Links if the original file is deleted.
- Hard Links cannot cross file systems, whereas Soft Links can.
- `ln` creates a Hard Link and `ln -s` creates a Soft Link.

---

# Related Topics

⬅️ Previous Topics

- **10-Inode.md**
- **11-Hard-Link.md**
- **12-Soft-Link.md**

