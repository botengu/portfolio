---
layout: post
title:  Machine Learning for Stocks Analysis pt2
date:   2020-07-10 23:32:57 -0400
categories: jekyll update
permalink: "/datasc/MovingStocks/"
---

<div class="w3-row">
    <h1 style="text-align:center">Principal component analysis to visualize stocks' evolution</h1>
    <p class = "justify">

    This post is the continuation of a previous post made about machine learning and stocks <a class = "ex1 ex3" href="/portfolio/datasc/ClusterStocks/" target="_blank" > (here) </a>. To understand the concepts that will be discussed, it is necessary to understand those discussed earlier. 
    I want to continue with the idea of representing stock price trends (STPs) using points in a cartesian graph. Last time, the SPT I had discussed were studied over a fixed period. However, it would be interesting to study how those SPTs evolve over a certain amount of time. By increasing the period during which we measure the SPT, we make those points on the cartesian graph to potentially affect the existing clusters. The image below shows how the periods can be taken. 
    </p> 
    <div class="w3-main w3-center" >
        <img src="/portfolio/assets/img/MSFT_periods.PNG" width="50%" height="50%">
        <figcaption>Diagram representing how the periods are taken, original picture taken from google.</figcaption>
    </div>
    <p class = "justify">
    The main justification of taking the periods this way rather than taking consecutive, separate intervals is that we want to measure how the trend is evolving. By continuously applying PCA over n periods, we get n points for one stock. Each one of the points shows the successive location of the SPT as we move forward in time. Below, I created an example rendered in Blender, of how to visualize the SPT of 4 stocks over a period.  When the distance between points decreases as the length of the period increases, the trends of two stock prices resemble each other more and more as we take bigger intervals of time. 
    </p>
    <div class="w3-main w3-center" >
        <img src="/portfolio/assets/img/PCA_stocks_absolute.gif" width="50%" height="50%">
        <figcaption> 3D visualization of the SPTs of Microsoft (Yellow), Tesla (Green), Amazon (Red) and Google (Blue)</figcaption>
    </div>
</div>

