#############################################################################################

1. How to Build kernel and mali
	- get Toolchain
		From android git server , codesourcery and etc ..
		 - arm-eabi-4.7
		
	- edit build_kernel.sh
		edit target architecture.
		 - ARCH ?= arm
		edit "CROSS_COMPILE" to right toolchain path(You downloaded).
		  EX)  CROSS_COMPILE= $(android platform directory you download)/android/prebuilts/gcc/linux-x86/arm/arm-eabi-4.7/bin/arm-eabi-
          Ex)  CROSS_COMPILE=/usr/local/toolchain/arm-eabi-4.7/bin/arm-eabi-          // check the location of toolchain
  	
		- run build_kernel.sh
		$ ./build_kernel.sh

2. Output files
	- Kernel : kernel/arch/arm/boot/zImage
	- module : kernel/modules/*.ko

3. How to Clean	
		$ ./build_kernel.sh Clean
#############################################################################################
