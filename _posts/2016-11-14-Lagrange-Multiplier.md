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

At any point **(x,y)**, the gradient **∇f(x,y)** is a vector which tells us the direction in which we should move inorder to increase **f** as efficiently as possible. As long as we are moving in that direction we are certainly going to increase **f**. This is the direction of steepest ascent. The gradient of any function evaluated at a particular point **(x,y)** always gives a vector perpendicular to the contour line passing through that point.

One thing we have to keep in mind that while climbing the hill we have to stay on the constraint curve **g(x,y)=c** all the time. In other words we are only allowed to move along the tangents to this constraint curve. Since these tangents are orthogonal to the gradient of the constraint function **g**, while moving along the constraint curve **g(x,y)=c** its value remain constant.

![_config.yml]({{ site.baseurl }}/images/LAGRANGE4.png)

While moving along the constraint curve **g(x,y)=c** we need to simultaneously observe how we move on the surface of **f**. If we are moving in a direction that has a non-trivial component along the gradient **∇f(x,y)**, we are still going to increase **f**. The moment we can only move in a direction orthogonal to the gradient **∇f(x,y)**, then we won't be able to increase **f** anymore. Here we have reached a local maximum. At this point the gradient of **f** and the gradient of **g** are pointing in the same direction. In other words, they are proportional. In other words, there is some constant **λ** such that the gradient of **f** is **λ** times the gradient of **g**. This **λ** is our **Lagrange Multiplier**.

![_config.yml]({{ site.baseurl }}/images/LAGRANGE3.png)

At point **A** the gradient of the function **f** to be maximized has a component along the direction we can move in. This is not the local maximum as we can increase **f** by moving to the right. At point **B** we can only move perpendicular to the gradient of **f**. Therefore this is the local maximum. 

The final equation is **∇f(x,y)=λ∇g(x,y)**

We can define a new function **L** as below:

**L(x,y,λ)=f(x,y)-λ(g(x,y)-c)**

We can call the function **L** as **Lagrange function**.

The final step is to gradient of **L** equal to the zero vector i.e, **∇L(x,y,λ)=0**

So our objective is to find the **critical points** of **L**.


