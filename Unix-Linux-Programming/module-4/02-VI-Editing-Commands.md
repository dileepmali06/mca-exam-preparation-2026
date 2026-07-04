# 4.1.2 VI Editor Editing Commands

> **Module:** Module 4 -- VI Editor and Shell Programming\
> **Section:** VI Editor\
> **Topic:** Change Word, Change Line, Delete Current Line, Delete n
> Lines, Delete Character

------------------------------------------------------------------------

# Learning Objectives

-   Learn common VI editing commands.
-   Change words and lines.
-   Delete characters and lines.
-   Practice editing in Command Mode.

------------------------------------------------------------------------

# Introduction

VI Editor provides editing commands to quickly modify text without using
the mouse.

These commands work in **Command Mode**.

------------------------------------------------------------------------

# Change Word (`cw`)

Changes the current word and enters Insert Mode.

``` text
cw
```

Example:

Before:

``` text
Linux Programming
```

After:

``` text
Unix Programming
```

------------------------------------------------------------------------

# Change Line (`cc`)

Changes the current line and enters Insert Mode.

``` text
cc
```

------------------------------------------------------------------------

# Delete Current Line (`dd`)

Deletes the current line.

``` text
dd
```

------------------------------------------------------------------------

# Delete Multiple Lines (`ndd`)

Deletes **n** lines from the current line.

Examples:

``` text
3dd
```

Delete 3 lines.

``` text
5dd
```

Delete 5 lines.

------------------------------------------------------------------------

# Delete Character (`x`)

Deletes the character under the cursor.

``` text
x
```

------------------------------------------------------------------------

# Editing Commands Summary

  Command   Purpose
  --------- --------------------------
  `cw`      Change current word
  `cc`      Change current line
  `dd`      Delete current line
  `3dd`     Delete 3 lines
  `5dd`     Delete 5 lines
  `x`       Delete current character

------------------------------------------------------------------------

# Practical

Open a file:

``` bash
vi demo.txt
```

Type text using Insert Mode, then press **Esc**.

Try the following commands:

``` text
cw
cc
dd
3dd
x
```

------------------------------------------------------------------------

# Quick Revision

-   `cw` → Change word
-   `cc` → Change line
-   `dd` → Delete line
-   `3dd` → Delete multiple lines
-   `x` → Delete character

------------------------------------------------------------------------

# MCQs

**Q1. Which command changes the current word?**

A. `dd`\
B. `cw`\
C. `cc`\
D. `x`

**Answer:** B

------------------------------------------------------------------------

**Q2. Which command changes the current line?**

A. `cw`\
B. `cc`\
C. `dd`\
D. `yy`

**Answer:** B

------------------------------------------------------------------------

**Q3. Which command deletes the current line?**

A. `dd`\
B. `cc`\
C. `cw`\
D. `x`

**Answer:** A

------------------------------------------------------------------------

**Q4. Which command deletes five lines?**

A. `5dd`\
B. `dd`\
C. `cw`\
D. `yy`

**Answer:** A

------------------------------------------------------------------------

**Q5. Which command deletes one character?**

A. `cc`\
B. `dd`\
C. `x`\
D. `cw`

**Answer:** C

------------------------------------------------------------------------

# Interview / Viva Questions

1.  What is the use of `cw`?
2.  What does `cc` do?
3.  Explain `dd`.
4.  What is `3dd`?
5.  What is the use of `x`?

------------------------------------------------------------------------

# Command Cheat Sheet

  Command   Purpose
  --------- -----------------------
  `cw`      Change word
  `cc`      Change line
  `dd`      Delete current line
  `ndd`     Delete multiple lines
  `x`       Delete character

------------------------------------------------------------------------

# Summary

-   Editing commands work in Command Mode.
-   `cw` changes a word.
-   `cc` changes a line.
-   `dd` deletes a line.
-   `ndd` deletes multiple lines.
-   `x` deletes a character.

------------------------------------------------------------------------

# Related Topics

**Previous:** 23-VI-Editor-Modes.md

**Next:** 25-VI-Cursor-and-Text-Commands.md
