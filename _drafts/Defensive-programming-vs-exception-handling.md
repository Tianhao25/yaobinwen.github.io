---
layout: draft
title: Defensive Programming vs Exception Handling
date: 2016-02-19
comments: true
category: Draft
tags: exception
description:

---

The links for this topic:
* [Exceptions vs. status returns](http://nedbatchelder.com/text/exceptions-vs-status.html)
* [Error codes vs exceptions: critical code vs typical code](http://yosefk.com/blog/error-codes-vs-exceptions-critical-code-vs-typical-code.html)
* Exception specification in Python:
  * [How Can I Find a List of All Exceptions That a Given Library Function Throws in Python?](http://stackoverflow.com/questions/2843112/how-can-i-find-a-list-of-all-exceptions-that-a-given-library-function-throws-in)
  * [Python: How can I know which exceptions might be thrown from a method call]( http://stackoverflow.com/questions/1591319/python-how-can-i-know-which-exceptions-might-be-thrown-from-a-method-call)
  * [Defensive Programming vs Exception Handling?](http://programmers.stackexchange.com/questions/139171/defensive-programming-vs-exception-handling)
* [Idioms and Anti-Idioms in Python](https://docs.python.org/2/howto/doanddont.html)
* [Write Cleaner Python: Use Exceptions](https://www.jeffknupp.com/blog/2013/02/06/write-cleaner-python-use-exceptions/)


My key points:
* If you don't know what exceptions to catch, you don't know enough about your program's scope of responsibilities. In other words, you don't know what you can do and what you can't.
