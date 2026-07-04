# 4.1.3 Insert Line, Delete Text and Cursor Movement Commands

> **Module:** Module 4 -- VI Editor and Shell Programming\
> **Section:** VI Editor\
> **Topic:** Insert Line, Delete Text and Commands for Moving the Cursor

------------------------------------------------------------------------

# Learning Objectives

-   Insert new lines in VI Editor.
-   Delete text using editing commands.
-   Move the cursor efficiently.
-   Practice common VI commands.

------------------------------------------------------------------------

# Introduction

VI Editor provides commands to insert lines, delete text and move the
cursor quickly without using the mouse.

These commands work in **Command Mode**.

------------------------------------------------------------------------

# Insert Line

  Command   Purpose
  --------- ------------------------------------------
  `o`       Insert a new line below the current line
  `O`       Insert a new line above the current line

### Example

``` text
o
```

Insert a line below.

``` text
O
```

Insert a line above.

------------------------------------------------------------------------

# Delete Text

## Delete Character

``` text
x
```

Deletes the character under the cursor.

## Delete Word

``` text
dw
```

Deletes the current word.

## Delete to End of Line

``` text
D
```

Deletes text from the cursor to the end of the line.

## Delete Current Line

``` text
dd
```

Deletes the entire current line.

------------------------------------------------------------------------

# Cursor Movement Commands

## Basic Movement

  Command   Purpose
  --------- ------------
  `h`       Move Left
  `j`       Move Down
  `k`       Move Up
  `l`       Move Right

## Line Movement

  Command   Purpose
  --------- -------------------
  `0`       Beginning of line
  `$`       End of line

## Word Movement

  Command   Purpose
  --------- ---------------------
  `w`       Next word
  `b`       Previous word
  `e`       End of current word

## File Movement

  Command   Purpose
  --------- ---------------
  `gg`      First line
  `G`       Last line
  `10G`     Go to line 10

------------------------------------------------------------------------

# Practical

Open a file:

``` bash
vi demo.txt
```

Try the following commands:

``` text
o
O
x
dw
D
dd
h
j
k
l
w
b
0
$
gg
G
10G
```

------------------------------------------------------------------------

# Quick Revision

-   `o` → New line below
-   `O` → New line above
-   `x` → Delete character
-   `dw` → Delete word
-   `D` → Delete to end of line
-   `dd` → Delete line
-   `h j k l` → Move cursor
-   `0` → Beginning of line
-   `$` → End of line
-   `gg` → First line
-   `G` → Last line
-   `10G` → Go to line 10

------------------------------------------------------------------------

# MCQs

**Q1. Which command inserts a line below the current line?**

A. `O`\
B. `o`\
C. `i`\
D. `a`

**Answer:** B

------------------------------------------------------------------------

**Q2. Which command inserts a line above the current line?**

A. `o`\
B. `O`\
C. `I`\
D. `A`

**Answer:** B

------------------------------------------------------------------------

**Q3. Which command deletes a word?**

A. `dw`\
B. `dd`\
C. `yy`\
D. `cc`

**Answer:** A

------------------------------------------------------------------------

**Q4. Which command moves to the first line?**

A. `G`\
B. `gg`\
C. `0`\
D. `$`

**Answer:** B

------------------------------------------------------------------------

**Q5. Which command moves to the last line?**

A. `gg`\
B. `10G`\
C. `G`\
D. `w`

**Answer:** C

------------------------------------------------------------------------

# Interview / Viva Questions

1.  What is the use of `o` and `O`?
2.  Explain `dw`.
3.  What does `D` do?
4.  Explain cursor movement commands.
5.  Differentiate between `gg` and `G`.

------------------------------------------------------------------------

# Command Cheat Sheet

  Command     Purpose
  ----------- -----------------------
  `o`         Insert line below
  `O`         Insert line above
  `x`         Delete character
  `dw`        Delete word
  `D`         Delete to end of line
  `dd`        Delete line
  `h j k l`   Move cursor
  `gg`        First line
  `G`         Last line
  `10G`       Go to specific line

------------------------------------------------------------------------

# Summary

-   `o` and `O` insert new lines.
-   `x`, `dw`, `D` and `dd` delete text.
-   Cursor movement commands make editing faster.
-   These commands are essential for efficient use of the VI Editor.

------------------------------------------------------------------------

# Related Topics

**Previous:** 24-VI-Editing-Commands.md

**Next:** 26-Shell-Script-Introduction.md
