TA-Ops
======

attempting to keep everyone's head on straight!

__TAOps__ is a set of docs, procedures, and tools for helping us effectively run CS10 and BJC at UC Berkeley.

Think DevOps, but for teaching.

## Background

Managing a large class and many projects related to the class can be complex...
We've complied some best practices and techniques.

Most of the stuff here will focus on tools and what we do, or at least try to do. We're not claiming to be perfect by any means, but hopefully this will be helpful to some others! The repo will hopefully also serve as some documentation for our ourselves so that we can build some institution knowledge. :)

Because of that dual nature of this document (internal and external), it may seem a little disjointed at times, or a few paragraphs might be irrelevant to you (whomever you are!), but please read along and let us know if it can be improved!

## The Meat

* Collaboration
* Using Git
    * Github
    * Web hooks
* HipChat
    * Hubot
* Asana
* GoogleDocs
    * Dropbox
* Miscellaneous Tools
* Projects Guide

#### Collaboration
<a name="collaboration"></a>

The core work that we're trying to do, is make collaboration easier across the staff. The bulk of our communication still happens over an email list-serve for course staff. (We currently have a few different lists for each role.) However, as we use tools like Docs and HipChat much more of the communication is moving away from email. There's no one good strategy for communication. Despite the fact that "hating email" is popular and cool, it's damn easy to get everyone on board.

#### Using Git
<a name="git"></a>
Version control is essential for code! We try to practice that as much as possible, mostly because we like to think of ourselves as decent humans (and computer scientists).

There are 2 big reasons for using version control, the first is obvious.
1. Easy versioning does make a big difference for a class! It's very helpful to mark items as happening for a specific semester or to know what things change from one semester to the next. A real VCS is more helpful than something like google docs in that regard.
2. VCS's like plain text and easy to update formats! Many of our resources get shared beyond the CS10 class. Using plain text (or Markdown or something) is generally much easier to automate and convert than say, a Google Doc.

##### Github
Of course, central to the VCS stuff is Github! First, Github for Education [INSERT LINK] is awesome and will give you free private repositories if you need to keep things locked down. However, mostly Github provides a safe way to collaborate on code that we write and a great place to share it with others.

Here's the features we use:

* Organizations:
    This is in a "CS10" organization. We use it as a central place where all staff members can find the projects they need and automatically have access to them. As staff come and go, the members list can be updated, but all the projects we use will have a consistent home.
* Github Pages
    GH-Pages are a very simple way to host static websites. We try to build gh-psges compatible versions of the websites we have which are a very useful backup in the event of a school server outage.
* Issue Tracking
    It's lightweight, and simple. Assign staff members tasks and use them to collaborate on anything. Unlike discussion over email, issues can be directly attached to and reference items in a repo which makes things a bit easier to follow.

##### Web Hooks
<a name="hooks"></a>

##### Barcode Scanner
* iClicker Check-Out
    * Cal Student IDs:
        * Code 39 Termination Char: Tab
* Lab Check-offs
    * Barcodes -- Code 39 Termination Char: None
    * We use hipchat
    
    