---
category: research

meta:
  keywords: Inpainting, Image Manipulation, Image Processing, Research
  description: Inpainting project overview

project:
  title: Inpainting
  preview_main: "/assets/media/research/inpainting/preview.webm"
  preview_backup: "/assets/media/research/inpainting/preview.mp4"

figures:
  - type: figure
    class: figure3
    content:
      -
        src: "/assets/media/research/inpainting/first1.jpg"
        alt: Original image
        caption: Original image
        width: 351
        height: 468

      -
        src: "/assets/media/research/inpainting/first2.jpg"
        alt: Mask image
        caption: Mask image
        width: 351
        height: 468

      -
        src: "/assets/media/research/inpainting/first3.jpg"
        alt: Result image
        caption: Result image
        width: 351
        height: 468

  - type: figure
    class: figure3
    content:
      -
        src: "/assets/media/research/inpainting/second1.jpg"
        alt: Original image
        caption: Original image
        width: 351
        height: 468

      -
        src: "/assets/media/research/inpainting/second2.jpg"
        alt: Mask image
        caption: Mask image
        width: 351
        height: 468

      -
        src: "/assets/media/research/inpainting/second3.jpg"
        alt: Result image
        caption: Result image
        width: 351
        height: 468

  - type: figure
    class: figure3
    content:
      -
        src: "/assets/media/research/inpainting/third1.jpg"
        alt: Original image
        caption: Original image
        width: 351
        height: 468

      -
        src: "/assets/media/research/inpainting/third2.jpg"
        alt: Mask image
        caption: Mask image
        width: 351
        height: 468

      -
        src: "/assets/media/research/inpainting/third3.jpg"
        alt: Result image
        caption: Result image
        width: 351
        height: 468"

sections:
  -
     - p: "While living in the Mission district I frequently saw a lot of tourists, a lot of graffiti and a lot of 
litter." 

     - p: "One day this finally made me very concerned! What if all of the pictures the tourists take accidentally contained graffiti or 
litter?"

     - p: "This concern led me to explore inpainting - the process of reconstructing regions of an image." 

  -
    - p: "The tool I made allows for a user to indicate the region of a photograph to be replaced and then uses 
exemplar-based texture synthesis to replace the region."

    - p: "At a high level, exemplar-based texture synthesis looks at the input photo and finds a region (the source) 
that is the best candidate to replace a patch in the selected (target) region of the image."

    - p: "While this is typically done in image editors such as Photoshop, finding a source region for 
inpainting can provide a more automated solution that is easier for those not familiar with image editing programs."

  -
    - figure:
        type: ul
        class: "acknowledge"
        caption: "This project implements the academic paper:"
        content:
          - '<a href="https://ieeexplore.ieee.org/abstract/document/1323101">Region Filling and Object Removal by 
Exemplar-Based Image Inpainting</a> by Criminisi et al.'
---