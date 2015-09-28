# Background
It's tricky to run a large university class. It's tricky to do it well, and to do so with lessening resources. This is a guide for how CS10 works at UC Berkeley.

This guide is both for course staff, but also should serve a resource for anyone else in academia to use, and maybe even improve upon. Because this is a public guide, there may be sections which are intentionally missing, or parts that are a bit unclear. If you'd like to know, please get in touch!

# What are [CS10] and [BJC]?
[CS10], is UC Berkeley's offering of [BJC], an entry level programming course, designed for non-majors.

_The Beauty and Joy of Computing_ is a curriculum that's designed both for high school students, and for college-level "CS0" courses. The course is built around a blocks-based programming language called [Snap<em>!</em>][snap], which inherits much of the design from MIT's [Scratch]. BJC focuses on some of the "big ideas" of computer science:

* Abstraction
* Recursion
* Lambdas (Higher Order Functions)

[CS10]: http://cs10.org/
[BJC]: http://bjc.berkeley.edu/
[Scratch]:
[BJC-Twitter]:
[BJC-FB]:

# So, is it _really_ that hard to run a class?


**Warning**: Stuff below this line needs to be moved...

---


* Collaboration
* Github
* HipChat
    * Hubot
* Asana
* GoogleDocs
    * Dropbox
* Miscellaneous Tools
* Projects Guide

#### Collaboration

The core work that we're trying to do, is make collaboration easier across the staff. The bulk of our communication still happens over an email list-serve for course staff. (We currently have a few different lists for each role.) However, as we use tools like Docs and HipChat much more of the communication is moving away from email. There's no one good strategy for communication. Despite the fact that "hating email" is popular and cool, it's damn easy to get everyone on board.

#### Using Git
We have a large group of TA's and we want everyone to have access to the web site, so this means we need something like git. Github is a great interface, is free, and pretty easy to use!

##### Github
First, [Github for Education](education.github.com) is awesome and will give you free private repositories if you need to keep things locked down. However, mostly Github provides a safe way to collaborate on code that we write and a great place to share it with others.

Here's the features we use:

* Organizations:
    This is in a "CS10" organization. We use it as a central place where all staff members can find the projects they need and automatically have access to them. As staff come and go, the members list can be updated, but all the projects we use will have a consistent home.
* Github Pages
    GH-Pages are a very simple way to host static websites. We try to build `gh-pages` compatible versions of the websites we have which are a very useful backup in the event of a school server outage.
* Issue Tracking
    It's lightweight, and simple. Assign staff members tasks and use them to collaborate on anything. Unlike discussion over email, issues can be directly attached to and reference items in a repo which makes things a bit easier to follow.

##### Web Hooks
Github supports web hooks, that allow a server to be pinged whenever a certain repo event happens. This is handy if you want to host a website on something that isn't Github pages. We've used web hooks to have the Berkeley servers trigger a `git pull` from our web site repos. This is a pretty simple process and you can see the code [here](github.com/cs10/webhooks)

##### Barcode Scanner
This is mostly a small thing, but many many devices have bar codes on them! We use a bar code scanner to scan iClicker IDs and student ID cards when we check-in / check-out iClickers. [They're cheap](http://amzn.com/B00406YZGK?tag=calphoto-20) and don't need any configuration.
