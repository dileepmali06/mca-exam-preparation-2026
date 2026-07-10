# 4.2.1 Shell Script Introduction

> **Module:** Module 4 -- VI Editor and Shell Programming\
> **Section:** Shell Programming\
> **Topic:** Shell Script Introduction

------------------------------------------------------------------------

# Learning Objectives

-   Understand Shell and Shell Script.
-   Learn the purpose of Shell Scripting.
-   Create and execute a basic shell script.
-   Understand the basic structure of a shell script.

------------------------------------------------------------------------

# Introduction

A **Shell** is a command interpreter that acts as an interface between
the user and the Linux operating system.

A **Shell Script** is a text file containing a sequence of Linux
commands that are executed automatically.

------------------------------------------------------------------------

# What is a Shell?

A Shell accepts commands from the user and sends them to the Linux
Kernel for execution.

``` text
User
  |
Shell
  |
Kernel
  |
Hardware
```

------------------------------------------------------------------------

# What is a Shell Script?

A Shell Script is a file that contains multiple shell commands to
automate tasks.

------------------------------------------------------------------------

# Advantages of Shell Scripting

-   Automates repetitive tasks
-   Saves time
-   Reduces manual work
-   Easy to write and maintain
-   Useful for system administration

------------------------------------------------------------------------

# Basic Structure

Every shell script begins with the shebang line.

``` bash
#!/bin/bash

echo "Hello Linux"

pwd

date
```

------------------------------------------------------------------------

# Shebang

``` bash
#!/bin/bash
```

The shebang tells Linux to execute the script using the **Bash Shell**.

------------------------------------------------------------------------

# Create a Script

``` bash
vi hello.sh
```

Write:

``` bash
#!/bin/bash

echo "Welcome to Shell Programming"

pwd

date
```

Save the file:

``` text
Esc
:wq
```

------------------------------------------------------------------------

# Make Script Executable

``` bash
chmod +x hello.sh
```

``` bash
chmod +x hello.sh // please understand
```

------------------------------------------------------------------------

# Execute Script

``` bash
./hello.sh
```

------------------------------------------------------------------------

# Common Script Extension

``` text
.sh
```

Examples:

``` text
hello.sh
backup.sh
install.sh
```

------------------------------------------------------------------------

# Practical

Create script:

``` bash
vi hello.sh
```

Give execute permission:

``` bash
chmod +x hello.sh
```

Run:

``` bash
./hello.sh
```

------------------------------------------------------------------------

# Quick Revision

-   Shell → Command Interpreter
-   Shell Script → Collection of commands
-   `#!/bin/bash` → Shebang
-   `.sh` → Common extension
-   `chmod +x` → Execute permission
-   `./script.sh` → Run script

------------------------------------------------------------------------

# MCQs

**Q1. What is a Shell Script?**

A. Image file

B. Text file containing shell commands

C. Audio file

D. Database

**Answer:** B

------------------------------------------------------------------------

**Q2. Which line is called the Shebang?**

A. `echo`

B. `#!/bin/bash`

C. `pwd`

D. `ls`

**Answer:** B

------------------------------------------------------------------------

**Q3. Which command gives execute permission?**

A. `chmod +x hello.sh`

B. `pwd`

C. `cat`

D. `touch`

**Answer:** A

------------------------------------------------------------------------

**Q4. Which command executes a script?**

A. `./hello.sh`

B. `vi hello.sh`

C. `ls`

D. `pwd`

**Answer:** A

------------------------------------------------------------------------

**Q5. Which shell is used in the example?**

A. Fish

B. Zsh

C. Bash

D. C Shell

**Answer:** C

------------------------------------------------------------------------

# Interview / Viva Questions

1.  What is a Shell?
2.  What is a Shell Script?
3.  What is the purpose of `#!/bin/bash`?
4.  Why is `chmod +x` required?
5.  What are the advantages of Shell Scripting?

------------------------------------------------------------------------

# Command Cheat Sheet

  Command               Purpose
  --------------------- -----------------
  `vi hello.sh`         Create script
  `chmod +x hello.sh`   Make executable
  `./hello.sh`          Execute script

------------------------------------------------------------------------

# Summary

-   A Shell Script automates Linux commands.
-   `#!/bin/bash` specifies the Bash interpreter.
-   Use `chmod +x` before executing a script.
-   Shell scripts are widely used for automation and system
    administration.

------------------------------------------------------------------------

# Related Topics

**Previous:** 25-VI-Cursor-and-Text-Commands.md

**Next:** 27-Shell-Scripts-and-Execution-Methods.md
