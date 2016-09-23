---
layout: draft
title: A Framework to Read and Understand Not-well Written Requirement Documents
date: 2016-09-22
comments: true

---

> This article discusses a possible framework to help the software developers read and understand requirement documents that are not-well written.

TODO:

* Define the problem.
* Define the goal.
* Describe the solution.

When working on a software development project, one kind of artifacts that we developers need to deal with are requirement documents. Because the requirements themselves could be potentially complex, the documents, even if the authors have already striven to write concisely, may end up being very large and full of information.

I also need to deal with such documents, and sometimes I feel pressured and directionless due to the overwhelming information, especially when there are many tiny requirements that are prone to being overlooked. In order to cope with such situation, I tried to develop a framework to help me grasp such complex documents better.

This framework is still in its early phase and I believe there will be a lot of work to be done to make it complete. Please feel free to leave me comments.

Basically, when reading the target document, I will focus on the following aspects in the document:

* Event triggers
* Data items
* Virtual resources
* Physical objects and hardware
* Human roles

An **event trigger** is a situation in which a particular event happens. For example:

* A specific time: "The system is scheduled to be restarted **at 00:00**."
* Another event: "The map will be updated accordingly **when a new street is built**."
* A human input: "A prompt message box is popped up **when the user clicks the confirmation button**."

These event triggers are important because they could potentially make the system react according to what has just happened.

A **data item** is a piece of information, large or small. For example:

* The number of a company's employee;
* The population of Pennsylvania;
* The sentence the user enters in the text box.

The data items are never physically touchable.

A **virtual resource** is a container that stores one or more data items. For example:

* A file system file or directory;
* A database table;
* A program or a running process.

These resources are _virtual_ because they are not physically touchable, either. However, these resources themselves are not data or information but a data container.

A **physical object or hardware** is a physically touchable object that stores or holds data items. For example:

* The map that you see from Google Map is considered as data, but a paper map that you buy from a bookstore is a physical object.
* The population of all the states in the U.S. is stored in a database table which is considered as a virtual resource, the laptop on which the database program is running is a piece of hardware.
* The files and directories that are stored in the hard drive are considered as virtual resources, but the hard drive itself is a piece of hardware.

A **human role** is the collection of human responsibilities. For example:

* A system administrator;
* A salesperson;
* A product owner in the Scrum process.

I do not expect to identify all of these in just one pass of the document. I'll just collect as many as possible.

Then I will use the workflows, which are sometimes written as use cases, to examine whether I have identified everything in these aspects. A workflow consists of one or more steps, and for every workflow and each step in it, I will ask the following questions:

* What triggers this workflow to happen? - Examine the event triggers as well as the human roles.
* What data item is input, processed or output in the current step? - Examine the data items.
* Where specifically is the data item is extracted from or stored to? - Examine the virtual resources, possibly also the physical objects.
