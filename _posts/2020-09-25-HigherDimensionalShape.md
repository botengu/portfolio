---
layout: post
title:  Bezier Objects in Higher Dimensions   
categories: jekyll update
permalink: "/cad/nDBezier/"
---

<div class="w3-row ">
    <h1 style="text-align:center">Bézier objects in higher dimensions</h1>
    <p class = "justify">
    This particular topic will discuss reusing Bézier surfaces. Those who have seen my previous posts will indeed find that I am a huge fan of Bezier objects (curve, surface, and volumes). I think they are great ways of obtaining normalized, smooth, parametric objects. <br>
    Although many posts have used Bézier concepts, I will describe them in more detail here. 
    Bézier curves are curves that are controlled by a set of control points.
    A linear Bézier curve  \(C(u)\) is the curve obtained by two points \(P_{0}\) and \(P_{1}\) such that:
    $$C(u) = P_{0} + u \cdot (P_{1} - P_{0}) $$
    $$C(u) = (1-u)\cdot P_{0}+ u \cdot P_{1} $$
    for 0 \(\leq\) u \(\leq\)  1. 
    </p>
    <p class = "justify">
    Higher-order Bézier curves ( which require more than two points) follow the same pattern. Overall, the  nth degree Bézier curve can be obtained by the following function: 
    $$ C(u) = \sum ^{n}_{i=0} B^{n}_{i}(u) \cdot P_{i} $$
    where  \(P_{i}\) is the ith control point and n is the number of points and \(B^{n}_{i}(u)\) is the Bernstein polynomial in the u direction:
    $$ B^{n}_{i}(u)=  \binom{n}{i} (1-u)^{n-i}\cdot u^i  $$
    <br>
    Let me state something obvious, for Bézier curves to be curves and not just lines; the control points need to be non-colinear. In other words, for a Bézier curve, which is a uni-dimensional Bézier object (it has only one parameter u), the control points should belong to (at least) a two-dimensional space. This statement will be useful for future Bézier objects in higher dimensions.  The pictures below show two Bézier curves cases, one where the control points are restricted to a uni-dimensional domain and the other where the control points are non-colinear. 
    </p> 
    <div class="w3-main w3-center" >
        <img src="/portfolio/assets/img/Bzcurveflat.png" width="50%" height="50%">
        <figcaption> Bézier curve with colinear control points  </figcaption>
    </div>
    <div class="w3-main w3-center" >
        <img src="/portfolio/assets/img/Bzcurve.png" width="50%" height="50%">
        <figcaption> Bézier curve with non-colinear control points  </figcaption>
    </div>
     <p class = "justify">
    Bézier surfaces use the same rules as the Bézier curves, but in two different dimensions simultaneously, the surface obeys the following equation: 
    $$ S(u,v) = \sum ^{n}_{i=0} \sum ^{m}_{j=0} B^{n}_{i}(u) \cdot B^{m}_{j}(v)  \cdot P_{i,j} $$
    where P is the matrix of points and \(P_{i,j}\) is the point at location i and j in the matrix and n, and m are the numbers of points both directions. \(B^{n}_{i}(u)\) was explained earlier and \(B^{m}_{j}(v)\) are the Bernstein polynomials applied in the v direction:
    $$ B^{m}_{j}(v) =  \binom{m}{j} (1-v)^{m-j}\cdot v^j $$
    In this particular case, for a Bézier surface to be non-planar, the control points have to be non-planar.  
    The pictures below show two Bézier surface cases, one where the control points are restricted to a two-dimensional domain and the other where the control points are non-planar. 
    </p> 
    <div class="w3-main w3-center" >
        <img src="/portfolio/assets/img/Bzsurfflat.png" width="50%" height="50%">
        <figcaption> Bézier surface with coplanar control points </figcaption>
    </div>
    <div class="w3-main w3-center" >
        <img src="/portfolio/assets/img/Bzsurf1.png" width="50%" height="50%">
        <img src="/portfolio/assets/img/Bzsurf1_2.PNG" width="40%" height="40%">
        <figcaption> Bézier surface with non-coplanar control points</figcaption>
    </div>
     <p class = "justify">
    In the project <a class = "ex1 ex3" href="/portfolio/cad/MorphingSurfaces/" target="_blank"> "Morphing parametrized surfaces" </a>, I have shown the transition between a surface passing through points and the resulting Bézier surface when the original points are used as control points. 
    </p>
    <p class = "justify">
    Bézier volumes use the same rules as the Bézier surfaces, but in three different dimensions simultaneously, the volume obeys the following equation: 
    $$ V(u,v,w) = \sum ^{n}_{i=0} \sum ^{m}_{j=0} \sum ^{l}_{k=0} B^{n}_{i}(u) \cdot B^{m}_{j}(v) \cdot B^{l}_{k}(w)\cdot P_{i,j,k} $$
    where P is the matrix of points and \(P_{i,j,k}\) is the point at location i and j in the matrix and n, and m are the numbers of points both directions. \(B^{n}_{i}(u)\) and \(B^{m}_{j}(v)\) were explained earlier. \(B^{l}_{k}(w)\)  is the Bernstein polynomial applied in the w direction:
    $$ B^{l}_{k}(w) =  \binom{l}{k} (1-w)^{l-k}\cdot w^k  $$
    Now, this is where the obvious becomes interesting: the same way a uni-dimensional Bézier object (a curve) needs at least two-dimensional control points to be curved, three-dimensional Bézier objects (volume) need at least four-dimensional control points to avoid being regular cubes and the values for the fourth coordinate cannot all be zero.
    The problem here lies in the fact that the human eye cannot visualize four-dimensional elements. <br>
    This is where projection is important. For this project to be completed, the four-dimensional points must be projected into a three-dimensional world. In 3D, the shadow of any object is the 2D projection of that object. To be able to see Bézier solids, we need to take the 3D shadow of a 4D object.
    </p> 
    <p class = "justify">
          The pictures below show the shadow two Bézier solids. For the first set of images, the control points of the bezier solids are "flat" in 4D (the value of the fourth coordinate is 0 for all points), and for the second set of images, the control points can have non-zero fourth coordinate. 
    </p>
    <div class="w3-main w3-center" >
        <img src="/portfolio/assets/img/Bzvolumeflat.png" width="40%" height="40%">
        <img src="/portfolio/assets/img/Bzvolumeflat2.png" width="40%" height="40%">
        <img src="/portfolio/assets/img/Bzvolumeflat3.png" width="40%" height="40%">
        <figcaption> The images above show a Bézier solid projected (a) and rotated around the xz axis and zw axis (b and c) - control points are in red </figcaption>
    </div>     
    <p class = "justify">
    It should be made clear that the previous images do not show a tesseract, it shows a cube (8 vertices, 6 faces) created and rotated in the fourth dimension and projected to a three-dimensional space. The same way the flat surface \(S(u,v)\) was a rectangle in three dimensional space. Adding non-zero third coordinates allowed us to add waves to the flat surfaces, those waves can only be fully seen if the observer can see in 3D. The following set of images show a non flat cube with 4D coordinates which can only be fully seen in 4D. To give the observer a sense of the "waves", the solid was rotated in 4D and projected back to 3D mutliple times.  
    </p> 
    <div class="w3-main w3-center" >
        <img src="/portfolio/assets/img/Bzvolume.png" width="40%" height="40%">
        <img src="/portfolio/assets/img/Bzvolume2.png" width="40%" height="40%">
        <img src="/portfolio/assets/img/Bzvolume3.png" width="40%" height="40%">
        <img src="/portfolio/assets/img/Bzvolume4.png" width="40%" height="40%">
        <figcaption> Bézier solid made with 4D points projected to 3D (a and b) and rotated around the zw axis (c and d) - control points are in red </figcaption>
    </div> 

</div>



