# Acer 5750G/5755G Fan Maximiser
==========================

Max out Acer 5755G/5750 Fan Speed.

**WARNING:** this is untested software that, as far as the author is concerned, writes magic values to unknown ports on your laptop. This can easily cause **BRICKING** of your device. Use at your own risk and be sure to read the source code before running! This Software has been tested on by the authors on Acer 5750G and Acer 5755G laptops. Even so, it can not be guaranteed to work on your (same model) laptop as well. You have been warned!

This repository contains source code that maximises fan speed on the Acer 5750G or 5755G (and possibly similar models). It writes one of two magic values (0x77 and 0x76) to port 0x68. One value (0x77) makes the fan spin at maximum speed, the other value makes it return to normal (BIOS-operated maybe?) mode.

Modles reported Working by users. Try on your own Risk.
* 5750G
* 5755G
* V3-571G 
* 5742G
* 5741G

The magic values, port numbers and read/write sequences were obtained by reverse engineering FanController.exe provided by Acer for Windows OEM:
http://community.acer.com/t5/Notebooks-Netbooks/Fan-Control-Problems-With-5750G-And-similar-machines/m-p/199637/highlight/true#M33756

Files and description:
* `acer_5750G_fan_controller.pl`: perl script that does the magic.
Can be invoked with `perl acer_5750G_fan_controller.pl MAX` or `perl acer_5750G_fan_controller.pl NORMAL`.
Permission to access /dev/ports is required.

For details about how this project came to be as well as how the values were obtained from FanController.exe and eblib.dll, go to http://neduard.wikidot.com/acer-fancontroller-linux

I forked the official version, just for my convenience. 
