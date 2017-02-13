---
layout: post
title: How to Fix _Package is in a very bad inconsistent state_ Error?
date: 2017-02-13
tags: [dpkg][inconsistent]
category: [Tech]
comments: true

---

Today I encountered the following problem when trying to install a piece of software:

> dpkg: error processing package libjpeg62:amd64 (--configure): <br />
 package is in a very bad inconsistent state; you should <br />
 reinstall it before attempting configuration <br />
Errors were encountered while processing: <br />
 libjpeg62:amd64 <br />
E: Sub-process /usr/bin/dpkg returned an error code (1) <br />

See [this answer to the post](http://askubuntu.com/a/170808/514711) for the solution. Basically, I need to remove the reinstallation request first and then try to install the package again to solve the problem.
