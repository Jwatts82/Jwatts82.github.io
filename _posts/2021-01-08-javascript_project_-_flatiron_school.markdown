---
layout: post
title:      "JavaScript Project - Flatiron School"
date:       2021-01-08 17:28:46 -0500
permalink:  javascript_project_-_flatiron_school
---



### The Requirements
<p> The fourth software engineering project for Flatiron School required us to build an application with a HTML, CSS, and JavaScript frontend with a Rails API backend.  All interactions between client and server were required to be handled asynchronously (AJAX) and use JSON as the communication format.  It was required to be Object Oriented JavScript to encapsulate related data and behavior.  The Rails backend needed to have a resource with a has-many relationship and have at least 3 AJAX calls (at least two of Create, Read, Update, and Delete).


My project is a quarantine movie system that keeps a record of movies to watch during quarantine.  The object model relationship is a category has many movies in its list.  
</p>

### What I Did
<p> Please view my github repo [[here]](http://)(https://github.com/Jwatts82/quarantine-movies.git).  My project is a quarantine movie system that keeps a record of movies to watch during quarantine.  The object model relationship is a category has many movies in its list.  
</p>

<a href="https://imgur.com/vvchAL1"><img src="https://i.imgur.com/vvchAL1.png" title="source: imgur.com" /></a>

<p>  On the Categories index page, I have a list of movie categories that, when clicked, show the category movie list itmes. When the movie list items are clicked, the movie information with name, description and watched or not watched is shown . 

<p> To achieve exposing the data via json, I made use of the Active Model Serializers gem. an active model serializer is great for serializing database content, especially content that is built with relational content. Setting up serialization was as easy as generating a serializer for a model and defining the associations that needed to be serialized.</p>

<p> The next challenge was to take the json content and work with it via JavaScript. I took some time to gear out of ruby and work with JavaScript objects. I decided to use the ES6 class syntax to build my objects. The example i have below is a Movie Class.  I took advantage of ES6 template literals to output html with model content - you can see this below below.</p>

<a href="https://imgur.com/n2ZnnUg"><img src="https://i.imgur.com/n2ZnnUg.png" title="source: imgur.com" /></a>

I used iterators and JQuery to process the data and append content to the DOM. The challenge for me was to work through the a step-by-step processes of collecting data and displaying it.  But in the end it came together:

<a href="https://imgur.com/vvchAL1"><img src="https://i.imgur.com/vvchAL1.png" title="source: imgur.com" /></a>







