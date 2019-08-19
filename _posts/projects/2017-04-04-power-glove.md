---
layout: project_image_and_vimeo
permalink: /:title/
category: projects

meta:
  keywords: "Power Glove, Project, Hardware"

project:
  title: "Power Glove"
  url: "https://willynolan.com/power-glove"
  logo_type: "video"
  logo: "/assets/media/projects/power-glove/logo.webm"
  logo_backup: "/assets/media/projects/power-glove/logo.mp4"

images:
  - image:
    url: "/assets/media/projects/power-glove/first.png"
    alt: "The Power Glove hardware"
  - image:
    url: "/assets/media/projects/power-glove/second.png"
    alt: "The Power Glove PCB and circuit layout"

videos:
  - video:
    id: "350044732"
---
<p>
In the Summer of 2011 I was getting into DJing and was having a hard time breaking free from my computer.  I wanted to 
be able to move and control the music at the same time. All the MIDI controllers I found required a USB cable connected 
to the computer.  Clearly this was an untenable situation!
</p>

<p>
For some reason I started to look at video game controllers as a solution, and specifically the Power Glove. 
Today there are many modified versions of the Power Glove controlling a variety of things but back in 2011 I could only find two examples. 
The most influential version was from <a href="http://biphenyl.org/blog/2009/04/03/the-power-glove-20th-anniversary-edition">biphenyl</a>. The issue with 
this was that most of the buttons on the panel did not work after the modification. The other example was from 
Yueda Ben-Atar who used an adapter cable to convert the Power Glove to USB. The issue was this version was that the 
positional data would not work and Power Glove still had to be tethered to a computer.
</p>

<p>
In order to combine the strengths of each of these hacked gloves I needed to fabricate my own PCB that would have the same 
form factor as the original Power Glove circuit board. You can see the finished circuit diagram and final board design 
in the second featured image. Once this was complete, adding a bluetooth module, accelerometer (for positional data) 
and using the Power Glove’s built-in bend sensors was a straightforward process.
</p>

<p>
The featured video shows an early proof of concept.  Eventually I used this as a DJ controller and after 
a few shows was interviewed for the documentary <a href="https://thepowerofglove.com/">The Power of Glove</a>.
</p>