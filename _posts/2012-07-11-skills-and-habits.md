---
layout: post
author: <a href="http://examinedcode.blogspot.com">Leif Frenzel</a>
category : introduction
tags : [introduction, approach, didactics]
---
{% include JB/setup %}

## TDD as a skill and habit

Our goal is to teach test-driven development (TDD) in a way so that it becomes
a programming habit, an integral part of how developers work on their software
projects.

This is an ambitious goal: it goes further than just getting the basic idea
across; and it is likely to require a re-thinking of the ways in which TDD
has been trained so far.


#### The target audience

In order to make TDD into an integral part of your daily coding practice, you
need to

* know what TDD is (understand the basic idea and the TDD cycle)
* know why you want to do it (understand the benefits of test-first programming)

TDD has been around for so long now that we simply assume these two conditions:
our target audience are those developers who have command of the basic ideas
(the TDD cycle, and how to use tools such as xUnit) and who are convinced 
enough of the benefits of test-driven development that they want to seriously
integrate it in their coding practice. 

The first applies probably to a large majority of programmers in the mainstream
object-oriented languages nowadays, and even if you happen to have no idea
about the basics of TDD yet, there are plenty of books and web tutorials around
where you can pick them up. The second may limit the audience a little more; 
not everybody may be as convinced of the positive value of test-driven
development as we are. If you're not, you may still be interested to hear
about our approach to establishing a development _practice_, because that 
approach may be applicable to other practices as well, possibly practices which
you take to be more worthwhile. (In fact, we are currently working on extending
this approach to another object-oriented development style, namely, code 
contracts.) 

So this is our intended audience: if you're a software developer with a basic
knowledge of TDD and some belief that it's a good thing to do it more often,
then this site may be of interest to you.


#### Success conditions

If this was what we simply assume, the tricky bit comes now &mdash; for in 
order to fully integrate TDD in your daily work, you need also

*   during your everyday coding work, in each concrete situation:
    * _remember_ that you want to write a test case first;
    * _know how to do it_ (given the real-world code base you are facing);
    * have enough time and acceptance in your team to do the extra amount of
      work that it takes.

If any of these conditions is not fulfilled, it won't happen, _even though_
you know the basic TDD cycle and _even though_ you are convinced of the 
advantages. It's simply that there has to be more than just that.

Let's break these three conditions down and look a little closer at them.

**1)** In every concrete coding situation you have to _remember_ that you want
to start with a test. Since you have presumably written software for years
already without necessarily writing test cases first (or without necessarily
writing them at all), this is not the first thing that will come to your mind.
What comes to your mind first is typically something else: most likely, it's
an implementation idea. That idea will probably pull you into doing an 
implementation sketch, one thing will lead to another, and you'll quickly end
up with some substantial portion of working code before you even start 
thinking about tests.

Of course, when you learned about TDD for the first time, you _resolved_ to do
it differently. You submitted to the rule that says not to touch production
code without a red test. You formed an intention to write your test cases 
first. But when you delved back into the daily coding routine, old habits 
swiftly kicked in and your resolutions were'nt on the forefront of your mind
for much longer. It's not that you didn't _want_ to do it. From within the
middle of things you simple often didn't _remember_.

The ability required here is called _prospective memory_ &mdash; it's a 
specific form of memory where you form an intention to recall something later,
and then in fact _do_ recall it. Here's an everyday example. In the morning
you tell yourself: "When I'm in town today for my lunch break, I must remember
to buy some flowers in the shop at the corner." Then you go off into your day.
With weak prospective memory, you will likely not remember (after your morning
commute, your first half workday, and your lunch break), and you'll walk by the
corner shop thinking of something else entirely, but not buying the flowers.
In the evening, when you find yourself without them, it will suddenly come
back. ("Damn, I forgot!") In contrast, if you have good prospective memory, 
when you stand up from your lunch table you will find yourself thinking: "Well,
and now I'll get those flowers." Needless to say, it's a capacity that is 
developed to a different degree in different people; but of course it is 
something that can be learned and deliberately improved with some training.

When you want to establish a new programming habit, such as test-driven 
development, then you need prospective memory. Most of your typical everyday
coding situations will be just like hundreds have been before, and you'll most
likely fall into old working habits just like a hundred times before. Therefore
it is an essential first condition for effecting any change that you learn to
reliably _remember_ that (and when) you want to do something differently.

