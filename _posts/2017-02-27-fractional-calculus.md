---
title: "Elementary Fractional Calculus"
categories:
  - Spectral Theory
tags:
  - fractional-differentiation
  - applied-mathematics
---

In this note we define the fractional derivative \\(\frac{\mathrm{d}^\alpha f}{\mathrm{d}x^\alpha}\\) of a function \\(f\\), where 
\\(\alpha\\) is allowed to be an arbitrary complex parameter. Notice that, heuristically speaking,
<div class="mathjax">\begin{equation*}
  \frac{\mathrm{d}}{\mathrm{d}x} \int f = f = \int \frac{\mathrm{d}}{\mathrm{d}x} f.
\end{equation*}</div>
So, in a sense that will be made more precise, we have
<div class="mathjax">\begin{equation*}
  \int = \left(\frac{\mathrm{d}}{\mathrm{d}x}\right)^{-1} = \frac{\mathrm{d}^{-1}}{\mathrm{d}x^{-1}}.
\end{equation*}</div>
This means that by extending the derivative we also obtain a generalized integration in "fractional dimension". In fact, it turns out that
fractional integration makes a good starting point for fractional calculus theory in general.
To keep things clear we disregard all convergence issues in what follows. 

### Fractional Integration Approach

We begin by defining fractional integration. Since 
<div class="mathjax">\begin{equation*}
  \frac{\mathrm{d}}{\mathrm{d}x} \int_{c}^{x} f(t) ~\text{d} t = f(x)
\end{equation*}</div>
we can think of the operator \\(f \longmapsto \int_{c}^{x} f(t) ~\text{d} t\\) as an inverse to differentiation. We express this by writing
<div class="mathjax">\begin{equation*}
  {}_{c}D_x^{-1}f(x) = \int_{c}^{x} f(t) ~\text{d} t
\end{equation*}</div>
Here we think of \\(D\\) as a generalized differentation/integration operator. The superscript denotes the order to which we are 
differentiating. The fact that integration is the inverse to differentation translates to a superscript of \\(-1\\). Notice that these 
generalized derivatives depend on a choice of base point \\(c\\).

If we repeat this process, we see that it makes sense to define 
<div class="mathjax">\begin{equation*}
  {}_{c}D_{x}^{-2} = {}_{c}D_{x}^{-1} \circ {}_{c}D_{x}^{-1}
\end{equation*}</div>
Let us compute what this means explicitly:
<div class="mathjax">\begin{align*}
  {}_{c}D_x^{-2}f(x) 
    &= 
  \int_{c}^{x} {}_{c}D_{t_0}^{-1}f(t_0) ~\text{d} t_0 
    =
  \int_{c}^{x} \int_{c}^{t_0} f(t_1) ~\text{d} t_1 ~\text{d} t_0 \\
    &= 
  \int_{c}^{x} f(t_1) \int_{t_1}^{x}  ~\text{d} t_0 ~\text{d} t_1 \\
    &=
  \int_{c}^{x} f(t_1)(x-t_1) ~\text{d} t_1
\end{align*}</div>
Applying this procedure recursively we arrive at a definition for \\({} _ {c}D _ {x}^{-n}\\):
<div class="mathjax">\begin{equation*}
  {}_{c}D_{x}^{-n}f(x) = \frac{1}{(n-1)!} \int_{c}^{x} f(t)(x-t)^{n-1} ~\text{d} t
\end{equation*}</div>
To keep notation standard, we replace \\(-n\\) with \\(n\\) in the formula above to obtain
<div class="mathjax">\begin{equation*}
  {}_{c}D_{x}^{n}f(x) = \frac{1}{(-n-1)!} \int_{c}^{x} \frac{f(t)}{(x-t)^{n+1}} ~\text{d} t
