---
category: research

meta:
  keywords: Image Manipulation, Image Processing, Research, Image Blending, Blending
  description: Pyramid blending project overview

project:
  title: Pyramid Blending
  preview_main: "/assets/media/research/pyramid-blending/preview.webm"
  preview_backup: "/assets/media/research/pyramid-blending/preview.mp4"

mathjax: true

figures:
  - type: figure
    content:
      -
        src: "/assets/media/research/pyramid-blending/first.jpg"
        alt: Blended image of a Quagga
        caption: 'Blended image of a <a class="link-highlight" href="https://en.wikipedia.org/wiki/Quagga">Quagga</a>'
        width: 435
        height: 290

  - type: figure
    content:
      -
        src: "/assets/media/research/pyramid-blending/second.jpg"
        alt: Result blended image
        caption: Result blended image
        width: 435
        height: 292

  - type: figure
    content:
      -
        src: "/assets/media/research/pyramid-blending/third.jpg"
        alt: Result blended image
        caption: Result blended image
        width: 435
        height: 291

sections:
  -
    - p: 'Representing an image as a <a href="https://en.wikipedia.org/wiki/Pyramid_(image_processing)">pyramid</a> has a 
number of uses in image processing.  The general process is to downsize and blur an image multiple times creating a stack 
(or pyramid) of images each at a lower resolution.'

    - figure:
        type: figure
        class: figure3
        content:
          -
            src: "/assets/media/research/pyramid-blending/first1.jpg"
            alt: White input image pyramids
            caption: White input image pyramids
            width: 200
            height: 400

          -
            src: "/assets/media/research/pyramid-blending/first2.jpg"
            alt: Mask image pyramids
            caption: Mask image pyramids
            width: 200
            height: 400

          -
            src: "/assets/media/research/pyramid-blending/first3.jpg"
            alt: Black input image pyramids
            caption: Black input image pyramids
            width: 200
            height: 400

    - p: 'The resulting pyramid can be used for things such as object recognition at different scales and certain 
types of compression.'

  -
    - p: 'In this application an image pyramid is used to create a blended image.  The smaller and more blurry images in the 
pyramid serve as a low-pass filtered version of the image. A stack of these images form what is known as a "Gaussian pyramid".'

    - figure:
        type: figure
        class: figure3
        content:
          -
            src: "/assets/media/research/pyramid-blending/second1.jpg"
            alt: White input image pyramids
            caption: White input image pyramids
            width: 208
            height: 417

          -
            src: "/assets/media/research/pyramid-blending/second2.jpg"
            alt: Mask image pyramids
            caption: Mask image pyramids
            width: 208
            height: 417

          -
            src: "/assets/media/research/pyramid-blending/second3.jpg"
            alt: Black input image pyramids
            caption: Black input image pyramids
            width: 208
            height: 417

    - p : 'The Gaussian pyramid can be used to create a high-pass filtered version of the image known as a "Laplacian pyramid".
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

    - figure:
        type: figure
        class: figure3
        content:
          -
            src: "/assets/media/research/pyramid-blending/third1.jpg"
            alt: White input image pyramids
            caption: White input image pyramids
            width: 207
            height: 424

          -
            src: "/assets/media/research/pyramid-blending/third2.jpg"
            alt: Mask image pyramids
            caption: Mask image pyramids
            width: 207
            height: 425

          -
            src: "/assets/media/research/pyramid-blending/third3.jpg"
            alt: Black input image
            caption: Black input image
            width: 207
            height: 424

    - p: This technique can be used to avoid a halo effect in images which make blend regions more noticeable.

    - figure:
        type: ul
        class: "acknowledge"
        caption: "This project implements the academic papers:"
        content:
          - '<a href="https://ieeexplore.ieee.org/document/1095851/authors#authors">The Laplacian Pyramid as a Compact Image Code</a>'
          - '<a href="http://citeseerx.ist.psu.edu/viewdoc/summary?doi=10.1.1.56.690">A Multiresolution Spline With Application to Image Mosaics</a>'
          - 'Both of which were authored by Peter Burt and Edward Adelson'
---
