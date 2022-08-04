---
layout: post
title:  Linear Regression for Stocks
permalink: "/datasc/LinRegStock/"
---

  <div class="w3-row ">
      <h1 style="text-align:center">Linear regression and stocks </h1>
        <p class = "justify">
    This is not the first project I have done to help visualize the evolution of the stock price trends. But I realized that the ones I have done using PCA might have been a bit more complex for most audiences. Hence the reason I've decided to come up with a simpler way of comparing stocks. I have chosen two parameters to compare them and they are both based on the linear regression concept. Linear regression is used in statistics and machine learning, it studies how one variable changes based on another, returns the line that best predicts the studied variable, and the amount by which each value of the studied variable differs from that line, the residuals. 
        </p> 
        <div class="w3-main w3-center" >
            <img src="/portfolio/assets/img/Slope_Res_1.png" width="40%" height="40%">
            <figcaption>Linear regression case: the regression line is in blue and the data is in red </figcaption>
        </div>
         <br>
        <p class = "justify">
        For different stocks, I have used regression to track their evolution over a custom time interval (positive vs negative) which I have labeled "price change". Then, I have taken the sum of their residuals. Then, I plotted one with respect to the other. Finally, to help investors and traders make more informed decisions, I have used the color of the markers, as a third variable, to display the average volume of stocks traded for each case. 
        </p> 
        <div class="w3-main w3-center" >
            <img src="/portfolio/assets/img/Slope_Res.png" width="40%" height="40%">
            <figcaption> Visualization of stocks' data between the 4th of August 2021 and the 4th of August 2022 </figcaption>
        </div>
        <br>
        <p class = "justify">
        What is interesting is that this table can be divided in multiple zones to further help the analysis (see image below). The stocks near the top have had the biggest increase for the chosen date. While the stocks at the bottom have had the lowest. The stocks on the left have had a steady change, while the ones on the right have had a messy one. So Ideally, the stocks you would want would be located in the top left corner (green zone). While the stocks you would want to avoid would be in the bottom right corner.
        </p> 
        <div class="w3-main w3-center" >
            <img src="/portfolio/assets/img/Slope_Res_2.png" width="40%" height="40%">
            <figcaption> Important zones </figcaption>
        </div>
</div>


