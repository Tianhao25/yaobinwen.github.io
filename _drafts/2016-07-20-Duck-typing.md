---
layout: draft
title: Thinking in Duck Typing
date: 2016-07-20
comments: true
category: Essay
tags: [duck-typing]
description: An essay of how to view, understand and code in a duck-typing way.

---

My serious study of "duck typing" all started from reading the Stack Overflow post: [Best way to check if a list is empty](http://stackoverflow.com/questions/53513/best-way-to-check-if-a-list-is-empty). In this post, basically, people are arguing each other about which solution is more pythonic:

    if not a:
        print "List is empty"

or

    if len(li) == 0:
        print 'the list is empty'

After reading many of the comments, I realize that most of the commentators who down vote the "implicit" solution may have a strong background of static typing, which means they might be thinking about the coding practice in a static-typing idiom. However, as one comment said, **"If you need to do type checking (which you rarely should in a well-designed duck-typed system), then that should be done explicitly."**(see the comment [here](http://stackoverflow.com/questions/53513/best-way-to-check-if-a-list-is-empty#comment27931884_53522))

This comment made me think: The reason that we favor the traditional

# References
* [Duck Typing Is More Than Quackery](http://haacked.com/archive/2014/01/04/duck-typing/): This is the first online article that I read about duck-typing understanding. It also listed some articles from another blog site: [What is “duck typing”?](https://ericlippert.com/2014/01/02/what-is-duck-typing/) which further references to an older post [Is C# a strongly typed or a weakly typed language?](https://ericlippert.com/2012/10/15/is-c-a-strongly-typed-or-a-weakly-typed-language/) that discusses **compile-time typing**, as well as a post [What is late binding?](https://ericlippert.com/2012/02/06/what-is-late-binding/) that discusses **run-time typing**.
* [Is Duck Typing a Type System, or a Way of Thinking?](http://johnatten.com/2014/01/04/is-duck-typing-a-type-system-or-a-way-of-thinking/)
