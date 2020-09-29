---
layout: project_image_and_vimeo
permalink: /:title/
category: research

meta:
  keywords: "Inpainting, Image Manipulation, Image Processing, Research"

project:
  title: "Inpainting"
  url: "https://willynolan.com/inpainting"
  preview: "video"
  preview_main: "/assets/media/research/inpainting/preview.webm"
  preview_backup: "/assets/media/research/inpainting/logo.mp4"

images:
  - image:
    url: "/assets/media/research/inpainting/first.png"
    alt: "Demonstration of inpainting on litter"
  - image:
    url: "/assets/media/research/inpainting/second.png"
    alt: "Demonstration of inpainting on graffiti"
  - image:
    url: "/assets/media/research/inpainting/third.png"
    alt: "Demonstration of inpainting on a pattern"
videos:
---
<p>
Living in the Mission district I frequently see a lot of tourists, a lot of graffiti and a lot of litter. One day I 
grew concerned - what if all of the pictures the tourists take accidentally contained graffiti or litter?
</p>

<p>
This concern led me to explore inpainting - the process of reconstructing regions of an image. The tool I made allows 
for a user to indicate the region of a photograph to be replaced and then uses exemplar-based texture synthesis to fill 
in the region.
</p>    

<p>
At a high level, exemplar-based texture synthesis looks at the input photo and finds a region (the source) 
that is the best candidate to replace a patch in the selected (target) region of the image. 
</p>  
    
<p>
This project implements the academic paper 
<a href="https://ieeexplore.ieee.org/abstract/document/1323101">Region Filling and Object Removal by Exemplar-Based Image Inpainting</a>
by Criminisi et al.
</p>
