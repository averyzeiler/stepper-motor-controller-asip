# Codebase
Here, you will find an outline of all relevant Verilog HDL modules written for this project.<br>
<br>**alu.v:** Arithmetic Logic Unit; output forwarded to result_mux module to write to register, and pc module to update program counter.<br>
**branch_logic.v:** Facilitates implementation of BRZ (branch if) instruction.<br>
**control_fsm.v:** FSM for ASIP. Generates control signal outputs based on status inputs from other modules.<br>
**datapath.v:** Datapath; connects outputs to inputs in accordance with Appendix B.<br>
**decoder.v:** Instruction decoder. Sets outputs high based on which instruction is being pointed to by PC; output forwarded to control module.<br>
**delay_counter.v:** Used for delay timing and motor pacing.<br>
**immediate_extractor.v:** Extracts data from instruction being pointed to by PC; forwarded to Operand 2 multiplexer.<br>
**instruction_rom.v:** Hardware implementation of the ASIP's instruction ROM (256 x 8 synchronous memory). Its contents can be viewed in instruction_rom.mif.<br>
**lab5.v:** <u>Top-level module</u> which connects the datapath to the FSM and internal signals to output pins.<br>
**op1_mux.v:** Selector for first operand forwarded to ALU.<br>
**op2_mux.v:** Selector for second operand forwarded to ALU.<br>
**pc.v:** Program counter.<br>
**regfile.v:** Contains 4 registers, R0 through R3.
* R0 & R1: General purpose
* R2: Stepper motor position
* R3: Delay value

**result_mux.v:** Used to select between 00h (CLR instruction) or ALU output.<br>
**stepper_rom.v:** Hardware implementation of the stepper's ROM (values are used to drive stepper motor rotation) (8 x 4 synchronous memory). Its contents can be viewed in stepper_rom.mif.<br>
**temp_register.v:** Facilitates implementation of MOVR and MOVRHS instructions by counting half-steps.<br>
**write_address_select.v:** Selects which register within the regfile module to be written to.
