---
layout: post
title:      "**Flatiron School Ruby CLI Project**"
date:       2020-10-01 16:45:22 -0400
permalink:  flatiron_school_ruby_cli_project
---


It is a few weeks into the Flatiron School Software Engineer program and it is project time! The project assignment is to build a Command Line Interface (CLI) that interacts with a website to display data to the user. The requirements i sthat the data provided must go at least one level deep.  A "level" is where a user can make a choice and then get detailed information about their choice. 


## **Commence Freak Out!**

<iframe src="https://giphy.com/embed/NKBc1zpXB47Xa" width="480" height="270" frameBorder="0" class="giphy-embed" allowFullScreen></iframe><p><a href="https://giphy.com/gifs/scared-shocked-scream-NKBc1zpXB47Xa">via GIPHY</a></p>


After spending a good amount of time freaking out, i finally deciede i needed to just pic a topic and go with it.  The topic i chose was National Park Services sites.  I chose this topic because recently my family and i took two road trips in a sprinter van exploring state and national parks.


<br>
<br>
<iframe width="560" height="315" src="https://www.youtube.com/embed/zM_6kDqcf-8" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
<br>
<br>
### **National Parks Service API**

The National Park Service provides an API to locate National Park Services sites by state.  

An API key for this site, once you have a key, the url to the site is as follows, where you pass the sattae code of the state you would like to search for sites in the url query string.
"https://developer.nps.gov/api/v1/parks?stateCode=#{state_code}&api_key=#{key}"


### ***Coding Process***

After watching Avi's second videos and reviewing all of the lecture videos I first started with creating a flow chart to understand where i wanted to go and how to go about getting there.  This worked out well, and made it easier for me to see the data flow.  I proceded with setting up the CLI and creating a skeleton for my project to start on.  since my API required a key i had to register for one and provide that information to my CLI in order for it to work.  I proceded through the project utilizing the API KEY to retrieve the information I needed to present to the user.

The CLI performs as follows:

1.  User is greeted and asked to enter a state code (ex. AL, CA, ME) for the state they would like to see all of the National Parks Services sites for.

2.  Once the user chooses a state that they would like to see, all of the National Park Service sites form a list.

3. The user then selects the site they would like information on.

4. The user can decide from ther to look at another site from the original states list or they are given the option to select another state or exit.

One challeng that i struggled with was understanding how the key worked and how to make it a part of my CLI without allowing others to see it.   by utilizing rubyguides i was able to navigate through the process. 



Overall it was a fun and stressful experience. 

<iframe src="https://giphy.com/embed/KCdolWLJ7FCPq3b9jR" width="480" height="270" frameBorder="0" class="giphy-embed" allowFullScreen></iframe><p><a href="https://giphy.com/gifs/rka-ink-rachael-kay-albers-KCdolWLJ7FCPq3b9jR">via GIPHY</a></p>
