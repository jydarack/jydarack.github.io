---
layout: post
title:  "The Pragmatic Programmer (Andrew Hunt, David Thomas)"
book_author: "Andrew Hunt, David Thomas"
categories: reading
review_lang: en
---

Hear a ***LOT*** about this book so I bought it during one of my recent haul. A new version is supposed to come out at the end of 2019 but, too late for me. So yes, I am reading the 2000 edition, and that will be fun to read.

- [Chapter 1: A pragmatic philosophy](#chapter-1-a-pragmatic-philosophy)
  - [The Cat ate my source code](#the-cat-ate-my-source-code)
  - [Software entropy](#software-entropy)
  - [Stone soup and Boiled frogs](#stone-soup-and-boiled-frogs)
  - [Good enough software](#good-enough-software)
  - [Your knowledge portfolio](#your-knowledge-portfolio)
  - [Communicate](#communicate)
- [Chapter 2: A Pragmatic Approach](#chapter-2-a-pragmatic-approach)
  - [The evil of duplication](#the-evil-of-duplication)
  - [Orthogonality](#orthogonality)
  - [Reversability](#reversability)
  - [Tracer bullet](#tracer-bullet)
  - [Prototypes and Post-it Notes](#prototypes-and-post-it-notes)
  - [Domain Language](#domain-language)

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

> Nothing is forever - and if you rely heavily on some fact, you can almost guarantee that it will change.

[CORBA](https://www.techopedia.com/definition/1293/common-object-request-broker-architecture-corba) architecture comes back quite often. Concept is pretty clear but need to see real case example. Same with the n-tier architecture.

Beyond the personal comments above, the key message would be that rather than design with an architecture in mind, design with an architecture *knowing it will change sometime in the future*. So need to take this incertitude into the way you approach the problem.

### Tracer bullet

If I understand correctly, Tracer bullet code is some kind of MVP containing end-to-end logic, allowing to adjust and make sure that we reach the requirements. If OK, we can progressively meat-up the code with all the functionalities.

Reading further, I know understand that tracer code is similar to a complete process in Quality Management. Independant code blocks aka modules are independant activities, developped in *silos*. Tracer codes aims at building a first iteration of the whole process and **then** focusing and optimizing locally in each module. This is also code which will continue to serve as the backbone of future development.

Another benefit is that it is a good commnication medium from the early stages.

It's also an integration platform to deploy code bit by bit instead of GoLive. As much as I like this, I wonder how it fits into real life projects. Need to maintain business service while increasing covering and no disruption. So far, I understand how this would work for a brand new project but less with a running DB or running application. Or maybe it's because my current client DB management is not really tip-top.

Interesting precision: Tracer code vs Prototyping.

- Tracer code: end-to-end system, code is kept
- Prototyping: specific aspect of the whole system, code is scraped after demonstration.

> Think of *prototyping* as the reconnaissance and intelligence gathering that takes place before a single *tracer bullet* is fired.

Very clear to be explained this way.

### Prototypes and Post-it Notes

Prototyping = managing risks / managing the unknown and learning in the process.

Prototyping is meant to be rough. Can ignore:

- correctness (= use dummy data)
- completeness
- robustness
- style

Prototyping architecture can be done with non-functional code or on a blackboard. For reference, here are some of the element of the architecture which require attention:

> - responsibilities of the major components
> - collaborations between the components
> - coupling minimized
> - identify source of duplication
> - interface definition and constraints acceptable ?
> - *does each module have access to the data it needs, when it needs it?*

Make clear prototyping is just investigation and not a brick of the finalised code. If pressure or culture or environment seem to be pushing toward using the prototype code in production, go with tracer code instead.

### Domain Language

A word on the citation opening the chapter:

> The limit of language are the limits of one's world. (Ludzig Wittgenstein)

As a French guy living in Japan and communicating quite a lot in English, I love this quote.
