---
title: Geometric Compressed Sensing
subtitle: Understanding the landscape of exact recovery in Compressed Sensing
date: 2022-01-29T01:06:56.542Z
draft: false
featured: false
image:
  filename: featured
  focal_point: Smart
  preview_only: false
---
We will attempt to describe spaces in the exact recovery problem.

We are in $\mathbb{R}^n$, the signal space.

First define the prior space T, which may or may not be linear. Then we have a measurement matrix $A$, and an original unknown signal $x$.

Recovery is possible when the null space of the measurement matrix ker(A) and the prior-error space T-T are incompatible. We define two incompatible space as subspaces whose intersection contains only the zero vector.

Let us now introduce the error vector $h:= w - x$. $h$ is some vector in $\mathbb{R}^n$. If $w$ and $x$ have the same measurments, then the error vector is in the measurment-error space, ker(A). If $w$ is in T, then $h$ is in the prior-error space. Exact recovery is equivalent to the idea that the prior-error space and the measurment-error space are incompatible. Indeed, if there is a non-zero error vector in both of these spaces, than its associate signal $w$ satisfies all the information that we have about $x$. $w$ has then succesfully performed identity theft on $x$, and it is then impossible to recover $x$ with certainty.

Let us now specialise to the sparsity setting. T is then the r-sparse space, ${||x||_o \leq r}$. First notice that the prior-error space T-T is the 2r-sparse space. We need the measurement-error space to be incompatible with the prior-error space. We are interested in sufficient conditions for this previous statement. This means that we can take a capsule-space B containing the prior-error space T-T, and then showing that the measurement-error space is incompatible with the capsule space will be sufficient. Equivalently, we can capsule the measurement-error space, and if we prove incompatibility then we are done.

There are two important such capsule spaces: the almost-euclidean space.

If we are interested in recovery from l1 minimisation, we introduce the almost-sparse space S1, which we define with the support $S$ of x as ${||x_S||\_1 \geq ||x\_{S^c}||_1}$. This space is the set of all error vectors resulting form an l1 minimisation. Indeed, if $w$ is the result of an l1 minimisation program, then $||w||_1 \leq ||x||_1$, and the resulting error vector $h$ will be in the almost-sparse space (all the mass of x will be in S, and w has not enough to give to make the mass of $S^c$ bigger).

That exact recovery is possible stems from the prior-error space being incompatible with the measurment-error space. Similarly, the fact that this $x$ can be recovered with an l1 program stems from S1 being incompatible with the measurement-error space.

## Restricted Isometry Property

In the sense of sets, the results about this say that if the restricted Isometry Property holds for a matrix A, then the kernel of said matrix lies outside of S1. The proof of Vershinin takes an h assumed to be in S1 and also in the measurement-error space and finds a contradiction. This is done because we take h to be almost-sparse, and so through inequalities the isometry properties of A on sparse vectors can be applied to h almost-sparse also. Then Ah = 0 means that h = 0 by isometry property.