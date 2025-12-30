# RAM-DESIGN

*COMPANY*: CODTECH IT SOLUTIONS PVT LTD

*NAME*: GUJJULA TIRUPATHI REDDY

*INTERN ID*: CTIS0865

*DOMAIN*: VLSI

*DURATION*: 24 WEEKS

*DESCRIPTION*:
Random Access Memory (RAM) is a fundamental memory element used in digital systems for temporary data storage and fast data retrieval. In processors, microcontrollers, and FPGA-based systems, RAM enables efficient program execution by storing intermediate values, instructions, and data. In this project, a simple synchronous RAM was designed using Verilog along with its testbench and simulation results. The purpose of this project was to understand memory architecture, read/write operations, synchronous behavior, and functional verification using HDL simulation tools.

The RAM designed for this project is an 8-bit wide, 16-location synchronous memory, meaning each memory location stores 8 bits, and the RAM contains 16 addressable locations. The term “synchronous” means both read and write operations occur only on the rising edge of the clock signal. This ensures predictable timing, making it suitable for use in synchronous digital systems such as CPUs and DSPs.

Working Principle

The RAM has four primary inputs: clock, write enable (we), address, and data input, along with one output, data out. When the write enable signal is HIGH during a clock edge, the data present at the input is stored at the selected memory address. When write enable is LOW, the RAM performs a read operation and outputs the data stored at the given address. The design uses a two-dimensional register array in Verilog to model memory (reg [7:0] mem [0:15]). On every rising clock edge, the system checks whether to read or write. This ensures deterministic behavior and avoids race conditions.

Simulation and Verification

A comprehensive Verilog testbench was created to verify correct RAM functionality. The testbench generates a clock, initializes the RAM, performs multiple write cycles, and then reads back the stored values. For example, the testbench writes values like 8'hAA, 8'h55, and 8'hF0 into memory addresses 0, 1, and 2 respectively. In the subsequent cycles, read operations retrieve these values, confirming the correctness of the RAM.
Waveform simulations in tools such as Vivado Simulator clearly show write events happening at rising clock edges, followed by correct read-back data. The simulation validates that the internal memory array correctly retains values and that data output transitions occur synchronously. This verification process ensures that both functional correctness and timing behavior meet design expectations.

Tools Used

The RAM was coded in Verilog HDL, which synthesizes efficiently on most FPGA platforms. For simulation, standard tools such as Vivado can be used. These tools provide waveform viewers, memory inspectors, and debugging consoles that help confirm design correctness. On FPGA hardware, the RAM can be synthesized using Xilinx Vivado where block RAM resources (BRAM) can be inferred from the HDL code.

Performance Analysis
The designed RAM performs efficiently due to its synchronous operation and simple architecture. Latency equals one clock cycle since both read and write operations occur only on clock edges. Throughput is one operation per cycle, making it suitable for high-speed digital systems. Since the RAM is implemented as registers, it offers high access speed but uses more hardware resources compared to large block RAMs. Power consumption remains low due to reduced switching activity inside the controlled synchronous design. This makes the RAM suitable for small embedded systems, memory buffers, or instruction storage.

*OUTPUT*:

![Image](https://github.com/user-attachments/assets/2c086f1d-6e14-430f-b32b-92d43aa44684)
