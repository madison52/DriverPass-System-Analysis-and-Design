# DriverPass System Analysis and Design

CS 255 portfolio submission by Madison Macachor

## What's in this repository

- **Business Requirements Document** (Project One): the requirements I collected from the client interview, along with the schedule and the assumptions and limitations of the system.
- **System Design Document** (Project Two): the UML diagrams and technical requirements for the system.

## Project summary

DriverPass is a new company owned by Liam. It wants to help students pass their driving test, since research showed that more than 65% of applicants fail because all they did was study old tests. Liam wanted a web based system that combines online classes and practice tests with on the road driving lessons. Customers can book, change, and cancel lessons online, or through the secretary, and the owner gets reports and a record of who changed what. My job as the systems analyst was to capture those needs in a business requirements document and then design the system with UML diagrams and technical requirements.

## What I did well

I read the interview closely and noticed what wasn't said. The registration information had no email address, even though customers need to reset their own passwords. Drivers leave comments after lessons, but they were never listed as users. The length of the in person lesson wasn't given. I wrote these up as assumptions and questions for the client instead of guessing. I also built the schedule from the dates in the interview and showed how each task depends on the one before it.

## What I would revise

I would revise the performance and security numbers. The client didn't set speed targets or a limit on failed logins, so I proposed some, such as pages loading in about three seconds and an account locking after five wrong passwords. Next time I'd go back to Liam and Ian with specific questions, like how fast is fast enough and how many failed tries are acceptable, and replace my proposals with numbers they agree to. I'd also compare every diagram against the others, line by line, so the names and steps match exactly. Small differences can confuse the developers who build from them.

## How I interpreted the user's needs

I started by listing each type of user (customers, the secretary, the owner, the IT officer, and drivers) and what each one needed to do. Then I tied each need to a requirement and a design choice. Liam's wish to know who made, canceled, or changed each reservation became an activity log entry that every reservation change records. Phone bookings became the secretary using the same reservation screens as customers. His request to turn off a package became an active flag, so a package can be disabled without affecting current customers. His request for offline access became online only changes with downloadable reports, because offline edits would create duplicate data. My instructor's question about the in person lesson led me to make Reservation a parent class with two types, since that lesson isn't a two hour driving session.

Users matter because the system exists for them. A system that works technically but doesn't fit how people do their jobs gets worked around or abandoned. Catching a misunderstanding in the design stage is much cheaper than finding it after the code is written.

## How I approach designing software

I start with the people and what they need, then map out the steps they follow, then identify the things the system keeps track of. In this project I used both a process view and an object view. The process view helped me confirm steps and reports with the client, and the object view gave developers a structure to build from. I explain the design differently for each audience, in plain language for the client and with more detail for developers. I also keep a running list of assumptions and open questions and update it as I learn more. In the future, I'd add early mockups so clients can react to something they can see, write user stories for each type of user, and tie test plans directly to the requirements so nothing gets missed.
