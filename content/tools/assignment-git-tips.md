---
title : "Git Tips for Assignments"
author : ["Matt Price"]
date : 2015-07-21T13:48:00-04:00
lastmod : 2018-01-18T12:25:26-05:00
draft : false
banner : "testbanner"
menu :
  main:
    weight : 1004
    identifier : "git-tips-for-assignments"
    parent : "Tools"
---

Well the first assignment is done.  Whew! There were some common git issues that came up, and I hope we can cut back on them by documenting them here.


## Learn how to navigate! {#learn-how-to-navigate}

The command line is very new to everyone, and I did a lousy job of explaining how to traverse the filesystem from the terminal.  [I have now posted some instructions that should help with this](../../navigate-command-line/). **Pro tip:** in both Windows and Mac, you can open a terminal/git-bash window by right clicking on a location and clicking the "terminal here" or "bash  window here" buttons (screenshots anyone?). This should help reduce the amount of time spent hopelessly floundering in the early stages of command-line training.


## Don't commit .DS\_Store {#don-t-commit-dot-ds-store}

**Mac users:** MacOS creates these annoying files in every directory. They are useless for non-mac users and clutter up the repository.  I have taken steps that **should** stop you from accidentally adding these files to your repository, but if you have already started work on [Assignment 1](https://classroom.github.com/a/y1HlCM6k) you may have cloned the repository too early to get the benefits of that work. Here's how you remove \`.DS\_Store\` files from a repository:

-   first, navigate to the repository root directory in a terminal window
-   then, type the following commands (dark magic!):

```sh
find . -name .DS_Store -print0 | xargs -0 git rm -f --cached --ignore-unmatch
echo ".DS_Store" >> .gitignore
git commit -a -m "Git thee behind me, .DS_Store"
```

For an explanation of these commands, you can [look at random posts o n the Internet](https://hints.binaryage.com/how-to-remove-ds-store-files-from-a-git-repo/), [ask Stackoverflow](https://stackoverflow.com/questions/107701/how-can-i-remove-ds-store-files-from-a-git-repository), or read the official manuals (at least on MacOS) by typing `man find`, `man xargs`, `man echo`, and `man gitignore`. A lot of those explanations will be kind of complicated, though, especially the (insanely complicated) `find` manual.

**Note:** this command doesn't actually delete the files - -they will still be there, but git will **act** as though the files have been deleted, and will not "see" and files named `.DS_Store` when it looks for untracked files.


## Beware package-lock.json {#beware-package-lock-dot-json}

**Deprecation notice:** you shouldn't have to follow these instructions. check to make sure that package-lock.json is not present in your **web fork**. If it is, then something has gone wrong and you should follow these steps.

Unfortunately I rather misunderstood how package-lock.json works (because of outdated documentation). As a result I have removed it from the repository. You should remove it, too.  As above, you can do so by navigating to the repository root and typing:

```sh
git rm --cached package-lock.json
echo "package-lock.json" >> .gitignore
git commit -a -m "Goodbye, package-lock.json!"
```

Again, the file `package-lock.json` will still be on your computer, but git will act as though it had been deleted, and won't ask you to change it anymore.


## SPECIAL FOR ASSIGNMENT 1! {#special-for-assignment-1}

I've made some late-breaking changes to Assignment 1 to help with these issues. I've managed to push those changes to all of your repositories, so **please pull in my changes by executing \`git pull\`**. Everything below is **DEPRECATED**, but I'm keeping the info up here just in case something goes wrong.


## Deprecated detailed instructions -- DON'T FOLLOW THESE UNLESS SOMETHING HAS GONE TERRIBLY WRONG {#deprecated-detailed-instructions-don-t-follow-these-unless-something-has-gone-terribly-wrong}

You have 2 choices:

-   take the steps described above, then manually update `package.json` and `test/test-node.js` as described below
-   take the steps described above, then carefully read the new instructions -- **which tell you to name your reflection `Reflection/reflection.md` rather than `Reflection/yourgithubid.md` -- and ignore the fact that your tests are failing**
-   take a chance and do some fancy gitwork as described in the final section, below.


### `package.json` and `test/test-node.js` have been updated. Be careful! {#package-dot-json-and-test-test-node-dot-js-have-been-updated-dot-be-careful}

I've updated the tests a little bit to make it easier to run automated tests. My recommendation is as follows:

-   update `package.json` so that it's exactly the same as mine.  You really don't want there to be even 1 character of difference, or git might be mad at you.  [Here's my current version](https://raw.githubusercontent.com/DigitalHistory/assignment-01-html-css/master/package.json), and [here it is in the Github web interface](https://github.com/DigitalHistory/assignment-01-html-css/blob/master/package.json).


### Pulling changes from Assignment 1 [ADVANCED!] {#pulling-changes-from-assignment-1-advanced}

Alternatively... you can take care of almost all of the above issues by pulling my changes directly from the assignment repository. But, beware! There's a chance there will be "merge conflicts" and your whole repo will get screwed up.  Still, here's how i would do it:

-   first, make sure all of your changes have been committed with `git commit -a -m "emergency commit"`
-   Then make a note of the current git commit "hash" by executing `git log`. The output will look kind of like this:

```nil
commit cf369d7a9d7282270a95ab1ff0f8718b84015bfb (HEAD -> development, origin/development)
Merge: bd1c351 734d07c
Author: Matt Price <matt.price@utoronto.ca>
Date:   Thu Jan 18 08:37:22 2018 -0500

    Merge tag 'fix-json' into development

    fix it!

commit 734d07cd1b25ff428d13b802b07741aed470c5cd (tag: fix-json, origin/master, origin/HEAD, master)
Merge: 62423b7 e9c8f65
Author: Matt Price <matt.price@utoronto.ca>
Date:   Wed Jan 17 22:07:30 2018 -0500

    Merge branch 'hotfix/fix-json'

commit e9c8f6507ec13a4c53cff1c35293fc2c70d68f8e
Author: Matt Price <matt.price@utoronto.ca>
Date:   Wed Jan 17 22:05:27 2018 -0500

    remove syntax-breaking comma

    travis build should succeed now

```

The strange string of numbers and letters is called the "commit hash".  Copy the one at at the top to a safe location. In this example the hash to save would be `cf369d7a9d7282270a95ab1ff0f8718b84015bfb`.

-   now the dangerous step -- pull from my repo and merge into yours!
    `git pull https://github.com/DigitalHistory/assignment-01-html-css.git master`
-   if there are conflicts, you can either [try to fix them](https://help.github.com/articles/addressing-merge-conflicts), or (my recommendation) completely undo the merge by resetting your repo to the last working state.  For this you need that hash you copied a couple of steps ago.  This command will completely reset your master branch to the place it was before you tried to merge in my work:
    `git reset --hard cf369d7a9d7282270a95ab1ff0f8718b84015bfb`
    (**remember to use YOUR hash, not mine!**)

Looking forward to hearing how all of this goes!
