---
layout: page
title: Projects
permalink: "/projects/"
---
<script src='https://kit.fontawesome.com/a076d05399.js' crossorigin='anonymous'></script>


<div class="w3-container w3-center">
  <h1 >Projects</h1>
</div>

<div class="row" >
  <div class="column">
    <div class="w3-card w3-container w3-center border" style="min-height:200px">
    <h3>Geometry</h3>
    <i class="fas fa-draw-polygon w3-margin-bottom w3-text-theme" style="font-size:120px"></i>
    </div >
    <br>
    {% for item in site.posts %}
    {% if item.url contains 'cad'%}
    <a href="{{ item.url | absolute_url }}">
        <div class="w3-card w3-container w3-center ex1 ex3 border2" style="min-height:50px">
        <h5>{{ item.title }}</h5>
        </div>
        </a>
    {% endif %}
    {% endfor %}  
    </div>  
    <div class="column">
    <div class="w3-card w3-container w3-center border" style="min-height:200px">
    <h3>Data Science</h3>
    <i class="fa fa-line-chart w3-margin-bottom w3-text-theme" style="font-size:120px"></i>
    </div>
    <br>
    {% for item in site.posts %}
    {% if item.url contains 'datasc'%}
    <a href="{{ item.url | absolute_url }}"  >
        <div class="w3-card w3-container w3-center ex1 ex3 border2" style="min-height:50px ">
        <h5>{{ item.title }}</h5>
        </div>
        </a>
    {% endif %}
    {% endfor %}  
    </div>  
    <div class="column">
    <div class="w3-card w3-container w3-center border" style="min-height:200px">
    <h3>Music</h3>
    <i class="fa fa-music w3-margin-bottom w3-text-theme " style="font-size:120px"></i>
    </div>
    <br>
    {% for item in site.posts %}
    {% if item.url contains 'music'%}
    <a href="{{ item.url | absolute_url  }}"  >
        <div class="w3-card w3-container w3-center ex1 ex3 border2" style="min-height:50px ">
        <h5>{{ item.title }}</h5>
        </div>
        </a>
    {% endif %}
    {% endfor %}  
    </div>  
</div>




