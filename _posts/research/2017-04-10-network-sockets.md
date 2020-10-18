---
category: research
class: "post single-col"

meta:
  keywords: "Sockets, Networking, Berkeley Sockets"

project:
  title: "Sockets"
  preview: "video"
  preview_main: "/assets/media/research/sockets/preview.webm"
  preview_backup: "/assets/media/research/sockets/preview.mp4"

sections:
  -
    - p: 'Programming network sockets directly, rather than using an abstraction or library, is a challenging task.
This holds true in any language that exposes sockets be it C and C++ or Python or Rust.'

    - p: 'Challenging as though they may be, sockets provide an essential part of most modern computing, particularly interactive
computing. Networked communication is often a preferred way to get devices to talk to each other, from microcontrollers and embedded 
devices to enterprise servers.'

    - p: 'Furthermore, the basic API for sockets is actually not that complicated, with most of the semantics not changing much 
since <a href="https://en.wikipedia.org/wiki/Berkeley_sockets"> Berkeley Sockets</a>.
Even today modern operating systems implement some version of the Berkeley socket interface.'

  -
    - p: "To explore sockets further I created an application in C++ that allows a user to interactively:"

    - ul:
      - Create a TCP or UDP

      - Client or Server

      - Specify the port to send data to or to listen on

    - p: 'The result was a greater appreciation for sockets and for the libraries and programs that make them easier to use.'

    - figure:
        type: ul
        class: "acknowledge"
        caption: "Much of the code used was adapted from:"
        content:
          - '<a href="https://beej.us/guide/bgnet/">Beej''s Guide to Network Programming: Using Internet Sockets</a> by 
Brian Beej Jorgensen Hall'
---