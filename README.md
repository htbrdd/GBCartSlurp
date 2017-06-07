# NOTICE: 
This project may be deprecated as I can't really get the transfer speed up to where I'd like it for a RPi 1/ZERO. I'm going to experiment with SPI however after playing with a JoeyJoebags the speed difference between using a microcontroller as the interface is phenominal. a cart that takes ~9 minutes to dump using I2C takes mere seconds on a joebags. I know the interface on that is a microcontroller so I'm considering switching totally to a teensy as the interface, unless SPI/23S17 chips can make a significant difference
# GBCartSlurp
Dumps Gameboy and Gameboy color cartridges with a suitable reader. Code is based on the original @insidegadgets [GBCartRead](https://github.com/insidegadgets/GBCartRead) for arduino but modified to work with the wiringPi library on the Pi. The hardware consists of a Raspberry Pi and 2 MCP23017 I2C 16 way port expanders.  See GBCartSlurpWiringDiagram.svg for how to connect the Pi and configure the 23017's. Full configuration to be documented once the design is finalised.

### Deps:
[wiringPi](https://projects.drogon.net/raspberry-pi/wiringpi)
specifically the header file 23x017.h for the port name defines

### Improvements:
higher speed may be acheived with the SPI version of the MCP23S17 port expander
