# 3.3.1 Introduction to Filters

> **Module:** Module 3 – Unix/Linux Commands
>
> **Topic:** Introduction to Filters
>
> **Subject:** Unix/Linux Programming
>
> **Based On:** Amity University PDF

---

# Learning Objectives

After studying this topic, you will be able to:

- Understand the concept of Filters.
- Learn how Filters process data.
- Understand Standard Input, Standard Output and Standard Error.
- Understand the concept of Pipes.
- Perform basic filtering operations in Linux.

---

# Introduction

A Filter is a Linux command that reads data from **Standard Input (stdin)**, processes it, and displays the processed result on **Standard Output (stdout)**.

Filters are mainly used to process text data, search information, sort records, count lines, and manipulate file contents.

Most Linux filter commands are used together with **Pipes (`|`)**.

---

# What is a Filter?

## Definition

A **Filter** is a command that accepts data as input, processes it, and produces the modified result as output.

In Linux, filters are commonly used to:

- Process text files
- Search data
- Sort records
- Count words and lines
- Extract specific information

---

# Working of a Filter

```text
Input
   │
   ▼
Filter
   │
   ▼
Output
```

Example

```bash
cat students.txt | sort
```

Flow

```text
students.txt
      │
      ▼
cat
      │
      ▼
sort
      │
      ▼
Sorted Output
```

---

# Standard Input (stdin)

Standard Input (stdin) is the input that a command receives.

Normally, the keyboard acts as the standard input device.

Example

```bash
sort
```

The user enters data using the keyboard, and the `sort` command processes it.

---

# Standard Output (stdout)

Standard Output (stdout) is the normal output displayed by a command.

Example

```bash
ls
```

The list of files displayed on the terminal is the standard output.

---

# Standard Error (stderr)

Standard Error (stderr) is used to display error messages.

Example

```bash
cat demo.txt
```

Output

```text
cat: demo.txt: No such file or directory
```

The above message is displayed through **stderr**.

---

# Pipe (`|`)

A Pipe connects two commands.

The output of the first command becomes the input of the second command.

## Syntax

```bash
command1 | command2
```

### Example

```bash
cat students.txt | sort
```

Explanation:

- `cat` displays the file contents.
- `sort` receives that output and sorts it alphabetically.

---

# Common Filter Commands

| Command | Purpose |
|----------|---------|
| `head` | Display first lines of a file |
| `tail` | Display last lines of a file |
| `cut` | Extract selected columns |
| `sort` | Sort data |
| `wc` | Count lines, words and characters |
| `grep` | Search text |
| `uniq` | Remove duplicate lines |
| `cmp` | Compare two files |
| `comm` | Compare sorted files |
| `diff` | Display differences between files |

---

# Practical (Ubuntu)

## Step 1

Create a sample file.

```bash
cat > students.txt
```

Type:

```text
Rahul
Aman
Dilip
Karan
Neha
```

Press

```text
Ctrl + D
```

---

## Step 2

Display the file.

```bash
cat students.txt
```

---

## Step 3

Sort the file.

```bash
cat students.txt | sort
```

Output

```text
Aman
Dilip
Karan
Neha
Rahul
```

---

## Step 4

Count the number of lines.

```bash
cat students.txt | wc -l
```

Output

```text
5
```

---

# Advantages of Filters

- Process text efficiently.
- Reduce manual work.
- Work with large files.
- Can be combined using Pipes.
- Useful in shell scripting.

---

# Common Mistakes

### Mistake 1

Assuming every Linux command is a filter.

**Correct:** Only commands that process input data are considered filters.

---

### Mistake 2

Confusing Pipes with Filters.

**Correct:**

- Filter → Processes data.
- Pipe → Connects commands.

---

# Quick Revision

- Filter → Processes input data.
- stdin → Standard Input.
- stdout → Standard Output.
- stderr → Standard Error.
- `|` → Pipe.

---

# Important Keywords

- Filter
- stdin
- stdout
- stderr
- Pipe
- Data Processing

---

# MCQs

### Q1. What is a Filter?

A. Hardware Device

B. Linux Command that Processes Input

C. Memory

D. CPU

**Answer:** B

---

### Q2. Which symbol represents a Pipe?

A. `>`

B. `<`

C. `|`

D. `&`

**Answer:** C

---

### Q3. What is stdin?

A. Standard Input

B. Standard Output

C. Standard Error

D. Shell

**Answer:** A

---

### Q4. Which command counts lines?

A. `wc`

B. `pwd`

C. `mkdir`

D. `cd`

**Answer:** A

---

### Q5. Which command sorts data?

A. `sort`

B. `mv`

C. `cp`

D. `rm`

**Answer:** A

---

# Interview Questions

1. What is a Filter in Linux?
2. Explain stdin, stdout and stderr.
3. What is the purpose of a Pipe?
4. How do Filters work?
5. Why are Filters important in Linux?

---

# Viva Questions

1. Define Filter.
2. What is stdin?
3. What is stdout?
4. What is stderr?
5. What is a Pipe?

---

# Command Cheat Sheet

| Command | Purpose |
|----------|---------|
| `cat file.txt` | Display file contents |
| `sort` | Sort data |
| `wc -l` | Count lines |
| `cat file.txt \| sort` | Sort file contents |
| `cat file.txt \| wc -l` | Count lines in a file |

---

# Summary

- Filters process input data and produce output.
- Most filters work with text data.
- stdin provides input to a command.
- stdout displays normal output.
- stderr displays error messages.
- Pipes (`|`) connect multiple commands.
- Filters are essential tools for text processing in Linux.

---

# Related Topics

⬅️ Previous Topic

**09-Wildcards-and-Meta-Characters.md**

➡️ Next Topic

**11-Head-Tail-Cut.md**