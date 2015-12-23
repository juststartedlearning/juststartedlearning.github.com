---
layout: post
title:  "Some Basic definitions"
date:   2015-12-22 20:52:10 +0400
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
2. The inputs that influence the price of the house (or that we think influence it anyway) are called .. well, **inputs**. The symbol for those is \\(x\\) (and potentially, \\(x_1\\), \\(x_2\\), ...).
3. Our goal, in a supervised learning scenario is to come up with some sort of **relationship** (equation, not that other type you silly person) between the input(s) and the output. We'd then be able to use that relationship to predict the \\(y\\) from the \\(x\\)'s. This relationship is called a hypothesis, and is referenced by the symbol \\(h\\).

Let's talk abit more about point #3 above, about the hypothesis \\(h\\). Essentially, if the relationship is linear (Andrew promises to tell us later how to get the best possible fit, linear or otherwise), then the relationship takes the form of:

$$h = \theta_0 + \theta_1 x$$

This looks kinda similar to an equation I remember from school:

$$y = mx + c \text{ (or } y = c + mx)$$

That's the straight line formula, where \\(m\\) is the gradient/slope, \\(c\\) is the y-intercept and \\(x, y\\) are both coordinates of any point on the line. It's clear, just by comparing the two, that \\(\theta_0 = c\\) (the y-intercept) and \\(\theta_1 = m\\) (the gradient/slope). In general, we call these \\(\theta\\) things **parameters** of the hypothesis (so we don't have to call them *theta things* the whole time).

Now, for our purposes, we're not supposed to dig too deep into this just yet. Things get icky pretty quickly when you add multiple \\(x\\)'s, and higher order hypotheses (like quadratic equations, cubic equations, etc.).

Let's not worry about all that just yet .. and focus on getting this darn thing to work with the most basic case first.

### Training data
Like we said earlier, we'll be given a bunch of training data (which are really just \\((x, y)\\) pairs .. and later asked to predict the value of \\(y\\) when given \\(x\\).

Here's what a sample training data set might look like:

| Size in ft<sup>2</sup> | Price (x $1,000) |
|---------------|------------------|
| 2104          | 460              |
| 1416          | 232              |
| 1534          | 315              |
| ...           | ...              |

The total number of rows (or pairs) of training data is called \\(m\\), and we'll be using that a bunch of times in our calculations.
