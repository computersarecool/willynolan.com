---
layout: project_image_and_vimeo
permalink: /:title/
category: research

meta:
  keywords: "Planning and Control, Robobtics, Research, Software"

project:
  title: "Planning and Control"
  url: "https://willynolan.com/planning-and-control"
  logo_type: "video"
  logo: "/assets/media/research/planning-and-control/logo.webm"
  logo_backup: "/assets/media/research/planning-and-control/logo.mp4"

images:
  - image:
    url: "/assets/media/research/planning-and-control/first.png"
    alt: "Warehouse representation"

videos:
  - video:
    id: "354555624"
---
<p>

</p>

<p>
The goal of this project was to implement planning and control algorithms to guide a simulated robot through a warehouse.
</p>

<p>
The warehouse layout is described with an ASCII file where <code>#</code> symbols represent walls, numbers represent packages that 
need to be retrieved, <code>A</code> represents the starting position, <code>.</code>s represent traversable space and the <code>@</code> symbol represents 
the dropzone.
</p>

<p>
A warehouse layout for the featured image would be given as the following:
<pre class="codeblock">
.0#..
.....
..#1.
....@
....A
</pre>
</p>

<p>
The rules are as follows:
<ul>
    <li>- Packages must be picked up and dropped off in order</li>
    <li>- The robot cannot come within a certain distance of the walls or the drop off location</li>
    <li>- There are limits on the amount the robot can rotate in each time step</li>
    <li>- More efficient routes are preferred</li>
</ul>
</p>

<p>
The challenge is that sometimes package locations are not integers.  This research and my project solved this through 
discretization of the provided warehouse file and precise calculation of the robot heading.
</p>

<p>
A video showing the completion of a more complex warehouse layout is featured.
</p>
