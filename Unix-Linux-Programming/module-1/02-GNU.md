# 1.1.2 GNU (GNU's Not UNIX)

---

# Introduction

GNU is a free software project started by **Richard Stallman** with the goal of developing a **free UNIX-compatible operating system**.

The GNU Project allows users to freely use, study, modify, and distribute software.

GNU plays a very important role in modern Linux operating systems because many Linux distributions use GNU tools together with the Linux Kernel.

---

# What is GNU?

## Definition

GNU is a free software project whose objective is to develop a completely free UNIX-compatible operating system.

GNU provides various software tools, utilities, compilers, libraries, and shell programs that are widely used in Linux systems.

> GNU Full Form:
>
> **GNU's Not UNIX**

It is called a **recursive acronym** because the word GNU appears inside its own full form.

---

# History of GNU

The GNU Project was started by **Richard Stallman** while working at the **MIT Artificial Intelligence Laboratory**.

Important Timeline:

| Year | Event |
|------|-------|
| 1983 | GNU Project announced |
| 1984 | Richard Stallman left MIT to work full-time on GNU |
| 1985 | GNU Manifesto published |
| 1985 | Free Software Foundation (FSF) established |

---

# Why GNU Was Created?

Before GNU, most operating systems were proprietary.

This created several problems:

- Users could not view the source code.
- Users could not modify software.
- Users could not distribute software.
- Software freedom was restricted.

Richard Stallman wanted software to be available for everyone without these restrictions.

---

# Objectives of GNU Project

The main objectives of GNU are:

- Develop a free operating system.
- Make software available with source code.
- Allow users to modify software.
- Allow users to share software.
- Create software compatible with UNIX.

---

# GNU Philosophy

GNU follows the philosophy of **Free Software**.

According to Richard Stallman, every user should have the following freedoms.

## Freedom 0

Run the software for any purpose.

---

## Freedom 1

Study how the software works.

Modify the source code according to your needs.

---

## Freedom 2

Share copies of the software with others.

---

## Freedom 3

Improve the software and distribute the modified version.

---

# GNU Manifesto

The GNU Manifesto was published by Richard Stallman in **1985**.

It explains:

- Why free software is important.
- Why users should control software.
- Why software freedom benefits society.

The GNU Manifesto became the foundation of the Free Software Movement.

---

# Free Software Foundation (FSF)

## Definition

The **Free Software Foundation (FSF)** is a non-profit organization established by Richard Stallman.

Its purpose is to support and promote free software.

### Responsibilities

- Promote Free Software
- Support GNU Project
- Protect Software Freedom
- Encourage Open Development

---

# GNU Components

GNU provides many important software tools.

Some popular GNU software includes:

- GNU Bash
- GCC Compiler
- GDB Debugger
- GNU Core Utilities
- GNU Make
- GNU C Library (glibc)

These tools are widely used in Linux operating systems.

---

# GNU and Linux

Many beginners think GNU and Linux are the same.

They are different.

## GNU

Provides:

- Shell
- Compiler
- Libraries
- Utilities
- Commands

## Linux

Provides:

- Kernel

When combined:

```text
GNU Tools
      +
Linux Kernel
      =
GNU/Linux Operating System
```

This is why Ubuntu, Debian, Fedora, and many other Linux distributions are technically called **GNU/Linux**.

---

# GNU vs UNIX

| GNU | UNIX |
|------|------|
| Free Software | Proprietary (Traditional UNIX) |
| Open Source | Mostly Closed Source |
| Source Code Available | Source Code Restricted |
| Users Can Modify | Modification Restricted |
| UNIX Compatible | Original UNIX |

---

# GNU Architecture

```text
+--------------------------+
| Application Programs     |
+--------------------------+
            │
+--------------------------+
| GNU Utilities            |
| GNU Libraries            |
| GNU Bash                 |
| GCC                      |
+--------------------------+
            │
+--------------------------+
| Linux Kernel             |
+--------------------------+
            │
+--------------------------+
| Hardware                 |
+--------------------------+
```

---

# Practical (Ubuntu VirtualBox)

Open Terminal

```bash
Ctrl + Alt + T
```

---

## Check Bash Version

