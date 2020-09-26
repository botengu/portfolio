---
layout: post
title:  Bezier Objects in Higher Dimensions   
categories: jekyll update
permalink: "/cad/nDBezier/"
---

<div class="w3-row ">
    <h1 style="text-align:center">Bézier objects in higher dimensions</h1>
    <p class = "justify">
    This particular topic will discuss reuse Bezier surface. Those who have seen my previous posts will indeed find that I am huge fan of Bezier objects (curve, surface and volumes). I think they are great ways of obtaining normalized, smooth, parametric objects. <br>
    Although many posts have used Bézier concepts, I will describe them in more details here. 
    Bézier curves are curves that are controlled by a set of control points.
    A linear Bézier curve c(t) is the curve obtained by two points \(P_{0}\) and \(P_{1}\) such that:
    $$c(t) = P_{0} + t \cdot (P_{1} - P_{0}) $$
    $$c(t) = (1-t)\cdot P_{0}+ t \cdot P_{1} $$
    for 0 \(\leq\) t \(\leq\)  1. 
    </p>
    <div class="w3-main w3-center" >
        <img src="/portfolio/assets/img/" width="50%" height="50%">
        <figcaption> caption </figcaption>
    </div>
    <p class = "justify">
    Quadratic Bézier curves are interpolations of two linear interpolations (the one between the first and second point and the one between the second and third point). Higher order Bézier curves ( which require more than two points) follow the same pattern. Overall, the  nth degree Bézier curve can be obtained by the following function: 
    $$ c(t) = \sum ^{n}_{i=0} \binom{n}{1} (1-t)^{n-i}\cdot t^i \cdot P_{i} $$
    $$ c(t) = \sum ^{n}_{i=0} B^{n}_{i} \cdot P_{i} $$
    where  \(P_{i}\) is the ith control point, n is the number of points and \(B^{n}_{i}\) is the Bernstein polynomial.
    <br>
    Let me state something obvious, for Bézier curves to be curves and not just lines, the control points need to be non-colinear. In other words for a Bézier curve which is a uni-dimensional Bézier object (it has only one parameter t), the control points should belong to (at least) a two-dimensional space. This statement will be useful for future Bézier objects in higher dimensions.  The pictures below show two Bézier curves cases, one where the control points are restricted to a uni-dimensional domain and the other where the control points are non-colinear. 
    </p> 
    <div class="w3-main w3-center" >
        <img src="/portfolio/assets/img/" width="50%" height="50%">
        <figcaption> Bézier curve with colinear control points  </figcaption>
    </div>
    <div class="w3-main w3-center" >
        <img src="/portfolio/assets/img/" width="50%" height="50%">
        <figcaption> Bézier curve with non-colinear control points  </figcaption>
    </div>
     <p class = "justify">
    Bézier surfaces use the same rules as the Bézier curves but in two different dimensions simultaneously, the surface obeys the following equation: 
    $$ s(u,v) = \sum ^{n}_{i=0} \sum ^{m}_{j=0} B^{n}_{i} \cdot B^{m}_{j}  \cdot P_{i,j} $$
    where P is the matrix of points and \(P_{i,j}\) is the point at location i and j in the matrix and n, and m are the numbers of points both directions. \(B^{n}_{i}\) and \(B^{m}_{j}\) are the Bernstein polynomials applied in both directions. 
    In this particular case, for a Bézier surface to be non-planar, the control points have to be non-planar.  
    The pictures below show two Bézier surface cases, one where the control points are restricted to a two-dimensional domain and the other where the control points are non-planar. 
    </p> 
    <div class="w3-main w3-center" >
        <img src="/portfolio/assets/img/" width="50%" height="50%">
        <figcaption> Bézier surface with coplanar control points </figcaption>
    </div>
    <div class="w3-main w3-center" >
        <img src="/portfolio/assets/img/" width="50%" height="50%">
        <figcaption> Bézier surface with non-coplanar control points</figcaption>
    </div>
     <p class = "justify">
    Bézier volumes use the same rules as the Bézier surfaces but in three different dimensions simultaneously, the volume obeys the following equation: 
    $$ V(u,v,w) = \sum ^{n}_{i=0} \sum ^{m}_{j=0} \sum ^{o}_{k=0} B^{n}_{i} \cdot B^{m}_{j} \cdot B^{o}_{k} \cdot P_{i,j,k} $$
    where P is the matrix of points and \(P_{i,j,k}\) is the point at location i and j in the matrix and n, and m are the numbers of points both directions. \(B^{n}_{i}\), \(B^{m}_{j}\) and \(B^{o}_{k}\)  are the Bernstein polynomials applied in all three directions. 
    Now this is where the obvious becomes interesing: the same way a uni-dimensional Bézier object (a curve) needs at least two dimensional control points to e curved, three-dimensional Bézier objects (volume), need at least four-dimensional control points to exist.
    The problem here lies in the fact that four dimensional elements cannot be visualized by the human eye. <br>
    This is where projection is important. For this project to be completed, the four dimensional points have to be projected back to a three dimensional world. In 3D, the shadow of any object is the 2D projection of that object. For us to be able to see Bézier solids, we need take the 3D shadow of a 4D object. The figures below show a hypercube (4D cube) projected to 3D and rotated at different angles. 
    </p> 
    <div class="w3-main w3-center" >
        <img src="/portfolio/assets/img/" width="50%" height="50%">
        <figcaption> Bézier surface with coplanar control points </figcaption>
    </div>
    <div class="w3-main w3-center" >
        <img src="/portfolio/assets/img/" width="50%" height="50%">
        <figcaption> Bézier surface with non-coplanar control points</figcaption>
    </div>
    <p class = "justify">
    The pictures below show two Bézier solid cases, one where the control points are restricted to a 3D domain and the other where the control points belong can exist in a 4D domain. 
    </p>
</div>



