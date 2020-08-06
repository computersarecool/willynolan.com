---
layout: project_image_and_vimeo
permalink: /:title/
category: research

meta:
  keywords: "OpenGL, DSA, Direct State Access, Computer Graphics"

project:
  title: "DSA OpenGL"
  url: "https://willynolan.com/dsa-opengl"
  logo_type: "video"
  logo: "/assets/media/research/dsa-opengl/logo.webm"
  logo_backup: "/assets/media/research/dsa-opengl/logo.mp4"

images:
  - image:
    url: "/assets/media/research/dsa-opengl/first.png"
    alt: "Example tessellation shader"
  - image:
    url: "/assets/media/research/dsa-opengl/second.png"
    alt: "Phong Lighting Model"
  - image:
    url: "/assets/media/research/dsa-opengl/third.png"
    alt: "Real time raytracer"
videos:
---
<p>
The evolution of OpenGL basically goes like this:
Immediate mode -> Modern OpenGL (3.0+) -> 
<a href="https://www.khronos.org/registry/OpenGL/extensions/EXT/EXT_direct_state_access.txt">Direct State Access</a> -> 
Vulkan. As the APIs have progressed, progressively more control has been given the the programmer.
</p>

<p>
Direct State Access provides a nice balance between verbosity and control. 
In particular, getting rid of the “state-machine” construct makes interacting with the GPU feel much more similar to native C++.
</p>

<p>
Early OpenGL does not provide enough control to the user, but Vulkan can make getting started with graphics very 
intimidating and prototyping / experimenting with the GPU challenging.
</p>

<p>
The research I did resulted in applications that explore many of the ways in which DSA leads to a more elegant 
programming experience.
</p>

<p>
The featured images show just a few examples of applications made easier with DSA.
These include (in order) tessellation, an example of the Phong Illumincation Model and a realtime raytracer.
</p>
