---
layout: post
title:  Comparing Melodic Phrases
permalink: "/mu$sic/mel_phrases/"
---

  <div class="w3-row">
      <h1 style="text-align:center">Comparing Melodic Phrases</h1>
        <p class = "justify">
        Recently, I made a video about makossa music, a popular genre in Cameroon. The video is in French, and I have included a personal aspect to it, given my upbringing in the Cameroonian diaspora in Montreal. My parents immigrated from Cameroon in the mid-80s and early 90s, during the peak of the "new wave makossa." They didn't follow the subsequent trends that emerged from the country after the decline of makossa. Growing up in the early 2000s, my sister and I have fond memories of listening to old Dina Bell CDs and "Testament du Makossa" by the amazing bass player, Aladji Toure.
        <br>
        </p>
        <iframe width="300" height="160"
        src="https://www.youtube.com/embed/wCJ50xkwLLs">
        </iframe>
        <p class = "justify">
        In the video, I delve into the genre's history and also discuss a recurring melodic phrase that I've noticed in many makossa songs. However, in this post, I'd like to focus more on the process behind creating the musical graph that you can see at the end of the video.
        <br>
        First, I recreated the melodies I investigated using the FL Studio platform. Then, I imported all the individual notes of each melody into the Jupyter Notebook platform using the mido library, which allows for the import and reading of MIDI format files. The notes from FL Studio were converted into a 2D array with three columns and 'n' rows, where 'n' represents the number of notes in the sequence.
        The first column represents the note as a number, the second column indicates the relative start time of the note, and the third column represents the duration of the note. 
        </p>
        <div class="w3-main w3-center">
            <img src="/portfolio/assets/img/mwassa_Vis_pic.png" width="50%" height="50%">
            <figcaption>Notes sequence in FL studio </figcaption>
            <img src="/portfolio/assets/img/midi_picture.png" width="50%" height="50%">
            <figcaption>Imported notes in Jupyter notebook using mido</figcaption>
            <img src="/portfolio/assets/img/midi_picture_2.png" width="50%" height="50%">
            <figcaption>Final 2D array of notes </figcaption>
        </div>
        <p class = "justify">
        I normalized the total time of the sequence and divided the imported phrase into two different segments, which I then superimposed.
        </p>
        <div class="w3-main w3-center">
            <img src="/portfolio/assets/img/Mwassa_Vis_Graph.png" width="50%" height="50%">
            <figcaption>Graph linking the whole phrase </figcaption>
            <img src="/portfolio/assets/img/Mwassa_Vis_Graph_2.png" width="50%" height="50%">
            <figcaption>The two segments superposed</figcaption>
        </div>
        <p class = "justify">
        The purpose of this exercise was to demonstrate the contrast between successive melodic segments within a melodic phrase. This analysis helped me further explore the musical characteristics or signature of the genre. In this case, the first segment ends on the third note of the scale, while the second segment ends on the first note of the scale, also known as the tonic note. Ending on the tonic note often provides a sense of finality, while ending on the third note creates a feeling of partial closure.
        <br>
        This exercise represents one of my initial attempts to analyze and quantify melodies, aiming to better visualize the mood and feeling of a song, as well as to compare and differentiate between songs and genres.
        </p>
</div>




