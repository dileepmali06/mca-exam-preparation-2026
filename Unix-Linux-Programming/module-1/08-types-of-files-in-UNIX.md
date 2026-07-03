# Types of Files in UNIX

---

# Introduction

One of the most important features of the UNIX operating system is that it treats almost everything as a file.

However, not every file stores the same type of information.

Different files perform different tasks.

For this reason, UNIX classifies files into different categories.

Understanding file types is important for:

- File Management
- System Administration
- Shell Programming
- Linux Commands
- Software Development

---

# Types of UNIX Files

UNIX supports the following file types:

1. Ordinary (Regular) File
2. Directory File
3. Device File
4. Hidden File
5. Pipe (FIFO)
6. Socket
7. Symbolic Link

Regular files are further divided into:

- Text File
- Binary File

---

# UNIX File Types Diagram

```text
UNIX Files

│

├── Ordinary (Regular) File

│      ├── Text File

│      └── Binary File

│

├── Directory File

├── Device File

├── Hidden File

├── Pipe (FIFO)

├── Socket

└── Symbolic Link
```

---

# 1. Ordinary (Regular) File

## Definition

A Regular File is the most common type of file in UNIX.

It stores:

- Text
- Programs
- Images
- Audio
- Videos
- Documents

Regular files cannot contain other files or directories.

---

## Examples

```text
notes.txt

resume.pdf

photo.jpg

video.mp4

program.c

index.html

music.mp3
```

---

## Characteristics

- Stores actual data.
- Can be created by users.
- Can be copied, moved, renamed and deleted.
- Most user-created files are regular files.

---

# Types of Regular Files

Regular files are divided into two categories.

---

# A. Text File

## Definition

A Text File stores human-readable characters.

Each line ends with a newline character.

Text files can be opened and edited using text editors.

---

## Examples

```text
notes.txt

program.c

script.sh

README.md

index.html
```

---

## Characteristics

- Human Readable
- Easy to Edit
- Uses ASCII or Unicode Characters
- Small in Size

---

## Practical

Create a file

```bash
touch notes.txt
```

Open file

```bash
nano notes.txt
```

Write

```text
Hello Linux
```

Save

```
Ctrl + O
```

Exit

```
Ctrl + X
```

Display contents

```bash
cat notes.txt
```

---

# B. Binary File

## Definition

A Binary File stores data in binary format.

It contains machine-readable instructions rather than plain text.

Humans cannot read binary files directly.

---

## Examples

```text
firefox

chrome

python

song.mp3

movie.mp4

image.png

app.exe
```

---

## Characteristics

- Not Human Readable
- Executable Programs
- Multimedia Files
- Faster Processing

---

## Practical

Check file type

```bash
file /bin/ls
```

Example Output

```text
ELF 64-bit executable
```

---

# Text File vs Binary File

| Text File | Binary File |
|------------|-------------|
| Human Readable | Machine Readable |
| Editable | Normally Not Editable |
| Stores Characters | Stores Binary Data |
| Example: notes.txt | Example: firefox |

---

# 2. Directory File

## Definition

A Directory is a special file that stores references to other files and directories.

It helps organize data in a structured manner.

---

## Example

```text
Projects

├── Java

├── Python

├── Node

└── React
```

---

## Characteristics

- Organizes Files
- Organizes Subdirectories
- Makes Navigation Easy

---

## Practical

Create directory

```bash
mkdir Linux
```

Display directories

```bash
ls
```

---

# 3. Device File

## Definition

UNIX treats hardware devices as files.

These files are stored inside:

```text
/dev
```

---

## Examples

```text
/dev/sda

/dev/null

/dev/tty

/dev/random

/dev/zero
```

---

## Why Device Files?

Applications communicate with hardware through device files.

Examples:

- Hard Disk
- USB
- Printer
- Keyboard
- Mouse

---

## Practical

Display device files

```bash
ls /dev
```

---

# 4. Hidden File

## Definition

A Hidden File is a file whose name begins with a dot (`.`).

These files usually store system or user configuration.

---

## Examples

```text
.bashrc

.profile

.gitignore

.env
```

---

## Characteristics

- Hidden by Default
- Stores Configuration
- Important for System Settings

---

## Practical

Display hidden files

```bash
ls -a
```

---

# 5. Pipe (FIFO)

## Definition

A Pipe is a special file used to transfer data from one command to another.

The output of one command becomes the input of another.

---

## Example

```bash
ls | sort
```

Flow

```text
ls

↓

Pipe

↓

sort
```

---

## Advantages

- Faster Processing
- Command Chaining
- Better Automation

---

# 6. Socket

## Definition

A Socket is a special file used for communication between two processes.

Sockets are mainly used in networking.

---

## Examples

