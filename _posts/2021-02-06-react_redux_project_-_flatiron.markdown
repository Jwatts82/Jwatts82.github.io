---
layout: post
title:      "React Redux Project - Flatiron"
date:       2021-02-06 18:00:53 +0000
permalink:  react_redux_project_-_flatiron
---


## Trails 

"<img src="https://i.imgur.com/xadKGGx.png" />

### The Idea

For final project at Flatiron School, I created an application called [Trails](https://github.com/Jwatts82/trails-client.git) — which is a simple application for outdoor adventurers to track their hiking trails. Users can click on a Park that leads to a list of all the trails they have hiked in that park which includes the number of miles the trail is and its difficulty.  If users wish to see all the the trails they have entered they can do so as well.

#### Project Structure

4 Routes

<Route exact path='/' component={Home} />
<Route exact path='/parks' component={ParkList} />
<Route exact path='/parks/new' component={ParkForm} />
<Route path='/parks/:id' component={ParkTrailsContainer} />
<Route exact path='/trails' component={TrailsContainer} />


3 Containers

ParksContainer.js
ParkTrailsContainer.js
TrailsContainer.js


#### 5 Stateless components

Home.js
Carousel.js
Navigation.js
Footer.js
Nps.js

Creating a Rails API Backend
The Rails API handles data persistence so setting this up first was key.  I used scaffolding and active_model_serializers gem to accomplish this.

Associations:

Park
has_many :trails
Trails
belongs_to :park

Set up CORS - Cross-Origin Resource Sharing

 
#### 2. Creating a React App Frontend

I used create-react-app to generate the start of the project. Then added React-Redux, using functions such as store, provider, connect. Redux-Thunk middleware was applied next. Last the Router was added which allows for a single page web application with navigation without page refresh when navigating.  

Here is a [link](http://youtu.be/cZyTyRuoYvc) to a video demonstration of the application.
 
