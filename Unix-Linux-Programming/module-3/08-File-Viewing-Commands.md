# 3.2.6 Viewing Files (`cat`, `more`, `pg`, `less`)

> **Module:** Module 3 – Unix/Linux Commands
>
> **Topic:** Viewing Files (`cat`, `more`, `pg`, `less`)
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

- Understand different Linux file viewing commands.
- View small and large files efficiently.
- Use `cat`, `more`, `less`, and `pg`.
- Navigate large files page by page.
- Compare different file viewing commands.
- Perform practical file viewing operations in Ubuntu Linux.

---

# Introduction

Linux provides several commands to view the contents of files.

Different commands are suitable for different situations.

For example:

- Small files → `cat`
- Large files → `more`
- Very large files → `less`
- Traditional Unix systems → `pg`

Choosing the appropriate command makes file reading easier and more efficient.

---

# The `cat` Command

## Definition

The **`cat` (Concatenate)** command is used to display the complete contents of a file.

It is most suitable for small text files.

---

# Syntax

```bash
cat filename
```

---

# Example

```bash
cat notes.txt
```

Output

```text
Linux

Unix

Kernel

Shell
```

---

# Features of `cat`

- Displays complete file contents.
- Fast and simple.
- Can display multiple files.
- Suitable for small files.

---

# The `more` Command

## Definition

The **`more`** command displays file contents one page at a time.

It is useful for reading large files.

---

# Syntax

```bash
more filename
```

---

# Example

```bash
more notes.txt
```

Output

```text
Linux

Unix

Kernel

Shell

------More------
```

---

# Navigation Keys

| Key | Function |
|------|----------|
| Space | Next Page |
| Enter | Next Line |
| q | Quit |

---

# Features of `more`

- Page-by-page viewing.
- Easy to read large files.
- Simple navigation.

---

# Limitations of `more`

- Cannot scroll backward.
- Limited navigation options.

---

# The `less` Command

## Definition

The **`less`** command is an advanced file viewer.

It allows both forward and backward navigation.

It is considered an improved version of `more`.

---

# Syntax

```bash
less filename
```

---

# Example

```bash
less notes.txt
```

---

# Navigation Keys

| Key | Function |
|------|----------|
| Space | Next Page |
| b | Previous Page |
| ↑ | Scroll Up |
| ↓ | Scroll Down |
| /text | Search Text |
| q | Quit |

---

# Features of `less`

- Scroll forward.
- Scroll backward.
- Search within files.
- Efficient for very large files.
- Faster than `cat` for large files.

---

# The `pg` Command

## Definition

The **`pg`** command is a traditional Unix page viewer.

It displays files one page at a time.

Modern Linux systems generally prefer the `less` command.

---

# Syntax

```bash
pg filename
```

---

# Example

```bash
pg notes.txt
```

---

# Features of `pg`

- Page-by-page viewing.
- Simple navigation.
- Mostly used on older Unix systems.

---

# Comparison of File Viewing Commands

| Command | Best For | Forward | Backward | Search |
|----------|----------|----------|-----------|---------|
| `cat` | Small Files | No | No | No |
| `more` | Large Files | Yes | No | Limited |
| `less` | Very Large Files | Yes | Yes | Yes |
| `pg` | Unix Systems | Yes | Limited | Limited |

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

Create a Sample File.

```bash
cat > notes.txt
```

Type:

```text
Linux

Unix

Kernel

Shell

Operating System

Commands

Programming
```

Press:

```text
Ctrl + D
```

---

## Step 3

Display the File Using `cat`.

```bash
cat notes.txt
```

---

## Step 4

Display the File Using `more`.

```bash
more notes.txt
```

Use:

- Space → Next Page
- Enter → Next Line
- q → Quit

---

## Step 5

Display the File Using `less`.

```bash
less notes.txt
```

Try:

- Space
- b
- ↑
- ↓
- /Kernel
- q

---

## Step 6

Display the File Using `pg` (if installed).

```bash
pg notes.txt
```

---

# Expected Output

```text
$ cat notes.txt

Linux

Unix

Kernel

Shell
```

---

```text
$ more notes.txt

Linux

Unix

Kernel

------More------
```

---

```text
$ less notes.txt
```

(Interactive viewer opens.)

---

# Real World Applications

## Software Developers

- Read source code files.
- View README files.
- Check configuration files.

---

## Backend Developers

