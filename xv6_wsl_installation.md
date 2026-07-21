# How to Set Up xv6 in WSL

This guide shows how to get xv6 running inside WSL.

## What xv6 is

xv6 is a small teaching operating system. It is not the Windows you use every day. It is a simple Linux-like system made for learning how operating systems work.

## Why you need QEMU

QEMU is the tool that runs xv6 like a tiny computer inside your computer. Without QEMU, xv6 cannot easily start on your machine.

## What WSL does

WSL lets Windows run Linux tools. That matters because xv6 projects usually use Linux commands and build tools.

## Before you begin

Make sure these things are ready:

- WSL is installed on Windows
- Ubuntu or another Linux distro is installed inside WSL
- QEMU is installed in WSL
- Basic build tools like `make` and `gcc` are available

## Install the basic tools

Open your WSL terminal and run:

```bash
sudo apt update
sudo apt install build-essential qemu-system-x86 qemu-utils
```

This gives you the tools needed to build and run xv6.

## Get into the xv6 folder

Go to the folder where the xv6 project is stored. For example:

```bash
cd ~/xv6-public
```

If your folder has a different name, use that instead.

## Build xv6

Run:

```bash
make clean
make
```

This step prepares xv6 so QEMU can run it.

## Start xv6

Run:

```bash
make qemu
```

If everything is set up correctly, xv6 should open inside QEMU.

## What to do if it fails

If xv6 does not start, check these common problems:

1. QEMU is not installed
2. You are not inside WSL
3. The xv6 project folder is incomplete
4. `make` is missing or failed earlier

## Simple way to think about it

Think of xv6 as a practice version of an operating system. WSL is the Linux workspace inside Windows. QEMU is the machine that lets xv6 run. All three work together so you can learn and test safely.

## Quick summary

Install the tools, open the xv6 folder, build it, and run `make qemu`.
