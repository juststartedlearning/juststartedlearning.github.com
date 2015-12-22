---
layout: post
title:  "Some Basic definitions"
date:   2015-12-22 20:52:10 +0200
categories: machine-learning
excerpt: |
  Today, I learned a bunch of variable definitions that are used quite a bit
  when defining the kind of problem we're trying to solve with Machine Learning.
---

Here's what I learned today:

- The goal of supervised Machine Learning is to try to make **good guesses**, given the output of many previous guesses.
- How to translate problems from plains words to some juicy mathematics (oh joy!).

### Goal of supervised Machine Learning

Apparently, the entire purpose of supervised Machine Learning is to try and predict an output given (one or more) inputs.

### Some definitions
In the examples I followed, Andrew took the case of housing prices. His imaginary friend, James, wanted to sell his house and came to Andrew asking for advice. What he then did was look at a bunch of different factors (e.g size of the house) and the impact this had on the price of the house.

There's a couple of important definitions to note here:

1. The price of the house (what we're trying to estimate) is called the **output**, referred to by the symbol \(y\) (I can now write fancy math symbols, thanks to [Mr.Gaston Sanchez's post](http://gastonsanchez.com/blog/opinion/2014/02/16/Mathjax-with-jekyll.html) )
2. The inputs that influence the price of the house (or that we think influence it anyway) are called .. well, **inputs**. The symbol for those is \(x\) (and potentially, \(x1\), \(x2\), ...).
3. Our goal, in a supervised learning scenario is to come up with some sort of relationship (equation, not the other type you silly person) between the input(s) and the output. We'd then be able to use that relationship to predict the \(y\) from the \(x\)'s.
