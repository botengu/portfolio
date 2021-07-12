---
layout: post
title:  The Shape of Music
permalink: "/music/shapemusic/"
---

<div class="w3-row">
    <h1 style="text-align:center">The Shape of Music: A New Visualization Tool for Cyclic Rhythmic and Melodic Patterns</h1>
      <p class = "justify">
<br>
Many tools have been developed to visualize music. Visualizing music has many applications whether they are educational or industrial. 
Several reviews have discussed some of the ways music can be visualized, such as the one done by Khulusi et al. \cite{khulusi2020survey}. Their work has categorized the visualization of music into different categories; charts, graphs, heat maps, maps, piano roll view, timeline, 3D rendering, and the rest. Many articles have studied the similarity of melodies and the usual approach is to compare the note frequencies; rare are the studies that consider the relative frequencies of notes in a piece. Visualizing music considering the ratio between the frequency of each note of the melodic pattern and the one of its root would be a great way to compare the similarity between melodic patterns irrespective of their scales.  
<br>
Toussaint \cite{toussaint2010computational} has contributed a lot in the field of visualization of rhythms. Drawing from his expertise in computational geometry, he has been able to analyze and to compare the rhythmic patterns from different cultures. The tool he has developed is essential when it comes to visualizing all types of rhythms, including non-western rhythms. He has also worked on inserting the melodic patterns inside his visualization tool. However, only the rhythmic components of the melodic patterns were taken into consideration. 
<br>
The present work aims at building upon the tools developed by the latter author. Aside from rhythm, the chord progression is often a distinctive feature of a song, even to the ear of the one who has never studied music. While some songs are made by strumming distinctive chords cyclically, others are made by adding several melodic patterns that each comprise sequential single notes; those patterns are added in an interlocking manner (for example, the lead and rhythmic guitar in Congolese Rumba). Most songs combine the two styles.  
<br>
Melodic patterns can be seen as rhythmic patterns with an additional dimension - the pitch. When musicians improvise over different chord progressions, they need to adjust how they go up and down the scale. The purpose of the following tool is to visualize that adjustment. Also, the way musicians improvise is heavily influenced by the drums' patterns, the present tool also allows us to visualize the relation between the patterns of melodic instruments and the drums' patterns.
<br>
The workflow for the work I intend on doing can be summarized as follow: First, for a musical piece, all the notes of each instrument's melodic pattern are extracted. Having all notes allow us to find the key. Instead of a Cartesian frame, polar coordinates are used. All those notes are spread in a circular manner.  Each note is represented by a point that has two coordinates; a radial, the distance from the origin (center of the circle), and an angular one - which is the angle between two lines: the first line which passes by the point (representing the note) and the origin and the second line which is the horizontal diameter of the circle. The angle is related to the time at which the note appears in a melodic pattern. The total angle of 360$^\circ$ corresponds to the duration of a melodic pattern. To determine the radial component of each point, a new metric was developed to show how to relate each note of the melodic pattern to the key of the song. 
Finally, the rhythmic wheel from Toussaint's work is added on top of the existing polar graph and centered at the origin.  
<br>
The purpose of such a tool will be to visualize and recognize a chord progression from a melodic pattern made of successive single notes. Furthermore, this work will also allow us to geometrically infer rules between existing melodic and rhythmic patterns. 
<br>
For future work, geometrical and algorithmic algorithms can be used to analyze musical pieces and find their similarity. Also, once the rules will have been established, I plan to investigate whether or not the same rules can be used to generate new musical patterns.  
<br>
<br>

<br>
<audio controls>
  <source src="horse.ogg" type="audio/ogg">
  <source src="horse.mp3" type="audio/mpeg">
Your browser does not support the audio element.
</audio>
</div>