**2)** But even if you _do_ remember, in a given everyday situation when you 
are working on the code base of your project, that alone won't be enough. You
also need to _know how to proceed_ in that particular situation. What is the
strategy for finding good unit test cases here? How do I deal with complicated,
obscure, and seemingly untestable code constructs? (The real world is full of
those!) Unless you have a very good idea how to proceed, writing a test case 
will appear to be harder and more effortful than just changing the production
code.

Note that this is not about the unit testing tool itself. Books about TDD often
stress that "writing tests must be easy, or else you won't be motivated to do
it." That's true, and if JUnit (for instance) would be difficult in its use,
unwieldy in its syntax, or badly integrated in popular IDEs, then everybody's
motivation to try out TDD would come to a quick death. But the simplicity of
the tool is only part of the story. (I have already noted that most
programmers easily learn the basics, which means that it works well enough as
far as _that_ goes. And yet many of those still don't make a daily habit out 
of it.)

When you are in a real-world situation, facing a real-world software system, 
it is often difficult and takes some experience to 'see' how a test case for a
given code passage might look like. You need to develop an eye for these kinds
of situations. Here's another everyday example: an experienced chess player
doesn't go through all the possible moves by all the pieces on the board, in a
given position. She doesn't need to. The good moves are highly apparent, they 
rather stand out. And it won't be just single moves. She will probably easily
discern entire chains of moves, counter moves, and responses to the counter
moves; she will see at a single glance one or two promising strategies she 
could employ given this position. (Have you ever met a person who looked at a
chess board for a few seconds and simply remarked: "Checkmate in three moves"?
That's the kind of skill I mean.) With an untrained eye, you won't be able to
distinguish good and bad moves easily, often you won't even see all
the _possible_ moves. With a well-trained eye, on the other hand, you can
filter out all the unhelpful moves and focus on the few worth thinking about.

![Chessboard, by Anna Langova](http://andrena.github.com/reality-tdd/assets/images/2012-07-11-chessboard.jpg "Chessboard, by Anna Langova")

It's similar with code bases. For the untrained eye (unexperienced in writing
unit tests in a realistic scenario) almost every piece of code that wasn't
developed already against unit tests will look untestable. Only with training
you will get to the point where you can quickly 'see' what a fruitful testing
approach would look like.

Therefore, the ease of finding a way to unit-test some code doesn't merely
come from the tool you use, and how easy _it_ (the tool) makes it to
write tests. It depends much more on your experience in finding ways to test
_the code base_.

To summarize, then: in addition to _remembering_ that you want to write
a test, in a given situation, you also have to _know how to do it_. You
need good prospective memory, and you need an eye for finding test cases.

In the approach that we have developed, we focus on exactly those skills. I
have written in my post on the didactics of TDD (TODO link) that you need to
start slow and develop a habit. But you have to develop it facing a
_realistic code base_, in order to develop the eye for finding test cases. You
start with recognizing certain situations, and then train to find test cases. 
This works especially well because these situations are comparatively easy to
recognize and there is an already proven strategy: that's why we call working
with these situations 
[_set-piece play_](http://andrena.github.com/reality-tdd/introduction/2012/07/10/set-play/). 
Once you have learned to recognize and handle set-piece situations, you just
have to integrate them in your daily habits, all along training your 
prospective memory (for which you can use the catalog of set-piece situations
again). That's our approach in a nutshell.

**3)** There is a third condition that must be fulfilled: even when you 
remember to write a test case, and when you know how to do it, you must be 
free to do so. If your project doesn't allow it because you don't get the time
or your team mates won't accept it, then you can't work in a test-driven way.

This third condition depends mostly on how the software development process 
in your project works, and this is not a topic for this blog. If you are using
Scrum in your project, then one place to discuss a lack of time or acceptance
for test-driven development would be the sprint retrospectives. Obviously,
the extra amount of time needed for programming tasks done with TDD must be
taken into account when your team does its sprint planning. On the positive
side, an agile process such as Scrum will provide a good framework to keep
TDD as a habit alive &mdash; your team might set up small reminders to write
unit tests on task cards, or it might help to mention it at the Daily Scrum
when a stretch of test-first coding worked particularly well. As always, it's
not just a question of how much your process and environment is there to 
support you, but also how well _you_ engage them and work with, and not 
against them. 

_This post belongs to a three-part introduction to our approach. Read the
other parts here:_

*   _The didactics of test-driven development_ 
*   _TDD as a skill and habit (this post)_
*   [_Set-piece play_](http://andrena.github.com/reality-tdd/introduction/2012/07/10/set-play/)

_Note that this is a draft and might still change a little in the near future._

<sub><sup>Copyright (c) 2012 by Leif Frenzel. All rights reserved.</sup></sub>