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
Hence the law is unchanged under rotations.

### Projections of X
Take any unit vector $u$. By rotation invariance, properties of u will be the same of properties of a basis vector $e_1$, since they are only separated by a rotation. Hence the distribution of <u, X> has to be the same as $<e_1, X> = X_1$. Hence we have found that $<u, X> \tilde N(0,1)$.

### Uniqueness of the Gaussian Rotation Invariance
Uniqueness arrises in the Gaussian from the i.i.d. property of the elements of $X$.
Assuming only the i.i.d. property, elements $X_i$ have a distribution $\mu$ which they all obey independently. Then the n-times product measure $\mu^n$ is the law of $X$.

### Generalisations: what is a rotation
I take "rotation" to mean a linear transformation which preserves distances. It is modeled by the $SO(n)$ group.

Taking the 

### Rotation Invariance in the sum

Taking the sum of gaussian random variables we obtain a gaussian random variable. We show how this is related to rotation invariance. If we let $v$ be the all-one vector,

$$\sum_{i=1}^n X_i = <v,X>