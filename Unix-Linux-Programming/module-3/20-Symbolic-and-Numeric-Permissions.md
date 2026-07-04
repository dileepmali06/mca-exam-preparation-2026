# 3.5.2 Symbolic and Numeric Permissions

> **Module:** Module 3 -- Unix/Linux Commands\
> **Section:** Unix Permissions\
> **Topic:** Symbolic and Numeric Permissions\
> **Subject:** Unix/Linux Programming

------------------------------------------------------------------------

# Learning Objectives

-   Understand Symbolic Permissions.
-   Understand Numeric Permissions.
-   Learn permission values.
-   Use symbolic and numeric modes with `chmod`.

------------------------------------------------------------------------

# Introduction

Linux permissions can be represented in two ways:

-   **Symbolic Permissions** (r, w, x)
-   **Numeric Permissions** (755, 644, 777)

Both methods are used with the `chmod` command to manage file and
directory permissions.

------------------------------------------------------------------------

# Symbolic Permissions

## Definition

Symbolic permissions use letters to represent file permissions.

  Symbol   Meaning
  -------- ---------
  `r`      Read
  `w`      Write
  `x`      Execute

------------------------------------------------------------------------

# User Categories

  Symbol   Meaning
  -------- --------------
  `u`      User (Owner)
  `g`      Group
  `o`      Others
  `a`      All Users

------------------------------------------------------------------------

# Symbolic Operators

  Operator   Purpose
  ---------- ----------------------
  `+`        Add permission
  `-`        Remove permission
  `=`        Set exact permission

------------------------------------------------------------------------

# Examples

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

Give execute permission to everyone:

``` bash
chmod a+x program.sh
```

Set exact permission:

``` bash
chmod u=rwx file.txt
```

------------------------------------------------------------------------

# Numeric Permissions

## Definition

Numeric permissions use numbers instead of letters.

Permission values:

  Permission        Value
  --------------- -------
  Read (`r`)            4
  Write (`w`)           2
  Execute (`x`)         1

------------------------------------------------------------------------

# Numeric Permission Table

  Permission     Number
  ------------ --------
  `---`               0
  `--x`               1
  `-w-`               2
  `-wx`               3
  `r--`               4
  `r-x`               5
  `rw-`               6
  `rwx`               7

------------------------------------------------------------------------

# Common Numeric Permissions

## 777

``` text
rwxrwxrwx
```

``` bash
chmod 777 file.txt
```

Everyone has full access.

------------------------------------------------------------------------

## 755

``` text
rwxr-xr-x
```

``` bash
chmod 755 script.sh
```

-   Owner → Read, Write, Execute
-   Group → Read, Execute
-   Others → Read, Execute

------------------------------------------------------------------------

## 644

``` text
rw-r--r--
```

``` bash
chmod 644 notes.txt
```

-   Owner → Read, Write
-   Group → Read
-   Others → Read

------------------------------------------------------------------------

## 600

``` text
rw-------
```

``` bash
chmod 600 secret.txt
```

Only the owner can read and write.

------------------------------------------------------------------------

# Difference

  -----------------------------------------------------------------------
  Symbolic Permissions                 Numeric Permissions
  ------------------------------------ ----------------------------------
  Uses letters (`rwx`)                 Uses numbers (`755`)

  Easy to modify specific permissions  Easy to assign complete
                                       permissions

  Uses `u`, `g`, `o`, `a`              Uses values 0--7
  -----------------------------------------------------------------------

------------------------------------------------------------------------

# Practical

Create a file:

``` bash
touch demo.txt
```

Check permissions:

``` bash
ls -l demo.txt
```

Add execute permission:

``` bash
chmod u+x demo.txt
```

Remove group write permission:

``` bash
chmod g-w demo.txt
```

Apply numeric permission:

``` bash
chmod 755 demo.txt
```

Verify:

``` bash
ls -l demo.txt
```

------------------------------------------------------------------------

# Quick Revision

-   `r = 4`
-   `w = 2`
-   `x = 1`
-   `7 = rwx`
-   `6 = rw-`
-   `5 = r-x`
-   `4 = r--`
-   `chmod u+x` → Add execute
-   `chmod g-w` → Remove write
-   `chmod 755` → Numeric permission

------------------------------------------------------------------------

# MCQs

**Q1. What is the value of Read permission?**

A. 1\
B. 2\
C. 4\
D. 7

**Answer:** C

------------------------------------------------------------------------

**Q2. What is the value of Execute permission?**

A. 1\
B. 2\
C. 4\
D. 7

**Answer:** A

------------------------------------------------------------------------

**Q3. Which command gives execute permission to the owner?**

``` bash
chmod u+x file.txt
```

**Answer:** Correct

------------------------------------------------------------------------

**Q4. What does permission `755` represent?**

A. `rw-r--r--`\
B. `rwxr-xr-x`\
C. `rwxrwxrwx`\
D. `rw-------`

**Answer:** B

------------------------------------------------------------------------

**Q5. Which permission is commonly used for normal files?**

A. 777\
B. 755\
C. 644\
D. 000

**Answer:** C

------------------------------------------------------------------------

# Interview / Viva Questions

1.  What are Symbolic Permissions?
2.  What are Numeric Permissions?
3.  Explain permission values (4, 2, 1).
4.  Differentiate between Symbolic and Numeric Permissions.
5.  Explain common permissions such as 755 and 644.

------------------------------------------------------------------------

# Command Cheat Sheet

  Command                Purpose
  ---------------------- -------------------------------
  `chmod u+x file.txt`   Add execute permission
  `chmod g-w file.txt`   Remove group write permission
  `chmod o+r file.txt`   Add read permission to others
  `chmod a+x file.txt`   Add execute permission to all
  `chmod 755 file.txt`   Set permission to 755
  `chmod 644 file.txt`   Set permission to 644

------------------------------------------------------------------------

# Summary

-   Symbolic permissions use letters (`r`, `w`, `x`).
-   Numeric permissions use numbers (755, 644, 777).
-   The `chmod` command supports both symbolic and numeric methods.
-   Correct permissions improve Linux system security.

------------------------------------------------------------------------

# Related Topics

**Previous:** 19-Understanding-Permissions.md

**Next:** 21-Changing-Permissions.md
