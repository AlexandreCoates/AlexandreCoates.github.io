---
title: "Interactive Localisation, thanks to Bokeh"
date: 2021-07-22
author_profile: true
layout: single
excerpt: "Using Bokeh I can turn the figures I use to understand localisation into something interactive. More coming soon."
header:
  overlay_color: "#84CBBD"
  show_overlay_excerpt: true
  
categories:
  - blog
tags:
  - PhD
  - misc
  - code
 
---
The latest from me is that I have submitted [my first preprint to ArXiv](https://arxiv.org/abs/2106.12567), **Localisation determines the optimal noise rate for quantum transport**. 
It is the result of a few years of fumbling around in the dark until I found a result I ultimately thought was quite neat. Namely, that the eigenstate localisation of a system can tell you a lot about the relative importance of different Environment-Assisted Quantum Transport (ENAQT) effects. 
I'm hoping to write a nice popular summary before the referees get back to me, but before that I felt it might be good to stretch myself and try some new programming. 

Namely, I decided to try and make some bits of the paper interactive, to show how different forms of localisation occur. 

Setup: consider a chain of 10, two level systems with nearest neighbour coupling. Perhaps Calcium ions coupled to each other by lasers. If you put these sites in a linear potential (increasing the energy at one end for example), you would expect to see Wannier-Stark localisation. 
Just below you should _hopefully_ be able to play around with just that, varying the potential with respect to a bond strength _J_ and seeing how the eigenenergies change their spacing, as well as seeing the eigenstates contract onto fewer and fewer sites until each eigenstate only overlaps with its neighbours. 

 <embed type="text/html" src="/assets/wannier-N10.html" width="600" height="500"> 
Then here we have Anderson localisation, pull a random value from a Gaussian distribution and apply it to each site. The increasing disorder exponentially increases the amount of destructive interference in the system, also localising it, but in a much more disordered way. (For visual simplicity, one set of random disorders has been generated and you can scale those up and down). 
 <embed type="text/html" src="/assets/anderson-N10.html" width="600" height="500"> 

These two were made in Bokeh, an open-source more web-friendly visualisation suite than matplotlib which I've made most of my other figures in. Who knows, maybe more interactive visualisations lie in my future