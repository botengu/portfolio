---
layout: post
title:  Chladni Plates for Music Visualization
permalink: "/music/chladni/"
---

<div class="w3-row">
    <h1 style="text-align:center">Chladni Plates for Music Visualization</h1>
      <p class = "justify">
      When particles are thrown on a plate, and that plate is vibrating at a certain frequency, those particles will arrange in a certain pattern. Those patterns are commonly known as the Chladni plates/ Since notes are simply the frequencies with particular waves, Chladni plates are a great opportunity to visualize music.
        </p>
        <p class = "justify">
        I had first heard of those patterns on the interview of John Anthony West on the Joe Rogan podcast, and since then, I have been interested in the math behind them. It turns out that it is just a partial differential equation (PDE). As a trained engineer, PDEs are a fundamental part of our curriculum; there is the basis for a few of our courses.<br /> In summary, when any medium resonates, there are locations along with the medium where there is no displacement. A Chladni pattern is the location of all zero-displacement on a plate that resonates. All locations along the plate are allowed to resonate, which makes it an open boundary problem. The vibration is introduced at the ends of the plate. The maximum displacement at the different locations of the plate is given by the function f(x,y) such that: <br />
        $$f(x,y) = { C \cdot cos\left( \frac{m \cdot \pi\cdot x}{a}\right)\cdot cos \left( \frac{n \cdot \pi\cdot y}{b} \right) + 
        D \cdot cos\left( \frac{p \cdot \pi\cdot x}{a}\right)\cdot cos \left( \frac{q \cdot \pi\cdot y}{b} \right) }$$
        where a and b are the dimensions of the plates, m,n,p and q are constant related to the frequency of the vibration and C and D are related to the amplitude of the vibration. 
        </p>
      <div class="w3-main w3-center" >
          <img src="/portfolio/assets/img/wave.png" width="40%" height="40%">
          <figcaption>Surface of f(x,y) for a particular combination of m,n,p and q</figcaption>
      </div>
      <div class="w3-main w3-center" >
          <img src="/portfolio/assets/img/wave1.png" width="40%" height="40%">
          <figcaption>Level set of surface for an isovalue of 0</figcaption>
      </div>
      <p class = "justify">
     Level sets can be evolved by switching between various frequency values; the following images show different ways frequency values can be changed to obtain a different shape. 
      </p>
      <div class="w3-main w3-center" >
          <img src="/portfolio/assets/img/Chladni-gradual.gif" width="50%" height="50%">
          <figcaption>The frequency related constants all have the same values and they are increased continously </figcaption>
      </div>
    <div class="w3-main w3-center" >
          <img src="/portfolio/assets/img/Chladni-shift.gif" width="50%" height="50%">
          <figcaption>The frequency related constants all have the same values and they switched discretly from an intial value to a final value</figcaption>
      </div>
      <p class = "justify">
    Another interesting thing that can be tried is switched between different combinations of frequency values switch between them. This essentially what musicians do when playing notes.  
      </p>
          <div class="w3-main w3-center" >
          <img src="/portfolio/assets/img/Chladni_different.gif" width="50%" height="50%">
          <figcaption>The frequency related constants all have the same values and they switched discretly between 3 different configurations/combinations</figcaption>
      </div>
</div>



