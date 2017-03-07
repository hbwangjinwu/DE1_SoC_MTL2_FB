
# DE1_SoC_MTL2_FB

## Discription
This is the FPGA hardware project for mtl2 with de1soc. The hardware project supports touch and display in FPGA partion.

The software driver code and dtbs are located in https://github.com/hbwangjinwu/linux-socfpga/tree/socfpga-4.5. You can git clone the code and switch to the socfpga-4.5 branch in the Linux system. 

## Compile

The hardware project should be compiled with the Quartus Prime. A sof file should be generated after compiling. And you can generate a .rbf file manually with executing the sof_to_rbf.bat file.

The linux code should be compiled with A linux PC or Virtual Machine.

The dtb file should also be generated in the linux kernel source by the command **make dtbs**.

## Setup

I tested it with the LXDE image.

Copy the zImage and .dtb file to the SD card.

Copy the soc_system.rbf file to the SD card and Set the MSEL[4..0] to 00000.

The desktop environment will be displayed on the screen. And you can touch the screen for testing the touch function.  For you own developing, the tslib should be added to your project.
