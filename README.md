XMOS Nokia 6100 display driver
======================

**Introduction**  
This is a driver for the Nokia 6100 (knock off) Display with NXP PCF8833 controller.
This display has 130x130 pixels with 12bpp (4096 colors) and uses a 9 bit SPI interface.
This driver supports only 12bpp (the controller supports also 8bpp and 16bpp).

**Controller compatibility**  
The Nokia 6100 (knockoff) display comes with two different controller which are
not fully compatible with each other: NXP PCF8833 and Epson S1D15G10.
A possible way to distinguish them is that displays with the NXP controller
likely have a brown flexible PCB and Epson a green flexible PCB. Currently only
the NXP controller is explicitly supported

**Where to get this display?**  
Sparkfun (also sells breakout boards)  
Ebay (usually better pricing)

**Driver functionality**  
* Draw pixel
* Draw line
* Draw and fill rectangle
* Draw circle (no filling!)
* Draw character
* Draw string
* Draw image using a raw image buffer

**Acknowledgement**  
Large part of the driver is based on the driver written by James P Lynch.

**To Do**  
* Add support for Epson S1D15G10 controller.
* Create a module compatible with the XMOS development tools.
* Used timed port operations instead of timers for delays in SPI routine.

**bmpdump**  
bmpdump is a utility written by me to convert a 24 bit uncompressed
BMP image to other formats. It can be used for this driver to convert an image
into a bitmap C array (12bpp) for the image drawing function.
See https://github.com/BiancoZandbergen/bmpdump

<p align="center">
  <img src="http://biancozandbergen.github.io/images/xmos_nokia6100_display_1.jpg"/>
</p>
