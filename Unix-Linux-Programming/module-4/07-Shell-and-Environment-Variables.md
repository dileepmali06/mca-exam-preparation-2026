# 4.2.4 Shell Variables & Environment Variables

> **Module:** Module 4 -- VI Editor and Shell Programming\
> **Section:** Shell Programming\
> **Topic:** Shell Variables & Environment Variables

------------------------------------------------------------------------

# Learning Objectives

-   Understand Shell Variables.
-   Understand Environment Variables.
-   Learn `export` and `unset`.
-   Display predefined environment variables.

------------------------------------------------------------------------

# Introduction

A **Variable** stores data that can be used later in a shell script.

Linux mainly provides:

-   Shell Variables (Local Variables)
-   Environment Variables

------------------------------------------------------------------------

# Shell Variable

A Shell Variable is available only in the current shell.

### Syntax

``` bash
VARIABLE=value
```

### Example

``` bash
NAME="Dilip"
echo $NAME
```

------------------------------------------------------------------------

# Variable Naming Rules

-   Start with a letter or `_`
-   No spaces around `=`
-   Case-sensitive
-   Cannot start with a number

------------------------------------------------------------------------

# Environment Variable

Environment Variables are inherited by child processes.

Common variables:

  Variable      Purpose
  ------------- ---------------------------
  `$HOME`       Home directory
  `$USER`       Current user
  `$PATH`       Command search path
  `$PWD`        Present working directory
  `$SHELL`      Current shell
  `$HOSTNAME`   System hostname

View all:

``` bash
printenv
```

or

``` bash
env
```

------------------------------------------------------------------------

# `export` Command

Converts a shell variable into an environment variable.

``` bash
NAME="Dilip"
export NAME
```

------------------------------------------------------------------------

# `unset` Command

Removes a variable.

``` bash
unset NAME
```

------------------------------------------------------------------------

# Practical

Create variables:

``` bash
NAME="Dilip"
AGE=21
```

Display:

``` bash
echo $NAME
echo $AGE
```

Show environment variables:

``` bash
echo $HOME
echo $USER
printenv
```

Export:

``` bash
export NAME
```

Remove variable:

``` bash
unset NAME
```

------------------------------------------------------------------------

# Difference

  Shell Variable           Environment Variable
  ------------------------ ------------------------------
  Local to current shell   Available to child processes
  Not inherited            Inherited
  Normal assignment        Created using `export`

------------------------------------------------------------------------

# Quick Revision

-   `NAME="Dilip"` → Create variable
-   `echo $NAME` → Display variable
-   `export NAME` → Environment variable
-   `unset NAME` → Delete variable
-   `printenv` → Show environment variables

------------------------------------------------------------------------

# MCQs

**Q1. Which command displays all environment variables?**

A. `ls`\
B. `printenv`\
C. `pwd`\
D. `cat`

**Answer:** B

------------------------------------------------------------------------

**Q2. Which command converts a shell variable into an environment
variable?**

A. `unset`\
B. `echo`\
C. `export`\
D. `set`

**Answer:** C

------------------------------------------------------------------------

**Q3. Which command removes a variable?**

A. `unset`\
B. `export`\
C. `echo`\
D. `pwd`

**Answer:** A

------------------------------------------------------------------------

**Q4. Which variable stores the user's home directory?**

A. `$PATH`\
B. `$HOME`\
C. `$PWD`\
D. `$USER`

**Answer:** B

------------------------------------------------------------------------

**Q5. Which symbol is used to access a variable?**

A. `#`\
B. `@`\
C. `$`\
D. `%`

**Answer:** C

------------------------------------------------------------------------

# Interview / Viva Questions

1.  What is a Shell Variable?
2.  What is an Environment Variable?
3.  Explain `export`.
4.  Explain `unset`.
5.  Differentiate between Shell and Environment Variables.

------------------------------------------------------------------------

# Command Cheat Sheet

  Command          Purpose
  ---------------- ----------------------------
  `NAME="Dilip"`   Create variable
  `echo $NAME`     Display variable
  `export NAME`    Export variable
  `unset NAME`     Remove variable
  `printenv`       Show environment variables

------------------------------------------------------------------------

# Summary

-   Shell Variables are local to the current shell.
-   Environment Variables are inherited by child processes.
-   `export` makes a variable available to child shells.
-   `unset` removes a variable.
-   `printenv` displays environment variables.

------------------------------------------------------------------------

# Related Topics

**Previous:** 28-Positional-Parameters.md

**Next:** 30-Operators-Read-and-Echo.md
