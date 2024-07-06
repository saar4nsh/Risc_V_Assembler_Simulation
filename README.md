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
testcases/: Directory containing test cases (bubble sort, quick sort, sqrt test).
branch_predictor_report: A report containing the information regarding the regarding the different branch prediction techniques used and the accuracy of each branch prediction technique
