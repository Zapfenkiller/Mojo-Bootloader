# Spartan Configurator Bootloader

Alternative to the genuine Alchitry Mojo V3 software:  
Caterina bootloder adapted fully to 8 MHz clock and 500 mA of possible current
draw.

Build using LUFA 111009.

From their documentation:
> To build the bootloader for the ATmega32U4 (Mojo V3 and some V2) use
> Makefile-v3 (the default).
> To build the bootloader for the ATmega16U4 (Mojo V2) copy Makefile-v2 to
> Makefile and run make.
This means that `Makefile` is just a copy of the respective `Makefile-v*` made
before `make` gets called. Or you call the respective Makefiles directly, e. g.
`make -f Makefile-v3`.

**Check the VID/PID combination you use. The ones given are never legally
covered by the license and keep property of their respective owners!**

While "ISP"ing the bootloader to the Mojo it is recommended to also set some
fuses to new values:

LOW = 0xDE  
HIGH = 0xD8  
EXTENDED = 0xF3  

In any case ensure the BOOTRST fuse points to the bootloader section!

After the bootloader is in the ATmega you might want to secure it against
accidental overwrites:

LOCKBIT = 0xEF  


## See also

https://alchitry.com/blogs/tutorials/flashing-the-bootloader


## Licenses:

* LUFA = MIT, Dean Camera
* Mojo-Caterina = MIT, Embedded Micro
* My modifications = MIT, René Trapp

Please see respective files for the license details.