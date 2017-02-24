---
title: "The Bessel Equation"
categories:
  - Differential Equations
tags:
  - bessel-equation
---

In this note we investigate series solutions to the [Bessel equation](https://www.encyclopediaofmath.org/index.php/Bessel_equation)
<div class="mathjax">\begin{equation} \label{eq:bessel}
  z^2 u'' + zu' + (z^2 - \nu^2)u = 0
\end{equation}</div>
Solutions to the Bessel equation are transcendental functions, and they have wide application. For instance they appear in the classical theory 
of [modular forms](https://en.wikipedia.org/wiki/Modular_form) on the upper half plane, and the solutions of the 
[heat equation](https://en.wikipedia.org/wiki/Heat_equation) and 
[Schrodinger equation](https://en.wikipedia.org/wiki/Schr%C3%B6dinger_equation)
in cylindrical coordinates. 

### First Solutions

Note that our equation has a [regular singular point](https://en.wikipedia.org/wiki/Regular_singular_point) at \\(z = 0\\). As usual we look for
solutions of the form
<div class="mathjax">\begin{equation*} 
  u(z) = z^\alpha \sum_{n=0}^{\infty} a_n z^n = \sum_{n=0}^{\infty} a_n z^{n+\alpha}
\end{equation*}</div>
where \\(a_0 \ne 0\\). Substituting this into equation \ref{eq:bessel} yields
<div class="mathjax">\begin{align*}
  0 
    &= 
  \sum_{n=0}^{\infty} (n+\alpha)(n+\alpha -1)z^{n+\alpha} 
    + \sum_{n=0}^{\infty} (n+\alpha) z^{n+\alpha}
    + \sum_{n=0}^{\infty} a_n z^{n+2+\alpha} 
	- \sum_{n=0}^{\infty} \nu^2 a_n z^{n+\alpha} \\
    &=
  \sum_{n=0}^{\infty} [((n+\alpha -1) + 1)(n+\alpha) - \nu^2]a_nz^{n+\alpha} + \sum_{n=2}^{\infty} a_{n-2}z^{n+\alpha} \\
    &=
  \sum_{n=0}^{\infty} ((n+\alpha)^2 - \nu^2)a_nz^{n+\alpha} + \sum_{n=2}^{\infty} a_{n-2}z^{n+\alpha} \\
    &=
  (\alpha^2 - \nu^2)a_0z^\alpha + ((1 + \alpha)^2 - \nu^2)a_1z^{1+\alpha} + \sum_{n=2}^{\infty} [((n + \alpha)^2 - \nu^2)a_n + a_{n-2}]z^{n+\alpha}
\end{align*}</div>
Comparing \\(z^{n+\alpha}\\)-coefficients in the equation above produces a series of identities involving the \\(a_n\\) terms. We consider the 
coefficients on \\(z^\alpha\\), \\(z^{1+\alpha}\\), and \\(z^{n+\alpha}\\) separately. 
To keep matters simple for the moment, it will be useful to assume that the terms \\((n + \alpha)^2 - \nu^2\\) appearing above do not vanish
for any integer \\(n \geq 1\\); we treat the remaining cases later. Since 
<div class="mathjax">\begin{equation*}
  (n + \alpha)^2 - \nu^2 = (\alpha + \nu + n)(\alpha - \nu + n),
\end{equation*}</div>
it will be enough to assume \\(\alpha \pm \nu\\) is not a negative integer.

**Case \\(z^{\alpha}\\):** Comparing these coefficients shows that
<div class="mathjax">\begin{equation*}
  (\alpha^2 - \nu^2)a_0 = 0
\end{equation*}</div>
Since \\(a_0 \ne 0\\), this implies \\(\alpha = \pm \nu\\). The restriction \\(\alpha \pm \nu \not\in \mathbb{Z}_{<0}\\) thus reduces to requiring
\\(\nu\\) not be a half-integer when \\(\alpha = -\nu\\) (resp. \\(\nu\\) not be a negative half-integer when \\(\alpha = \nu\\)).

**Case \\(z^{\alpha + 1}\\):** From this coefficient we obtain
<div class="mathjax">\begin{equation*}
  ((1 - \alpha)^2 - \nu^2)a_1 = (\alpha - \nu + 1)(\alpha + \nu + 1)a_1 = 0
\end{equation*}</div>
We have assumed \\((\alpha \pm \nu) \ne - 1\\), so the above implies \\(a_1 = 0\\). 

**Case \\(z^{\alpha + n}\\):** This time we obtain a recurrence of the form
<div class="mathjax">\begin{equation*} 
  [(n + \alpha)^2 - \nu^2]a_n + a_{n-2} = (\alpha - \nu + n)(\alpha + \nu + n)a_n + a_{n-2} = 0
\end{equation*}</div>
Rearranging, this is the same as
<div class="mathjax">\begin{equation*} 
  a_n = - \frac{a_{n-2}}{(\alpha - \nu + n)(\alpha - \nu + n)} 
\end{equation*}</div>
This allows us to quickly compute the odd-order terms \\(a_n = a_{2k - 1}\\). In particular, bootstrapping from the above case, 
<div class="mathjax">\begin{equation*} 
  a_3 = - \frac{a_{1}}{(\alpha - \nu + 3)(\alpha - \nu + 3)} = 0
\end{equation*}</div>
Repeating this for \\(n = 5, 7, \dots\\) demonstrates that \\(a _ {2k-1} = 0\\) for all \\(k \in \mathbb{Z} _ {>0}\\).
Induction also allows us to compute the even-order terms \\(a_n = a_{2k}\\). Indeed, when \\(n = 2\\) we have
<div class="mathjax">\begin{equation*} 
  a_2 = \frac{-a_{0}}{(\alpha - \nu + 2)(\alpha - \nu + 2)}
\end{equation*}</div>
and in general
<div class="mathjax">\begin{equation*} 
  a_{2k} = \frac{(-1)^k a_{0}}{(\alpha - \nu + 2)(\alpha - \nu + 4) \cdots (\alpha - \nu + 2k)(\alpha + \nu + 2) \cdots (\alpha - \nu + 2k)}
\end{equation*}</div>
If we take \\(\alpha = \nu\\), this reduces to
<div class="mathjax">\begin{equation*} 
  a_{2k} = - \frac{(-1)^k a_{0}}{2^{2k} k! (\nu + 1)(\nu + 2) \cdots (\nu + k)}
\end{equation*}</div>
Notice that there is no restriction on \\(a_0\\). 

Combining all of our work so far, we arrive at our first candidate solution for the Bessel equation:
<div class="mathjax">\begin{equation} \label{eq:candidate1} 
  u(z) = z^\nu \left[a_0 + \sum_{k=1}^{\infty} \frac{a_0 (-1)^k (\frac{1}{2}z)^{2k}}{k! (\nu +1)(\nu +2)\cdots (\nu + m)} \right]
\end{equation}</div>
Since we have no restriction on \\(a_0\\), it is convenient to choose \\(a_0 = \frac{1}{2^\nu \Gamma(\nu + 1)}\\). The solution \\(u\\)
in equation \ref{eq:candidate1} then simplifies to
<div class="mathjax">\begin{equation*} 
  J_\nu(z) = u(z) = \sum_{k=0}^{\infty} \frac{(-1)^k (\frac{1}{2}z)^{\nu + 2k}}{k! \Gamma(\nu + k + 1)}
\end{equation*}</div>
If we had instead choosen \\(\alpha = -\nu\\) above, we could have set \\(a_0 = \frac{1}{2^{-\nu} \Gamma(-\nu + 1)}\\). This leads to a solution
of the form
<div class="mathjax">\begin{equation*} 
  J_{-\nu}(z) = \sum_{k=0}^{\infty} \frac{(-1)^k (\frac{1}{2}z)^{\nu + 2k}}{k! \Gamma(\nu + k + 1)}
\end{equation*}</div>
In all situations considered so far (ie. when \\(2\nu\\) is not an integer) the sums defining \\(J_{\pm \nu}\\) converge for all 
\\(z \in \mathbb{C}\setminus \\{0\\}\\).

**Definition 1:** The functions \\(J_\nu\\) and \\(J_{-\nu}\\) defined above are called *Bessel functions of the first kind*.
∎
