---
layout: draft
title: My Understanding of Software Engineering
date: 2016-03-12
comments: true
category: Draft
tags: software engineering
keywords: software engineering

---

# 我对软件工程的理解

这篇文章是对《名不副实的“软件工程”》(以下简称《名》)的读后感。我虽然毕业于美国某世界知名大学的软件工程专业，但并不专门为该专业说话，只是对《名》文中的观点说说自己的看法，有同意的有不同意的。欢迎讨论。

《名》文讲的是国内高校的软件工程专业和业界脱节的问题。这里我首先就有一些眼光的局限：
1. 我没有在国内读过软件工程专业，不熟悉国内软件工程专业的设置。
2. 虽然本科的时候学过《软件工程》这门课，但那是将近十几年前的事了，未必和现在的情况相符。

作者开篇对```软件工程```做了诠释：

    顾名思义，“软件工程”讲的应当是把软件开发出来的学问。所以，它是名不副实的：如果你按照
    “软件工程”教的去做，多半开发不出来软件，至少开发不出好的软件。

另外请注意：作者这里否定的```软件工程```特指```国内高校开设的软件工程专业或课程```，而不是一般化的软件工程这个领域所包含的知识和实践，因为作者下面也推荐了一些软件工程范畴的书并且认为很好的书，说明在这个领域其实还是有一些非常好的积累的。

接下来作者列举了一些在```国内```软件开发相关教材上共同出现过的主题，例如


---

说一下我的观点吧。国内软件工程专业的教学之所以会出现文章中所说的问题，在我看来一个很重要的原因是偏“工具主义”和“教条主义”。就像文章说的，软件开发确实是非常复杂且变数极多的一个领域，除了软件要解决的问题本身可能足够复杂之外，还有人的因素在里面。它可能具有的复杂度恐怕不是任何单一的方法论和工具可以解决的。比如，OOP是对世界的一种建模，有很广泛的应用，但并不是所有领域都使用OOP建模，所以才有函数式编程范式以及诸多种范式。另外，有些事情必须是在问题具有一定的规模、量变引起质变之后，某些方法才会适用，例如百万级用户访问量的网站服务器该如何搭建。而问题是：学校作为一种学术机构，在偏理论的领域很可能是领先业界的，但是恰恰在软件开发这个强实践的领域里，学校很可能不占优势。比如教材的编写肯定落后于一个技术大牛花一晚上写一篇技术博客，同时学校里的教学项目很可能也无法提供业界面临的真实问题那么大的规模。这样的问题在CMU的SE专业一样存在。CMU的SE专业和美国的软件工程研究所(SEI)有密切关系，而SEI有军方背景，他们做的很多软件都不是类似Google那种互联网的软件，所以他们研究出来的方法论(例如你们很快要学习的PSP和之前很火的CMMI)很可能不是那么很容易就应用到互联网行业。比如现在互联网行业非常流行的敏捷开发方法就不是SEI提出的。另外这边的老师们也难免有时代局限，他们以前的工作很多都是在非互联网时代完成的，所以和现在互联网企业中应用的方法肯定会有一些脱节和代沟。

中间漏了一点：我一开始说的“工具主义”和“教条主义”的意思是：现在的很多教学可能是教给学生某几种工具和某种方法论，并暗示软件都是这样开发的。这肯定是不行的，因为问题太多样了，领域也太多了，不是几种工具或一种方法论能cover住的。具体的工具和方法论在它们产生的背景和领域中一定有很大的用处，但出了这个背景和领域可能效能就打折扣了。就像是我们做数学推导，使用定理的时候必须注意前提条件一样。前提条件不具备，定理不能随便用。

所以即便在CMU，甚至CMU的软工号称世界最强，也还是有这个局限，你会发现老师讲的很多case都不是互联网的，或者一个case用一万遍。不过，我觉得这边的软件工程其实是在一个正确的方向上做教学的，就是说：不仅仅要学习具体的工具和方法论，还要学习如何根据具体的问题情形做决策。在CMU的SE专业里，你们一定会听到老师说一句话：You need to learn how to make judgment. 我认为是非常正确的。我认为，无论是企业级软件开发还是互联网软件，目前最强的“银弹”一定不是某种工具和方法论，而是思考方式。只有学会分析问题并根据具体问题的特性去制定解决方案和选择工具，才能以不变应万变。说得装逼点，就是“上升到哲学层次去考虑”。

