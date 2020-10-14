---
meta:
  keywords: "Perspective Projection, UV Mapping, Computer Graphics"

project:
  title: "Perspective Projection"
  preview: "video"
  preview_main: "/assets/media/projects/perspective-projection/preview.webm"
  preview_backup: "/assets/media/projects/perspective-projection/preview.mp4"

media:
  - type: image
    url: "/assets/media/projects/perspective-projection/first.jpg"
    alt: "Multi-colored cube in 3D environment"
  
  - type: image
    url: "/assets/media/projects/perspective-projection/second.png"
    alt: "Cube map in cross form"

    
sections:
  -
    - p: "Projecting content onto a non-planar surface has many technical elements that can make it tricky. However, 
once the technological and physical challenges of projecting an image onto a surface are handled (rigging and 
blending projectors, supplying power, tuning the playback system etc.) it really comes down to content."

    - p: 'Unfortunately most "projection mapping" projects turn into what are essentially slide shows on buildings.'

    - p: 'In order to make a significantly interesting projection project, the concept of <i>perspective</i> must be addressed.'

    - p: "Let's start out with something simple, such as a multi-colored cube."

  -
    - p: "The resulting UV map for a cube typically looks like a cross because that is what you would get if you cut
the seams of a box and unwrapped the object."

    - p: "This map alone is enough to create some content but it would be quite challenging to create any 
movement. If, for example, text were supposed to scroll from the yellow square to the magenta square (which 
would make sense from the camera's viewpoint) it would have to make an illogical jump on the cube map."

    - p: "The key is to think and work in 3D."

    - p: "What if we wanted to created a 3D scene where the box is actually a see through container with things 
floating inside it? Or what if we wanted the box to appear as a solid, reflective object with something floating 
outside it?"

    - p: "For that we would need to create a perspective projection."
  
  -
    - p: "For our example cube the process goes like this:"

    - ul:
         - '<p>Create a 3D scene and render it from the eventual viewer''s perspective 
            <img src="/assets/media/projects/perspective-projection/third.jpg" alt="Colored Cube" height="325" width="325" class="margin-center"></p>'

         - '<p>Add a new set of UV coordinates to the the cube <i>from the perspective of the camera that rendered the scene</i>'

         - '<p>Apply the rendered image as a texture to the model and bake the texture to a new material on the same mesh with 
the original UV coordinate (i.e. cube map coordinates)'

    - p: 'The resulting cube map will look strange on its own, but when reapplied to the object it wall look perspective-correct.'  

    - p: "For example here is the object with a solid green color and the 3D scene (blue spheres) visible."

    - raw: '<img src="/assets/media/projects/perspective-projection/fifth.jpg" alt="Colored Cube" height="325" width="325">'
  
    - p: "And here is the image with the blue spheres removed but the perspective texture map applied."

    - raw: '<img src="/assets/media/projects/perspective-projection/sixth.jpg" alt="Colored Cube" height="325" width="325">'

  -
    - raw: '<figure>
<img src="/assets/media/projects/perspective-projection/seventh.jpg" alt="Colored Cube" height="325" width="325">
<figcaption>Applying the texture <em>and</em> the original scene can also be helpful in understanding how projection 
works as one can see which parts of the 3D scene were mapped to the cube.
</figcaption>'

  -
    - p: 'This process can be difficult to figure out and tedious to do repeatedly. The project I made explored 
automated ways to texture bake perspective-correct projections in modeling software.'
---