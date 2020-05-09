---
layout: plain
permalink: /:title/
category: research

meta:
  keywords: "Structured Light, Geometric Camer Calibration, Projector Calibration, Projection Mapping"

project:
  title: "Infrared Communication"
  url: "https://willynolan.com/infrared-communication"
  logo_type: "video"
  logo: "/assets/media/research/infrared-communication/logo.webm"
  logo_backup: "/assets/media/research/infrared-communication/logo.mp4"
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
However, for anybody that wants to interact with infrared communication directly (e.g. in a Python program)
there are not many options.
</p>

<p>
For instance, if someone wanted to use a vintage remote control to control a webserver, LIRC would be less than ideal.
</p>

<p>
There are a variety of infrared protocols in existence.  A commonly used one is the <a href="https://techdocs.altium.com/display/FPGA/NEC+Infrared+Transmission+Protocol">
NEC Infrared Transmission Protocol</a>.
</p>

<p>
This protocol is robust and a good place to start for anybody interested in learning how IR communication works.
</p>

<p>
The complete message (which is sent when a button is pressed) consists of the following (in order):
</p>

<ul class="extra-bottom">
    <li>- A leading pulse</li>
    <li>- A pause</li>
    <li>- The 8-bit address for the receiving device</li>
    <li>- The 8-bit logical inverse of that address</li>
    <li>- The 8-bit command</li>
    <li>- The 8-bit logical inverse of the command</li>
    <li>- A final end burst</li>
</ul>

<p>
So an example command would look like:
<img class="research-post" alt="NEC IR frame" src="https://www.sbprojects.net/knowledge/ir/nectrain.png">
</p>

<p>
This image shows the command <code>16</code> sent to the address <code>59</code> (both in hex).
Mapping the bits to the actual command can be tricky as they are sent in binary, with the least significant bit first.
</p>

<p>
The logical inverse of the address and command is sent with each frame for error correction purposes.
</p>

<p>
There are also other messages that can be transmitted for repeat buttons or if the controller is operating with the 
"extended" NEC protocol (which doesn't use the logical inverse of the address).
</p>

<p>
As an IR remote only flashes light, a logical question would be, how are the flashes interpreted as numbers?
IR communication uses 38khz modulation and the length of time in a burst determines which binary digit is being 
sent. Graphically this looks like:
<img class="research-post" alt="IR modulation" src="https://www.sbprojects.net/knowledge/ir/necmodulation.png">
Where the longer spaces between pulses indicate a 1 and shorter spaces indicate a 0.
</p>

<p>
Because the command and address inverses are sent with each frame, each message should take the same amount of time to transmit.
</p>

<p>
The protocol itself is very straightforward.  The most challenging aspect was dealing with the timing tolerances 
from both the remotes and and from the Raspberry pi.
</p>


<p>
During research the following equipment was used:
</p>

<ul class="extra-bottom">
    <li>Raspberry Pi</li>
    <li><a href="https://www.vishay.com/docs/82491/tsop382.pdf">TSOP 382 IR Receiver</a></li>
    <li>YAMAHA MRX-70 Learning capable remote</li>
</ul>

<p>
This end result of this exploration was the <a href="https://pypi.org/project/irreceiver/">irreceiver</a> Python
library which is available on PyPi. It is fully tested and well commented and a good place for someone interested in
using IR communication with a Raspberry Pi or just interested in exploring the protocol more.
</p>

<small class="last-paragraph">
    All images and video in accompanying this post are courtesy of <a href="https://www.sbprojects.net/knowledge/ir/index.php">SB-Projects</a> 
    which is a great resource for this topic.
</small>
