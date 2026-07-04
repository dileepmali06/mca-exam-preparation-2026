# 3.3.2 Head, Tail and Cut Commands

> **Module:** Module 3 -- Unix/Linux Commands\
> **Topic:** Head, Tail and Cut Commands\
> **Subject:** Unix/Linux Programming

------------------------------------------------------------------------

# Learning Objectives

-   Understand the `head`, `tail`, and `cut` commands.
-   Display the beginning and end of files.
-   Extract specific fields and characters.
-   Perform basic practical commands in Ubuntu Linux.

------------------------------------------------------------------------

# Introduction

Linux provides several filter commands to display or extract only the
required part of a file. The most commonly used commands are:

-   `head`
-   `tail`
-   `cut`

These commands help users work efficiently with large files.

------------------------------------------------------------------------

# Head Command

## Definition

The **head** command displays the first 10 lines of a file by default.

### Syntax

``` bash
head filename
```

### Examples

``` bash
head students.txt
head -5 students.txt
head -n 3 students.txt
```

### Features

-   Displays first lines of a file.
-   Default output is 10 lines.
-   Supports custom number of lines.

------------------------------------------------------------------------

# Tail Command

## Definition

The **tail** command displays the last 10 lines of a file by default.

### Syntax

``` bash
tail filename
```

### Examples

``` bash
tail students.txt
tail -5 students.txt
tail -n 3 students.txt
```

### Live Monitoring

``` bash
tail -f logfile.txt
```

`tail -f` continuously displays newly added data in a log file.

### Features

-   Displays last lines of a file.
-   Useful for monitoring log files.
-   Supports custom number of lines.

------------------------------------------------------------------------

# Cut Command

## Definition

The **cut** command extracts selected fields or characters from a file.

### Syntax

``` bash
cut [options] filename
```

### Important Options

  Option   Purpose
  -------- ---------------------------
  `-d`     Specify delimiter
  `-f`     Select field
  `-c`     Select character position

### Sample File

``` text
Rahul,20,BCA
Aman,21,MCA
Dilip,22,MCA
```

### Examples

Extract first field:

``` bash
cut -d "," -f1 students.txt
```

Extract second field:

``` bash
cut -d "," -f2 students.txt
```

Extract third field:

``` bash
cut -d "," -f3 students.txt
```

Extract characters:

``` bash
cut -c 1-5 students.txt
```

------------------------------------------------------------------------

# Difference

  Command     Purpose
  ----------- ------------------------------
  `head`      Displays first lines
  `tail`      Displays last lines
  `tail -f`   Live monitoring
  `cut`       Extract fields or characters

------------------------------------------------------------------------

# Practical

Create sample file:

``` bash
cat > students.txt
```

``` text
Rahul,20,BCA
Aman,21,MCA
Dilip,22,MCA
Karan,21,BCA
Neha,20,BCA
```

Run:

``` bash
head -3 students.txt
tail -2 students.txt
cut -d "," -f1 students.txt
cut -d "," -f3 students.txt
```

------------------------------------------------------------------------

# Quick Revision

-   `head` → First 10 lines
-   `head -n N` → First N lines
-   `tail` → Last 10 lines
-   `tail -f` → Monitor log files
-   `cut -d` → Delimiter
-   `cut -f` → Field
-   `cut -c` → Character position

------------------------------------------------------------------------

# MCQs

**Q1. Which command displays the first 10 lines of a file?**

A. tail\
B. head\
C. cut\
D. grep

**Answer:** B

------------------------------------------------------------------------

**Q2. Which option is used for continuous monitoring?**

A. `-d`\
B. `-f`\
C. `-n`\
D. `-c`

**Answer:** B

------------------------------------------------------------------------

**Q3. Which command extracts fields from a file?**

A. sort\
B. cut\
C. wc\
D. grep

**Answer:** B

------------------------------------------------------------------------

# Interview / Viva Questions

1.  What is the head command?
2.  What is the use of tail -f?
3.  Explain the cut command.
4.  What is the difference between head and tail?
5.  Explain the `-d` and `-f` options.

------------------------------------------------------------------------

# Command Cheat Sheet

  Command                     Purpose
  --------------------------- -----------------
  `head file.txt`             First 10 lines
  `head -5 file.txt`          First 5 lines
  `tail file.txt`             Last 10 lines
  `tail -f logfile.txt`       Live monitoring
  `cut -d "," -f1 file.txt`   First field
  `cut -c 1-5 file.txt`       Characters 1--5

------------------------------------------------------------------------

# Summary

-   `head` displays the beginning of a file.
-   `tail` displays the end of a file.
-   `tail -f` is mainly used for monitoring log files.
-   `cut` extracts selected fields and characters from a file.

------------------------------------------------------------------------

# Related Topics

**Previous:** 10-Introduction-to-Filters.md

**Next:** 12-Sort-and-WC.md
