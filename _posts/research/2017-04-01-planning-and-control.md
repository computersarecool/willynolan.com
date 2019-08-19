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
The goal of this project was to implement planning and control algorithms to guide a simulated robot through a 
warehouse.
</p>

<p>
The warehouse was described with an ASCII file where <code>#</code> symbols represented walls, numbers represented 
packages that needed to be retreived <code>A</code> represented the starting position and the <code>@</code> symbol 
represented the drop off location.
</p>

<p>
The rules are as follows:
<ul>
  <li>- Packages must be picked up and dropped off in order</li>
  <li>- The robot cannot come within a certain distance of the walls or the drop off location</li>
  <li>- More efficient routes are preferred</li>
</ul>
</p>

<p>
This problem can be solved through discretization of the provided grid and precise calculation of the robot heading. 
</p>
