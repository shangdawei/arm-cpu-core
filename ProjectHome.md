# ARMv4 compatible CPU core #

This ARMv4-compatible CPU core is written in synthesiable verilog.It could run uCLinux in MODELSIM. It has high Dhrystone benchmark value: 1.2 DMIPS/MHz.

It could be utilized in your FPGA design as one submodule, if you master the interface of this .v file.

This IP core is very compact. It is one .v file and has only less 1800 lines.

Its key feature:
  * Harvard structure, 3-stage pipeline;
  * Little-endian format;
  * ARMv4 instructions and interrupts are supported;
  * Not support: Thumb and coprocessor instructions(developping);

|Vendor|FPGA type|Area|Fmax(constraint)|note|
|:-----|:--------|:---|:---------------|:---|
|xilinx|Spartan3E-3S-500-4|3030 Slice(65%)|39MHz           |I have one design kit |
|      | Virtex2p-2VP30-7|2953 Slice(21%)|63MHz           |I want to have |
|SMIC  |0.18um   |24,000(NAND gates)|100MHz          |with 32X32 multiplier|
|SMIC  |0.18um   |17,000(NAND gates)|250MHz          |without 32X32 multiplier|



Q: What is the main advantage of this CPU core?

A: Simple is best. This simple CPU core will lead you to a complex SoC design based on ARM architecture. Simple descirption of synthesiable verilog will bring less trouble in synthesis or simulation for FPGA or ASIC. All you need do is mastering the interface of this CPU core and make it being one of your submodule.

The figure below is running uCLinux in MODELSIM with this CPU core.

![http://arm-cpu-core.googlecode.com/files/uclinux_large.jpg](http://arm-cpu-core.googlecode.com/files/uclinux_large.jpg)
http://arm-cpu-core.googlecode.com/files/uart.JPG