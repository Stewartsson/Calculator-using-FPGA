# Calculator-using-FPGA
This project demonstrates the design and hardware implementation of a combinational Arithmetic Logic Unit (ALU). Developed in Verilog HDL, the system performs 2-bit binary arithmetic across four operations, mapped to the physical sliding switches and LED array of a Xilinx ZedBoard. 

# ZedBoard 2-Bit Multi-Function ALU Calculator

A hardware-based binary calculator implemented on the **Xilinx ZedBoard (Zynq-7000)** using Verilog HDL.

## 🚀 Project Overview
This project demonstrates a fundamental VLSI design of an Arithmetic Logic Unit (ALU). It processes two 2-bit binary numbers to perform basic arithmetic operations, controlled entirely by physical hardware switches.

## 🛠 Features
- **4 Operations:** Addition (+), Subtraction (-), Multiplication (*), and Division (/).
- **Error Detection:** Real-time "Division by Zero" flag on LED LD7.
- **Physical I/O:** Uses 8 sliding DIP switches for input and 8 LEDs for visual output.
- **Combinational Logic:** Zero-latency execution without requiring a system clock.

## 🎮 Hardware Control Map
| Switch(es) | Function | Range / Description |
|------------|----------|---------------------|
| **SW7, SW6** | Input A | 00 (0) to 11 (3) |
| **SW3, SW2** | OpCode | 00:+, 01:-, 10:*, 11:/ |
| **SW1, SW0** | Input B | 00 (0) to 11 (3) |

## 📊 Result Mapping (LEDs)
- **LD3 - LD0:** 4-bit Binary Result (Max value: 9 for 3x3).
- **LD7:** Error Flag (High if Division by Zero occurs).

## 💻 How to Run
1. Open **Xilinx Vivado 2026** (or later).
2. Create a new project targeting the **ZedBoard (xc7z020clg484-1)**.
3. Add `Simple_Digital_Calculator.v` as a design source.
4. Add `ZedBoard_ALU.xdc` as a constraint file.
5. Run **Synthesis**, **Implementation**, and **Generate Bitstream**.
6. Connect your ZedBoard and use the **Hardware Manager** to program the device.

## 📝 Author
**John Stewartsson J R** Electronics and Communication Engineering Student  
*St. Joseph's Institute of Technology*
