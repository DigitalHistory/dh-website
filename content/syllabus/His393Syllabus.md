---
title : "Syllabus"
author : ["Matt Price"]
date : 2017-01-03T00:00:00-05:00
draft : false
creator : "Emacs 27.0.5 (Org mode 9.1.4)"
banner : "testbanner"
menu :
  main:
    identifier : "syllabus"
    weight : 10
---

## Logistics {#logistics}

| **Instructor:**   | Matt Price                                                     |
|-------------------|----------------------------------------------------------------|
| **Email:**        | matt.price@utoronto.ca                                         |
| **Office Hrs:**   | T 1-2:30, [SS 3077](http://map.utoronto.ca/utsg/building/033)  |
| **Meeting Times** | Thurs 2-4, [SS 1088](http://map.utoronto.ca/utsg/building/033) |
| **Web:**          | <http://digital.hackinghistory.ca/>                            |
| **Slack:**        | <https://digitalhistoryuoft.slack.com/>                        |

In general, communication should take place **via Slack**.  In the case of questions having to do with official University business (requests for extensions, discussion of accommodations, any message involving sensitive personal data) please [use my University email, being sure to put "HIS393" in the subject line](matt.price@utoronto.ca?subject=HIS389%20Digital%20History).


## Introduction {#introduction}

We all know &#x2013; it is so commonplace that we barely even notice it! &#x2013; that we are living through a revolutionary period in the history of communication.  In the year of your birth, the World Wide Web was a scrawny, hand-powered frontier of hand-coded sites and Internet startups.  Amazon and Google were infants.  The University of Toronto Library website [looked something like this](https://web.archive.org/web/19971210222202/http://library.utoronto.ca/):

{{<figure src="/ox-hugo/Screenshot from 2015-06-23 16-12-51.png" class="someclass">}}

and many students and faculty still used the card catalog to find books in Robarts.

Today, the processes of research, writing and reading are all dramatically transformed by information technology.  Instead of painstakingly discovering rare books and manuscript artifacts, we can do full-text searches on a vast corpus.  Our writing is mediated by immensely powerful computing machines, and our creations need not be limited exclusively to the linear texts around which all the humanities initially took shape.  Readers encounter our writing, not as a few precious drops of information in a desert of ignorance, but as part of an endless stream of information that assaults them all day long.

How should history respond to these new conditions of our existence?  In this class we explore foundational topics in the "[digital](http://whatisdigitalhumanities.com/) [humanities](http://digital.humanities.ox.ac.uk/Support/whatarethedh.aspx)" and ask what we can learn from them about _how we should be doing history_ &#x2013; in particular, how we should be collecting, analyzing, synthesizing and presenting knowledge.

-   How do the digital media developed in the last two decades change the way we understand history? Can the fundamental goal of _interpreting_ the past survive?
-   What, if any, new technical skills do we need to acquire?
-   Can we use the new media to ask (and answer!) new kinds of questions? Can they help us improve our answers to the old questions?
-   Perhaps most powerfully: how do the new digital conditions of existence relate to the question of "engaged" scholarship?  What new opportunities, constraints, and dangers does digital production call forth when we mix scholarship and citizenship?


## Objectives {#objectives}

At the end of this course, you should:

-   be able to describe to others what the phrase "digital humanities" means to you.
-   be able to frame a coherent and nuanced argument _of your own_ about the value of DH methods to the field of history
-   be able to clearly state and defend a position regarding "engaged scholarship", and articulate the relationship of your argument to the contemporary media landscape
-   have a basic understanding of markup languages and their use in DH
-   be able to make compelling use of media materials such as audio, video, and animation in historical arguments
-   understand how to create simple historical maps, and have an opinion about the value of GIS in historical argument


## Method {#method}

There are many approaches to the digital humanities, all of them involving tools that are under rapid and iterative development.  A given project is likely to require a substantial training period in the particular tools chosen by the principal investigators.  It is therefore not possible for this course to provide an effective survey of "the" digital humanities toolkit. But learning  tools is an essential skill for the digital humanist. So what should we do?

Almost every digital humanist will, at some point, need to do the following:

-   read and edit HTML, CSS and Javascript
-   debug running web pages using the browser's built-in tools
-   use a text editor to write code in any of several languages
-   collaborate with peers using version control software, almost always `git`

Our emphasis is therefore on _simple coding_ taught using _standard tools that are available almost everywhere_.  Almost all of the software we use is Free or Open Source. You will learn very basic web development skills and _slowly_ come to apply them to _increasingly sophisticated_ (but still pretty simple!) historical questions.  These baby steps will give you some sense of what skills a "real" digital history project requires, and give you the tools you'll need to _teach yourself_ when you encounter new tools in the course of a project.


## Policies {#policies}


### Accessibility {#accessibility}

The University provides academic accommodations for students with disabilities in accordance with the terms of the Ontario Human Rights Code. For information on services and resources, see <http://www.studentlife.utoronto.ca/as>


### Respecting Diversity {#respecting-diversity}

Diverse backgrounds, embodiments, and experiences are essential to the critical thinking endeavor at the heart of higher education. We expect you to be respectful of the many social and cultural differences among us, which may include, but are not limited to: age, cultural background, disability, ethnicity, technical ability, gender identity and presentation, citizenship and immigration status, national origin, race, religious and political beliefs, sex, sexual orientation, and socioeconomic status. Please talk with me right away if you experience disrespect in this class—from any source, including myself—and I will active work to address it.


### Correspondence {#correspondence}

As noted above, most communication should take place **via Slack**.  In the case of questions having to do with official University business (requests for extensions, discussion of accommodations, any message involving sensitive personal data) please [use my University email, being sure to put "HIS393" in the subject line](matt.price@utoronto.ca?subject=HIS389%20Digital%20History).  I'll do my best to reply within two working days, though occasionally the delay may be slightly longer. Please allow the full 48 hours to elapse before sending a repeat email.

**Also:** I have an injury-related difficulty co-ordinating action between my left and right hands, which leads to very frequent & distinctive typographical errors (and is also one of the many reasons you don't want to hear me play a musical instrument). In my course materials, assignment comments, and announcements, I strive to eliminate those errors, but in instant messaging I am less attentive, as typing corrections approximately triples my composition time. So&#x2026; please bear with me.


### Attendance {#attendance}

Make every effort to attend each class meeting (including lab sections)! Class will begin and (usually) end on time. Please do your best to get to class before the start of the session. Students are expected to attend all meetings, with exceptions permitted in case of illness and family emergencies.

Please silence all cell phones/pagers/etc. before the beginning of each class. You should bring your laptop for in-class work, but please don't use class time (lecture or lab) to check your email, update your Facebook, read reddit, watch YouTube, make dank memes, seize the means of production (allowed), etc. Such usage is distracting and interferes with learning both for you and for all the other students around you. Spend class time on class materials. If another student's activity is distracting, please ask them to stop it (or let me know outside of class).


## Tools {#tools}

Course assignments will require you to install software. All of the software we use is free, but it **requires a laptop to run**. A Chromebook unfortunately will not be sufficient. While it is in principle possible to do all of your assignments on the web or using a very basic text editor, I do not recommend that method, and will not offer technical support.  If you don't own a laptop, you should find a way to borrow one, or buy a cheap model on College St to use for the duration of the semester.

I can offer help with the following

| Tool                   | On Mac                                                                                                                     | On Windows                                                                                                                                             | On Linux                                                                                                                 |
|------------------------|----------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| Real Web Browser       | [Firefox](https://www.mozilla.org/en-US/firefox/) and/or [Chrome](https://www.google.com/chrome/)                          | [Firefox](https://www.mozilla.org/en-US/firefox/) and/or [Chrome](https://www.google.com/chrome/)                                                      | [Firefox](https://www.mozilla.org/en-US/firefox/) and/or [Chrome](https://www.google.com/chrome/)                        |
| Text Editor            | [Atom](https://atom.io/)                                                                                                   | [Atom](https://atom.io/)                                                                                                                               | [Atom](https://atom.io/)                                                                                                 |
| Bash Shell Environment | Terminal (Built in)                                                                                                        | [Git for Windows](https://git-for-windows.github.io/) or [Windows Subsystem for Linux](https://msdn.microsoft.com/en-us/commandline/wsl/install-win10) | gnome-terminal, qterm, etc                                                                                               |
| Git Version Control    | [Git for OSX](https://sourceforge.net/projects/git-osx-installer/files/)                                                   | [Git for Windows](https://git-for-windows.github.io/)                                                                                                  | `apt-get install git`                                                                                                    |
| Git Visualization      | [gitKraken](https://www.gitkraken.com/)                                                                                    | [gitKraken](https://www.gitkraken.com/)                                                                                                                | [gitKraken](https://www.gitkraken.com/)                                                                                  |
| Github Org Membership  | [Sign up here](https://github.com/join)                                                                                    | [Sign up here](https://github.com/join)                                                                                                                | [Sign up here](https://github.com/join)                                                                                  |
| Node and NPM           | [Node Website](https://nodejs.org/en/download/) ([guide](http://nodesource.com/blog/installing-nodejs-tutorial-mac-os-x/)) | [Node Website](https://nodejs.org/en/download/) ([guide](https://wsvincent.com/install-node-js-npm-windows/))                                          | [Node Website](https://nodejs.org/en/download/) ([distro instructions](https://nodejs.org/en/download/package-manager/)) |

Please see the [Setup](http://digital.hackinghistory.ca/article/tools) page for more details about the particular tools we will be using. **YOU WILL ABSOLUTEY NEED TO HAVE THESE TOOLS IN ORDER TO TAKE THE COURSE**


## Course Requirements & Grading {#course-requirements-and-grading}

The assignments in this course take a wide variety of forms, and for the most part, differ significantly from what you're likely to have encountered in other History courses. If you have little technical experience, or have perhaps ended up in this course by accident (!), you may find some of the work daunting at first. I have done my very best to make the assignments feasible for beginners, but you will likely encounter some difficult moments.  I therefore **strongly** urge you to (1) start early! and (2) persevere through the difficult initial stages.  The frustration you experience is, in fact, part of pedagogical method here.  You are not expected to become a coding ninja, but _learning how to learn_ is a major component of work in the Digital Humanities.

Be warned! Marking in this course is unusual!

Grading in this course is done using a _modified point system_. The system may seem odd at first, but it has definite advantages for both students and teachers, so don't be intimidated. Instead of receiving a number or letter grade for each assignment, and then getting a weighted sum of those grades as your final mark, you will _choose what final mark to try for_ and then _complete the assignments required for that mark_.  A certain set of assignments is required for a D; for a C, you must complete all of the "D" assignments plus another set; for a B, all of the C assignments plus some more; and the same goes for an A.

Here are some more details:

-   **All Assignments Are Graded Pass/Fail:** Each assignment you get will include a careful explanation of my expectations. If your work meets those expectations, you get full credit; if not you get _no credit_.
-   **A 'Passing' Mark on Assignments is a B+:** In order to get credit for an assignment, you will have to demonstrate a high level of mastery &#x2013; about the level normally required for a B+.
-   **Each Higher Grade Represents a quantum level of additional achievement:** As you move up the ladder, assignments test more advanced and difficult concepts from the course.
-   **If you fail, you can try again:** You start the semester with 5 'retry' chits, which you can use to resubmit assignments that have not succeeded. If necessary, you can use all of those chits on a single assignment! Resubmission process must be completed withing 1 week of the return date of the original version.
-   **A late assignment costs one 'retry' chit:** There is no percentage penalty for late work; instead, a late paper will cost you one of your retry opportunities.
-   **Second and third tries get fewer comments:** I will give substantial comments on first tries; additional tries will get less and less fulsome commentary.
-   **Pluses and Minuses are determined by participation:** The only part of your grade which is not determined on a pass/fail basis is the "+" or "-" part, which is assigned based on your on and offline participation.  See the participation grade sheet for more details.

I know there will be questions!  Please don't hesitate to ask them.  And here, finally, is the list of assignments. Detailed assignments will be handed out with adequate time to permit completion.

| Assignment          | Due Date                                                                      | Brief Description                 | A           | B           | C           | D           |
|---------------------|-------------------------------------------------------------------------------|-----------------------------------|-------------|-------------|-------------|-------------|
| Git & Github        | <span class="timestamp-wrapper"><span class="timestamp">Jan. 15</span></span> | version control and collaboration | &checkmark; | &checkmark; | &checkmark; | &checkmark; |
| G & GH Extras       |                                                                               |                                   | &checkmark; |             |             |             |
| HTML & CSS          | <span class="timestamp-wrapper"><span class="timestamp">Jan. 26</span></span> | web markup and presentation       | &checkmark; | &checkmark; | &checkmark; | &checkmark; |
| H & C Extras        |                                                                               |                                   | &checkmark; |             |             |             |
| Javascript for DH   | <span class="timestamp-wrapper"><span class="timestamp">Feb. 02</span></span> | intro to programming              | &checkmark; | &checkmark; | &checkmark; | &checkmark; |
| JS Extras           |                                                                               |                                   | &checkmark; |             |             |             |
| Data-Driven History | <span class="timestamp-wrapper"><span class="timestamp">Feb. 16</span></span> | CANCELLED                         | x           | x           | x           | x           |
| Spatial History     | <span class="timestamp-wrapper"><span class="timestamp">Mar. 02</span></span> | Simple GIS Web project            | &checkmark; | &checkmark; |             |             |
| Oral History        | <span class="timestamp-wrapper"><span class="timestamp">Mar. 16</span></span> | Multimedia Web Project            | &checkmark; | &checkmark; | &checkmark; | &checkmark; |
| Project Proposal    | <span class="timestamp-wrapper"><span class="timestamp">Mar. 23</span></span> | Imagine a Digital History Project | &checkmark; |             |             |             |
|                     |                                                                               |                                   |             |             |             |             |


## Texts {#texts}

The following texts are required and available at the Bookstore, or via various online booksellers:

-   Moretti, Franco. _Graphs, Maps, Trees: Abstract Models for a Literary History_ Verso, 2005.
-   Geddes et al _Toward Spatial Humanities_ Bloomington: Indiana University Press, 2014.
-   Perks, et al. _The Oral History Reader_. 2006


## Course Outline {#course-outline}


### Text, Code, and the Web {#text-code-and-the-web}


#### Introducing _Digital History_ (<span class="timestamp-wrapper"><span class="timestamp">Jan. 04</span></span>) {#introducing-digital-history}

**Class Synopsis:** Introduction to the course, Github, and Markdown.

**Readings:** You may want to read some of these as general preparation for this and other history classes:

-   W. Caleb McDaniel. “How to Read for History.” W. Caleb McDaniel. Accessed June 27, 2015. <http://wcm1.web.rice.edu/howtoread.html>.
-   William Cronon, ["Why the Past Matters"](http://www.williamcronon.net/writing/Cronon_Why_the_Past_Matters.pdf)
-   Cohen, Daniel J, and Roy Rosenzweig. “Becoming Digital.” In _Digital History: A Guide to Gathering, Preserving, and Presenting the Past on the Web_. Philadelphia: University of Pennsylvania Press, 2006. <http://chnm.gmu.edu/digitalhistory/digitizing/>.

**In-Class Activity: Collaboration on Github, Markdown**


#### What the Web Signifies (<span class="timestamp-wrapper"><span class="timestamp">Jan. 11</span></span>) {#what-the-web-signifies}

We all live with the web, but that doesn't mean we think much about _how it works_ and _what it's changed_. This week's lecture presents some thoughts on the changing nature of the public sphere and the significance of the web's _digital_ and _machine-readable_ nature.

**Readings:**

-   Juergen Habermas, "The Public Sphere: An Encyclopedia Article" (1964) <http://www.sociol.unimi.it/docenti/barisione/documenti/File/2008-09/Habermas%20%281964%29%20-%20The%20Public%20Sphere.pdf>
-   Cohen, Daniel J. “Interchange: The Promise of Digital History” 95, no. 2 (September 1, 2008): 452–91. <http://jah.oxfordjournals.org.myaccess.library.utoronto.ca/content/95/2/452.short>

**In-Class Activity: HTML + CSS**


#### Abundance and Openness (<span class="timestamp-wrapper"><span class="timestamp">Jan. 18</span></span>) {#abundance-and-openness}

One of the key features of the web is its _immenseness_. We will discuss how this genuinely new circumstance transforms the work of the historian.

-   W. Caleb McDaniel. “How to Read for History.” W. Caleb McDaniel. Accessed June 27, 2015. <http://wcm1.web.rice.edu/howtoread.html>.
-   Council. “Many More than a Million: Building the Digital Environment for the Age of Abundance.” Council on Library and Information Resources. Accessed June 7, 2011. <http://www.clir.org/activities/digitalscholar/index.html>.
-   Turkel, William J. “Going Digital.” Accessed October 12, 2011.  <http://williamjturkel.net/2011/03/15/going-digital/>.

-   “Learn How Google Works: In Gory Detail.” _PPCBlog_. Accessed June 30, 2015. <http://www.ppcblog.com/how-google-works/>.

**In-Class Activity: More HTML + CSS**


### Data Driven History {#data-driven-history}


#### Distant Reading 1 (<span class="timestamp-wrapper"><span class="timestamp">Jan. 25</span></span>) {#distant-reading-1}

Franco Moretti's _Graphs, Maps, Trees_ was a manifesto of sorts for a data-driven literary history. We'll discuss the first 2/3s of this book before turning to some practical skills

**Readings:**

-   Moretti, Franco. _Graphs, Maps, Trees: Abstract Models for a Literary History_. Verso, 2005 through p. 64, or  Moretti, Franco. “[Graphs, Maps, Trees.](http://search.proquest.com.myaccess.library.utoronto.ca/docview/1301929949/citation/D2E84E1A5CCD4A82PQ/1)” New Left Review 24 (November 1, 2003): 67–93m and Moretti, Franco. “[Graphs, Maps, Trees - 2](http://search.proquest.com.myaccess.library.utoronto.ca/docview/1301999488/citation/72DD61D56A3244B9PQ/1).” New Left Review 26 (March 1, 2004): 79–103
-   "Basic Text Mining" in _The Historian's Macroscope:_ <http://www.themacroscope.org/?page_id=362>

**In-Class Activity: Javascript variables & functions**


#### Distant Reading 2: Are Texts Data? (<span class="timestamp-wrapper"><span class="timestamp">Feb. 01</span></span>) {#distant-reading-2-are-texts-data}

More Moretti, and some criticisms

**Readings:**

-   Moretti, Franco. _Graphs, Maps, Trees: Abstract Models for a Literary History_. Verso, 2005, ch. 3 to end, or  “[Graphs, Maps, Trees - 3](http://search.proquest.com.myaccess.library.utoronto.ca/docview/1301919189/citation/3A603D9A5D1F4366PQ/1).” New Left Review 28 (July 1, 2004): 43–63. .
-   Stephen Ramsay, "[The Hermeneutics of Screwing Around](https://web.archive.org/web/20120611222242/http://www.playingwithhistory.com/wp-content/uploads/2010/04/hermeneutics.pdf)"
-   Gibbs, Fred. “Hermeneutics of Data and Historical Writing” Writing History in the Digital Age, March 14, 2012. <http://writinghistory.trincoll.edu/data/gibbs-owens-2012-spring/>.
-   Marc Dunkelman. “[What Data Can't Convey](http://chronicle.com/blogs/conversation/2014/08/19/what-data-cant-convey/).” Blog. _The Chronicle of Higher Education_, 19 2014.

**In-Class Activity: Javascript objects and DOM manipulation**


### Maps, Visualization, and History {#maps-visualization-and-history}


#### Spatial History (<span class="timestamp-wrapper"><span class="timestamp">Feb. 08</span></span>) {#spatial-history}

Contemporary "Historical GIS" and web-based geohistory projects descend from an illustrious lineage of qualitative and quantitative "spatial histories". In class today we explore what happens when "place" takes centre stage in a historical analysis.

**Readings:**

-   Mark Monmonier,  "[Lying with Maps](http://faculty.maxwell.syr.edu/mon2ier/e_reprints/StatSci%20Aug2005%20%28Lying%20with%20Maps%29.pdf)" _Statistical Science_ 20:3, 2005. 215-222.
-   Ben Schmidt, "[Data narratives and structural histories: Melville, Maury, and American whaling](http://sappingattention.blogspot.com/2012/10/data-narratives-and-structural.html)

**In-Class Activity: Mapping with Google**


#### ??? (<span class="timestamp-wrapper"><span class="timestamp">Feb. 15</span></span>) {#}

**Note: In all likelihood, there will be no class this week due to a scheduling conflict.**


#### NO CLASS (<span class="timestamp-wrapper"><span class="timestamp">Feb. 22</span></span>): READING WEEK {#no-class--reading-week}


#### Visualization (<span class="timestamp-wrapper"><span class="timestamp">Mar. 01</span></span>) {#visualization}

Of course, maps and graphs are in a certain sense part of a much broader field of _rhetorical visualizations:_ attempts to convey quantitative information through pictures in an effort to convince the reader.

**Readings:**

-   Jefferson Bailey and Lily Pregill, ‘[Speak to the Eyes: The History and Practice of Information Visualization](http://www.jeffersonbailey.com/speak-to-the-eyes-the-history-and-practice-of-information-visualization/)’, Art Documentation: Journal of the Art Libraries Society of North America, vol. 33 (2014).
-   Kostiantyn Kucher and Andreas Kerren, ‘[Text Visualization Browser: A Visual Survey of Text Visualization Techniques](http://textvis.lnu.se/)’, (2014)
-   Andy Kirk, 298 Data Visualisation Resources, Visualising Data, (2015).

**In-Class Activity: Reading visualizations**


#### Maps Online (<span class="timestamp-wrapper"><span class="timestamp">Mar. 08</span></span>) {#maps-online}

Maps and visiaulizations are neat and all, but contemporary web-based geohistory allows historical maps to interact powerfully with other data sources.  We'll explore some possibilities!

**Readings:**

-   "Railways and Agriculture in France and Great Britain" in _Spatial Histories_
-   "The Development, Persistance, and Change of Racial Segregation in U.S. Urban Areas, 1880-2010" in _Spatial Histories_
-   google earth tutorial: <https://geospatialhistorian.wordpress.com/lessons/lesson-1/>

**In-Class Activity: GIS**


### Oral History, Crowdsourcing, and the Promise of the Public Sphere {#oral-history-crowdsourcing-and-the-promise-of-the-public-sphere}


#### What's Special about Oral History (<span class="timestamp-wrapper"><span class="timestamp">Mar. 15</span></span>) {#what-s-special-about-oral-history}

Oral History has a long tradition; we explore its roots and peculiarities, and

**Readings:**

-   "The Voice of the Past" and "What makes Oral History Different" in _The Oral History Reader_
-   Listen to some part of  "I can almost see the lights of home" <http://www.albany.edu/jmmh/vol2no1/lightssoundessay.html>

**In-Class Activity: Popcorn.js**


#### Interlude: Project Planning & Citizen History  (<span class="timestamp-wrapper"><span class="timestamp">Mar. 22</span></span>) {#interlude-project-planning-and-citizen-history}

We'll discuss some project management techniques that should help you with your final proposal

-   <http://publichistorycommons.org/where-are-the-citizen-historians/>


#### Oral History & Remix Culture (<span class="timestamp-wrapper"><span class="timestamp">Mar. 29</span></span>) {#oral-history-and-remix-culture}

Once oral histories migrate to the web, they, like maps, can interact with other kinds of data.

If we're ahead of schedule, we'll watch _Harlan County USA_ in class.

**Readings:**

-   "Oral History and the Digital Revolution" and "Authoring in Sound" in _The Oral History Reader_
-   Gunkel, David J. “Rethinking the Digital Remix: Mash‐ups and the Metaphysics of Sound Recording.” Popular Music and Society 31, no. 4 (October 1, 2008): 489–510. <http://resolver.scholarsportal.info/resolve/03007766/v31i0004/489_rtdrmatmosr.xml>.

**In-Class Activity: popcorn.js (just in case)**


## Acknowledgments {#acknowledgments}

Thanks to Joel Wrossley of the University of Washington and Thomas J Bradley of Algonquin Collegee for help and inspiration in assignments and grading strategy.  The "Policies" section above is taken almost verbatim from [Joel's web development course](https://canvas.uw.edu/courses/1118282/pages/policies). Various pieces of the course have been inspired by other teachers over the year, and I hope to do a better job of document theft and inspiration from here on in.
