# 3.6 Unix Links

> **Module:** Module 3 -- Unix/Linux Commands\
> **Section:** Unix Links\
> **Subject:** Unix/Linux Programming

------------------------------------------------------------------------

# Learning Objectives

-   Understand Unix Links.
-   Learn Hard Link and Soft (Symbolic) Link.
-   Use the `ln` command.
-   Compare Hard and Soft Links.

------------------------------------------------------------------------

# Introduction

A **Unix Link** is another name or reference to an existing file or
directory. Links help avoid duplicate files, save disk space, and
simplify file management.

------------------------------------------------------------------------

# What is a Link?

A **Link** is a reference that connects one file name to another
existing file.

------------------------------------------------------------------------

# Why Use Links?

-   Avoid duplicate files
-   Save disk space
-   Easy file access
-   Better file organization
-   Share the same file from multiple locations

------------------------------------------------------------------------

# Types of Links

Linux provides two types of links:

1.  **Hard Link**
2.  **Soft (Symbolic) Link**

------------------------------------------------------------------------

# Hard Link

## Definition

A **Hard Link** is another name for the same file. Both file names point
to the same inode.

### Features

-   Same inode number
-   Shares the same data
-   Cannot link directories
-   Cannot cross file systems
-   Deleting one link does not delete the data until all hard links are
    removed

### Syntax

``` bash
ln source_file hard_link
```

### Example

``` bash
touch notes.txt
ln notes.txt notes_hard.txt
```

------------------------------------------------------------------------

# Soft (Symbolic) Link

## Definition

A **Soft Link** (Symbolic Link) is a shortcut that stores the path of
the original file.

### Features

-   Different inode number
-   Can link directories
-   Can cross file systems
-   Breaks if the original file is deleted

### Syntax

``` bash
ln -s source_file soft_link
```

### Example

``` bash
ln -s notes.txt notes_soft.txt
```

------------------------------------------------------------------------

# Hard Link vs Soft Link

  -----------------------------------------------------------------------
  Hard Link                           Soft Link
  ----------------------------------- -----------------------------------
  Same inode                          Different inode

  Cannot link directories             Can link directories

  Cannot cross file systems           Can cross file systems

  Works even if one link is removed   Breaks if original file is deleted
  -----------------------------------------------------------------------

------------------------------------------------------------------------

# ln Command

## Definition

The **ln** command creates hard links and symbolic links.

### Hard Link

``` bash
ln notes.txt notes_hard.txt
```

### Soft Link

``` bash
ln -s notes.txt notes_soft.txt
```

------------------------------------------------------------------------

# View Links

Display links:

``` bash
ls -l
```

Display inode numbers:

``` bash
ls -i
```

------------------------------------------------------------------------

# Practical

Create a file:

``` bash
touch notes.txt
```

Create a hard link:

``` bash
ln notes.txt notes_hard.txt
```

Create a soft link:

``` bash
ln -s notes.txt notes_soft.txt
```

View links:

``` bash
ls -l
```

View inode numbers:

``` bash
ls -i
```

------------------------------------------------------------------------

# Quick Revision

-   Link → Reference to a file
-   Hard Link → Same inode
-   Soft Link → Shortcut (different inode)
-   `ln` → Create hard link
-   `ln -s` → Create symbolic link
-   `ls -l` → View links
-   `ls -i` → View inode numbers

------------------------------------------------------------------------

# MCQs

**Q1. Which command creates a hard link?**

A. `ln file1 file2`\
B. `ln -s file1 file2`\
C. `cp file1 file2`\
D. `mv file1 file2`

**Answer:** A

------------------------------------------------------------------------

**Q2. Which option creates a symbolic link?**

A. `-r`\
B. `-l`\
C. `-s`\
D. `-i`

**Answer:** C

------------------------------------------------------------------------

**Q3. Hard Links share the same:**

A. Path\
B. Folder\
C. Inode\
D. Directory

**Answer:** C

------------------------------------------------------------------------

**Q4. Which link breaks if the original file is deleted?**

A. Hard Link\
B. Soft Link\
C. Both\
D. None

**Answer:** B

------------------------------------------------------------------------

**Q5. Which command displays inode numbers?**

A. `ls -i`\
B. `pwd`\
C. `cat`\
D. `mkdir`

**Answer:** A

------------------------------------------------------------------------

# Interview / Viva Questions

1.  What is a Unix Link?
2.  Explain Hard Link.
3.  Explain Soft Link.
4.  Differentiate between Hard Link and Soft Link.
5.  Explain the `ln` command.

------------------------------------------------------------------------

# Command Cheat Sheet

  Command               Purpose
  --------------------- ----------------------
  `ln file1 file2`      Create hard link
  `ln -s file1 file2`   Create symbolic link
  `ls -l`               View links
  `ls -i`               View inode numbers

------------------------------------------------------------------------

# Summary

-   Unix Links provide another reference to files.
-   Hard Links use the same inode.
-   Soft Links act as shortcuts.
-   The `ln` command creates links.

------------------------------------------------------------------------

# Related Topics

**Previous:** 21-Changing-Permissions.md

**Next:** Module 4
