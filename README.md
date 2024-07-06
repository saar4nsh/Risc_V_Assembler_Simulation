# Risc_V_Assembler_and_Branch_Predictor_Simulator

# Overview
This project implements a RISC-V assembler and a branch predictor simulator in C++. The assembler converts RISC-V assembly code into machine code, while the branch predictor simulates different branch prediction strategies.

# Features
# Assembler
Input: RISC-V assembly code in a .asm file.
Output: Machine code in a .mc file.
Instruction Support: Limited to 31 RISC-V 32-bit ISA instructions (R, I, S, SB, U, UJ formats).
Assembler Directives: .text, .data, .byte, .half, .word, .dword, .asciz.
Segments: Code, data, heap, and stack segments.

# Branch Predictor
# Methods:
Always taken
Always not-taken
1-bit dynamic predictor
2-bit dynamic predictor
# Components:
Branch target buffer
History table
Output: Overall accuracy of the branch predictor and the branch target buffer.

# File Structure
assembler.cpp: Implementation of the RISC-V assembler.
branch_predictor.cpp: Implementation of the branch predictor simulator.
README.md: Project documentation.
testcases.zip: Directory containing test cases (bubble sort, quick sort, sqrt test).
branch_predictor_report: A report containing the information regarding the regarding the different branch prediction techniques used and the accuracy of each branch prediction technique

# Usage
# Assembler
# 1. Compile:
```terminal
g++ assembler.cpp -o assembler
```
# 2. Run:
```terminal
./assembler input.asm output.mc
```
# Branch Predictor
# Compile:
```terminal
g++ branch_predictor.cpp -o branch_predictor
```

# Run:
```terminal
./branch_predictor trace_file.txt
```

# Example
# Assembler Input ("input.asm"):
``` .asm
.text
add x1, x2, x3
andi x5, x6, 10
```
# Assembler Output ("output.mc"):
``` .text
0x0 0x003100B3
0x4 0x00A37293
0x8 0x00000000
```
# Branch Predictor Trace ("trace_file.txt"):
``` .text
0x0    0x00000293    addi x5 x0 0
0x4    0x00A28333    add x6 x5 x10
...
```

