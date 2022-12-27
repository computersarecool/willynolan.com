---
category: research
class: "post single-col"

meta:
  keywords: Infrared communication, IR communication, Python, Raspberry Pi
  description: Infrared communication project overview

project:
  title: Infrared Communication
  preview_main: "/assets/media/research/infrared-communication/preview.webm"
  preview_backup: "/assets/media/research/infrared-communication/preview.mp4"

sections:
  -
    - p: 'At some point in time (probably in the 1980s) my parents acquired a complete Yamaha soundsystem. Although I
loved the music, ever since I can remember, my favorite part was the tower of devices was the Yamaha MRX-70 learning capable remote (pictured in the first image of this post).'
    
    - p: 'It is massive, about six inches long, and one of the rare remotes designed to be held in "landscape" orientation.'

    - p: 'When single disc CDs players the size of car tires began to dissapear my parents decided to get rid of the system but I kept the remote
wondering if one day I would be able to use it for something else.'

    - p: 'This project focused on using a Raspberry Pi to allow the MRX-70 remote to control modern electronic devices.'
    
    - figure:
        type: figure
        content:
          -
            caption: "Yamaha MRX-70 Remote Control"
            src: /assets/media/research/infrared-communication/remote.jpg
            alt: "Yamaha MRX-70 Remote Control"
        width: 1280
        height: 719

  -
    - p: 'The Raspberry Pi microcomputer has built-in support for IR communication in the form of 
<a href="https://learn.adafruit.com/using-an-ir-remote-with-a-raspberry-pi-media-center/lirc"><abbr>LIRC</abbr></a> which 
stands for Linux Infrared Remote Control.'

    - p: 'However, for anybody that wants to interact with infrared communication directly (e.g. by using a computer program),
there are not many options. LIRC has a specific, targeted focus and is not ideal for general IR control of electronics.'

    - p: This research set out to make direct IR communication using a Raspberry Pi and Python easier.

  -
    - p: 'There are a variety of infrared protocols in existence.  A commonly used one is the <a href="https://techdocs.altium.com/display/FPGA/NEC+Infrared+Transmission+Protocol">
NEC Infrared Transmission Protocol</a>.'

    - p: This protocol is robust and a good place to start for anybody interested in learning how IR communication works.

    - p: 'A complete message (sent when a button is pressed) in the NEC protocol consists of the following (in order):'

    - ul:
      - A leading pulse

      - A pause

      - The 8-bit address for the receiving device

      - The 8-bit logical inverse of that address

      - The 8-bit command

      - The 8-bit logical inverse of the command

      - An end burst

    - figure:
        type: figure
        content:
          -
            caption: 'This image shows the command <code>16</code> sent to the address <code>59</code> (both in hex). The 
message is sent in binary with the least significant bit first.'
            src: https://www.sbprojects.net/knowledge/ir/nectrain.png
            alt: NEC IR frame
            width: 550
            height: 110

    - p: 'The logical inverse of the address and command is sent with each frame for error correction purposes.'

    - p: 'There are also messages that are transmitted for repeat presses or if the controller is operating with the
"extended" NEC protocol (which doesn''t use the logical inverse of the address).'

  -
    - p: 'As an IR remote only flashes light, a logical question would be: "how are the flashes of light interpreted 
as numbers?"'

    - p: 'IR communication uses 38khz modulation and the duration of a burst determines which binary digit is being
sent.'

    - figure:
        type: figure
        content:
          -
            caption: 'This image visualizes the modulation. The longer spaces between pulses indicate a 1, the shorter spaces 
indicate a 0.'
            src: https://www.sbprojects.net/knowledge/ir/necmodulation.png
            alt: IR modulation
            width: 425
            height: 125

    - p: 'Since the command and address inverses are sent with each frame, each message takes the same amount of time to transmit.'

    - p: 'The protocol itself is very straightforward.  The most challenging aspect in this project was dealing with 
the timing tolerances from both the remotes and the Raspberry Pi.'

    - p: 'My research explored creating an easy way to use IR communication directly from Python on a Raspberry Pi, 
specifically so old remotes could control new electronics.'
    
    - p: 'During development the following equipment was used:'

    - ul:
      - Raspberry Pi

      - <a href="https://www.vishay.com/docs/82491/tsop382.pdf">TSOP 382 IR Receiver</a>

      - Yamaha MRX-70 Learning capable remote

  -
    - p: 'The end result of this exploration was the <a href="https://pypi.org/project/irreceiver/">irreceiver</a> Python
library which is available on PyPi.'

    - p: "It is fully tested and well commented and a good place to start for someone interested in using IR 
communication with a Raspberry Pi or just interested in exploring IR in general."

    - figure:
        type: ul
        class: acknowledge
        caption: "Non-remote images and video in this post are courtesy of:"
        content:
          - <a href="https://www.sbprojects.net/knowledge/ir/index.php">SB-Projects</a> (also a great resource for this topic)
---