![image](https://github.com/AnoushkaTripathi/NIELIT-INTERNSHIP-ON-HLS-PROGRAMMING/assets/98522737/0532da74-92ae-4b9e-935b-68390bdacd12)

# NIELIT-INTERNSHIP-ON-HLS-PROGRAMMING


<details>

<summary> WEEK 1</summary>

# DAY 1 - Introduction to HLS programming

![image](https://github.com/AnoushkaTripathi/NIELIT-INTERNSHIP-ON-HLS-PROGRAMMING/assets/98522737/b5400a7f-5283-4e22-9c73-81e22c7296dc)

Applications of FPGA

![Screenshot 2024-06-06 164353vxvx](https://github.com/AnoushkaTripathi/NIELIT-INTERNSHIP-ON-HLS-PROGRAMMING/assets/98522737/326b3492-9bd2-487d-bddf-cbbb4b78f398)

FPGA Design Approach

![image](https://github.com/AnoushkaTripathi/NIELIT-INTERNSHIP-ON-HLS-PROGRAMMING/assets/98522737/95d75d24-ecc2-465d-bed3-0c0fa2635069)


![image](https://github.com/AnoushkaTripathi/NIELIT-INTERNSHIP-ON-HLS-PROGRAMMING/assets/98522737/706199ab-8905-46f1-9912-0f3f69819e73)



HLS in Industries
 - NVIDIA for designing embedded GPU
 - Google in building VP9 encoder/decoder
 - AMD in desigining Microprocessor
 - STM for H.265



Why do we need FPGA?

![image](https://github.com/AnoushkaTripathi/NIELIT-INTERNSHIP-ON-HLS-PROGRAMMING/assets/98522737/e9ac96b5-5bb7-4c79-bdc0-d3ae46ca7e62)


FPGA and CPU both can have logic synthesis

CPU have a OS on it whereas FPGA don't than why should we work with FPGA

FPGA Vs CPU

![image](https://github.com/AnoushkaTripathi/NIELIT-INTERNSHIP-ON-HLS-PROGRAMMING/assets/98522737/2a299adf-69f7-468f-bf91-59b1fe475903)

| FPGA | CPU | 
|----------|----------|
| Computing platform with no predefined hardware architecture,each C/C++ program we create have it's own optimized hardware architecture| CPUs are computing platform with fixed hardware architecture, generic to perform any logical algorithmic function as long as it is compiled into CPU instructions| 
|  Translate C functions into hardware block,that is why it can perform operations in parallel   | In CPU compiler translate c function to assembly language,sequential execution|
| Parallelism | Sequential execution |
![image](https://github.com/AnoushkaTripathi/NIELIT-INTERNSHIP-ON-HLS-PROGRAMMING/assets/98522737/509b3a9f-effb-441f-800f-6f88dfb3f8c3)


Computing Structure of CPU

 ![image](https://github.com/AnoushkaTripathi/NIELIT-INTERNSHIP-ON-HLS-PROGRAMMING/assets/98522737/94d767fb-62ff-4c1e-879d-7487481757c5)

![image](https://github.com/AnoushkaTripathi/NIELIT-INTERNSHIP-ON-HLS-PROGRAMMING/assets/98522737/def5c085-0ed6-4c28-aa13-5a3cb9b76983)

**FPGA computing structure**

![image](https://github.com/AnoushkaTripathi/NIELIT-INTERNSHIP-ON-HLS-PROGRAMMING/assets/98522737/f39c0553-7a34-4c7a-9722-cee2f2a8b368)


![image](https://github.com/AnoushkaTripathi/NIELIT-INTERNSHIP-ON-HLS-PROGRAMMING/assets/98522737/dd550fd3-7415-408b-b4e9-c9c3ec0af5fd)
 
 GPU also performs parallelism , but every application is not suitable for GPU

 # FPGA BASICS

 **FPGA Structure**

 ![image](https://github.com/AnoushkaTripathi/NIELIT-INTERNSHIP-ON-HLS-PROGRAMMING/assets/98522737/94d34fb8-d4d1-4c61-981d-2115e2bf1e1f)

## FPGA Application Layer and Configuration Layer

In FPGA (Field-Programmable Gate Array) design, understanding the application layer and configuration layer is essential. Let's explore these layers:

## 1. Application Layer

- **Purpose:**
  - The application layer represents the top-level functionality implemented on the FPGA.
  - It includes user-defined logic, custom IP cores, and specific algorithms.
  - Designers create and program this layer to perform specific tasks or computations.

## 2. Configuration Layer

- **Purpose:**
  - The configuration layer handles the initial setup of the FPGA.
  - It involves loading the configuration data into the FPGA's memory elements (such as SRAM cells or flash memory).
  - The configuration layer determines how the FPGA behaves during operation.
![image](https://github.com/AnoushkaTripathi/NIELIT-INTERNSHIP-ON-HLS-PROGRAMMING/assets/98522737/ead615e2-0ece-4001-8a89-66fe0264d99e)

An LUT (LookUp Table) in FPGA design is a fundamental building block. It can implement any Boolean function of N input variables. Essentially, an LUT acts as a truth table, defining how your combinatorial logic behaves. When an FPGA is configured, it fills in the LUT with output values, which are stored in SRAM bits. The same physical LUT can implement different logic functions by changing the LUT-Mask (the truth table). Think of LUTs as memory, where inputs serve as addresses, and outputs are the data stored in those addresses

# FPGA Design Flow and Basic Elements

## FPGA Design Flow

The FPGA (Field-Programmable Gate Array) design flow involves several critical steps to ensure the successful implementation of digital circuits. Below is an overview of the typical stages:

1. **Specification**: Define the requirements and functionality of the design.
2. **Design Entry**: Create the design using hardware description languages (HDL) such as VHDL or Verilog, or through schematic entry.
3. **Synthesis**: Convert the HDL code into a gate-level netlist.
4. **Implementation**: Map, place, and route the netlist onto the FPGA fabric. This involves:
   - **Mapping**: Assign logic to specific resources.
   - **Placement**: Determine the physical locations of logic blocks.
   - **Routing**: Establish the connections between the placed blocks.
5. **Simulation**: Verify the design functionality at various stages (pre-synthesis, post-synthesis, and post-implementation) using simulation tools.
6. **Configuration**: Program the FPGA with the final design using configuration files.
7. **Validation and Testing**: Test the programmed FPGA in the real hardware environment to ensure it meets the specified requirements.
   ![image](https://github.com/user-attachments/assets/0e8f9dcd-a684-4531-8507-9c577859f839)


## FPGA Basic Elements

FPGA consists of several fundamental components:

- **Logic Blocks**: The basic computational units, typically comprising lookup tables (LUTs), flip-flops, and multiplexers. They perform the primary logic functions.
- **Interconnects**: The routing resources that connect the logic blocks. They allow for complex signal routing within the FPGA.
- **I/O Blocks**: Interfaces that connect the internal FPGA logic to the external pins of the device. They manage input and output signals.
- **Clock Management**: Components like PLLs (Phase-Locked Loops) and MMCMs (Mixed-Mode Clock Managers) for clock distribution and timing management.
- **Embedded Memory**: Blocks of memory such as RAM and ROM within the FPGA for data storage and buffering.
- **DSP Blocks**: Dedicated blocks for digital signal processing tasks, offering efficient implementation of arithmetic operations.

![image](https://github.com/user-attachments/assets/433a6f87-1803-4076-a827-cf78efdb987d)

# LUT Example

A Look-Up Table (LUT) is a fundamental component in digital logic design, particularly in FPGAs (Field-Programmable Gate Arrays). It is used to implement combinational logic functions. The LUT works by mapping input combinations to their corresponding output values based on a pre-defined truth table.

## Understanding LUT with the Provided Example

### Given Logic Function
The logic function provided is:
\[ d = (\neg a \land b) \lor c \]
where `a`, `b`, and `c` are inputs, and `d` is the output.

### Truth Table
The truth table lists all possible combinations of inputs `a`, `b`, and `c`, and their corresponding output `d` based on the given logic function.

| a | b | c | d |
|---|---|---|---|
| 0 | 0 | 0 | 0 |
| 1 | 0 | 0 | 0 |
| 0 | 1 | 0 | 1 |
| 1 | 1 | 0 | 0 |
| 0 | 0 | 1 | 1 |
| 1 | 0 | 1 | 1 |
| 0 | 1 | 1 | 1 |
| 1 | 1 | 1 | 1 |

### LUT Implementation
A LUT can be visualized as a table that stores output values for each possible input combination. For a 3-input LUT (as in this example), there are \( 2^3 = 8 \) possible input combinations.

- **Inputs**: The inputs `a`, `b`, and `c` are fed into the LUT.
- **Output**: The LUT outputs the value `d` based on the combination of inputs.

## How LUT Works

### Inputs Mapping
- Each combination of inputs `(a, b, c)` is treated as an address to access a specific location in the LUT.
- For instance, if `a = 0`, `b = 0`, and `c = 0`, this combination points to the first row in the truth table, resulting in `d = 0`.

### Output Determination
- The LUT stores the output values for each input combination based on the truth table.
- When a specific combination of inputs is applied to the LUT, it outputs the pre-stored value for that combination.

## Example Walkthrough

- **Input Combination (0, 0, 0)**:
  - The combination `a = 0`, `b = 0`, `c = 0` corresponds to the first row in the truth table, giving `d = 0`.

- **Input Combination (0, 1, 0)**:
  - The combination `a = 0`, `b = 1`, `c = 0` corresponds to the third row in the truth table, giving `d = 1`.

- **Input Combination (1, 1, 1)**:
  - The combination `a = 1`, `b = 1`, `c = 1` corresponds to the last row in the truth table, giving `d = 1`.

![image](https://github.com/user-attachments/assets/eeae876c-3526-4118-b6bb-a26af6fede80)


- The diagram on the right shows a LUT with three inputs (`a`, `b`, `c`) and one output (`d`).
- The truth table on the left provides the mapping of inputs to the corresponding output values.
- When the inputs are applied to the LUT, it looks up the pre-stored value based on the input combination and produces the output.

# FPGA Architecture: Slices, Configuration Logic Block, and Overall FPGA Structure

This document provides an explanation of key components in FPGA architecture, focusing on slices, configuration logic blocks, and the overall FPGA structure. The images included illustrate these components in the context of Xilinx's 7 Series FPGAs.

## Slices

![image](https://github.com/user-attachments/assets/89ae7b94-8c41-401e-8ad2-91efbea21bbf)


A slice is a fundamental building block within an FPGA's Configurable Logic Block (CLB). Each slice contains multiple Look-Up Tables (LUTs), flip-flops, and multiplexers. These elements are used to implement combinational and sequential logic functions.

- **Components of a Slice**:
  - **LUTs (Look-Up Tables)**: Used for implementing combinational logic.
  - **Flip-Flops**: Used for storing state information and implementing sequential logic.
  - **Multiplexers**: Used for routing signals within the slice and to/from the CLB.

The image illustrates the internal structure of a slice, showing how these components are interconnected to form complex logic functions.

## Configuration Logic Block (CLB)

![image](https://github.com/user-attachments/assets/d8f1f495-1cec-4d30-9ba4-ffee76deb141)


A CLB is a larger building block within an FPGA that contains multiple slices. The CLB provides the necessary routing and switching logic to connect slices to each other and to other parts of the FPGA.

- **Components of a CLB**:
  - **Slices**: Each CLB contains multiple slices (usually two in Xilinx FPGAs).
  - **Switch Matrix**: Facilitates the routing of signals between slices and to/from other CLBs.
  - **CIN/COUT (Carry In/Carry Out)**: Used for implementing fast carry chains in arithmetic operations.

The image shows the structure of a CLB, highlighting its internal slices and the switch matrix used for routing signals.

## Overall FPGA Architecture

![image](https://github.com/user-attachments/assets/503766f1-6909-464c-8c7a-02347f6af7c6)


The overall FPGA architecture consists of an array of CLBs, each containing multiple slices. The CLBs are interconnected by a complex routing matrix, allowing for flexible signal routing and interconnection.

- **Components of FPGA Architecture**:
  - **CLBs (Configurable Logic Blocks)**: The primary building blocks containing slices.
  - **Switch Matrix**: Facilitates the routing of signals between CLBs.
  - **I/O Pads**: Used for interfacing the FPGA with external signals and devices.
  - **Wires**: Interconnect the CLBs and other components within the FPGA.
    ![image](https://github.com/user-attachments/assets/208302cc-f576-47a0-be2b-eddbe3b697cf)
High-Level Synthesis (HLS) involves two main tasks:

1. **Function Synthesis**:
   - **Objective**: Convert the software function into a hardware module.
   - **Process**: Translate the function body into hardware logic, optimizing for parallelism.
   - **Components**: Input ports (arguments), function body (logic), output ports (arguments).

2. **Interface Synthesis**:
   - **Objective**: Define the communication protocols for the hardware module.
   - **Process**: Create interfaces that handle the input/output ports, ensuring efficient data transfer and control.
   - **Considerations**: Bandwidth, throughput, and protocol adherence.
# Software/Hardware Analogy and High-Level Synthesis Tasks

This document explains the analogy between software functions and hardware modules, highlighting their differences and detailing the main tasks in High-Level Synthesis (HLS).

## Software/Hardware Analogy

![image](https://github.com/user-attachments/assets/9d17666c-967f-4426-841d-c6c77eeb2a72)
The analogy between software functions and hardware modules can be understood as follows:

- **Software Function**:
  - **Input Arguments**: Variables passed to the function.
  - **Function Body**: The main logic of the function.
  - **Output Arguments**: Variables returned by the function.

- **Hardware Modules**:
  - **Input Ports**: Equivalent to input arguments in software.
  - **Hardware Body**: The core logic of the hardware module.
  - **Output Ports**: Equivalent to output arguments in software.

The image illustrates how a software function can be mapped to a hardware module, showing the correspondence between input/output arguments and ports, as well as the function body and hardware body.

## Software/Hardware Analogy - Differences


![image](https://github.com/user-attachments/assets/46303aed-6627-4290-9cc6-dd2f60dc4bbe)



Despite the analogy, there are key differences between software functions and hardware modules:

- **Execution Model**:
  - **Software Function**: Sequential execution.
  - **Hardware Modules**: Fully parallel execution, leveraging the intrinsic parallelism of electronic circuits.

- **Memory Access**:
  - **Software Function**: Easy memory access, often abstracted away by the programming environment.
  - **Hardware Modules**: Complicated memory access, requiring explicit control and design.

- **Control and Controller**:
  - **Software**: Relies on the underlying cash and controller mechanisms of the processor.
  - **Hardware**: Needs explicit design of control mechanisms to manage data flow and operations.

The image highlights these differences, showing the sequential nature of software execution versus the parallel nature of hardware execution, as well as the differences in memory access complexity.

## Two Main HLS Tasks
![image](https://github.com/user-attachments/assets/b9c9b609-c37a-450c-84b4-2c7c7d0cf4ed)


High-Level Synthesis (HLS) involves two main tasks:

1. **Function Synthesis**:
   - **Objective**: Convert the software function into a hardware module.
   - **Process**: Translate the function body into hardware logic, optimizing for parallelism.
   - **Components**: Input ports (arguments), function body (logic), output ports (arguments).

2. **Interface Synthesis**:
   - **Objective**: Define the communication protocols for the hardware module.
   - **Process**: Create interfaces that handle the input/output ports, ensuring efficient data transfer and control.
   - **Considerations**: Bandwidth, throughput, and protocol adherence.


</details>

<details>

<summary> WEEK 1 - LABS </summary>
![image](https://github.com/AnoushkaTripathi/NIELIT-INTERNSHIP-ON-HLS-PROGRAMMING/assets/98522737/e07e5535-fd47-4664-bf6f-9d3208b19945)


![image](https://github.com/AnoushkaTripathi/NIELIT-INTERNSHIP-ON-HLS-PROGRAMMING/assets/98522737/57d7e14b-b268-4ba8-b032-daae47cb5fdd)

![image](https://github.com/AnoushkaTripathi/NIELIT-INTERNSHIP-ON-HLS-PROGRAMMING/assets/98522737/c9a9598a-c95f-406d-b241-e9e20d9defdc)

![image](https://github.com/AnoushkaTripathi/NIELIT-INTERNSHIP-ON-HLS-PROGRAMMING/assets/98522737/e2c80ae6-4889-451a-aff4-27d2c04cce33)


![image](https://github.com/AnoushkaTripathi/NIELIT-INTERNSHIP-ON-HLS-PROGRAMMING/assets/98522737/93451a76-de08-413a-b699-0118c683c54f)


![image](https://github.com/AnoushkaTripathi/NIELIT-INTERNSHIP-ON-HLS-PROGRAMMING/assets/98522737/164b7bcd-f664-4d29-86f0-3437f87ccf88)


![image](https://github.com/AnoushkaTripathi/NIELIT-INTERNSHIP-ON-HLS-PROGRAMMING/assets/98522737/486cdc68-fc24-4a80-9eba-11816896c7bc)


![image](https://github.com/AnoushkaTripathi/NIELIT-INTERNSHIP-ON-HLS-PROGRAMMING/assets/98522737/803b9864-b875-4870-835e-1aeabfc15405)

![Screenshot 2024-06-30 112316](https://github.com/AnoushkaTripathi/NIELIT-INTERNSHIP-ON-HLS-PROGRAMMING/assets/98522737/d6cb09fc-11d1-4ffd-a39d-89a75af78a4f)



![image](https://github.com/AnoushkaTripathi/NIELIT-INTERNSHIP-ON-HLS-PROGRAMMING/assets/98522737/6294f38a-b210-4653-bd6f-f51d5eb99f74)



</details>

## Capstone Project

# HUFFMAN ENCODING

  huffman-encoding-core
  
![image](https://github.com/user-attachments/assets/e1074bd7-1a4d-4123-a4dd-7dfb1ef2576f)

