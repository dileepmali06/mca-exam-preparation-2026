# 1.1.6 Types of Shell

> **Module:** Module 1 - Introduction
>
> **Topic:** 1.1.6 Types of Shell
>
> **Subject:** Unix/Linux Programming
>
> **Level:** Beginner → Advanced
>
> **University:** MCA Semester III
>
> **Based On:** Amity University PDF
>
> **Author:** Dilip
>
> **Maintained By:** Dilip

---

# Learning Objectives

After studying this topic, you will be able to:

- Understand what a Shell is.
- Explain why a Shell is required.
- Understand the relationship between User, Shell, and Kernel.
- Identify different types of UNIX Shells.
- Compare Bourne Shell, Bash, Korn Shell, C Shell, POSIX Shell, and tcsh.
- Execute basic shell-related commands in Linux.

---

# Introduction

A **Shell** is a command interpreter that acts as an interface between the **User** and the **Kernel**.

Whenever a user enters a command, the Shell reads the command, checks it, sends it to the Kernel for execution, and finally displays the output.

Without a Shell, users cannot directly communicate with the Kernel.

---

# Why Do We Need a Shell?

The Kernel understands only low-level system instructions.

Users cannot communicate directly with the Kernel.

Therefore, a Shell is required to translate user commands into instructions that the Kernel can execute.

---

# Shell Architecture

```text
User
   │
   ▼
Shell
   │
   ▼
Kernel
   │
   ▼
Hardware
```

---

# Working of Shell

Suppose the user executes:

```bash
ls
```

Execution Flow

```text
User

↓

Shell

↓

Kernel

↓

File System

↓

Output

↓

Shell

↓

User
```

---

# Functions of Shell

The Shell performs the following functions:

- Reads user commands.
- Interprets commands.
- Executes programs.
- Starts applications.
- Runs shell scripts.
- Manages shell variables.
- Supports Input/Output Redirection.
- Supports Pipes.
- Provides command history.
- Displays command output.

---

# Shell Prompt

When the Terminal is opened, a prompt appears.

Example

```text
dilip@ubuntu:~$
```

The symbol:

```text
$
```

indicates that the Shell is ready to accept commands.

---

# Types of UNIX Shell

The common UNIX Shells are:

1. Bourne Shell (sh)
2. Bourne Again Shell (bash)
3. Korn Shell (ksh)
4. C Shell (csh)
5. TENEX C Shell (tcsh)
6. POSIX Shell (sh)

---

# 1. Bourne Shell (sh)

## Introduction

The Bourne Shell was developed by **Stephen Bourne** at Bell Labs.

It became the first widely used UNIX Shell and laid the foundation for Shell Programming.

### Location

```text
/bin/sh
```

### Features

- Simple
- Fast
- Stable
- Script Support
- Easy to Learn

### Limitations

- No Command History
- No Auto Completion
- Limited Interactive Features

### Best Use

- Shell Scripting
- System Administration

---

# 2. Bourne Again Shell (bash)

## Introduction

Bash stands for:

> **Bourne Again Shell**

It was developed by the **GNU Project**.

Bash is the default shell in most Linux distributions.

Examples:

- Ubuntu
- Debian
- Fedora
- CentOS
- Arch Linux

### Features

- Command History
- Auto Completion (Tab)
- Aliases
- Variables
- Shell Scripting
- Job Control
- Better Error Handling

### Advantages

- User Friendly
- Powerful
- Highly Customizable
- Most Popular Shell

---

# 3. Korn Shell (ksh)

## Introduction

The Korn Shell was developed by **David Korn**.

It combines the scripting power of the Bourne Shell with the interactive features of the C Shell.

### Features

- Command History
- Aliases
- Arrays
- Integer Arithmetic
- Better Performance
- Interactive Features

### Best Use

- Enterprise UNIX Systems
- Advanced Shell Scripting

---

# 4. C Shell (csh)

## Introduction

The C Shell was developed by **Bill Joy**.

Its syntax is similar to the C Programming Language.

### Features

- Command History
- Aliases
- Job Control
- Interactive Commands
- Filename Completion

### Best Use

- Interactive Usage
- C Programmers

---

# 5. TENEX C Shell (tcsh)

## Introduction

The TENEX C Shell (tcsh) is an improved version of the C Shell.

### Features

- Command History
- Auto Completion
- Command Line Editing
- Better User Interface

### Advantages

- More Interactive
- Easy Editing
- Improved Productivity

---

# 6. POSIX Shell

## Introduction

POSIX Shell follows the POSIX standard.

POSIX stands for:

**Portable Operating System Interface**

Its purpose is to make shell scripts portable across different UNIX systems.

### Features

- Standardized Syntax
- Portable Scripts
- Cross-platform Compatibility

---

# Comparison of Different Shells

| Shell | Developer | Best For |
|--------|-----------|----------|
| Bourne Shell (sh) | Stephen Bourne | Shell Scripting |
| Bash | GNU Project | Default Linux Shell |
| Korn Shell (ksh) | David Korn | Enterprise Scripting |
| C Shell (csh) | Bill Joy | Interactive Usage |
| tcsh | Improved C Shell | Better Editing |
| POSIX Shell | POSIX Standard | Portability |

---

# Shell vs Kernel

| Shell | Kernel |
|--------|---------|
| Interface between User and Kernel | Core of Operating System |
| Executes Commands | Manages Hardware |
| Replaceable | Essential Component |
| User Level | System Level |

---

# Practical (Ubuntu VirtualBox)

Open Terminal

```bash
Ctrl + Alt + T
```

