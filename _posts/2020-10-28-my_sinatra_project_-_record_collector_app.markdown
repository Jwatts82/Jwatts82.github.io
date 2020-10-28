---
layout: post
title:      "My Sinatra Project - Record Collector App"
date:       2020-10-28 18:25:58 +0000
permalink:  my_sinatra_project_-_record_collector_app
---


<a href="https://imgur.com/tKXXIGs"><img src="https://i.imgur.com/tKXXIGs.jpg" title="source: imgur.com" /></a>

My second project for my Flatiron course was to create a Sinatra application that tracks something.  I love music and have many albums so I went with creating and app that tracks the records each user has in their collection.  This is the first CRUD, MVC (Models, Views, Controllers) app using Sinatra that we made from scratch.

### Structuring the app

I used the Corneal gem to get started on this project.  This set up the basic structure of my project including models, views and controllers. 

### Creating Database Tables & Migration Files

After Corneal created the basic structure for my project I created migration files to create my tables.

<a href="https://imgur.com/ssvYyAF"><img src="https://i.imgur.com/ssvYyAF.png" title="source: imgur.com" /></a> <a href="https://imgur.com/fxuRUho"><img src="https://i.imgur.com/fxuRUho.png" title="source: imgur.com" /></a>

The next step was to set up the models that inherit from active record, it was required to have a has_many relationship on a User model and one belongs_to relationship on another model. 

<a href="https://imgur.com/hGRJSsn"><img src="https://i.imgur.com/hGRJSsn.png" title="source: imgur.com" /></a>
<a href="https://imgur.com/mKXNomT"><img src="https://i.imgur.com/mKXNomT.png" title="source: imgur.com" /></a>


### Next the controllers were set, these handle all of the routing or “logic” for the project.
  
1. application_controller (all other controllers inherit from this controller)
2. albums_controller ( app routes::inherit from application controller)
3. users_controller (users sign up route::inherit from application controller)
4. sessions_controller (users log in route::inherit from application controller)

### Styling
All that was left was styling and not having much experience in this it was a little difficult for me at first.  I found Bootstrap and decided to give it a go, only problem was I did not know how to use it! After completing the quick start in the documentation introduction part of the site I had access to bootstrap, now how to use it?  I was able to find the components and utilities links on the page that led to information and code to style my project but I needed a little more guidance to understand how it worked.  For that I turned to an awesome YouTube.com channel [Academind](https://www.youtube.com/channel/UCSJbGtTlrDami-tDGPUV9-w ) that helped me to understand the how and why of bootstrap and enabled me to get some styling added to my project.  

Feel free to check out my repo [Here](https://github.com/Jwatts82/Record-Collection-App.git).

