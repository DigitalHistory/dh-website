---
title: "Installing Node Dependencies"
lastmod: 2019-09-10T12:03:57-04:00
draft: false
menu:
  main:
    identifier: "installing-node-dependencies"
    parent: "Tools"
    weight: 10
---

Node.js is an exquisite piece of programming infrastructure. One of its main features is support for _developer-defined dependencies_. As a programmer &#x2013; or in my case, as a teacher &#x2013; you can inform the underlying node package manager (`npm`) that your project "depends" on some group of other projects. This allows programmers to build constantly on each other's work.

In our assignments, node dependencies are mostly used to enable the **tests**, whose main function is to help you figure out whether you've done the assignments correctly.  Installing node dependencies is pretty simple, but can be confusing if you're completely new to node, the command line, and programming in general.  Here are the (very simple!) instructions:

1.  Install Node and NPM as per [this section of the "Setup" instructions](../setup/#node-and-npm-this-is-the-hardest-part)
2.  From the command line, navigate to the root directory of your repository using `cd` as per [the navigation help page](https://digitalhistory.github.io/tools/navigating-command-line/)
3.  From the root directory of your repository,type the following command into the terminal/git-bash prompt: `npm install`

You should see some complex output from the command, after which your node dependencies will be installed. You can actually see the installed files by browsing the contents of the `node_modules` directory, which should now be present in your working directory.

Once the dependencies are installed, you should be able to run the node tests with `npm test` (issued from the same directory, that is, the root directory of your repository). If you've installed the VSCode extentions, ou

I hope that helps!