\end{equation*}</div>
valid for negative integers \\(n\\). In order to extend \\(D\\) to arbitrary complex order, we simply replace the factorials with gamma 
functions, then swap out the negative integers \\(n\\) for arbitrary complex \\(\alpha\\). In this way we arrive at the following formula
for the generalized \\(\alpha^{th}\\)-derivative of \\(f\\):
<div class="mathjax">\begin{equation} \label{eq:def1}
  {}_{c}D_{x}^{\alpha}f(x) = \frac{1}{\Gamma(-\alpha)} \int_{c}^{x} \frac{f(t)}{(x-t)^{\alpha+1}} ~\text{d} t
\end{equation}</div>


### Fourier Transform Approach

In this section we attempt to define a fractional derivative using Fourier analtyic methods. Recall that the Fourier transform is the
automorphism of \\(L^2(\mathbb{R})\\) defined by
<div class="mathjax">\begin{equation*}
  \mathcal{F}[f](\xi) = \int_{\mathbb{R}}^{} f(x)e^{-2\pi i\xi x} ~\text{d}x
\end{equation*}</div>
Let \\(S\\) be an operator defined on \\(L^2\\) functions, and let \\(S\\) satisfy the following Fourier transform identity:
<div class="mathjax">\begin{equation*}
  \sigma(\xi) \cdot \mathcal{F}[f](\xi) = \mathcal{F}[Sf](\xi)
\end{equation*}</div>
Then we call the function \\(\sigma\\) the *symbol* of the operator \\(S\\). We shall be particularly interested in the symbol of the 
differentiation operator \\(\frac{\mathrm{d}}{\mathrm{d}x}\\). We know that the derivative transforms like
<div class="mathjax">\begin{equation*}
  (2\pi i \xi) \cdot \mathcal{F}[f](\xi) = \mathcal{F} \left[ \frac{\mathrm{d}f}{\mathrm{d}x}\right](\xi)
\end{equation*}</div>
so \\(\frac{\mathrm{d}}{\mathrm{d}x}\\) has symbol \\(2\pi i \xi\\). In general \\(\frac{\mathrm{d}^n}{\mathrm{d}x^n}\\) has symbol 
\\((2\pi i\xi)^n\\) since
<div class="mathjax">\begin{equation*}
  (2\pi i \xi)^n \cdot \mathcal{F}[f](\xi) = \mathcal{F} \left[ \frac{\mathrm{d}^nf}{\mathrm{d}x^n}\right](\xi)
\end{equation*}</div>

If we invert the Fourier transform in the equations above, we obtain a new expression for the derivative of \\(f\\), namely
<div class="mathjax">\begin{align*}
  \frac{\mathrm{d}^nf}{\mathrm{d}x^n}(x) 
    &= 
  \mathcal{F}^{-1}[(2\pi i\xi)^n \cdot \mathcal{F}[f](\xi)] \\
    &=
  \mathcal{F}^{-1}[(2\pi i\xi)^n] \ast f(x)
\end{align*}</div>
Here we must interpret the Fourier transform in the sense of Schwartz distributions. This line of reasoning suggests we define the generalized 
\\(\alpha^{th}\\) derivative by
<div class="mathjax">\begin{equation} \label{eq:def2}
  D^\alpha f(x) = \mathcal{F} ^{-1}[(2\pi i \xi)^\alpha]\ast f(x)
\end{equation}</div>

Let us try to reconcile this definition with the one given in equation \ref{eq:def1}. We will show that the so-called Weyl fractional
derivative \\({} _ {-\infty}D _ {x}^\alpha f\\) with base point \\(-\infty\\) has symbol \\((2\pi i\xi)^\alpha\\), meaning that equation
\ref{eq:def2} defines the same operator as \ref{eq:def1} when \\(c = -\infty\\). To this end we compute
<div class="mathjax">\begin{align*}
  \mathcal{F}[{} _ {-\infty} D _ {x}^\alpha f](\xi) 
    &=
  \int _ {\mathbb{R}}^{} {} _ {-\infty}D _ {x}^\alpha f(x) e^{-2\pi i \xi x} ~\text{d}x \\
    &=
  \frac{1}{\Gamma(-\alpha)} \int_{\mathbb{R}}^{} \int_{-\infty}^{x} \frac{f(t)}{(x-t)^{\alpha + 1}} ~\text{d} t ~ e^{-2\pi i \xi x} ~\text{d} x \\
    &=
  \frac{1}{\Gamma(-\alpha)} \int_{\mathbb{R}} \int_{t}^{\infty} \frac{f(t)}{(x-t)^{\alpha + 1}} e^{-2\pi i \xi x} ~\text{d} x ~\text{d} t \\
    &=
  \frac{1}{\Gamma(-\alpha)} \int_{\mathbb{R}} f(t)e^{-2\pi i \xi t} \int_{0}^{\infty} x^{-\alpha - 1} e^{-2\pi i \xi x} ~\text{d} x ~\text{d} t \\
    &=
  (2\pi i \xi)^{\alpha} \int_{\mathbb{R}}^{} f(t) e^{-2\pi i \xi x} ~\text{d} x \\
    &=
  (2\pi i \xi)^{\alpha} \mathcal{F}[f](\xi)
