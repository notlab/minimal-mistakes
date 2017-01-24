---
title: "Delay Differential Equations II"
categories:
  - Applied Mathematics
tags:
  - mathematics
  - differential-equations
---

In the note [Delay Differential Equations I]({{ site.baseurl }}{% post_url 2017-01-22-delay-differential-equations %})
we introduced a simple algorithm for solving delay equations of the form
<div class="mathjax">\begin{equation} \label{eq:dde-std} 
  \frac{\mathrm{d}x}{\mathrm{d}t} = f(t, x(t), x(t - \tau))
\end{equation}</div>
This method has its limitations. For instance, it cannot address equations with "distributed delay" such as
<div class="mathjax">\begin{equation} \label{eq:dde-dist}
  \frac{\mathrm{d}x}{\mathrm{d}t} = f \left(t, x(t), \int_{-\tau}^{0} g(x(t - \sigma)) ~\text{d}\sigma \right)
\end{equation}</div>
In this note we give a definition of delay differential equation that includes equations like \ref{eq:dde-std} and \ref{eq:dde-dist}
as special cases. We also outline a theoretical framework for the analysis of DDEs.

## Abstract definition of a DDE

Let \\(C \_ {d,\tau}\\) denote the space \\(C([-\tau, 0] ; \mathbb{R}^d)\\) of continuous functions. Fix a continuously Frechet differentiable
function \\(f \colon C_{d,\tau} \to C_{d,\tau}\\) satisfying \\(f(0) = 0\\). Given some
\\(x \colon (\alpha, \beta) \to \mathbb{R}^d\\), where \\((\alpha, \beta)\\) is an interval containing \\([-\tau, 0]\\), we can construct
a family of new functions
\\(x_t \colon [-\tau, 0] \to \mathbb{R}^d\\) according to the formula
<div class="mathjax">\begin{equation*}
  x_t(\sigma) ~:= x(t + \sigma)
\end{equation*}</div>
For a given value of \\(t\\), the function \\(x_t\\) represents the history of the function \\(x\\) on the interval \\([t-\tau, t]\\). 
By the term *delay differential equation* we shall mean an equation of the form
<div class="mathjax">\begin{equation} \label{eq:absdde}
  \frac{\mathrm{d}x_t}{\mathrm{d}t} = f(x_t)
\end{equation}</div>
The important thing distinguishing this from an ODE is that the evolution at time \\(t\\) depends on the history of the solution on the
entire interval \\([t-\tau, t]\\). As before, we typically impose an initial function condition of the form \\(x| \_ {[-\tau, 0]} = \varphi\\) 
for some \\(\varphi \in C_{\tau, d}\\).

## DDE Semigroups

Denote by \\(L\\) the linearization (Frechet derivative) of the operator \\(f\\) at the zero function, and let us consider the simplified 
system
<div class="mathjax">\begin{equation*}
\begin{split}
  \frac{\mathrm{d}x_t}{\mathrm{d}t} &= L[x_t] \\
  x_0 &= \varphi
\end{split}
\end{equation*}</div>
If \\(x_t[\varphi]\\) is a solution to this system
