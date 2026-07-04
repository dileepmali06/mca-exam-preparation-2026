# 3.3.3 Sort and WC Commands

> **Module:** Module 3 -- Unix/Linux Commands\
> **Topic:** Sort and WC Commands\
> **Subject:** Unix/Linux Programming

------------------------------------------------------------------------

# Learning Objectives

-   Understand the `sort` command.
-   Learn sorting options.
-   Understand the `wc` command.
-   Count lines, words, characters and bytes.
-   Perform practical examples.

------------------------------------------------------------------------

# Introduction

The `sort` and `wc` commands are Linux filter commands used to process
text files.

-   **sort** → Arranges data alphabetically or numerically.
-   **wc** → Counts lines, words, characters and bytes.

------------------------------------------------------------------------

# Sort Command

## Definition

The **sort** command arranges file contents in alphabetical or numerical
order.

### Syntax

``` bash
sort filename
```

### Examples

Alphabetical Sort

``` bash
sort students.txt
```

Reverse Sort

``` bash
sort -r students.txt
```

Numeric Sort

``` bash
sort -n numbers.txt
```

Remove Duplicate Lines

``` bash
sort -u students.txt
```

Save Sorted Output

``` bash
sort students.txt -o sorted.txt
```

### Important Options

  Option   Purpose
  -------- ------------------------
  `-r`     Reverse sorting
  `-n`     Numeric sorting
  `-u`     Remove duplicate lines
  `-o`     Save output to file

------------------------------------------------------------------------

# WC Command

## Definition

The **wc (Word Count)** command counts:

-   Lines
-   Words
-   Characters
-   Bytes

### Syntax

``` bash
wc filename
```

### Examples

Count everything

``` bash
wc students.txt
```

Count lines

``` bash
wc -l students.txt
```

Count words

``` bash
wc -w students.txt
```

Count characters

``` bash
wc -m students.txt
```

Count bytes

``` bash
wc -c students.txt
```

### Important Options

  Option   Purpose
  -------- ------------------
  `-l`     Count lines
  `-w`     Count words
  `-m`     Count characters
  `-c`     Count bytes

------------------------------------------------------------------------

# Difference

  Command   Purpose
  --------- ------------------------------------------
  `sort`    Arrange data
  `wc`      Count lines, words, characters and bytes

------------------------------------------------------------------------

# Practical

Create a sample file:

``` bash
cat > students.txt
```

``` text
Rahul
Aman
Neha
Dilip
Karan
```

Run the commands:

``` bash
sort students.txt
sort -r students.txt
```

Create a number file:

``` bash
cat > numbers.txt
```

``` text
50
2
100
10
```

Run:

``` bash
sort -n numbers.txt
wc students.txt
wc -l students.txt
wc -w students.txt
wc -m students.txt
wc -c students.txt
```

------------------------------------------------------------------------

# Quick Revision

-   `sort` → Alphabetical sorting
-   `sort -r` → Reverse sorting
-   `sort -n` → Numeric sorting
-   `sort -u` → Remove duplicates
-   `wc` → Count everything
-   `wc -l` → Lines
-   `wc -w` → Words
-   `wc -m` → Characters
-   `wc -c` → Bytes

------------------------------------------------------------------------

# MCQs

**Q1. Which command arranges data alphabetically?**

A. grep\
B. sort\
C. cut\
D. wc

**Answer:** B

------------------------------------------------------------------------

**Q2. Which option performs numeric sorting?**

A. `-r`\
B. `-u`\
C. `-n`\
D. `-l`

**Answer:** C

------------------------------------------------------------------------

**Q3. Which command counts lines?**

A. sort\
B. wc -l\
C. grep\
D. tail

**Answer:** B

------------------------------------------------------------------------

**Q4. Which option removes duplicate lines?**

A. `-u`\
B. `-r`\
C. `-n`\
D. `-o`

**Answer:** A

------------------------------------------------------------------------

**Q5. Which command counts words?**

A. wc -m\
B. wc -w\
C. wc -c\
D. sort

**Answer:** B

------------------------------------------------------------------------

# Interview / Viva Questions

1.  What is the sort command?
2.  Explain `sort -n`.
3.  What is the use of the wc command?
4.  Explain `wc -l` and `wc -w`.
5.  Differentiate between `sort` and `wc`.

------------------------------------------------------------------------

# Command Cheat Sheet

  Command              Purpose
  -------------------- -------------------
  `sort file.txt`      Alphabetical sort
  `sort -r file.txt`   Reverse sort
  `sort -n file.txt`   Numeric sort
  `sort -u file.txt`   Remove duplicates
  `wc file.txt`        Count all
  `wc -l file.txt`     Count lines
  `wc -w file.txt`     Count words
  `wc -m file.txt`     Count characters
  `wc -c file.txt`     Count bytes

------------------------------------------------------------------------

# Summary

-   `sort` arranges text alphabetically or numerically.
-   `wc` counts lines, words, characters and bytes.
-   Both are important Linux filter commands used in text processing.

------------------------------------------------------------------------

# Related Topics

**Previous:** 11-Head-Tail-Cut.md

**Next:** 13-Grep-Command.md
