# 3.3.4 grep Command

> **Module:** Module 3 -- Unix/Linux Commands\
> **Topic:** grep Command\
> **Subject:** Unix/Linux Programming

------------------------------------------------------------------------

# Learning Objectives

-   Understand the `grep` command.
-   Search text or patterns in files.
-   Learn important grep options.
-   Perform practical examples.

------------------------------------------------------------------------

# Introduction

The **grep (Global Regular Expression Print)** command is used to search
a specific word or pattern in one or more files.

It is one of the most commonly used Linux filter commands.

------------------------------------------------------------------------

# grep Command

## Definition

The **grep** command searches for a word or pattern and displays only
the matching lines.

### Syntax

``` bash
grep [options] "pattern" filename
```

------------------------------------------------------------------------

# Examples

Search a word:

``` bash
grep "MCA" students.txt
```

Ignore case:

``` bash
grep -i "linux" notes.txt
```

Show line numbers:

``` bash
grep -n "MCA" students.txt
```

Show non-matching lines:

``` bash
grep -v "MCA" students.txt
```

Count matching lines:

``` bash
grep -c "MCA" students.txt
```

Search whole word:

``` bash
grep -w "Linux" notes.txt
```

------------------------------------------------------------------------

# Important Options

  Option   Purpose
  -------- ----------------------------
  `-i`     Ignore case
  `-n`     Show line numbers
  `-v`     Display non-matching lines
  `-c`     Count matching lines
  `-w`     Match whole word

------------------------------------------------------------------------

# Practical

Create a sample file:

``` bash
cat > students.txt
```

``` text
Rahul MCA
Aman BCA
Dilip MCA
Neha BCA
Karan MCA
```

Run the commands:

``` bash
grep "MCA" students.txt
grep -i "mca" students.txt
grep -n "MCA" students.txt
grep -v "MCA" students.txt
grep -c "MCA" students.txt
grep -w "MCA" students.txt
```

------------------------------------------------------------------------

# Quick Revision

-   `grep` → Search text or pattern
-   `-i` → Ignore case
-   `-n` → Line numbers
-   `-v` → Non-matching lines
-   `-c` → Count matches
-   `-w` → Whole word

------------------------------------------------------------------------

# MCQs

**Q1. Which command is used to search text?**

A. sort\
B. grep\
C. cut\
D. wc

**Answer:** B

------------------------------------------------------------------------

**Q2. Which option ignores case?**

A. `-n`\
B. `-v`\
C. `-i`\
D. `-c`

**Answer:** C

------------------------------------------------------------------------

**Q3. Which option displays line numbers?**

A. `-w`\
B. `-n`\
C. `-i`\
D. `-c`

**Answer:** B

------------------------------------------------------------------------

**Q4. Which option counts matching lines?**

A. `-v`\
B. `-w`\
C. `-c`\
D. `-n`

**Answer:** C

------------------------------------------------------------------------

**Q5. Which option displays non-matching lines?**

A. `-v`\
B. `-n`\
C. `-i`\
D. `-w`

**Answer:** A

------------------------------------------------------------------------

# Interview / Viva Questions

1.  What is the grep command?
2.  Explain `grep -i`.
3.  Explain `grep -n`.
4.  What is the use of `grep -v`?
5.  Differentiate between `grep -c` and `grep -w`.

------------------------------------------------------------------------

# Command Cheat Sheet

  Command                     Purpose
  --------------------------- -------------------------
  `grep "word" file.txt`      Search text
  `grep -i "word" file.txt`   Ignore case
  `grep -n "word" file.txt`   Show line numbers
  `grep -v "word" file.txt`   Show non-matching lines
  `grep -c "word" file.txt`   Count matches
  `grep -w "word" file.txt`   Whole word search

------------------------------------------------------------------------

# Summary

-   `grep` searches words or patterns in files.
-   It supports case-insensitive search, line numbers, counting and
    whole-word matching.
-   It is one of the most important Linux filter commands.

------------------------------------------------------------------------

# Related Topics

**Previous:** 12-Sort-and-WC.md

**Next:** 14-CMP-COMM-DIFF-UNIQ.md
