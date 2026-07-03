---

# 1.3.2 Linux Booting Process

## Introduction

Whenever we press the **Power Button** of a computer, Linux does not start immediately.

The operating system follows a sequence of steps before the login screen appears.

This sequence is known as the **Linux Booting Process**.

Booting is the process of loading the operating system into the computer's main memory (RAM) so that the user can start using the system.

---

# What is Booting?

## Definition

**Booting** is the process of starting a computer and loading the operating system into memory.

Without the booting process, Linux cannot communicate with the hardware or start its services.

---

# Types of Booting

## 1. Cold Boot

A Cold Boot occurs when the computer is started from a completely powered-off state.

Example:

- Pressing the Power Button after shutting down the laptop.

---

## 2. Warm Boot

A Warm Boot occurs when the computer restarts without turning off the power.

Example:

```bash
sudo reboot
```

or

Restart option from Ubuntu Menu.

---

# Linux Booting Process

The Linux Boot Process consists of the following steps:

```text
Power ON
      │
      ▼
BIOS / UEFI
      │
      ▼
POST
      │
      ▼
Boot Loader (GRUB)
      │
      ▼
Linux Kernel
      │
      ▼
systemd (init)
      │
      ▼
System Services
      │
      ▼
Login Screen
      │
      ▼
Desktop (GNOME / KDE)
```

---

# Step 1 – Power ON

The boot process starts when the user presses the Power Button.

Electricity is supplied to all hardware components.

Examples:

- CPU
- RAM
- SSD/HDD
- Keyboard
- Mouse
- Monitor

---

# Step 2 – BIOS / UEFI

## BIOS

BIOS stands for

**Basic Input Output System**

It is firmware stored on the motherboard.

Its job is to:

- Detect hardware
- Check RAM
- Check CPU
- Check Storage Devices
- Start the Boot Loader

---

## UEFI

Modern computers use

**UEFI (Unified Extensible Firmware Interface)**

instead of BIOS.

Advantages of UEFI:

- Faster Boot
- Better Security
- Supports Large Hard Drives
- Better User Interface

---

# Step 3 – POST

POST stands for

**Power-On Self-Test**

During POST, the computer checks whether the hardware is working properly.

Hardware Checked:

- CPU
- RAM
- Keyboard
- Mouse
- Hard Disk / SSD
- Display

If a problem is found,

the system displays an error message or beep sound.

---

# Step 4 – Boot Loader (GRUB)

After POST is completed,

BIOS/UEFI loads the Boot Loader.

Linux commonly uses

**GRUB**

which stands for

**GRand Unified Bootloader**.

---

# Functions of GRUB

GRUB performs the following tasks:

- Displays Boot Menu
- Allows selection of Operating System
- Loads the Linux Kernel
- Passes control to the Kernel

Example:

```text
Ubuntu

Advanced Options

Windows Boot Manager
```

---

# Step 5 – Linux Kernel

After selecting Ubuntu,

GRUB loads the Linux Kernel into RAM.

The Kernel is the heart of Linux.

---

# Responsibilities of Kernel

The Kernel manages:

- CPU Scheduling
- Memory Management
- Device Drivers
- File System
- Process Management
- Input/Output Devices
- Security

---

# Step 6 – systemd (init)

Once the Kernel is loaded,

it starts the first user-space process called:

```text
systemd
```

Older Linux systems used

```text
init
```

Modern Ubuntu uses

```text
systemd
```

---

# Why systemd is Important?

systemd starts all essential services required by Linux.

Examples:

- Networking
- Bluetooth
- Printer
- Audio
- Login Manager
- Display Manager

Without systemd,

Linux cannot complete the boot process.

---

# Step 7 – Login Screen

After all services start successfully,

Linux displays the Login Screen.

The user enters:

- Username
- Password

Linux verifies the credentials.

---

# Step 8 – Desktop Environment

After successful login,

Linux loads the Desktop Environment.

Examples:

