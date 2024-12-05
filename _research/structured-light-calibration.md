---
order_number: 110

category: _research
class: "post single-col"

meta:
  keywords: Structured Light, Geometric Camera Calibration, Projector Calibration, Projection Mapping
  description: Structured light project overview

project:
  title: Structured Light Calibration
  preview_main: "/assets/media/research/structured-light-calibration/preview.webm"
  preview_backup: "/assets/media/research/structured-light-calibration/preview.mp4"

mathjax: true

sections:
  -
    - p: 'There is a rich body of _research surrounding camera calibration.  The process is usually broken up into <em>
geometric</em> and <em>radiometric / photometric</em> calibration.'

    - p: 'Projectors can essentially be thought of the inverse of a camera.  Instead caputuring a scene projected onto an 
image plane as a camera does, projectors project an image plane onto an environment.'

    - p: 'Due to this similarity, projector calibration is a topic of interest in the interactive computer 
graphics field.'

    - p: 'In a projection mapping context, usually what is meant by "projector calibration" is "placing video content where it
is supposed to go in a physical environment".'

  -
    - p: 'There are many strategies for performing camera calibration, with structured light being a popular one which is implemented 
in several applications such as <a href="https://madmapper.com">MadMapper</a> and <a href="https://www.disguise.one/en/">disguise</a>.'

  -
    - p: 'In this _research, <a href="http://www.michaelwalczyk.com/">Mike Walczyk</a> and I explored the structured light 
"projector calibration" process based on the academic paper which first described the technique.'

    - p: 'To explain the structured light process it helps to imagine there is a room (like in the figure below) and for 
some reason you want to project an image where two walls meet.'

    - figure:
        type: figure
        content:
          -
            src: "/assets/media/research/structured-light-calibration/first.jpg"
            alt: Example room
            caption: Example room
            width: 500
            height: 442

    - p: "In the above picture that would be a corner of the room, for instance the corner located at the top of the 
above image."

    - p: "For illustration purposes let's say the image you want to project is this simple checkerboard image (which is overlaid with
the letter F to show distortion):"

    - figure:
        type: figure
        content:
          -
            src: "/assets/media/research/structured-light-calibration/second.jpg"
            alt: Pattern to project
            caption: Pattern to project
            width: 500
            height: 500

  -
    - p: "If you project that image directly onto the corner, the image will show obvious distortion."

    - figure:
        type: figure
        content:
          -
            src: "/assets/media/research/structured-light-calibration/third.jpg"
            alt: Pattern projected with distortion
            caption: Pattern projected with distortion
            width: 640
            height: 360

    - p: "Using structured light (in this case that means the simultaneous projection and photographing of different black 
and white images) the distortion can be fixed."

    - figure:
        type: figure
        content:
          -
            src: "/assets/media/research/structured-light-calibration/fifth.jpg"
            alt: Example structured light patterns
            caption: Example structured light patterns
            width: 215
            height: 144

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
            alt: Perspective corrected image projected
            caption: Perspective corrected image projected
            width: 640
            height: 360

    - p: "Our _research included a Python implementation of structured light calibration as well as a projector/camera 
simulator which was used to create the images in this post."

    - figure:
        type: ul
        class: "acknowledge"
        caption: "This project implemented the academic paper:"
        content:
          - '<a href="https://ieeexplore.ieee.org/document/1240253">Multi-projectors for Arbitrary Surfaces Without Explicit
          Calibration nor Reconstruction</a> by J.-P. Tardif et al.'
---