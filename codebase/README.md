# Codebase
Here, you will find an outline of all relevant Verilog HDL modules written for this project.
**alu.v:** Arithmetic Logic Unit; output forwarded to result_mux module to write to register, and pc module to update program counter.
**branch_logic.v:** Facilitates implementation of BRZ (branch if) instruction.
**control_fsm.v:** FSM for ASIP. Generates control signal outputs based on status inputs from other modules.
**datapath.v:** Datapath; connects outputs to inputs in accordance with Appendix B.
**decoder.v:** Instruction decoder. Sets outputs high based on which instruction is being pointed to by PC; output forwarded to control module.
**delay_counter.v:** Used for delay timing and motor pacing.
**immediate_extractor.v:** Extracts data from instruction being pointed to by PC; forwarded to Operand 2 multiplexer.
**instruction_rom.v:** Hardware implementation of the ASIP's instruction ROM (256 x 8 synchronous memory). Its contents can be viewed in instruction_rom.mif.
**lab5.v:** <u>Top-level module</u> which connects the datapath to the FSM and internal signals to output pins.
**op1_mux.v:** Selector for first operand forwarded to ALU.
**op2_mux.v:** Selector for second operand forwarded to ALU.
**pc.v:** Program counter.
**regfile.v:** Contains 4 registers, R0 through R3.
* R0 & R1: General purpose
* R2: Stepper motor position
* R3: Delay value
**result_mux.v:** Used to select between 00h (CLR instruction) or ALU output.
**stepper_rom.v:** Hardware implementation of the stepper's ROM (values are used to drive stepper motor rotation) (8 x 4 synchronous memory). Its contents can be viewed in stepper_rom.mif.
**temp_register.v:** Facilitates implementation of MOVR and MOVRHS instructions by counting half-steps.
**write_address_select.v:** Selects which register within the regfile module to be written to.