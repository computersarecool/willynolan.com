---
category: research

meta:
  keywords: "OpenGL, DSA, Direct State Access, Computer Graphics"

project:
  title: "DSA OpenGL"
  preview: "video"
  preview_main: "/assets/media/research/dsa-opengl/preview.webm"
  preview_backup: "/assets/media/research/dsa-opengl/preview.mp4"

media:
  - type: image
    url: "/assets/media/research/dsa-opengl/first.png"
    alt: "Example tessellation shader"

  - type: image
    url: "/assets/media/research/dsa-opengl/second.png"
    alt: "Phong Lighting Model"

  - type: image
    url: "/assets/media/research/dsa-opengl/third.png"
    alt: "Real time raytracer"

sections:
  -
    - p: 'The evolution of OpenGL basically goes like this: Immediate mode -> Modern OpenGL (3.0+) -> 
<a href="https://www.khronos.org/registry/OpenGL/extensions/EXT/EXT_direct_state_access.txt">
Direct State Access</a> -> Vulkan.'

    - p: 'As the APIs have progressed, progressively more control has been given to the programmer.'

  -
    - p: 'Direct State Access (DSA) provides a nice balance between verbosity and control. In particular, minimizing 
or eliminating the “state-machine” construct with DSA makes interacting with the GPU feel much more similar to native C++.'

  -
    - p: 'Early OpenGL does not provide enough control to the user, but Vulkan can make getting started with graphics very 
intimidating and prototyping or experimenting with the GPU challenging.'

    - p: 'The research I did resulted in applications that explore many of the ways in which DSA leads to a more elegant 
programming experience.'

    - p: 'The featured images show just a few examples of applications made easier with DSA.
These include (in order) tessellation, an example of the Phong Illumination Model and a real time raytracer.'
---