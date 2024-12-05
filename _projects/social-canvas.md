---
order_number: 50

layout: default
meta:
  keywords: MGM Cotai Stadium, Emoji, Social Canvas, WeChat, Project, Software
  description: Social Canvas project overview

project:
  title: Social Canvas
  preview_main: "/assets/media/projects/social-canvas/preview.webm"
  preview_backup: "/assets/media/projects/social-canvas/preview.mp4"

figures:
  - type: figure
    content:
      - src: "/assets/media/projects/social-canvas/first.jpg"
        alt: Social Canvas Layout
        width: 1024
        height: 640

  - type: video
    id: "354169578"

  - type: video
    id: "354168138"

sections:
  -
    - p: "Social Canvas is probably the world's largest multiplayer game installation.  It functions like most 
tile-matching video games except on a much, much larger scale. It was created in 2018 and installed at the MGM Cotai in 
Macau."

  -
    - p: 'Visitors to MGM Cotai can quickly join the game by scanning a QR code and submit entries by sending 
messages to a dedicated WeChat channel.'

    - p: 'These entries are then displayed in “The Spectacle”, MGM’s term for the world’s largest area of permanent 
indoor LED screens that makes up their lobby and casino entrance.'

  -
    - p: 'In addition to the scale of this installation it is also unique in that it is truly interactive. Guests are 
allowed to directly participate in the game, creating a shared experience for all.' 

    - p: 'MGM''s write up is <a href="https://www.mgm.mo/en/cotai/art/art-tour/collaboration/social-canvas">here</a>. 
The featured videos show an overview of the project and a demo of the project in action.'

    - figure:
        type: ul
        class: "acknowledge under"
        caption: "Acknowledgements:"
        content:
          - "Database programming: Michael Clement"
          - "Show System: Matt Ragan"
---

<main class="{{ page.class }}">
    <h2 class="{{ page.class }}">{{ page.project.title }}</h2>

{%- for section in page.sections %}
    <section class="{{ page.class }}">
    {%- for element in section %}
        {%- if element.raw %}
        {{ element.raw }}

        {%- elsif element.p %}
        <p class="{{ page.class }}">{{ element.p }}</p>

        {%- elsif element.bq %}
        <blockquote class="{{ page.class }}">
            <p>{{ element.bq }}</p>
        </blockquote>

        {%- elsif element.ul %}
        <ul class="{{ page.class }}">
            {%- for li in element.ul %}
            <li class="{{ page.class }}">
                <p>{{ li }}</p>
            </li>
            {%- endfor %}
        </ul>

        {%- else %}
        {%- assign figelem = element.figure %}
        {%- include post-figure.html %}

        {%- endif %}
    {%- endfor %}
    </section>
{%- endfor %}

{%- for figelem in page.figures %}
    {%- include post-figure.html %}
{%- endfor %}
</main>