---
layout: post
title: Let's build a DOS .EXE like it's 1992
---

# Let's build a DOS .EXE like it's 1992

## Introduction

In this post, we will build a simple DOS .EXE file from scratch. We will use 
the NASM assembler and the OpenWatcom C compiler to create a simple program 
that prints "Hello, World!" to the console.

We have tried to recreate an environment that is similar to what a developer
would have used in 1992. 

## Prerequisites

You will need the following tools to follow along with this post:

- NASM assembler
- OpenWatcom C compiler (wlink)
- FreeDOS
- A text editor (FED)

We'll use NASM to write the assembly code for our program, OpenWatcom to link 
the assembly code with the C runtime library, and FreeDOS to run the resulting
.EXE file. (this was not as easily done in 1992, or 2025) 

## Setting up the environment

First, download and install the NASM assembler and the OpenWatcom C compiler
on your system. 

## Building the program

First, create a new file called `hello.asm` and add the following code:

```assembly

section .text
    global _start

_start:
    mov ah, 9
    mov dx, msg
    int 21h
    mov ah, 4ch
    int 21h

section .data
    msg db 'Hello, World!', 0

```

Next we need to compile the assembly code using NASM:

```bash
nasm -f obj hello.asm
```

the we need to link the object file with the OpenWatcom C runtime library:

```bash
wlink sys dos name hello.exe start=_start file hello.obj
```

Breakng this down a bit, the `sys dos` option tells the linker to create a
DOS executable file. The `name hello.exe` option specifies the name of the
output file. The `start=_start` option tells the linker to use the `_start`
symbol as the entry point of the program. The `file hello.obj` option tells
the linker to link the `hello.obj` file with the C runtime library.

## Running the program

To run the program, copy the `hello.exe` file to a FreeDOS system and run it
from the command line. You should see the message "Hello, World!" printed to
the console.

## Conclusion

In this post, we built a simple DOS .EXE file from scratch using the NASM
assembler and the OpenWatcom C compiler. We used FreeDOS to run the resulting
.EXE file and saw the message "Hello, World!" printed to the console. This
demonstrates how to create a simple DOS program using tools that were commonly
used in 1992.

I hope you found this post helpful. If you have any questions or comments,
please feel free to contact me.
