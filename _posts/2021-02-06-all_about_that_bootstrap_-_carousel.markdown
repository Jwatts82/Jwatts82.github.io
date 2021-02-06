---
layout: post
title:      "All About That Bootstrap - Carousel"
date:       2021-02-06 18:56:38 +0000
permalink:  all_about_that_bootstrap_-_carousel
---


#### Its All About The Bootstrap…..

During my project building at Flatiron School I noticed I was pretty “Plain Jane” and thought I would brush up on some styling. In my search I found  Bootstrap but I still did not understand how to really apply it to my project.  Then came in Udemy, I found a course on Bootstrap and it was on!  One problem, I watched the course went to my next project which was in React-Redux and the Bootstrapping was applied in some different ways.

##### First you have to run: 

npm install react-bootstrap bootstrap

##### Next you import the following on your index page:

Import ‘bootstrap/dist/css/bootstrap.min.css’

##### Finally you must import the component 

For each page you use bootstrap on you must import the individual components rather then the entire library:

import { Button } from ‘react-bootstrap’ 

After this it was all about the styling, my favorite component was the Carousel.  I was able to create a carousel of images to show on my homepage.  Carousels don’t automatically normalize slide dimensions so you have to put these in yourself. 

![]("https://i.imgur.com/FqsFbM1.png" title="source: imgur.com")


Here is the code i used to make my React Bootstrap Carousel:

```
const BootstrapCarousel = () => {  
        return (  
            <div>  
                <div className='container' > 
                    <div className='row' > 
                        <div className='col-sm-8 m-auto' >
                            <Carousel>  
                                <Carousel.Item style={{'height':"300px"}} >  
                                    <img style={{'height':"300px"}}  
                                    className="d-block w-100"  
                                    src={"https://source.unsplash.com/PtCmDqF8nXc/700x400"} alt="Arches National Park" />  
                                    <Carousel.Caption>  
                                        <h3>Arches National Park </h3> 
                                        <p>Grand County, Utah</p> 
                                    </Carousel.Caption>  
                                </Carousel.Item  >  
                                <Carousel.Item style={{'height':"300px"}}>  
                                    <img style={{'height':"300px"}}  
                                    className="d-block w-100"  
                                    src={"https://source.unsplash.com/vIEJB5ZQD3g/700x400"} alt="Acadia National Park" />  
                                    <Carousel.Caption>  
                                        <h3>Acadia National Park</h3>
                                        <p>Maine</p> 
                                    </Carousel.Caption>  
                                </Carousel.Item>  
                                <Carousel.Item style={{'height':"300px"}}>  
                                    <img style={{'height':"300px"}}  
                                        className="d-block w-100"  
                                        src={"https://source.unsplash.com/Hwd6xMr1xng/700x400"} alt="Point Lobos State Natural Reserve" />  
                                    <Carousel.Caption>  
                                        <h3>Point Lobos State Natural Reserve</h3>
                                        <p>Carmel, California</p> 
                                    </Carousel.Caption>  
                                    </Carousel.Item>  
                                <Carousel.Item style={{'height':"300px"}}>  
                                    <img style={{'height':"300px"}}  
                                        className="d-block w-100"  
                                        src={"https://source.unsplash.com//dvtc1AU0CjI/700x400"} alt="Escola State Park"/>  
                                    <Carousel.Caption>  
                                        <h3>Ecola State Park</h3>
                                        <p>Cannon Beach, Oregon</p>  
                                    </Carousel.Caption>  
                                </Carousel.Item>  
                            </Carousel>
                        </div>
                    </div>
                </div>  
            </div>  
        )  
     
}  

export default BootstrapCarousel  
```




