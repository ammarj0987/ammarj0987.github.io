---
layout: post
title: "Web Scraper"
---

<h3> Web Scraper </h3> [Github](https://github.com/ammarj0987/Web-Scraper)

<p> Web Scraping can be used in many ways for many different reasons. In this project I implemented a web scraping script to extract useful performance metrics of different vehicles. <a href="https://www.caranddriver.com/">Car And Driver</a> is an American automotive enthusiast magazine that reviews and tests all kinds of cars. They provide a spec sheet of all the testing that is done on a car. I collected urls of some of the cars that I am interested in and compiled them into a csv file. </p>

![c/d]({{  site.baseurl }}/assets/cd.png)

<p> I used <a href="https://jsoup.org/">Jsoup</a> which is a Java library for working with real-world HTML. It provides a very convenient API for fetching URLs and extracting and manipulating data, using the best of HTML5 DOM methods and CSS selectors. With the help of Jsoup, I was able to connect to each url and search only the spec sheet part of the page to collect data that I am interested in. </p> 

<p> I used <a href="http://opencsv.sourceforge.net/">openCSV</a> to import the urls that I collected and export a csv file containing the data from the spec sheet. I was interested in comparing weight, hp, torque, 0-60, 5-60 and 1/4 mile time of different cars so I created a csv file with openCSV that contains all these metrics of all the cars I am interested in comparing. I can now further use this data to analyze why some cars are faster than others and how each of these performance metrics relate to each other. </p>

![scraper-input]({{  site.baseurl }}/assets/scraper-input.png)
![scraper-output]({{  site.baseurl }}/assets/scraper-output.png)