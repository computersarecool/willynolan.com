---
category: _research

meta:
  keywords: HDR, Photography, Camera Response Function, Image Processing, Research, Computational Photography
  description: HDR project overview

project:
  title: "HDR // Camera Response Recovery"
  preview_main: "/assets/media/research/hdr/preview.webm"
  preview_backup: "/assets/media/research/hdr/preview.mp4"

mathjax: true

figures:
  - type: figure
    class: figure2
    content:
      -
        src: "/assets/media/research/hdr/first1.jpg"
        alt: Input images
        caption: Input images
        width: 327
        height: 327

      -
        src: "/assets/media/research/hdr/first2.jpg"
        alt: HDR Result image
        caption: HDR Result image
        width: 488
        height: 327

  - type: figure
    class: figure2 onecol
    content:
      -
        src: "/assets/media/research/hdr/second1.jpg"
        alt: Image capture pipeline
        caption: Image capture pipeline
        width: 900
        height: 129

      -
        src: "/assets/media/research/hdr/second2.jpg"
        alt: False color image showing radiance levels
        caption: False color image showing radiance levels
        width: 478
        height: 286

  - type: figure
    content:
      -
        src: "/assets/media/research/hdr/third1.jpg"
        alt: HDR input images showing example corresponding keypoints
        caption: HDR input images showing example corresponding keypoints
        width: 327
        height: 327

sections:
  -
    - p: 'Today high-dynamic-range imaging (HDRI) is ubiquitous. Many smartphones contain built-in support for HDR 
and some even default to using HDR to capture images.'

    - p: 'At a basic level, working with HDR data is all about capturing the radiance of the scene. A naive thought would 
be that pixels appearing twice as bright in an image are from areas in the photographed scene with twice as much radiance.'

    - p: 'The psuedo color image shows this is not the case. A tremendous range of radiance values have to be mapped to 
a significantly smaller range of pixel intensities.'

    - p: 'The specific non-linear response function of an individual camera is not usually published by camera makers 
who consider it a trade secret.'

    - p: 'Recovering this function allows more than just the the common "HDR look" (and the hyper-realistic 
tone-mapped style), including being able to achieve more realistic motion-blur, color correction and edge detection in 
images.'

  -
    - p: 'With a stack of aligned images at different exposures (such as in the last figure in this post) the non-linear 
response function can be recovered with the following formula:'

    - p: '$$Z_{ij} = f(E\Delta t)$$'

    - p: 'Where $i$ indexes over pixel locations and $j$ indexes over the different equations.'

    - p: 'With some manipulation this simplifies to:'

    - p: '$$ g(Z_{ij}) = \ln E_i + \ln \Delta t_j $$ Where $g = \ln f^{-1}$'

    - p: 'Written in this form $g$ (and therefore eventually $f$) can be recovered up to a scale by using the $SVD$ to 
minimize a related objective function.'

  -
    - p: 'With this function recovered the radiance can be visualized a number of ways (usually by scaling the radiance
to the display device).'

    - figure:
        type: ul
        class: "acknowledge"
        caption: "This project implements the academic papers:"
        content:
          - '<a href="https://dl.acm.org/doi/10.1145/1401132.1401174">Recovering High Dynamic Range Radiance Maps from
Photographs</a> by Paul E. Debevec and Jitendra M. Malik'

          - '<a href="https://ieeexplore.ieee.org/document/1240119">Determining the camera response from images: what is
knowable?</a> by M.D. Grossberg and S.K. Nayar'

          - '<a href="https://ieeexplore.ieee.org/document/1323796">Modeling the space of camera response functions</a> 
by M.D. Grossberg and S.K. Nayar'
---