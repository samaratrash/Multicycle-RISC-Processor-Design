# Multi-Cycle RISC Processor

## Project Overview

This project contains the implementation of a simple 16-bit multi-cycle RISC processor designed in Verilog. 

## Features

- **16-bit instruction and data size** with byte-addressable memory.
- **8 General-Purpose Registers** (R0 to R7), with R0 hardwired to zero.
- **Multi-cycle execution** for efficient instruction processing.
- **Instruction Set**: Supports R-Type, I-Type, J-Type, and S-Type instructions.
- **Separate Data and Instruction Memory** with Little Endian byte ordering.
- **ALU** with condition signal generation for branch outcomes (e.g., zero, carry, overflow).

## Instruction Set

The processor implements a subset of the following instruction formats:

- **R-Type**: AND, ADD, SUB
- **I-Type**: ADDI, ANDI, LW, SW, Branch instructions (BGT, BEQ, etc.)
- **J-Type**: JMP, CALL, RET
- **S-Type**: Store instruction

## Design Summary

- **Multi-cycle Design**: Instructions are divided across multiple cycles, including fetch, decode, execute, memory access, and write-back stages.
- **Control Path**: Control signals are generated for each cycle to manage the datapath.
- **ALU Operations**: Perform arithmetic, logic, and comparison operations.
- **Memory**: Separate instruction and data memories for efficient pipelining.

## Project Files

- `verilog/`: Contains the Verilog source files for the processor design.
- `testbench/`: Contains the testbenches used for simulation and verification.
- `datapath/` : Contains an image of the datapath


## Acknowledgements

This project was developed as part of the Computer Architecture course under the guidance of the Department of Electrical and Computer Engineering at Birzeit University.

