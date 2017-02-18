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
In this note we define the rational projective determinant and investigate some of its elementary properties. As an aside, this paper is
a must read.

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
