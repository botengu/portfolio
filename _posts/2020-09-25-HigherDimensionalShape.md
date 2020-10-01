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
    Quadratic Bézier curves are interpolations of two linear interpolations (the one between the first and second points and the one between the second and third points). Higher-order Bézier curves ( which require more than two points) follow the same pattern. Overall, the  nth degree Bézier curve can be obtained by the following function: 
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
    Now, this is where the obvious becomes interesting: the same way a uni-dimensional Bézier object (a curve) needs at least two-dimensional control points to e curved, three-dimensional Bézier objects (volume) need at least four-dimensional control points to exist.
    The problem here lies in the fact that the human eye cannot visualize four-dimensional elements. <br>
    This is where projection is important. For this project to be completed, the four-dimensional object must be projected into a three-dimensional world. In 3D, the shadow of any object is the 2D projection of that object. To be able to see Bézier solids, we need to take the 3D shadow of a 4D object. The figures below show a hypercube (4D cube) projected to 3D and rotated at different angles. 
    </p> 
    <div class="w3-main w3-center" >
        <img src="/portfolio/assets/img/BzvolumeProjected.png" width="50%" height="50%">
        <figcaption> Hypercube projected (not rotated) </figcaption>
    </div>
    <div class="w3-main w3-center" >
        <img src="/portfolio/assets/img/" width="40%" height="40%">
        <img src="/portfolio/assets/img/" width="40%" height="40%">
        <figcaption> Hypercube projected and rotated (the pictures will be shown soon)</figcaption>
    </div>
    <p class = "justify">
          The pictures below show the shadow two Bézier solid cases, where the control points are restricted to a 3D domain, and the other where the control points belong can exist in a 4D domain. 
    </p>
        <div class="w3-main w3-center" >
        <img src="/portfolio/assets/img/BzvolumeProjected.png" width="50%" height="50%">
        <figcaption> Bézier solid with 3D control points </figcaption>
    </div>     
    <div class="w3-main w3-center" >
        <img src="/portfolio/assets/img/" width="50%" height="50%">
        <figcaption>Bézier solid with 4D control points projected and rotated (the pictures will be shown soon)</figcaption>
    </div>
    
</div>



