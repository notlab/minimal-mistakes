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

**Definition 1.** By the term *delay differential equation* we shall mean an equation of the form
<div class="mathjax">\begin{equation} \label{eq:absdde}
  \frac{\mathrm{d}x_t}{\mathrm{d}t} = f(x_t)
\end{equation}</div>
Note that on the left hand side we are taking a Frechet derivative in the space \\(C_{\tau, d}\\). As before, we typically impose an initial 
function condition of the form \\(x| \_ {[-\tau, 0]} = \varphi\\) for some \\(\varphi \in C_{\tau, d}\\). We shall denote a solution to equation 
\ref{eq:absdde} with initial function \\(\varphi\\) by \\(x_t^\varphi\\).
∎

The important thing distinguishing a DDE from an ODE is that the evolution at time \\(t\\) depends on the history of the solution on the
entire interval \\([t-\tau, t]\\).


## DDE Semigroups

Denote by \\(L\\) the linearization (Frechet derivative) of the operator \\(f\\) at the zero function, and let us consider the simplified 
system
<div class="mathjax">\begin{equation}\label{eq:lin}
  \frac{\mathrm{d}x}{\mathrm{d}t} = L[x_t], \quad
  x_0 = \varphi
\end{equation}</div>
As usual we can learn a lot about a DDE by studying the flow of solutions to its linearization. 

**Definition 2.** Suppose we are given a linearized DDE as in equation \ref{eq:lin}. For each \\(t > 0\\), the *solution operator* 
\\(P[t] \colon C_{\tau, d} \to C_{\tau, d}\\) is defined according to the formula
<div class="mathjax">\begin{equation*}
  P[t](\varphi) = x_t^\varphi
\end{equation*}</div> ∎

It is easy to verify the solution operators satisfy the axioms of a one-parameter semigroup. In other words, the solution operators
satisfy the following three properties:

* For all \\(t \geq 0\\), \\(P[t]\\) is bounded linear operator on \\(C_{\tau, d}\\) satisfying
  <div class="mathjax">\begin{equation*}
    P[s + t](\varphi) = P[s](P[t](\varphi));
  \end{equation*}</div>
* \\(P\[0\](\varphi) = \varphi\\);
* \\(\lim_{s \rightarrow t} \| P\[s\](\varphi) - P\[t\](\varphi) \| = 0\\).

