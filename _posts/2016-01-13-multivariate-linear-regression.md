---
layout: post
title:  "Multivariate Linear Regression"
date:   2016-01-13 20:40:10 +0400
categories: machine-learning
excerpt: |
  Ah, now things start to get more complicated. We'd previously taken the most basic case where we only have one feature, and one output we're trying to predict -- with a linear relationship connecting them. Now, we start considering what happens when we have multiple features.
---

Here's the deal. So far, we'd only discussed the most basic possible example: a case where you had:

- a **single feature** (our \\(x\\), the area of the house)
- a **single output** (our \\(y\\), the price of the house)
- and a **linear relationship** between the two

Now, we're about to grow up .. because in the real world, we don't just have a single feature. We have many .. sometimes even thousands!

Think about it .. it sounds absolutely absurd that you would even think that it's possible to accurately predict the price of a house based on area alone! So many other things matter, like the number of rooms, the floors, the size of the garden, how old it is and it's sentimental value to you (actually, scratch that last one).

So that's what we'll be covering in this post .. how to consider a more complex prediction example.

Don't forget our goal .. we're still trying to come up with a hypothesis function that would allow us to accurately predict the price of the house, based on the inputs we're given.

Let's do this.

### Revisiting our (now broken) equations

We're going to have to go back and fix the equations we discussed earlier. The definitions (or rather, the meaning) of the equations won't change .. but we no longer have just one \\(x\\) to deal with.

First, **a few new definitions.**

Since we have many \\(x\\)'s now, let's give them subscripts (e.g. \\(x_1, x_2, x_3\\)) to refer to our different features.

We also need a way to refer to the total number of features we've got .. let's go ahead and call that \\(n\\).

Now that we have that out of the way, let's take a look at those equations .. starting with our hypothesis \\(h_0(x)\\):