```bash
bash --version
```

Expected Output

```text
GNU bash, version 5.x.x
```

This shows that Ubuntu uses **GNU Bash**.

---

## Display Operating System Information

```bash
cat /etc/os-release
```

Expected Output

```text
NAME="Ubuntu"
VERSION="24.xx LTS"
```

---

## Display Kernel Information

```bash
uname -a
```

Expected Output

```text
Linux ubuntu ...
```

Notice:

- GNU provides user-space tools.
- Linux provides the kernel.

---

# Real World Applications

GNU tools are used by:

## Software Developers

- Programming
- Compiling Code
- Debugging

---

## Backend Developers

- Shell scripting
- Server management
- Automation

---

## DevOps Engineers

- Bash scripting
- Deployment
- CI/CD Pipelines
- Docker
- Kubernetes

---

## Cloud Engineers

GNU tools are used in:

- AWS EC2
- Azure Virtual Machines
- Google Cloud Compute Engine

Almost every Linux server uses GNU tools.

---

# Advantages of GNU

- Free to use
- Open Source
- Secure
- Stable
- UNIX Compatible
- Community Driven
- Easy to Modify
- Supports Collaboration

---

# Limitations

- GNU alone is not a complete operating system.
- It requires a kernel.
- Usually combined with the Linux Kernel.

---

# GNU + Linux Relationship

```text
GNU
│
├── Bash
├── GCC
├── Libraries
├── Utilities
│
└──────────────┐
               │
        Linux Kernel
               │
               ▼
       GNU/Linux System
```

---

# Quick Revision

- GNU stands for **GNU's Not UNIX**.
- Started by Richard Stallman.
- GNU Project announced in 1983.
- GNU Manifesto published in 1985.
- Free Software Foundation supports GNU.
- GNU provides software tools.
- Linux provides the Kernel.
- GNU + Linux = GNU/Linux.

---

# Important Keywords

- GNU
- GNU's Not UNIX
- Richard Stallman
- GNU Project
- GNU Manifesto
- Free Software Foundation (FSF)
- Free Software
- Open Source
- Linux Kernel
- GNU/Linux

---

# Frequently Asked Questions

## Q1. What is GNU?

GNU is a free software project that aims to develop a free UNIX-compatible operating system.

---

## Q2. Who started the GNU Project?

Richard Stallman.

---

## Q3. What is the full form of GNU?

GNU's Not UNIX.

---

## Q4. What is FSF?

Free Software Foundation is a non-profit organization established to support free software and the GNU Project.

---

## Q5. Why is Ubuntu called GNU/Linux?

Because Ubuntu uses:

- GNU tools
- Linux Kernel

Together they form a complete operating system.

---

# 2 Marks Questions

1. Define GNU.
2. What is the full form of GNU?
3. Who started the GNU Project?
4. What is GNU Manifesto?
5. What is FSF?

---

# 5 Marks Questions

1. Explain GNU Project.
2. Explain GNU Manifesto.
3. Explain Free Software Foundation.
4. Explain GNU and Linux relationship.

---

# Long Answer Questions

1. Explain GNU with its objectives.
2. Explain the history of GNU Project.
3. Explain GNU Architecture.
4. Explain GNU and Linux with a suitable diagram.

---

# Practical Questions

### Display Bash Version

```bash
bash --version
```

---

### Display Linux Kernel Information

```bash
uname -a
```

---

### Display Ubuntu Information

```bash
cat /etc/os-release
```

---

# University Exam Tips

If the question is:

**"Explain GNU."**

Write your answer in the following order:

1. Definition
2. Full Form
3. History
4. Richard Stallman
5. Objectives
6. GNU Manifesto
7. Free Software Foundation
8. GNU + Linux Relationship
9. Diagram
10. Conclusion

This answer structure helps in scoring maximum marks.

---

# Summary

- GNU is a free software project started by Richard Stallman.
- GNU was developed to create a free UNIX-compatible operating system.
- The GNU Project promotes software freedom.
- The Free Software Foundation supports GNU development.
- GNU provides utilities, libraries, compilers, and shells.
- Linux provides the kernel.
- Together they form a complete GNU/Linux operating system.