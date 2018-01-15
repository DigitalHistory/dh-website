---
title : "Installing Node Dependencies"
author : ["Matt Price"]
date : 2015-07-21T13:48:00-04:00
lastmod : 2018-01-14T19:59:18-05:00
draft : false
banner : "testbanner"
menu :
  main:
    weight : 1003
    identifier : "installing-node-dependencies"
    parent : "Tools"
---

Node.js is an exquisite piece of programming infrastructure. One of its main features is support for _developer-defined dependencies_. As a programmer -- or in my case, as a teacher -- you can inform the underlying node package manager (`npm`) that your project "depends" on some group of other projects. This allows programmers to build constantly on each other's work.

In our assignments, node dependencies are mostly used to enable the **tests**, whose main function is to help you figure out whether you've done the assignments correctly.  Installing node dependencies is pretty simple, but can be confusing if you're completely new to node, the command line, and programming in general.  Here are the (very simple!) instructions:

1.  Install Node and NPM as per [this section of the "Setup" instructions](https://digital.hackinghistory.ca/tools/setup/#node-and-npm)
2.  From the command line, navigate to the root directory of your repository using `cd` as per [the navigation help page](https://digital.hackinghistory.ca/tools/navigating-command-line/)
3.  From the root directory of your repository,type the following command into the terminal/git-bash prompt: `npm install`

You should see some complex output from the command, after which your node dependencies will be installed. You can actually see the installed files by browsing the contents of the `node_modules` directory, which should now be present in your working directory.

Once the dependencies are installed, you should be able to run the node tests with `npm test` (issued from the same directory, that is, the root directory of your repository).

I hope that helps!
