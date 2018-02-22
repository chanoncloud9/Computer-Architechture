# Single Cycle MIPS

Summary:

In this assignment, you will implement an instruction-level simulator for a single cycle MIPS processor in C++ step by step. The simulator supports a subset of the MIPS instruction set and can model the execution of each instruction.

The MIPS program is provided to the simulator as a text file “imem.txt” file which is used to initialize the Instruction Memory. Each line of the file corresponds to a Byte stored in the Instruction Memory in binary format, with the first line at address 0, the next line at address 1 and so on. Four contiguous lines correspond to a whole instruction. Note that the words stored in memory are in “Big-Endian” format, meaning that the most significant byte is stored first.

We have defined a “halt” instruction as 32’b1 (0xFFFFFFFF) which is the last instruction in every “imem.txt” file. As the name suggests, when this instruction is fetched, the simulation is terminated. We will provide a sample “imem.txt” file containing a MIPS program. You are encouraged to generate other “imem.txt” files to test your simulator.

The Data Memory is initialized using the “dmem.txt” file. The format of the stored words is the same as the Instruction Memory. As with the instruction memory, the data memory addresses also begin at 0 and increment by one in each line.

The instructions that the simulator supports and their encodings are shown in Table 1. Note that all instructions, except for “halt”, exist in the MIPS ISA. The MIPS Green Sheet from HW1 defines the semantics of each instruction.

Name
Format Type
Opcode (Hex)
Func (Hex)

addu
R-Type
00
21

subu
R-Type
00
23

addiu
I-T ype
09
 
and
R-Type
00
24
 
or
R-Type
00
25

nor
R-Type
00
27
 
beq
I-Type
04

j
J-Type
02

lw 
I-Type
23

sw
I-Type
2B

halt 
J-Type
3F

useful references for this:
A brief introduction to C++ (https://web.eecs.umich.edu/~sugih/pointers/c++.pdf)
A reference for the C++ bitset class (http://www.cplusplus.com/reference/bitset/bitset/) 
A reference to the C++ string class (http://www.cplusplus.com/reference/string/string/)
