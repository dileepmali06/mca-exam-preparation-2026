# 1.2.4 Soft Link (Symbolic Link)

> **Module:** Module 1 - UNIX File System
>
> **Topic:** Soft Link (Symbolic Link)
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

- Understand what a Soft Link is.
- Explain why Soft Links are used.
- Differentiate between Soft Link and Hard Link.
- Create Symbolic Links using Linux commands.
- Understand Broken Links.
- Perform practical demonstrations in Ubuntu Linux.

---

# Introduction

In UNIX/Linux, a **Soft Link (Symbolic Link)** is a special type of file that acts as a shortcut to another file or directory.

Unlike a Hard Link, a Soft Link does not share the same inode.

Instead, it stores the **path of the original file**.

If the original file is moved or deleted, the Soft Link becomes invalid.

---

# Why Do We Need Soft Links?

Suppose you have installed Google Chrome.

On your desktop, you see a Chrome icon.

```text
Chrome Icon

↓

Double Click

↓

Google Chrome Opens
```

The desktop icon is not the actual application.

It is only a **Shortcut**.

Similarly,

A Soft Link is simply a shortcut to another file.

---

# Definition

A **Soft Link (Symbolic Link)** is a special file that stores the **path** of another file or directory.

It has its own inode number and redirects the operating system to the original file whenever it is accessed.

---

# Characteristics of Soft Link

- Has its own inode number.
- Stores the path of another file.
- Works like a shortcut.
- Can point to files as well as directories.
- Can be created across different file systems.
- Created using the `ln -s` command.

---

# Architecture of a Soft Link

```text
shortcut.txt

↓

Inode #530500

↓

Stores Path

↓

notes.txt

↓

Inode #530461

↓

Data Block

↓

Hello Linux
```

Notice:

- `shortcut.txt` has its own inode.
- It stores only the location of `notes.txt`.

---

# Creating a Soft Link

## Syntax

```bash
ln -s source_file shortcut_name
```

---

## Example

Create a file.

```bash
touch notes.txt
```

Write data.

```bash
echo "Hello Linux" > notes.txt
```

Create a Symbolic Link.

```bash
ln -s notes.txt shortcut.txt
```

---

# Verify the Link

Run:

```bash
ls -l
```

Example Output

```text
lrwxrwxrwx

shortcut.txt -> notes.txt
```

Explanation:

- `l` indicates a symbolic link.
- `->` shows the destination file.

---

# Verify Inode Numbers

Run:

```bash
ls -li
```

Example Output

```text
530461 notes.txt

530500 shortcut.txt
```

Notice:

The inode numbers are different.

---

# Working of a Soft Link

```text
shortcut.txt

↓

Path

↓

notes.txt

↓

Inode

↓

Data Block

↓

Hello Linux
```

Unlike a Hard Link, the Soft Link first reads the stored path.

Then Linux accesses the original file.

---

# Editing Through Soft Link

Open the Soft Link.

```bash
nano shortcut.txt
```

Add

```text
Linux is Awesome
```

Now display the original file.

```bash
cat notes.txt
```

Output

```text
Hello Linux

Linux is Awesome
```

Both display the same data because the Soft Link redirects to the original file.

---

# What Happens if the Original File is Deleted?

Delete the original file.

```bash
rm notes.txt
```

Now access the Soft Link.

```bash
cat shortcut.txt
```

Output

```text
No such file or directory
```

The Soft Link cannot find the original file.

---

# Broken Link

When the original file no longer exists,

the Symbolic Link becomes a:

**Broken Link**

It still exists,

but it points to a location that no longer exists.

---

# Soft Link to a Directory

Unlike Hard Links,

Soft Links can also point to directories.

Example

```bash
ln -s /home/dilip/Documents DocsShortcut
```

Now

```bash
cd DocsShortcut
```

takes you directly to the Documents directory.

---

# Advantages

- Saves storage space.
- Easy to create.
- Can link directories.
- Can work across different file systems.
- Useful for shortcuts.

---

# Limitations

- Stops working if the original file is deleted.
- Slightly slower because Linux first resolves the stored path.
- Broken links may create confusion.

---

# Practical (Ubuntu VirtualBox)

Create a file.

```bash
touch notes.txt
```

Write content.

```bash
echo "Hello Linux" > notes.txt
```

