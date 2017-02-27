---
title: "The Rational Projective Determinant"
categories:
  - Number Theory
tags:
  - determinant
  - lattice
  - hyperdistance
---

For even \\(n\\), the rational projective determinant is a canonically defined function 
\\(\mathrm{Pdet} : \mathrm{Mat}(n;\mathbb{Q}) \to \mathbb{Z}\\) introduced by 
[John F. R. Duncan](https://sites.google.com/site/johnfrduncan/home) in his paper 
[Arithmetic Groups and the Affine E8 Dynkin Diagram](https://arxiv.org/abs/0810.1465). 
In this note we define the rational projective determinant and investigate some of its elementary properties. As an aside, this paper by
Duncan is a must read.

### Definition

Suppose \\(A = (a_{ij}) \in \mathrm{Mat}(n; \mathbb{Q})\\) for some positive, even \\(n\\). Since each \\(a_{ij}\\) is rational we can write
\\(a_{ij} = b_{ij}/c_{ij}\\) for some \\(b_{ij}, c_{ij} \in \mathbb{Z}\\). Define \\(\alpha_A \in \mathbb{Q}^\times\\) by
<div class="mathjax">\begin{equation*}
  \alpha_A = \left| \frac{\mathrm{lcm}\{c_{ij}\}}{\mathrm{gcd}\{b_{ij}\}} \right|
\end{equation*}</div>
Then \\(\alpha_A\\) is the smallest positive element of \\(\mathbb{Q}^\times\\) such that \\(\alpha_A a_{ij} \in \mathbb{Z}\\) for each 
\\(1 \leq i,j \leq n\\). With this notation, we define the *projective determinant* function 
\\(\mathrm{Pdet} : \mathrm{Mat}(n;\mathbb{Q}) \to \mathbb{Z}\\) by the formula
<div class="mathjax">\begin{equation*}
  \mathrm{Pdet}(A) := \begin{cases}
    \det(\alpha_A A) = \alpha_A^n\det(A) & \text{ if } A \ne 0 \\
	0 & \text{ if } A = 0
  \end{cases}
\end{equation*}</div>
Since \\(\alpha_A A\\) has integer entries by definition it is clear that \\(\mathrm{Pdet}\\) takes values in \\(\mathbb{Z}\\). 
∎

### Elementary properties.

By combining the next few propositions, it will follow that \\(\mathrm{Pdet}\\) induces a well-defined function on lattices 
[commensurable](https://en.wikipedia.org/wiki/Commensurability_(mathematics)) to a fixed lattice in \\(\mathbb{R}^n\\). See also
[this note]({{ site.baseurl }}{% post_url 2017-02-02-conways-big-picture %}) on Conway's big picture. 

**Proposition 1.** \\(\mathrm{Pdet}\\) descends to a well-defined function
<div class="mathjax">\begin{equation*}
  \mathrm{Pdet} : \mathrm{PGL}(2;\mathbb{Q}) \longrightarrow \mathbb{Z}
\end{equation*}</div>

*Proof:* Fix any \\(A \in \mathrm{Mat}(n;\mathbb{Q})\\), and any \\(r \in \mathbb{Q}^\times\\). With the same notation as above, it is not 
hard to see that \\(\alpha_{rA} A = \alpha_A A\\). Thus we the identity
<div class="mathjax">\begin{equation*}
  \mathrm{Pdet}(rA) = \det(\alpha_{rA} rA) = \det(\alpha_A A) = \mathrm{Pdet}(A)
\end{equation*}</div>
as required.
∎

Continuing in this vein, we have:

**Proposition 2.** The restriction of \\(\mathrm{Pdet}\\) to \\(\mathrm{PGL}^+(n;\mathbb{Q})\\) induces a well-defined function
<div class="mathjax">\begin{equation*}
  \mathrm{PSL}(n;\mathbb{Z}) \backslash \mathrm{PGL}^+(n;\mathbb{Q}) \longrightarrow \mathbb{Z}_{>0}
\end{equation*}</div>

*Proof:* Positivity is immediate from the fact we restrict our domain to \\(\mathrm{GL}^+(n;\mathbb{Q}\\). 

In light of the previous proposition it suffices to show, for all \\(A \in \mathrm{SL}(n;\mathbb{Z})\\) and 
\\(X \in \mathrm{Mat}(n;\mathbb{Q})\\), we have
<div class="mathjax">\begin{equation*}
  \mathrm{Pdet}(AX) = \mathrm{Pdet}(X) = \mathrm{Pdet}(XA)
\end{equation*}</div>
To this end, notice
<div class="mathjax">\begin{equation*}
  \mathrm{Pdet}(AX) = \alpha_{AX}^n \det(AX) = \alpha_{AX}^n \det(A)\det(X) = \alpha^n_{AX}\det(X)
\end{equation*}</div>
and
<div class="mathjax">\begin{equation*}
  \mathrm{Pdet}(X) = \alpha_X^n\det(X)
\end{equation*}</div>
Thus all we need to do is prove the identity \\(\alpha_{AX} = \alpha_{X}\\) for all \\(A \in \mathrm{SL}(n;\mathbb{Z})\\). Suppose
\\(\alpha \in \mathbb{Q}\\) is such that \\(\alpha AX \in \mathrm{Mat}(n;\mathbb{Z})\\), ie \\(AX\\) has integer entries. 
Since \\(A^{-1} \in \mathrm{SL}(2;\mathbb{Z})\\), the matrix
<div class="mathjax">\begin{equation*}
  A^{-1}\alpha AX = \alpha X
\end{equation*}</div>
also has integer entries. Conversely
<div class="mathjax">\begin{equation*}
  \alpha X \in \mathrm{Mat}(n;\mathbb{Z}) \quad \Longrightarrow \quad \alpha AX \in \mathrm{Mat}(n;\mathbb{Z})
\end{equation*}</div>
As an immediate consequence, we get the following equality of sets:
<div class="mathjax">\begin{equation*}
  \left\{ \alpha \in \mathbb{Q}^+ ~|~  \alpha AX \in \mathrm{Mat}(n;\mathbb{Z}\right\} 
    =
  \left\{\alpha \in \mathbb{Q}^+ ~|~ \alpha X \in \mathrm{Mat}(n;\mathbb{Z})\right\} 
\end{equation*}</div>
Since these two sets are equal, their smallest elements are also equal. In other words, \\(\alpha_{AX} = \alpha_X\\) and we are done.
∎

In the note [Conway's Big Picture]({{ site.baseurl }}{% post_url 2017-02-02-conways-big-picture %}) we will use the rational projective
determinant to define a (hyper-)distance function on the set of projective lattices in \\(\mathbb{C}\\). 
