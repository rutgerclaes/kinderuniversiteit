# Kinderuniversiteit guide

## Hardware

We currently have:

1. 10 Raspberry Pi 2 Model B's,
2. 20 MicroSD 8GB cards with SD card adapter,
3. 20 [TrafficHat's](https://ryanteck.uk/hats/1-traffichat-0635648607122.html) (actually 21, but one is not functioning)
4. 20 HDMI to DVI adapters
5. 20 Micro USB power adapters

*You will need to find an additional 10 Raspberry Pi 2 Model B's to use the 20 Traffichats.*

## Software

To run the workshop, I prepared an [image](image.img.bz2) based on [Raspian Jessie](https://www.raspberrypi.org/downloads/raspbian/).  On this image I did the following:

1. Install [ScratchGPIO7](http://simplesi.net/scratchgpio/scratch-raspberrypi-gpio/),
2. Configured Belgian AZERTY keyboards
3. Created a basic Scratch worksheet with the signals preconfigured
4. Wrote a small `reset.sh` bash script

The `reset.sh` script copies the basic worksheet into `~/Documents/Scratch
Projects/rsc.sb`.  When ScratchGPIO is started using the desktop icon, it will
open this file, `~/Documents/Scratch Projects/rsc.sb`.

The desktop icon acts as a shortcut to a script starting Scratch and a GPIO server in the background.  This is done as root.  If the user overwrites the `rsc.sb` file he will do so as root.  In this case, the `reset.sh` script will give an error and you need to run it as root.

## Handouts

I prepared [handouts](handouts.md).  You can generate an HTML version using [Pandoc](http://pandoc.org/): 

```
pandoc handouts.md -s -c pandoc.css -t html5 -o handouts.html
```

## Preparation

1. Check the display connectors in the room, you need monitors that have a HDMI or DVI input.
2. Check the keyboards.  You might need to alter the image if they are not AZERTY.
3. Write the (image)[image.img.bz2] to the Micro SD cards.
4. Print the handouts.
5. Install the old [Scratch 1.4](https://scratch.mit.edu/scratch_1.4/) on your machine.  If you use the new web based scratch it gets confusing when you demo stuff.

