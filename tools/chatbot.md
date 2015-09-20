# Alonzo the Chatbot

Based of Github's idea of "Chat-Ops" we have our own instance of [Hubot](github.com/github/hubot), called [Alonzo](github.com/cs10/Alonzo). Alonzo is deployed on Heroku for free, and is a user in the chat room. He's a simple nodeJS app which integrates with bCourses and provides some custom commands for helping TA's do less work.

* Lab Check Offs
	* During lab we can check students off with our phones very quickly. This is quicker than directly using the Canvas / bCourses app.
	* We allow lab assistants to check off students, but definitely not access to the course gradebook! Whenever a lab assistant enters a check off score in HipChat it is saved for a TA to review before being placed in the grade book.
* Custom Commands
	* We have a few custom commands for easy to forget info. This makes it easy for anyone to quickly help themselves.
* bCourses (Canvas) Tooling:
	* because we already integrated with bCourses, it's easy to add additional tooling to automate student processes or grading info. We have "slip days" which students can use throughout the semester. However, students tended to lose track of them, so now we have a web page which handles this. Because Alonzo is really just a web server, we can use any custom logic to build a new place for students to check their  slip days. In this case, the bot is an API for our class website so that students don't need to go anywhere else.
		* [Bot code](https://github.com/cs10/Alonzo/blob/master/scripts/cs10-slipdays.js)
		* [Website code](https://github.com/cs10/sp15/blob/gh-pages/slipdays.html)