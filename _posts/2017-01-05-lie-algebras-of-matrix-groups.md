---
title: "Lie Algebras of Matrix Groups"
categories:
  - Lie Theory
tags:
  - mathematics
  - lie
  - algebra
  - math
  - geometry
---

Let \\(G \leq \mathrm{GL}(n;\mathbb{R})\\) be a Lie group. Denote the Lie algebras of \\(G\\) and \\(\mathrm{GL}(n;\mathbb{R})\\) by
\\(\mathfrak{g}\\) and \\(\mathfrak{gl}(n;\mathbb{R})\\) respectively. We usually define the Lie algebra \\(\mathfrak{g}\\) to be the
space of left \\(G\\)-invariant vector fields on \\(G\\), ie. the set of vector fields \\(\mathcal{X}\\) such that, for all \\(g,a\in G\\)
we have
<div>\begin{equation}
\mathcal{X}_{g\cdot a} = (L_g)_\ast \mathcal{X}_a
\end{equation}</div>
Here the diffeomorphism \\(L_g \in \mathrm{Diff}(G)\\) is left multiplication by \\(g\\). It is well known that \\(\mathfrak{g}\\) is
isomorphic to the tangent space \\(T_{\mathrm{id}}G\\) and these two spaces are usually identified. In this note we prove a further
equivalence of the form
\\[\mathfrak{g} \cong \\{ A \in \mathrm{Mat}(n; \mathbb{R}) ~|~ \exp(tA) \in G \text{ for all } t \in \mathbb{R}\\}\\]
which holds for matrix groups like \\(G\\). 

Let us first consider the manifold \\(\mathrm{Mat}(n;\mathbb{R})\\) with coordinates \\((x_{ij})\\). The corresponding derivations
\\(\\{\frac{\partial}{\partial x^{ij}}\\}\\) span the tangent space \\(T_{\mathrm{id}}\mathrm{Mat}(n;\mathbb{R})\\), which we
can therefore think of as another copy of \\(\mathrm{Mat}(n;\mathbb{R})\\). Since \\(\mathfrak{g}\\) is a subspace of
\\(T_{\mathrm{id}}\mathrm{Mat}(n;\mathbb{R})\\), this gives us a way to identify elements of \\(\mathfrak{g}\\) with \\(n\times n\\)-matrices. 

Exploiting the identification above, suppose we are given some \\(n\times n\\) matrix \\(A\\) representing a vector in \\(\mathfrak{g}\\).
Viewing \\(\mathfrak{g}\\) as the space of left invariant vector fields on \\(G\\), \\(A\\) corresponds to the matrix differential equation
\\[\frac{\mathrm{d}X}{\mathrm{d}t} = A X\\]
which has as solution the matrix exponential \\(t \mapsto \exp(tA)\\). Since \\(\exp(tA)\\) is a flow on the manifold \\(G\\), it follows that
\\(\exp(tA) \in G\\) for all \\(t \in \mathbb{R}\\). Conversely, suppose we are given a matrix \\(A\\) such that \\(\exp(tA) \in G\\) for all
real \\(t\\). By the uniqueness theorem for systems of differential equations, \\(A\\) must be the coordinate representation of a vector field
tangent to the manifold \\(G\\). In other words, \\(A \in \mathfrak{g}\\) and we are done.
