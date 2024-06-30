![image](https://github.com/AnoushkaTripathi/NIELIT-INTERNSHIP-ON-HLS-PROGRAMMING/assets/98522737/0532da74-92ae-4b9e-935b-68390bdacd12)

# NIELIT-INTERNSHIP-ON-HLS-PROGRAMMING

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

An LUT (LookUp Table) in FPGA design is a fundamental building block. It can implement any Boolean function of N input variables. Essentially, an LUT acts as a truth table, defining how your combinatorial logic behaves. When an FPGA is configured, it fills in the LUT with output values, which are stored in SRAM bits. The same physical LUT can implement different logic functions by changing the LUT-Mask (the truth table). Think of LUTs as memory, where inputs serve as addresses, and outputs are the data stored in those addresses

![image](https://github.com/AnoushkaTripathi/NIELIT-INTERNSHIP-ON-HLS-PROGRAMMING/assets/98522737/ead615e2-0ece-4001-8a89-66fe0264d99e)

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



