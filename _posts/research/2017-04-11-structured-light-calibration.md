---
category: research
class: "post single-col"

meta:
  keywords: "Structured Light, Geometric Camera Calibration, Projector Calibration, Projection Mapping"

project:
  title: "Structured Light Calibration"
  preview: "video"
  preview_main: "/assets/media/research/structured-light-calibration/preview.webm"
  preview_backup: "/assets/media/research/structured-light-calibration/preview.mp4"

mathjax: true

sections:
  -
    - p: 'There is a rich body of research surrounding camera calibration.  The process is usually broken up into <em>
geometric</em> and <em>radiometric / photometric</em> calibration.'

    - p: 'Projectors can essentially be thought of the inverse of a camera.  Instead of projecting a scene onto an 
image plane, they project an image plane onto an environment.'

    - p: 'Due to this similarity, projector calibration is a topic of interest in the interactive computer 
graphics field.'

    - p: 'In a projection mapping context, usually what is meant by "projector calibration" is "putting content where it
is supposed to go in a physical environment".'

  -
    - p: 'There are many strategies for performing camera calibration, but using structured light is a popular one and 
it is built into several applications such as <a href="https://madmapper.com">MadMapper</a> and 
<a href="https://www.disguise.one/en/">disguise</a>.'

  -
    - p: 'In this research, <a href="http://www.michaelwalczyk.com/">Mike Walczyk</a> and I explored the structured light 
process based on the original academic paper to describe the technique.'

    - p: 'To explain a structured light process imagine there is a room and for some reason you want to project an image directly where two 
walls meet.'

    - figure:
        type: figure
        content:
          -
            src: "/assets/media/research/structured-light-calibration/first.jpg"
            alt: "Texture Mapping LEDs"
            caption: "Example room"

    - p: "In the above picture that would be a corner of the room, for instance the corner located at the top of the 
above image."

    - p: "For illustration purposes let's say the image you want to project is this simple checkerboard image (using 
the letter F to show distortion):"

    - figure:
        type: figure
        content:
          -
            src: "/assets/media/research/structured-light-calibration/second.jpg"
            alt: "Texture Mapping LEDs"
            caption: "Example room"

  -
    - p: "If you project that image directly onto the corner, the image will show obvious distortion."

    - figure:
        type: figure
        content:
          -
            src: "/assets/media/research/structured-light-calibration/third.jpg"
            alt: "Texture Mapping LEDs"
            caption: "Example room"

    - p: "Using structured light, which is essentially the simultaneous projection and photographing of different black 
and white images, this problem can be fixed. Example structured light patterns are below."

    - figure:
        type: figure
        content:
          -
            src: "/assets/media/research/structured-light-calibration/fifth.jpg"
            alt: "Texture Mapping LEDs"
            caption: "Example room"

  -
    - p: "A structured light process allows for the acquisition of a complete mapping (which the source paper refers to 
as $R$) from the camera pixels to the projector pixels."
  
    - p: "This can be used to project content without distortion from the position of the viewer.
At the end of the process the image can be projected with corrected perspective."

    - figure:
        type: figure
        content:
          -
            src: "/assets/media/research/structured-light-calibration/fourth.jpg"
            alt: "Texture Mapping LEDs"
            caption: "Example room"

    - p: "Our research included a Python implementation of structured light calibration as well as a projector/camera 
simulator."

    - figure:
        type: ul
        class: "acknowledge"
        caption: "This project implemented the academic paper:"
        content:
          - '<a href="https://ieeexplore.ieee.org/document/1240253">Multi-projectors for Arbitrary Surfaces Without Explicit
          Calibration nor Reconstruction</a> by J.-P. Tardif et al.'
---