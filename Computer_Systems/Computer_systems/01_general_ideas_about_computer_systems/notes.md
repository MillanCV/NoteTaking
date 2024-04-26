## What type of files can we find in a computer?

There are two types of files, text files and binary files

## If you write a hello_world program and you save in a file called hello.c what do you have?

I have a source program saved in a text file as a sequence of bytes. Each byte represents a character that i wrote.

## How text is organized on a text file?

The text file contains a sequence of bits, organized in bytes. Each byte represents a character.

## What is ASCII?

Is a standard to represent characters with unique byte-size integer value.

## How is information represented in a system?

It is always represented as a bunch of bits.

## How can we know that some bits on a file represents integers, floats, ascii characters... ?

It depends of the context. Dependings of the context the same sequence of bits can represent different things.

## Are numbers in a computer the same that numbers in life?

No, they are just finite aproximations, that can behave in unexpected ways.

## Can I execute directly a hello.c file?

No, it has to be transformed into a sequence of low-level machine-language instructions packed as a executable object program and stored as a binary file, also called executable object files.

## Can I manually transform a hello.c into an executable object file?

No, I need a program or programs to do it. In linux i would need a compiler driver.

## What are the phases of c files compilation system, especifying with programs and outputs?

* Pre-processor: hello.c -> cpp -> hello.i (modified source program)
* Compiler: hello.i -> cc1 -> hello.a (assembly program)
* Assembler: hello.a -> as -> hello.o (relocatable objecto program)
* Linker: hello.o -> ld -> hello (binary)

##  What happens in the pre-processor phase?

The pre-processor modifies the source program according to directives that starts wit '#' like '#include <stdio.h>', that reads that header and inserts it into the program text.

## What happens in the compilation phase?

The compiler transform the source file into a text file that contains an assembly-language program

## What happens in the assembly phase?

The assembler translates the .a text file into machine-language instructions and packages them in a form known as relocatable object program. This file is a binary file.

## What happens in the linking phase?

The linker merge the hello.o with other separated object files required into the executable object file ready to be loaded into memory and executed by the system.
