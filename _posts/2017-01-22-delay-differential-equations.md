---
title: "Delay Differential Equations I"
categories:
  - Applied Mathematics
tags:
  - mathematics
  - differential-equations
---

Consider a differential equation of the form
<div class="mathjax">\begin{equation} \label{eq:dde} 
  \frac{\mathrm{d}x}{\mathrm{d}t} = f(t, x(t), x(t - \tau))
\end{equation}</div>
for some locally Lipschitz function \\(f \colon \mathbb{R} \times \mathbb{R}^d \times \mathbb{R}^d \to \mathbb{R}^d\\) and \\(\tau > 0\\).
An equation of the form \ref{eq:dde} is an example of a *delay differential equation* (DDE). The \\(x(t-\tau)\\) term signifies that the value
\\(x(t)\\) of a solution depends on the earlier state at time \\(t - \tau\\). In applications we are generally interested in solutions
defined for \\(t>0\\), and where we specify an initial function \\(\varphi \colon [-\tau, 0] \to \mathbb{R}^d\\) representing the
history of the system before our initial time \\(t = 0\\).

In this note we provide a naive method for solving DDEs of the type in equation \ref{eq:dde}. While this method is of limited practical
use, it provides an initial understanding into the behaviour of solutions to DDEs.


## The method of steps

Suppose we are given equation \ref{eq:dde} with history function \\(\varphi\\) on \\([-\tau, 0]\\). Once \\(\varphi\\) is fixed, equation
\ref{eq:dde} reduces to the initial value problem
<div class="mathjax">\begin{equation*}
\begin{split}
  \frac{\mathrm{d}x}{\mathrm{d}t} &= f(t, x(t), \varphi(t - \tau)), \quad t \in (0, \tau]\\
  x(0) &= \varphi(0)
\end{split}
\end{equation*}</div>
Such an IVP can be solved explicitly on \\([0, \tau]\\) using the usual techniques from ODE theory. Once we know the value of \\(x\\) on
\\([0, \tau]\\) we obtain a new ODE
<div class="mathjax">\begin{equation*}
\begin{split}
  \frac{\mathrm{d}\widetilde{x}}{\mathrm{d}t} &= f(t, \widetilde{x}(t), x(t - \tau)), \quad t \in (\tau, 2\tau] \\
  \widetilde{x}(\tau) &= x(\tau)
\end{split}
\end{equation*}</div>
A function \\(\widetilde{x}\\) solving this new system gives an extension of our previous solution to the interval \\([\tau, 2\tau]\\).
Repeating this process we can extend our initial solution as far in time as required. The recursive algorithm for solving DDEs described
above is called the *method of steps*.

## Example

Fix some constant \\(\theta_0 \in \mathbb{R}\\) and consider the DDE
<div class="mathjax">\begin{equation*}
\begin{split}
  \frac{\mathrm{d} x}{\mathrm{d}t} &= - cx(t - \tau), \quad t > 0 \\
  x(t) &\equiv \theta_0 \quad \forall t \in [-\tau, 0]
\end{split}
\end{equation*}</div>
In light of the initial history function being constant this reduces to the ODE
<div class="mathjax">\begin{equation*}
  \frac{\mathrm{d}x}{\mathrm{d}t} -c\theta_0, \quad x(0) = \theta_0
\end{equation*}</div>
on the interval \\([0, \tau]\\). The solution is given by
<div class="mathjax">\begin{equation*}
  x(t) = -c\theta_0 t + \theta_0
\end{equation*}</div>
Stepping forward to \\([\tau, 2\tau]\\) we obtain the new ODE
<div class="mathjax">\begin{equation*}
  \frac{\mathrm{d}x}{\mathrm{d}t} = -c\theta_0(t-\tau) + \theta_0, \quad x(\tau) = -c\theta_0\tau + \theta_0
\end{equation*}</div>
which in turn has solution
<div class="mathjax">\begin{equation*}
  x(t) = -c\theta_o(t^2 - \tau t) + \theta_0t - \theta_0\tau(c + 1) + \theta_0
\end{equation*}</div>
Repeating this process we can extend this solution as long as we like.

In [Delay Differential Equations II]({{ site.baseurl }}{% post_url 2017-01-22-delay-differential-equations-ii %}) we consider
more powerful methods for solving a class of DDE that includes equations of the type \ref{eq:dde}.
