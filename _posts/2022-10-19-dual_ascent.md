---
layout: single
title: "Dual Ascent"
categories:
 - Algorithm
use_math: true
---
# Dual ascent


Consider the constrained optimization problem

$\min_{x\in \mathbb{R}^{n}} f(x)$

$s.t. \ Ax=b$

where $A\in \mathbb{R}^{m\times n}$, $b\in \mathbb{R}^{m}$ and $f:\mathbb{R}^{n}\rightarrow \mathbb{R}$ is a convex function.
---



Its Lagrangian function is

$L(x, y) = f(x) + y^{T}(Ax-b)$

where y is a Lagrangian multiplier.
---



Its dual function is

$g(y) = \inf _{x\in \mathbb{R}^{n}} L(x, y) = -f^{\ast}(-A^{T}y)-b^{T}y$

where $f^{\ast}$ is a conjugate of $f$.
---



Then we have to optimize the dual function,

$\max _{y\in \mathbb{R}^{n}} g(y)$
---



Consider the strong duality holds, the optimal values of the primal and dual solution are the same.

The primal optimal point $x^{\ast}$ is recovered from a dual optimal point $y^{\ast}$.

$x^{\ast}=argmin_{x\in \mathbb{R}^n}\ L\left (x, y^{\ast}\right )$
---



Assuming that $g$ is differentiable, we use gradient ascent method to find out the residual for the equality constraint.

Then the gradient $\triangledown g(y^{\ast} )$ can be updated as follows,

$\triangledown g(y^{\ast} ) = Ax^{\ast} - b$
---



The dual ascent method consists of iterative steps

$1.$ Minimization step

$x^{k+1}=argmin_{x\in \mathbb{R}^n}\ L\left (x, y^{k}\right )$

where $k$ is number of iterations.

$2.$ Dual variable update step

$y^{k+1}= y^{k} + \alpha^{k}(Ax^{k+1}-b)$

where $\alpha^{k}$ is step size parameter.


