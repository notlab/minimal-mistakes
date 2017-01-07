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

Consider a Lie subgroup \\(G \leq \mathrm{GL}(n;\mathbb{R})\\). There are three ways to define the Lie algebra \\(\mathfrak{g}\\) of \\(G\\):

* the set of left \\(G\\)-invariant vector fields on the manifold \\(G\\);
* the tangent space \\(T_{\mathrm{id}}G\\) to the identity in \\(G\\);
* the set of matrices \\(A \in \mathrm{GL}(n;\mathbb{R})\\) such that \\(\exp(tA) \in G\\) for all \\(t \in \mathbb{R}\\). 

The equivalence of the first two is well-known and holds for general Lie groups. We give a quick argument establishing the equivalence
of the third definition. 

Let us first establish a coordinate system on \\(\mathrm{GL}(n; \mathbb{R})\\). The easiest way to do this is to identify \\(\mathrm{GL}(n;\mathbb{R})\\) with \\(\mathbb{R}^{n^2}\\). The tangent space 
\\(T_{\mathrm{id}}\mathrm{GL}(n;\mathbb{R})\\) is then seen to be another copy of \\(\mathbb{R}^{n^2}\\), and hence of \\(\mathrm{GL}(n; \mathbb{R}^2)\\). In other words, as sets we have
\\[ \mathfrak{gl}(n;\mathbb{R}) = \mathrm{GL}(n; \mathbb{R}) \\]
where \\(\mathfrak{gl}(n;\mathbb{R})\\) denotes the Lie algebra of \\(\mathrm{GL}(n;\mathbb{R})\\). 

Next, observe that \\(T_{\mathrm{id}}G \subseteq T_{\mathrm{id}}\mathrm{GL}(n;\mathbb{R})\\); in other words, we have \\(\mathfrak{g} \subseteq \mathfrak{gl}(n;\mathbb{R})\\). Together with the above, this provides a way of associating 
a matrix \\(A \in \mathrm{GL}(n; \mathbb{R})\\) to each element \\(g \in G\\). 