\end{align*}</div>
In order to complete the last two steps of the above computation, we use the defintion of the \\(\Gamma\\)-function, which is
<div class="mathjax">\begin{equation*}
  \Gamma(\alpha) = \int_{0}^{\infty} t^{\alpha} e^{-\alpha} \frac{~\text{d}t}{t} 
\end{equation*}</div>
along with the change of variables \\(s = 2\pi i\xi s\\) with \\(\mathrm{d}s = 2\pi i\xi \mathrm{d}t\\), in order to derive
<div class="mathjax">\begin{equation*}
  (2\pi i \xi)^{-\alpha} = \frac{1}{\Gamma(\alpha)} \int_{0}^{\infty} s^{\alpha}e^{-2\pi i\xi s} \frac{~\text{d} s}{s}
\end{equation*}</div>
Or, what is the same,
<div class="mathjax">\begin{equation*}
  (2\pi i \xi)^{\alpha} = \frac{1}{\Gamma(-\alpha)} \int_{0}^{\infty} t^{-\alpha}e^{-2\pi i\xi t} \frac{~\text{d} t}{t}
\end{equation*}</div>
which is exactly the identity we used in the computation above. So to recap, we have shown that the Fourier transform definition of the fractional
deriviative corresponds to the previous definition, provided we choose the base point \\(c = -\infty\\).  


### Cauchy Integral Formula Approach

In this section we take a different approach to defining fractional differentiation, this time based on the Cauchy integral formula. As a 
result, we temporarily require \\(f\\) to be analytic in a neighbourhood of \\(\mathbb{R}\\). As we shall see, this approach ends up
agreeing with the one in the previous section.

Suppose \\(C_R\\) is the circle of radius \\(R\\) about the point \\(x\in \mathbb{R}\\). The generalized Cauchy integral formula states
<div class="mathjax">\begin{equation*}
  D^n f(x) = \frac{n!}{2\pi i} \int_{C_R}^{} \frac{f(\zeta)}{(\zeta - x)^{n+1}} ~\text{d}\zeta
\end{equation*}</div>
We may attempt to replace the positive integer \\(n\\) in this formula with an arbitrary complex number to obtain
<div class="mathjax">\begin{equation*}
  D^\alpha f(x) = \frac{\Gamma(\alpha + 1)}{2\pi i} \int_{C_R}^{} \frac{f(\zeta)}{(\zeta - x)^{\alpha + 1}} ~\text{d}\zeta
\end{equation*}</div>
However we have now introduced a branching singularity at \\(x\\). To get around this we:

1. Choose \\(r < R\\), make a branch cut along the ray \\((-\infty, x)\\), and replace the contour \\(C_R\\) with the curve
<div class="mathjax">\begin{equation*}
  \gamma = L_1 \cup C_r \cup L_2
\end{equation*}</div>
where \\(L_1\\) is the line segment joining \\(x - R\\) to \\(x - r\\), and \\(L_2\\) is \\(L_1\\) with reversed orientation. Take the
branch of the logarithm with argument ranging from \\(-\pi\\) to \\(\pi\\). Depending on which segment of \\(\gamma\\) contains \\(\zeta\\)
we get the following representations for the function \\((\zeta - x)^{-\alpha - 1}\\):

