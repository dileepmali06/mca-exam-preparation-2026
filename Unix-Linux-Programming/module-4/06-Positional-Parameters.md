# 4.2.3 Positional Parameters (`set`, `shift`)

> **Module:** Module 4 -- VI Editor and Shell Programming\
> **Section:** Shell Programming\
> **Topic:** Positional Parameters (`set`, `shift`)

------------------------------------------------------------------------

# Learning Objectives

-   Understand Positional Parameters.
-   Learn command-line arguments.
-   Use `$0`, `$1`, `$2`, `$#`, `$*`, `$@`.
-   Understand `set` and `shift`.

------------------------------------------------------------------------

# Introduction

Positional Parameters are variables that store command-line arguments
passed to a shell script.

------------------------------------------------------------------------

# Positional Parameters

  Parameter   Meaning
  ----------- ----------------------------------
  `$0`        Script name
  `$1`        First argument
  `$2`        Second argument
  `$3`        Third argument
  `$#`        Total number of arguments
  `$*`        All arguments as a single string
  `$@`        All arguments
  `$$`        Process ID (PID)
  `$?`        Exit status of last command

------------------------------------------------------------------------

# Example

Create a script:

``` bash
#!/bin/bash

echo "Script Name : $0"
echo "First Argument : $1"
echo "Second Argument : $2"
echo "Total Arguments : $#"
```

Run:

``` bash
./demo.sh Linux Ubuntu
```

Output:

``` text
Script Name : ./demo.sh
First Argument : Linux
Second Argument : Ubuntu
Total Arguments : 2
```

------------------------------------------------------------------------

# `set` Command

Assigns new positional parameters.

### Syntax

``` bash
set value1 value2 value3
```

### Example

``` bash
#!/bin/bash

set Java Python C

echo $1
echo $2
echo $3
```

Output:

``` text
Java
Python
C
```

------------------------------------------------------------------------

# `shift` Command

Moves positional parameters one position to the left.

### Before Shift

``` text
$1 = One
$2 = Two
$3 = Three
```

Command:

``` bash
shift
```

### After Shift

``` text
$1 = Two
$2 = Three
```

------------------------------------------------------------------------

# Practical

Create a script:

``` bash
vi demo.sh
```

Write:

``` bash
#!/bin/bash

echo "Script : $0"
echo "Arg1 : $1"
echo "Arg2 : $2"
echo "Count : $#"
```

Make executable:

``` bash
chmod +x demo.sh
```

Run:

``` bash
./demo.sh Linux Ubuntu
```

------------------------------------------------------------------------

# Quick Revision

-   `$0` → Script name
-   `$1` → First argument
-   `$2` → Second argument
-   `$#` → Total arguments
-   `$*` → All arguments
-   `$@` → All arguments
-   `set` → Assign parameters
-   `shift` → Shift parameters left

------------------------------------------------------------------------

# MCQs

**Q1. Which variable stores the script name?**

A. `$1`\
B. `$0`\
C. `$#`\
D. `$@`

**Answer:** B

------------------------------------------------------------------------

**Q2. Which variable stores the first argument?**

A. `$1`\
B. `$2`\
C. `$0`\
D. `$#`

**Answer:** A

------------------------------------------------------------------------

**Q3. Which variable stores the total number of arguments?**

A. `$*`\
B. `$@`\
C. `$#`\
D. `$0`

**Answer:** C

------------------------------------------------------------------------

**Q4. Which command shifts positional parameters?**

A. `set`\
B. `shift`\
C. `echo`\
D. `read`

**Answer:** B

------------------------------------------------------------------------

**Q5. Which command assigns new positional parameters?**

A. `read`\
B. `echo`\
C. `set`\
D. `pwd`

**Answer:** C

------------------------------------------------------------------------

# Interview / Viva Questions

1.  What are positional parameters?
2.  Explain `$0`, `$1` and `$#`.
3.  What is the use of `set`?
4.  What is the use of `shift`?
5.  Differentiate between `$*` and `$@`.

------------------------------------------------------------------------

# Command Cheat Sheet

  Command           Purpose
  ----------------- -------------------
  `./demo.sh A B`   Pass arguments
  `set A B C`       Assign parameters
  `shift`           Shift parameters

------------------------------------------------------------------------

# Summary

-   Positional parameters store command-line arguments.
-   `$0` stores the script name.
-   `$1`, `$2` store arguments.
-   `set` assigns parameters.
-   `shift` shifts parameters left.

------------------------------------------------------------------------

# Related Topics

**Previous:** 27-Shell-Scripts-and-Execution-Methods.md

**Next:** 29-Shell-and-Environment-Variables.md