- Inspect JSON files.
- Read application logs.
- View server configuration.

---

## DevOps Engineers

- Analyze deployment logs.
- Monitor server log files.
- Read configuration files.

---

## Linux System Administrators

- View system logs.
- Read configuration files.
- Monitor server reports.

---

# Common Beginner Mistakes

### Mistake 1

Using `cat` for extremely large files.

**Correct:**

Use:

```bash
less filename
```

---

### Mistake 2

Expecting backward scrolling in `more`.

**Correct:**

`more` supports mainly forward navigation.

---

### Mistake 3

Assuming `pg` is available on every Linux system.

**Correct:**

Many modern Linux distributions do not install `pg` by default.

---

# Advantages

## `cat`

- Simple.
- Fast.
- Best for small files.

---

## `more`

- Reads large files page by page.
- Easy navigation.

---

## `less`

- Supports forward and backward navigation.
- Search functionality.
- Best for large files.

---

## `pg`

- Traditional Unix pager.
- Useful on older Unix systems.

---

# Quick Revision

- `cat` displays complete file contents.
- `more` displays files page by page.
- `less` allows forward and backward navigation.
- `pg` is a traditional Unix page viewer.
- `less` is generally preferred over `more` and `pg`.

---

# Important Keywords

- `cat`
- `more`
- `less`
- `pg`
- File Viewer
- Page Viewer
- File Navigation
- Search

---

# Frequently Asked Questions

## What is the purpose of the `cat` command?

It displays the complete contents of a file.

---

## Which command is best for large files?

```bash
less filename
```

---

## Which command displays files page by page?

```bash
more filename
```

---

## Which command supports backward scrolling?

```bash
less filename
```

---

## Which command is mainly used on older Unix systems?

```bash
pg filename
```

---

# MCQ Questions

### Q1.

Which command is best for viewing small files?

A. `less`

B. `cat`

C. `more`

D. `pg`

**Answer:** B

---

### Q2.

Which command supports backward navigation?

A. `cat`

B. `more`

C. `less`

D. `touch`

**Answer:** C

---

### Q3.

Which command displays files page by page?

A. `ls`

B. `more`

C. `pwd`

D. `mkdir`

**Answer:** B

---

### Q4.

Which command is considered an advanced version of `more`?

A. `cat`

B. `less`

C. `touch`

D. `echo`

**Answer:** B

---

### Q5.

Which command is mainly associated with traditional Unix systems?

A. `pg`

B. `mv`

C. `cp`

D. `rm`

**Answer:** A

---

# Interview Questions

- What is the purpose of the `cat` command?
- Explain the difference between `more` and `less`.
- Why is `less` preferred for large files?
- What is the use of the `pg` command?
- Compare all file viewing commands.

---

# Viva Questions

1. What is the `cat` command?
2. What is the `more` command?
3. What is the `less` command?
4. What is the purpose of `pg`?
5. Which command is best for large files?

---

# 2 Marks Questions

1. Define the `cat` command.
2. Define the `more` command.
3. Define the `less` command.
4. What is the purpose of the `pg` command?

---

# 5 Marks Questions

1. Explain the `cat` command with examples.
2. Explain the `more` command with examples.
3. Differentiate between `more` and `less`.

---

# Long Answer Questions

1. Explain different file viewing commands in Linux.
2. Compare `cat`, `more`, `less`, and `pg`.
3. Explain the advantages and limitations of different Linux file viewing commands.

---

# Command Cheat Sheet

| Command | Purpose |
|----------|---------|
| `cat file.txt` | Display file contents |
| `more file.txt` | View file page by page |
| `less file.txt` | Advanced file viewer |
| `pg file.txt` | Traditional Unix page viewer |

---

# Previous Year Exam Focus

⭐⭐⭐⭐⭐ Very Important

- `cat`
- `more`
- `less`
- `pg`
- Difference between `more` and `less`
- File Viewing Commands

---

# Summary

- Linux provides multiple commands to view file contents.
- `cat` is suitable for small files.
- `more` displays files page by page.
- `less` is an advanced viewer with forward, backward, and search capabilities.
- `pg` is a traditional Unix page viewer and is less common on modern Linux systems.
- Choosing the correct command improves efficiency when working with text files.

---

# Related Topics

⬅️ Previous Topic

**07-CP-MV-RM-Commands.md**

➡️ Next Topic

**09-Wildcards-and-Meta-Characters.md**