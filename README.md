# Spartan Configurator Bootloader

Alternative to the genuine Mojo software:  
Caterina bootloder adapted fully to 8 MHz clock and 500 mA of current draw.
Experimental VID/PID combination use due to some severe bootloader issues
on a Win10 machine using genuine 0x29DD / 0x0001 signature.

Build using LUFA 170418.

From their documentation:
> To build the bootloader for the ATmega32U4 (Mojo V3 and some V2) use
> Makefile-v3 (the default).
> To build the bootloader for the ATmega16U4 (Mojo V2) copy Makefile-v2 to
> Makefile and run make.
This means that `Makefile` is just a copy of the respective `Makefile-v*` made
before `make` gets called. **Check the VID/PID combination you use. The ones
given are never legally covered by the license and keep property of Microchip
Technology, Inc.!**

Licenses:

* LUFA = MIT, Dean Camera
* Mojo-Caterina = MIT, Embedded Micro
* My modifications = MIT, René Trapp

Please see respective files for the license details.