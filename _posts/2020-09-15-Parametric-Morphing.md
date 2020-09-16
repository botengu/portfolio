---
layout: post
title:  Morphing Parametrized Surfaces  
date:   2020-09-15 23:32:57 -0400
categories: jekyll update
permalink: "/cad/MorphingSurfaces/"
---

<div class="w3-row ">
    <h1 style="text-align:center">Morphing Parametrized Surfaces</h1>
    <p class = "justify">
    The purpose of this work was to reinforce my knowledge in parametrized surfaces. Since I have learned a couple of theoretical concepts, it was an opportunity for me to verify if I understood things correctly. The first concept I wanted to test was the Mobius strip. Take rectanle and glue two of its opposite sides, what you obtain is a hollow cylinder. Now if you take the same rectangle but apply a twist to one side before you glue it to its opposite side, you get a Mobius strip; a one-sided surface. 
    </p> 
    <div class="w3-main w3-center" >
        <img src="/portfolio/assets/img/Mobius.gif" width="50%" height="50%">
        <figcaption>Example of Mobius strip</figcaption>
    </div>
    <p class = "justify">
    In the event where two mobius strips are glued together on their side, the resulting shape is what is called a Klein bottle. Both the paramteric equations for the Klein bottle and the Mobius strip were found on Wikipedia. The Klein bottle and the morphing of the mobius strip into the Klein bottle can be shown below. Keep in mind that this morphing technic does not show how two mobius strip are glued to give the Klein bottle but just a common parametric morphing. 
    </p>
        <div class="w3-main w3-center" >
        <img src="/portfolio/assets/img/Klein.PNG" width="60%" height="60%">
        <figcaption>Klein bottle</figcaption>
        <div class="w3-main w3-center" >
        <img src="/portfolio/assets/img/MobiusToKlein.gif" width="60%" height="60%">
        <figcaption>Mobius strip morphed into a Klein bottle</figcaption>
    </div> 
    <p class = "justify">
    For my research, I happen to use Bezier curves and surfaces a lot. Bezier curves are drawn using control points. The resulting curve starts at the first control and finishes at the second control points but does not pass by the intermediary control points. 
    </p>
    <div class="w3-main w3-center" >
        <img src="/portfolio/assets/img/Bez1.PNG" width="30%" height="30%">
        <img src="/portfolio/assets/img/Bez2.PNG" width="30%" height="30%">
        <figcaption>Bezier Curves in blue for control points in red</figcaption>
    </div>  
    <p class = "justify">
    When the points represent experimental data, Bezier curves and surfaces are a great way of averaging out the results. 
    </p>
    <div class="w3-main w3-center" >
        <img src="/portfolio/assets/img/BezierEvol.gif" width="70%" height="70%">
        <figcaption>Smoothing of experimental data surface</figcaption>
    </div> 
</div>

