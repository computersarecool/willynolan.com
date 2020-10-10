---
category: research

meta:
  keywords: "Planning and Control, Robotics, Research, Software"

project:
  title: "Planning and Control"
  preview: "video"
  preview_main: "/assets/media/research/planning-and-control/preview.webm"
  preview_backup: "/assets/media/research/planning-and-control/logo.mp4"

images:
  - url: "/assets/media/research/planning-and-control/first.png"
    alt: "Warehouse representation of map"
    
  - url: "/assets/media/research/planning-and-control/second.png"
    alt: "Warehouse representation of map with motion plan"
    
videos:
  - id: "354555624"

sections:  
    - content:
        - p: "The goal of this project was to implement planning and control algorithms to guide a simulated robot 
            through a warehouse."
        - p: 'The warehouse layout is described with an ASCII file where <code>#</code> symbols represent walls, numbers 
            represent packages that need to be retrieved, <code>A</code> represents the starting position, 
            <code>.</code>s represent traversable space and the <code>@</code> symbol represents the drop zone.'

    - content:
        - p: 'A warehouse layout for the featured images would be given as the following:'
        - p: '<pre>
            .0#..
            .....
            ..#1.
            .....
            A...@</pre>'
        - p: 'The rules are as follows:'
        - ul:
            - 'Packages must be picked up and dropped off in order'
            - 'The robot cannot come within a certain distance of the walls or the drop off location'
            - 'There are limits on the amount the robot can rotate in each time step'
            - 'More efficient routes are preferred'

    - content:
        - p: 'The challenge is that packages are located in fractional -- not integer -- locations. My research 
            solved this through discretization of the provided warehouse layout file and precise calculation of the 
            robot heading.'
        - p: 'The two featured images show the layout of a simple warehouse with two packages. A brief overview for 
            picking up and delivering one of the packages is shown in the second image. The green arrows show where pick up
            or drop offs happen.'
        - p: 'A video showing the completion of a more complex warehouse layout is also shown.'
---