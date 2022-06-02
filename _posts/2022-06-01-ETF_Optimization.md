---
layout: post
title:  Optimization of ETF Securities' Weights  
categories: jekyll update
permalink: "/datasc/ETFOptimization/"
---

<div class="w3-row">
    <h1 style="text-align:center"> Optimization of ETF Securities' Weights</h1>
    <p class = "justify">
    The term ETF stands for Exchange Traded Fund, they usually track the index of a group of diverse securities. All of the different securities are not equally represented, each of them have a different weight. I have always wondered how the weights were calculated. I found  the holdings details of one of the ETF that I possess in my portfolio: ARKK. 
    Amongst the 30+ stocks that it tracked, I selected the 6 most important ones. The purpose of the optimization that I performed was to revisit a time-interval and within that time interval the purpose was to find the right weightst that would have maximized the gain.    
    To do the optimization, I have used the "simulated annealing" technic. Initially the weights could go from 0 to 100% but that made one stock overly represented and the other stocks had really small weights. To overcome this I introduced a limit, to ensure diversity the weights could not be over a certain percentage. They would all start at an equal weight and based on the performance of the stocks during the time period, they would be increased or decreased. The result can be seen below.
    </p> 
    <div class="w3-main w3-center" >
        <img src="/portfolio/assets/img/ETF_STocks.gif" width="50%" height="50%">
        <figcaption>Optimization of stock's weights to optimize an ETF performance during a defined time-interval </figcaption>
    </div>
</div>

