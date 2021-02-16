---
title: "A LaTeX Thesis Template - feel free to use it!"
date: 2021-02-16
author_profile: true
layout: single
excerpt: "Heriot-Watt University only had one PhD Thesis template, which dated from 2013 and had a shield that looked like it was traced in MS Paint, I've updated it now."
header:
  overlay_color: "#4b75fe"
  show_overlay_excerpt: true
  
categories:
  - blog
tags:
  - PhD
  - misc
  - code
 
---
A quick update here - I have now produced a new and updated LaTeX PhD Thesis template for Heriot-Watt University. If you aren't at Heriot-Watt feel free to adapt and update it to your needs as well. 

I have mainly done this now as I'm approached the 2.5 year mark in my PhD, and have a mean collection of spare figures that aren't relevant for publication, but _are_ relevant to my research more broadly. 

The main updates I've implemented are quite simple but nice, especially for students who don't use much LaTeX:
  1. Better University shield for the title page (previous one was a trace, mine is at least a nice crop of an svg)
  2. subfiles support - this means you can now typeset individual parts of chapters of the thesis, without rendering all of it at once. This saves a lot of time for people with Theses particularly full of images
  3. Replaced the glossaries package with the acro package, a simple way to include specialist terms you might have to type repeatedly, like Alloy names, chemicals etc.
  4. Added more maths packages for typesetting
  5. A little bit of context and humour - added a few examples of each bit of functionality, and linked the university guidelines on what a thesis needs, just to make it more self-contained
  
My forked Github repo is public, so you can [click here to access it](https://github.com/AlexandreCoates/HW_LaTex_thesis_template), and download it, then use it in Overleaf or offline in your favourite LaTeX editor. 
I have also made the repository a template, meaning you should be able to copy the thing wholesale without any of the commit history. Forking is still possible too of course.

Any comments or wonderful ideas? Feel free to contact me