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

$s.t. \,Ax=b$

where $A\in \mathbb{R}^{m\times n}$, $b\in \mathbb{R}^{m}$ and $f:\mathbb{R}^{n}\rightarrow \mathbb{R}$ is a convex function.

Its Lagrangian function is

$L(x, y) = f(x) + y^{T}(Ax-b)$

where y is a Lagrangian multiplier.

Its dual function is

$g(y) = \inf _{x\in \mathbb{R}^{n}} L(x, y) = -f^{*}(-A^{T}y)-b^{T}y$

where $f^{*}$ is a conjugate of $f$.

Then we have to optimize the dual function,

$\max _{y\in \mathbb{R}^{n}} g(y)$

$\,y^{*}$

Consider the strong duality holds, the optimal values of the primal and dual solution are the same.

The primal optimal point $x^{*}$ is recovered from a dual optimal point $y^{*}$.

$x^{*}=arg\min_{x\in \mathbb{R}^{n}} L(x,y^{*})$


