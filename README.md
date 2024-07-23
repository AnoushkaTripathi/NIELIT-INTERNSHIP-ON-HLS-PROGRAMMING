![image](https://github.com/AnoushkaTripathi/NIELIT-INTERNSHIP-ON-HLS-PROGRAMMING/assets/98522737/0532da74-92ae-4b9e-935b-68390bdacd12)

# NIELIT-INTERNSHIP-ON-HLS-PROGRAMMING

## Objective of this Internship

- Provide theoretical concepts of High-Level Synthesis (HLS)
- Provide a comprehensive understanding of HLS design flow for FPGAs
- In-system Hardware-debugging of the post-implemented design
- Case studies and projects using HLS Programming

# Outcome of the Internship
After successful completion of this Internship, the I learnt to
- Create my own IP and SoC design for FPGA implementation
- Develop my own software application with Zynq APSoC

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


# DAY 2

![image](https://github.com/user-attachments/assets/14173de3-a512-4384-9fb4-fa6340f73bfb)

# Design Flow in Vivado HLS

## Overview

The design flow in Vivado HLS allows you to create custom hardware accelerators from high-level C/C++ code. This process simplifies FPGA (Field-Programmable Gate Array) development by abstracting low-level details. Here’s how it works:

### 1. Coding Functionality
- Write your algorithm or functionality in C/C++.
- This high-level code will serve as the basis for your hardware design.

### 2. C-Simulation (Optional)
- Simulate your C/C++ code to verify correctness.
- Use test vectors to ensure expected behavior.

### 3. C/RTL Co-Simulation (Optional)
- Co-simulate the C/C++ code with RTL (Register Transfer Level) code.
- Validate consistency between the high-level and low-level representations.

### 4. Synthesis
- Transform your C/C++ code into RTL.
- Vivado HLS generates hardware components (datapaths, controllers, etc.).

### 5. Co-Simulation (Optional)
- Verify the synthesized RTL against the original C/C++ code.
- Ensure functional equivalence.

### 6. IP Generation
- Export the generated IP (Intellectual Property) for use in Vivado Design Suite.
- Integrate the custom IP into your FPGA project.

  # Hardware Design and Software Programming Analogy


![image](https://github.com/user-attachments/assets/5c3c1603-1870-455b-8f35-c8fb84654486)


### Hardware Design
- **Inputs**: Analogous to call-by-value arguments in software programming.
- **Outputs**: Analogous to function returns and call-by-reference arguments in software programming.
- **Inouts**: Inputs/outputs (inout) in hardware design correspond to call-by-reference arguments in software programming.
- **Design**: The hardware design itself is analogous to the function body in software programming.

### Software Programming
The software side of the analogy explains how arguments and return values are handled in a function:
- **Call by Value**: Arguments passed by value, meaning a copy of the value is passed.
- **Call by Reference**: Arguments passed by reference, allowing the function to modify the variable.
- **Function Return**: The value that the function returns after execution.

### Example Code
The example code provided in the diagram demonstrates a function that performs an addition operation using both call-by-value and call-by-reference arguments:

```cpp
int add (int a, int *b, int &c) {
    int d;
    d = a + *b + c;
    return d;
}
```

![image](https://github.com/user-attachments/assets/cfc54597-0787-41e6-a24b-99051f978498)

## Hardware Port Examples

![image](https://github.com/user-attachments/assets/f1846ec1-90da-4485-a826-85307a918b93)

- **1 bit data**
- **8 bit data**
- **A complex port**

### Types of Ports:
- **USB port**: Universal Serial Bus port, used for connecting peripherals to the hardware design, providing data transfer and power supply.
- **DDR memory port**: Double Data Rate memory port, used for connecting to high-speed memory modules, facilitating fast data read/write operations.
- **Data stream port**: Used for continuous data transmission between the hardware design and external devices or systems, often in real-time applications.
- **I²C access port**: Inter-Integrated Circuit port, used for communication between low-speed peripherals and the hardware design, typically requiring only two lines (SDA and SCL).

## HLS Design Ports

![image](https://github.com/user-attachments/assets/254d900a-be69-4970-aa97-d77ecbd6a692)


```c
void ledonoff(unsigned char *o) {
    *o = 0b11111000;
}
```

# DAY 3

![image](https://github.com/user-attachments/assets/e85f4ea8-71a8-4ca3-b2c7-24afe469da90)


```
#define data_type unsigned char

void basic_input_output(
    data_type input
    data_type *output) {
    
    *output = input;
}
```



#### Interface Synthesis

![image](https://github.com/user-attachments/assets/45194563-7ba8-4331-b786-df4f46c9c0b7)

- **Description**: When the top-level function is synthesized, the arguments (or parameters) to the function are synthesized into RTL (Register Transfer Level) ports. This process is called **interface synthesis**.
- **Illustration**: The diagram shows a top-level function `top-function()` with arguments `p1`, `p2`, and `p3` that are synthesized into ports. This top function calls several other functions (`func1()`, `func2()`, `func3()`, etc.), which are also connected via ports.

#### Port Interfaces
- **Description**: Port interfaces define how data is transferred between different modules or functions in the FPGA design. The diagram provides an example of a function `basic_input_output()` that uses port interfaces.
- **Example Code**:
  ```cpp
  void basic_input_output(data_type *output) {
      #pragma HLS INTERFACE ap_none port=output
      *output = 0b11110000;
  }
  ```
   **Explanation**: The `#pragma HLS INTERFACE` directive specifies the type of interface for the `output` port. In this case, `ap_none` indicates that the port does not use any specific handshaking protocol.

#### List of Interface Modes

  - `ap_ack`
  - `ap_bus`
  - `ap_ctrl_hs`
  - `ap_fifo`
  - `ap_hs`
  - `ap_memory`
  - `ap_none`
  - `ap_ovld`

These modes define different ways to handle data transfer and synchronization between the modules.

![image](https://github.com/user-attachments/assets/621e40f3-cfe1-433d-b956-ab02e02bc312)

### 1. `ap_none`
- **Configuration**: Simple data output.
- **Description**: 
  - The module has an 8-bit output `o[7:0]` connected directly to the `led[7:0]`.
  - No handshaking signals are used.
  - This configuration is the most straightforward and has no control signals.

### 2. `ap_hls`
- **Configuration**: Data output with HLS protocol signals.
- **Description**: 
  - The module has an 8-bit output `o[7:0]` connected to the `led[7:0]` with control signals.
  - Control signals include:
    - `ap_ack_0`: Acknowledge signal for the process.
    - `ap_clk_0`: Clock signal for synchronization.
    - `ap_rst_0`: Reset signal.
    - `ap_vld_0`: Valid signal indicating valid data.
  - These control signals facilitate handshaking, ensuring proper data transfer and synchronization between the module and the connected components.

### 3. `s_axilite`
- **Configuration**: Data output with AXI-Lite interface.
- **Description**: 
  - The module interfaces using the AXI-Lite protocol, suitable for control registers and low-throughput data transfers.
  - Signals include:
    - `s_axi_AXILiteS_AWADDR_0[9:0]`: Write address.
    - `s_axi_AXILiteS_AWVALID_0`: Write address valid.
    - `s_axi_AXILiteS_AWREADY_0`: Write address ready.
    - `s_axi_AXILiteS_WDATA_0[31:0]`: Write data.
    - `s_axi_AXILiteS_WSTRB_0[3:0]`: Write strobes.
    - `s_axi_AXILiteS_WVALID_0`: Write data valid.
    - `s_axi_AXILiteS_WREADY_0`: Write data ready.
    - `s_axi_AXILiteS_BRESP_0[1:0]`: Write response.
    - `s_axi_AXILiteS_BVALID_0`: Write response valid.
    - `s_axi_AXILiteS_BREADY_0`: Write response ready.
    - `s_axi_AXILiteS_ARADDR_0[9:0]`: Read address.
    - `s_axi_AXILiteS_ARVALID_0`: Read address valid.
    - `s_axi_AXILiteS_ARREADY_0`: Read address ready.
    - `s_axi_AXILiteS_RDATA_0[31:0]`: Read data.
    - `s_axi_AXILiteS_RRESP_0[1:0]`: Read response.
    - `s_axi_AXILiteS_RVALID_0`: Read data valid.
    - `s_axi_AXILiteS_RREADY_0`: Read data ready.
  - This interface allows communication with the module using standard AXI-Lite signals, making it suitable for integration in larger systems with AXI interconnects.

These configurations demonstrate different levels of complexity and capability for interfacing a design module, from simple direct connections (`ap_none`) to more complex handshaking (`ap_hls`) and standardized bus interfaces (`s_axilite`).

## Combinational Circuits

![image](https://github.com/user-attachments/assets/a6dd79a2-e1d3-47c6-b920-46f4948fa145)

![image](https://github.com/user-attachments/assets/dbd52fa8-e01e-47d7-9b56-dc069899e7c1)

# C/C++ Testbench

![image](https://github.com/AnoushkaTripathi/NIELIT-INTERNSHIP-ON-HLS-PROGRAMMING/assets/98522737/fefdf1ab-71f0-4fed-9d7b-14fe6ec5e7d5)

## Verification 

In this course we will learn simulation based verification


![image](https://github.com/AnoushkaTripathi/NIELIT-INTERNSHIP-ON-HLS-PROGRAMMING/assets/98522737/7246fac8-e4fe-4fc1-83a4-e09cffae5e98)


![image](https://github.com/user-attachments/assets/b43aab2c-ee14-4985-8fd7-e4568708e75a)

# Flowchart of Design Process

This flowchart outlines the steps involved in computer engineering design. Here’s a brief summary:

- C Test Bench: Create a test environment in the C programming language.
- Design in C/C++: Perform the actual design work using C or C++.
- Constraints Directives: Specify design constraints, such as timing requirements.
- C Synthesis: Synthesize the design into a hardware description language (HDL).
- RTL Description: Create a Register Transfer Level (RTL) description.
- Package IP: Package the final design as intellectual property (IP).

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

## WEEK 6-8: Capstone Project

# HUFFMAN ENCODING

  huffman-encoding-core

  ![image](https://github.com/user-attachments/assets/6847cf6c-1f94-4a0d-a32c-8cf56359edab)


---

# Canonical Huffman Encoding Project

## Overview

The Canonical Huffman Encoding project involves designing, simulating, and evaluating a hardware accelerator for Huffman encoding using High-Level Synthesis (HLS) tools. The primary goal is to implement a Canonical Huffman code, which is a variant of Huffman coding where the codes are ordered in a way that minimizes storage requirements and simplifies the encoding and decoding processes.

## Table of Contents

1. [Introduction](#introduction)
2. [Prerequisites](#prerequisites)
3. [Project Structure](#project-structure)
4. [Modules and Functions](#modules-and-functions)
    - [Histogram Calculation](#histogram-calculation)
    - [Tree Construction](#tree-construction)
    - [Tree Truncation](#tree-truncation)
    - [Create Codeword](#create-codeword)
    - [Testbench](#testbench)
5. [Usage](#usage)
6. [Example](#example)
7. [References](#references)

## Introduction

Canonical Huffman codes are a variant of Huffman codes with specific properties that make them easier to store and manipulate. This project implements a Canonical Huffman encoding process in hardware using HLS tools. The project includes several stages, from histogram calculation to tree truncation and codeword assignment.

## Prerequisites

- Vivado HLS or similar HLS tools
- Basic understanding of Huffman encoding
- Familiarity with C/C++ programming
- Basic knowledge of FPGA design and Verilog

## Project Structure

```
.
├── src
│   ├── huffman.h
│   ├── huffman.cpp
│   ├── create_codeword.cpp
│   └── testbench.cpp
├── data
│   ├── huffman.random256.txt
│   └── huffman.random256.gold
└── README.md
```

- `src`: Contains the source code for the Huffman encoding project.
- `data`: Contains the input frequency data and the golden reference output.

## Modules and Functions

### Histogram Calculation


This module calculates the histogram of symbol frequencies from the input data. The histogram is used to build the Huffman tree.

Detailed Description:


The histogram calculation step involves reading the input data and counting the occurrences of each symbol. This frequency count is essential for constructing the Huffman tree, as it determines the weights of the tree nodes.

- Input: An array of symbol frequencies.
- Output: A histogram array where each index represents a symbol, and the value at that index represents the frequency of that symbol.

![image](https://github.com/user-attachments/assets/3478417f-a8f4-40d2-ace6-7af8c87dc52e)


This module calculates the histogram of symbol frequencies from the input data. The histogram is used to build the Huffman tree.

**Code Snippet:**
```cpp
void calculate_histogram(const int* frequencies, int* histogram) {
    for (int i = 0; i < INPUT_SYMBOL_SIZE; ++i) {
        histogram[frequencies[i]]++;
    }
}
```

### Tree Construction


This module constructs the Huffman tree based on the symbol frequencies. It uses a priority queue to ensure that the tree is built correctly.


The Huffman tree construction involves creating a binary tree where each leaf node represents a symbol, and the path from the root to the leaf determines the symbol's codeword. The priority queue is used to build the tree efficiently, ensuring that nodes with lower frequencies are combined first.

Input: A histogram array of symbol frequencies.


Output: A Huffman tree where each node contains a symbol and its frequency.


Steps:

Initialize a priority queue and insert all non-zero frequency symbols as leaf nodes.
Extract the two nodes with the smallest frequencies from the queue, combine them into a new node, and insert the new node back into the queue.
Repeat until there is only one node left in the queue, which will be the root of the Huffman tree.

**Code Snippet:**
```cpp
HuffmanTree construct_tree(const int* histogram) {
    std::priority_queue<HuffmanNode, std::vector<HuffmanNode>, Compare> pq;
    for (int i = 0; i < INPUT_SYMBOL_SIZE; ++i) {
        if (histogram[i] > 0) {
            pq.push(HuffmanNode(i, histogram[i]));
        }
    }

    while (pq.size() > 1) {
        HuffmanNode left = pq.top(); pq.pop();
        HuffmanNode right = pq.top(); pq.pop();
        HuffmanNode parent(left, right);
        pq.push(parent);
    }

    return pq.top();
}
```

### Tree Truncation


This module truncates the Huffman tree to a maximum codeword length. This step is necessary to ensure that the codewords fit within the desired bit-width.

Detailed Description


Tree truncation involves adjusting the Huffman tree to ensure that no codeword exceeds a specified maximum length. This is important for hardware implementations where the bit-width is limited.

Input: A Huffman tree and the maximum allowed codeword length.


Output: A truncated Huffman tree.

Steps:

Traverse the Huffman tree to determine the initial lengths of the codewords.
If any codeword exceeds the maximum length, redistribute the codewords to shorten the longer ones while maintaining the prefix property of Huffman codes.

**Code Snippet:**
```cpp
void truncate_tree(HuffmanTree& tree, int max_length) {
    // Truncation logic here
}
```

### Create Codeword
This module assigns codewords to each symbol based on the truncated tree. It ensures that the codewords are in canonical form, which simplifies storage and manipulation.

Detailed Description


Canonical Huffman codes assign the shortest codes to the most frequent symbols. The codes are sorted by length, and within each length, the codes are assigned in lexicographic order.

Input: A truncated Huffman tree.


Output: An array of codewords for each symbol.


Steps:

Calculate the first codeword for each length.
Assign codewords to symbols based on their lengths, ensuring the codes are in lexicographic order.
#### Process Description:

1. **First Codeword Calculation:** 
   - Determine the first codeword for each length using the codeword length histogram.
   - Formula:
     ```cpp
     first_codeword[1] = 0;
     for(int i = 2; i <= MAX_CODEWORD_LENGTH; ++i) {
         first_codeword[i] = (first_codeword[i - 1] + codeword_length_histogram[i - 1]) << 1;
     }
     ```

2. **Assigning Codewords:**
   - Assign codewords to symbols and format them for encoding and decoding.
   - Store codewords in bit-reversed order for easier decoding.

**Code Snippet:**
```cpp
void create_codeword(
    const CodewordLength symbol_bits[INPUT_SYMBOL_SIZE],
    const ap_uint<SYMBOL_BITS> codeword_length_histogram[TREE_DEPTH],
    PackedCodewordAndLength encoding[INPUT_SYMBOL_SIZE]
) {
    Codeword first_codeword[MAX_CODEWORD_LENGTH];
    first_codeword[0] = 0;
    for (int i = 1; i < MAX_CODEWORD_LENGTH; ++i) {
        first_codeword[i] = (first_codeword[i - 1] + codeword_length_histogram[i - 1]) << 1;
    }

    for (int i = 0; i < INPUT_SYMBOL_SIZE; ++i) {
        CodewordLength length = symbol_bits[i];
        if (length != 0) {
            Codeword out_reversed = first_codeword[length];
            out_reversed.reverse();
            out_reversed >>= (MAX_CODEWORD_LENGTH - length);
            encoding[i] = (out_reversed << CODEWORD_LENGTH_BITS) + length;
            first_codeword[length]++;
        } else {
            encoding[i] = 0;
        }
    }
}
```

### Testbench

The final part of the code is the testbench. It reads the input frequency values from a file, processes them using the Huffman encoding function, and compares the resulting codewords with an existing golden reference stored in a file.


Detailed Description
The testbench verifies the correctness of the Huffman encoding implementation by comparing the output with a precomputed golden reference.


Input: A file containing symbol frequencies.


Output: A file containing the encoded symbols.
Steps:

Read the input frequencies from a file.


Perform the Huffman encoding process.


Write the encoded symbols to an output file.


Compare the output file with the golden reference file to verify correctness.


**Code Snippet:**
```cpp
int main() {
    ap_uint<16> *frequencies = NULL;
    file_to_array("data/huffman.random256.txt", frequencies, INPUT_SYMBOL_SIZE);

    Symbol in[INPUT_SYMBOL_SIZE];
    for (int i = 0; i < INPUT_SYMBOL_SIZE; ++i) {
        in[i].frequency = frequencies[i];
        in[i].value = i;
    }

    PackedCodewordAndLength encoding[INPUT_SYMBOL_SIZE];
    int num_nonzero_symbols;
    huffman_encoding(in, encoding, &num_nonzero_symbols);

    FILE* output_file = fopen("data/huffman.random256.out", "w");
    for (int i = 0; i < INPUT_SYMBOL_SIZE; ++i) {
        fprintf(output_file, "%d, %x\n", i, (unsigned int)encoding[i]);
    }
    fclose(output_file);

    if (system("diff data/huffman.random256.out data/huffman.random256.gold")) {
        printf("FAIL: Output DOES NOT match the golden output\n");
        return 1;
    } else {
        printf("PASS: The output matches the golden output\n");
        return 0;
    }
}
```

## Usage

1. **Clone the Repository**

    ```bash
    git clone https://github.com/AnoushkaTripathi/NIELIT-INTERNSHIP-ON-HLS-PROGRAMMING
    cd huffman-encoding
    ```

2. **Compile the Project**

    Use Vivado HLS or your preferred HLS tool to compile the project.

3. **Run the Testbench**

    Execute the testbench to verify the implementation.

![image](https://github.com/user-attachments/assets/17cdcde7-083a-47d5-ac71-ed30f0f00dd1)


## References

- [Huffman Coding](https://en.wikipedia.org/wiki/Huffman_coding)
- [pp4fpga](https://pp4fpgas.readthedocs.io/en/latest/)
- [Vivado HLS Documentation](https://www.xilinx.com/products/design-tools/vivado.html)

---



