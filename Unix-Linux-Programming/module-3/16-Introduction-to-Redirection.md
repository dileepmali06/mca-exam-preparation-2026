# 3.4.1 Introduction to Redirection

> **Module:** Module 3 -- Unix/Linux Commands\
> **Section:** Standard Input/Output\
> **Topic:** Introduction to Redirection\
> **Subject:** Unix/Linux Programming

------------------------------------------------------------------------

# Learning Objectives

-   Understand Redirection.
-   Learn Standard Input, Output and Error.
-   Understand common redirection operators.
-   Perform basic redirection in Linux.

------------------------------------------------------------------------

# Introduction

Redirection is used to change the default source of input or destination
of output.

Normally:

-   **Input** comes from the keyboard.
-   **Output** is displayed on the terminal.
-   **Errors** are also displayed on the terminal.

Using redirection, input, output or errors can be redirected to files.

------------------------------------------------------------------------

# What is Redirection?

## Definition

**Redirection** is the process of changing the default input or output
location of a Linux command.

------------------------------------------------------------------------

# Standard Streams

  Stream   Name              Default Source/Destination
  -------- ----------------- ----------------------------
  stdin    Standard Input    Keyboard
  stdout   Standard Output   Terminal Screen
  stderr   Standard Error    Terminal Screen

------------------------------------------------------------------------

# Types of Redirection

  Operator   Purpose
  ---------- -----------------------------
  `>`        Redirect output (Overwrite)
  `>>`       Append output
  `<`        Redirect input
  `2>`       Redirect error
  `2>>`      Append error
  `&>`       Redirect output and error

------------------------------------------------------------------------

# Examples

## Output Redirection

``` bash
ls > files.txt
```

Saves command output into `files.txt`.

------------------------------------------------------------------------

## Append Output

``` bash
echo Linux >> notes.txt
```

Appends data to an existing file.

------------------------------------------------------------------------

## Input Redirection

``` bash
sort < names.txt
```

Reads input from `names.txt`.

------------------------------------------------------------------------

## Error Redirection

``` bash
cat demo.txt 2> error.txt
```

Stores error messages in `error.txt`.

------------------------------------------------------------------------

# Working of Redirection

``` text
Keyboard (stdin)
      │
      ▼
   Command
   /     \
stdout   stderr
  |         |
Screen   Screen
```

Using redirection:

``` text
stdout → output.txt
stderr → error.txt
```

------------------------------------------------------------------------

# Practical

Display files:

``` bash
ls
```

Save output:

``` bash
ls > files.txt
```

View file:

``` bash
cat files.txt
```

Append output:

``` bash
echo Ubuntu >> files.txt
```

Generate error:

``` bash
cat abc.txt
```

Redirect error:

``` bash
cat abc.txt 2> error.txt
```

------------------------------------------------------------------------

# Quick Revision

-   Redirection → Change input/output location.
-   stdin → Keyboard.
-   stdout → Terminal.
-   stderr → Error output.
-   `>` → Overwrite output.
-   `>>` → Append output.
-   `<` → Input redirection.
-   `2>` → Error redirection.

------------------------------------------------------------------------

# MCQs

**Q1. What is Redirection?**

A. Copying files\
B. Changing input/output destination\
C. Creating folders\
D. Deleting files

**Answer:** B

------------------------------------------------------------------------

**Q2. Which operator redirects output?**

A. `<`\
B. `>`\
C. `|`\
D. `&`

**Answer:** B

------------------------------------------------------------------------

**Q3. Which operator appends output?**

A. `>>`\
B. `>`\
C. `<`\
D. `2>`

**Answer:** A

------------------------------------------------------------------------

**Q4. What is the default Standard Input?**

A. File\
B. Printer\
C. Keyboard\
D. Screen

**Answer:** C

------------------------------------------------------------------------

**Q5. Which operator redirects errors?**

A. `>`\
B. `<`\
C. `2>`\
D. `>>`

**Answer:** C

------------------------------------------------------------------------

# Interview / Viva Questions

1.  What is Redirection?
2.  What is stdin?
3.  What is stdout?
4.  What is stderr?
5.  Explain the `>` and `>>` operators.

------------------------------------------------------------------------

# Command Cheat Sheet

  Command                       Purpose
  ----------------------------- ---------------
  `ls > files.txt`              Save output
  `echo Linux >> notes.txt`     Append output
  `sort < names.txt`            Read input
  `cat demo.txt 2> error.txt`   Save errors

------------------------------------------------------------------------

# Summary

-   Redirection changes the default input or output destination.
-   Linux uses three standard streams: stdin, stdout and stderr.
-   Redirection operators help save output, provide input and store
    errors.

------------------------------------------------------------------------

# Related Topics

**Previous:** 15-expr-bc-exit.md

**Next:** 16-Redirecting-Input.md
