---
layout: post
title:  Music Transcription on Instruments
permalink: "/music/transcription/"
---

<div class="w3-row">
    <h1 style="text-align:center">Transcription of notes on instruments</h1>
      <p class = "justify">
          I have been interested in audio processing and music theory for a while, and I've tried to write a music transcription algorihtm. The algorithm in question should take as inputs notes from an audio file and outputs the location of the notes on the instrument of choice (guitar,bass, piano). 
        </p>
        <p class = "justify">
        Doing so required me to go through a certain amount of steps.
      <ul>
        <li>First, I had to find how to extrat notes from an audio file: A note is essentially a wave, a melody is hence made of superimopsed of waves. Info from audio file can thus be extracted as a signal's plot showing how the amplitude varies with respect to time.</li>
      </ul>
      </p>
      <div class="w3-main w3-center" >
          <img src="/botengu/assets/img/timdom.PNG" width="50%" height="50%">
          <figcaption>Plot of a signal from an audio file</figcaption>
      </div>
      <p class = "justify">
      <br>
      <ul>
        <li>To extract the frequencies of all the waves in the previous plot, I had to use the Fast Fourier transform.<br>
        Fast fourier transform is a great tool to get from a time domain plot to a frequency domain one.</li>
      </ul>
      </p>
      <div class="w3-main w3-center" >
          <img src="/botengu/assets/img/frequencydom.PNG" width="50%" height="50%">
          <figcaption>Frequency domain of the original plot</figcaption>
      </div>
      <p class = "justify">
      <ul>
        <li> Then, online information was gathered to link those frequencies to right notes: I, myself, had some knowledge on the location of notes on instruments, hence I used this knowledge to link the right notes to the right position. Online info was obtained to find which frequencies belong to which notes using <a class= "links" href=" https://pages.mtu.edu/~suits/notefreqs.html">this link</a>.</li>
      </ul>
        </p>
      <div class="w3-main w3-center" >
          <img src="/botengu/assets/img/notes_freq.PNG" width="30%" height="30%">
          <figcaption>Online info was obtained to find which frequencies belong to which notes <a class= "links" href=" https://pages.mtu.edu/~suits/notefreqs.html">(https://pages.mtu.edu/~suits/notefreqs.html)</a>  </figcaption>
      </div>
      <br>
      <div class="w3-main w3-center" >
        <img src="/botengu/assets/img/Musicgif.gif" width="50%" height="50%">
        <figcaption>The tKinter tool was used to create the fretboard and visualize the notes</figcaption>
      </div>
        <p class = "justify">
        It is important to mention that I still am struggling with some issues. More precisely :<br> 
        <ul>
        <li>Some of the notes are right but are played at a lower octave (the frequency is halved) and there is also the noise which creates additional random notes. </li>
        <li>There is still noise from the audio file that can often be confused as notes. </li>
        <li>For guitars there are multiple locations for the same note, we should thus find how the set of locations which minimize the total distance travelled by the fingers. </li>
      </ul>




