---
layout: post
title:  Smoothing score
permalink: "/cad/Impl_Laplace/"
---

  <div class="w3-row">
      <h1 style="text-align:center">Smoothing score</h1>
        <p class = "justify">
        For this exercise, the purpose was to develop an algorithm to smooth a 3D model.
        </p>
        <div class="w3-main w3-center">
            <img src="/portfolio/assets/img/Smooth_1.png" width="50%" height="50%">
        </div>
        <p class = "justify">
        I will go through all the steps.  
        <br>
        Step 1: Rough part is imported and decimated.
        </p>
        <div class="w3-main w3-center">
            <img src="/portfolio/assets/img/smooth_2.png" width="50%" height="50%">
        </div>
        <p class = "justify">
        A bounding box is created around the part and it is filled with a point grid. The points outside the part are given a value of 0. While the points inside the part are given a value of 1. The 3D contour is taken using the marching cube algorithm with threshold 0.5. 
        </p>
        <div class="w3-main w3-center">
            <img src="/portfolio/assets/img/smooth_3.png" width="30%" height="30%">
        </div>
        <p class = "justify">
        This is the contour of a 3d array of values. Now we can apply iteration of Laplacian smoothing, to find smoothen the part by fixing the values at the boundaries of the 3D grid of points. <br>
        Here is a link to more info about <a class = "ex1 ex3" href="https://en.wikipedia.org/wiki/Laplacian_smoothing" target="_blank">Laplacian smoothing </a>, I have used this algorithm a lot in my research internship in 2015. <br>
        The problem with using Laplacian smoothing, especially when we restrict the boundaries is that it causes shrinking, when there is a lot of iterations. To prevent that we multiply the marching cube threshold by  a factor that is a function of the amount of  smoothing iterations. 
        </p>
        <div class="w3-main w3-center">
            <img src="/portfolio/assets/img/smooth_4.png" width="40%" height="40%">
        </div>
        <p class = "justify">
        The result is also a mesh, but a smoother one. We can juxtapose the original mesh and the transformed one. 
        </p>
        <div class="w3-main w3-center">
            <img src="/portfolio/assets/img/smooth_5.png" width="40%" height="40%">
        </div>
        <p class = "justify"> 
        Now comes the time to adequately quantify the smoothness between the initial and final part.<br>
        To do so, for every single triangle t we take its normal, and we measure the angle it does with the normal of all the adjacent triangles. We take the average of those angles and the color of the triangle t is dictated  by  that average.    
        </p>
        <div class="w3-main w3-center">
            <img src="/portfolio/assets/img/smooth_6.png" width="40%" height="40%">
        </div>
        <p class = "justify"> 
        A histogram can be build in order to highlight the distribution of those averages. 
        The first picture is the histogram for the initial model and the second picture shows the histogram for the final model. 
        </p>
        <div class="w3-main w3-center">
            <img src="/portfolio/assets/img/smooth_7.png" width="40%" height="40%">
            <img src="/portfolio/assets/img/smooth_8.png" width="40%" height="40%">
        </div>
</div>




