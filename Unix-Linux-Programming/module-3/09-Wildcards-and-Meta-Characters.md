# 3.2.7 Wildcards and Meta Characters

> **Module:** Module 3 – Unix/Linux Commands
>
> **Topic:** Wildcards and Meta Characters
>
> **Subject:** Unix/Linux Programming

---

# Learning Objectives

- Understand Wildcards and Meta Characters.
- Use `*`, `?`, `[]`, `{}` effectively.
- Understand shell meta characters like `>`, `>>`, `<`, `|`, `$`, `~`, `&`.
- Perform filename pattern matching.

---

# Introduction

Wildcards and Meta Characters make Linux commands more powerful by allowing users to work with multiple files and perform advanced shell operations.

---

# What are Wildcards?

Wildcards are special characters used to match one or more filenames.

## 1. Asterisk (`*`)

Matches **zero or more characters**.

### Syntax

```bash
ls *.txt
```

### Example

```text
notes.txt
linux.txt
readme.txt
```

---

## 2. Question Mark (`?`)

Matches **exactly one character**.

### Example

```bash
ls file?.txt
```

Matches:

```text
file1.txt
file2.txt
fileA.txt
```

---

## 3. Square Brackets (`[]`)

Matches one character from a given set.

### Example

```bash
ls file[123].txt
```

Matches:

```text
file1.txt
file2.txt
file3.txt
```

### Range Example

```bash
ls file[a-z].txt
ls image[1-5].jpg
```

---

## 4. Curly Braces (`{}`)

Creates multiple filenames.

```bash
touch file{1,2,3}.txt
```

Creates:

```text
file1.txt
file2.txt
file3.txt
```

---

# What are Meta Characters?

Meta Characters have special meanings in the Linux shell.

| Character | Purpose |
|-----------|---------|
| `~` | Home Directory |
| `$` | Variable |
| `>` | Output Redirection |
| `>>` | Append Output |
| `<` | Input Redirection |
| `|` | Pipe |
| `&` | Background Process |
| `;` | Execute Multiple Commands |

---

# Examples

## Home Directory

```bash
cd ~
```

## Variable

```bash
echo $HOME
```

## Output Redirection

```bash
ls > files.txt
```

## Append Output

```bash
echo Linux >> notes.txt
```

## Input Redirection

```bash
sort < names.txt
```

## Pipe

```bash
ls | more
```

## Background Process

```bash
firefox &
```

---

# Difference Between Wildcards and Meta Characters

| Wildcards | Meta Characters |
|-----------|-----------------|
| Used for filename matching | Used for shell operations |
| `*`, `?`, `[]`, `{}` | `>`, `<`, `|`, `$`, `~`, `&` |

---

# Practical (Ubuntu)

```bash
touch file1.txt file2.txt file3.txt
touch image1.jpg image2.jpg

ls *.txt
ls file?.txt
ls file[1-3].txt
touch demo{1,2,3}.txt
echo $HOME
ls > files.txt
cat files.txt
ls | more
```

---

# Quick Revision

- `*` → Zero or more characters
- `?` → Exactly one character
- `[]` → Character matching
- `{}` → Multiple filename expansion
- `>` → Output Redirection
- `>>` → Append Output
- `<` → Input Redirection
- `|` → Pipe
- `$` → Variable
- `~` → Home Directory

---

# MCQ Questions

### Q1. Which wildcard matches zero or more characters?

A. `?`
B. `*`
C. `[]`
D. `{}`

**Answer:** B

### Q2. Which wildcard matches exactly one character?

A. `*`
B. `?`
C. `[]`
D. `~`

**Answer:** B

### Q3. Which symbol is used for output redirection?

A. `|`
B. `>`
C. `&`
D. `$`

**Answer:** B

### Q4. Which symbol represents the Home Directory?

A. `/`
B. `~`
C. `*`
D. `$`

**Answer:** B

### Q5. Which symbol is used for Pipe?

A. `>`
B. `<`
C. `|`
D. `&`

**Answer:** C

---

# Interview Questions

1. What are Wildcards?
2. What are Meta Characters?
3. Explain `*` and `?`.
4. Explain `[]` with an example.
5. Explain output redirection and pipe.

---

# Viva Questions

1. Define Wildcards.
2. Define Meta Characters.
3. What is the use of `*`?
4. What is the use of `?`?
5. What is the purpose of `|`?

---

# Command Cheat Sheet

| Command | Purpose |
|----------|---------|
| `ls *.txt` | List all text files |
| `ls file?.txt` | Match one character |
| `ls file[1-3].txt` | Match range |
| `touch file{1,2,3}.txt` | Create multiple files |
| `echo $HOME` | Show Home Directory |
| `ls > files.txt` | Redirect output |
| `ls \| more` | Pipe output |

---

# Summary

- Wildcards simplify filename matching.
- Meta Characters control shell behavior.
- `less` and `more` are unrelated; Wildcards are mainly for file selection.
- Wildcards and Meta Characters are essential for Linux command-line efficiency.

---

# Related Topics

⬅️ **08-File-Viewing-Commands.md**

➡️ **Module 4 – Filters and Pipes**
