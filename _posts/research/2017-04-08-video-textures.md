---
category: research

meta:
  keywords: "Video, Video textures, Photography, Image Processing, Research, Computational Photography"

project:
  title: "Video Textures"
  preview: "video"
  preview_main: "/assets/media/research/video-textures/preview.webm"
  preview_backup: "/assets/media/research/video-textures/logo.mp4"

mathjax: true

media:
  - type: image
    url: "/assets/media/research/video-textures/first.png"
    alt: "video-textures image created from a radiance map"

  - type: image
    url: "/assets/media/research/video-textures/second.png"
    alt: "Image acquisition pipeline and false color image of radiance map"

sections:
  -
    - p: "A video texture is somewhere between a video and an image. The idea is to create the appearance of an 
infinitely long video from a fixed-length input video, saving data the process."

    - p: "The concept is similar to a seamlessly looping video except, in the case of video textures, playback jumps around between similar 
frames providing infinite iterations."

  -
    - p: "The process of creating a video texture starts with a video volume which is essentially a stack of the input video frames.
The root mean square deviation between every frame against every other frame and itself is computed and stored in
a transition matrix. The closer the similarity metric is to zero, the more similar the two frames are."
  
    - p: 'Then a transition difference matrix is determined by looking at the two frames ahead and behind.  This is because
even though two frames may be very similar, the content before or after may not be which would cause problems. Values
in the transition difference matrix are calculated as:
$$T_{ij} = \sum_{k=-2}^{2} B * S[i + k, j + k])$$
Where $T$ is the transition matrix $B$ is a binomial filter, $S$ is the similarity matrix and $i$ and $j$ are indexes into $S$.'

  -
    - p: "In practice these matrices could be used to infinitely loop the input video without ever repeating the same transition.
To make the effect even more convincing, techniques such as alignment, blending and brightness correction could be applied."

    - p: "The program I made finds the longest, smoothest loop and extracts those frames to be made into a video loop."

    - p: "The thumbnail video shows the entire original source video next to a transition matrix proceeding with no random seeking
      in the clip. The featured images show other possible transitions that could be chosen and their associated start and end
      frames."

    - p: "The original publication on which my research is based is:"

    - ul:
      - '<a href="https://dl.acm.org/doi/10.1145/344779.345012">Video Textures</a> by Arno Sch&ouml;dl et al.'
---