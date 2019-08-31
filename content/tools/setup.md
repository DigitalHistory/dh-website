---
title: "Setup"
author: ["Matt Price"]
lastmod: 2019-08-20T15:39:52-04:00
draft: false
banner: "testbanner"
menu:
  main:
    identifier: "setup"
    parent: "Tools"
    weight: 10
---

For the duration of this course, you will need to set up a "development environment" to do your work. You'll need to download,install, and interact with a group of programs and services that make it possible to do your work. Setting your environment up can be difficult, so be sure to budget some time to do so! Also be aware that these tools will take up significant spae on your laptop and may cause your laptop to slow down somewhat if run simultaneously with


## Platform Notes {#platform-notes}

I run [Arch Linux](https://archlinux.org) on my laptop, and have experience with [Ubuntu](https://www.ubuntu.com/) as well. For the purposes of this class, I have installed Windows 10 Education Edition ([available free to U of T students here](https://uoft.onthehub.com/WebStore/Security/Signin.aspx)).  I wil also attempt to support MacOS as best I can.

-   if you have an earlier edition of Windows, some of our tools may not work properly. I encourage you to upgrade to Windows 10 Education Edition, which has good support for modern tools.
-   if you have a Chromebook, you will need to install a full Linux OS in order to do the coursework. [Gallium OS](https://wiki.galliumos.org/Welcome%5Fto%5Fthe%5FGalliumOS%5FWiki) and [Crouton](https://github.com/dnschneid/crouton) are the two recommended tools for this, and you can find [some instructions here](https://arstechnica.com/gadgets/2017/06/how-to-install-linux-on-a-chromebook/). It's not easy, and I won't be able to help you.  If this seems hard, you may want to think about buying an inexpensive, older laptop and installing an ordinary Linux distribution.  [Here are](https://fossbytes.com/best-lightweight-linux-distros/) [two lists](https://fossbytes.com/best-linux-distro-beginners/) of distributions, but the choice is up to you. .


## Details {#details}

Here's the table of tools from the syllabus:

| Tool                   | On Mac                                                                                                                     | On Windows                                                                                                                                             | On Linux                                                                                                                 |
|------------------------|----------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| Real Web Browser       | [Firefox](https://www.mozilla.org/en-US/firefox/) and/or [Chrome](https://www.google.com/chrome/)                          | [Firefox](https://www.mozilla.org/en-US/firefox/) and/or [Chrome](https://www.google.com/chrome/)                                                      | [Firefox](https://www.mozilla.org/en-US/firefox/) and/or [Chrome](https://www.google.com/chrome/)                        |
| Text Editor            | [VSCode](https://code.visualstudio.com/download)                                                                           | [VSCode](https://code.visualstudio.com/download)                                                                                                       | [VSCode](https://code.visualstudio.com/download)                                                                         |
| Bash Shell Environment | Terminal (Built in)                                                                                                        | [Git for Windows](https://git-for-windows.github.io/) or [Windows Subsystem for Linux](https://msdn.microsoft.com/en-us/commandline/wsl/install-win10) | gnome-terminal, qterm, etc                                                                                               |
| Git Version Control    | [Git for OSX](https://sourceforge.net/projects/git-osx-installer/files/)                                                   | [Git for Windows](https://git-for-windows.github.io/)                                                                                                  | `apt-get install git`                                                                                                    |
| Slack Community        | [Client Download](https://slack.com/downloads), [Signup Link](https://join.slack.com/t/digitalhistoryuoft/signup)          | [Client Download](https://slack.com/downloads), [Signup Link](https://join.slack.com/t/digitalhistoryuoft/signup)                                      | [Client Download](https://slack.com/downloads), [Signup Link](https://join.slack.com/t/digitalhistoryuoft/signup)        |
| Github Org Membership  | [Sign up here](https://github.com/join)                                                                                    | [Sign up here](https://github.com/join)                                                                                                                | [Sign up here](https://github.com/join)                                                                                  |
| Node and NPM           | [Node Website](https://nodejs.org/en/download/) ([guide](http://nodesource.com/blog/installing-nodejs-tutorial-mac-os-x/)) | [Node Website](https://nodejs.org/en/download/) ([guide](https://wsvincent.com/install-node-js-npm-windows/))                                          | [Node Website](https://nodejs.org/en/download/) ([distro instructions](https://nodejs.org/en/download/package-manager/)) |

If you're comfortable exploring and installing software, you can probably get set up quickly by following the links above. **Please nonetheless read the detailed instructions below.** Things will go smoother if you do!


## Web browser {#web-browser}

All of our work will involve interacting with the World Wide Web. Firefox and Chrome are head and shoulders above all other web browsers, and you should install one (or preferably both) of them. In class, I will use Firefox almost exclusively. If you haven't tried Firefox for a while, give the new Quantum version a try' it is much, much faster and more stable than its predecessors.

Both have highly sophisticated **developer tools** with which you should familiarize yourself. As you learn more about web design, you'll come to rely on these tools more and more. Follow these links for more about [Firefox Dev Tools](https://developer.mozilla.org/en-US/docs/Tools/Page%5FInspector) and [Chrome's version](https://developer.chrome.com/devtools).

Of particular value in both Chrome and Firefox is the "Javascript Consoles," accessible from the developer tools: `Tools \rightarrow Web Developer \rightarrow Console` or `Menu \rightarrow More Tools \rightarrow Developer \rightarrow Console`

The Firefox console is a little awkward to use for multi-line programming, so they have also provided a "Scratchpad" tool (`Shift-F4`), which I find helpful, though I now use VSCode's Javascript console instead (see "Text Editor", below).

The other tool I use all the time is "inspect element", available by right-clicking on any part of a web page.  Both of these tools will prove **essential** for figuring out why your code isn't working right!


## Text Editor {#text-editor}

If you want to code, you have to write like a coder. This means using a powerful text editor. In this class we use [Visual Studio Code](https://code.visualstudio.com/). Please follow the download links and install to your computer. There's a separate post about using VSCode -- once you've installed it, navigate there!


## Command Line {#command-line}

Web developers and digital humanists spend a lot of their time in the _command-line environment_, interacting with their computers through text-based commands instead of a mouse or voice interface.  It takes some time to learn to use the command-line, but it's a very powerful and effective way to work once you get used to it. One goal of this course is to help you get comfortable in this environment and learn to take advantage of its power.

There are actually many different command-line environments; in this class we use [bash](https://www.gnu.org/software/bash/), the most popular.

On Mac and Linux, bash is built in to the system.  In Mac, open the `Terminal` app to find the bash prompt; in Linux you may have any of several terminal emulators installed, search your program list for "term" to find yours.

In Windows, bash comes with the Git installation -- follow the instructions below. Note that very recent editions of Windows 10 come with the "Windows Subsystem for Linux (WSL)", which you can use instead of the Git Bash method.

**IMPORTANT UPDATE**: VSCode has an [integrated terminal](https://code.visualstudio.com/docs/editor/integrated-terminal), and it's extremely useful. Windows users will have to do a little bit of work in order to use bash in the integrated terminal. See the excellent [terminal configuration instructions online](https://code.visualstudio.com/docs/editor/integrated-terminal#%5Fconfiguration), and be sure to follow the link explaining [how to access the user settings screen in VSCode](https://code.visualstudio.com/docs/getstarted/settings#%5Fcreating-user-and-workspace-settings).


## Git, Github, and GitKraken {#git-github-and-gitkraken}

Software development is made **vastly** easier by "[version control](https://git-scm.com/book/en/v2/Getting-Started-About-Version-Control)" systems: specialized software that keeps track of the history and current state of files and directories. In the past there were many such systems, but now almost the whole user uses [git](https://git-scm.com/), and we're all grateful for it.


### Install Git {#install-git}

To install git, follow the [download links](https://git-scm.com/downloads) on the website (see the table above for OS-specific links and instructions). We'll come back to the Git command-line in a minute.


### Sign up for Github {#sign-up-for-github}

For many developers -- maybe even most of them -- using Git is intimately tied to the [Github](https://github.com) code-sharing website.  We'll be using Github for almost all of our work this semester, so it's important that you get familiar with it.  If you were present for the first class, you've already done this. If not, you'll need to [sign Up for a Github account](https://github.com/join). Once you've done that, you have two choices:

-   practice working at the command line
-   go straight to a GUI ("Graphical User Interface") that will make working with git a little more comfortable.

I recommend at least trying the command line first.


### Command-line Setup {#command-line-setup}

You need to tell git a little bit about yourself. Start with your [email address](https://help.github.com/articles/setting-your-email-in-git/) and [your user name](https://help.github.com/articles/setting-your-username-in-git/). Open your bash shell (Terminal in Mac, git-bash in Windows) and type:

```sh
git config --global user.name "Your Name"
git config --global user.email "youraddress@ mail.utoronto.ca"
git config --global github.user YourGithubId
```

Great -- now git knows who you are. If you're feeling ambitious, you can also [set up SSH keys so you don't have to type in your password every time you commit to Git](https://help.github.com/articles/connecting-to-github-with-ssh/).


### VSCode Git {#vscode-git}

VSCode also has an interface to Git and Github. It's pretty powerful and intuitive, so I recommend trying it before installing GitKraken. [The instructions are here](https://code.visualstudio.com/docs/editor/versioncontrol#%5Fgit-support).


### Using the GitKraken GUI client {#using-the-gitkraken-gui-client}

Sometimes it's nice to have a backp. [GitKraken](https://www.gitkraken.com/) is an impressive visual tool that also makes it easy to [configure all of your information](https://support.gitkraken.com/start-here/profiles).  They have a nice video about [SSH integration](https://support.gitkraken.com/integrations/authentication), which you can watch if you like.


### Learn more {#learn-more}

There is a somewhat more wordy [Git tutorial on this website](http://digitalhistory.github.io/introduction-to-github), which you should read. For now, [Install the Github Desktop App](https://desktop.github.com/) which also includes the command-line version of git.  You can follow the [excellent tutorial in the downloadable git-it application](https://github.com/jlord/git-it-electron/releases), as well as the [Github Desktop documentation](https://help.github.com/desktop/guides/).  There is also a [quite helpful tutorial on The Programming Historian](http://programminghistorian.org/lessons/getting-started-with-github-desktop). We'll be discussing Git and Github further in our first class.


## Node and NPM -- This is the hardest part! {#node-and-npm-this-is-the-hardest-part}

**Right now it looks like the drag and drop tool we wanted to make will NOT be ready for this semester** :frowning_face:

Installing Node is not strictly necessary for the first assignment. If you are having trouble, put this off till next week.

Most of our programming work will involve Javascript, which runs most of the web. The [Node.js](https://nodejs.org/en/) environment and its "package manager," [NPM](https://www.npmjs.com/), are an incredible resource for Javascript development. In fact, Slack, VSCode, and gitKraken are all written as Node applications themselves! Installing the "bare" versions of node and NPM lets us access some of that power while we work.

You can survive this class without installing Node, but without it, you won't be able to run the test suites that accompany all of the assignments. You'll therefore be at a disadvantage in the class, because the tests offer hints about what's wrong with your code.

-   In Mac and Linux, the instructions linked to in the table above are probably good enough.
-   In Windows, you may follow all the instructions and then find yourself getting an error ("`Command not found`"). If that happens, you may want to try [the instructions laid out here](http://blog.theodo.fr/2017/01/use-git-ssh-and-npm-on-windows-with-git-bash/), or if you're on Windows 10, [you could go crazy and install the amazing Windows Subsystem for Linux](https://hackernoon.com/running-nodejs-on-linux-on-windows-88bd12993bae), which allows you to work as if your computer had a real Unix operating system like everyone else.

The details of Node and NPM are a little outside the scope of our class, but [a colleague at the University of Washington](https://info343.github.io/machine-setup.html#node-and-npm) has an excellent introduction in one of his courses.


## Slack {#slack}

Slack is not strictly necessary to do your work, but it is the principal means of conversation for the class. Your activity in our Slack team is part of your participation assessment. So, please sign up for the team using the signup links above, and if you're not familiar with Slack already, read [some of the Slack documentation](https://get.slack.help/hc/en-us/search?utf8=%E2%9C%93&query=bold+italic&commit=Search).
