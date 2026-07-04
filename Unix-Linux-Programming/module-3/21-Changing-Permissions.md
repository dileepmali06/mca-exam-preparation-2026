# 3.5.3 Changing Permissions (`chmod`)

> **Module:** Module 3 -- Unix/Linux Commands\
> **Section:** Unix Permissions\
> **Topic:** Changing Permissions (`chmod`)\
> **Subject:** Unix/Linux Programming

------------------------------------------------------------------------

# Learning Objectives

-   Understand the `chmod` command.
-   Change file and directory permissions.
-   Use symbolic and numeric modes.
-   Apply recursive permissions.

------------------------------------------------------------------------

# Introduction

The **chmod (Change Mode)** command is used to change the permissions of
files and directories in Linux.

It supports:

-   Symbolic Mode
-   Numeric Mode

------------------------------------------------------------------------

# Syntax

## Symbolic Mode

``` bash
chmod [who][operator][permission] filename
```

Example:

``` bash
chmod u+x script.sh
```

## Numeric Mode

``` bash
chmod permission filename
```

Example:

``` bash
chmod 755 script.sh
```

------------------------------------------------------------------------

# Symbolic Mode Examples

Add execute permission to owner:

``` bash
chmod u+x script.sh
```

Remove write permission from group:

``` bash
chmod g-w file.txt
```

Give read permission to others:

``` bash
chmod o+r notes.txt
```

Give execute permission to all:

``` bash
chmod a+x program.sh
```

Set exact permission:

``` bash
chmod u=rwx file.txt
```

------------------------------------------------------------------------

# Numeric Mode Examples

## Permission 777

``` bash
chmod 777 file.txt
```

``` text
rwxrwxrwx
```

Everyone has full access.

------------------------------------------------------------------------

## Permission 755

``` bash
chmod 755 script.sh
```

``` text
rwxr-xr-x
```

-   Owner → Read, Write, Execute
-   Group → Read, Execute
-   Others → Read, Execute

------------------------------------------------------------------------

## Permission 644

``` bash
chmod 644 notes.txt
```

``` text
rw-r--r--
```

-   Owner → Read, Write
-   Group → Read
-   Others → Read

------------------------------------------------------------------------

## Permission 600

``` bash
chmod 600 secret.txt
```

``` text
rw-------
```

Only the owner can read and write.

------------------------------------------------------------------------

# Recursive Permission

Change permission for a directory and all its contents:

``` bash
chmod -R 755 project
```

`-R` means **Recursive**.

------------------------------------------------------------------------

# View Permissions

``` bash
ls -l
```

View directory permissions:

``` bash
ls -ld project
```

------------------------------------------------------------------------

# Practical

Create a file:

``` bash
touch script.sh
```

Check permissions:

``` bash
ls -l script.sh
```

Change permissions:

``` bash
chmod u+x script.sh
chmod 755 script.sh
```

Create a directory:

``` bash
mkdir project
```

Apply recursive permission:

``` bash
chmod -R 755 project
```

Verify:

``` bash
ls -l
```

------------------------------------------------------------------------

# Difference

  Symbolic Mode                 Numeric Mode
  ----------------------------- --------------------------
  `chmod u+x file`              `chmod 755 file`
  Changes specific permission   Sets complete permission
  Uses letters                  Uses numbers

------------------------------------------------------------------------

# Quick Revision

-   `chmod` → Change permissions
-   `u+x` → Add execute to owner
-   `g-w` → Remove write from group
-   `o+r` → Add read to others
-   `755` → `rwxr-xr-x`
-   `644` → `rw-r--r--`
-   `600` → `rw-------`
-   `-R` → Recursive permission change

------------------------------------------------------------------------

# MCQs

**Q1. Which command changes file permissions?**

A. ls\
B. chmod\
C. cat\
D. pwd

**Answer:** B

------------------------------------------------------------------------

**Q2. Which option changes permissions recursively?**

A. -l\
B. -R\
C. -a\
D. -r

**Answer:** B

------------------------------------------------------------------------

**Q3. Which command gives execute permission to the owner?**

``` bash
chmod u+x script.sh
```

**Answer:** Correct

------------------------------------------------------------------------

**Q4. Which permission is commonly used for executable scripts?**

A. 644\
B. 755\
C. 777\
D. 600

**Answer:** B

------------------------------------------------------------------------

**Q5. What does `chmod 644 file.txt` represent?**

A. rwxrwxrwx\
B. rw-r--r--\
C. rwxr-xr-x\
D. rw-------

**Answer:** B

------------------------------------------------------------------------

# Interview / Viva Questions

1.  What is the `chmod` command?
2.  Explain symbolic and numeric modes.
3.  What is the use of `chmod -R`?
4.  Differentiate between `755` and `644`.
5.  Why is `777` generally not recommended?

------------------------------------------------------------------------

# Command Cheat Sheet

  Command              Purpose
  -------------------- -------------------------------
  `chmod u+x file`     Add execute permission
  `chmod g-w file`     Remove group write permission
  `chmod o+r file`     Add read permission
  `chmod a+x file`     Add execute to all
  `chmod 755 file`     Set permission 755
  `chmod 644 file`     Set permission 644
  `chmod -R 755 dir`   Recursive permission

------------------------------------------------------------------------

# Summary

-   `chmod` changes file and directory permissions.
-   It supports symbolic and numeric modes.
-   `755` is commonly used for executable files.
-   `644` is commonly used for normal files.
-   `-R` changes permissions recursively.

------------------------------------------------------------------------

# Related Topics

**Previous:** 20-Symbolic-and-Numeric-Permissions.md

**Next:** Module 4
