---
layout: post
title: How to explain Logistic Regression to a novice 
---
First of all thanks to **David Cox** for popularizing such a dominating method for the analysis of binary data.

![_config.yml]({{ site.baseurl }}/images/logisticregression.png)

In case of linear regression, the dependent variable is a linear combination of the independent variables.

![_config.yml]({{ site.baseurl }}/images/linear_regression.jpg)

Logistic regression equation is just rewriting the linear regression equation with dependent variable enclosed in a **link function**.

![_config.yml]({{ site.baseurl }}/images/linear_regression_link.jpg)

In the above case, the link function is a **logit link function**.

The logit for a number p between 0 and 1 is given as below :

![_config.yml]({{ site.baseurl }}/images/logit.png)

The link function can be defined as **g(Y) = log( p(Y) / ( 1 - p(Y) ))**

Since the dependent variable **Y** is categorical, **p(Y)** is simply the probability of **Y** belonging to different classes.

## Why logit link function ?

The dependent variable **Y** in case of logistic regression is categorical. For simplicity lets assume it can take two values , either 0 or 1.

So its quite reasonable to be concerned about the probability of **Y** taking the value of either 0 or 1, i.e, **P(Y)** which must satisfy the following criteria

**0 <= P(Y) <= 1**

How can we determine the value of **P(Y)** so that it must  always be greater than or equal to zero and less than or equal to one.

The simplest way of doing this is **P(Y) = Z/(1+Z)** , where **Z** is a positive integer.

But rather than choosing just any positive integer as **Z** , we choose **Z = e^Y** for following reasons.

(i) Bounded between 0 and 1.<br>
(ii) Derivative can be easily calculated.<br>
(iii) It easily introduces non-linearity into the model.





