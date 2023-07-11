---
layout: post
title:  "Welcome TWO Jekyll! This is a very, very, very long title to see if wrapping a title in a collapsible works"
date:   2023-07-04 21:11:53 -0700
categories: jekyll update
---
This equation, $e^{i\pi} = -1$, is an inline Latex expression.
On the other hand, this one gets its own paragraph:

$$
e^{i\pi} = -1
$$

Check out [this link](https://stackoverflow.com/questions/26275645/how-to-support-latex-in-github-pages) for more information.

Jekyll also offers powerful support for code snippets:

```python
def foo():
  pass # whatever
```

```cpp
void foo() {%raw%}{{%endraw%}
  return 0;
{%raw%}}{%endraw%}
```

I just lost all my work. :(

General summary:
- Reviewed cross products and determinants.

----
Highlight of my notes:
- Cofactors are the way to go. Where the heck does the determinant come from anyway? What does it have to do with cross products?

$$

\begin{align*}
\text{cross products have nice properties (area)} &\rightarrow \text{area formed by transformed basis vectors}
\\ &\rightarrow \text{size of a matrix defined to be that area}
\\ &\rightarrow \text{algebraic formula for determinant involves cofactors}
\end{align*}

$$

- Row/col operations help with minor expansion.


Cross product, $\overset{\rightharpoonup}{% raw %}{{% endraw%}x{% raw %}}{% endraw%} =\overset{\rightharpoonup}{v}\times \overset{\rightharpoonup}{w}$, properties:
1. Perpendicular: $\overset{\rightharpoonup}{x}\cdot \overset{\rightharpoonup}{v}=\overset{\rightharpoonup}{x}\cdot\overset{\rightharpoonup}{w}=0$
2. Area: $\overset{\rightharpoonup}{x}=\text{area of parallelogram spanned by}\overset{\rightharpoonup}{v} \text{ and } \overset{\rightharpoonup}{w}=\|\|\overset{\rightharpoonup}{v}\|\| \text{ } \|\|\overset{\rightharpoonup}{w}\|\| \sin\theta$
3. Sign (right hand rule): index along axis of first, middle finger along second.

Direct calculation of determinant:
1. Pick a row or column.
2. For each entry, cross out the row and column its in. For the leftover submatrix (==**minor**==), calculate its determinant. Multiply it with the entry, creating a product called the ==**cofactor**==.
3. The sign of that term is $(-1)^{i+j}$ (1-indexed). Easier to remember that the top left term is positive and just alternate from there as you move across.

Row/col operations to make it easier:
1. Add/subtract a multiple of a row or column from another row or column preserves the determinant.

Note that $(1)$ implies a few things almost directly:
1. Same row/col $\rightarrow$ determinant is 0
2. Multiplying a row by a constant also scales the determinant directly.
$(1)$ just makes the cofactor expansion so much nicer as you can get 0's pretty easily. For example, triangular matrices have determinants equal to the product of the entries along the diagonal.

There's a section up ahead that deals with inequality so that max/min f problem from yesterday could be solved reading up ahead a bit. But I wonder if there's a way to do it without the chapter on inequalities.

