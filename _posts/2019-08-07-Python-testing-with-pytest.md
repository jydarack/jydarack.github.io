---
layout: post
title:  "Python testing with pytest (Bryan Okken)"
book_author: "Bryan Okken"
categories: reading
review_lang: en
---

Going through the book I bought after listening to the [Python Bytes podcast](https://pythonbytes.fm/). Perfect as it was topic I *had* to deal with in my current project at work.

Also a good occasion for me to practice correct formating, docstrings etc as I transition from working on small-medium scale data analytics projects running in Jupyter Notebooks to a more public setting where documentation and readability must prevail.

Reading status: **ongoing**

- [Chapter 1 : Getting started with pytest](#chapter-1--getting-started-with-pytest)
- [Chapter 2 : Writing Test Functions](#chapter-2--writing-test-functions)
- [Chapter 3 : pytest fixtures](#chapter-3--pytest-fixtures)
- [Appendix 1 : Virtual environments](#appendix-1--virtual-environments)
- [Appendix 2 : Pip](#appendix-2--pip)
- [Appendix 3 : Plugin sampler Pack](#appendix-3--plugin-sampler-pack)
- [Appendix 4 : Packaging and Distributing Python Project](#appendix-4--packaging-and-distributing-python-project)

## Chapter 1 : Getting started with pytest

So far, nothing new.

Need to get better at virtual environments.

## Chapter 2 : Writing Test Functions

First point: explanation of how to package a script is what I didn't know I was looking for. Part of what is not taught in Data Science curriculum (see notes on [Appendix 4](#appendix-4--packaging-and-distributing-python-project)).

Basic information about test functions. Testing if exceptions are raised (is it possible to test if exceptions are not raised? Seem to not catch if expression is caught in a try except clause.)

Need more practice with parametrize. What is more pythonic: using pytest.mark.parametrize or declaring variables in the test function? Learning along the way so my code is a mess.

## Chapter 3 : pytest fixtures

To be read

## Appendix 1 : Virtual environments

Hear about them too many times but never took the time to **actually** learn them. Never had to work with a package manager either (npm, composer).
Chapter goes throught the bare minimum but at least it covers what I need to know (and the difference between Win and Un*x)

## Appendix 2 : Pip

To Be Read

## Appendix 3 : Plugin sampler Pack

To Be Read

## Appendix 4 : Packaging and Distributing Python Project

How much I needed that !
Different infrastructures, what is need and where and so on. Perfect.

Following reading the chapter, I was looking for a way to automate the structure and settings. On Twitter, [Rodrigo Fuentealba](https://twitter.com/datasciencegems) mentionned [PyScaffold](https://pypi.org/project/PyScaffold/) and that was perfect. I have been playing with it locally and have just started a small development at work based on it. It covers all I wanted by I still need to dive into the settings and the various arguments to really understand what is possible. I currently understand 30-40% of what it does and that far too little for me to be satisfied.
