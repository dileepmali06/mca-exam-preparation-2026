# 3.1.1 Work on Linux Terminal – Telnet Connection, Login Account, Password and Logout

> **Module:** Module 3 – Unix/Linux Commands
>
> **Topic:** Work on Linux Terminal – Telnet Connection through Login Account, Password and Logout
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

- Understand the Linux Terminal.
- Understand Login, User Account, Password and Logout.
- Explain Authentication in Linux.
- Understand the Telnet protocol.
- Differentiate between Telnet and SSH.
- Perform basic login and logout operations in Ubuntu Linux.

---

# Introduction

Linux is a multi-user operating system.

It allows multiple users to access the same computer while keeping each user's files and settings separate.

Before accessing Linux, every user must authenticate themselves using a valid username and password.

After successful authentication, Linux provides access to the Terminal and the user's working environment.

---

# Why is Login Required?

Login provides security to the operating system.

Without a login system:

- Anyone could access personal files.
- Anyone could modify system settings.
- Anyone could delete important data.
- Unauthorized users could use the computer.

Therefore, Linux requires authentication before granting access.

---

# User Account

A **User Account** is the identity of a user inside the Linux operating system.

Every user account contains:

- Username
- Password
- Home Directory
- User ID (UID)
- Permissions
- Personal Settings

Example

```text
User: dilip

Home Directory:

/home/dilip
```

Every user has an independent working environment.

---

# Username

A **Username** uniquely identifies a user in Linux.

Examples

```text
dilip

rahul

ubuntu

admin
```

The operating system uses the username to determine who is requesting access.

---

# Password

A **Password** protects the user account from unauthorized access.

Linux stores passwords in encrypted (hashed) form rather than plain text.

This improves system security.

---

# Authentication

Authentication is the process of verifying the identity of a user.

The Linux operating system checks:

- Username
- Password

If both are correct, access is granted.

Otherwise, login is denied.

---

# Login Process

```text
User

↓

Enter Username

↓

Enter Password

↓

Authentication

↓

Credentials Verified

↓

Login Successful

↓

Shell Starts

↓

Home Directory Opened
```

---

# What Happens After Login?

After successful login:

- User Home Directory opens.
- Default Shell starts.
- Environment Variables are loaded.
- User profile is initialized.
- The user can execute Linux commands.

---

# Logout

Logout means ending the current user session safely.

After logout:

- The terminal session closes.
- Running interactive session ends.
- Another user can log in safely.

---

# Logout Commands

```bash
logout
```

or

```bash
exit
```

Shortcut

```text
Ctrl + D
```

---

# Telnet

## Definition

**Telnet** is a client-server network protocol used to remotely access another computer over a TCP/IP network.

It allows users to log in to a remote system and execute commands as if they were sitting in front of that computer.

---

# Working of Telnet

```text
Client Computer

↓

Telnet Client

↓

Network

↓

Telnet Server

↓

Remote Linux Machine
```

---

# Default Port Number

Telnet uses:

```text
Port 23
```

---

# Features of Telnet

- Remote Login
- Text-Based Communication
- Client-Server Architecture
- Supports Command Execution
- Uses TCP Protocol

---

# Limitations of Telnet

- Password transmitted in plain text.
- No encryption.
- Vulnerable to network attacks.
- Not suitable for modern secure communication.

---

# SSH as an Alternative

Today, Telnet has been replaced by **SSH (Secure Shell)**.

SSH provides:

- Encrypted Communication
- Secure Authentication
- Secure Remote Login
- Secure File Transfer

SSH uses:

```text
Port 22
```

---

# Telnet vs SSH

| Telnet | SSH |
|---------|-----|
| Port 23 | Port 22 |
| No Encryption | Encrypted Communication |
| Less Secure | Highly Secure |
| Plain Text Authentication | Secure Authentication |
| Rarely Used Today | Widely Used Today |

---

# Practical (Ubuntu VirtualBox)

## Step 1

Open Ubuntu.

---

## Step 2

Open Terminal.

Shortcut

```text
Ctrl + Alt + T
```

---

## Step 3

Display Current Logged-in User

```bash
whoami
```

Example Output

```text
dilip
```

---

## Step 4

Display Home Directory

```bash
pwd
```

Example Output

```text
/home/dilip
```

---

## Step 5

Logout from Terminal

```bash
logout
```

or

```bash
exit
```

or press

```text
Ctrl + D
```

---

## Step 6 (Optional)

Check whether Telnet is installed

```bash
telnet
```

If the command is not found:

```bash
sudo apt update
```

```bash
sudo apt install telnet
```

---

# Expected Output

```text
$ whoami

dilip
```

---

```text
$ pwd

/home/dilip
```

