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

The tangent space to a manifold \\(M\\) is usually defined in terms of derivations of smooth functions on \\(M\\). While this definition
is usually sufficient, some applications benefit from a more ring-theoretic characterization. In this note we present this ring-theoretic
characterization and prove its equivalence to the standard definition.

Let us briefly recall the usual defintion of the tangent space. Suppose we are given a \\(C^\infty\\)-manifold \\(M\\) together with a
point \\(m \in M\\). A linear function \\(\delta \colon C^\infty(M) \to \mathbb{R}\\) is called a derivation at \\(m\\) if it satisfies the
following "product rule":
\\[ \delta(fg) = \delta(f) \cdot g(m) + f(m)\cdot \delta(g)\\]
It is easy to see that the set of derivations at \\(m\\) is closed under addition and scalar multiplication, and hence that it is a vector space.
The usual definition of the tangent space \\(T_mM\\) at \\(m\\) is precisely this vector space of derivations.

Now let \\(\mathcal{O}\\) denote the ring of germs of smooth functions at \\(m\\). Let
\\(\mathrm{ev}_m \colon \mathcal{O} \rightarrow \mathbb{R}\\) be the evaluation map, ie.
\\[ \mathrm{ev}_m(f) = f(m)\\]
This evaluation map is a ring homomorphism, meaning that \\(\mathfrak{m} = \mathrm{ker}(\mathrm{ev}_m)\\) is an ideal
\\(\mathcal{O}\\). Moreover, since \\(\mathbb{R} \cong \mathcal{O}/\mathfrak{m}\\) it follows that \\(\mathfrak{m}\\) is a maximal ideal.
 We show that the tangent space \\(T_mM\\) can be recharacterized as the dual space \\((\mathfrak{m}/\mathfrak{m}^2)^\ast\\). In other words,
 we exhibit an isomorphism of the form
\\[T_mM \cong (\mathfrak{m}/\mathfrak{m}^2)^\ast\\]

Let \\(\delta\\) be any derivation at \\(m\\), and suppose we are given \\(F \in \mathfrak{m}^2\\). By definition we can write \\(F = fg\\)
for some \\(f, g \in \mathcal{O}\\). Applying \\(\delta\\) we obtain
\\[\delta(F) = \delta(f)\cdot g(m) + f(m) \delta(g) = 0\\]
Thus \\(\delta\\) descends to a linear function \\(\mathfrak{m}/\mathfrak{m}^2 \to \mathbb{R}\\). Clearly unique derivations have unique images
in \\((\mathfrak{m}/\mathfrak{m}^2)^\ast\\), and so we have the inclusion
\\[T_mM \subseteq \left(\mathfrak{m}/\mathfrak{m}^2\right)^\ast\\]
To obtain the reverse inclusion, suppose we have a linear functional \\(\lambda \in \mathfrak{m}/\mathfrak{m}^2\\) and an arbitrary
\\(f \in \mathcal{O}\\). The modified function \\(f - f(m)\\) vanishes at \\(m\\), so that \\(f - f(m) \in \mathfrak{m}\\). We can therefore
define a derivation \\(\delta_\lambda\\) according to the formula
\\[\delta_\lambda(f) = \lambda(f - f(m) + \mathfrak{m}^2)\\]
The correspondence \\(\lambda \mapsto \delta_\lambda\\) is clearly injective, whence we may conclude
\\[T_mM = \mathfrak{m}/\mathfrak{m}^2\\]
as claimed. 
