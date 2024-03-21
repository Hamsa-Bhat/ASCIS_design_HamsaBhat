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

As seen above the PLL, SRAM,adc and dac together are called as the _Foundry IP'S_
