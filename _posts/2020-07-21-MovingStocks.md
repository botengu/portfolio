---
layout: post
title:  Machine Learning for Stocks Analysis pt2
date:   2020-07-10 23:32:57 -0400
categories: jekyll update
permalink: "/datasc/MovingStocks/"
---

<div class="w3-row">
    <h1 style="text-align:center">  </h1>
    <p class = "justify">

    This post is the continuation of a previous post made about machine learning and stocks <a class = "ex1 ex3" href="/portfolio/datasc/ClusterStocks/" target="_blank" > (here) </a>. To understand the concepts that will be discussed, it is necessary to understand those discussed earlier. 
    I want to continue with the idea of representing stock price trends (STPs) using points in a cartesian graph. Last time, the SPT I had discussed were studied over a fixed period. However, it would be interesting to study how those SPTs evolve for different time periods. 
    </p> 
    <div class="w3-main w3-center" >
        <img src="/portfolio/assets/img/MSFT_periods.PNG" width="50%" height="50%">
        <figcaption>Diagram representing how the periods are taken, original picture taken from google.</figcaption>
    </div>
    <p class = "justify">
    To illustrate the use of Stock Price Trend (SPT) point-cloud, I have selected 8 stocks, 4 pharmaceutical ones and 4 related to oil companies. Depending on the time-interval selected I can guess which trends are closer to which other. 
    </p>
    <div class="w3-main w3-center" >
        <img src="/portfolio/assets/img/Financial_stocks.gif" width="50%" height="50%">
        <figcaption> 2D visualization of the SPTs for customly selected intervals (Oil SPTs are in red and Pharmaceutical SPTs are in green)</figcaption>
    </div>

    <p class = "justify">
    Multiple things can be inferred from the graph, first, pharmaceutical SPTs tend to be closer to each other than Oil SPTs; Their trends tend to be less diverse that those of Oil SPTs. Second, for a lot of time intervals, both types of SPTs seem to be at different sections of the canvas, indicating a clear distinction between the two types SPTs. 
    </p>


</div>

