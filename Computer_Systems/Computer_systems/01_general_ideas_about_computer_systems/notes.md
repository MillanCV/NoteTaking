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

## What is a shell?

It's a command-line interpreter that prints prompts and waits for the user to introduce commands to execute them. If the command is not one of the built in commands the shell asumes that it is a executable file to be loaded and to be run.

## Why programmers need to understand compilation systems?

To optimize programs, avoid security problems and understand linking problems.

## What is a word?

It is a chunck of bytes. Normally 4 bytes or 8 bytes.

## What is a bus?

An electrical conduit that carry bytes between components.

## What is an I/O device?

They are devices to connect to the external world.

## How I/O devices are connected to the computer?

They are connected to the I/O bus, by a controller or by an adapter. Both transfer information betwwn the I/O bus and the I/O device.

## What is the main memory?

The RAM, is a temporary storage that holds programs and data that the processor manipulates during the exection of a program.

## How is organized the main memory?

As a linear array of bytes, each one with an address.

## What is the CPU?

Is the central processing unit or processor.

## What does the CPU? 

Interprets instructions stored in main memory.

## What is the Program Counter?

Is a word-size register that points at some machine-language instruction in main memory.

## What does de CPU?

Execute repeatdly the instruction pointed by the PC. Read the counter, interpretates the bits in the instruction, perfom a simple operation, updates the pc to point to the next instruction.

## What is the ALU?

The arithmetic/logic unit in the CPU that computes new data and addreses.

## What is the register file?

A storage device word size in the CPU.

## What tipical operations does the CPU?

Load, store, operate, jump.

## What is a load operation?

Copy a byte or word from main memory into a register overwriting.

## What is a store operation?

Copy a byte or word from a register to a location in main memory overwriting

## What is an operate operation?

Copy the content of two registers to the ALU, perform an arithmetic operation and store the result in a register.

## What is a jump operation?

Extract a word from the instruction a copy the word in the program counter.

## Describe what happens when you enter a command in a shell and enter is pressed

* The shell reads each character into a register and then stores it in memory
* After hitting enter the shell loads the executable hello copying code and data from hello executable object file from disk to main memory.
	* This data movement goes directly from disk to memory thanks to DMA, direct memory access.
* While loaded in memory, processor starts to execute the instructions in the main routine of program hello.
	* Instructions in program copy the bites of "hello, world\n" from memory to register file, and from there to display device.

## Is moving information a costly operation?

Yes, system designers should made these operations run as fast as possible.

## Compare storage devices

Larger storage are slower than smallers. Slower are cheaper.

## Compare processor evolution vs memory evolution

Is easier and cheaper to make processor run faster, which brings the processor-memory gap.

## How to deal with processor-memory gap

With cache memories that serves as temporary stagins areas that processor will need in near future.

## What is locality when running a program?

Is the tendency to access data and code in localized regions.

## How caches exploits locality to increase performance?

Setting up caches to hold data that i likely to be accesed often. This drives to perfom most meory operations using fast caches.

## How are storages organized in a system?

They form a memory hierarchy with a piramid shape. On top the fastest, smallest and more costly per bit. On the bottom the larger, larger and less costly. From the registers, caches L1, L2, L3, main memory, locals disks and remote disks.

## What is the main idea of the memory hierachy?

Each level serves as a cache for the next lower level.
