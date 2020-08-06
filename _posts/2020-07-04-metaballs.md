---
layout: post
title: Primitive Shapes in Implicit Modeling 
permalink: "/cad/metaballs/"
---
  <div class="w3-row ">
      <h1 style="text-align:center">Primitive Shapes in Implicit Modeling </h1>
        <p class = "justify">
        An Implicit Model is a continuous mathematical representation of an attribute across a volume.  It has an infinitely fine resolution. Creating tangible surfaces from this model is a separate and secondary step and is independent of the creation of the Implicit Model (from www.micromine.com).
        Metaballs use implicit modeling to represent objects.  Their main particularity is that they describe a field. Hence, object fields can be added together to create smooth transitions between the two objects. To obtain the field of an object, we need to take the inverse of the function describing that object. For a sphere the object is described by the equality: 
        $$ {x^2+y^2+z^2} = r^2 $$
        where r is the sphere's radius. When considering the field of a sphere located at the point (a,b,c), the function becomes will be:
        $$f = {r^2  \over {(x-a)^2+(y-b)^2+(z-c)^2}  }$$
        When superimposing spherical objects, one gets a greater sphere. While when adding two spherical fields, we can get a transition between two spheres.  The pictures below show the superimposition of different type fields (the marching cube algorithm is still used to represent the fields).  
        </p>
        <br>
        <div class="w3-main w3-center" >
            <img src="/portfolio/assets/img/merged-spheres.PNG" width="50%" height="50%">
            <figcaption>Isosurface of superimposed spherical fields</figcaption>
        </div>
        <br>
        <div class="w3-main w3-center" >
            <img src="/portfolio/assets/img/merged-cubes.PNG" width="50%" height="50%" >
            <figcaption>Isosurface of superimposed diamond fields</figcaption>
        </div>
        <br>
        <div class="w3-main w3-center" >
            <img src="/portfolio/assets/img/Cylinders.PNG" width="50%" height="50%">
            <figcaption>Isosurface of superimposed cylindrical fields</figcaption>
        </div>
        <p class = "justify">
        Spherical fields can be further used in order thicken non straight curves like Bezier curve with more than one control point. 
        </p>
        <div class="w3-main w3-center" >
            <img src="/portfolio/assets/img/bezierCurve_pts.PNG" width="30%" height="30%">
            <img src="/portfolio/assets/img/bezierCurve.PNG" width="30%" height="30%">
            <img src="/portfolio/assets/img/Thickened_bezierCurve.PNG" width="30%" height="30%">
            <figcaption>Isosurface of superimposed spherical fields along a spline</figcaption>
        </div>
        <p class = "justify">
        Below I will show an interesting example of how implicit modeling can be used for a greater purpose
        I was asked to create a star-looking shape where members had to be non-coplanar.
        To properly blend the members of the star, I thought it would be a good idea to use implicit modeling.
        After randomizing the length and the orientation of the members, and after increasing the size of the center, I ended up with this virus-looking shape.
        As someone who had long searched for ways to apply my CAD knowledge to the biomedical field, I couldn't have asked for better...
        It's also mesmerizing to see how implicit modeling yields shapes that are more probable to be found in nature.  
        </p>
        <div class="w3-main w3-center" >
            <img src="/portfolio/assets/img/Virus_square.PNG" width="70%" height="70%">
            <img src="/portfolio/assets/img/Inside_vir.PNG" width="70%" height="70%">
            <figcaption>Virus like shape obtained through the superimposition of primitive shapes' fields. The second figure shows the inside of the virus like shape.</figcaption>
        </div>
</div>

