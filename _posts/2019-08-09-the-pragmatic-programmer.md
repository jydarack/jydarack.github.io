---
layout: post
title:  "The Pragmatic Programmer (Andrew Hunt, David Thomas)"
categories: reading
---

Hear a ***LOT*** about this book so I bought it during one of my recent haul. A new version is supposed to come out at the end of 2019 but, too late for me. So yes, I am reading the 2000 edition, and that will be fun to read.

## Chapter 1: A pragmatic philosophy

### The Cat ate my source code

This one reads like a chapter of the Zen of Motorcycle repair. Taking responsibility, being involved in the code and not just an observer.

### Software entropy

Things will go bad. Be ready to act before they go bad and play on top of each other. Coming from a railway maintenance engineering background, this speaks to me.
So far, take responsibility and manage your code as a *bon père de famille*

### Stone soup and Boiled frogs

Oh, how I hate these two examples.

### Good enough software

Starting with an old joke about japanese manufacturing, my neighbours won't be happy. Other than that, Good Enough is MVP before MVP was born. In a way, I like to read these older books just to find these concept which resurface now and then as revolutionary... As revolutionary as the last time. Don't get me started on cashless.

Involve your users in the trade-off + Know when to stop = start with the end in mind. A formalised deliverable.

### Your knowledge portfolio

OK, agreed with this one. Need to continue learning. Been pretty consistant on this part for the last 6 years

### Communicate

Sure. I know. And I suck at it.

## Chapter 2: A Pragmatic Approach

### The evil of duplication

No project / production / maintenance mode, programmins is being *always* in maintenance mode. Requirements keep evolving etc.

> [...] means that we spend a large part of our time in maintenance mode, reorganizing and reexpressing the knowledge in our systems.

I like this way of presenting code as cristalized knowledge and / representation of information.

Here comes DRY.

Sources of duplication:

- Imposed duplication
- Inadvertent duplication
- Impatient duplication
- Interdeveloper duplication

Duplication in Code is something I have hard time to understand, mostly because I have no idea what is good documentation *in* code.

Think about implementation / architecture before rushing to code. Think about what can be reused. Better: think about packaging the code for later use in other project (think Python's package, Ruby's gem, R's libraries). Make them available *and* communicate.

### Orthogonality

I knew the mathematical definition of orthogonality but first time seen in a code or system design context. Makes sense for modularity.
Doesn't seem to be even considered in the JavaScript world.
The point about orthogonality in project teams was my biggest problem for the first 3 months in my current gig. Huge overlaps with existing members and no responsibilities.

Need to go deeper into software architecture (layers etc). Rarely went beyond simple script (or django app) so this is brand new to me. Added to my "To investigate" list.

> Don't rely on the properties of things you can't control

### Reversability

To be continued