其实我不是在批驳那篇文章，我认为他里面讲的问题很实在。我也不是想吹捧这边的专业如何好。只是两相比较下来，我觉得在CMU的软工教学方法其实更具长远的和普适的效果。但问题是：学生们在这里时间短，学习任务重(核心课和选修课都不轻松)，类似这种在我看来偏“哲学”的思维方式的建立不容易在一年或一年半的时间里建立起来，反而非常容易让人觉得很玄很虚不知所措，最后的感觉可能真的就是“这学了半天没用的东西找工作又用不上”。。[Grimace]

哦，对了，这篇文章的立足点主要是互联网企业，所以他的观点里说的软件工程教学和实践脱节，首先应该特指“和互联网企业的研发脱节”。但目前这个世界上不是所有的软件都是基于互联网思维构建的。比如特斯拉的车载软件，比如NASA航天器上的软件，比如银行的系统，比如Matlab，比如Adobe Reader、以及你们第一个学期在Models of Software Systems这门课上要使用的排版软件LeTeX。我不是说在这些其他方面没有脱节，只是提醒注意一下作者的立足点。另外，软件开发要处理人的因素，这个人不仅包括开发人员，也包括客户，其实也包括了组织文化和规章制度，因为制度是人顶出来的嘛。所以，某些软件研发模型和流程，可能仍然适用于某些项目的特点，不能说因为在互联网行业玩不转就全盘否定。比如，文章里有一个部分列出了一些软件工程教材的共同主题，并说“就我的调查，大多数人的答案是“没多大关系”。”。学过统计学的人应该首先询问一下这个调查到底是如何采样的，样本空间有多大，等等。我不是说不允许否定某些事情，我是认为否定的时候要尽量谨慎一些，注意否定所波及的范围。因为，我在CMU这边做的一个项目是带有科研背景的，我们的客户自己都还不是非常清楚下一步该怎么走，于是我们共同做了将近半个多学期的“可行性研究”，并且发现他们初始设置的目标不现实，于是及时调整项目方向，没有浪费更多的资源。所以我知道对于某些类型的项目，可行性研究是非常有用的。但是在互联网企业里，产品的研发可能的确需要用“短、频、快”的方式，有一些想法就立刻做出来投入市场检验，根据反馈再进一步调整，没有那么多时间做很多传统意义上的可行性研究(不过，我倒觉得这种快速的试错也是另一种形式的可行性研究，看你怎么定义了)。所以，你目力所见觉得没用的东西，可能只是你没有看到足够多的情形而已，并不保证它在普适意义上失去价值。

@周宇超 所以，回归到最初的问题上来。我首先认为软件工程是非常有用的，但确实教学方式需要改进。CMU这边的软工教学一定有自己的问题，但我认为他们教学的方式和培养的目标大体上是正确的(细一些的方面也有被我们吐槽很严重的，尤其是缺少互联网项目的案例这点上)。

# References
* [Software Engineering Methodologies](http://www.slideshare.net/DamianGordon1/software-engineering-methodologies)
* [Introduction to Software Engineering/Process/Methodology](https://en.wikibooks.org/wiki/Introduction_to_Software_Engineering/Process/Methodology)
* [Software Development Methodologies](http://www.itinfo.am/eng/software-development-methodologies/)
* [History of software engineering](https://en.wikipedia.org/wiki/History_of_software_engineering)
* [History of Software Engineering](https://www.dagstuhl.de/Reports/96/9635.pdf)
* [A Brief History of Software Engineering](http://people.inf.ethz.ch/wirth/Miscellaneous/IEEE-Annals.pdf)
* [Software Engineering: History](http://www.tandfencys.com/ese/Entry.pdf)
* [A Very Brief History of Software Engineering](https://www.vikingcodeschool.com/software-engineering-basics/a-brief-history-of-software-engineering)
* [Software engineering history](https://ifs.host.cs.st-andrews.ac.uk/Books/SE9/Web/History/)
* [Milestones in Software Engineering and Knowledge Engineering History: A Comparative Review](http://www.hindawi.com/journals/tswj/2014/692510/)
* [The result pages from Google](https://www.google.com/webhp?sourceid=chrome-instant&ion=1&espv=2&ie=UTF-8#q=software+engineering+history&start=0)
