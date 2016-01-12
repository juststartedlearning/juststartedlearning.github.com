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

Instead then, what we need to do is find a mathematical way to get the answers we need.

### The Concept

At the core of the gradient descent technique is a very simple idea. If we can take a starting point - any starting point - and then take a tiny step "downhill" (towards a point with a lower *cost*), then we'll eventually get to a pit .. somewhere where we can't descend any further without going back up. This point is known as the **local minima** and that's what we're aiming for.

The only question is: "how do we know which way is downhill?".

Well, that's where your old from high school - derivatives - come in. If you remember one thing about derivatives in school, it's that a derivative is that it's the slope at a given point (if you're completely lost, check out [this excellent introduction to derivates](https://www.khanacademy.org/math/differential-calculus/taking-derivatives/derivative-intro/v/calculus-derivatives-1)).

So all we need to do then is follow the derivative (the slope at a particular point), and it will give us a direction to move towards.

$$\theta_j := \theta_j - \alpha[\text{derivative of J}]$$

$$\theta_j := \theta_j - \alpha \frac{\partial}{\partial \theta_j} J(\theta_0, \theta_1)$$

### The code

Nothing drives a point home like seeing some code, and I really struggled to get my head around this whole vector business until I actually saw it implemented in traditional arrays.

<script src="https://gist.github.com/yazinsai/c898d488cb00413673df.js"></script>

You'll find the `data.csv` file [here](https://gist.github.com/yazinsai/a962de1d2efcf3aa4986).

**Note: I've used Python in the example above, but going forward most examples will be written using [Octave](http://www.wikiwand.com/en/GNU_Octave).**

Here's what the output looks like:

{% highlight shell %}
> $python gradient_descent_example.py
Starting gradient descent at theta_0 = 0, theta_1 = 0, error = 2782.55391724
Running...
After 1000 iterations theta_0 = 0.0590585566422, theta_1 = 1.47833132745, error = 56.3163353936
{% endhighlight %}

It took me a while to wrap my head around this, and to get the code to a working state. [Matt Nedrich's post](http://spin.atomicobject.com/2014/06/24/gradient-descent-linear-regression/) on the topic was very helpful.
