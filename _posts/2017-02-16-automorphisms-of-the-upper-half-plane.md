---
title: "Automorphisms of the Upper Half Plane"
categories:
  - Automorphic Forms
  - Hyperbolic Geometry
tags:
  - geometry
  - hyperbolic
---

In this note we study the group \\(\mathrm{Aut}(\mathbb{H})\\) of analytic automorpisms of the upper half plane. We review the usual 
classification of such automorphisms based on their fixed points on the Riemann sphere \\(\mathbb{PC}^1\\), and investigate certain subgroups 
occuring frequently in applications. It is well known that \\(\mathrm{Aut}(\mathbb{H})\\) can be described explicitly via the isomorphisms
<div class="mathjax">\begin{equation*}
  \mathrm{GL}^+(2;\mathbb{R})/\mathbb{R}^\times \cong 
  \mathrm{SL}(2;\mathbb{R}) / \{\pm 1\} \cong
  \mathrm{Aut}(\mathbb{H})
\end{equation*}</div>
where the groups \\(\mathrm{GL}^+(2;\mathbb{R})\\) and \\(\mathrm{SL}(2;\mathbb{R})\\) act by fractional linear transformations. We make use of 
these identifications implicitly throughout. 

## Classification of automorphisms

In this section we derive a classification of the elements of \\(\mathrm{Aut}(\mathbb{H})\\) based on their fixed points. Let 
\\(g = \left(\begin{smallmatrix} a & b  \\\\ c & d \end{smallmatrix}\right) \in \mathrm{GL}^+(2;\mathbb{R})\\) by an arbitrary automorphism,
and suppose \\(z\\) is a fixed point of \\(g\\). Note that
<div class="mathjax">\begin{equation*}
  g\cdot\infty = \frac{a\infty + b}{c\infty + d} = \frac{a}{c} 
\end{equation*}</div>
so that \\(g\\) fixes \\(\infty\\) if and only if \\(c = 0\\). We consider the cases \\(c \ne 0\\) and \\(c = 0\\) separately.

**Case 1:** \\(c \ne 0\\). In this case we can also suppose \\(z \ne \infty\\). Then we have
<div class="mathjax">\begin{equation*}
  g\cdot z = \frac{az + b}{cz + d} = z
    \quad \Longrightarrow \quad
  cz^2 + (d-a)z - b = 0
\end{equation*}</div>
Since \\(c \ne 0\\) the quadratic equation gives solutions
<div class="mathjax">\begin{equation*}
  \frac{-(d-a) \pm \sqrt{(d-a)^2 + 4cb}}{2c} 
\end{equation*}</div>
The discriminant of the above is given by
<div class="mathjax">\begin{equation*}
  (d-a)^2 +4cb = \mathrm{tr}(g)^2 - 4 \mathrm{det}(g)
\end{equation*}</div>
We can conclude that:

- \\(\mathrm{tr}(g)^2 > 4\mathrm{det}(g)\\) implies \\(g\\) has two distinct fixed points \\(\in \mathbb{R}\\). 
- \\(\mathrm{tr}(g)^2 = 4\mathrm{det}(g)\\) implies \\(g\\) has a single fixed point \\(\in \mathbb{R}\\).
- \\(\mathrm{tr}(g)^2 < 4\mathrm{det}(g)\\) implies \\(g\\) has two distinct fixed points \\(z, \bar{z} \in \mathbb{C} \setminus \mathbb{R}\\). 

**Case 2:** \\(c = 0\\) In this case, \\(\infty\\) is automatically a fixed point of \\(g\\). For \\(z\ne \infty\\) we have
<div class="mathjax">\begin{equation*}
  g\cdot z = \frac{a}{d} z + \frac{b}{d} 
\end{equation*}</div>
If \\(a = d\\) then this is simply the map \\(z\mapsto z + b/d\\) which clearly has a single fixed point at \\(\infty \in \mathbb{PC}^1\\)
Moreover, note that \\(a = d\\) implies \\(\mathrm{tr}(g)^2 = 4 \mathrm{det}(g)\\). If \\(a \ne d\\) then solving the fixed point 
equation \\(z = g\cdot z\\) for \\(z\\) yields
<div class="mathjax">\begin{equation*}
  z = \frac{b}{d-a} 
\end{equation*}</div>
In other words, \\(a \ne d\\) implies \\(g\\) has two fixed points, \\(b/(d-a)\\) and \\(\infty\\). We also have 
\\(\mathrm{tr}(g)^2 > 4 \mathrm{det}(g)\\) in this case. 

Inspired by the roles of \\(\mathrm{tr}(g)\\) and \\(\mathrm{det}\\) in the above argument, we make the following definitions:

