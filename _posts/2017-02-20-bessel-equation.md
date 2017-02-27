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
Solutions to the Bessel equation are transcendental functions called Bessel functions, and they have wide application. For instance they appear 
in the classical theory of [modular forms](https://en.wikipedia.org/wiki/Modular_form) on the upper half plane, and the solutions of the 
[heat equation](https://en.wikipedia.org/wiki/Heat_equation) and 
[Schrodinger equation](https://en.wikipedia.org/wiki/Schr%C3%B6dinger_equation)
in cylindrical coordinates. There are many different kinds of Bessel function. Each of these tends to be best suited to a specific type of 
application. In this note we treat the most common kinds of Bessel function.

For convenience, we introduce the notation
<div class="mathjax">\begin{equation*} 
  L_\nu = z^2 \frac{\mathrm{d}^2}{\mathrm{d}z^2} + z \frac{\mathrm{d}}{\mathrm{d}z} + (z^2 - \nu^2)
\end{equation*}</div>
for the differential operator in \ref{eq:bessel}. The Bessel equation can then be rewritten as
<div class="mathjax">\begin{equation*} 
  L_\nu[v] = 0
\end{equation*}</div>

## Bessel Functions of the First Kind

### Derivation of Solutions

Note that our equation has a [regular singular point](https://en.wikipedia.org/wiki/Regular_singular_point) at \\(z = 0\\). In this section
we follow the usual approach for finding series solutions to ODE with regular singularities. Namely, we look for solutions of the form 
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
Since \\(a _ 0 \ne 0\\), this implies \\(\alpha = \pm \nu\\). The restriction \\(\alpha \pm \nu \not\in \mathbb{Z} _ {<0}\\) thus reduces to 
requiring \\(-2\nu \not\in \mathbb{Z} _ {<0}\\) when \\(\alpha = -\nu\\) (resp. \\(2\nu \not\in \mathbb{Z}_{<0}\\) when \\(\alpha = \nu\\)).

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

It can be shown, eg. with the Weierstrass M-test, that the sum defining \\(J_\nu\\) converges absolutely and uniformly in a 
neighbourhood of any \\(z \in \mathbb{C} \setminus \\{ 0 \\}\\) and in any bounded domain of values of \\(\nu\\). 

### Fundamental System of \\(1^{st}\\)-kind solutions.

In this section we show that, provided \\(\nu \not\in \mathbb{Z}\\), the system \\(\\{ J_\nu, J_{-\nu}\\}\\) forms a linearly independent basis 
of solutions for the Bessel equation \ref{eq:bessel}. To do so, it suffices to show the Wronskian determinant
\\(\mathcal{W}(J_\nu, J_{-\nu}) \\) does not vanish. In other words, we want to show
<div class="mathjax">\begin{equation*} 
  \mathcal{W}(J_{\nu}(z), J_{-\nu}(z)) 
    =
  \det \begin{pmatrix}
  J_\nu & J_{-\nu} \\
  \frac{\partial J_\nu}{\partial z} & \frac{\partial J_{-\nu}}{\partial z}
  \end{pmatrix}
    =
  0
\end{equation*}</div>

First, we attempt to extract a Wronskian-like quantity from the Bessel equation by computing
<div class="mathjax">\begin{align*} 
  J_\nu \cdot L_\nu[J_{-\nu}] &- J_{-\nu} \cdot L_\nu[J_\nu] \\
    &=
  z^2 J_\nu \frac{\partial^2 J_{-\nu}}{\partial z^2} - z^2 J_{-\nu} \frac{\partial^2 J_\nu}{\partial z^2} +
    z J_\nu  \frac{\partial J_{-\nu}}{\partial z} - z J_{-\nu} \frac{\partial J_\nu}{\partial z} \\
    &=
  z \left[z J_\nu \frac{\partial^2 J_{-\nu}}{\partial z^2} - z J_{-\nu} \frac{\partial^2 J_\nu}{\partial z^2} +
    J_\nu \frac{\partial J_{-\nu}}{\partial z} - J_{-\nu} \frac{\partial J_\nu}{\partial z} \right] \\
    &=
  0
\end{align*}</div>
The whole expression equals zero since \\(L_\nu[J_{-\nu}] = 0 = L_\nu[J_\nu]\\). The bracketed term on the last line above somewhat resembles the 
product \\(z \mathcal{W}(J_\nu, J_{-\nu})\\). The main differences between the two are the second-order derivatives and factor of \\(z\\). 
Both of these differences can be accounted for by taking a derivative. We compute:
<div class="mathjax">\begin{align*} 
  \frac{\mathrm{d}}{\mathrm{d}z} [ zW(J_\nu &, J_{-\nu})] \\
    &=
  z J_\nu \frac{\partial^2 J_{-\nu}}{\partial z^2} 
    + \left(z \frac{\partial J_{\nu}}{\partial z} + J_\nu\right)\frac{\partial J_{-\nu}}{\partial z}
	- z J_{-\nu} \frac{\partial^2 J_\nu}{\partial z^2} 
	- \left(z \frac{\partial J_{-\nu}}{\partial z} + J_{-\nu}\right) \frac{\partial J_\nu}{\partial z} \\
	&=
  z J_\nu \frac{\partial^2 J_{-\nu}}{\partial z^2} J_{-\nu} - z J_{-\nu} \frac{\partial^2 J_\nu}{\partial z^2}
    + J_\nu \frac{\partial J_{-\nu}}{\partial z} - J_{-\nu} \frac{\partial J_\nu}{\partial z} \\
	&= 
  \frac{J_\nu \cdot L_\nu[J_{-\nu}] - J_{-\nu} \cdot L_\nu[J_\nu]}{z} \\
    &=
  0
\end{align*}</div>
In other words, the function \\(z \mapsto z\cdot \mathcal{W}(J_\nu(z), J_{-\nu}(z))\\) is constant. Solving for the Wronskian, we have
<div class="mathjax"> \begin{equation} \label{eq:frac}
  \mathcal{W}(J_\nu, J_{-\nu}) = \frac{C}{z}
\end{equation}</div>

In order to evaluate the constant \\(C\\), first let us note the easily obtained formulae, valid when \\(\nu \not\in \mathbb{Z}\\) and for 
small \\(|z|\\):
<div class="mathjax">\begin{equation*}
  J_\nu(z) = \frac{\left(\frac{1}{2} z\right)^\nu}{\Gamma(\nu + 1)} (1 + O(z^2)), \quad\quad
  \frac{\partial J_{\nu}(z)}{\partial z} = \frac{\left(\frac{1}{2} z\right)^{\nu-1}}{2\Gamma(\nu)} (1 + O(z^2)) 
\end{equation*}</div>
Similar formulae exist for \\(J_{-\nu}\\) and \\(\frac{\partial J_{-nu}}{\partial z}\\). This allows us to compute
<div class="mathjax"> \begin{align*}
  \mathcal{W}(J_\nu, J_{-\nu}) 
    = 
  J_\nu \frac{\partial J_\nu}{\partial z} - J_{-\nu} \frac{\partial J_{-\nu}}{\partial z}
    &=
  \frac{1}{z} \left[\frac{1}{\Gamma(\nu + 1)\Gamma(-\nu)} - \frac{1}{\Gamma(\nu)\Gamma(-\nu + 1)} \right] + O(z) \\
    &=
  -\frac{2\sin(\nu\pi)}{\pi z} + O(z)
\end{align*} </div>
In light of equation \ref{eq:frac} the \\(O(z)\\) term above must vanish. We conclude
<div class="mathjax"> \begin{equation*}
  \mathcal{W}(J _ \nu, J _ {-\nu}) = \frac{2\sin(\nu\pi)}{\pi z} 
\end{equation*}</div>
Since \\(\nu \not\in \mathbb{Z}\\), \\(\sin(\nu z\\) does not vanish. We arrive at the following theorem:

**Theorem 1:** When \\(\nu \not\in \mathbb{Z}\\), the \\(1^{st}\\)-kind functions \\(J_\nu\\) and \\(J_{-\nu}\\) form a fundamental system 
of solutions to Bessel's equation.
∎

On account of the relation \\(J_n(z) = (-1)^n J_{-n}(z)\\), these functions do *not* form a fundamental system when \\(\nu = n \in \mathbb{Z}\\).


## Bessel Functions of the Second Kind

### Derivation of Solutions

In the previous section we derived a fundamental system of solutions to the Bessel equation \ref{eq:bessel} subject to the condition
\\(\pm 2\nu \ne n\\) for any integer \\(n\in \mathbb{Z}\\). That is, we required \\(\nu\\) not be an even integer, nor half of an odd integer.
In this section we shall derive a solution that is valid even in the case \\(\nu \in \mathbb{Z}\\). 

For the remainder of this section let us fix some \\(n \in \mathbb{Z}\\). Now, since \\(J_\nu\\) and \\(J_{-\nu}\\) solve the Bessel equation for 
non-integer \\(\nu\\), so does the linear combination
<div class="mathjax">\begin{equation*}
  \frac{J_\nu(z) - (-1)^n J_{-\nu}(z)}{\nu - n} 
\end{equation*}</div>
If we then set
<div class="mathjax">\begin{equation*}
  \mathbf{Y}(z) = \lim_{\nu \rightarrow n}  \frac{J_\nu(z) - (-1)^n J_{-\nu}(z)}{\nu - n} 
\end{equation*}</div>
it seems reasonable to believe that \\(\mathbf{Y}\\) is also a solution to Bessel's equation. In order to check this, we recall 
\\(J_\nu\\) is analytic in \\(\nu\\) and compute
<div class="mathjax">\begin{align*}
  \mathbf{Y}(z) 
    &=
  \lim_{\nu \rightarrow n} \frac{J_\nu(z) - (-1)^n J_{-\nu}(z)}{\nu - n} \\
    &=
  \lim_{\nu \rightarrow n} \frac{J_\nu(z) - J_n(z)}{\nu - n} - (-1)^n \frac{J_{-nu}(z) - J_{-n}(z)}{\nu - n} \\
    &=
  \left. \frac{\partial}{\partial\nu}J_\nu(z) \right|_{\nu = n} - \left. (-1)^n \frac{\partial}{\partial\nu} J_{-\nu} \right|_{\nu = n}
\end{align*}</div>
We will show this expression solves equation \ref{eq:bessel}. First we exploit the equality of mixed partials to write
<div class="mathjax">\begin{equation*}
  \frac{\partial}{\partial\nu} L_\nu[J_{\pm\nu}]
\end{equation*}</div>
