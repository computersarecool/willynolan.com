---
layout: default
permalink: /:title/
category: research

meta:
  keywords: "Seam Carving, Liquid Resizing, Liquid Rescaling, Image Manipulation, Research"

project:
  title: "Seam Carving"
  url: "https://willynolan.com/seam-carving"
  preview: "video"
  preview_main: "/assets/media/research/seam-carving/preview.webm"
  preview_backup: "/assets/media/research/seam-carving/logo.mp4"

media:
  - type: image
    url: "/assets/media/research/seam-carving/first.png"
    alt: "Original image of two airplanes"
  - type: image
    url: "/assets/media/research/seam-carving/second.png"
    alt: "Original image of two airplanes with seams marked for removal"
  - type: image
    url: "/assets/media/research/seam-carving/third.png"
    alt: "Result image of two airplanes with seams removed"
  - type: image
    url: "/assets/media/research/seam-carving/fourth.png"
    alt: "Image of motorcycle in all three stages of seam carving"
  - type: image
    url: "/assets/media/research/seam-carving/fifth.png"
    alt: "Image of birds"
  - type: image
    url: "/assets/media/research/seam-carving/sixth.png"
    alt: "Image of birds with seams marked for insertion"
  - type: image
    url: "/assets/media/research/seam-carving/seventh.png"
    alt: "Result image of birds"
---
<p>
Cropping an image is typically limited to selecting rectangular portions of an image and removing them.
Enlarging an image typically means stretching an image which can result in pixelation.
<a href="https://en.wikipedia.org/wiki/Seam_carving">Seam Carving</a>,
also known as Liquid Resizing is a technique that removes both of these limitations.
</p>

<p>
Seam carving works by finding the low-energy seams of the image and then removing vertical or horizontal
(but not necessarily straight) seams from the image. In this context low-energy seams are single-pixel wide parts of the 
image where there is not much change. Because the seams occur in areas where there is not much change, their removal is 
less likely to be noticed.
</p>

<p>
For this implementation I created a program that uses a Sobel filter to determine low-energy seams in the input image.
These seams are marked with red in the featured images accompanying this post.
</p>

<p>
The technique can also be used to increase image size, essentially by working in reverse. The idea is to identify 
seams that would have been removed and then insert seams in those locations as again, these seems are unlikely to be
noticed.  
</p>

<p>
In the last series of featured images newly added seams are marked in green. The color of the added seams in the final
image is calculated by averaging the color of pixels on either side of the image.
This is known as “seam insertion” and its usefulness is one reason “Liquid Resizing” could be a better name for this
general algorithm.
</p>

<p>
This technique has been implemented in several image editing programs including both
<a href="https://helpx.adobe.com/photoshop/using/content-aware-scaling.html">Photoshop </a> and
<a href="http://liquidrescale.wikidot.com/en:tutorial">Gimp</a>.
</p>

<p>
This project implements the academic paper
<a href="http://www.faculty.idc.ac.il/arik/SCWeb/imret/imret.pdf">
    Region Filling and Object Removal by Exemplar-Based Image Inpainting
</a>
by Shai Avidan and Ariel Shamir.
</p>
