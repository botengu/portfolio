---
layout: post
title:  Medical Imaging
permalink: "/cad/MedImag/"
---

  <div class="w3-row">
      <h1 style="text-align:center">Computer vision for medical purposes</h1>
        <p class = "justify">
        Three avenues have helped guide my work while working for Sonoscope.<br> 
        The first one was analytics performed on segmented thoraxes: 
        <ul>
        <li>Since the purpose of our start-up was to use segmented ct scan to infer certain information about where to place the probe to have the best view of the heart, I was tasked with performing certain analytics. </li>
        <li>Below, you can see a transparent view of the segmented thorax. The lungs are in purple, the skin is in cyan, the ribcage in yellow and the left ventricle is in green. The red dots show the intercoastal spaces and the yellow dot is the spot in the intercoastal space that has been chosen. The black dot is the projection of that dot on the skin and the blue vector goes from the black dot to the center of the left ventricle. 
        </li>
        </ul>
        </p>
        <div class="w3-main w3-center">
            <img src="/portfolio/assets/img/sonoscope_1.png" width="30%" height="30%">
            <figcaption>Picture of segmented thorax</figcaption>
        </div>
        <p class = "justify">
        The second one was the classification of morphologies based on custom shape representation:
        <ul>
        <li>The idea here was to used a specific shape representation (that I cannot disclose) in order to be able create a latent space for morphologies.  </li>
        <li>Once the patients morphologies are discretized I am able to reduce the feature dimensionality to 2 using PCA and thus I can represent them on a graph.
        </li>
        </ul>
        <br>
        </p>
        <div class="w3-main w3-center">
            <img src="/portfolio/assets/img/sonoscope_2.png" width="50%" height="50%">
            <figcaption>Latent space for the patients' morphologies</figcaption>
        </div>
        <p class = "justify">
        The third one is the automatic segmentation of of CT SCANS: 
        <br>
        <ul>
        <li>Hiring a firm to segment the ct scans was getting expensive and it using different thresholding technics my role was to find a way to identify the different parts of the thorax. The pictures below shows how far I made it:</li>
        </ul>
        </p>
        <div class="w3-main w3-center">
            <img src="/portfolio/assets/img/sonoscope_3.png" width="30%" height="30%">
            <img src="/portfolio/assets/img/sonoscope_4.png" width="30%" height="30%">
            <img src="/portfolio/assets/img/sonoscope_5.png" width="30%" height="30%">
            <figcaption>Automatic segmentation using thresholding</figcaption>
        </div>

</div>




