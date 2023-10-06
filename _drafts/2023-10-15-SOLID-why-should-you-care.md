---
title: SOLID - Why should you care?
date: 2023-10-15
categories: [ SOLID series ]
tags: [ SOLID ]
image:
  path: /assets/posts/SOLID/SOLID.png
  alt: SOLID - Why should you care?
---

This is the first post in a solid series (pun intended) where I will try to convince you to keep reading and learning 
about SOLID principles.

SOLID Principles are broadly promoted around the industry. They were put together by Robert C. Martin a.k.a “Uncle Bob”, 
they are usually asked in software engineering interviews, and some companies go even further and ask you to apply them 
in your code base 😮 (could you believe the nerve of some companies …)


So… what is all the fuss about SOLID? Why should you care about learning them? Or even more importantly, why should you 
care about applying them to your code base?

In this series of posts, I will try to show all the benefits you get from applying SOLID to your code base and what 
problems can appear when you break them.

# The Basis
There are several properties desirable for a code base, of which I would like to highlight:

* Is desirable for a code base to be loosely coupled
* Is desirable for a code base to have a high cohesion
* Is desirable for a code base to be testable
* Is desirable for a code base to be simple

On top of all that, we could add **Is desirable for a code base to be clean**, but I won’t, simply because the condition 
of being clean for a code base is highly subjective, and we know, as engineers we only base our truth in hardcore math 
statements and not opinions … right? 😅

Even though, if you were paying attention, you may also think: “simplicity can be also subjective” … well … it is my post, 
so I will stick to my subjective truth 🤓

# Loose Coupling
It may be a good idea to refresh our memory by revisiting what coupling means, from Wikipedia:

Coupling is the degree of interdependence between software modules; a measure of how closely connected two routines or modules are; the strength of the relationships between modules.

They say “an image is worth a thousand words”, then let me try to represent coupling in images:


The green module is tightly coupled to the yellow module

The purple module is loosely coupled to the grey module

The red and blue modules are completely decoupled
What does coupling mean in practice?
Whenever we change the yellow module we more likely will need to change the green module in order to adapt to the changes made to yellow.

On the other hand, there are high chances that changes on the grey module do not impact at all the purple one (even though, some changes may impact it).

Finally, we can see that the red and blue modules are totally independent and then we can change them without any impact on the other module.

It becomes evident that the less coupled a code base is, the easier it becomes to modify, as the changes on one module won’t cascade to its dependants.

# High Cohesion
As before, let us go back and review cohesion’s definition, and just for the sake of consistency, let us make Wikipedia our source of truth 🤓:

Cohesion refers to the degree to which the elements inside a module belong together […] it is a measure of the strength of relationship between the methods and data of a class and some unifying purpose or concept served by that class.

Back to image representations:


Grey Module
Would you say that the elements of the grey Module “belong together”?

They may, all of them are geometric shapes, that condition can make this module cohesive.


Green Module
Would you say that the elements of the Green Module “belong together”?

All of them are also geometric shapes, and they additionally share the same colour: they are green 🐸!!

After seeing the Green module, you may have gone back and start thinking that the Grey module maybe wasn’t as cohesive as you originally thought.

It is important to notice that Cohesion only makes sense when evaluated against a context, a condition or relationship that makes our elements to “belong together”.

For example, if our relationship is “an element should be Green”, then we could add a frog to the Green Module and keep it cohesive.

The main advantage of a highly cohesive module is the reduction of complexity as the elements used to solve a particular problem (with a particular focus) are kept together.

High Cohesion also improves the maintainability of the system, when a change on a particular focused solution has to be implemented, the changes will impact a single module instead of changing code here and there across the whole system.

# Testability
Yet again, Wikipedia for the win:

Software testability is the degree to which a software artifact (i.e. a software system, software module, requirements- or design document) supports testing in a given test context. If the testability of the software artifact is high, then finding faults in the system (if it has any) by means of testing is easier.

There is not much more to add to what Wikipedia says...

Based on my experience, I could highlight that finding faults in the system becomes much more critical once you have a running systems and you want to ensure that your newly added feature did not break any pre-existing one (no regression introduced), then is when you can really appreciate a good covering and meaningful test suit 😍

# Simplicity
Programming is not about telling the computer what to do. Programming is the art of telling another human what the computer should do.

— Donald Knuth

It follows then that if you tell what your program should do in a simple way, chances are that more humans will understand it, with less effort.

If you can’t explain it simply, you don’t understand it well enough.

— Albert Einstein

More importantly, so you, yourself are able to understand it!

# SOLID
During this series I will try to showcase how applying SOLID principles will make your code loosely coupled, highly cohesive, testable and (more importantly? 🧐) simple!

Stay tuned for the next post where I will refresh your memory of the 5 SOLID principles: SOLID: The Cheatsheet