- On \\(L_1\\):
<div class="mathjax">\begin{align*}
  (\zeta - x)^{-\alpha - 1} 
    &= \exp[(-\alpha - 1)(\log(|\zeta - x|) - i\pi)[ \\
    &= \exp[(-\alpha - 1)(\log(x - \zeta) - i\pi)]
\end{align*}</div>

- On \\(C_r\\): (with angular variable \\(-\pi \leq \theta \leq \pi\\))
<div class="mathjax">\begin{align*}
  (\zeta - x)^{-\alpha - 1} 
    &= \exp[(-\alpha - 1)(\log(|\zeta - x|) + i\theta)] \\
    &= \exp[(-\alpha - 1)(\log(r) + i\theta)]
\end{align*}</div>

- On \\(L_2\\):
<div class="mathjax">\begin{align*}
  (\zeta - x)^{-\alpha - 1} 
    &= \exp[(-\alpha - 1)(\log(|\zeta - x|) + i\pi)] \\
    &= \exp[(-\alpha - 1)(\log(x - \zeta) + i\pi)]
\end{align*}</div>

Therefore, we compute
<div class="mathjax">\begin{align*}
  \int_{\gamma}^{} \frac{f(\zeta)}{(\zeta - x)^{\alpha + 1}}  ~\text{d} \zeta 
    &=
  e^{(\alpha + 1)i\pi}\int_{x-R}^{x-r} \frac{f(t)}{(x- t)^{\alpha + 1}}  ~\text{d} t \\
    &\quad+ \int_{C_r}^{} \frac{f(\zeta)}{(\zeta - x)^{\alpha + 1}}  ~\text{d} \zeta \\
	&\quad+ e^{-(\alpha + 1)i\pi} \int_{x-r}^{x-R} \frac{f(t)}{(x-t)^{\alpha + 1}}  ~\text{d} t
\end{align*}</div>
We can estimate the portion of the integral over \\(C_r\\) via the inequality
<div class="mathjax">\begin{align*}
  \left| \int_{C_r}^{} \frac{f(\zeta)}{(\zeta - x)^{\alpha + 1}}  ~\text{d} \zeta \right|
    =
  \left| \int_{-\pi}^{\pi} \frac{f(x + re^{i\theta})}{r^{\alpha + 1}e^{(\alpha + 1)i\theta}} ire^{i\theta} ~\text{d} \theta \right| 
    \leq
  r^{-\Re(\alpha)} \int_{-\pi}^{\pi} |f(x+re^{i\theta})| ~\text{d} \theta
\end{align*}</div>
It follows that once \\(\Re(\alpha) < 0\\) we can let \\(r\to 0\\) to obtain
<div class="mathjax">\begin{align*}
  D^\alpha f(x) 
    &= 
  \frac{\Gamma(\alpha + 1)}{2\pi i} \int_{\gamma}^{} \frac{f(\zeta)}{(\zeta - x)^{\alpha + 1}}  ~\text{d} \zeta \\
    &=
  \frac{\Gamma(\alpha + 1)}{2\pi i} (e^{(\alpha + 1)i\pi} - e^{-(\alpha + 1)i\pi}) \int_{x-R}^{x} \frac{f(t)}{(x-t)^{\alpha + 1}}  ~\text{d} t \\
    &=
  \frac{\Gamma(\alpha + 1)\sin(\alpha + 1)\pi}{\pi} \int_{x-R}^{x} \frac{f(t)}{(x-t)^{\alpha + 1}}  ~\text{d} t
\end{align*}</div>
Let us set \\(c := x - R\\) and employ the lovely [reflection formula](https://proofwiki.org/wiki/Euler%27s_Reflection_Formula) to rewrite
the above as
<div class="mathjax">\begin{align*}
  {}_{c}D_{x}^\alpha f(x) 
    &= 
  \frac{1}{\Gamma(-\alpha)}  \int_{c}^{x} \frac{f(t)}{(x-t)^{\alpha + 1}}  ~\text{d} t
\end{align*}</div>
