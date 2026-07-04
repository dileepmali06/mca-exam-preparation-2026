# 4.2.2 Shell Scripts and Execution Methods

> **Module:** Module 4 -- VI Editor and Shell Programming\
> **Section:** Shell Programming\
> **Topic:** Shell Scripts and Execution Methods

------------------------------------------------------------------------

# Learning Objectives

-   Learn different methods to execute shell scripts.
-   Understand `sh`, `bash`, `./` and `source`.
-   Compare execution methods.
-   Execute scripts correctly in Linux.

------------------------------------------------------------------------

# Introduction

A shell script can be executed in multiple ways depending on the
requirement. The most common methods are:

-   `sh`
-   `bash`
-   `./`
-   `source`

------------------------------------------------------------------------

# Method 1 -- Using `sh`

### Syntax

``` bash
sh script.sh
```

### Example

``` bash
sh hello.sh
```

### Features

-   Uses the **sh** shell.
-   Execute permission is **not required**.
-   Suitable for simple scripts.

------------------------------------------------------------------------

# Method 2 -- Using `bash`

### Syntax

``` bash
bash script.sh
```

### Example

``` bash
bash hello.sh
```

### Features

-   Uses the **Bash** shell.
-   Execute permission is **not required**.
-   Supports Bash-specific features.

------------------------------------------------------------------------

# Method 3 -- Using `./`

### Syntax

``` bash
./script.sh
```

### Example

``` bash
./hello.sh
```

### Requirements

Give execute permission:

``` bash
chmod +x hello.sh
```

Script should start with:

``` bash
#!/bin/bash
```

------------------------------------------------------------------------

# Method 4 -- Using `source`

### Syntax

``` bash
source script.sh
```

or

``` bash
. script.sh
```

### Example

``` bash
source hello.sh
```

### Features

-   Executes in the **current shell**.
-   Does not create a new shell.
-   Useful for loading variables and functions.

------------------------------------------------------------------------

# Comparison

  Method               Execute Permission   New Shell   Common Use
  -------------------- -------------------- ----------- ----------------
  `sh script.sh`       No                   Yes         Simple scripts
  `bash script.sh`     No                   Yes         Bash scripts
  `./script.sh`        Yes                  Yes         Recommended
  `source script.sh`   No                   No          Load variables

------------------------------------------------------------------------

# Practical

Create a script:

``` bash
vi hello.sh
```

Run using `sh`:

``` bash
sh hello.sh
```

Run using `bash`:

``` bash
bash hello.sh
```

Make executable:

``` bash
chmod +x hello.sh
```

Run directly:

``` bash
./hello.sh
```

Run in current shell:

``` bash
source hello.sh
```

------------------------------------------------------------------------

# Quick Revision

-   `sh script.sh` → Run with sh
-   `bash script.sh` → Run with Bash
-   `./script.sh` → Direct execution
-   `source script.sh` → Current shell
-   `chmod +x` → Make executable
-   `#!/bin/bash` → Bash interpreter

------------------------------------------------------------------------

# MCQs

**Q1. Which command executes a script using Bash?**

A. `sh script.sh`\
B. `bash script.sh`\
C. `source script.sh`\
D. `chmod script.sh`

**Answer:** B

------------------------------------------------------------------------

**Q2. Which method requires execute permission?**

A. `sh script.sh`\
B. `bash script.sh`\
C. `./script.sh`\
D. `source script.sh`

**Answer:** C

------------------------------------------------------------------------

**Q3. Which command runs a script in the current shell?**

A. `bash`\
B. `sh`\
C. `source`\
D. `./`

**Answer:** C

------------------------------------------------------------------------

**Q4. Which command gives execute permission?**

A. `chmod +x hello.sh`\
B. `pwd`\
C. `ls`\
D. `cat`

**Answer:** A

------------------------------------------------------------------------

**Q5. Which execution method is generally recommended?**

A. `sh`\
B. `bash`\
C. `./script.sh`\
D. `source`

**Answer:** C

------------------------------------------------------------------------

# Interview / Viva Questions

1.  What are the different methods to execute a shell script?
2.  Explain `sh` and `bash`.
3.  Why is `chmod +x` required?
4.  What is the use of `source`?
5.  Differentiate between `./script.sh` and `source script.sh`.

------------------------------------------------------------------------

# Command Cheat Sheet

  Command                Purpose
  ---------------------- --------------------------
  `sh script.sh`         Run using sh
  `bash script.sh`       Run using Bash
  `chmod +x script.sh`   Make executable
  `./script.sh`          Execute directly
  `source script.sh`     Execute in current shell

------------------------------------------------------------------------

# Summary

-   Shell scripts can be executed using `sh`, `bash`, `./` or `source`.
-   `./script.sh` requires execute permission.
-   `source` runs the script in the current shell.
-   Choose the execution method based on your requirement.

------------------------------------------------------------------------

# Related Topics

**Previous:** 26-Shell-Script-Introduction.md

**Next:** 28-Positional-Parameters.md