---

## Display Current Shell

```bash
echo $SHELL
```

---

## Display Bash Version

```bash
bash --version
```

---

## Display Available Shells

```bash
cat /etc/shells
```

---

## Display Current Shell Name

```bash
echo $0
```

---

# Expected Output

```text
/bin/bash
```

or

```text
GNU bash, version 5.x.x
```

---

# Common Beginner Mistakes

### Mistake 1

Thinking Shell is the Operating System.

Correct:

Shell is only an interface.

---

### Mistake 2

Thinking Kernel and Shell are the same.

Correct:

Kernel manages hardware.

Shell executes user commands.

---

### Mistake 3

Thinking Bash is the only Shell.

Correct:

UNIX supports multiple Shells.

---

# Real World Applications

## Software Developers

- Shell Scripting
- Automation
- Compilation

---

## Backend Developers

- Server Management
- Deployment Scripts
- Environment Configuration

---

## DevOps Engineers

- Bash Automation
- Docker
- Kubernetes
- Jenkins
- CI/CD Pipelines

---

## Cloud Engineers

Most Linux cloud servers use **Bash** for:

- Server Configuration
- Automation
- Monitoring
- Deployment

---

# Advantages of Shell

- Easy Command Execution
- Supports Automation
- Fast Processing
- Powerful Scripting
- Interactive Environment
- Supports Redirection and Pipes

---

# Limitations

- Command-line learning curve.
- Different shells have different syntax.
- Beginners may find scripting difficult initially.

---

# Quick Revision

- Shell is a Command Interpreter.
- Shell acts as an interface between User and Kernel.
- Bourne Shell is the first popular UNIX Shell.
- Bash is the default shell in Linux.
- Korn Shell combines Bourne and C Shell features.
- C Shell provides interactive features.
- tcsh is an improved C Shell.
- POSIX Shell provides portability.

---

# Important Keywords

- Shell
- Command Interpreter
- Bash
- Bourne Shell
- Korn Shell
- C Shell
- tcsh
- POSIX
- Shell Prompt
- Shell Scripting

---

# Frequently Asked Questions

## Q1. What is a Shell?

A Shell is a command interpreter that acts as an interface between the user and the Kernel.

---

## Q2. Which is the default shell in Linux?

Bash (Bourne Again Shell).

---

## Q3. Who developed the Bourne Shell?

Stephen Bourne.

---

## Q4. Who developed the Korn Shell?

David Korn.

---

## Q5. What is the full form of Bash?

Bourne Again Shell.

---

# MCQ Questions

## Q1.

Shell is a:

- A. Hardware
- B. Command Interpreter
- C. CPU
- D. RAM

**Answer:** B

---

## Q2.

Which is the default Linux Shell?

- A. sh
- B. bash
- C. csh
- D. ksh

**Answer:** B

---

## Q3.

Who developed the Bourne Shell?

- A. Bill Joy
- B. Stephen Bourne
- C. David Korn
- D. Richard Stallman

**Answer:** B

---

## Q4.

Who developed the C Shell?

- A. Bill Joy
- B. Stephen Bourne
- C. David Korn
- D. GNU Project

**Answer:** A

---

## Q5.

Bash stands for:

- A. Bourne Again Shell
- B. Basic Shell
- C. Binary Shell
- D. Bourne Advanced Shell

**Answer:** A

---

## Q6.

Which shell is based on the POSIX standard?

- A. Bash
- B. POSIX Shell
- C. C Shell
- D. Korn Shell

**Answer:** B

---

## Q7.

Which command displays the current shell?

- A. pwd
- B. echo $SHELL
- C. uname
- D. ls

**Answer:** B

---

## Q8.

Which command displays all available shells?

- A. cat /etc/shells
- B. ls
- C. pwd
- D. whoami

**Answer:** A

---

# 2 Marks Questions

1. Define Shell.
2. What is Bash?
3. What is Shell Prompt?
4. What is POSIX Shell?
5. Name any four UNIX Shells.

---

# 5 Marks Questions

1. Explain different types of UNIX Shells.
2. Explain the functions of Shell.
3. Differentiate between Shell and Kernel.
4. Explain Bash and its features.

---

# Long Answer Questions

1. Explain different types of UNIX Shells with suitable examples.
2. Explain the working of Shell with a neat diagram.
3. Compare Bourne Shell, Bash, Korn Shell, and C Shell.

---

# Viva Questions

- What is a Shell?
- Why is Bash the default shell in Linux?
- What is the difference between Shell and Kernel?
- Which Shell are you using in Ubuntu?
- What is Shell Prompt?

---

# Command Cheat Sheet

| Command | Purpose |
|----------|---------|
| `echo $SHELL` | Display Current Shell |
| `bash --version` | Display Bash Version |
| `cat /etc/shells` | Display Available Shells |
| `echo $0` | Display Current Shell Name |

---

# Previous Year Exam Focus

⭐ Very Important

- Types of Shell
- Shell vs Kernel
- Bash Features
- Bourne Shell
- Shell Diagram

---

# Summary

- Shell is the interface between the User and the Kernel.
- It interprets commands and sends them to the Kernel.
- UNIX supports multiple Shells such as Bourne, Bash, Korn, C Shell, tcsh, and POSIX Shell.
- Bash is the most widely used shell in modern Linux systems.
- Shell scripting is widely used for automation, DevOps, and server administration.

---

# Related Topics

⬅️ Previous Topic

**1.1.5 UNIX Layered Architecture**

➡️ Next Topic

**1.2.1 UNIX File System**