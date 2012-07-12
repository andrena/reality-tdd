---
layout: post
category : background
author: <a href="http://examinedcode.blogspot.com">Leif Frenzel</a>
title: The didactics of test-driven development
tagline: General background, part 1
tags : [introduction, approach, didactics]
---
{% include JB/setup %}

If you are like most software developers, you probably know how to do 
test-driven development (TDD). Perhaps you have learned it from a book, a
tutorial on the web, or at a 1&ndash;2 day course or workshop. And frankly,
there is not that much involved in picking up the basic idea: it's simple 
enough.

On the other hand, if you are one of those programmers who work test-first
(almost) _all the time_, you are most likely in a very small minority. If you
look around in real-world software projects, not many people do that. Some
people do it sometimes; but many, many don't do it at all. Here's the obvious
question: if it's that simple to learn, and so many people have in fact 
learned to do it, then why isn't it a much more common practice?


#### A natural approach

I confess to be one of those who have taught the kind of 1&ndash;2 day courses
I have mentioned above. At the time, the didactics of what I was doing seemed
obvious to me:

<ul>
  <li>explain the basic TDD cycle;</li>
  <li>create some very simple code examples, ideally from a domain everybody
  knows (such as the well known bank account classes that are a staple of
  such courses);</li>
  <li>let people practice the basic idea on these sandbox code bases.</li>
</ul>

As I said, it's not that complicated, and people got the idea quickly; most
of them worked their way through the exercises competently enough. Sadly,
though, with the practice of TDD it's a little as with marriage: the easy part
is the one that leads up to the big wedding event, the part that you can watch
and enjoy in a hundred Hollywood romances. The real challenge, though, lies
in what comes _after_, the bit that is never shown in those romantic comedies. 
Therefore, I want to invite you to take a deep breath and consider what comes
after the successful (and fun) workshop.


#### A frustrating story

We begin with a frustrating story: let's look at a hypothetical developer's
progress &mdash; call him _Meno_. Meno has just attended a two-day course
entitled "Getting started with TDD", last Thursday and Friday. After the
weekend, he returns to his everyday work on a software project. Still fully
motivated from the workshop, he fires up his development environment and grabs
his first development task for the week. Mindful of the TDD rules, he knows he
is supposed to write a test case now. But how? He does have a first vague idea
what to do (in the production code) in order to get off the ground with the
task. But what he has in mind are several smallish changes scattered over 
various modules in the code. There is no obvious way for Meno to see for
formulating a test case. (It was different with those simple, small examples
at the workshop.) For half an hour, Meno tinkers around, but nothing works 
out; the classes from the production code he has in mind can't even be simply
instantiated, much less made to work in isolation. So, as things stand, Meno
concludes that this task just happens to be an unfortunate choice for starting
with a test case. He proceeds (somewhat sadly) without one, and gets along well
enough; still he decides to give it another try tomorrow.

(Note at this point that what the story illustrates is not that it is 
impossible to write a test case in this situation &mdash; it's perfectly 
possible, but for the untrained eye, it's hard to see how it might be done.
That's the difficulty that confronts Meno here.)

Our friend makes a fresh start on Tuesday. Again he resolves to write a test
first and loads up his code base to go to work. Yet (unsurprisingly) he runs
into very similar complications again, and after a while he handles them the
same way as before: he puts off TDD and makes do without it. On Wednesday, he
is held up in meetings all day; but on Thursday, the game repeats itself. By
now it costs Meno some effort already to get himself to try as decidedly to
keep to the TDD rules. He's lost some trust already. (Not necessarily trust in
the TDD rules, but in his belief that they would fit his project's code base
as well as they seem to have worked for others elsewhere.)  On Friday, he
considers shortly, but then doesn't make another attempt at test-first coding.
He has now given up on TDD.


#### The least painful explanation

Most likely, what Meno will think is that the code base in his project is
somehow not a good fit for the TDD strategy. After all, it's a project with
a weighty proportion of GUI code, and he has already heard opinions that GUI
code is simply not testable with unit tests. (You could insert other technical
conditions here instead of GUIs: databases, file system access, web frontends,
hardware components, mobile devices, virtualized environments, ... There is
not much that hasn't been claimed to make unit tests impracticable at some
time or other.) Some pessimists will say that it is simply 'in the nature of
things'; some optimists will expect that at some point a clever technical
extension to the unit testing tool will come along that can resolve the
difficulty.

