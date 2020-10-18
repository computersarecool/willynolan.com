---
category: research

meta:
  keywords: OpenGL, DSA, Direct State Access, Computer Graphics
  description: DSA OpenGL project overview

project:
  title: DSA OpenGL
  preview_main: "/assets/media/research/dsa-opengl/preview.webm"
  preview_backup: "/assets/media/research/dsa-opengl/preview.mp4"

figures:
  - type: figure
    class: figure3
    content:
      -
        src: "/assets/media/research/dsa-opengl/first.jpg"
        alt: Tessellation example
        caption: Tessellation example
        width: 598
        height: 600

      -
        src: "/assets/media/research/dsa-opengl/second.jpg"
        alt: Phong illumination example
        caption: Phong illumination example
        width: 292
        height: 292

      -
        src: "/assets/media/research/dsa-opengl/third.jpg"
        alt: Raytracer example
        caption: Raytracer example
        width: 292
        height: 292

sections:
  -
    - p: 'The evolution of OpenGL basically goes like this: Immediate mode -> Modern OpenGL (3.0+) -> 
<a href="https://www.khronos.org/registry/OpenGL/extensions/EXT/EXT_direct_state_access.txt">
Direct State Access</a> -> Vulkan.'

    - p: 'As the APIs have progressed, progressively more control has been given to the programmer.'

    - p: 'Direct State Access (DSA) provides a nice balance between verbosity and control. In particular, minimizing 
or eliminating the “state-machine” construct with DSA makes interacting with the GPU feel much more similar to native C++.'

    - p: 'Early OpenGL does not provide enough control to the user, but Vulkan can make getting started with graphics very 
intimidating and prototyping or experimenting with the GPU challenging.'

    - p: 'The research I did resulted in applications that explore many of the ways in which DSA leads to a more elegant 
programming experience.'

    - p: 'The featured images shows just a few examples of graphics techniques made easier with DSA. These include 
tessellation, an example of the Phong Illumination Model and a real time raytracer.'
---