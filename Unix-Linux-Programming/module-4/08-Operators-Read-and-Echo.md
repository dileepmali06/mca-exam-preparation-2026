# 4.2.5 Assignment Statements, Arithmetic, Logical & Relational Operators, `read` and `echo`

> **Module:** Module 4 -- VI Editor and Shell Programming\
> **Section:** Shell Programming\
> **Topic:** Assignment Statements, Arithmetic, Logical & Relational
> Operators, `read` and `echo`

------------------------------------------------------------------------

# Learning Objectives

-   Learn variable assignment.
-   Perform arithmetic operations.
-   Understand relational and logical operators.
-   Use `read` and `echo` commands.

------------------------------------------------------------------------

# Assignment Statement

Stores a value in a variable.

### Syntax

``` bash
VARIABLE=value
```

### Example

``` bash
NAME="Dilip"
AGE=21

echo $NAME
echo $AGE
```

> **Note:** Do not put spaces around `=`.

------------------------------------------------------------------------

# Arithmetic Operators

Use arithmetic expansion:

``` bash
echo $((A+B))
```

  Operator   Meaning
  ---------- ----------------
  `+`        Addition
  `-`        Subtraction
  `*`        Multiplication
  `/`        Division
  `%`        Modulus

### Example

``` bash
A=20
B=10

echo $((A+B))
echo $((A-B))
echo $((A*B))
echo $((A/B))
echo $((A%B))
```

------------------------------------------------------------------------

# Relational Operators

Used to compare numbers.

  Operator   Meaning
  ---------- -----------------------
  `-eq`      Equal
  `-ne`      Not Equal
  `-gt`      Greater Than
  `-lt`      Less Than
  `-ge`      Greater Than or Equal
  `-le`      Less Than or Equal

### Example

``` bash
[ 10 -gt 5 ]
```

------------------------------------------------------------------------

# Logical Operators

  Operator   Meaning
  ---------- ---------
  `&&`       AND
  `||`       OR
  `!`        NOT

### Example

``` bash
[ 10 -gt 5 ] && [ 20 -gt 10 ]
```

------------------------------------------------------------------------

# `echo` Command

Displays output.

``` bash
echo "Welcome to Linux"
```

Display a variable:

``` bash
NAME="Dilip"
echo $NAME
```

------------------------------------------------------------------------

# `read` Command

Accepts input from the user.

``` bash
read NAME
echo "Hello $NAME"
```

------------------------------------------------------------------------

# Complete Program

``` bash
#!/bin/bash

echo "Enter First Number:"
read A

echo "Enter Second Number:"
read B

SUM=$((A+B))

echo "Addition = $SUM"
```

------------------------------------------------------------------------

# Practical

Create script:

``` bash
vi add.sh
```

Make executable:

``` bash
chmod +x add.sh
```

Run:

``` bash
./add.sh
```

------------------------------------------------------------------------

# Quick Revision

-   `NAME="Dilip"` → Assignment
-   `$(( ))` → Arithmetic
-   `-eq` → Equal
-   `-gt` → Greater Than
-   `&&` → AND
-   `||` → OR
-   `echo` → Display output
-   `read` → Take input

------------------------------------------------------------------------

# MCQs

**Q1. Which command takes user input?**

A. `echo`\
B. `read`\
C. `pwd`\
D. `ls`

**Answer:** B

------------------------------------------------------------------------

**Q2. Which command displays output?**

A. `read`\
B. `echo`\
C. `cat`\
D. `touch`

**Answer:** B

------------------------------------------------------------------------

**Q3. Which operator performs addition?**

A. `+`\
B. `-`\
C. `*`\
D. `%`

**Answer:** A

------------------------------------------------------------------------

**Q4. Which operator means Greater Than?**

A. `-lt`\
B. `-eq`\
C. `-gt`\
D. `-le`

**Answer:** C

------------------------------------------------------------------------

**Q5. Which operator represents Logical AND?**

A. `||`\
B. `&&`\
C. `!`\
D. `==`

**Answer:** B

------------------------------------------------------------------------

# Interview / Viva Questions

1.  What is an assignment statement?
2.  Explain arithmetic operators.
3.  Explain relational operators.
4.  What is the use of `read`?
5.  What is the use of `echo`?

------------------------------------------------------------------------

# Command Cheat Sheet

  Command        Purpose
  -------------- ------------------------
  `NAME=value`   Assign variable
  `echo $VAR`    Display variable
  `read VAR`     Take input
  `$((A+B))`     Arithmetic calculation

------------------------------------------------------------------------

# Summary

-   Assignment statements store values in variables.
-   Arithmetic operators perform calculations.
-   Relational operators compare values.
-   Logical operators combine conditions.
-   `read` accepts input and `echo` displays output.

------------------------------------------------------------------------

# Related Topics

**Previous:** 29-Shell-and-Environment-Variables.md

**Next:** 31-IF-Statement.md