**Definition 1:** We say that \\(g = \left(\begin{smallmatrix} a & b  \\\\ c & d \end{smallmatrix}\right) \in \mathrm{Aut}(\mathbb{H})\\)
is

- *hyperbolic* if \\(\mathrm{tr}(g)^2 > 4\mathrm{det}(g)\\);
- *parabolic* if \\(\mathrm{tr}(g)^2 = 4\mathrm{det}(g)\\);
- *elliptic* if \\(\mathrm{tr}(g)^2 < 4\mathrm{det}(g)\\).
∎

Using this terminology and Combining cases 1 and 2, we arrive at a classification of elements in \\(\mathrm{Aut}(\mathbb{H})\\) based on their
fixed points in \\(\mathbb{PC}^1\\):

**Theorem 1:** Let \\(g \in \mathrm{Aut}(\mathbb{H})\\) be arbitrary. Then

- \\(g\\) hyperbolic implies \\(g\\) has two distinct fixed points \\(\in \mathbb{R} \cup \infty\\);
- \\(g\\) parabolic implies \\(g\\) has a single fixed point \\(\in \mathbb{R} \cup \infty\\).
- \\(g\\) elliptic implies \\(g\\) has two distinct fixed points \\(z, \bar{z} \in \mathbb{C} \setminus (\mathbb{R} \cup \infty)\\).
∎


### Stabilizer subgroups

For convenience, we introduce the following notation for certain stabilizer subgroups.

**Definition 2:** Let \\(z \in \mathbb{H} \cup \mathbb{R} \cup \{\infty \}\\). We set 
<div class="mathjax">\begin{align*}
  \mathrm{GL}^+(2;\mathbb{R})_z &:= \text{ stabilizer of } z \text{ in } \mathbb{GL}^+(2;\mathbb{R}) \\
  \mathrm{GL}^+(2;\mathbb{R})^{(p)}_z &:= \text{ parabolic elements of } \mathrm{GL}^+(2;\mathbb{R})_z
\end{align*}</div>
The group \\(\mathrm{GL}^+(2; \mathbb{R})^{(p)}_z\\) is called the *parabolic stabilizer* of \\(z\\).
∎

The next result is immediate from our discussion on the first section.

**Theorem 2:** The stabilizer of \\(\infty\\) in \\(\mathrm{GL}^+(2; \mathbb{R})\\) is given by
<div class="mathjax">\begin{equation*}
  \mathrm{GL}^+(2;\mathbb{R})_z = \left\{ \begin{pmatrix}
  a & b \\
  0 & d
  \end{pmatrix} ~\colon~ a, d \in \mathbb{R},~ ad > 0,~ b \in \mathbb{R}\right\} 
\end{equation*}</div>
while the parabolic stabilizer is
<div class="mathjax">\begin{equation*}
  \mathrm{GL}^+(2;\mathbb{R})^{(p)}_z = \left\{ \begin{pmatrix}
  a & b \\
  0 & a
  \end{pmatrix} ~\colon~ a \in \mathbb{R} \setminus \{0\},~ b \in \mathbb{R}\right\} 
\end{equation*}</div>
∎

**Theorem 3:** The stabilizer of \\(i\\) is \\(\mathbb{R}^\times \times \mathbb{SO}(2;\mathbb{R})\\).

*Proof:* 
Suppose \\(g = \left(\begin{smallmatrix} a & b  \\\\ c & d \end{smallmatrix}\right) \in \mathbb{GL}^+(2;\mathbb{R})\\) stabilizes 
\\(i \in \mathbb{H}\\). We have
<div class="mathjax">\begin{equation*}
  \frac{ai + b}{ci + d}  = i \quad \Leftrightarrow \quad ai + b = -c + di
\end{equation*}</div>
So it is necessary that \\(a = d\\) and \\(b = -c\\); in other words, 
\\(g = \left(\begin{smallmatrix} a & b  \\\\ -b & a \end{smallmatrix}\right)\\). Computing the determinant gives
\\(\mathrm{det} \left(\begin{smallmatrix} a & b  \\\\ -b & a \end{smallmatrix} \right) = a^2 + b^2 = R\\) for some 
\\(R > 0\\). The matrices satisfying this equation are precisely those of the form
\\(\pm \sqrt{R} \cdot \left(\begin{smallmatrix} \cos(\theta) & \sin(\theta)  \\\\ -\sin(\theta) & \cos(\theta) \end{smallmatrix} \right)\\)
with \\(\theta \in [0, 2\pi)\\). But this set is precisely \\(\mathbb{R}^\times \times \mathbb{SO}(2;\mathbb{R})\\), so we are done. 
∎
