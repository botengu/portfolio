---
layout: post
title:  Parts from Stress Lines  
date:   2020-09-19 00:30:57 -0400
categories: jekyll update
permalink: "/cad/StressLines/"
---

<div class="w3-row ">
    <h1 style="text-align:center">Creating Parts from Stress Lines</h1>
    <p class = "justify">
    Aside from topology optimization which has been addressed in a different post <a class = "ex1 ex3" href="/cad/topopt/" target="_blank" > (here) </a>, parts can also be created using stress lines. To derive stress lines, a 2D FEA code was used <a class = "ex1 ex3" href=" https://github.com/largurajr/FEA-Protus" target="_blank" > (link here) </a>. I chose a design space and imposed boundary conditions as well as loads.  
    </p> 
    <div class="w3-main w3-center" >
        <img src="/portfolio/assets/img/designspace.PNG" width="50%" height="50%">
        <figcaption>Design space with boundary conditions and loads</figcaption>
    </div>
    <p class = "justify">
    Once everything had been defined, the design space was discretized and the FEA code was run. The code gave the Von Mises stresses values at all the different nodes. Those nodal values were used to interpolated the stress values over the entire domain.  
    </p> 
    <div class="w3-main w3-center" >
        <img src="/portfolio/assets/img/StressLines3.png" width="50%" height="50%">
        <figcaption>Colormap of the interpolated normalized Von Mises Stresses</figcaption>
    </div>
    <p class = "justify">
    I was also able to obtain the principal stresses from the code and I have plotted the resulting stress field. 
    </p> 
    <div class="w3-main w3-center" >
        <img src="/portfolio/assets/img/StressLines1.png" width="50%" height="50%">
        <figcaption>Stress field</figcaption>
    </div>
    <p class = "justify">
    The stress field was interpolated accross the whole domain. The advantage of having a stress field is that I can start from a random point, draw a segment in the direction given by the stress field at that starting point, this will lead me to another point, where I'll do the same thing (over a fixed number of iterations). I used some of the boundary points as starting points. The resulting lines were then smoothed using Bezier Curves. 
    </p> 
    <div class="w3-main w3-center" >
        <img src="/portfolio/assets/img/StressLines2.png" width="50%" height="50%">
        <figcaption>Stress lines</figcaption>
    </div>
    <p class = "justify">
    The resulting lines have then be thickened, extruded and rendered using Rhino3D, Grasshopper3D and Blender. 
    </p> 
    <div class="w3-main w3-center" >
        <img src="/portfolio/assets/img/StressLines.png" width="50%" height="50%">
        <figcaption>Thickened stress lines</figcaption>
    </div>
        <div class="w3-main w3-center" >
        <img src="/portfolio/assets/img/StressLinesCAD.png" width="50%" height="50%">
        <figcaption>Rendered part made from stress lines</figcaption>
    </div>
</div>



