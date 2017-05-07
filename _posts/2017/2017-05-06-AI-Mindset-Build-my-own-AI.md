---
layout: post
title: AI Mindset Series of Build My Own AI
date: 2017-05-06
tags: artificial intelligence
category: [Tech, AI]
comments: true

---

> This is my GAME, NOT science or engineering.

Yes, this article is about a game of my own, not any kind of science or engineering. Building my own A.I. without much A.I. knowledge can't be anything but a personal interest. Today I spent almost the whole day skimming online documents, Wikipedia entries, and other people's talks or slides to get a basic idea of the artificial intelligence field. That's all what I have learned so far. However, the boundary of my current knowledge wouldn't stop me from trying to develop my own artificial intelligence.

In fact, there is another reason that supports me doing so: Trying to solve a problem before being exposed to a solution generally results in better learning, as mentioned in the book [_Make It Stick: The Science of Successful Learning_](https://www.amazon.com/Make-Stick-Science-Successful-Learning/dp/0674729013/ref=sr_1_1?ie=UTF8&qid=1494121685&sr=8-1&keywords=make+it+stick).

OK. I'll start.

My goal is to build an artificial intelligence that is able to acquire new knowledge by itself. Humans can train it in two ways: establish the initial base of knowledge; correct its wrong knowledge. I don't think the training here is the same as the training people do in machine learning. In machine learning, as far as I have learned (and my understanding could be wrong), the training in machine learning focuses on the correctness of the output. The training doesn't focus on helping the machine to build the truth within it. In other words, if the machine makes two negatives (wrong knowledge) a positive, we human trainers may not care about these "negatives". But in my own artificial intelligence, we human trainers focus on the knowledge building. The artificial intelligence comes to the results by itself and, although we humans can express our agree- or disagreement to the results, we can hardly do anything to force the artificial intelligence to give up the result unless we find the wrong knowledge and correct it.

Alan Turing suggested the four major components of artificial intelligence: **knowledge**, **reasoning**, **understanding of language**, and **learning**. I, here, revise these components as follows:

* **Knowledge** is the understanding of how the external environment works.
* **Feeling** is the sense or emotion aroused during the interaction between the artificial intelligence and the environment.
* **Reasoning** is the internal connection among the **concepts** in the knowledge and feelings. I'll talk about _concept_ later.
* **Learning** is the processing of building new knowledge, feelings and reasoning.
* **Goals** are the motives of the artificial intelligence to do a particular thing.

First of all, we need to decide how the **knowledge** is represented and acquired.

The artificial intelligence senses the external environment via **sensors**, and reacts via **actuators**. The sensors and actuators are the outer limits of how the artificial intelligence can understand and affect the external environment. This can be depicted as follows:

![Interaction](https://raw.githubusercontent.com/yaobinwen/yaobinwen.github.io/master/images/posts/2017/05-06/ai_interaction.png)

Sensors are the input; actuators are the output.

If we think in object-oriented methodology, then the external environment can be described as a huge collection of **objects** - **"Everything is an object."** says Java. Somehow, the artificial intelligence should be able to turn the objects from the environment into **concepts** that are maintained in the artificial intelligence's mind. A **concept** is quite like a **class** in an object-oriented programming language: it is the abstract description of all the objects that share the same traits. The **reasoning** happens on the concept level, but the reactions are performed on concrete objects by the actuators.

Here the key question is: How is a **concept** created without human intervention when the artificial intelligence is exposed to enough objects in the external environment?

I don't know how the creation happens. But one possible way is to let a human trainer establish the initial set of concepts, very similar to teaching a kid in an elementary school. As the artificial intelligence grasps more and more concepts, the new concepts may be able to get created spontaneously, without human intervention.

The next question is: Should reasoning be a built-in system that connects two concepts? If not, then how are two concepts connected in artificial intelligence's mind?

To answer the first question, we must define "reasoning". My quick and dirty definition is: reasoning is the capability of connecting two concepts by applying causality. So far as I think, I do believe the **capability of connecting two concepts** is a more fundamental and thus built-in system of an intelligence (like the conditioned reflex of Pavlov's dog). However, causality is not, thus reasoning is not, either, because connecting two concepts does not necessarily require these two concepts have causality, but connecting two concepts by reasoning requires the causality that lies behind the concepts that must be learned in order to be known. Because everything that must be learned should not be considered as part of the built-in system of the intelligence, reasoning is thus not a built-in part.

Then how the two concepts are connected? When observing human's behavior, I find that they seem to be connected by repeated **"remember"** and **"forget"**. Every time two objects are shown to a human, the objects are firstly translated into their corresponding concepts, and then the human connects them once and remembers the connection. However, this remembrance quickly erodes as time goes by, which is the process of **forget**. If the two objects - or the two concepts - are not shown to the human again within a certain length of period, the connection is completely forgotten. But if they are, the connection is strengthened and becomes harder to be forgotten (although still can be forgotten given long enough time). This seems to be how humans connect two concepts. Causality is just one particular way of understanding the connections.

All right... I do need to do more research to give my aforementioned "theory" a more solid foundation.

Here is a gap that I haven't got an idea of how to achieve it, but let's imagine that I have taught my artificial intelligence reasoning with causality, then there are the following types of connections between two concepts (where "p" is the probability of an event):

* C1 is C2
* C1 is not C2
* C1 definitely results in C2 (p = 1)
* C1 probably results in C2 (0 < p < 1)
* C1 does not result in C2 (p = 0)

The artificial intelligence's knowledge base is a set of concepts and their connections.

The human trainers can teach the artificial intelligence knowledge. If I finish building the infrastructure of this artificial intelligence, I can further develop a user interface that allows such human teaching to happen. For example:

* A human teacher is presented with a small number of questions, such as three, in every teaching session.
* The teacher is asked to either confirm the correctness or incorrectness of an existing piece of knowledge, or to help the artificial intelligence build new knowledge.
* If the teacher doesn't know the answer, he/she can skip the question.
* The question can be presented as a multiple-choice question: "C1 ___ C2. A). is; B). is not; C). results in (p=1); ..."
* Because the artificial intelligence's lexical parsing may not be perfect, the "C1" or "C2" in the question may have redundant elements. For example, the question may look like "the tornado of ___ rain on Tuesday". The teacher can modify the "C1" and "C2" parts to make them "tornado" and "rain".

This is so far what I have thought about building my own artificial intelligence.
