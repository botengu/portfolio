---
layout: post
title:  Fourier Series for Shape Parametrization   
categories: jekyll update
permalink: "/cad/FourierParam/"
---

<div class="w3-row ">
    <h1 style="text-align:center">Fourier series for compact shape parametrization</h1>
    <p class = "justify">
    I discovered Fourier series like most of my peers in PDEs (partial differential equations). In ODEs (ordinary differential equations) one of myprof mentionned that this could be used to redraw figures. I thought it was interesting but it is only recently, thanks to the video.... 
    that I decided to take another look. <br>
    To summarize, Fourier mentionned that any curve can be approximated using a sum of cosines and sines. but any curve can be wrapped around a circle when considering the imaginary and real axis. Therefore, any closed curve can be approximated using the Euler's equation: \(e^{\theta i} = cos( \theta ) + i \cdot sin(\theta) \).  
    The fast fourier transform method can be used to extract move from a time domain to a frequecy domain. The inverse fast fourier transform  takes a frequency vs amplitude plot and gives a time vs amplitude plot (or the curves).  For closed curves, there are two plots and complex one and a real one (one with a complex amplitude and the other one with a real amplitude). 
    <br>Below is an example of a shape and its frequency plots.
    </p> 
        <div class="w3-main w3-center" >
        <img src="/portfolio/assets/img/Fmodel1.png" width="100%" height="100%">
        <figcaption>Parameterized 2D diamond and resulting frequency plot (real amplitudes are in orange and complex amplitudes are in blue)</figcaption>
    </div> 
    <p class = "justify">
    To fully reconstruct the shape, all the frequencies need to be added (multiplied by a constraint) as they all more or less contribute to the shape. The figure below shows how frequencies can be added one by one to get to a final shape. 
    </p> 
    <div class="w3-main w3-center" >
        <img src="/portfolio/assets/img/Fmodel3.gif" width="50%" height="50%">
        <figcaption>Cumulative contributions of the multiple frequencies to the final shape</figcaption>
    </div> 
    <p class = "justify">
    As I am extremely interested in geometric modeling, a natural question came to mind, can model shapes only using frequencies (sines and cosines), and how would the properties of the shape vary based on those frequencies, can we visually predict a shape's propeties based on the frequencies? Do two similar shapes have similar frequency plots and do two similar frequency plots result in similar shapes? 
    <br>
    A lot of thoses shapes are not necessarily viable shapes, hence it is important to know what set of frequencies will give non-intersecting shapes. The opposite approach was thus taken. Instead of creating shapes from random frequencies, I took the frequency plot of an existing shape (the one above) and modified it. More precisely, each complex and real frequency of the frequency graph was multplied by a different random value. So I ended up with 2 frequency plots, one refering to the original shape and the other one referring to the radomly modified shape.
    </p> 
    <div class="w3-main w3-center" >
        <img src="/portfolio/assets/img/Fmodel2.PNG" width="100%" height="100%">
        <figcaption>New shape obtained based on randomized frequency plot</figcaption>
    </div> 
    <p class = "justify">
     I created a set of interpolated plots between the two frequency plots. Then, for each of the interpolated frequency plot, I have computed the inverse fast fourier transform to visualize the resulting shapes.
    </p> 
    <div class="w3-main w3-center" >
        <img src="/portfolio/assets/img/Fmodel4.gif" width="100%" height="100%">
        <figcaption>Interpolated plots between original frequency plots and randomized plots (left) with correspoding shapes (right)</figcaption>
    </div> 
    <p class = "justify">
        More research should be done to investigate whether all shapes can be parametrized this way.  
    </p> 
</div>




