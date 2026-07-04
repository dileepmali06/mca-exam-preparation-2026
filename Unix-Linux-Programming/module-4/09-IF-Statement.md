# 4.2.6 IF Statement (Numerical, File & String Test)

> **Module:** Module 4 -- VI Editor and Shell Programming\
> **Section:** Shell Programming\
> **Topic:** IF Statement (Numerical, File & String Test)

------------------------------------------------------------------------

# Learning Objectives

-   Understand the IF statement.
-   Learn `if`, `if...else` and `if...elif...else`.
-   Perform Numerical, String and File tests.
-   Write decision-making shell scripts.

------------------------------------------------------------------------

# Introduction

The **IF Statement** is used to make decisions in a shell script. It
executes a block of commands only when the specified condition is true.

------------------------------------------------------------------------

# Types of IF Statements

-   Simple `if`
-   `if...else`
-   `if...elif...else`

------------------------------------------------------------------------

# Simple IF

### Syntax

``` bash
if [ condition ]
then
    commands
fi
```

### Example

``` bash
A=20

if [ $A -gt 10 ]
then
    echo "A is Greater than 10"
fi
```

------------------------------------------------------------------------

# IF...ELSE

### Syntax

``` bash
if [ condition ]
then
    commands
else
    commands
fi
```

### Example

``` bash
read AGE

if [ $AGE -ge 18 ]
then
    echo "Eligible for Voting"
else
    echo "Not Eligible"
fi
```

------------------------------------------------------------------------

# IF...ELIF...ELSE

### Syntax

``` bash
if [ condition1 ]
then
    commands
elif [ condition2 ]
then
    commands
else
    commands
fi
```

### Example

``` bash
read MARKS

if [ $MARKS -ge 90 ]
then
    echo "Grade A"
elif [ $MARKS -ge 75 ]
then
    echo "Grade B"
else
    echo "Grade C"
fi
```

------------------------------------------------------------------------

# Numerical Test Operators

  Operator   Meaning
  ---------- -----------------------
  `-eq`      Equal
  `-ne`      Not Equal
  `-gt`      Greater Than
  `-lt`      Less Than
  `-ge`      Greater Than or Equal
  `-le`      Less Than or Equal

Example:

``` bash
if [ $A -gt $B ]
then
    echo "A is Greater"
fi
```

------------------------------------------------------------------------

# String Test Operators

  Operator   Meaning
  ---------- ---------------------
  `=`        Equal
  `!=`       Not Equal
  `-z`       String is empty
  `-n`       String is not empty

Example:

``` bash
NAME="Dilip"

if [ "$NAME" = "Dilip" ]
then
    echo "Welcome"
fi
```

------------------------------------------------------------------------

# File Test Operators

  Operator   Meaning
  ---------- --------------------------
  `-f`       File exists
  `-d`       Directory exists
  `-r`       Read permission
  `-w`       Write permission
  `-x`       Execute permission
  `-e`       File or directory exists
  `-s`       File is not empty

Example:

``` bash
if [ -f demo.txt ]
then
    echo "File Exists"
fi
```

------------------------------------------------------------------------

# Practical

``` bash
#!/bin/bash

echo "Enter Age:"
read AGE

if [ $AGE -ge 18 ]
then
    echo "Adult"
else
    echo "Minor"
fi
```

Run:

``` bash
chmod +x ifdemo.sh
./ifdemo.sh
```

------------------------------------------------------------------------

# Quick Revision

-   `if` → Decision making
-   `then` → Execute block
-   `else` → Alternative block
-   `elif` → Multiple conditions
-   `fi` → End of IF
-   `-gt` → Greater than
-   `-eq` → Equal
-   `-f` → File exists
-   `-d` → Directory exists
-   `-z` → Empty string

------------------------------------------------------------------------

# MCQs

**Q1. Which keyword starts an IF statement?**

A. `for`\
B. `if`\
C. `while`\
D. `case`

**Answer:** B

------------------------------------------------------------------------

**Q2. Which keyword ends an IF statement?**

A. `done`\
B. `end`\
C. `fi`\
D. `stop`

**Answer:** C

------------------------------------------------------------------------

**Q3. Which operator means Greater Than?**

A. `-eq`\
B. `-lt`\
C. `-gt`\
D. `=`

**Answer:** C

------------------------------------------------------------------------

**Q4. Which operator checks whether a file exists?**

A. `-d`\
B. `-f`\
C. `-z`\
D. `-n`

**Answer:** B

------------------------------------------------------------------------

**Q5. Which operator checks whether a string is empty?**

A. `-n`\
B. `-z`\
C. `-e`\
D. `-w`

**Answer:** B

------------------------------------------------------------------------

# Interview / Viva Questions

1.  What is an IF statement?
2.  Explain `if...else`.
3.  What is `elif`?
4.  Explain Numerical Test operators.
5.  Explain File and String Test operators.

------------------------------------------------------------------------

# Command Cheat Sheet

  Command              Purpose
  -------------------- ----------------------
  `if [ condition ]`   Start IF block
  `then`               Execute when true
  `else`               Alternative block
  `elif`               Additional condition
  `fi`                 End IF block

------------------------------------------------------------------------

# Summary

-   IF statements perform decision making.
-   Numerical, String and File tests are used to evaluate conditions.
-   `fi` terminates an IF block.
-   `if`, `if...else` and `if...elif...else` are the main decision
    structures.

------------------------------------------------------------------------

# Related Topics

**Previous:** 30-Operators-Read-and-Echo.md

**Next:** 32-Test-Command.md
