# MIPS-I-architecture-emulator
 A simple MIPS processor simulator written in Python. The goal is to provide an educational and research-oriented implementation that models the core functionality of a MIPS CPU, including instruction fetch, decode, execution, memory access, and write-back.<br/>

This project can be used to explore computer architecture concepts, test MIPS assembly programs, or serve as a base for further research and development.

## Features

- Simulates a subset of the MIPS-I (32-bit) instruction set
- Instruction types supported:
  - Arithmetic and logical instructions (`add`, `sub`, `and`, `or`, `slt`)
  - Immediate instructions (`addi`, `andi`, `ori`)
  - Memory access instructions (`lw`, `sw`)
  - Control flow instructions (`beq`, `bne`, `j`)
  - System call simulation (`syscall`)
- Implements major CPU components:
  - Register file
  - ALU
  - Memory unit
  - Control logic
- Instruction-level simulation with clear output of register and memory state

## Project Structure

- alu.py - Arithmetic and logic unit
- memory.py - Simulated memory model
- register_file.py - Register file with 32 MIPS registers
- instruction.py - Instruction parsing and decoding
- control_unit.py - Control signal logic
- cpu.py - Core simulation engine
- program.txt - Sample MIPS assembly input
- main.py - Entry point for simulation

## Example

Input Program (program.txt):<br/>
```
addi $t0, $zero, 5 
addi $t1, $zero, 10
add $t2, $t0, $t1
```

Expected Output:<br/>
```
$t0 = 5 
$t1 = 10
$t2 = 15
```

## Getting Started

### Requirements

- Python 3.7 or higher

### Running the Simulator

1. Clone this repository:<br/>
```
git clone https://github.com/achintyaPiko/MIPS-I-Architecture-Emulator.git
cd MIPS-I-Architecture-Emulator
```
2. Run the simulator:<br/>
```
python main.py
```
3. Edit `program.txt` to write your own MIPS assembly programs.

## Learning Objectives

This project aims to:

- Demonstrate the core structure and operation of a MIPS32 CPU
- Help learners understand CPU pipeline stages (if extended)
- Support instruction-level debugging and visualization
- Provide a foundation for future enhancements such as pipelining, caching, or hardware translation

## Future Work

- Support for full MIPS32 instruction set
- Assembler integration for raw `.asm` files
- C-based version for embedded system simulation
- GUI for visualization of instruction cycles and registers
- Verilog implementation of the above architecture for FPGA  

## License

This project is licensed under the MIT License. See the LICENSE file for details.

## Reference Used<br/>
[MIPS-I Assembly Language Instruction Set](https://user.eng.umd.edu/~manoj/759M/MIPSALM.html)<br/>
[MIPS Green Sheet](https://courses.cs.washington.edu/courses/cse378/09au/MIPS_Green_Sheet.pdf)


GitHub: https://github.com/achintyaPiko


