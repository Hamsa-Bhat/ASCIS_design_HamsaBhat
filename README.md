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

Here we see the entire flow of how it works - 
![<img width="585" alt="image" src="https://github.com/Hamsa-Bhat/ASCIS_design_HamsaBhat/assets/163815218/fd69ee48-8ca2-4256-8660-9b4516882ae5">]!

## SoC design and OpenLANE - Mohamed Shalan

There are some important things which we MUST have from the starting to create an ASIC design such as - RTL IP's, EDA Tools and PDK DATA 

PDK is basically the interface between the FAB and the designers, PDK -Process design knit 

![<img width="357" alt="image" src="https://github.com/Hamsa-Bhat/ASCIS_design_HamsaBhat/assets/163815218/a7395553-da1e-4110-9c7b-0a6ae4a179b3">]!

This is the simplified RTL to GDSII flow, which has major implementation steps such as Synthesis, Floor/power Planning, Placement, Clock Tree synthesis, Routing and finally sign off

![<img width="558" alt="image" src="https://github.com/Hamsa-Bhat/ASCIS_design_HamsaBhat/assets/163815218/7a37dc19-67ab-494c-91a9-cedd10f99900">]!

Synthesis is the first step in an ASIC floor. The synthesis converts RTL into circuits which are made out of components.

![<img width="375" alt="image" src="https://github.com/Hamsa-Bhat/ASCIS_design_HamsaBhat/assets/163815218/9b32c424-6fb3-4d89-a94b-0147acd316dc">]!

Floor and Power planning - The main goal here is to exactly plan the silicon area to make the chip efficient and in the Macro floor planning the Chip die is partioned between different chip components.

![<img width="357" alt="image" src="https://github.com/Hamsa-Bhat/ASCIS_design_HamsaBhat/assets/163815218/fee2e41d-41fd-4d6b-8ea7-0c0b7698d6ba">]!

Power Planning - Power network is constructed and the power network is constructed and the power pens are connected to ll the componets and these structers are important to reduce the resistance and reduce the voltage drop, if its needed. Due to these staying on the upper metal they are thicker than the rest hence low amount of resistance is present.

![<img width="373" alt="image" src="https://github.com/Hamsa-Bhat/ASCIS_design_HamsaBhat/assets/163815218/37f1efb6-b432-42a4-a051-243c63f9cbe0">]!

## Introduction to OpenLANE and Strive chipsets

Open source PDK (OpenLANE), developed by efabless. OpenLANE converts the RTLI into GDSII, striVE is basically the family of open everything - Open PDK, Open RTL, Open EDA

![<img width="395" alt="image" src="https://github.com/Hamsa-Bhat/ASCIS_design_HamsaBhat/assets/163815218/7ddfb856-67e5-43a5-898e-91e492de2919">]!

![<img width="398" alt="image" src="https://github.com/Hamsa-Bhat/ASCIS_design_HamsaBhat/assets/163815218/68dcfea0-3dc8-449a-8f65-51baf3183344">]!

striVe 2 is identical along with striVe and striVe 2a is similar to striVe 2 and so on.

**Main goal of OpenLANE** 

To produce clean GDSII tools (no human in the loop), along with no LVS violations, DRC violations, Timing violations.
This Softawre can be used to harden the Macros and Chips.

## Introduction to OpenLANE detailed ASIC design flow 

The flow starts form the Design RTL and ends with the end product (GDSII)
![<img width="397" alt="image" src="https://github.com/Hamsa-Bhat/ASCIS_design_HamsaBhat/assets/163815218/ac757148-1b5b-4a9c-9290-52a984a310a7">]!

- Synthesis exploration used to genreate reports based on the delay and area is affected.
![<img width="404" alt="image" src="https://github.com/Hamsa-Bhat/ASCIS_design_HamsaBhat/assets/163815218/b680107c-8544-4888-9e2e-9b66f4142bb0">]!

- Design exploration shows the numbers of violation genreated after genreating the final layout, used to design configurations 
  ![<img width="558" alt="image" src="https://github.com/Hamsa-Bhat/ASCIS_design_HamsaBhat/assets/163815218/a3fd57bd-c782-4ca4-afb2-346f0827e5f8">]!

- OpenLANE Regression  Testing used for regression testing

![<img width="570" alt="image" src="https://github.com/Hamsa-Bhat/ASCIS_design_HamsaBhat/assets/163815218/3bef0de7-1363-47b3-89ae-4a897d030372">]!

- Design for test (Optional) and alos adds extra logic
![<img width="563" alt="image" src="https://github.com/Hamsa-Bhat/ASCIS_design_HamsaBhat/assets/163815218/4680a3ca-2dac-44f6-bb18-b2236ff14262">]!

-Physical Implementation

![ <img width="554" alt="image" src="https://github.com/Hamsa-Bhat/ASCIS_design_HamsaBhat/assets/163815218/ef99b21d-8f12-4c7e-9ef1-e59e803c1362">]!

when a metal wire is fabricatted and can act as an antenna, as an Antenna it collects charges which can damage Transistor gates 

![<img width="550" alt="image" src="https://github.com/Hamsa-Bhat/ASCIS_design_HamsaBhat/assets/163815218/5776bb24-f624-4b06-b530-540e3d8d2760">]!

there are 2 solutions while dealing with Antenna rules violations - 

- Bridging top metal layers
- Instert Antenna diodes 

![<img width="519" alt="image" src="https://github.com/Hamsa-Bhat/ASCIS_design_HamsaBhat/assets/163815218/d4dedd00-859d-487b-8998-b382690a33f3">]!

- Physical verification DRC & LVS
  
![<img width="517" alt="image" src="https://github.com/Hamsa-Bhat/ASCIS_design_HamsaBhat/assets/163815218/0da85d9e-f66d-4994-ab3b-f5e984939d28">]!





