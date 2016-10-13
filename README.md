
SB Serial USB Interface
=======================

![SB Serial USB Interface](/img/ch340.jpg?raw=true "staticboards Serial USB Interface")


Why did you make a new USB Serial Interface
===========================================


I would love to use FTDI chips. But they are quite **costly**. In most of the cases, the FTDI chip will be more expensive than the rest of the board.

But I found the **ch340g** with a cheap Arduino Clone. And I was curious about it.

I asked to one of my chinese suppliers, and they sent me a bunch of them for a very reasonable price.

Fortunately, there is some documentation for the chip!

On the other hand, I was playing with an *ESP8266* board. If you turn on the wifi, it will eat a lot of current, over 500mA. And my Bus Pirate didn’t like it very much.

So, I made this board, to see if the chip actually works, and because I need a powerful Serial USB interface.

**This is the USB serial port for makers**. It works at 5V, or at 3.3V. You only need to change the jumper.

Most of the linux distributions already have the driver installed. And in windows, it will auto install without problems.

What can you do with the SB USB Serial?
=======================================

It has a micrel **MIC39100**, a low dropout linear regulator that can convert from 5V to 3.3V. And it supports 1A of power.

So, you can power most of your prototypes using the VCC pin.

Most of the USB ports are limited in some way, and 1A is quite a lot off power. So, it is not warranted that you can use 1A with your computer.

The chip has all the modem signals for **hardware flow contro**l, You can control them with software.

For example, using python, etc. You can reset a device (*for example, to upload a new firmware*) or you can activate one led when the communication is ready.

Schematic
=========

![SB Serial USB Interface](/img/ch340g-schematic?raw=true "Schematic")
![SB Serial USB Interface](/img/ch340g-silk?raw=true "Silk Screen")
![SB Serial USB Interface](/img/ch340g-pcb?raw=true "PCB")

Features
========

 - Max Baudrate up to **2Mbps**
 - Drivers commonly available for linux and windows (I guess that also
   for osx, I have to confirm it)
 - Hardware full duplex
 - Support for common MODEM signals RTS, DTR, DCD, RI, DSR and CTS
 - Select between 5V and 3.3V with an easy jumper.
 - **Micro USB** connector
 - USB 2.0

Pins
====

 - 5V : Always 5V from the USB
 - 3V : Always 3.3V from the Linear Regulator
 - GND : Common ground
 - RX : input UART Receive Pin
 - TX : output UART Transmit Pin
 - CTS : Clear to send input
 - DSR : Data Set Ready input
 - RI : Ring In input
 - DCD : Data Carrier Detect Input
 - DTR : Data Terminal Ready Output
 - RTS : Request to Send Output
 - R232 :  Internal pull down. Active High. If enabled, it will invert the
   RX pin

Useful Links
============

https://www.staticboards.es : Author website

https://www.olimex.com/Products/Breadboarding/BB-CH340T/resources/CH340DS1.PDF : datasheet



