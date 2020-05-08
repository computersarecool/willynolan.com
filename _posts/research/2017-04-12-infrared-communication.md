---
layout: plain
permalink: /:title/
category: research

meta:
  keywords: "Structured Light, Geometric Camer Calibration, Projector Calibration, Projection Mapping"

project:
  title: "Structured Light Calibration"
  url: "https://willynolan.com/structured-light-calibration"
  logo_type: "video"
  logo: "/assets/media/research/structured-light-calibration/logo.webm"
  logo_backup: "/assets/media/research/structured-light-calibration/logo.mp4"
---
<p>
Infrared (IR) communication is one of the lowest-cost ways to control electronics.
Additionally, a Raspberry Pi is one of the cheapest ways to explore electronics.
</p>

<p>
The Raspberry Pi microcomputer has built-in support for IR communication in the form of 
<a href="https://learn.adafruit.com/using-an-ir-remote-with-a-raspberry-pi-media-center/lirc"> LIRC</a> which 
stands for Linux Infrared Remote Control.
</p>

<p>
However, for anybody that wants more low-level control of what happens when an IR command is received, there are not 
many options.
</p>

<p>
For instance, if someone wanted to use a vintage remote control to control a webserver, LIRC would not work. 
</p>

<p>
There are a variety of infrared protocols in existence.  A commonly used one is the <a href="https://techdocs.altium.com/display/FPGA/NEC+Infrared+Transmission+Protocol">
NEC Infrared Transmission Protocol</a>.
</p>

<p>
This protocol is robust and a good place to start for anybody interested in IR protocol.
The complete message (from one button press) consists of the following (in order):
</p>

<ul>
    <li>A leading pulse</li>
    <li>A pause</li>
    <li>The 8-bit address for the receiving device</li>
    <li>The 8-bit logical inverse of that address</li>
    <li>The 8-bit command</li>
    <li>The 8-bit logical inverse of the command</li>
    <li>A final end burst</li>
</ul>

<p>
There are also other messages that can be transmitted for repeat buttons or if the controller is operating with the 
"extended" NEC protocol (which doesn't use the logical inverse of the address).
</p>

<p>
The protocol itself is very straightforward.  The most challenging thing was dealing with tolerances from remotes 
and from the Raspberry pi.
</p>

<p>
Testing used:
</p>

<ul>
    <li>Raspberry Pi</li>
    <li><a href="https://www.vishay.com/docs/82491/tsop382.pdf">TSOP 382 IR Receiver</a>
    <li>YAMAHA MRX-70 Learning capable remote</li>
</ul>

<p>
This research project resulted in the <a href="https://pypi.org/project/irreceiver/"><code>irreceiver</code></a> Python
library which is available on PyPi.
</p>
