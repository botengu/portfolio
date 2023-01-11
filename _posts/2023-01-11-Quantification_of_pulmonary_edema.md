---
layout: post
title:  Quantifying Pulmonary Edema
permalink: "/cad/QuantPulmEde/"
---

  <div class="w3-row">
      <h1 style="text-align:center">Quantifying pulmonary edema</h1>
        <p class = "justify">
        Pulmonary Edema is one of the most direct symptoms of congestive heart failure [1]. Although many authors have suggested using neural networks (encoders, CNN) to detect relevant characteristics related to pulmonary edema [2], experience from the medical staff has shown that there are certain visual indicators of the severity of the disease. Relying on those indicators could help enhance the quantification of its severity. Pulmonary edema occurs when external pressure causes pulmonary veins to dilate around the alveoli. Fluid from the veins leaches out and spreads within the alveoli passing first through the interstitial space.
        The chest x-ray of a patient suffering from edema thus displays specific characteristics; the size of the vessels in the upper lungs is similar to those in the lower lung, even though they should be smaller. The blurriness caused by the fluid in the pulmonary area is another characteristic.
        </p>
        <div class="w3-main w3-center">
            <img src="/portfolio/assets/img/Edema_Stages.png" width="80%" height="80%">
            <figcaption>Pictures of the different stages of pulmonary Edema</figcaption>
        </div>
        <p class = "justify">
        The method I propose first uses machine learning to segment and extract the pulmonary zones from the chest x-ray images.
        To do so, I used the lung segmentation code from the repository found here <a class = "ex1 ex3" href="https://github.com/imlab-uiip/lung-segmentation-2d/blob/master/train_model.py" target="_blank" > (repo) </a>. The models were trained using an architecture similar to UNet (which itself uses Convolutional Neural Networks for biomedical images). 
        <br>
        I was able to segment the 4 images of the different stages of Edema:
        </p>
        <div class="w3-main w3-center">
            <img src="/portfolio/assets/img/Lungs_1.jpg" width="40%" height="40%">
            <figcaption>Original images with segmented pictures</figcaption>
        </div>
        <p class = "justify">
        The first step was to only consider the pulmonary area, therefore I superposed the segmented images on top of the original one and I only allowed color variation in the pulmonary area. 
        </p>
        <div class="w3-main w3-center">
            <img src="/portfolio/assets/img/Lungs_2.jpg" width="40%" height="40%">
            <figcaption>Grayscale rendering of pulmonary area</figcaption>
        </div>
        <p class = "justify">
        Once this is done, I have used two relevant pieces of information to quantify the severity of the disease. On one side, there is the area of the segmented lungs, which can be obtained by computing the number of pixels above a certain threshold. On the other side, there is the blurriness of the pulmonary area.  
        <br>
        In this case the blurriness was calculated by analyzing the standard deviation of the values of the pixels. So I thought that plotting the area vs the blurriness.
        </p>
        <div class="w3-main w3-center">
            <img src="/portfolio/assets/img/Lungs_2.png" width="80%" height="80%">
            2D plot of pulmonary area vs pulmonary blurriness for the 4 levels 
            <figcaption></figcaption>
        </div>
        <p class = "justify">
            It was expected that the level2 and level1 would be swapped. But if we look at the oriignal images, it seems that the level2 is less severe than the level1. <br>
            Except for that, the blurriness vs area seems to be a good metric, but more data should be used to confirm that.  
        </p>
<h2 style="text-align:center">References</h2>
<p class = "justify">

<ol>
<li> H. Mahdyoon, R. Klein, W. Eyler, J. B. Lakier, S. Chakko, and M. Gheorghiade, “Radiographic pulmonary congestion in end-stage congestive heart failure,” The American journal of cardiology, vol. 63, no. 9, pp. 625–627, 1989. </li>
<li> A. Koul, R. K. Bawa, and Y. Kumar, “Artificial intelligence techniques to predict the airway disorders illness: A systematic review,” Archives of Computational Methods in Engineering, pp. 1–34, 2022.</li>
</ol>
</p>
</div>




