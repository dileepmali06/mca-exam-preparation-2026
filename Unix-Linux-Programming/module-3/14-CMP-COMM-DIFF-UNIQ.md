# 3.3.5 cmp, comm, diff and uniq Commands

> **Module:** Module 3 -- Unix/Linux Commands\
> **Topic:** cmp, comm, diff and uniq Commands\
> **Subject:** Unix/Linux Programming

------------------------------------------------------------------------

# Learning Objectives

-   Understand `cmp`, `comm`, `diff`, and `uniq`.
-   Compare files in Linux.
-   Find differences between files.
-   Remove duplicate lines.

------------------------------------------------------------------------

# Introduction

These Linux filter commands are used to compare files and process
duplicate data.

-   **cmp** → Compare two files byte by byte.
-   **comm** → Compare two sorted files.
-   **diff** → Show differences between files.
-   **uniq** → Remove duplicate adjacent lines.

------------------------------------------------------------------------

# cmp Command

## Definition

The **cmp** command compares two files byte by byte.

### Syntax

``` bash
cmp file1 file2
```

### Example

``` bash
cmp file1.txt file2.txt
```

If files differ:

``` text
file1.txt file2.txt differ: byte 15, line 2
```

------------------------------------------------------------------------

# comm Command

## Definition

The **comm** command compares two **sorted** files line by line.

> Both files should be sorted before using `comm`.

### Syntax

``` bash
comm file1 file2
```

### Example

``` bash
sort file1.txt > s1.txt
sort file2.txt > s2.txt
comm s1.txt s2.txt
```

------------------------------------------------------------------------

# diff Command

## Definition

The **diff** command displays differences between two files.

### Syntax

``` bash
diff file1 file2
```

### Example

``` bash
diff old.txt new.txt
```

Sample Output

``` text
2c2
< Linux
---
> Ubuntu
```

------------------------------------------------------------------------

# uniq Command

## Definition

The **uniq** command removes or displays duplicate adjacent lines.

> It works best with sorted files.

### Syntax

``` bash
uniq filename
```

### Examples

Remove duplicates

``` bash
uniq fruits.txt
```

Count duplicates

``` bash
uniq -c fruits.txt
```

Display duplicate lines

``` bash
uniq -d fruits.txt
```

Display unique lines

``` bash
uniq -u fruits.txt
```

------------------------------------------------------------------------

# Important Options

  Command     Purpose
  ----------- ----------------------------
  `cmp`       Compare files byte by byte
  `comm`      Compare sorted files
  `diff`      Show differences
  `uniq -c`   Count duplicate lines
  `uniq -d`   Show duplicate lines
  `uniq -u`   Show unique lines

------------------------------------------------------------------------

# Difference

  Command   Use
  --------- --------------------------------
  `cmp`     First difference between files
  `comm`    Compare sorted files
  `diff`    Show all differences
  `uniq`    Remove duplicate lines

------------------------------------------------------------------------

# Practical

Create two files:

``` bash
cat > file1.txt
```

``` text
Apple
Banana
Mango
```

``` bash
cat > file2.txt
```

``` text
Apple
Grapes
Mango
```

Run:

``` bash
cmp file1.txt file2.txt
diff file1.txt file2.txt
sort file1.txt > s1.txt
sort file2.txt > s2.txt
comm s1.txt s2.txt
```

Create duplicate file:

``` bash
cat > fruits.txt
```

``` text
Apple
Apple
Banana
Banana
Mango
```

Run:

``` bash
uniq fruits.txt
uniq -c fruits.txt
uniq -d fruits.txt
uniq -u fruits.txt
```

------------------------------------------------------------------------

# Quick Revision

-   `cmp` → Byte-by-byte comparison
-   `comm` → Compare sorted files
-   `diff` → Show differences
-   `uniq` → Remove duplicates
-   `uniq -c` → Count duplicates
-   `uniq -d` → Duplicate only
-   `uniq -u` → Unique only

------------------------------------------------------------------------

# MCQs

**Q1. Which command compares files byte by byte?**

A. diff\
B. cmp\
C. uniq\
D. grep

**Answer:** B

------------------------------------------------------------------------

**Q2. Which command compares sorted files?**

A. cmp\
B. comm\
C. uniq\
D. wc

**Answer:** B

------------------------------------------------------------------------

**Q3. Which command shows differences between files?**

A. diff\
B. grep\
C. sort\
D. cut

**Answer:** A

------------------------------------------------------------------------

**Q4. Which command removes duplicate lines?**

A. uniq\
B. head\
C. wc\
D. tail

**Answer:** A

------------------------------------------------------------------------

**Q5. Which option counts duplicate lines?**

A. `-u`\
B. `-d`\
C. `-c`\
D. `-n`

**Answer:** C

------------------------------------------------------------------------

# Interview / Viva Questions

1.  What is the cmp command?
2.  Explain the comm command.
3.  What is the use of diff?
4.  Explain uniq with examples.
5.  Differentiate between cmp and diff.

------------------------------------------------------------------------

# Command Cheat Sheet

  Command              Purpose
  -------------------- ----------------------
  `cmp file1 file2`    Compare files
  `comm s1 s2`         Compare sorted files
  `diff file1 file2`   Show differences
  `uniq file.txt`      Remove duplicates
  `uniq -c file.txt`   Count duplicates
  `uniq -d file.txt`   Show duplicates
  `uniq -u file.txt`   Show unique lines

------------------------------------------------------------------------

# Summary

-   `cmp` compares files byte by byte.
-   `comm` compares sorted files.
-   `diff` displays file differences.
-   `uniq` removes or displays duplicate lines.

------------------------------------------------------------------------

# Related Topics

**Previous:** 13-Grep-Command.md

**Next:** 15-expr-bc-exit.md
