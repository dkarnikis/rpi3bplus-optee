# rpi3b-optee
Optee os support for raspberry pi 3b+ with hdmi support

Assuming you have built the optee os for raspberry pi3b+ https://github.com/OP-TEE/optee_os

and have flashed the boot and rootfs to your card using make img-help.

Copy the contents of BOOT/* into your partition#1 of your card and boot your rpi.


The main reasons that optee os is not compatible with rpi3b+ is that it target rpi3b.

## Problems

Optee uses raspberry pi 3b dtb rather than 3b+, so we change it.

Checking the pattern of the led + it's red color (4 flashes in a row) during boot means that there is a problem with the start.elf so I swapped some files from the latest ubuntu core image boot partition into the optee created partition (based on https://optee.readthedocs.io/building/devices/rpi3.html?fbclid=IwAR23CicZeElvW11AfLk9cj2dRxVZsDR9odzDJnGMxSTPvQkBDQpUimWNPJI#boot-sequence)

Network is not available, i have managed to get it to work, might post it later till i clean it up and patch the whole 'guide' aswell (not very good with this stuff)


## Contact

Feel free to mail me dkarnikis(at)gmail(dot)com
