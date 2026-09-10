---
title: Gaussian Rotation Invariance
subtitle: Exploring the different ways of approaching rotation invariance
date: 2022-01-12T01:23:55.209Z
draft: false
featured: false
image:
  filename: featured
  focal_point: Smart
  preview_only: false
---
A gaussian random vector in $R^n$ has its distribution unchanged under rotations. In this article we investigate how gaussian rotation invariance is special as well as how it can be understood logically.

We take a gaussian random vector $X$ in $\mathbb{R}^n$. X is defined to have $N(0,1)$ i.i.d. entries. Then we show that rotation invariance occurs.

# First

$$\sum_{i=1}^N$$

Rotation relies crucially on the fact that 

### Measure
The law of $X$ is $C e^{\frac{-r^2}{2}}r d\theta \times dr$. The law does not depend on the value of theta. The rotation transformation preserves:
- Value of r
- Change in r
- Change in $\theta$
Hence the law is unchanged under rotations. The choice of these coordinates is special because $r$ is the $l_2$ norm from the origin, and $\theta$ can be defined as the always-orthogonal coordinate of $r$. It measures the level curves of $r$ according to the lebesgue measure.

### $l_2$ norm
The measure is one-dimensionnal, it effectively exists only in r 

### Projections of X
Take any unit vector $u$. By rotation invariance, properties of u will be the same of properties of a basis vector $e_1$, since they are only separated by a rotation. Hence the distribution of <u, X> has to be the same as $<e_1, X> = X_1$. Hence we have found that $<u, X> \sim N(0,1)$.

### General $u$
What if $u$ is not normalised? Then there is a scalar $\alpha$ such that $\alpha u$ is normalised. Then $<u, X> = \frac{1}{\alpha} <\alpha u, X> \sim N(0,\frac{1}{\alpha^2})$. Notice that $\alpha = \frac{1}{||u||_2}$, and so $<u,X> \sim N(0, ||u||_2^2)$

### Uniqueness of the Gaussian Rotation Invariance
Uniqueness arrises in the Gaussian from the i.i.d. property of the elements of $X$.
Assuming only the i.i.d. property, elements $X_i$ have a distribution $\mu$ which they all obey independently. Then the n-times product measure $\mu^n$ is the law of $X$. We take the cdf $f_i(x)$ of the laws $\mu_i$. Then the cdf of $X$ at some coordinate point $x$ as $\{x_i\}$ is $f(x) = \prod_{i=1}^n f_i(x_i)$. This quantity can only depend on the radius of the point, meaning that any dependency on $x_i$ must go to compute the $l_2$ norm of $x$. The essential feature is that the $l_2$ norm is computed additively, but we have a product.
$$\prod_{i=1}^n \tilde f(x_i^2) = \tilde f(\sum_{i=1}^n x_i^2)$$
The only way for this to happen is for $\tilde f$ to be exponential. From this follows that we must have a gaussian.

### Generalisations: what is a rotation
I take "rotation" to mean a linear transformation which preserves distances. It is modeled by the $SO(n)$ group.

We can think of the fact that rotations exist as the fact that there are more degrees of freedom in $\mathbb{R}^n$ than there is associated with the euclidean metric. Rotations are both norm and distance preserving.

### Rotation Invariance in the sum

Taking the sum of gaussian random variables we obtain a gaussian random variable. We show how this is related to rotation invariance. If we let $v$ be the all-one vector,

$$\sum_{i=1}^n X_i = <v,X> \sim N(0, ||v||_2^2) = N(0, n)$$