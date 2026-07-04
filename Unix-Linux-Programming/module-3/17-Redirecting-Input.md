# 3.4.2 Redirecting Input

> **Module:** Module 3 -- Unix/Linux Commands\
> **Section:** Standard Input/Output\
> **Topic:** Redirecting Input (`<`)\
> **Subject:** Unix/Linux Programming

------------------------------------------------------------------------

# Learning Objectives

-   Understand Input Redirection.
-   Learn the `<` operator.
-   Read input from a file.
-   Perform practical examples.

------------------------------------------------------------------------

# Introduction

Input Redirection allows a command to read data from a **file** instead
of the **keyboard**.

Normally, Linux commands take input from the keyboard (stdin). Using the
`<` operator, the input source can be changed to a file.

------------------------------------------------------------------------

# What is Input Redirection?

**Input Redirection** is the process of providing input to a command
from a file using the `<` operator.

------------------------------------------------------------------------

# Syntax

``` bash
command < filename
```

------------------------------------------------------------------------

# Working

Without Redirection

``` text
Keyboard
   │
   ▼
Command
   │
   ▼
Output
```

With Input Redirection

``` text
File
 │
 ▼
Command
 │
 ▼
Output
```

------------------------------------------------------------------------

# Examples

## Sort Data

``` bash
sort < names.txt
```

------------------------------------------------------------------------

## Count Lines, Words and Characters

``` bash
wc < names.txt
```

------------------------------------------------------------------------

## Display File

``` bash
cat < names.txt
```

------------------------------------------------------------------------

# Sample File

Create a file:

``` bash
cat > names.txt
```

``` text
Rahul
Aman
Dilip
Neha
Karan
```

Press **Ctrl + D** to save.

------------------------------------------------------------------------

# Advantages

-   Reads input from a file.
-   Saves time.
-   Useful for large files.
-   Commonly used in shell scripts.
-   Improves automation.

------------------------------------------------------------------------

# Practical

Display file:

``` bash
cat < names.txt
```

Sort data:

``` bash
sort < names.txt
```

Count contents:

``` bash
wc < names.txt
```

------------------------------------------------------------------------

# Difference

  Normal Input              Input Redirection
  ------------------------- -------------------------
  Keyboard input            File input
  Manual typing             Automatic reading
  Suitable for small data   Suitable for large data

------------------------------------------------------------------------

# Quick Revision

-   `<` → Input Redirection
-   Reads input from a file.
-   Replaces keyboard input.
-   Does not modify the file.
-   Uses **stdin**.

------------------------------------------------------------------------

# MCQs

**Q1. Which operator is used for Input Redirection?**

A. `>`\
B. `<`\
C. `>>`\
D. `|`

**Answer:** B

------------------------------------------------------------------------

**Q2. Input Redirection reads data from:**

A. Keyboard\
B. Screen\
C. File\
D. Printer

**Answer:** C

------------------------------------------------------------------------

**Q3. Which stream is used for Input Redirection?**

A. stdout\
B. stderr\
C. stdin\
D. pipe

**Answer:** C

------------------------------------------------------------------------

**Q4. Which command sorts data from a file?**

``` bash
sort < names.txt
```

**Answer:** Correct

------------------------------------------------------------------------

**Q5. Does Input Redirection modify the input file?**

A. Yes\
B. No

**Answer:** B

------------------------------------------------------------------------

# Interview / Viva Questions

1.  What is Input Redirection?
2.  Explain the `<` operator.
3.  What is stdin?
4.  Give an example of Input Redirection.
5.  What are the advantages of Input Redirection?

------------------------------------------------------------------------

# Command Cheat Sheet

  Command              Purpose
  -------------------- ---------------------
  `sort < names.txt`   Sort file data
  `wc < names.txt`     Count file contents
  `cat < names.txt`    Display file

------------------------------------------------------------------------

# Summary

-   Input Redirection uses the `<` operator.
-   It reads data from a file instead of the keyboard.
-   It is useful for automation, shell scripting and processing large
    files.

------------------------------------------------------------------------

# Related Topics

**Previous:** 16-Introduction-to-Redirection.md

**Next:** 17-Redirecting-Output-and-Error.md
