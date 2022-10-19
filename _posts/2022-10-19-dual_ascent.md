---
layout: single
title: "Dual Ascent"
categories:
 - Algorithm
use_math: true
---

# Dual ascent

Consider the constrained optimization problem

$min_{x\in \mathbb{R}^{n}} f(x)$

$s.t. \,Ax=b$

where $A\in \mathbb{R}^{m\times n}$, $b\in \mathbb{R}^{m}$ and $f:\mathbb{R}^{n}\rightarrow \mathbb{R}$ is a convex function.

Its Lagrangian function is

$L(x, y) = f(x) + y^{T}(Ax-b)$

where y is a Lagrangian multiplier.
