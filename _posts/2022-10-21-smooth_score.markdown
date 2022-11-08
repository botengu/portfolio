---
layout: post
title:  Smoothing Score
permalink: "/data**/smoothscore/"
---

  <div class="w3-row">
      <h1 style="text-align:center">Smoothing score for meshes</h1>
        <p class = "justify">
        First and foremost in order to better understand this, I invite you to refer to this other page: 
        <br>
        The purpose of this project was to compare how smooth 2 meshes are by giving a smooth index/score. The smooth score/index can be visually obtained by comparing the unsmooth mesh to the smooth one.  
        <br>
        To get the score, I looked at every triangle of the stl meshes and I studied their normal as well as the normals of the triangles adjacent to that triangle. I calculted the angle between the normal of the main face and each normals of the adjacent faces. For each triangle a color was given based on how big that mean is. 
        </p>
        <div class="w3-main w3-center">
            <img src="/portfolio/assets/img/Gyroid-Single-layer.PNG" width="40%" height="40%">
            "Pictures of unsmooth vs smooth with triangles " 
            <figcaption></figcaption>
        </div>
        <p class = "justify">
        The yellow triangles tend to be in the corners where there is a sharp turn and the purple in flat areas. 
        <br>
        The score values can then be plotted as an histogram.
        <div class="w3-main w3-center">
            <img src="/portfolio/assets/img/Gyroid-Single-layer.PNG" width="40%" height="40%">
            "The two histograms " 
            <figcaption></figcaption>
        </div>
        <p class = "justify">
         Now making a final score can be done in many ways: (for each case compare the two)
        - finding the maximum value 
        - finding the average value 
        - finding the standard deviation 
        - Finding the median 
        </p>
        <div class="w3-main w3-center">
            <img src="/portfolio/assets/img/TPMSrendered2_new.png" width="100%" height="100%">
            "Do things with red dot on histograms for the different options" 
            <figcaption>  </figcaption>
        </div>
    

  </div>




