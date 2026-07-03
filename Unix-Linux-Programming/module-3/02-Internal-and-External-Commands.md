# 3.1.2 Internal and External Commands

> **Module:** Module 3 – Unix/Linux Commands
>
> **Topic:** Internal and External Commands
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

- Understand Internal Commands.
- Understand External Commands.
- Differentiate between Internal and External Commands.
- Understand how Linux executes commands.
- Use the `type` and `which` commands.
- Understand the PATH environment variable.

---

# Introduction

Linux provides hundreds of commands to perform different tasks.

These commands are mainly divided into two categories:

- Internal Commands
- External Commands

Both types of commands help users interact with the Linux operating system, but they differ in the way they are executed.

---

# What are Internal Commands?

## Definition

Internal Commands are commands that are built into the shell.

They are executed directly by the shell without loading any external executable file.

These commands are always available once the shell starts.

---

# Features of Internal Commands

- Built into the shell.
- Execute very quickly.
- Do not require a separate executable file.
- Consume less execution time.
- Always available while the shell is running.

---

# Examples of Internal Commands

```text
cd
pwd
echo
exit
history
alias
unalias
type
```

---

# Working of Internal Commands

```text
User

↓

Shell

↓

Internal Command Found

↓

Execute

↓

Output
```

Since the command is already available inside the shell, no file searching is required.

---

# What are External Commands?

## Definition

External Commands are commands stored as executable files in the Linux file system.

The shell searches for these executable files using the PATH environment variable before executing them.

---

# Features of External Commands

- Stored as executable files.
- Located in directories such as `/bin`, `/usr/bin`, and `/usr/local/bin`.
- Loaded into memory before execution.
- Slightly slower than internal commands.
- Can be installed or removed.

---

# Examples of External Commands

```text
ls
cat
cp
mv
rm
mkdir
touch
grep
find
ps
```

---

# Working of External Commands

```text
User

↓

Shell

↓

Search PATH

↓

Executable File Found

↓

Load into Memory

↓

Execute

↓

Output
```

---

# PATH Environment Variable

The PATH variable stores the directories where Linux searches for executable commands.

View the PATH variable:

```bash
echo $PATH
```

Example Output

```text
/usr/local/bin:/usr/bin:/bin
```

---

# Checking Command Type

## Using `type`

The `type` command tells whether a command is internal or external.

### Example 1

```bash
type cd
```

Output

```text
cd is a shell builtin
```

---

### Example 2

```bash
type ls
```

Output

```text
ls is /usr/bin/ls
```

---

# Finding the Location of External Commands

The `which` command displays the location of an external command.

Example

```bash
which ls
```

Output

```text
/usr/bin/ls
```

---

# Difference Between Internal and External Commands

| Internal Commands | External Commands |
|-------------------|-------------------|
| Built into the shell | Stored as executable files |
| Faster execution | Slightly slower execution |
| No separate executable file | Separate executable file required |
| Always available after shell starts | Executed after searching PATH |
| Cannot be installed separately | Can be installed or removed |
| Example: `cd`, `pwd`, `echo` | Example: `ls`, `cp`, `mv`, `grep` |

---

# Practical (Ubuntu VirtualBox)

## Step 1

Open Terminal.

Shortcut:

```text
Ctrl + Alt + T
```

---

## Step 2

Check an Internal Command.

```bash
type cd
```

Expected Output

```text
cd is a shell builtin
```

---

## Step 3

Check an External Command.

```bash
type ls
```

Expected Output

```text
ls is /usr/bin/ls
```

---

## Step 4

Find the Location of an External Command.

```bash
which ls
```

Expected Output

```text
/usr/bin/ls
```

---

## Step 5

Display the PATH Variable.

```bash
echo $PATH
```

---

# Real World Applications

## Software Developers

- Use `cd` to navigate project folders.
- Use `echo` for debugging shell scripts.
- Use `ls` to view project files.

---

## Backend Developers

- Use `grep` to search logs.
- Use `ps` to monitor running services.
- Use `cat` to read configuration files.

---

## DevOps Engineers

- Navigate servers using internal commands.
- Manage files using external commands.
- Search logs and monitor applications.

---

## Linux System Administrators

