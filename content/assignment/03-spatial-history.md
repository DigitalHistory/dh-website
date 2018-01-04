---
title : "Assignment 03: Spatial History"
author : ["Matt Price"]
date : 2017-01-04T21:55:00-05:00
lastmod : 2018-01-04T13:46:37-05:00
draft : false
banner : "testbanner"
menu :
  main:
    weight : 1007
    identifier : "assignment-03-spatial-history"
    parent : "Asisgnments"
---

**Due Date: March 02**

In class, we made a kind of toy Google Map out of hand-coded HTML, CSS, and Javascript.  You will remember it from the course website, from [JSBin](http://jsbin.com/jusena/10/edit?html,js,output), and from [Github](https://github.com/titaniumbones/maps-with-markdown).

Your next assignment builds directly from that in-class exercise, and should be quite a bit easier to manage, technically, than your last assignment.  Essentially, you will repeat the in-class assignment with much greater intellectual effort, but using the same technical framework. [Please work directly with the files in the Github repo](https://github.com/titaniumbones/maps-with-markdown), either by forking the repo, or downloading the zipball.


## Assignment {#assignment}

Build a web page that includes a Google Map (complete with markers) as part of a short but substantive historical exploration of a historical topic of interest to you.  We discussed a number of such themes in the class (you should remember them from our discussion). The final product should meet the following criteria:

-   **Essay:** You should write a short essay, approximately 900 words (~ 3-4 pages double-spaced, if we were using word processors) addressing a small, specific historical topic _with a spatial history component_. That is, the "spatial" element shouldn't just be an afterthought, but should be at the centre of your analysis.

    Here are some plausible examples of appropriate topics:

    -   Corridor of Power: Berlin's Friedrichstrasse in the Nazi Era
    -   End of an Era: Toronto's last meatpacking plants
    -   An Empire at Home: conservative Think Tanks in Washington, D.C.

    I just made these up, of course. You should pick something that you (a) know something about already, and (b) are interested in. Ideally, you will already have done some research into this topic, and will have a small number of sources ready to hand. The essay should introduce the reader to the topic, and make a not-too-complex argument which, again, highlights the spatial component.  ("Think tanks, so important in the construction of policy in today's United States, are a relatively new feature of American politics. In this paper, I will discuss the early history of this now-paramount institutional form, and argue that the _geographical proximity_ of these think tanks is actually an important feature.")

    You may notice that most of my examples are drawn from a kind of urban history. Urban history is obviously well-suited to spatial analysis, but there's no reason you can't describe, for instance, more widespread networks (e.g., to take some examples at random, networks of hippies, underground bus networks, comparative suffrage movements. etc.)

    Take this opportunity to think about the effect of _form_ on _content_.  How does the present of the map change the way you express your thoughts? Are new kinds of arguments possible? On the flip side, does the map lead you to ignore or downplay any important elements?

    The essay will be written in [Markdown](http://markdowntutorial.com/lesson/1/), which makes traditional citations a little complicated ([Scholarly Markdown](http://scholdoc.scholarlymarkdown.com/) solves that problem, but it's fairly difficult to set up).  So please use simple links for your citations; in Markdown, these take the form `[I'm an inline-style link](https://www.google.com)`. So, for instance: `[Latour, p. 97](http://search.library.utoronto.ca/details?5484640&uuid=4f41639c-43d4-45e8-81f2-d8acd9263f8a)`.  Don't worry about a bibliography.

-   **Map:** Your map should have at least 5 markers, and could have many more.  You can explore more complex objects -- such as polygons -- using the geoJSON import feature sof Google Maps.  There are links to the API documentation in the code.

    In class, we cut and paste to create multiple markers. The assignment template uses a [_for_ loop](http://www.w3schools.com/js/js_loop_for.asp) to _iterate_, that is, repeat, a set of actions for a group of markers.  See the template for details.  Each marker's info-window contents should contain a brief headline and some explanatory text.  Your essay should refer back to the markers, and you are free to refer to your essay in the marker text itself.

-   **Styling:** As was also the case with our in-class assignment, the bulk of the styling work is accomplished for us by the _strapdown.js_ script that we call at the bottom of the page. Remember that you can use any of several _bootswatch_ themes if you would like to try a different overall look. If you like, you can also customize the CSS further by using  the _style.css_ file in the project folder


## Getting your assignment, and handing it in {#getting-your-assignment-and-handing-it-in}

This assignment is stored on Github. You can get it easily by navigating to <https://github.com/titaniumbones/maps-with-markdown> and locating the "DownloadZIP" button.

To hand it in, simply rezip the folder and send it to me at the Dropbox Request URL I'll send you before the due date; be sure to rename the folder itself to something that contains your name before zipping, e.g., "matt-price-his389-spatial-history". If you don't take this step, your work will not be preserved and I won't grade your assignment.

**Or:** If you like, you are more than welcome to login to your github account, fork the repository, edit, and push your changes to the web; if you do that, then all you need to do is send me the URL of your new repository.


## Learning Objectives {#learning-objectives}

-   Understand what a Google Map is and how it relates to GIS
-   Learn the simplest parts of the Google Maps Javascript API, and use them to create map elements
-   Integrate a written historical narrative with a digital map object


## Expectations {#expectations}

Your essay should meet the ordinary criteria for an historical essay: clearly written, providing adequate evidence, minimal spelling and grammatical errors, etc. The relationship between topic and map should not be artificial -- the map should serve as an important part of your historical argument or explanation.

Your Map should _work_ -- all your markers should display correctly. The initial zoom should be set so that all of your markers are visible, and when I click on those markers the appropriate text should display.  Markers should provide information that makes your written text clearer or more persuasive.

While there is not much styling work to do, you should not create a terrible mess! You should make small visual changes to the default layout to make the legend more useful and visually appealling, and think about further work if it seems appropriate.

A "B" paper will make a convincing, interesting argument, using the map as an important and cogent support.  An "A" paper will do the same, but will do all of the above just a little bit better. "C" and "D" papers wil lbe deficient in some of these areas.
