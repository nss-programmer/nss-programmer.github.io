---
layout: post
title: A short intro to Lagrange Multiplier 
---
In this article I will try my best to explain what exactly a **Lagrange Multiplier** means and how these multipliers play important role in solving some of the crucial optimization problems in the context of machine learning.

Before getting started with Lagrange multipliers lets understand **contour lines**. The better we understand contour lines, the more we can visualize whats happening with Lagrange multipliers.

A **contour** is a way to visualize a three-dimensional function in two dimensions. In such a representation of the function, for each point on a contour line, the function returns the same value. Lets consider the following three functions.

![_config.yml]({{ site.baseurl }}/images/contours1.png)

![_config.yml]({{ site.baseurl }}/images/contours2.png)

![_config.yml]({{ site.baseurl }}/images/contours3.png)

In all the above cases for each point on the contour line, the function returns the same value.

Now lets come back to our original discussion. Lets say we have an objective function **f(x,y)** which we need to maximize under a constraint of the form **g(x,y)=c**. Lets visualize this problem statement before we go deeper into our discussion.


![_config.yml]({{ site.baseurl }}/images/LANGRANGE1.png)

![_config.yml]({{ site.baseurl }}/images/LAGRANGE2.png)

At any point **(x,y)**, the gradient **∇f(x,y)** is a vector which tells us the direction in which we should move inorder to increase **f** as efficiently as possible. As long as we are moving in that direction we are certainly going to increase **f**. 

