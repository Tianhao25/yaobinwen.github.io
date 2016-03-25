---
layout: draft
title: How os.system() Deals with Signals
date: 2016-03-25
comments: true
category: Draft
tags: system(), signals
description:

---

## The Problem

(TODO)

## Analysis

Python's os.system() calls C's system() function.

In glibc, C's ```system()``` function is an alias of ```do_system()``` function which is implemented with the calls to fork(), execl() and waitpid(), as shown in [its source code](http://code.metager.de/source/xref/gnu/glibc/sysdeps/posix/system.c).

The source code shows that the SIGINT and SIGQUIT are both ignored:
* ```Line 58```: A signal action ```sa``` is defined.
* ```Line 64```: ```sa```'s handler is assigned to [```SIG_IGN```](http://code.metager.de/source/xref/gnu/gcc/fixincludes/tests/base/sys/signal.h).
* ```Line 68 ~ 83```: Ignore the ```SIGINT``` and ```SIGQUIT```.

The lines in ```Line 115 ~ 119``` spawn a new child process. On the child side, the normal handling of ```SIGINT``` and ```SIGQUIT``` is restored, and then ```__execve()``` is called to run the specified program.

However, on the parent side, which is also the side which initiated the ```do_system()``` call, the handling of these two signals are not restored. Shortly, it calls the ```__waitpid()``` to wait for the completion of the just-spawned child process.

After the child process is completed, the normal signal handling is restored in the parent process, as shown in ```Line 157 ~ 171```.

## References

https://www.gnu.org/software/bash/manual/html_node/Signals.html
http://unix.stackexchange.com/questions/149741/why-is-sigint-not-propagated-to-child-process-when-sent-to-its-parent-process
http://www.cons.org/cracauer/sigint.html
http://www.vidarholen.net/contents/blog/?p=34
"what would happen behind when an interactive bash receives SIGINT"