Create a Soft Link.

```bash
ln -s notes.txt shortcut.txt
```

Display the link.

```bash
ls -l
```

Check inode numbers.

```bash
ls -li
```

Delete the original file.

```bash
rm notes.txt
```

Read the shortcut.

```bash
cat shortcut.txt
```

Observe the Broken Link error.

---

# Real World Applications

## Software Developers

Create shortcuts to project folders.

---

## Linux Administrators

Manage configuration files.

---

## DevOps Engineers

Use symbolic links for deployment.

Example

```text
/etc/nginx/sites-enabled
```

contains symbolic links.

---

## Cloud Engineers

Deploy applications using symbolic links for shared resources.

---

# Common Beginner Mistakes

### Mistake 1

Thinking Soft Link stores the file data.

Correct:

It stores only the file path.

---

### Mistake 2

Thinking Soft Link and Hard Link are the same.

Correct:

Hard Link shares the inode.

Soft Link stores the path.

---

### Mistake 3

Deleting the original file.

Correct:

The Soft Link becomes a Broken Link.

---

# Quick Revision

- Soft Link = Shortcut.
- Has its own inode.
- Stores only the path.
- Created using `ln -s`.
- Original file deletion creates a Broken Link.
- Can link directories.
- Can work across different file systems.

---

# Important Keywords

- Soft Link
- Symbolic Link
- Broken Link
- Path
- Shortcut

---

# Frequently Asked Questions

## What is a Soft Link?

A Soft Link is a shortcut pointing to another file or directory.

---

## Which command creates a Soft Link?

```bash
ln -s
```

---

## Does a Soft Link have its own inode?

Yes.

---

## Can a Soft Link point to directories?

Yes.

---

## What happens if the original file is deleted?

The Soft Link becomes a Broken Link.

---

# MCQ Questions

### Q1.

Which command creates a Soft Link?

A. ln

B. cp

C. ln -s

D. mv

**Answer:** C

---

### Q2.

A Soft Link stores:

A. Data

B. Metadata

C. Path

D. Owner

**Answer:** C

---

### Q3.

Soft Link has:

A. Same inode

B. Different inode

C. No inode

D. Shared inode

**Answer:** B

---

### Q4.

Deleting the original file results in:

A. File duplication

B. Broken Link

C. Link Count increase

D. Permission error

**Answer:** B

---

### Q5.

Soft Links can be created:

A. Only inside one filesystem

B. Across different file systems

C. Only inside /home

D. Only for files

**Answer:** B

---

# Interview Questions

- What is a Symbolic Link?
- Why do we use Soft Links?
- What is a Broken Link?
- How is a Soft Link different from a Hard Link?
- Which command creates a Soft Link?

---

# Viva Questions

1. Define Soft Link.
2. What is another name for Soft Link?
3. Which command creates a Soft Link?
4. What is a Broken Link?
5. Can a Soft Link point to a directory?

---

# 2 Marks Questions

1. Define Soft Link.
2. What is a Broken Link?
3. Which command creates a Soft Link?
4. Can Soft Links work across different file systems?

---

# 5 Marks Questions

1. Explain Soft Link with a suitable example.
2. Explain the working of a Symbolic Link.

---

# Long Answer Questions

1. Explain Soft Links in UNIX/Linux with diagram and practical example.
2. Explain the advantages and limitations of Soft Links.

---

# Command Cheat Sheet

| Command | Purpose |
|----------|---------|
| `ln -s source target` | Create Soft Link |
| `ls -l` | Display Link Information |
| `ls -li` | Display Inode Numbers |
| `cat filename` | Display File Contents |
| `rm filename` | Delete File |

---

# Previous Year Exam Focus

⭐⭐⭐⭐⭐ Very Important

- Definition of Soft Link
- Symbolic Link
- Broken Link
- ln -s Command
- Practical Commands

---

# Summary

- A Soft Link (Symbolic Link) is a shortcut to another file or directory.
- It has its own inode number.
- It stores the path of the original file.
- It is created using the `ln -s` command.
- If the original file is deleted, the Soft Link becomes a Broken Link.
- Soft Links can also point to directories and work across different file systems.

---

# Related Topics

⬅️ Previous Topic

**11-Hard-Link.md**

➡️ Next Topic

**13-Hard-Link-vs-Soft-Link.md**