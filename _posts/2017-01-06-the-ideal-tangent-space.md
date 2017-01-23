---
title: "The Ideal Tangent Space"
categories:
  - Geometry
  - Algebra
tags:
  - mathematics
  - geometry
  - algebra
  - tangent-space
---

The tangent space to a manifold \\(M\\) is usually defined in terms of derivations of smooth functions on \\(M\\). This definition works most
of the time, but some applications benefit from a more ring-theoretic characterization. In this note we present this ring-theoretic
characterization and prove its equivalence to the standard definition.

## Tangent space as derivations

Suppose we are given a \\(C^\infty\\)-manifold \\(M\\) together with a point \\(m \in M\\). A linear function
\\(\delta \colon C^\infty(M) \to \mathbb{R}\\) is called a derivation at \\(m\\) if it satisfies the following "product rule":
<div class="mathjax">\begin{equation*}
\delta(fg) = \delta(f) g(m) + f(m) \delta(g)
\end{equation*}</div>
It is easy to see that the set of derivations at \\(m\\) is closed under addition and scalar multiplication, and hence that it is a vector space.
The usual definition of the tangent space \\(T_mM\\) is precisely this vector space of derivations.

## Ring theoretic tangent space

Now let \\(\mathcal{O}\\) denote the ring of germs of smooth functions at \\(m\\). Let
\\(\mathrm{ev}_m \colon \mathcal{O} \rightarrow \mathbb{R}\\) be the evaluation map, ie.
<div class="mathjax">\begin{equation*}
\mathrm{ev}_m(f) = f(m)
\end{equation*}</div>
This evaluation map is a ring homomorphism, meaning that \\(\mathfrak{m} = \mathrm{ker}(\mathrm{ev}_m)\\) is an ideal of
\\(\mathcal{O}\\). Moreover, \\(\mathbb{R} \cong \mathcal{O}/\mathfrak{m}\\) implies \\(\mathfrak{m}\\) is maximal.
 We show that the tangent space \\(T_mM\\) can be recharacterized as the dual space \\((\mathfrak{m}/\mathfrak{m}^2)^\ast\\). In other words,
 we exhibit an isomorphism of the form
<div class="mathjax">\begin{equation*}
T_mM \cong (\mathfrak{m}/\mathfrak{m}^2)^\ast
\end{equation*}</div>

Let \\(\delta\\) be any derivation at \\(m\\), and suppose we are given \\(F \in \mathfrak{m}^2\\). By definition we can write \\(F = fg\\)
for some \\(f, g \in \mathcal{O}\\). Applying \\(\delta\\) we obtain
<div class="mathjax">\begin{equation*}\delta(F) = \delta(f) g(m) + f(m) \delta(g) = 0\end{equation*}</div>
Thus \\(\delta\\) descends to a linear function \\(\mathfrak{m}/\mathfrak{m}^2 \to \mathbb{R}\\). Clearly unique derivations have unique images
in \\((\mathfrak{m}/\mathfrak{m}^2)^\ast\\), and so we have the inclusion
<div class="mathjax">\begin{equation*}T_mM \subseteq \left(\mathfrak{m}/\mathfrak{m}^2\right)^\ast\end{equation*}</div>
To obtain the reverse inclusion, suppose we have a linear functional \\(\lambda \in (\mathfrak{m}/\mathfrak{m}^2)^\ast\\) and an arbitrary
\\(f \in \mathcal{O}\\). The modified function \\(f - f(m)\\) vanishes at \\(m\\), so that \\(f - f(m) \in \mathfrak{m}\\). We can therefore
define a derivation \\(\delta_\lambda\\) according to the formula
<div class="mathjax">\begin{equation*}\delta_\lambda(f) = \lambda(f - f(m) + \mathfrak{m}^2)\end{equation*}</div>
The correspondence \\(\lambda \mapsto \delta_\lambda\\) is clearly injective, whence we may conclude
<div class="mathjax">\begin{equation*}T_mM = \mathfrak{m}/\mathfrak{m}^2\end{equation*}</div>
as claimed. 
