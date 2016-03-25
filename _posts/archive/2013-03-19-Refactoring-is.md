---
published: true
layout: post
date: "2013-03-19 23:35:13 +0200"
categories: archive
title: "Refactoring is ..."
---

In almost all projects I was involved as a developer it always a problem with the word refactoring. Every time when the “[REFACTORING][1]” word was heard there was an issue. Maybe it was not understood correctly, or it was overused. What is “[Refactoring][2]“, is a disciplined technique for restructuring an existing body of code, altering its internal structure without changing its external behavior.”

Some of the discussions at the planning ware like this:

Developer: We would like to have some time for refactoring in the next weeks.
Managers: What refactoring, we did it some time ago also…
Developer: But you know, we realized that this is not very nice implemented.
Managers: They passed the test…

And so on. Time after time, and right now, when I am more involved into architecture I would have had other arguments for refactoring. Some linked with learning, patterns, extensibility, maintainability, reuse and testability. Not only the basic ones like: you know, we did not understood it properly, it is to much code in one place, we need to have a class with this responsibility and so one and so forth.

Refactoring is good, in my opinion, because:

- the developers learn new, better, methods of fixing the problem;
- in the refactoring process the code will become more extensible and clean;
- the new features will be much more easy to implement;
- in the refactoring process almost every time there are patterns involved;
- the code will be easier an easier to work with, so +1 for maintainability;
- and I can add a lot more lines and you can find some more [here][3] too :)

The thing with all of this about improving and refactoring is that it needs to be made all the time. If you wait to do it at the end basically you will rewrite all the application. And it is a difference between making a feature better and refactoring a piece of code. Doing the feature should be approves and planed, refactoring should be part of the developing process, we should do it every time when is necessary and not end up in a situation like the one [Scott H][4] ended up with a long time ago.

Step by step is always good. But this is true, not only with code, also with processes, with creating the architecture, with refining the requirements. If you realize in the current step that the previous one should change also a little bit, do it now, because afterwords you will forget about it and it will remain the same till the end. And… At the end it will take double the time or more, to fix it and adopt it properly.

Ya… I know, you can say that if you will redo it every time,you will finish never ever, and yes, you need to realize when a thing is good enough. But, improving is always good.

Here is a nice quote about it:

<“Everything should be made as simple as
<
<possible, but no simpler” – Albert Einstein

But do not end up in this other one:

<“I have not failed -
<
<I’ve just found 10,000 ways that won’t work” –

<Ralph Waldo Emerson

Find just a middle way that works for you and keep in mind that improving is always good.


[1]:http://en.wikipedia.org/wiki/Code_refactoring
[2]:http://www.refactoring.com/
[3]:http://c2.com/cgi/wiki?ConstantRefactoringIsaGoodThing
[4]:http://www.hanselman.com/blog/AReminderOnThreeMultiTierLayerArchitectureDesignBroughtToYouByMyLateNightFrustrations.aspx
