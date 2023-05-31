---
layout: post
title:  Parametrizing Feet Scans
permalink: "/cad/Feet_Scan/"
---

  <div class="w3-row">
      <h1 style="text-align:center">Foot orthotic generation</h1>
        <p class = "justify">
        From September 2021 to April 2022,while working at Podform3d, I was tasked with developing a technic that would automatically generate a foot orthotic from the STL of a scanned foot. <br>
        This task reminded me of a problem I had thought about a lot for a while. Turning meshes into parametric surfaces. While turning parametric surfaces into meshes was almost deemed impossible. <br> 
        When a 3d object is saved as a mesh, its surfaces are discretized using triangles. The final output is thus comprised of a list of coordinates for all the points and list of triangles as as a list of trios of indices of points. <br>
        Parametric surfaces are simply surfaces where every point on the surface can be defined as a combination of two parameters usually called u and v. If we normalized u and v (which means lmimiting the parametres to make them go from 0 to 1) the center of a surface is simply the point for which (u,v)=(0.5,0.5). The parametric surface thus has some spatial relations properties that the mesh simply doesn’t. 
        </p>
        <div class="w3-main w3-center">
            <img src="/portfolio/assets/img/podform_1.gif" width="50%" height="50%">
            <img src="/portfolio/assets/img/podform_2.gif" width="50%" height="50%">
        </div>
        <p class = "justify">
        Positive: By having the same parametric system on many surfaces, design that were initially on one surface can be mapped to another surface, this is efficient in surface warping. <br>
        Issues: only specific types of surfaces can be parametrized. <br> 
        Parametrizing the bottom surface of the foot was useful for two endeavors. 
        One it could allow us to generate a surface representing the in-sole that ought to be placed on the bottom of the foot. By giving volume to that part we could then obtain the final orthotic.
        </p>
        <div class="w3-main w3-center">
            <img src="/portfolio/assets/img/podform_3.png" width="40%" height="40%">
            <img src="/portfolio/assets/img/podform_4.png" width="40%" height="40%">
            <img src="/portfolio/assets/img/podform_5.png" width="40%" height="40%">
            <img src="/portfolio/assets/img/podform_6.png" width="40%" height="40%">
            <img src="/portfolio/assets/img/podform_7.png" width="40%" height="40%">
            <img src="/portfolio/assets/img/podform_7_5.png" width="40%" height="40%">
        </div>
        <p class = "justify">
        Second, parametrizing the scan of the foot can also be helpful for creating a new slightly modified model of the foot. For example, some feet were poorly scanned and the reconstructed surface is poorly done and has some holes in it. Parametrizing the foot surface allows me to fill those holes and I can even elongate the foot to generate a mock-up meant to be printed. 
        </p>
        <div class="w3-main w3-center">
            <img src="/portfolio/assets/img/podform_8.png" width="40%" height="40%">
            <img src="/portfolio/assets/img/podform_10.png" width="40%" height="40%">
            <img src="/portfolio/assets/img/podform_11.png" width="40%" height="40%">
            <img src="/portfolio/assets/img/podform_13.png" width="40%" height="40%">
            <img src="/portfolio/assets/img/podform_14.png" width="40%" height="40%">
            <img src="/portfolio/assets/img/podform_15.png" width="40%" height="40%">
        </div>
</div>




