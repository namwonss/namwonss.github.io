---
layout: single
title: "Dual Decomposition"
categories:
 - Algorithm
use_math: true
---
In computer science, decomposition is breaking down a complex problem (difficult) into smaller problems. It is sometimes more efficient or easier to understand.


Consider


<center>$f\left ( x \right ) = \sum_{i=1}^{N}f_{i} \left ( x_{i} \right )$</center>


where objective function $f$ is separable, $x=\left ( x_{1},...,x_{N} \right )$, and the variables $x_{i} \in \mathbb{R}^{n}$ are subvectors of $x$.


Similarly, $A=\left [ A_{1},A_{2},...,A_{N} \right ]$


so $Ax = \sum_{i=1}^{N} A_{i}x_{i}$, and the Lagrangian function is as follows,


<center>$L\left ( x,y \right ) = \sum_{i=1}^{N} L_{i}\left ( x_{i},y_{i} \right )$</center>

<center>$=\sum_{i=1}^{N} \left ( f\left ( x \right ) +y^{T}A_{i}x_{i}-\frac{1}{N}y^{T}b\right )$.</center>


The minimization step splits into $N$ separate problems, which are solved parallelly.


<center>$x^{k+1}=argmin_{x\in \mathbb{R}^n}\ L_{i}\left (x_{i}, y^{k}_{i}\right )$</center>


The dual variable update is as follows,


<center>$y^{k+1}=y^{k}+\alpha^{k}\left ( Ax^{k+1}-b \right )$</center>


Thus, this decomposition in dual ascent is referred to as dual decomposition.
