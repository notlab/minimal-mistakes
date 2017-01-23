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
