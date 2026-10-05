# Stepper Motor Controller ASIP
This project involved designing and implementing a custom Application-Specific Instruction Set Processor (ASIP) in Verilog HDL to control a stepper motor using an Intel/Altera Cyclone V FPGA on a DE1-SoC development board.
## Project Summary
### Goal
To design, simulate, debug, and deploy a complete ASIP based on datapath and control unit descriptions, to practise using available on-chip memory modules, and to learn how a simple processor operates on a cycle-by-cycle basis.
### Process
The project required writing Verilog for the processor modules, connecting the datapath, implementing the control FSM, and creating assembly-level programs that were manually encoded into machine code. Individual modules were simulated and debugged before being combined into the complete processor.
The final design was deployed to the FPGA and connected to the stepper motor through an external SN754410NE motor-driver interface. Quartus Prime and the Signal Tap Logic Analyzer were used to simulate, test, and debug the design on external stepper motor hardware.
## ASIP Structure
The ASIP uses 8-bit instructions and data stored in instruction memory, which are fetched, decoded, and used to produce predictable system behaviour for all 12 available instructions. It contains a register file which consists of 4 8-bit registers used for general-purpose functionality, stepper motor position storage, and delay timing. The ASIP also contains an immediate extractor, ALU, multiplexers, a stepper ROM, and additional counters and registers.
To learn more about the individual modules and their functions, click here.
## Repository Structure
**assignment:** Contains all files detailing the assignment outline and desired design.
**codebase:** Final implementation of the stepper motor controller ASIP project.