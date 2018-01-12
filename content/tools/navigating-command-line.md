---
title : "Navigating at the Command Line"
author : ["Matt Price"]
date : 2015-07-21T13:48:00-04:00
lastmod : 2018-01-12T13:07:07-05:00
draft : false
banner : "testbanner"
menu :
  main:
    weight : 1002
    identifier : "navigating-at-the-command-line"
    parent : "Tools"
---

**The _Programming Historian_ link below is excellent.  Having some trouble with screenshots ATM, will fix soon as I can reload my desktop -- but for next few hours pls refer to the _PH_ link for images!**

One common issue for people new to the command line is that it can be tough to understand the notion of _location in the filesystem_. Most ordinary users interact with their filesystems through the so-called [GUI layer](https://en.wikipedia.org/wiki/Graphical_user_interface) -- the graphical interface of windows. Often the user-accessible files are more or less restyricted to special directories (or "folders") with meaningful names like `Desktop`, `MyDocuments`, etc. However, once you start working at the command line this convenient feature can become something of a curse.  It's important to recognize that these special locations are just part of a complex, hierarchical filesystem -- a branching tree of directories and files, on which your operating system relies in many ways. You will need to learn to navigate that filesystem, not from the GUI, but from the command line.

When you first start using the command line, it often feels (a) confusing and (b) somehow primitive or over-simple. The command line is, in fact, a sophisticated and incredibly efficient way to interact with the filesystem -- but you need to learn your way around it first. In this class we won't discuss the wonderful world of shell scripting (see below for guides to scripting); instead, I just want you to learn a few **very** basic commands to help you move around.


## Navigation {#navigation}

The file system is a "branching tree" of files and folders.  At the top (or bottom, depending on how you imagine things) of the tree is the "root". In bash, we represent this as `/`.  Every folder has a **path** that starts with `/` and proceeds down the file hierarchy. So, for instance, my global git configuration is located at `/home/matt/.gitconfig`.  `/` is the root. `/home/` is where all user files can be found. `/home/matt/` contains all **my** user files. `/home/matt/.gitconfig` identifies the specific file I'm looking for.

Your file exlorer will represent this tree for you visually; you can also picture it schematically, as is done e.g. in the following image:
{{<figure src="https://tr1.cbsistatic.com/hub/i/2015/06/03/208a6a3f-0987-11e5-940f-14feb5cc3d2a/10_things_linux_filesystems.jpg">}}

We can also explore from the command line. Here are a few basic commands to learn for this purpose.


### pwd {#pwd}

`pwd` is short for "print working directory", and will show you where you are in the file system.
<../../images/pwd.phg>


### ls {#ls}

`ls` will **list** the contents of a directory. With no further arguments it will list the directory you're currently in, but you can ask it to list some other directory too. Here are some examples.  Note the "switches" `-l` and `-la`.  Switches give firther instructions to the command. In this case `-l` means "long" while ~-a" isshort for "all". You can see in the screenshot below what the effect is.
{{<figure src="../../images/ls-screenshot.png">}}


### cat and less {#cat-and-less}

Sometimes you want to look at the contents of a file.  `cat` and `less` are two ways to do so.  `cat` will print the contents of the file directly to your terminal window.  `less` will create a simple interface that you can use to scroll through a longer file using a kayboard interface.
{{<figure src="../../images/cat-ss.png">}}


### mkdir and touch {#mkdir-and-touch}

`mkdir` wil lcreate a new directory, while `touch` will create a new (empty) file.

```sh
mkdir some-directory-name
touch some-directory-name/somefile.txt
```

These commands will create the file somefile.txt in the folder some-directory-name, inside the current working directory.


## Learn More {#learn-more}

OK, that's all for now, hopefully this helps you navigate around your projects. I may add to this guide as we go through the semester, but here are some further guides.

-   [this introduction](https://sklise.com/2012/09/22/introduction-to-git/#no-buttons) is quite clear and simple
-   [the programming historian](https://programminghistorian.org/lessons/intro-to-bash) has a great guide too
-   [the TLDP guide](http://tldp.org/HOWTO/Bash-Prog-Intro-HOWTO.html) introduced generations of programmers to bash scripting, and is still a useful reference point
