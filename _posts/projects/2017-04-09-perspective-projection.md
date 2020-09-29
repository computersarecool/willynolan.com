---
layout: plain
permalink: /:title/
category: projects

meta:
  keywords: "Perspective Projection, UV Mapping, Computer Graphics"

project:
  title: "Perspective Projection"
  url: "https://willynolan.com/perspective-projection"
  preview: "video"
  preview_main: "/assets/media/projects/perspective-projection/preview.webm"
  preview_backup: "/assets/media/projects/perspective-projection/logo.mp4"
---
<p>
Projecting content onto a non-planar surface has many technical elements that can make it tricky. However, once the 
technological and physical challenges of projecting an image onto a surface are handled (rigging and blending projectors
, supplying power, tuning the playback system etc.) it really comes down to content.
</p>

<p>
Unfortunately most "projection mapping" projects turn into what are essentially slide shows on buildings.
</p>

<p>
In order to make a significantly interesting projection project, the concept of <span class="highlight small">perspective</span> 
must be addressed.
</p>

<p>
Let's start out with something simple, such as a multi-colored cube.
</p>

<img class="end-post" src="/assets/media/projects/perspective-projection/first.png" alt="Colored Cube" height="325" width="325">

<p>
The resulting UV map for a cube typically looks like a cross because that is what you would get if you cut the seams 
of a box and unwrapped the object.
</p>
<img class="end-post one-outline" src="/assets/media/projects/perspective-projection/second.png" alt="Colored Cube" height="325" width="325">

<p>
This map alone is enough to create some animation, but it would be quite challenging to create any movement. If, for 
example, text were supposed to scroll from the yellow square to the magenta square (which would make sense from the 
camera's viewpoint) it would have to make an illogical jump on the cube map.
</p>

<p>
The key is to think and work in 3D.
</p>

<p>
What if we wanted to created a 3D scene where the box is actually a see through container with things floating inside it?
Or what if we wanted the box to be a solid, reflective object with something floating outside it?
</p>

<p>
For that we would need to create a perspective projection.
</p>

<p>
For our example cube the process goes like this:
</p>

<ul>
    <li>
        <p>
            - Create a 3D scene and render it from the eventual viewer's perspective
            <img class="end-post" src="/assets/media/projects/perspective-projection/third.png" alt="Colored Cube" height="325" width="325">
        </p>
    </li>
    <li>
        <p>
            - Add a new set of UV coordinates to the the cube <i>from the perspective of the camera that rendered the scene</i>
        </p>
    </li>
    <li>
        <p>
            - Apply the rendered image as a texture to the model and bake the texture to a new material on the same mesh with 
            the original UV coordinate (i.e. cube map coordinates)
        </p>
    </li>
</ul>

<img class="end-post one-outline" src="/assets/media/projects/perspective-projection/fourth.png" alt="Colored Cube" height="325" width="325">

<p>
The resulting cube map will look strange on its own, but when reapplied to the object it wall look perspective-correct.  
</p>

<p>
For example here is the object with a solid green color and the 3D scene (blue spheres) visible.
<img class="end-post" src="/assets/media/projects/perspective-projection/fifth.png" alt="Colored Cube" height="325" width="325">
And here is the image with the blue spheres removed but the perspective texture map applied.
<img class="end-post" src="/assets/media/projects/perspective-projection/sixth.png" alt="Colored Cube" height="325" width="325">
The only difference is in the first image some default lighting is used by the 3D modeling program.
</p>

<p>
Applying the texture <em>and</em> the original scene can also be helpful in understanding how projection works as one 
can see which parts of the 3D scene were mapped to the cube.
<img class="end-post" src="/assets/media/projects/perspective-projection/seventh.png" alt="Colored Cube" height="325" width="325">
</p>

<p class="last-paragraph">
This process can be difficult to figure out and tedious to do repeatedly.
The project I made explored automated ways to texture bake perspective-correct projections in modeling software.
</p>