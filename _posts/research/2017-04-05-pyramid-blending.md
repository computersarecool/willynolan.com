---
category: research

meta:
  keywords: "Image Manipulation, Image Processing, Research, Image Blending, Blending"

project:
  title: "Pyramid Blending"
  preview: "video"
  preview_main: "/assets/media/research/pyramid-blending/preview.webm"
  preview_backup: "/assets/media/research/pyramid-blending/preview.mp4"

mathjax: true

media:
  - type: figure4
    caption: "The mapping process and eventual result."
    imgs:
      -
        src: "/assets/media/research/pyramid-blending/first1.jpg"
        alt: "Texture Mapping LEDs"
        caption: "Original Image"
      -
        src: "/assets/media/research/pyramid-blending/first2.jpg"
        alt: "Texture Mapping LEDs"
        caption: "Mask Image"
      -
        src: "/assets/media/research/pyramid-blending/first3.jpg"
        alt: "Texture Mapping LEDs"
        caption: "Result Image"
      -
        src: "/assets/media/research/pyramid-blending/first.jpg"
        alt: "Texture Mapping LEDs"
        caption: "Result Image"

  - type: figure4
    caption: "The mapping process and eventual result."
    imgs:
      -
        src: "/assets/media/research/pyramid-blending/third1.jpg"
        alt: "Texture Mapping LEDs"
        caption: "Original Image"
      -
        src: "/assets/media/research/pyramid-blending/third2.jpg"
        alt: "Texture Mapping LEDs"
        caption: "Mask Image"
      -
        src: "/assets/media/research/pyramid-blending/third3.jpg"
        alt: "Texture Mapping LEDs"
        caption: "Result Image"
      -
        src: "/assets/media/research/pyramid-blending/third.jpg"
        alt: "Texture Mapping LEDs"
        caption: "Result Image"

  - type: figure4
    caption: "The mapping process and eventual result."
    imgs:
      -
        src: "/assets/media/research/pyramid-blending/third1.jpg"
        alt: "Texture Mapping LEDs"
        caption: "Original Image"
      -
        src: "/assets/media/research/pyramid-blending/third2.jpg"
        alt: "Texture Mapping LEDs"
        caption: "Mask Image"
      -
        src: "/assets/media/research/pyramid-blending/third3.jpg"
        alt: "Texture Mapping LEDs"
        caption: "Result Image"
      -
        src: "/assets/media/research/pyramid-blending/third4.jpg"
        alt: "Texture Mapping LEDs"
        caption: "Result Image"

sections:
  -
    - p: 'Representing an image as a <a href="https://en.wikipedia.org/wiki/Pyramid_(image_processing)">pyramid</a> has a 
number of uses in image processing.  The general process is to downsize and blur an image multiple times creating a stack 
(or pyramid) of images each at a lower resolution.'

    - p: 'The resulting pyramid can be used for things such as object recognition at different scales and certain 
types of compression.'

    - p: 'In this application the image pyramid is used to create a blended image.  The smaller and more blurry images in the 
pyramid serve as a low-pass filtered version of the image. A stack of these forms a Gaussian pyramid.'

  -
    - p : 'The Gaussian pyramid can be used to create a high-pass filtered version of the image called a Laplacian pyramid.
The formula for a Laplacian pyramid at a level $i$ is given as:'

    - p: '$$ \begin{aligned}
L_{i} = G_{i} - (K * G_{i})
\end{aligned}
$$'


    - p: 'Where $K$ is the downsize and blur operator and $G_{i}$ represents an image from the Gaussian pyramid at level $i$.
Expanding and adding images from the Laplacian pyramid can recreate the original image with no data loss.'

  -
    - p: 'Effectively this means that a wider blend region can be used in low-frequency content and a
narrower blend region can be used in high-frequency content such as edges.'

    - p: 'This technique can be used to avoid a halo effect in images which make blend regions more noticeable.'
  -
    - figul:
        - '<a href="https://ieeexplore.ieee.org/document/1095851/authors#authors">The Laplacian Pyramid as a Compact Image Code</a>'
        - '<a href="http://citeseerx.ist.psu.edu/viewdoc/summary?doi=10.1.1.56.690">A Multiresolution Spline With Application to Image Mosaics</a>'
        - '<p>Both of which were authored by Peter Burt and Edward Adelson</p>'
      figcaption: "This project implements the academic papers:"
---
