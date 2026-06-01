This project demonstrates the design and implementation of Random Access Memory (RAM) and Read Only Memory (ROM) using the Verilog Hardware Description Language (HDL). The objective is to understand memory modeling, data storage, and retrieval operations in digital systems through RTL design and simulation.

Features
Verilog implementation of RAM and ROM modules
Synchronous memory operations using a clock signal
Read and write functionality for RAM
Preloaded memory contents for ROM
Testbench for functional verification
Simulation-ready design for FPGA and ASIC learning

RAM-AND-ROM-USING-VERILOG/
│
├── ram.v          # RAM module
├── rom.v          # ROM module
├── ram_tb       # RAM testbench
├── rom_tb       # ROM testbench
└── README.md

RAM Description

Random Access Memory (RAM) is a volatile memory used for temporary data storage. Data can be both written to and read from RAM.

Inputs
clk : Clock signal
en : Enable signal
we : Write enable signal
addr : Memory address
data_in : Input data
Output
data_out : Output data
Operation
When en = 1 and we = 1, data is written into the specified memory location.
When en = 1 and we = 0, data is read from the specified memory location.
ROM Description

Read Only Memory (ROM) is a non-volatile memory that stores predefined data. Data can only be read during operation.

Inputs
clk : Clock signal
en : Enable signal
addr : Memory address
Output
data_out : Stored data at the specified address
Operation
ROM contents are initialized during design time.
Data is read based on the provided address when the enable signal is active.
Simulation
Using Icarus Verilog

Install Icarus Verilog and run:
iverilog -o ram_sim ram.v ram_tb.v
vvp ram_sim

iverilog -o rom_sim rom.v rom_tb.v
vvp rom_sim
gtkwave dump.vcd

Expected Results
RAM
Successful write operation to memory locations.
Correct retrieval of stored data during read operations.
ROM
Correct output data corresponding to initialized memory locations.
Read-only access without modification of stored contents.
Applications
Digital system design
FPGA prototyping
Embedded systems
Memory subsystem design
RTL design and verification learning
Learning Outcomes

Through this project, you will learn:

Verilog memory modeling techniques
Synchronous design concepts
Read and write operations in memory devices
Testbench development and simulation
RTL design and verification fundamentals
Tools Used
Verilog HDL
Icarus Verilog for simulation
GTKWave for waveform analysis
Author

Parnika Tanguturu
