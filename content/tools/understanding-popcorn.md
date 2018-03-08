---
title : "Understanding Popcorn"
author : ["Matt Price"]
date : 2015-07-21T13:48:00-04:00
lastmod : 2018-03-08T12:05:03-05:00
draft : false
banner : "testbanner"
menu :
  main:
    weight : 1013
    identifier : "understanding-popcorn"
    parent : "Tools"
---

You may find it useful, as you prepare for the next assignment, to read the following post!


## What is Popcorn {#what-is-popcorn}

[Popcorn](http://popcornjs.org) is a Javascript "libary" -- a small collection of programs -- that lets web designers key events in a web page to a time-code in a media file.  So essentially ,popcorn lets you "cue up" content ad display it only during fixed periods, while a media element is playing. If you then pause or manually rewind/fast-forward the media element (audio or video), the events will also reset to the appropriate time.


### HTML5 & new possibilities {#html5-and-new-possibilities}

Popcorn works because of new functionality that is provided by the [HTML5](http://en.wikipedia.org/wiki/HTML5) standard, and in particular the [<audio> and <video>](http://www.html5rocks.com/en/features/multimedia) tags.  So you are working with very new technology here. The new standards let you manipulate audio  and video directly with HTML and Javascript -- something that wasn't possible until about a year ago.


### multi-media swiss-army knife {#multi-media-swiss-army-knife}

Popcorn is a sort of Swiss army knife for doing multi-media work in HTML5.  There's a main framework -- the popcorn library -- that provides a simple Javascript interface for talking directly to the media elements.  Doing that directly can be hard, so the Popcorn "layer" makes this work quite a bit easier.  This underlying library is used by the [Popcorn plugins](http://popcornjs.org/plugins), which are the elements you will actually be working with.  These plugins are fairly simple Javascript programs (the mapping ones are actually kinda complex, and some of the things one wants to do with maps -- especially smoothly animate a pan from one location to another -- aren't available yet, which is too bad and a bit of a disappointment).  It's the plugins that you will actually be working with.


### Using Popcorn {#using-popcorn}

To use popcorn in a web page, you need to define a variable -- usually named 'pop' -- that creates a popcorn 'instance' on your web page.  Then you wrap the variable definition in a simple function that makes sure it gets run when the web page loads.


## Popcorn Plugins {#popcorn-plugins}

Inside the variable definition, you "call" the plugin function for each event you want to create. The process is very similar to creating timeline events in your timeline -- there's a simple syntax that defines a couple of "parameters" -- variables that get "passed" to the plugin function.  The example file defines a bunch of popcorn events; essentially you'll just change the values of these parameters to create your own events.  So for instance, here's an example plugin definition:

```javascript
.footnote({"id":"intro","start":6,"end":16,"target":"popcorn-container","text":"Edna begins by talking about her father, Daniel Kelly (1861-1953). The US census of 1880 for Elgin, IL, gives Daniel’s occupation as blacksmith. In the 1900 census of Port Angeles his occupation is bridge builder; in the 1920 census of Eden Valley it is general farming; in the 1920 census of Eden Valley it is dairy farming.  In the 1930 census of Port Angeles he is retired."})
```

This is one of the plugins you'll use the most -- the footnote plugin. It has just five parameters:

-   **id** -- this is for your benefit so you can keep track of what you're doing. Use it, but don't worry about it too much
-   **start** -- when to start playing the element. This is in SECONDS -- so forinstance if you want to it to start playing at 6:34, the value would be 394.  Keep a calculator on hand. Note that the value is **not** in quotation marks -- that's significant.
-   **end** -- the end time
-   **target** -- where to pop up the event. Don't change this, or your events will show up in the wrong place.  With popcorn you can put the new events anywhere on the page, and change any existing element. It's really powerful; we're just brushing the tip of the iceberg.
-   **text** -- this is the text you're going to make appear.  This is where your own contribution really comes in.


### Available plugins {#available-plugins}

We've provided examples for three plugins:

-   Footnote you've just seen
-   [Image](https://github.com/mozilla/popcorn-js/tree/master/plugins/image) lets you display an image. This adds two new parameters -- 'src' and 'href' -- which let you select an image and also link that image to another location, if you so wish.
-   [Google Maps](https://github.com/mozilla/popcorn-js/tree/master/plugins/googlemap) Creates a google map. There are a bunch of new parameters here, see our source code for more info.
-   it's possible you will also want to use others; of these the most likely to be of use is [Wikipedia](https://github.com/mozilla/popcorn-js/tree/master/plugins/wikipedia).

(The links in this section take you to the plugin sourcecode, which will usually be a directory with 4 files. The `html` file contains a working example of the plugin code. The `js` file is the sourcecode itself, and usually starts off with a useful explanation of how the plugin works. The last two files are provided for testing purposes, you shouldn't need to have use it.


## Media Elements {#media-elements}

Popcorn woks by keying commands to a media element -- that is, an HTML tag `<audio>` or `<video>`.  Here's our sample audio tag:

```html
<!-- this is our audio div.  It's really important -->
 <audio id="media" controls="controls">
   <source src="media/audio/editededna.mp3" type="audio/mp3" />
</audio>
```

I just want you to note three things about this code:

-   See how the <audio> tag has two attributes. The **id** is essential, because when we defined "pop" we told it to look for the element called "id". "controls" is also important -- it ensures that you can pause, rewind, etc. in the browser's buiilt-in media player.
-   The actual file that will be used by the "audio" element is not defined in the tag itself, but within it -- in the <source> tags.


## Getting Help {#getting-help}

If you end up confused, there are a couple of useful popcorn resources on the web.

-   alas, most of the old resources have been taken down in the past 2 months. All that's really left is the [Github repo](https://github.com/mozilla/popcorn-js/).


## Generating Events with Tabletop {#generating-events-with-tabletop}

In class today, we _hand-coded_ our popcorn events. This is not particularly onerous but is a little clumsy. You are absolutely welcome to use this method for the assignment if you like; but there is another way.  the [tabletop.js](https://github.com/jsoma/tabletop) library lets you access information from a Google Spreadsheet and plug it into your scripts. I find it very handy for this kind of work (we could have used it for the mapping expercise, too).  In this way, you can create your popcorn events in the leisure of a Google Spreadsheet, and have the events automatically generated for you whenbever your web page loads.

The process is described [in the tabletop repository](https://github.com/jsoma/tabletop#1-publishing-your-google-sheet), and you are strongly advised to read it carefully. If you want to use the code I've provided for you in `popcorn-data-with-google.js`, you will need to [copy this spreadsheet](https://docs.google.com/spreadsheets/d/14jExD0zl9nvZyExoMsF_9wWr86Jmrk5c8Crt4G1EJuU/edit#gid=1715955432), then **publish it** as described in the tabletop instructions (see above), and also **copy the new URL** into the appropriate place in `popcorn-data-with-google.js`.  Then code your popcorn in the spreadsheet; unless you make any syntax errors, the technical work should now be done. In the spreadsheet it is somewhat easier, for instance, to arange your events in sequence, etc.
