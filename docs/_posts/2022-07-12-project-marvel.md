---
layout: post
title: "Marvel Connections"
---

([email](ammar.junejo0987@yahoo.com) for access)

![marvel]({{ site.baseurl }}/assets/marvel.png)

<p>In this project, I used Spark framework for beackend and React for frontend. The goal of this project was to find connections between Marvel superheroes. I started this project by implementing a Graph data structure. The graph is a HashMap of Node as key where the value is a HashSet of edges. I then loaded a csv file that contained all the marvel superheroes and the books they appeared in. These were stored in the graph in the form of nodes and edges. By creating this connection between chracters and books, I used Breadth-First-Search algorithm on the graph. The user can search and select two superheroes from Marvel Universe and when Find connection is clicked, All the books that the two superheroes appear in together are returned.</p>

<p>I used React to create the website. I added dropdown menus that are searchable so the user can choose between all the marvel characters. After choosing characters, when the find connection button is hit, spark server fetches the result from Model API and prints it on the screen</p>

