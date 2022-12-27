---
meta:
  keywords: Power Glove, Project, Hardware
  description: Power Glove hardware remix project overview

project:
  title: Power Glove
  preview_main: "/assets/media/projects/power-glove/preview.webm"
  preview_backup: "/assets/media/projects/power-glove/preview.mp4"

figures:
  - type: figure
    content:
      - src: "/assets/media/projects/power-glove/first.png"
        alt: "The original Power Glove"
        width: 1123
        height: 493

  - type: figure
    content:
      - src: "/assets/media/projects/power-glove/second.png"
        alt: "The Power Glove PCB and circuit layout"
        width: 936
        height: 340

  - type: video
    id: "350044732"

sections:
  -
    - p: In the summer of 2011 I was getting into DJing and was having a hard time breaking free from my computer.

    - p: 'I wanted to be able to move and control the music at the same time. All the MIDI controllers I found required a USB 
cable to be connected to the computer.  Clearly this was an untenable situation!'

    - p: 'For some reason I started to look at video game controllers as a solution, and specifically the Power Glove. 
Today there are many modified versions of the Power Glove controlling a variety of things but back in 2011, I could only
find two examples.'

  -
    - p: 'The most influential version was from 
<a href="http://biphenyl.org/blog/2009/04/03/the-power-glove-20th-anniversary-edition">biphenyl</a>. The issue 
with this modification was that most of the buttons on the glove did not work after the retrofitting process.'

    - p: 'The other version I found came from <a href="https://www.youtube.com/watch?v=J1hiacj1R2Y&ab_channel=Dubspot">
Yueda Ben-Atar</a> who used an adapter cable to convert the Power Glove to work over USB. The issue was this version 
was that the positional data would not work and Power Glove still had to be tethered to a computer.'

  -
    - p: 'In order to combine the strengths of each version of these modified gloves it was clear I would need to 
fabricate my own printed circuit board (PCB) with the same form factor as the original Power Glove circuit board.'

    - p: "The finished circuit diagram and final board design are shown in the second featured image. Once the PCB 
had been designed and manufactured, adding a bluetooth module, accelerometer (for positional data) and accessing the 
Power Glove's built-in bend sensors was a straightforward process."

    - p: 'The featured video shows an early proof of concept. Eventually I used this as a DJ controller and after a 
few shows was interviewed for the documentary <a href="https://thepowerofglove.com/" class="nobreak">The Power of Glove</a>.'
---