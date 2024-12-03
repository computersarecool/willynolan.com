---
class: "post single-col"

meta:
  keywords: Perspective Projection, UV Mapping, Computer Graphics
  description: Perspective projection project overview

project:
  title: Perspective Projection
  preview_main: "/assets/media/projects/perspective-projection/preview.webm"
  preview_backup: "/assets/media/projects/perspective-projection/preview.mp4"

sections:
  -
    - p: "Projecting content onto a non-planar surface has many technical elements that can make it tricky. However, 
once the technological and physical challenges of projecting an image onto a surface are handled (rigging and 
blending projectors, supplying power, tuning the playback system etc.) it really comes down to content."

    - p: 'Unfortunately most "projection mapping" _projects turn into what are essentially slide shows on buildings.'

    - p: 'In order to make a significantly interesting projection project, the concept of <i>perspective</i> must be 
addressed.'

    - p: "Let's start out with something simple, such as a multi-colored cube."

    - figure:
        type: figure
        content:
          -
            src: "/assets/media/projects/perspective-projection/first.jpg"
            alt: Multi-colored cube in 3D environment
            width: 325
            height: 325

  -
    - p: "The resulting UV map for a cube typically looks like a cross because that is what you would get if you cut
the seams of a box and unwrapped the object."

    - figure:
        type: figure
        content:
          -
            src: "/assets/media/projects/perspective-projection/second.png"
            alt: Multi-colored cube map
            width: 325
            height: 325

    - p: "This map alone is enough to create some content but it would be quite challenging to create any 
movement. If, for example, text were supposed to scroll from the yellow square to the magenta square (which 
would make sense from the camera's viewpoint) it would have to make an illogical jump on the cube map."

    - p: The key is to think and work in 3D.

    - p: "What if we wanted to create a 3D scene where the box is actually a see through container with things 
floating inside it? Or what if we wanted the box to appear as a solid, reflective object with something floating 
outside it?"

    - figure:
        type: figure
        content:
          -
            src: "/assets/media/projects/perspective-projection/third.jpg"
            alt: Multi-colored cube in 3D environment
            width: 325
            height: 325

    - p: "For that we would need to create a perspective projection."

  -
    - p: "In our example cube the process goes like this:"

    - ul:
         - 'Create a 3D scene and render it from the eventual viewer''s perspective'

         - 'Add a new set of UV coordinates to the cube <i>from the perspective of the camera that rendered the scene</i>'

         - 'Apply the rendered image as a texture to the model and bake the texture to a new material on the same mesh with 
the original UV coordinate (i.e. cube map coordinates)'

    - p: The resulting cube map will look strange on its own, but when reapplied to the object it will look perspective-correct.
      
    - figure:
        type: figure
        content:
          -
            src: "/assets/media/projects/perspective-projection/fourth.png"
            alt: Perspective cube map
            width: 325
            height: 325

    - p: For example here is the object with a solid green color and the 3D scene (blue spheres) visible.

    - figure:
        type: figure
        content:
          -
            src: "/assets/media/projects/perspective-projection/fifth.jpg"
            alt: 3D scene and cube without the cube map applied
            width: 577
            height: 325

    - p: And here is the image with the blue spheres removed but the perspective texture map applied.

    - figure:
        type: figure
        content:
          -
            src: "/assets/media/projects/perspective-projection/sixth.jpg"
            alt: 3D scene and cube with the cube map applied

    - figure:
        type: figure
        content:
          -
            src: "/assets/media/projects/perspective-projection/seventh.jpg"
            alt: 3D scene and cube with the cube map applied

    - p: This process can be difficult to figure out and tedious to do repeatedly.

    - p: The project I made explored automated ways to texture bake perspective-correct projections in modeling software.
---