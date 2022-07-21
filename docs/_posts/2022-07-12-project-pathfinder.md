---
layout: post
title: "UW Pathfinder"
---

<h3>UW Pathfinder</h3> ([email](ammar.junejo0987@yahoo.com) for access)

<p>In this project, I used Spark framework for backend and React for frontend. The goal of the project was to find the shortest path between two buildings on UW campus. I implemented a graph from scratch that has edges as routes and nodes as buildings. The graph is a HashMap of Node as key where the value is a HashSet of edges. By implementing and applying Dijkstra's algorithm, I was able to find the shortest paths in the graph. In the app, user can choose buldings from a drop-down menu and when draw is clicked, a route is drawn on the map showing the shortest route between the two selected buildings.</p>

<p>I used to React to design the app. I added the map and two drop-down searchable menus so the user can select two buildings. The menus are loaded in the start by pulling all the options from Model API. When the draw button is clicked, spark server fetches the shortest route in the form of cordinate points form model API. The cordinates are then used to draw lines on the map to show the shortest path.</p>

![pathfinder]({{ site.baseurl }}/assets/pathfinder.png)