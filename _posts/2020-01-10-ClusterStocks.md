---
layout: post
title:  Machine Learning for Stocks Analysis 
date:   2020-07-10 23:32:57 -0400
categories: jekyll update
permalink: "/finance/clusterStocks/"
---

<div class="w3-row ">
    <h1 style="text-align:center">K-Means clustering to identify stocks with similar trends</h1>
    <p class = "justify">
    Since the market crashed, we have witnessed a chaotic change in stock prices. The interesting thing is that, by having a glance at a few stocks, it is easy to see that a certain companies have gone through similar patterns after the market crash. I will refer to the evolution of the stock price over a certain amount of time as the stock price trend or SPT. 
    </p> 
    <div class="w3-main w3-center" >
        <img src="/portfolio/assets/img/MSFT_price.PNG" width="50%" height="50%">
        <figcaption>Evolution of Microsoft Stock Price over a given time period</figcaption>
    </div>
    <p class = "justify">
    The stock prices were given day by day, weekends are not counted. 
    The similarity in trends can be explained by different things, some stocks have had similar trends because they are related to the same industry but sometimes they can be explained by other reasons. Nonetheless, I was looking for a way to see how machine learning could be applied to finance. Most people, when they hear about artificial intelligence in finance, directly think of how it can be used to predict stock prices. I personally believe that it is a completely flawed approach, although it might be accurate sometimes, no AI or Machine learning model can perfectly encapsulate all the different factors that go into affecting the price of a stock. If people still have doubts about this fact the Covid-19 crisis which took place in early 2020 is a great example.</p>
    <p class = "justify">Hence, I thought of a different approach to use AI in stocks; unsupervised machine learning to group securities with similar SPTs. Clustering can be done using K-means clustering which partitions the data into k clusters that minimize the within-cluster sum of squares. K-clustering can easily be used to group points based on their proximity. 
    The main conceptual challenge of such a project: how to represent the points. More specifically, how do we go from a trend to a point in n-dimension? </p>
        <div class="w3-main w3-center" >
        <img src="/portfolio/assets/img/PCAex.PNG" width="60%" height="60%">
        <figcaption>Illustration of PCA. The features are converted into a smaller number of new features.</figcaption>
    </div> 
    <p class = "justify">
    The feasibility of the program relies on one simple concept, the stock price for each day can be seen as the value for a particular point or stock in a specific dimension. Hence, a SPT over 20 days can be seen as a point with 20 coordinates in a 20-dimensional space. Clustering can happen in hyperspace however, for the sake of visualization, I had to reduce dimensionality. However, I could not simply take 3 features out of the 20 coordinates of every point. Considering only 3 features amongst the 20 features would only be like considering 3 days instead of the 20. Therefore, a more elaborate approach has to be taken. I needed to transform a 20-dimensional features vector into a 3-dimensional features vector while retaining as most information as possible. PCA (principal component analysis) is the exact way to go about it. PCA is applied and we obtained the coordinates of stocks in 3-dimensional space.  Interestingly enough, clustering the stocks before and after PCA gives the exact same clusters (for an original dimensional space of about 20 days). 
    </p>
    <div class="w3-main w3-center" >
        <img src="/portfolio/assets/img/Stocksgif.gif" width="70%" height="70%">
        <figcaption>On top, the clusters in the different stocks are shown, on the bottom, PCA was applied to represent stocks as points in 3D. Each color refers to a different cluster.</figcaption>
    </div>  
    <p class = "justify">
    One important detail is the fact that because I am comparing trends and not just exact numbers, I had to normalize the coordinates for all points (stocks). 
    Such a method can have a  lot of benefits in many domains. For example, exchange-traded funds are made of similar stocks, one great way of generating additional ETFs would be by grouping stocks with similar performance (Although I am aware that for some, the advantage of an ETF is to have diversified securities and reduce the risks).
    </p>
</div>

