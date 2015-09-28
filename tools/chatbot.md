# Alonzo the Chatbot

Based of Github's idea of "Chat-Ops" we a bot named [Alonzo](github.com/cs10/Alonzo).

Alonzo is deployed on Heroku for free, and is a user each of our chatrooms. He's a simple nodeJS app, based on Github's [Hubot](github.com/github/hubot) framework. We've extended Hubot with integrations for bCourses, and Piazza and provides some custom commands for helping TA's do less work.

The goal of the chatbot is to find tasks which are tedious or error-prone, but relatively consistent that can be automated. Examples of this are doing lab checkoffs [link to process coming soon], or setting quiz passwords.

* Lab Check Offs
	* During lab we can check students off with our phones very quickly. This is quicker than directly using the Canvas / bCourses app.
	* We allow lab assistants to check off students, but definitely not access to the course gradebook! Whenever a lab assistant enters a check off score in HipChat it is saved for a TA to review before being placed in the grade book.
* Custom Commands
	* We have a few custom commands for easy to forget info. This makes it easy for anyone to quickly help themselves.
* bCourses (Canvas) Tooling:
	* because we already integrated with bCourses, it's easy to add additional tooling to automate student processes or grading info. We have "slip days" which students can use throughout the semester. However, students tended to lose track of them, so now we have a web page which handles this. Because Alonzo is really just a web server, we can use any custom logic to build a new place for students to check their  slip days. In this case, the bot is an API for our class website so that students don't need to go anywhere else.
		* [Bot code](https://github.com/cs10/Alonzo/blob/master/scripts/cs10-slipdays.js)
		* [Website code](https://github.com/cs10/sp15/blob/gh-pages/slipdays.html)