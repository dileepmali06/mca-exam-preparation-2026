# 4.1.1 Command Mode, Insert Mode and Last Line Mode

> **Module:** Module 4 -- VI Editor and Shell Programming **Section:**
> VI Editor **Topic:** Command Mode, Insert Mode and Last Line Mode

------------------------------------------------------------------------

# Learning Objectives

-   Understand the VI Editor.
-   Learn the three modes of VI Editor.
-   Create, edit, save and exit files.

------------------------------------------------------------------------

# Introduction

**VI Editor** is a text editor used to create and edit files in
Unix/Linux.

It has three modes:

-   Command Mode
-   Insert Mode
-   Last Line Mode

------------------------------------------------------------------------

# Open VI Editor

``` bash
vi notes.txt
```

------------------------------------------------------------------------

# Command Mode

-   Default mode when VI starts.
-   Used to move the cursor and execute commands.

  Command   Purpose
  --------- ---------------------
  `h`       Left
  `j`       Down
  `k`       Up
  `l`       Right
  `x`       Delete character
  `dd`      Delete current line
  `yy`      Copy line
  `p`       Paste

------------------------------------------------------------------------

# Insert Mode

Used for typing text.

  Command   Purpose
  --------- ----------------------
  `i`       Insert before cursor
  `I`       Beginning of line
  `a`       Append after cursor
  `A`       End of line
  `o`       New line below
  `O`       New line above

Press **Esc** to return to Command Mode.

------------------------------------------------------------------------

# Last Line Mode

Enter by pressing `:` in Command Mode.

  Command   Purpose
  --------- ---------------------
  `:w`      Save
  `:q`      Quit
  `:wq`     Save and Quit
  `:q!`     Quit without saving
  `:x`      Save and Exit

------------------------------------------------------------------------

# Mode Switching

``` text
Command Mode
      |
   i/a/o
      v
Insert Mode
      |
     Esc
      v
Command Mode
      |
      :
      v
Last Line Mode
```

------------------------------------------------------------------------

# Practical

``` bash
vi notes.txt
```

Press:

``` text
i
```

Type text, press:

``` text
Esc
```

Save:

``` text
:w
```

Exit:

``` text
:wq
```

------------------------------------------------------------------------

# Quick Revision

-   `vi file.txt` → Open editor
-   `i` → Insert Mode
-   `Esc` → Command Mode
-   `:` → Last Line Mode
-   `:w` → Save
-   `:q` → Quit
-   `:wq` → Save & Quit

------------------------------------------------------------------------

# MCQs

**Q1. Which mode opens by default?**

A. Insert B. Command C. Last Line D. Edit

**Answer:** B

------------------------------------------------------------------------

**Q2. Which key enters Insert Mode?**

A. Esc B. i C. : D. q

**Answer:** B

------------------------------------------------------------------------

# Interview Questions

1.  What is VI Editor?
2.  Explain the three modes.
3.  How do you save a file?
4.  How do you exit without saving?

------------------------------------------------------------------------

# Command Cheat Sheet

  Command         Purpose
  --------------- --------------
  `vi file.txt`   Open file
  `i`             Insert Mode
  `Esc`           Command Mode
  `:w`            Save
  `:q`            Quit
  `:wq`           Save & Quit

------------------------------------------------------------------------

# Summary

-   VI Editor is used to create and edit files.
-   It has Command, Insert and Last Line modes.
-   Use `:wq` to save and exit.

------------------------------------------------------------------------

# Related Topics

**Next:** 24-VI-Editing-Commands.md
