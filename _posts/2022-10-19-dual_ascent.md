---
layout: single
title: "Dual Ascent"
categories:
 - Algorithm
use_math: true
---
# Dual ascent


Consider the constrained optimization problem

<center>$\min_{x\in \mathbb{R}^{n}} f(x)$</center>

<center>$s.t. \ Ax=b$</center>

where $A\in \mathbb{R}^{m\times n}$, $b\in \mathbb{R}^{m}$ and $f:\mathbb{R}^{n}\rightarrow \mathbb{R}$ is a convex function.

---



Its Lagrangian function is

<center>$L(x, y) = f(x) + y^{T}(Ax-b)$</center>

where y is a Lagrangian multiplier.

---



Its dual function is

<center>$g(y) = \inf _{x\in \mathbb{R}^{n}} L(x, y) = -f^{\ast}(-A^{T}y)-b^{T}y$</center>

where $f^{\ast}$ is a conjugate of $f$.

---



Then we have to optimize the dual function,

<center>$\max _{y\in \mathbb{R}^{n}} g(y)$</center>

---



Consider the strong duality holds, the optimal values of the primal and dual solution are the same.

The primal optimal point $x^{\ast}$ is recovered from a dual optimal point $y^{\ast}$.

<center>$x^{\ast}=argmin_{x\in \mathbb{R}^n}\ L\left (x, y^{\ast}\right )$</center>

---



Assuming that $g$ is differentiable, we use gradient ascent method to find out the residual for the equality constraint.

Then the gradient $\triangledown g(y^{\ast} )$ can be updated as follows,

<center>$\triangledown g(y^{\ast} ) = Ax^{\ast} - b$</center>

---



The dual ascent method consists of iterative steps

$1.$ Minimization step

<center>$x^{k+1}=argmin_{x\in \mathbb{R}^n}\ L\left (x, y^{k}\right )$</center>

where $k$ is number of iterations.

$2.$ Dual variable update step

<center>$y^{k+1}= y^{k} + \alpha^{k}(Ax^{k+1}-b)$</center>

where $\alpha^{k}$ is step size parameter.


