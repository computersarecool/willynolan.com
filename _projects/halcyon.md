---
order_number: 30

meta:
  keywords: Halcyon, Nightclub, Project, GUI, Software
  description: Halcyon nightclub lighting control

project:
  title: Halcyon
  preview_main: "/assets/media/projects/halcyon/preview.webm"
  preview_backup: "/assets/media/projects/halcyon/preview.mp4"

figures:
  - type: figure
    content:
      - src: "/assets/media/projects/halcyon/first.png"
        alt: Halcyon GUI Mockup
        width: 829
        height: 665

  - type: figure
    class: figure4
    caption: "The mapping process and eventual result."
    content:
      -
        src: "/assets/media/projects/halcyon/second1.jpg"
        alt: 3D model of LED structure
        width: 302
        height: 247

      -
        src: "/assets/media/projects/halcyon/second2.jpg"
        alt: UV map for structure
        width: 302
        height: 247

      -
        src: "/assets/media/projects/halcyon/second3.jpg"
        alt: Structure with UV map applied
        width: 302
        height: 247

      -
        src: "/assets/media/projects/halcyon/second.jpg"
        alt: Halcyon LED installation
        width: 806
        height: 316

  - type: video
    id: "351283061"

sections:  
  -
    - p: 'The software requirements for the visual control system at 
<a href="https://www.youtube.com/results?search_query=halcyon+sf">Halcyon</a> in San Francisco were straightforward. It 
needed to control nine HD projectors as well as the club lighting system.'

    - p: More interesting was the process of pixel mapping the 20 universes of individually addressable LEDs.

  -
    - p: 'Mapping LEDs is a commonly requested task. Typically people create a structure, cover it with strips of
LEDs and then want to be able to apply a video or image to that structure. This last step is usually where _projects get 
interesting.' 

    - p: 'The mapping approach used at Halcyon was very similar to how texture mapping works in 3D animation and parts
of the process are shown in the second image. The process was as follows:'

    - ul:
      - Create a 3D model of the structure with a vertex for each LED
      - Unwrap and UV map the model
      - Apply a texture to the newly UV mapped model
      - Sample the color at each vertex and set the corresponding LED to this value

  -
      - p: 'This approach also creates a 3D model so anyone can pre-visualize how content is going to appear on the 
structure in real time.'

      - p: 'The featured video is a behind the scenes look at the final installation before the nightclub opened. 
There are more examples <a href="https://www.youtube.com/results?search_query=halcyon+sf">online</a>.'
---