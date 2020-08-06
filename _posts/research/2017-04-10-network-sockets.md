---
layout: project_simple
permalink: /:title/
category: research

meta:
  keywords: "Sockets, Networking, Berkeley Sockets"

project:
  title: "Sockets"
  url: "https://willynolan.com/sockets"
  logo_type: "video"
  logo: "/assets/media/research/sockets/logo.webm"
  logo_backup: "/assets/media/research/sockets/logo.mp4"
---
<p>
Programming networks sockets directly, rather than using an abstraction or library, is a challenging task.
This holds true in any language that exposes sockets from C and C++ to Python and Rust.
</p>

<p>
Challenging as though they may be, sockets provide an essential part of most modern computing, particularly interactive
computing.
Networked communication is often a preferred way to get devices to talk to each other, from microcontrollers and embedded 
devices to enterprise servers.
</p>

<p>
Furthermore, the basic API for sockets is actually not that complicated, with most of the semantics not changing much 
since <a href="https://en.wikipedia.org/wiki/Berkeley_sockets"> Berkeley Sockets</a>.
Even today modern operating systems implement some version of the Berkeley socket interface.
</p>

<p>
To explore sockets further I created an application in C++ that allows as user to interactively:
</p>

<ul>
    <li><p>- Create a TCP or UDP</p></li>
    <li><p>- Client or Server</p></li>
    <li><p>- Specify the port to send data to or to listen on</p></li>
</ul>

<p>
The result was a greater appreciation for sockets and for the libraries and programs that make them easier to use.
</p>

<p>
Much of the code was adapted from:
</p>
<ul>
    <li>
        <a href="https://beej.us/guide/bgnet/">
            Beej's Guide to Network Programming: Using Internet Sockets Video Textures
        </a>
         by Brian "Beej Jorgensen" Hall
    </li>
</ul>

