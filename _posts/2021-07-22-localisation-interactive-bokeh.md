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

toc: true
toc_label: "My Table of Contents"
toc_icon: "cog"

---
# What's new?
The latest from me is that I have submitted [my first preprint to ArXiv](https://arxiv.org/abs/2106.12567), **Localisation determines the optimal noise rate for quantum transport**. 
It is the result of a few years of fumbling around in the dark until I found a result I ultimately thought was quite neat. Namely, that the eigenstate localisation of a system can tell you a lot about the relative importance of different Environment-Assisted Quantum Transport (ENAQT) effects. 
I'm hoping to write a nice popular summary before the referees get back to me, but before that I felt it might be good to stretch myself and try something new.  

Namely, I decided to try and make some figure from the paper interactive, to show how different forms of localisation occur, as I think playing around gives a new sense of intuition. 
My work focussed on chains of two level systems, coupled to their neighbours, and looked at how localising them changed the importance of different ENAQT effects. 

So for these two visualisations we consider a chain of 10 two-level sites, say Calcium ions as experimentalists have done that. For the mathematically minded that would be $$H = \sum_{i = 1}^{N-1} |i>< i+1 | + |i+1>< i|.$$ If you were to change the energy linearly across the system by applying a field for example, you would observe Wannier-Stark localisation. 
That is, the eigenstates of the system contract, and are spread out over a smaller number of sites. The upshot being, they overlap with fewer of the other system eigenstates. The intuition is quite simple, vary the energy across a system, and in the eigenbasis, the high energy eigenstates will all be at one end, and *vice versa*.

## Wannier-Stark Localisation
You can play around with exactly that effect below. This shows the eigenstates of a length 10 system, and you can vary the difference in energy across the system in terms of the bond strength *J*, and the sites they are present on. The size of the diamonds are proportional to the propability density of the eigenstate being on that site. 
Note how the eigenstates overlap with fewer of their friends as the potential increases.  
<div class="iframe-container"> 
<iframe src="/assets/wannier-N10.html" title="Wannier-Stark localisation of length 10 chain" height = "500" width = "100%">  
 </iframe> 
</div>

## Anderson Localisation
Then here we have Anderson localisation, the one that always pops up in reality because it's hard to make anything perfect! The intuition is again quite simple, if you add random spikes to the system energy (manufacturing or experimental defects perhaps), then you get lots of destructive interference in the system. 
The result is the classic, exponential Anderson localisation. Here for visual clarity one set of random energies has been pulled from a Gaussian distribution, and applied to a degenerate chain. As you increase the anderson disorder, you scale up the size of these spikes and troughs. You should see a much less ordered localisation process. 
<div class="iframe-container"> 
<iframe src="/assets/anderson-N10.html" title="Anderson localisation of length 10 chain" height = "500" width = "100%">  
 </iframe> 
</div>

These two were made in Bokeh, an open-source and slightly more web-friendly visualisation suite than matplotlib (which I've made most of my other figures in). It was a slightly painful learning experience as I had to touch some javascript to make these work. 
But it was worthwhile nevertheless, or maybe I'm too easily entertained by little web interactives!

In any case, with this out of the way, the next step is to write a little popular summary - and maybe see if I can justify making any more interactive figures on the way. 
If you're interested in the preprint, do follow the arXiv link at the top, we did our best to make it as readable a paper as possible!

Until the next time, take care.