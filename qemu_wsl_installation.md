# How to Install QEMU in WSL

This guide shows how to install QEMU inside WSL.

## What QEMU is

QEMU is a tool that lets you run another operating system or a tiny virtual machine inside your computer. In this project, it helps you run xv6 without needing separate hardware.

## What WSL is

WSL means Windows Subsystem for Linux. It lets you use Linux tools on Windows. If you are on Windows and want to work on Linux-style projects, WSL is the easiest path.

## Before you start

Make sure:

- WSL is installed on your Windows machine
- You have a Linux distribution like Ubuntu installed in WSL
- Your WSL version is WSL 2, not WSL 1, because WSL 2 works better with virtualization tools

## Install QEMU

Open your WSL terminal and run these commands:

```bash
sudo apt update
sudo apt install qemu-system-x86 qemu-utils
```

If Ubuntu asks for your password, type the one you use for WSL.

## Check that it worked

Run this command:

```bash
qemu-system-x86_64 --version
```

If you see a version number, QEMU is installed correctly.

## Why these packages matter

- qemu-system-x86 gives you the main QEMU emulator for x86 machines
- qemu-utils adds helpful extra tools

## If the command is not found

If WSL says QEMU is missing, try these steps:

1. Run sudo apt update again
2. Re-run the install command
3. Make sure you are inside the WSL terminal, not Windows PowerShell

## Simple idea to remember

Think of QEMU as a small computer inside your real computer. WSL is the Linux room inside Windows. This setup lets you run Linux-based school or project tools from your Windows laptop.

## For xv6 users

After QEMU is installed, you can use it to run xv6 commands from the project folder.