It's easy for Meno to fall for the illusion that his problem is basically
technical, and that in a few months he will get hold of an article in a 
Java developer's magazine about those latest JUnit features that will take
care of all your troubles. But of course they won't. (Don't get me wrong: it's
always good to keep up to speed with the latest technology. It's just that it
isn't the whole story, and in this case, it is positively misleading to rely
on technology as a solution for a problem that in fact isn't technical.)

But note that seeing things this way has the advantage to account for the
depressing experience in a way that makes it less painful. After all, Meno is
neither stupid nor lazy. He had been honestly motivated, and he's given it a
fair try. So if the fault wasn't in himself, where else is there to look? It
seems natural to locate the fault in the code, or perhaps in the technical
setup, of the project.


#### One working solution

But this can't be quite correct, as you can observe in those cases where there
is what we call a 'coach': someone with experience in unit testing and TDD, who
can guide you through the transition from toying with sandbox examples to 
applying what you learned there to your real-world code. It doesn't have to
be a consultant external to the team &mdash; the same function is often taken
over by an experienced team member. Important is that the coach is someone who
already _has_ developed the eye and has enough experience to gauge where to 
start in a given situation, and what to do. (It's also important that a coach
can tell situations that you can handle from situations which are too 
complicated yet and will overwhelm you. A good coach will take care to make
you stretch, but not overstrain yourself.)

What the coach involvement shows, then, is that TDD is far from impossible (or
prevented by 'the nature of things'). Evidently there _is_ a way to do it. 
Experienced TDDers have a sometimes surprising ability to find ways of devising
unit tests; they are also likely to remind you, just at the right time, to get
back to writing tests when you drift off into a pattern of changing the
production code without them. 

Well then, precisely what is different here from the earlier situation in which
Meno was on his own? Again, it seems natural to assume that it is simply 
something the coach _knows_, and then teaches to the beginner. But this would 
be a mistake. (Consider: if it was simply a question of knowing a few tricks, 
then waiting for the article in that developer's magazine would work; moreover,
these few tricks would have been a part of the two-day course already anyway. 
Also, one would assume the word had spread for a long time. Know-how on most 
technologies takes only a couple of months to get around. TDD has been with us
for more than a decade now.) 

The real solution lies not in what the coach _knows_, but in what he _does_.


#### Knowing vs. doing

Whenever you want to change something, it goes against your current habits,
and it costs some willpower to do something in a different way than you're
used to. Once you have established a habit, once it is the thing you usually 
do, then consumes virtually no energy &mdash; it's easy and doesn't exhaust
you. But until you're there, it means going uphill.<sup>1</sup>

Thus you can't start all at once, you need to build it up slowly. Moreover,
this works best if you have some moral support from someone who knows it can
be done, and who can steer you towards first small successes. (That's the role
a coach actually plays: it's not that the coach knows something you don't 
about testing technologies; what a coach does is to guide you on some first,
carefully chosen routes through the jungle until you're capable of traveling
alone.)

So the task you're facing is to develop a _habit_. However, compared to some
other typical habits (like toothbrushing, say), the habit of test-driven 
development is more challenging. In many situations it's not just a matter of
simply doing it regularly. That is what the Meno story demonstrates: many
real-world situations are neither good starting places nor easily tackled 
without some skill. For the approach that we recommend (the approach that we 
describe here on this site), this means two things. First, we need to provide
some _selection_ of real-world situations that are good places for starting to
get into the habit. Secondly, we must also look closer at the kind of skill 
that must be built in addition to the habit we want to develop. The skills and 
habits must be built up together.

In the second and third part of this introduction respectively, I'll discuss
the requisite skills in more detail, and then introduce the central metaphor
of our approach, _set-play_, and sketch how it addresses the task of building
test-driven development as a skill and habit.


_This post belongs to a three-part introduction to our approach. Read the
other parts here:_

*   _The didactics of test-driven development (this post)_ 
*   [_TDD as a skill and habit_](http://andrena.github.com/reality-tdd/background/2012/07/11/skills-and-habits/)
*   [_Set-piece play_](http://andrena.github.com/reality-tdd/background/2012/07/10/set-play/)

1 For a very readable introduction to recent research on willpower, 
see Roy F. Baumeister and John Tierney, _Willpower_, Penguin Press 2011.

<sub><sup>Copyright (c) 2012 by Leif Frenzel. All rights reserved.</sup></sub>