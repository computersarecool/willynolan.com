---
category: _research

meta:
  keywords: Panorama, Photography, Image Processing, Research, Computational Photography
  description: Panorama project overview

project:
  title: Panorama
  preview_main: "/assets/media/research/panorama/preview.webm"
  preview_backup: "/assets/media/research/panorama/preview.mp4"

figures:
  - type: figure
    class: figure3
    caption: Input images (top) and resulting panorama image
    content:
      -
        src: "/assets/media/research/panorama/first1.jpg"
        alt: Input image 1
        width: 284
        height: 206

      -
        src: "/assets/media/research/panorama/first2.jpg"
        alt: Input image 2
        width: 285
        height: 206

      -
        src: "/assets/media/research/panorama/first3.jpg"
        alt: Input image 3
        width: 285
        height: 206

      -
        src: "/assets/media/research/panorama/first.jpg"
        alt: Result panorama image
        width: 900
        height: 295

  - type: figure
    content:
      -
        src: "/assets/media/research/panorama/second.png"
        alt: Image alignment and warping
        caption: Image alignment and warping
        width: 859
        height: 418

  - type: figure
    content:
      -
        src: "/assets/media/research/panorama/third.png"
        alt: Input images warped and blended
        caption: Input images warped and blended
        width: 847
        height: 408

sections:
  -
    - p: Creating a panorama can be seen as the combination of many different computational photography techniques.

    - p: Depending on the situation warping, blending, and corner detection may all be used.

    - p: There are many tools that create very nice panoramas but looking at the process at each step can be quite illuminating.

    - p: 'This _research resulted in a program that makes panoramas by finding a homography between the input images, warping
them into alignment, performing a multi-frequency blend and then an automated cropping.'

  -
    - p: 'First the corners of all the input images need to be found.  Then matches between the two images need to be located. 
In this project, the OpenCV <a href="https://docs.opencv.org/3.4/d3/da1/classcv_1_1BFMatcher.html">Brute Force Matcher</a> 
was used to find matches between the images.'

    - p: 'Once there is a list of the matching features between the images a homography can be found that connects the images. 
At this point, the “canvases” of the input image can be warped so that they align.'
    
  -
    - p: "The second featured image shows an outline of how the three images canvases (shown in purple, green and pink)
were warped after finding matching points."

    - p: 'After warping the images can be stitched and blended through a variety of ways. This project used 
<a href="/pyramid-blending">pyramid blending.</a>'

    - figure:
        type: ul
        class: "acknowledge"
        caption: "This project followed an approach described in:"
        content:
          - '<a href="http://szeliski.org/Book/">Computer Vision: Algorithms and Applications</a> by Richard Szeliski'
---