---
layout: post
title:  Porous Structures and Topology Optimization 
date:   2020-09-04 23:32:57 -0400
categories: jekyll update
permalink: "/cad/topopt/"
---

<div class="w3-row">
    <h1 style="text-align:center">Porous structures based on topology optimization results</h1>
    <p class = "justify">
    Structural topology optimization is a process in which topologies, sizes, and layouts of structures are altered through the maximization, minimizing an objective function while applying specific constraints. The results of such a process are sometimes hard to manufacture; therefore, the results can be used to vary the density of objects. The advancements in additive manufacturing have allowed for such intricate shapes to be printed.
    </p> 
    <div class="w3-main w3-center" >
        <img src="/portfolio/assets/img/Additional_plate.PNG" width="70%" height="70%">
        <figcaption> Left- Topology optimization results. Right- Resulting porous structure.</figcaption>
    </div>
    <p class = "justify">
    To create such a structure, the topology optimization results were first interpolated. I implemented a python function to control the size of the circles based on the field's value at their centers. The shapes were imported in Grasshopper3D to extrude the final surface. The topology optimization results were obtained using an adaptation of the famous code from Andreassen[1] into python. 
    </p> 
</div>
<footer>
    [1] Erik Andreassen, Anders Clausen, Mattias Schevenels, Boyan S Lazarov, and Ole
    Sigmund. Efficient topology optimization in matlab using 88 lines of code. Structural
    and Multidisciplinary Optimization, 43(1):1–16, 2011.
</footer>

