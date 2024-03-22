# ASCIS_design_HamsaBhat
  ## Day 1
  
### **Introduction**

In genereal an Arduino chip must contain various tools such as a JTAG tool, QSPI1 flash, I2C0- ELEPROM, VCC and Ground and an external SDRAM Chip is the typical board digram which every Aruino chip must have. 
  
In the below picture we see a common board diagram and how it looks -
![<img width="485" alt="image" src="https://github.com/Hamsa-Bhat/ASCIS_design_HamsaBhat/assets/163815218/1faa10f8-f89b-4b29-bef0-a20a07814026">]!

Till now whatever we might have considered as a "CHIP" is actually called a PACKAGE inside the package lies the chip which is in the centre of the package and is connected to the package through something called the "Wirebounds". These wirebounds help us to transfer all the signals from the exterior world to the chip.

![<img width="306" alt="image" src="https://github.com/Hamsa-Bhat/ASCIS_design_HamsaBhat/assets/163815218/803b43ba-a4e7-41e5-b34f-fd98356a311e">!]

- _**How to talk to computers?**_
  
  Further opening up the chip shown in the above image, we find various components such as -
  - **PADS** - Used to send signals from the interior of the chip to the exterior and vice versa.
  - **CORE** - This lies in the centre of the chip and contains all the digital logics sits, and usually consists of SRAM,SoC,adc, PLL and more.
  - **DIE** - Is the size of the entire chip, we can also look at it like the perimeter or the boder of the entire chip.
these terminologies can be observed in the below picture -

![<img width="394" alt="image" src="https://github.com/Hamsa-Bhat/ASCIS_design_HamsaBhat/assets/163815218/56da36c2-65c9-4557-b54d-1d382d5e59d8">]!

As seen above the PLL, SRAM,adc and dac together are called as the _Foundry IP'S_ and the blocks are called as _Macros_

## Introduction to RISC - V

If you want to execute the C - Program file whith a specific layout then you first need to compile the C - Program to the RISC - V, Which is further converted into machine language program (Binary language program) to be understood by the Computer hardware. The hardware description language is a must as it should be between the RISC - V and the Layot, as it implements the specifications given by the RISC - V and then goes to Layout. 

![<img width="960" alt="image" src="https://github.com/Hamsa-Bhat/ASCIS_design_HamsaBhat/assets/163815218/c287105e-a838-44f4-bf90-687af3716e13">]!

## From Software Applications to Hardware

We all use apps such as Google, Excel, Youtube and many more, but how exactly do these apps work on our software?, you may ask.
In simple words -->

- the application Software enters into a box known as the "System Software" which converts the program to the Binarylanguage.

There are three very important parts which are present in the System Software which are - **_OS, Compiler and the Assembler._**

**OS** - Handles IO operations, Stores memories and another important role of this component is to take the app and convert it into the respective Assembly language program further into the Binary language. 

**Compiler** - Takes the C++, Java languages and is converted into Instructions, which depends on what kind of software it is.

**Assembler** - Takes the particular instructions and converts it into Binary language. This language goes to the Hardware and according to the commands in Binary it genereats its output.

The entire process can be observed in the below picture. 

![<img width="543" alt="image" src="https://github.com/Hamsa-Bhat/ASCIS_design_HamsaBhat/assets/163815218/746a4edb-3ecc-4cf0-a3a8-d088d1351349">]!

The below image is also an example of an APP as it was mentioned in the lecture.
![<img width="542" alt="image" src="https://github.com/Hamsa-Bhat/ASCIS_design_HamsaBhat/assets/163815218/b4b71014-b3fa-4045-8065-5011da09e4e8">]!
