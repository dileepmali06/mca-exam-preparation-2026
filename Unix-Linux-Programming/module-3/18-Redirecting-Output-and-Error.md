# 3.4.3 Redirecting Output and Error

> **Module:** Module 3 -- Unix/Linux Commands\
> **Section:** Standard Input/Output\
> **Topic:** Redirecting Output and Error\
> **Subject:** Unix/Linux Programming

------------------------------------------------------------------------

# Learning Objectives

-   Understand Output Redirection.
-   Understand Error Redirection.
-   Learn the operators `>`, `>>`, `2>`, `2>>` and `&>`.
-   Perform practical examples in Linux.

------------------------------------------------------------------------

# Introduction

Linux allows the output and error messages of a command to be redirected
to files instead of displaying them on the terminal.

-   **stdout** → Standard Output
-   **stderr** → Standard Error

------------------------------------------------------------------------

# Standard Output (stdout)

Standard Output is the normal result produced by a command.

Example:

``` bash
ls
```

Redirect output:

``` bash
ls > files.txt
```

The output is stored in `files.txt`.

------------------------------------------------------------------------

# Standard Error (stderr)

Standard Error displays error messages.

Example:

``` bash
cat demo.txt
```

Redirect error:

``` bash
cat demo.txt 2> error.txt
```

The error message is stored in `error.txt`.

------------------------------------------------------------------------

# Output Redirection Operators

  Operator   Purpose
  ---------- --------------------------------
  `>`        Redirect output (Overwrite)
  `>>`       Append output
  `2>`       Redirect error (Overwrite)
  `2>>`      Append error
  `&>`       Redirect both output and error

------------------------------------------------------------------------

# Examples

Overwrite output:

``` bash
echo Linux > notes.txt
```

Append output:

``` bash
echo Ubuntu >> notes.txt
```

Redirect error:

``` bash
cat test.txt 2> error.txt
```

Append error:

``` bash
cat test.txt 2>> error.txt
```

Redirect output and error together:

``` bash
ls Documents missing_folder &> result.txt
```

------------------------------------------------------------------------

# Working

Without Redirection

``` text
Command
   │
 ┌─┴─┐
 ▼   ▼
stdout stderr
 │      │
 ▼      ▼
Screen Screen
```

With Redirection

``` text
stdout ───► output.txt
stderr ───► error.txt
```

------------------------------------------------------------------------

# Practical

Save output:

``` bash
ls > files.txt
```

Append output:

``` bash
echo Linux >> files.txt
```

Generate an error:

``` bash
cat abc.txt
```

Redirect error:

``` bash
cat abc.txt 2> error.txt
```

Append error:

``` bash
cat abc.txt 2>> error.txt
```

Redirect output and error:

``` bash
ls Documents abc &> result.txt
```

------------------------------------------------------------------------

# Difference

  Operator   Function
  ---------- -------------------------
  `>`        Overwrite output
  `>>`       Append output
  `2>`       Overwrite error
  `2>>`      Append error
  `&>`       Redirect output + error

------------------------------------------------------------------------

# Quick Revision

-   `>` → Output overwrite
-   `>>` → Output append
-   `2>` → Error overwrite
-   `2>>` → Error append
-   `&>` → Output + Error
-   stdout → Standard Output
-   stderr → Standard Error

------------------------------------------------------------------------

# MCQs

**Q1. Which operator redirects normal output?**

A. `<`\
B. `>`\
C. `2>`\
D. `|`

**Answer:** B

------------------------------------------------------------------------

**Q2. Which operator appends output?**

A. `>`\
B. `>>`\
C. `2>`\
D. `<`

**Answer:** B

------------------------------------------------------------------------

**Q3. Which operator redirects error messages?**

A. `2>`\
B. `>>`\
C. `|`\
D. `&`

**Answer:** A

------------------------------------------------------------------------

**Q4. Which operator redirects both output and error?**

A. `2>>`\
B. `&>`\
C. `>`\
D. `<`

**Answer:** B

------------------------------------------------------------------------

**Q5. What does stderr represent?**

A. Standard Input\
B. Standard Output\
C. Standard Error\
D. Standard Command

**Answer:** C

------------------------------------------------------------------------

# Interview / Viva Questions

1.  What is Output Redirection?
2.  What is stderr?
3.  Explain `>` and `>>`.
4.  Explain `2>` and `2>>`.
5.  How do you redirect output and error together?

------------------------------------------------------------------------

# Command Cheat Sheet

  Command                            Purpose
  ---------------------------------- -----------------------
  `ls > files.txt`                   Save output
  `echo Linux >> notes.txt`          Append output
  `cat demo.txt 2> error.txt`        Save error
  `cat demo.txt 2>> error.txt`       Append error
  `ls Documents abc &> result.txt`   Save output and error

------------------------------------------------------------------------

# Summary

-   `>` redirects output to a file.
-   `>>` appends output.
-   `2>` redirects error messages.
-   `2>>` appends error messages.
-   `&>` redirects both output and error to the same file.

------------------------------------------------------------------------

# Related Topics

**Previous:** 17-Redirecting-Input.md

**Next:** Module 3.5 -- Unix Permissions