- Use internal commands for shell management.
- Use external commands for system administration.

---

# Common Beginner Mistakes

### Mistake 1

Thinking every Linux command is an external command.

**Correct:** Some commands are built into the shell.

---

### Mistake 2

Using `which` for shell built-in commands.

**Correct:** Use `type` to identify both internal and external commands.

---

### Mistake 3

Thinking the PATH variable stores commands.

**Correct:** PATH stores directories where executable files are located.

---

# Advantages

## Internal Commands

- Fast execution.
- No disk search required.
- Always available.

---

## External Commands

- Easy to update.
- Easy to install.
- Large collection of utilities.

---

# Limitations

## Internal Commands

- Limited functionality.
- Fixed inside the shell.

---

## External Commands

- Require executable files.
- Slightly slower due to file lookup.

---

# Quick Revision

- Linux commands are of two types:
  - Internal Commands
  - External Commands
- Internal commands are built into the shell.
- External commands are stored as executable files.
- `type` identifies command type.
- `which` displays the location of external commands.
- PATH stores directories containing executable programs.

---

# Important Keywords

- Internal Command
- External Command
- Shell Built-in
- Executable File
- PATH
- `type`
- `which`

---

# Frequently Asked Questions

## What is an Internal Command?

An Internal Command is a command built into the shell.

---

## What is an External Command?

An External Command is an executable program stored in the Linux file system.

---

## Which command checks the type of a command?

```bash
type
```

---

## Which command displays the location of an external command?

```bash
which
```

---

## What is PATH?

PATH is an environment variable that stores directories where executable commands are searched.

---

# MCQ Questions

### Q1.

Internal commands are:

A. Stored in `/usr/bin`

B. Built into the shell

C. Installed separately

D. Network commands

**Answer:** B

---

### Q2.

Which command identifies whether a command is internal or external?

A. `pwd`

B. `type`

C. `ps`

D. `ls`

**Answer:** B

---

### Q3.

Which command displays the location of an external command?

A. `type`

B. `which`

C. `pwd`

D. `history`

**Answer:** B

---

### Q4.

Which of the following is an Internal Command?

A. `cp`

B. `mv`

C. `cd`

D. `grep`

**Answer:** C

---

### Q5.

Which of the following is an External Command?

A. `exit`

B. `alias`

C. `ls`

D. `history`

**Answer:** C

---

# Interview Questions

- What are Internal Commands?
- What are External Commands?
- Explain the difference between Internal and External Commands.
- What is the PATH environment variable?
- Explain the purpose of the `type` and `which` commands.

---

# Viva Questions

1. What is an Internal Command?
2. What is an External Command?
3. What is PATH?
4. What is the purpose of `type`?
5. What is the purpose of `which`?

---

# 2 Marks Questions

1. Define Internal Commands.
2. Define External Commands.
3. What is the PATH variable?
4. What is the use of the `type` command?

---

# 5 Marks Questions

1. Explain Internal Commands with examples.
2. Explain External Commands with examples.
3. Differentiate between Internal and External Commands.

---

# Long Answer Questions

1. Explain Internal and External Commands with suitable examples.
2. Explain how Linux executes Internal and External Commands.
3. Explain the role of the PATH environment variable.

---

# Command Cheat Sheet

| Command | Purpose |
|----------|---------|
| `type command` | Check whether a command is internal or external |
| `which command` | Display the location of an external command |
| `echo $PATH` | Display the PATH environment variable |

---

# Previous Year Exam Focus

⭐⭐⭐⭐⭐ Very Important

- Internal Commands
- External Commands
- Difference Between Internal and External Commands
- PATH Variable
- `type`
- `which`

---

# Summary

- Linux commands are classified into Internal and External Commands.
- Internal Commands are built into the shell and execute directly.
- External Commands are executable programs stored in the Linux file system.
- The shell searches the PATH environment variable to locate external commands.
- The `type` command identifies command types, while `which` shows the location of external commands.
- Understanding these command types is essential for Linux users, developers, system administrators, and DevOps engineers.

---

# Related Topics

⬅️ Previous Topic

**01-Work-on-Linux-Terminal.md**

➡️ Next Topic

**03-Current-Working-Directory-and-Home-Directory.md**