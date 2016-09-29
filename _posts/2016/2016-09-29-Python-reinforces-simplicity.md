---
layout: post
title: Python Reinforces Simplicity
date: 2016-09-29
comments: true

---

> Python reinforces code simplicity because you need to perform intensive testing on it to catch all the bugs.

I used to be a C++ programmer and kind of relied on the compiler and other static analysis tools such as [Coverity](https://www.coverity.com/) to find the potential run-time problems in the code. These tools can analyze the code in depth to find problems that are not easily caught by eyes thanks to the language static-typed nature.

Hence, I am having a (relatively) hard time when I started to program in Python, which is weak-typed. Although there are code static analysis tools, such as [pylint](https://www.pylint.org/), they cannot go that deep into the code to find as many potential issues as possible. Thus I sometimes end up in the situation that I run the code and get an exception thrown at me repeatedly only to find a stupid coding error because of careless overlook at something due to inexperience or code complexity.

However, today I suddenly realized what a good thing the lack of static analysis tools it is, for two reasons.

First, being a Python programmer, you therefore have to code with great care. Although I appreciate using various tools to help guarantee the code quality, I strongly believe the programmer's care is the first quality assurance measure regardless how many tools are available.

More importantly, Python forces the you **to write concise and less complex code**, because you need to make a good testing coverage, probably a full condition coverage at least, in order to guarantee code quality that's good enough. The testing workload could grow exponentially as you add more branches thus make the code more complex. Less complexity may help reduce the testing workload.

I think I love this programming language now, but I may also need to update the estimation for my current work.
