---
category: research

meta:
  keywords: "Inpainting, Image Manipulation, Image Processing, Research"

project:
  title: "Inpainting"
  preview_main: "/assets/media/research/inpainting/preview.webm"
  preview_backup: "/assets/media/research/inpainting/preview.mp4"

figures:
  - type: figure
    class: figure3
    content:
      -
        src: "/assets/media/research/inpainting/first1.jpg"
        alt: "Texture Mapping LEDs"
        caption: "Original Image"
      -
        src: "/assets/media/research/inpainting/first2.jpg"
        alt: "Texture Mapping LEDs"
        caption: "Mask Image"
      -
        src: "/assets/media/research/inpainting/first3.jpg"
        alt: "Texture Mapping LEDs"
        caption: "Result Image"

  - type: figure
    class: figure3
    content:
      -
        src: "/assets/media/research/inpainting/second1.jpg"
        alt: "Texture Mapping LEDs"
        caption: "Original Image"
      -
        src: "/assets/media/research/inpainting/second2.jpg"
        alt: "Texture Mapping LEDs"
        caption: "Mask Image"
      -
        src: "/assets/media/research/inpainting/second3.jpg"
        alt: "Texture Mapping LEDs"
        caption: "Result Image"

  - type: figure
    class: figure3
    content:
      -
        src: "/assets/media/research/inpainting/third1.jpg"
        alt: "Texture Mapping LEDs"
        caption: "Original Image"
      -
        src: "/assets/media/research/inpainting/third2.jpg"
        alt: "Texture Mapping LEDs"
        caption: "Mask Image"
      -
        src: "/assets/media/research/inpainting/third3.jpg"
        alt: "Texture Mapping LEDs"
        caption: "Result Image"

sections:
  -
     - p: "While living in the Mission district I frequently saw a lot of tourists, a lot of graffiti and a lot of 
litter." 

     - p: "One day I grew concerned - what if all of the pictures the tourists take accidentally contained graffiti or 
litter?"

     - p: "This concern led me to explore inpainting - the process of reconstructing regions of an image." 

  -
    - p: "The tool I made allows for a user to indicate the region of a photograph to be replaced and then uses 
exemplar-based texture synthesis to replace the region."

    - p: "At a high level, exemplar-based texture synthesis looks at the input photo and finds a region (the source) 
that is the best candidate to replace a patch in the selected (target) region of the image."

  -
    - figure:
        type: ul
        class: "acknowledge"
        caption: "This project implements the academic paper:"
        content:
          - '<a href="https://ieeexplore.ieee.org/abstract/document/1323101">Region Filling and Object Removal by 
Exemplar-Based Image Inpainting</a> by Criminisi et al.'
---