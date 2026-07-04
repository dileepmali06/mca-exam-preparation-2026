# 3.5.1 Understanding Permissions

> **Module:** Module 3 -- Unix/Linux Commands\
> **Section:** Unix Permissions\
> **Topic:** Understanding Permissions\
> **Subject:** Unix/Linux Programming

------------------------------------------------------------------------

# Learning Objectives

-   Understand Unix Permissions.
-   Learn Read, Write and Execute permissions.
-   Understand User, Group and Others.
-   View file permissions using Linux commands.

------------------------------------------------------------------------

# Introduction

Unix Permissions are security rules that control who can access a file
or directory and what actions they can perform.

Permissions help protect files from unauthorized access and
modification.

------------------------------------------------------------------------

# What are Unix Permissions?

**Unix Permissions** define whether a user can:

-   Read a file
-   Write (modify) a file
-   Execute a file

------------------------------------------------------------------------

# Permission Types

  Permission   Symbol   Meaning
  ------------ -------- ----------------------------------
  Read         `r`      View file contents
  Write        `w`      Modify or edit a file
  Execute      `x`      Run a file or access a directory

------------------------------------------------------------------------

# User Categories

  Category     Meaning
  ------------ -------------------------
  User (u)     File Owner
  Group (g)    Users in the same group
  Others (o)   All remaining users

------------------------------------------------------------------------

# Understanding Permission String

Command:

``` bash
ls -l
```

Example:

``` text
-rwxr-xr--
```

Breakdown:

``` text
- rwx r-x r--
| |   |   |
| |   |   └── Others
| |   └────── Group
| └────────── Owner
└──────────── File Type
```

------------------------------------------------------------------------

# File Types

  Symbol   Meaning
  -------- ---------------
  `-`      Regular File
  `d`      Directory
  `l`      Symbolic Link

------------------------------------------------------------------------

# Permission Meaning

Example:

``` text
-rwxr-xr--
```

**Owner:** `rwx`

-   Read ✔
-   Write ✔
-   Execute ✔

**Group:** `r-x`

-   Read ✔
-   Write ✘
-   Execute ✔

**Others:** `r--`

-   Read ✔
-   Write ✘
-   Execute ✘

------------------------------------------------------------------------

# Viewing Permissions

Display permissions:

``` bash
ls -l
```

Display directory permissions:

``` bash
ls -ld project
```

------------------------------------------------------------------------

# Practical

Create a file:

``` bash
touch notes.txt
```

Check permissions:

``` bash
ls -l notes.txt
```

Create a directory:

``` bash
mkdir project
```

Check directory permissions:

``` bash
ls -ld project
```

------------------------------------------------------------------------

# Importance of Permissions

-   Protect important files.
-   Prevent unauthorized access.
-   Improve system security.
-   Control user access.
-   Secure directories and scripts.

------------------------------------------------------------------------

# Quick Revision

-   `r` → Read
-   `w` → Write
-   `x` → Execute
-   User → Owner
-   Group → Same group
-   Others → Remaining users
-   `ls -l` → View permissions

------------------------------------------------------------------------

# MCQs

**Q1. What does `r` represent?**

A. Run\
B. Read\
C. Remove\
D. Rename

**Answer:** B

------------------------------------------------------------------------

**Q2. Which permission allows editing a file?**

A. Read\
B. Execute\
C. Write\
D. Open

**Answer:** C

------------------------------------------------------------------------

**Q3. Which command displays permissions?**

A. `pwd`\
B. `ls -l`\
C. `cat`\
D. `mkdir`

**Answer:** B

------------------------------------------------------------------------

**Q4. What does `x` represent?**

A. Execute\
B. Exit\
C. Extract\
D. Expand

**Answer:** A

------------------------------------------------------------------------

**Q5. Which category represents all remaining users?**

A. User\
B. Group\
C. Others\
D. Root

**Answer:** C

------------------------------------------------------------------------

# Interview / Viva Questions

1.  What are Unix Permissions?
2.  Explain Read, Write and Execute permissions.
3.  What is the difference between User, Group and Others?
4.  Explain the output of `ls -l`.
5.  Why are file permissions important?

------------------------------------------------------------------------

# Command Cheat Sheet

  Command            Purpose
  ------------------ ----------------------------
  `ls -l`            View file permissions
  `ls -ld folder`    View directory permissions
  `touch file.txt`   Create a file
  `mkdir folder`     Create a directory

------------------------------------------------------------------------

# Summary

-   Unix Permissions control access to files and directories.
-   There are three permissions: Read, Write and Execute.
-   Permissions are assigned to User, Group and Others.
-   The `ls -l` command displays permission information.

------------------------------------------------------------------------

# Related Topics

**Previous:** 18-Redirecting-Output-and-Error.md

**Next:** 20-Symbolic-and-Numeric-Permissions.md
