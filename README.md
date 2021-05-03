# Take Home Project
Congratulations on making it to this stage of the interview process with Higher Ground!

As you will see in the Project Description section, this take-home project is very open-ended. This is purposeful. You should approach it as a way to showcase both what you value in a codebase, and what you prioritize when solving messy, real world problems. You will have received some personalised notes via email on our expectations, but you should feel free to exceed or ignore them.

You should spend at most around one day's work on this project. **It is not required for you to hand back something fully implemented or perfect**, though we do expect you to have spent time thinking through the problem, and for any code you send us to be clean. We’d ideally like to be able to easily run your submission. 

In a follow up interview, we’ll spend some time discussing the goals you had, the decisions you made along the way, and the difficulties you encountered (if any!). If time allows, we may extend your project as part of a pairing exercise.

You are free to use any language you're most familar with (we use (java|type)script and python heavily).

***

# Project Description
In the `data` folder of this repository, you will find a number of `.csv` files. They contain data* exported from a number of third party tools (described below) which one of our newer schools uses to manage their teachers, students, and relationships with parents.

Right now, because data is inconsistently stored in multiple unconnected tools, a number of tasks (listed below) are exceedingly complicated, and require hours of manual effort.

**Your goal is to make the life of all involved better.** This can mean writing scripts to deal with the data as it exists, or building better tools for the input, management, and display of future data.

\* the data is fake, and semi-random. You may see some odd patterns.

### Data (and Tools) Description
The school uses **a CRM** (Customer Relationship Management) product to manage its relationship and communications with parents of enrolled students, and an **ERP** (Enterprise Resource Planning) tool to manage its teachers (including pay, assigned classes, and schedules). 

Individual teachers are tasked with keeping track of their class lists and student grades. They decided to use simple **spreadsheets** to manage both, which they keep updated manually.

`parents.csv`  is the export of the CRM. The data here is carefully inputted and checked by parents when they enroll, and as a result it is mostly free of errors or typos. In the `notes` column of this sheet, though, you will find a manually entered list of names. These are the names of enrolled children. If multiple parents in a family are on record, only one of them will have data in this field. The school uses the data in this field to decide who to contact about emergencies, events, and general news.

`classes.csv`, `students.csv`, `teachers.csv`  are all exports of the school's ERP. `classes.csv` is the list of scheduled classes during the week, `students.csv` is the up-to-date list of enrolled students, and `teachers.csv` is the list of teachers who work at the school. This data is generally well maintained and clean.

The `classes` and `grades` folders (and subdirectories) are all the spreadsheets which are manually managed by teachers. This data is the most inconsitently formatted, and the most likely to be out of date or badly entered. 

### School Tasks
At the start of the school year, and at several points throughout the school year, the following questions need to be answered:
* Are all the students assigned to classes?
* Are any teachers under-used? Are any over-used?
* Are any students double booked?
* Are we missing any contact information for any student?

Every week, the following lists need to be available:
* All students who have an average grade of D or below
	* All emails of the parents of the above students
* All parents of students in each year (i.e. all parents of students currently in year 1, all parents of students currently in year 2, etc.) for the weekly newsletter
* All classes where more than half of the students have had a D or below

Several times a day, each teacher has to ask themselves the following questions:
* Are all the students who are meant to be in this class here?
* Which students in my next class are struggling?
* What is my next class?
* Which students missed one (or multiple) tests?
