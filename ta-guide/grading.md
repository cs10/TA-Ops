# Grades and How To Make Them Suck Less

__Note__: This is a public doc and doesn't include any info about secret sauce nor any special policies for CS10's grade calculations.

## A Word About Grading
> Or, "Why You Should Stop Reading Now"

If you can afford to not grade something: **DON'T**. Instead give personal feedback. That's basically how we feel. However, grades are a necessary part of the course, so the goal is to make them as useful and friendly as possible.

### Goals
Before we begin, know that it's possible to design a grading scheme which emphasizes any aspects you wish. Instructors have freedom in the scales they choose, the curves that are applied and the tasks that are evaluated. When you create a grading system, you get to choose what a "90" or "√+" or whatever measures you use will mean. However, you also have to consider that grades don't exist in a vacuum. _If a grade ends up on a transcript, you must consider how those grades will be interpreted by others (students, parents, faculty, etc)._

The goal is to create a system that students will not have to worry about interpreting -- that they will have the context for their grade to provide a feedback about their performance and track record in the course. Grades _must_ also come with some qualitative feedback. (Do check out the [Gradescope section][gs] for thoughts on rubric design.)

[gs]: ../tools/gradescope.md

## Creating a System
TODO

- giving credit for hard work (labs)
- Balancing stress vs motivation and de-motivation
- find some research to back this all  up?

## Computing Grades: High-Level Notes

Most of the grading is done through modifying spreadsheets and combining data using traditional Excel formula fields. There are no standard grader scripts like there are in some courses because the processes is ever so slightly different each semester.

I've specifically chosen not to automate the entirely of the process because I get comfort in knowing that I have seen every student's grade and manually reviewed the vast majority of the many data points to make sure things seem in-line. However, for the future there is room to automate some of the steps I'm going to outline, and that wouldn't be a bad process to use.

Spreadsheets are an _excellent_ tool for this job, because like Snap<i>!</i>, they are incredibly interactive. Changing one formula can instantly upload an entire range of values. Plus, it's incredibly easy to make use of throwing in additional cells for things like averages, standard deviations, min/max, etc.

The basic process goes like this:

* Use a "master" grades workbook with many different sheets or columns. (Dan Garcia has a slightly different setup from what's described here but you can get his template from him.)
* Get the grades settled in bCourses.
	The means making sure that things like Gradescope scores are uploaded.
* Keep track of special case scores throughout the whole process!
	Incomplete grades, auditors, etc.
* Settle the Grades by each type of grade "category"
	* In CS10, the raw score is pretty much a sum of the individual assignments, and this is true within a category, but each type (like Reading Quizzes or Exams) has special rules like drop scores or the clobber policy.
	* Start with the simplest groupings of assignments (RQs, HW, etc) then do the more complex ones. Think of the final grade as a sum of 5-6 partial scores so that you're focusing on data which is easier to see in one computer-screen-full.
	* Handle Extra Credit, and person-specific adjustments last.
		They're the most time consuming because the tweaking can never end. :-) Do make sure to spend time here as this is why humans are involved in the process.

## Move this stuff to tools!
## Useful Spreadsheet Features
I'm going to assume that the reader has some knowledge of spreadsheet tools for these notes, as there are better guides online. However, this section should outline some of the basic tools I've come to rely on.

These should apply to Google Sheets, Excel, and Apple Numbers as well as most other apps. Numbers is particularly good at making things pretty, which always makes grading more pleasurable...

* Conditionally Colored Cells
	Use these to highlight points as data change. I will use it for certain categories of grades (Like As, Bs, Cs get a color), or to highlight students with negative score grades, or anything that might deserve special attention.
* Different Font Sizes
	This is stupidly simple, but a key reason for spreadsheets. Make the most important info super easy to read!
* `INDIRECT()` Formula
	This allows you to turn text into a reference to another cell / sheet
* `ROW()`
	Reference the current row, and can be used with the above very conveniently.
* `$` anchors.
	This anchors a column or row reference in a formula field so it doesn't change when doing a C&P between cells.
* `!` sheet references
	You can reference a cell (A1, etc.)in another sheet (say "bcourses") by using the following formula `=bcourses!A1`
* `:` function
	This allows you to reference a range of cells, for example `A1:A10`, are the cells in rows 1-10 in column A.


## The Process
Note, some of this setup exists in Michael's template sheet in Google Drive. Dan's sheet is slightly different by will function the same way. (This process is standard advice but the specific sheets will need to be obtained from a previous semester, since they almost always have grading data.)

* Get an export of all the raw student grades from bCourses as a CSV file that can be dumped in Excel.
* Start reviewing this sheet, but __don't__ modify it! You may need to adjust grades in bCourses as you finalize things, and you want to be able to easily drop in a new replacement copy.
* In the master sheet, use a _reference_ to cells in the bCourses sheet. Do this for everything from the student name to assignment scores.
* Setup the standard header rows.
	If you're using the bCourses data as a separate sheet, it's very handy to have the master sheet as well as the raw data have the same number of "header" rows so that Student 1 starts in the same row in each sheet. It's actually quite easy to manage if they're off by a row, but it's easier to very your formulas are correct if numbers are the same!
	Traditionally, the raw bCourses export has _3_ header rows.
* Create a row for the first student
	Only do the first student.
* Create columns for each category of assignment. (RQ, HW, Exams)
* Create some columns for the different totals you may want to visualize.
	W/ and w/o extra credit, GPA w/ and w/o P/NP status, etc.
* For each category of assignment:
	Add columns as necessary for that assignment category, but you might not need to! (Fewer columns is better!)
	For example, the grades for reading quizzes can usually be easily calculated in one function that's a `SUM() - SMALL()` over a range of grades. (`SMALL` is just like the `min()` function for dropping the lowest score.)
	_Future Notes_: This would be one place where automating the process of grouping by category could be done fairly easily and would potentially save some time.
	At this stage, I also like to spend some time viewing the grade statistics for each assignment / category just to get a better measure of how things were going. (Ideally, this is also done throughout the semester.)