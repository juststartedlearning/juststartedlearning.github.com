---
layout: post
title:  "Gradient Descent"
date:   2015-12-24 17:52:10 +0400
categories: machine-learning
excerpt: |
  Gradient Descent is at the core of machine learning, and I've seen it mentioned in every single machine learning publication I've read. In this post, we'll cover what the heck it is and how it's used.
---

### Gradient Descent
So now we have a hypothesis function and we've got a way to measure how accurate it is. All we need now is a way to improve our hypothesis function, eventually finding the best possible \\(\theta_0, \theta_1\\) values (that minimize our cost).

That's where **gradient descent** comes in.

Imagine plotting our \\(\theta_0, \theta_1\\) parameters on the \\(x, y\\) axes .. and a 3 dimensional \\(y\\) axis showing the corresponding cost function \\(J(\theta_0, \theta_1)\\) for those \\(\theta_1, \theta_1\\) values.

Here's what that would look like:

![Cost function vs thetas](/assets/cost-function-vs-thetas.png)

What we're looking for is the point on the graph would the **lowest cost**, which would represent the pit in the center. That's the sweet spot.. and the values of \\(\theta_0\\) and \\(\theta_1\\) at that point are what we are looking for (to optimize our holy hypothesis function \\(h\\)).

Since plotting these pretty graphs is not always possible (imagine what it would look like if you had just 20 features instead of 1).
