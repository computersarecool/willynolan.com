---
category: research

meta:
  keywords: "Respectrable, Ableton, Max, Max for Live"

project:
  title: "Respectrable"
  preview: "video"
  preview_main: "/assets/media/research/respectrable/preview.webm"
  preview_backup: "/assets/media/research/respectrable/logo.mp4"

media:
  - type: image
    url: "/assets/media/research/respectrable/first.png"
    alt: "The Live Object Model"

  - type: image
    url: "/assets/media/research/respectrable/second.png"
    alt: "Respectrable"

  - type: video
    id: "354581391"

sections:
  -
    - p: "Although most people who use Ableton Live probably use it to make music, it was also one of the first Digital 
Audio Workstations (DAW) to offer a fully programmatic interface and probably still offers the best live 
performance abilities of any DAW."

  -
    - p: "Live officially supports programmatic access to every knob, button and and slider through the Live Object 
Model (LOM). The LOM can be a bit of a maze but this is expected because of the large number of 
parameters available in Live."

    - p: "There is a learning curve to figuring out how the object hierarchy works but, 
once figured out, each and every property of a Live set is reachable programmatically."

    - p: 'The repeated necessity of a scriptable, real-time audio engine, and specifically one that could be used 
wirelessly through <a href="http://opensoundcontrol.org/introduction-osc"> Open Sound Control</a> (OSC) led to
the creation of <a href="https://github.com/computersarecool/respectrable">Respectrable</a>.'

  -
    - p: "Respectrable is a Max for Live device that facilitates easily accessing the Live Object Model through 
Javascript or Max objects. The featured video shows a very simple example of bi-directional control of the Live 
and a graphical application."
---