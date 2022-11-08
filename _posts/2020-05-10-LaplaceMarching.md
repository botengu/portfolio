---
layout: post
title:  Laplacian Smoothing and Marching Cubes 
permalink: "/cad/smoothing/"
---

  <div class="w3-row">
      <h1 style="text-align:center">Laplacian smoothing and marching cubes to smooth coarse meshes</h1>
        <p class = "justify">

            Laplacian smoothing is an algorithm that:  
        </p>
        <div class="w3-main w3-center">
            <img src="/portfolio/assets/img/Gyroid-Single-layer.PNG" width="40%" height="40%">
            "Pictures of laplacian and throught iterations" 
            <figcaption>Gyroid, Schwarz-D and Schwarz-P structures</figcaption>
        </div>
        <p class = "justify">
        Marching cubes on the other side: 

        I had referred to marching cubes in a different project: "Link here" 
        </p>
        <div class="w3-main w3-center">
            <img src="/portfolio/assets/img/TPMSrendered2_new.png" width="100%" height="100%">
            "Pictures of marching squares" 
            <figcaption>Rendered TPMS structure for squared gyroid constrained inside simple primitives</figcaption>
        </div>
        <p class = "justify">
        The idea was to treat the values we get for each gridpoints similar to we did the coordinates of the vertices in the mesh on which we applied laplacian smoothing. 

        There are three  parameters that we consider: the number of laplacian iterations, the density of the grid, the number at which we take our contours. 
         </p>
        <div class="w3-main w3-center">
            <img src="/portfolio/assets/img/TPMSrendered2_new.png" width="100%" height="100%">
            "change from n = 20 to n= 40 " 
            <figcaption></figcaption>
        </div>
                <div class="w3-main w3-center">
            <img src="/portfolio/assets/img/TPMSrendered2_new.png" width="100%" height="100%">
            "change from n = 20 to n= 40 " 
            <figcaption></figcaption>
        </div>
                <div class="w3-main w3-center">
            <img src="/portfolio/assets/img/TPMSrendered2_new.png" width="100%" height="100%">
            "change from n = 20 to n= 40 " 
            <figcaption></figcaption>
        </div>
        <p class = "justify">

        The work here can be used in the future to smooth topologically optimized structures. 
        
        Future work: to prevent the shrinking, write the contour number as a function of the number of iterations. 

         </p>


       
    

  </div>




