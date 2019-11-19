---
title: "Understanding Popcorn"
lastmod: 2019-11-19T13:51:56-05:00
draft: false
menu:
  main:
    identifier: "understanding-popcorn"
    parent: "Tools"
    weight: 10
---

You may find it useful, as you prepare for the next assignment, to read the following post!


## What is Popcorn {#what-is-popcorn}

[Popcorn](http://popcornjs.org) is a Javascript "library" &#x2013; a small collection of programs &#x2013; that lets web designers key events in a web page to a time-code in a media file.  So essentially, popcorn lets you "cue up" content ad display it only during fixed periods, while a media element is playing. If you then pause or manually rewind/fast-forward the media element (audio or video), the events will also reset to the appropriate time.


### HTML5 & new possibilities {#html5-and-new-possibilities}

Popcorn works because of ~~new~~ (actually, not so new!)  functionality that is provided by the [HTML5](http://en.wikipedia.org/wiki/HTML5) standard, and in particular the [<audio> and <video>](http://www.html5rocks.com/en/features/multimedia) tags. This standard lets you manipulate audio  and video directly with HTML and Javascript &#x2013; something that wasn't possible until about five years ago.


### multi-media swiss-army knife {#multi-media-swiss-army-knife}

Popcorn is a sort of Swiss army knife for doing multi-media work in HTML5.  There's a main framework &#x2013; the popcorn library &#x2013; that provides a simple Javascript interface for talking directly to the media elements.  Doing that directly can be hard, so the Popcorn "layer" makes this work quite a bit easier.  This underlying library is used by the [Popcorn plugins](http://popcornjs.org/plugins), which are the elements you will actually be working with.  These plugins are fairly simple Javascript programs (the mapping ones are actually kinda complex, and some of the things one wants to do with maps &#x2013; especially smoothly animate a pan from one location to another &#x2013; aren't available yet, which is too bad and a bit of a disappointment).  It's the plugins that you will actually be working with.


### Using Popcorn {#using-popcorn}

To use popcorn in a web page, you need to define a variable &#x2013; usually named 'pop' &#x2013; that creates a popcorn 'instance' on your web page.  Then you wrap the variable definition in a simple function that makes sure it gets run when the web page loads.


## Popcorn Plugins {#popcorn-plugins}

Inside the variable definition, you "call" the plugin function for each event you want to create. The process is very similar to creating timeline events in your timeline &#x2013; there's a simple syntax that defines a couple of "parameters" &#x2013; variables that get "passed" to the plugin function.  The example file defines a bunch of popcorn events; essentially you'll just change the values of these parameters to create your own events.  So for instance, here's an example plugin definition:

```javascript
let pop=Popcorn('#media')
// the leading "." says "call the `footnote` method of the new `pop` object"
.footnote({"id":"intro","start":6,"end":16,"target":"popcorn-container","text":"Edna begins by talking about her father, Daniel Kelly (1861-1953). The US census of 1880 for Elgin, IL, gives Daniel’s occupation as blacksmith. In the 1900 census of Port Angeles his occupation is bridge builder; in the 1920 census of Eden Valley it is general farming; in the 1920 census of Eden Valley it is dairy farming.  In the 1930 census of Port Angeles he is retired."})
```

This is one of the plugins you can use if you like  &#x2013; the footnote plugin. It has just five parameters:

-   **id** &#x2013; this is for your benefit so you can keep track of what you're doing. Use it, but don't worry about it too much
-   **start** &#x2013; when to start playing the element. This is in SECONDS &#x2013; so forinstance if you want to it to start playing at 6:34, the value would be 394.  Keep a calculator on hand. Note that the value is **not** in quotation marks &#x2013; that's significant.
-   **end** &#x2013; the end time
-   **target** &#x2013; where to pop up the event. Don't change this, or your events will show up in the wrong place.  With popcorn you can put the new events anywhere on the page, and change any existing element. It's really powerful; we're just brushing the tip of the iceberg.
-   **text** &#x2013; this is the text you're going to make appear.  This is where your own contribution really comes in.


### Available plugins {#available-plugins}

I've provided examples for as many plugins as I could.  All should work as-is:

-   Footnote you've just seen
-   [Figure](https://github.com/DigitalHistory/popcorn-js/blob/gmaps-update-api/plugins/figure/popcorn.figure.js) lets you display an image. This adds a new parameter &#x2013; 'src' &#x2013; which let you select an image and also link that image to another location, if you so wish. (I haven't tested the linking os it may not be implemented yet).
-   [Google Maps](https://github.com/mozilla/popcorn-js/tree/master/plugins/googlemap) Creates a google map. There are a bunch of new parameters here, see our source code for more info.
-   [Leaflet Maps](https://github.com/DigitalHistory/popcorn-js/blob/gmaps-update-api/plugins/leaflet/popcorn.leaflet.js) offers a slightly more familiar interface, though the problem with slow tile loading still persists.
-   [Markdown](https://github.com/DigitalHistory/popcorn-js/blob/gmaps-update-api/plugins/markdown/popcorn.markdown.js) allows you to add markdown annotations
-   [Wikipedia](https://github.com/DigitalHistory/popcorn-js/blob/gmaps-update-api/plugins/wikipedia/popcorn.wikipedia.js) will add the first few paragraphs from a Wikipedia page.
-   [Webpage](https://github.com/DigitalHistory/popcorn-js/blob/gmaps-update-api/plugins/webpage/popcorn.webpage.js) will embed a webpage in an iframe

(The links in this section take you to the plugin sourcecode, which will usually be a directory with 4 files. The `html` file contains a working example of the plugin code. The `js` file is the sourcecode itself, and usually starts off with a useful explanation of how the plugin works. The last two files are provided for testing purposes, you shouldn't need to have use them.)

You can explore the rest of the plugins as you wish; you may need to add some extra columns to your spreadsheet to get them to work


## Media Elements {#media-elements}

Popcorn works by keying commands to a media element &#x2013; that is, an HTML tag `<audio>` or `<video>`.  Here's our sample audio tag:

```html
<!-- this is our audio div.  It's really important -->
 <audio id="media" controls="controls">
   <source src="media/audio/editededna.mp3" type="audio/mp3" />
</audio>
```

I just want you to note three things about this code:

-   See how the <audio> tag has two attributes. The **id** is essential, because when we defined "pop" we told it to look for the element called "id". "controls" is also important &#x2013; it ensures that you can pause, rewind, etc. in the browser's buiilt-in media player.
-   The actual file that will be used by the "audio" element is not defined in the tag itself, but within it &#x2013; in the <source> tags.


## Popcorn Players {#popcorn-players}

Our default example plays a **local media file** from a **statically-defined media element**. I really hope you will choose to follow this method, though a web-based media element works just as well. However, if you need to, you can use Vimeo and Youtube videos, as well as Soundcloud audio.  To do that, you will need to rewrite the project HTML a bit. So, instead of this,

```html
<!-- this is our audio element.  It holds the audio file. -->
<audio id="media" controls="controls">
    <!-- Make sure this points to the actual mp3 file you are analyzing -->
    <source src="https://storycorpsorg-staging.s3.amazonaws.com/uploads/walsh2-1.mp3"
            type="audio/mp3" />
</audio>
```

You will want something like this:

```html

<section id=#media></section>
```

Then, you'll need to modify line 6 of `popcorn-data-from-google.js`:

```js
pop = Popcorn("#media")
```

and use something like one of the models below:

```js
const smart = Popcorn.smart( "#media", "http://www.youtube.com/watch?v=9oar9glUCL0" );
// const smart = Popcorn.smart( "#media", 'https://vimeo.com/267718090' );
// const smart = Popcorn.smart( "#media", 'https://soundcloud.com/corbanbrook/leaving-on-a-spaceship' );
```

the soundcloud player is a little buggy &#x2013; it emits a loud crackle when you start playback, and the 'play' button needs to be pushed twice. Also, there are no built-in volume controls (!). In fact, we have to add a little bit of hacky code to get the player to work at all. So you'll need something like this, on say line 22 (ish):

```js
pop.media.controls = true;
pop.unmute();
pop.media.volume = 65;
```

set the volume to whatever level feels right as the user won't be able to change it.


## Getting Help {#getting-help}

If you end up confused, there are a couple of useful popcorn resources on the web.

-   alas, most of the old resources have been taken down in the past 2 years. All that's really left is the [Github repo](https://github.com/menismu/popcorn-js/) and [the docs website](https://menismu.github.io/popcorn-docs/),  and both have been derelict for about 6 months. You can see my changes in [my main pull request](https://github.com/menismu/popcorn-js/pull/73), and browse through [the issues I've been submitting](https://github.com/menismu/popcorn-js/issues), especially [number 80](https://github.com/menismu/popcorn-js/issues/80).


## CSS and Popcorn display issues {#css-and-popcorn-display-issues}

In its day, Popcorn was designed for cutting-edge features that were just making their way to ghe browser. Now, no so much: the framework fails to take advantage of many of the new features of CSS3, and plugins are full of ugly, hard-coded CSS that can be hard to deal with. **I have started to fix this issue**, and in the plugins you are likely to use, much of the ugliest CSS has been stripped out. Instead, **most** plugins now neatly generate their own boxes (usually a \`div\` element) with an **id** and a **class** that you can set in CSS.

For the assignment, I have set the popcorn container element to `display: flex`, which is a pretty good default choice. Most events will attempt to set a width of `30em`, or about the width of 30 characters, and then grow or shrink if they have to. This default works well for most kinds of information, but not for all, so I've provided some examples of how to modify the default size.  You can set the element id for most plugins with the `id` column of the spreadsheet, and most plugins now add a class like `PLLUGINNAME-plugin` to their enclosing element.


## Generating Events with Tabletop {#generating-events-with-tabletop}

In class, we _hand-coded_ our popcorn events. This is not particularly onerous but is a little clumsy. You are absolutely welcome to use this method for the assignment if you like; but there is another way.  the [tabletop.js](https://github.com/jsoma/tabletop) library lets you access information from a Google Spreadsheet and plug it into your scripts. I find it very handy for this kind of work (we could have used it for the mapping expercise, too).  In this way, you can create your popcorn events in the leisure of a Google Spreadsheet, and have the events automatically generated for you whenbever your web page loads.

The process is described [in the tabletop repository](https://github.com/jsoma/tabletop#1-publishing-your-google-sheet), and you are strongly advised to read it carefully. If you want to use the code I've provided for you in `popcorn-data-with-google.js`, you will need to [copy this spreadsheet](https://docs.google.com/spreadsheets/d/1pL%5FLj62%5FZcW7iawTCQ%5F5BQsmdynCtC8y5BCNy3k2LOM/edit), then **publish it** as described in the tabletop instructions (see above), and also **copy the new URL** into the appropriate place in `popcorn-data-with-google.js`.  Then code your popcorn in the spreadsheet; unless you make any syntax errors, the technical work should now be done. In the spreadsheet it is somewhat easier, for instance, to arange your events in sequence, etc.
