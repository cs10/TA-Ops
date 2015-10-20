# A Logistical Overview of CS10

* Labs
* Lecture
* Discussion
* Assignments


* Collaboration
* Github
* HipChat
    * Hubot
* Asana
* GoogleDocs
    * Dropbox
* Miscellaneous Tools
* Projects Guide

---
### TO MOVDE:

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