- GNOME
- KDE
- XFCE
- LXQt

Ubuntu uses

**GNOME**

by default.

---

# Complete Booting Diagram

```text
Power Button
      │
      ▼
BIOS / UEFI
      │
      ▼
POST
      │
      ▼
GRUB Boot Loader
      │
      ▼
Linux Kernel
      │
      ▼
systemd
      │
      ▼
System Services
      │
      ▼
Login Screen
      │
      ▼
GNOME Desktop
```

---

# Practical (Ubuntu VirtualBox)

## Check Kernel Version

```bash
uname -r
```

Example Output

```text
6.8.0-31-generic
```

---

## Check Operating System

```bash
cat /etc/os-release
```

---

## Check Current User

```bash
whoami
```

---

## Check First Process (systemd)

```bash
ps -p 1
```

Example Output

```text
PID TTY TIME CMD

1 ? 00:00:03 systemd
```

---

## Check System Information

```bash
hostnamectl
```

This command displays:

- Hostname
- Kernel Version
- Architecture
- Operating System

---

# Real World Usage

## Software Engineers

Understand startup services.

---

## Linux Administrators

Troubleshoot boot failures.

---

## DevOps Engineers

Manage Linux servers.

---

## Cloud Engineers

Debug AWS EC2 boot issues.

---

## Cyber Security Professionals

Analyze startup services for malware.

---

# Common Boot Problems

## GRUB Missing

Cause:

Boot Loader damaged.

Solution:

Repair GRUB.

---

## Kernel Panic

Cause:

Kernel cannot continue.

Solution:

Boot using Recovery Mode.

---

## Login Failure

Cause:

Wrong password.

Corrupted user files.

---

## systemd Failure

Cause:

Essential service failed.

Linux may enter Emergency Mode.

---

# Common Beginner Mistakes

### Mistake 1

Thinking BIOS loads Linux directly.

Correct:

BIOS loads the Boot Loader.

---

### Mistake 2

Thinking Kernel starts before GRUB.

Correct:

GRUB loads the Kernel.

---

### Mistake 3

Thinking Desktop starts immediately.

Correct:

systemd starts services first.

---

# Quick Revision

- Booting loads Linux into RAM.
- BIOS/UEFI checks hardware.
- POST verifies hardware.
- GRUB loads the Kernel.
- Kernel starts systemd.
- systemd starts services.
- Login Screen appears.
- Desktop loads.

---

# Important Keywords

- Booting
- BIOS
- UEFI
- POST
- GRUB
- Kernel
- systemd
- Login Manager

---

# MCQ Questions

### Q1

Booting means:

A. Shutting Down

B. Loading the Operating System

C. Formatting the Disk

D. Installing Linux

**Answer:** B

---

### Q2

POST stands for:

A. Power Operating System Test

B. Power-On Self-Test

C. Program Operating Service Test

D. Process Operating System Test

**Answer:** B

---

### Q3

Which Boot Loader is commonly used in Linux?

A. LILO

B. CMD

C. GRUB

D. Bash

**Answer:** C

---

### Q4

Which component is called the Heart of Linux?

A. Shell

B. Kernel

C. BIOS

D. GUI

**Answer:** B

---

### Q5

Which process has PID 1 in modern Ubuntu?

A. bash

B. init

C. systemd

D. login

**Answer:** C

---

# Interview Questions

- What is Booting?
- Explain the Linux Boot Process.
- What is GRUB?
- Why is systemd important?
- What is the difference between BIOS and UEFI?

---

# Viva Questions

1. Define Booting.
2. What is POST?
3. What is GRUB?
4. What is Kernel?
5. What is systemd?
6. Which process has PID 1?

---

# Related Topics

➡️ Continue in:

**14-Linux.md (Part 4)**

Topics Covered:

- GNOME
- KDE
- Linux Desktop Environment
- GNOME vs KDE
- Practical
- Complete MCQs
- Long Answer Questions
- Summary