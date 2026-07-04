# 3.3.6 expr, bc and exit Commands

> **Module:** Module 3 -- Unix/Linux Commands\
> **Topic:** expr, bc and exit Commands\
> **Subject:** Unix/Linux Programming

------------------------------------------------------------------------

# Learning Objectives

-   Understand `expr`, `bc` and `exit` commands.
-   Perform integer and decimal calculations.
-   Exit the Linux shell correctly.

------------------------------------------------------------------------

# Introduction

Linux provides commands to perform arithmetic operations and manage
shell sessions.

-   **expr** → Integer calculations
-   **bc** → Advanced calculator
-   **exit** → Exit the current shell

------------------------------------------------------------------------

# expr Command

## Definition

The **expr (Expression)** command performs integer arithmetic.

### Syntax

``` bash
expr expression
```

### Examples

Addition

``` bash
expr 10 + 5
```

Subtraction

``` bash
expr 20 - 8
```

Multiplication

``` bash
expr 6 \* 5
```

Division

``` bash
expr 20 / 4
```

Modulus

``` bash
expr 17 % 5
```

> **Note:** Spaces between operands and operators are mandatory.

------------------------------------------------------------------------

# bc Command

## Definition

The **bc (Basic Calculator)** command performs integer and
floating-point calculations.

### Syntax

``` bash
bc
```

### Examples

Addition

``` text
10 + 20
```

Division

``` text
10 / 3
```

Decimal Result

``` text
scale=2
10 / 3
```

Square Root

``` text
sqrt(25)
```

Power

``` text
2^5
```

Exit from bc

``` text
quit
```

------------------------------------------------------------------------

# exit Command

## Definition

The **exit** command terminates the current shell session.

### Syntax

``` bash
exit
```

### Uses

-   Exit Terminal
-   Logout from Shell
-   Exit SSH Session
-   End Shell Script

------------------------------------------------------------------------

# Difference

  Command   Purpose
  --------- --------------------------------
  `expr`    Integer arithmetic
  `bc`      Integer & decimal calculations
  `exit`    Close current shell

------------------------------------------------------------------------

# Practical

Run integer calculations:

``` bash
expr 20 + 10
expr 20 - 10
expr 20 \* 5
expr 20 / 4
expr 20 % 3
```

Open calculator:

``` bash
bc
```

Run:

``` text
10 + 20
scale=2
10 / 3
sqrt(64)
2^8
quit
```

Exit terminal:

``` bash
exit
```

------------------------------------------------------------------------

# Quick Revision

-   `expr` → Integer calculations
-   `bc` → Advanced calculator
-   `scale` → Decimal precision
-   `sqrt()` → Square root
-   `^` → Power
-   `exit` → Close shell

------------------------------------------------------------------------

# MCQs

**Q1. Which command performs integer arithmetic?**

A. bc\
B. expr\
C. grep\
D. sort

**Answer:** B

------------------------------------------------------------------------

**Q2. Which command supports decimal calculations?**

A. expr\
B. bc\
C. wc\
D. cut

**Answer:** B

------------------------------------------------------------------------

**Q3. Which keyword sets decimal precision in bc?**

A. float\
B. scale\
C. decimal\
D. precision

**Answer:** B

------------------------------------------------------------------------

**Q4. Which command closes the current shell?**

A. logout\
B. quit\
C. exit\
D. leave

**Answer:** C

------------------------------------------------------------------------

**Q5. Which operator performs modulus in expr?**

A. \*\
B. /\
C. %\
D. \^

**Answer:** C

------------------------------------------------------------------------

# Interview / Viva Questions

1.  What is the expr command?
2.  Explain the bc command.
3.  What is the purpose of `scale` in bc?
4.  What is the exit command?
5.  Differentiate between expr and bc.

------------------------------------------------------------------------

# Command Cheat Sheet

  Command         Purpose
  --------------- -------------------
  `expr 5 + 3`    Addition
  `expr 6 \* 5`   Multiplication
  `expr 20 % 3`   Modulus
  `bc`            Open calculator
  `scale=2`       Decimal precision
  `sqrt(25)`      Square root
  `2^5`           Power
  `exit`          Exit shell

------------------------------------------------------------------------

# Summary

-   `expr` performs integer arithmetic.
-   `bc` performs advanced mathematical calculations including decimals.
-   `exit` closes the current shell session.
-   These commands are commonly used in shell scripting and Linux
    administration.

------------------------------------------------------------------------

# Related Topics

**Previous:** 14-CMP-COMM-DIFF-UNIQ.md

**Next:** Module 4
