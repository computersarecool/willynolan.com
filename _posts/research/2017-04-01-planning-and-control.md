---
category: research

meta:
  keywords: Planning and Control, Robotics, Research, Software
  description: Planning and control project overview

project:
  title: Planning and Control
  preview_main: "/assets/media/research/planning-and-control/preview.webm"
  preview_backup: "/assets/media/research/planning-and-control/preview.mp4"

figures:
  - type: figure
    class: narrow
    content:
      - src: "/assets/media/research/planning-and-control/first.jpg"
        alt: Graphic representation of a warehouse
        caption: Graphic representation of a warehouse
        width: 651
        height: 747

  - type: figure
    class: narrow
    content:
      - src: "/assets/media/research/planning-and-control/second.jpg"
        alt: Graphic representation of a warehouse with motion plan
        caption: Graphic representation of a warehouse with motion plan
        width: 653
        height: 750

  - type: video
    id: "354555624"

sections:  
  -
    - p: The goal of this project was to implement planning and control algorithms to guide a simulated delivery robot through a warehouse.

    - p: 'The warehouse layout is described with an ASCII file where <code>#</code> symbols represent walls, numbers 
represent packages that need to be retrieved, <code>A</code> represents the starting position, 
<code>.</code>s represent traversable space and the <code>@</code> symbol represents the drop zone.'

    - p: 'For example, the warehouse layout for the images in this post would be given as:'

    - raw: "
<pre class='code-diagram margin-center'>
.0#..\n
.....\n
..#1.\n
.....\n
A...@
</pre>
"

  -
    - p: 'The general restrictions for movement are as follows:'

    - ul:
        - Packages must be picked up and dropped off in order

        - The robot cannot come within a certain distance of the walls or the drop-off location

        - There are limits on the amount the robot can rotate in each time step

        - More efficient routes are preferred

    - p: The challenge is that packages are located in fractional -- not integer -- locations.

    - p: My research into planning and control solved this through discretization of the provided warehouse layout file and precise calculation of the robot heading.

  -
    - p: 'The two featured images show the layout of a simple warehouse with two packages. A brief overview for 
picking up and delivering one of the packages is shown in the second image. The green arrows show where the pickup and
drop off events took place.'

    - p: 'The featured video shows the completion of a more complex warehouse layout.'
---