- Web Browser
- Web Server
- Database Server
- Client-Server Communication

---

## Characteristics

- Inter Process Communication
- Network Communication
- Fast Data Exchange

---

# 7. Symbolic Link (Soft Link)

## Definition

A Symbolic Link is a special file that points to another file or directory.

It works like a shortcut in Windows.

---

## Example

Original File

```text
notes.txt
```

Symbolic Link

```text
shortcut.txt → notes.txt
```

---

## Practical

Create original file

```bash
touch notes.txt
```

Create symbolic link

```bash
ln -s notes.txt shortcut.txt
```

Display

```bash
ls -l
```

Example Output

```text
shortcut.txt -> notes.txt
```

---

# File Type Symbols

When using:

```bash
ls -l
```

The first character indicates the file type.

| Symbol | File Type |
|---------|-----------|
| - | Regular File |
| d | Directory |
| l | Symbolic Link |
| c | Character Device |
| b | Block Device |
| p | Pipe |
| s | Socket |

---

# Practical (Ubuntu VirtualBox)

Open Terminal

```bash
Ctrl + Alt + T
```

Execute:

```bash
pwd

ls

ls -l

ls -a

file /bin/ls

mkdir Linux

touch notes.txt

ln -s notes.txt shortcut.txt
```

---

# Common Beginner Mistakes

### Mistake 1

Thinking Folder and File are the same.

Correct:

Directory stores files.

---

### Mistake 2

Opening Binary Files using `cat`.

Correct:

Use

```bash
file
```

to identify file type.

---

### Mistake 3

Deleting Hidden Files accidentally.

Files like:

```text
.bashrc
.profile
```

are important system configuration files.

---

# Real World Applications

## Software Developers

- Source Code Files
- Documentation Files
- Configuration Files

---

## Backend Developers

- Environment Files
- Log Files
- Database Configuration

---

## DevOps Engineers

- Configuration Files
- Symbolic Links
- Device Files
- Log Files

---

## Cloud Engineers

Linux servers use all these file types internally.

---

# Quick Revision

- UNIX supports seven major file types.
- Regular files store actual data.
- Text files are human readable.
- Binary files are machine readable.
- Directory files organize files.
- Device files represent hardware.
- Hidden files store configuration.
- Pipes transfer data between commands.
- Sockets enable process communication.
- Symbolic links act like shortcuts.

---

# Important Keywords

- Regular File
- Text File
- Binary File
- Directory File
- Device File
- Hidden File
- Pipe
- Socket
- Symbolic Link

---

# Frequently Asked Questions

### What is a Regular File?

A Regular File stores user data such as text, images, videos, and programs.

---

### What is a Hidden File?

A Hidden File begins with a dot (`.`) and stores configuration information.

---

### What is a Symbolic Link?

A Symbolic Link is a shortcut pointing to another file or directory.

---

# MCQ Questions

### Q1.

How many major file types are supported by UNIX?

A. 4

B. 5

C. 7

D. 9

**Answer:** C

---

### Q2.

Which file type stores configuration information?

A. Binary File

B. Hidden File

C. Device File

D. Pipe

**Answer:** B

---

### Q3.

Which command displays hidden files?

A. ls

B. ls -a

C. pwd

D. mkdir

**Answer:** B

---

### Q4.

Which file acts like a Windows Shortcut?

A. Pipe

B. Socket

C. Symbolic Link

D. Device File

**Answer:** C

---

### Q5.

Which command identifies the type of a file?

A. cat

B. file

C. ls

D. pwd

**Answer:** B

---

# 2 Marks Questions

1. Define Regular File.
2. Define Hidden File.
3. What is a Device File?
4. What is a Pipe?
5. Define Symbolic Link.

---

# 5 Marks Questions

1. Explain different types of files in UNIX.
2. Explain Text File and Binary File.
3. Explain Symbolic Link with example.

---

# Long Answer Questions

1. Explain all UNIX file types with suitable examples.
2. Explain the difference between Text Files and Binary Files.

---

# Viva Questions

- Why does UNIX treat devices as files?
- What is the difference between Text File and Binary File?
- What is a Symbolic Link?
- What are Hidden Files?

---

# Command Cheat Sheet

| Command | Purpose |
|----------|---------|
| `ls -l` | Show detailed file information |
| `ls -a` | Show hidden files |
| `file filename` | Identify file type |
| `mkdir dirname` | Create directory |
| `touch filename` | Create file |
| `ln -s source target` | Create symbolic link |

---

# Previous Year Exam Focus

⭐ Very Important

- Types of Files
- Text vs Binary File
- Hidden Files
- Symbolic Link
- File Type Symbols

---

## Continue Reading

➡️ **Part 3 – UNIX File System Structure (Boot Block, Super Block, Inode Block, Data Block)**