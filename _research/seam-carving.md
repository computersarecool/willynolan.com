---
order_number: 40

category: _research

meta:
  keywords: Seam Carving, Liquid Resizing, Liquid Rescaling, Image Manipulation, Research
  description: Seam carving project overview

project:
  title: Seam Carving
  preview_main: "/assets/media/research/seam-carving/preview.webm"
  preview_backup: "/assets/media/research/seam-carving/preview.mp4"

figures:
  - type: figure
    class: figure3
    content:
      -
        src: "/assets/media/research/seam-carving/first.jpg"
        alt: Original image
        caption: Original image
        width: 1278
        height: 566

      -
        src: "/assets/media/research/seam-carving/second.jpg"
        alt: Image with seams marked
        caption: Image with seams marked
        width: 1280
        height: 570

      -
        src: "/assets/media/research/seam-carving/third.jpg"
        alt: Result image
        caption: Result image
        width: 852
        height: 570

  - type: figure
    class: figure3 baseline
    content:
      -
        src: "/assets/media/research/seam-carving/fourth1.jpg"
        alt: Original image
        caption: Original image
        width: 274
        height: 564

      -
        src: "/assets/media/research/seam-carving/fourth2.jpg"
        alt: Image with seams marked
        caption: Image with seams marked
        width: 274
        height: 564

      -
        src: "/assets/media/research/seam-carving/fourth3.jpg"
        alt: Result image
        caption: Result image
        width: 412
        height: 564

  - type: figure
    class: figure3
    content:
      -
        src: "/assets/media/research/seam-carving/fifth.jpg"
        alt: Original image
        caption: Original image
        width: 752
        height: 570

      -
        src: "/assets/media/research/seam-carving/sixth.jpg"
        alt: Image with seams marked
        caption: Image with seams marked
        width: 1131
        height: 570

      -
        src: "/assets/media/research/seam-carving/seventh.jpg"
        alt: Result image
        caption: Result image
        width: 1129
        height: 570

sections:
  -
    - p: 'Cropping an image is typically limited to selecting rectangular portions of an image and removing them.
Enlarging an image typically means stretching an image which can result in pixelation.'

    - p: '<a href="https://en.wikipedia.org/wiki/Seam_carving">Seam carving</a>, also known as "Liquid Resizing" is a 
technique that removes both of these limitations.'

    - p: 'Seam carving works by finding the low-energy seams of the image and then removing vertical or horizontal
(but not necessarily straight) seams from the image.'

    - p: 'In this context low-energy seams are single-pixel wide parts of the image where there is not much change. 
Because the seams occur in areas where there is not much change, their removal is less likely to be noticed.'

  -
    - p: 'For this implementation I created a program that uses a Sobel filter to determine low-energy seams in the 
input image. These seams are marked with red in the featured images accompanying this post.'

    - p: 'The technique can also be used to increase image size, essentially by working in reverse.'

    - p: 'The idea is to identify seams that would have been removed and then insert seams in those locations as again these 
seams are (as with seam removal) unlikely to be noticed.'

  -
    - p: 'In the last series of featured images newly added seams are marked in green. The color of the added seams in the final
image is calculated by averaging the color of pixels on either side of the image.' 

    - p: 'This is known as "seam insertion" and its usefulness is one reason "liquid resizing" could be a better name for this algorithm in 
general.'

    - p: 'This technique has been implemented in several image editing programs including both
<a href="https://helpx.adobe.com/photoshop/using/content-aware-scaling.html">Photoshop</a> and
<a href="http://liquidrescale.wikidot.com/en:tutorial">Gimp</a>.'

    - figure:
        type: ul
        class: "acknowledge"
        caption: "This project implements the academic paper:"
        content:
          - '<a href="http://www.faculty.idc.ac.il/arik/SCWeb/imret/imret.pdf">Seam Carving for Content-Aware Image 
Resizing</a> by Shai Avidan and Ariel Shamir.'
---