---

```text
$ exit
logout
```

---

# Real World Applications

## Software Developers

- Access Linux development servers remotely.
- Manage development environments.

---

## Backend Developers

- Connect to application servers.
- Perform server-side maintenance.

---

## DevOps Engineers

- Remote server administration.
- Deployment and monitoring.
- Infrastructure management.

---

## Linux System Administrators

- User management.
- Remote troubleshooting.
- System maintenance.

---

# Common Beginner Mistakes

### Mistake 1

Thinking Login and Username are the same.

**Correct:**

- Username identifies the user.
- Login is the authentication process.

---

### Mistake 2

Thinking Telnet is secure.

**Correct:**

Telnet sends data in plain text.

SSH is the secure alternative.

---

### Mistake 3

Confusing Port Numbers.

Remember:

- Telnet → Port 23
- SSH → Port 22

---

# Advantages

- Supports remote login.
- Easy to use.
- Useful for learning networking concepts.
- Simple client-server communication.

---

# Limitations

- No encryption.
- Passwords transmitted in plain text.
- Vulnerable to attackers.
- Mostly replaced by SSH.

---

# Quick Revision

- Linux is a multi-user operating system.
- Every user requires a Login Account.
- Authentication verifies Username and Password.
- Logout ends the current session.
- Telnet provides remote login.
- Telnet uses Port 23.
- SSH uses Port 22 and provides encrypted communication.

---

# Important Keywords

- Linux Terminal
- Login
- Logout
- User Account
- Username
- Password
- Authentication
- Telnet
- Remote Login
- Port 23
- SSH
- Port 22

---

# Frequently Asked Questions

## What is a User Account?

A User Account is the identity of a user inside Linux.

---

## What is Authentication?

Authentication is the process of verifying a user's identity.

---

## What is Telnet?

Telnet is a protocol used for remote login over a TCP/IP network.

---

## Which port does Telnet use?

Port 23.

---

## Which protocol replaced Telnet?

SSH (Secure Shell).

---

# MCQ Questions

### Q1.

Linux is a:

A. Single User Operating System

B. Multi-user Operating System

C. Database

D. Programming Language

**Answer:** B

---

### Q2.

Which protocol provides remote login?

A. FTP

B. HTTP

C. Telnet

D. SMTP

**Answer:** C

---

### Q3.

Telnet uses which port?

A. 21

B. 22

C. 23

D. 80

**Answer:** C

---

### Q4.

Which protocol is more secure?

A. Telnet

B. SSH

C. FTP

D. HTTP

**Answer:** B

---

### Q5.

Which command displays the current logged-in user?

A.

```bash
pwd
```

B.

```bash
whoami
```

C.

```bash
ls
```

D.

```bash
ps
```

**Answer:** B

---

# Interview Questions

- What is the Linux Login Process?
- Explain User Account and Authentication.
- What is Telnet?
- Explain the working of Telnet.
- Differentiate between Telnet and SSH.

---

# Viva Questions

1. What is Login?
2. What is Logout?
3. What is Authentication?
4. What is Telnet?
5. Which port does Telnet use?
6. Why is SSH preferred over Telnet?

---

# 2 Marks Questions

1. Define Login.
2. Define Logout.
3. What is Telnet?
4. Which port is used by Telnet?

---

# 5 Marks Questions

1. Explain the Linux Login Process.
2. Explain the Telnet protocol.
3. Differentiate between Telnet and SSH.

---

# Long Answer Questions

1. Explain Login, User Account, Password and Logout in Linux.
2. Explain the Telnet protocol with its working and applications.
3. Compare Telnet and SSH with suitable examples.

---

# Command Cheat Sheet

| Command | Purpose |
|----------|---------|
| `whoami` | Display current logged-in user |
| `pwd` | Display current working directory |
| `exit` | Exit the terminal session |
| `logout` | Logout from the current session |
| `telnet` | Start the Telnet client (if installed) |

---

# Previous Year Exam Focus

⭐⭐⭐⭐⭐ Very Important

- Login Process
- User Account
- Authentication
- Telnet
- Telnet Port Number
- SSH
- Telnet vs SSH

---

# Summary

- Linux is a multi-user operating system that requires user authentication before granting access.
- Every user has a unique account consisting of a username, password, home directory, and permissions.
- Authentication verifies the user's identity using the username and password.
- Telnet is a remote login protocol that uses Port 23 but is considered insecure because it transmits data in plain text.
- SSH is the modern replacement for Telnet and provides encrypted, secure remote access using Port 22.

---

# Related Topics

⬅️ Previous Module

**Module 2 – Processes**

➡️ Next Topic

**02-Internal-and-External-Commands.md**