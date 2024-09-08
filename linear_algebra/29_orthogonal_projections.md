# Orthogonal Projections in Linear Algebra

In linear algebra, an **orthogonal projection** is a type of linear transformation that maps a vector onto a subspace in such a way that the difference between the vector and its projection is orthogonal to the subspace. Orthogonal projections are fundamental in various areas of mathematics, including statistics, optimization, and computer graphics.

## Definition

An **orthogonal projection** onto a subspace $W$ of a vector space $V$ is a linear operator $P$ such that:

1. $P^2 = P$ (idempotent property)
2. $P^T = P$ (symmetric property for orthogonal projections)

Given a vector $\mathbf{v} \in V$, the orthogonal projection of $\mathbf{v}$ onto the subspace $W$ is the vector $P(\mathbf{v})$ in $W$ such that the difference $\mathbf{v} - P(\mathbf{v})$ is orthogonal to $W$.

## Matrix Representation

If $W$ is spanned by an orthonormal basis $\{\mathbf{u}_1, \mathbf{u}_2, \ldots, \mathbf{u}_k\}$, the orthogonal projection matrix $P$ onto $W$ is given by:

$$
P = U U^T
$$

where $U$ is an $n \times k$ matrix whose columns are the orthonormal basis vectors of $W$.

## Examples

### Example 1: Projection onto a Line in $\mathbb{R}^2$

Consider the vector space $\mathbb{R}^2$ and let $W$ be the line spanned by the vector $\mathbf{u} = \begin{pmatrix} 1 \\ 1 \end{pmatrix}$. To find the orthogonal projection of a vector $\mathbf{v} = \begin{pmatrix} x \\ y \end{pmatrix}$ onto this line:

**Step 1: Normalize $\mathbf{u}$**

First, normalize $\mathbf{u}$:

$$
\mathbf{u}_{\text{norm}} = \frac{1}{\sqrt{2}} \begin{pmatrix} 1 \\ 1 \end{pmatrix}
$$

**Step 2: Compute the Projection Matrix**

The projection matrix $P$ is:

$$
P = \mathbf{u}_{\text{norm}} \mathbf{u}_{\text{norm}}^T
= \frac{1}{2} \begin{pmatrix}
1 & 1 \\
1 & 1
\end{pmatrix}
$$

**Step 3: Project a Vector**

For $\mathbf{v} = \begin{pmatrix} 3 \\ 4 \end{pmatrix}$:

$$
P \mathbf{v} = \frac{1}{2} \begin{pmatrix}
1 & 1 \\
1 & 1
\end{pmatrix}
\begin{pmatrix}
3 \\
4
\end{pmatrix}
= \frac{1}{2} \begin{pmatrix}
7 \\
7
\end{pmatrix}
= \begin{pmatrix}
3.5 \\
3.5
\end{pmatrix}
$$

### Example 2: Projection onto a Subspace in $\mathbb{R}^3$

Consider the subspace $W$ spanned by the vectors:

$$
\mathbf{u}_1 = \begin{pmatrix}
1 \\
0 \\
0
\end{pmatrix}
, \quad
\mathbf{u}_2 = \begin{pmatrix}
0 \\
1 \\
0
\end{pmatrix}
$$

**Step 1: Form the Matrix $U$**

The matrix $U$ with columns $\mathbf{u}_1$ and $\mathbf{u}_2$ is:

$$
U = \begin{pmatrix}
1 & 0 \\
0 & 1 \\
0 & 0
\end{pmatrix}
$$

**Step 2: Compute the Projection Matrix**

The projection matrix $P$ is:

$$
P = U U^T
= \begin{pmatrix}
1 & 0 \\
0 & 1 \\
0 & 0
\end{pmatrix}
\begin{pmatrix}
1 & 0 & 0 \\
0 & 1 & 0
\end{pmatrix}
= \begin{pmatrix}
1 & 0 & 0 \\
0 & 1 & 0 \\
0 & 0 & 0
\end{pmatrix}
$$

**Step 3: Project a Vector**

For $\mathbf{v} = \begin{pmatrix} 2 \\ 3 \\ 4 \end{pmatrix}$:

$$
P \mathbf{v} = \begin{pmatrix}
1 & 0 & 0 \\
0 & 1 & 0 \\
0 & 0 & 0
\end{pmatrix}
\begin{pmatrix}
2 \\
3 \\
4
\end{pmatrix}
= \begin{pmatrix}
2 \\
3 \\
0
\end{pmatrix}
$$

### Example 3: Projection onto a Plane in $\mathbb{R}^3$

Consider the plane $W$ in $\mathbb{R}^3$ defined by the normal vector $\mathbf{n} = \begin{pmatrix} 1 \\ 1 \\ 1 \end{pmatrix}$.

**Step 1: Normalize $\mathbf{n}$**

The normalized normal vector is:

$$
\mathbf{n}_{\text{norm}} = \frac{1}{\sqrt{3}} \begin{pmatrix} 1 \\ 1 \\ 1 \end{pmatrix}
$$

**Step 2: Compute the Projection Matrix**

The projection matrix $P$ onto the plane orthogonal to $\mathbf{n}_{\text{norm}}$ is:

$$
P = I - \mathbf{n}_{\text{norm}} \mathbf{n}_{\text{norm}}^T
= I - \frac{1}{3} \begin{pmatrix}
1 & 1 & 1 \\
1 & 1 & 1 \\
1 & 1 & 1
\end{pmatrix}
= \begin{pmatrix}
\frac{2}{3} & -\frac{1}{3} & -\frac{1}{3} \\
-\frac{1}{3} & \frac{2}{3} & -\frac{1}{3} \\
-\frac{1}{3} & -\frac{1}{3} & \frac{2}{3}
\end{pmatrix}
$$

**Step 3: Project a Vector**

For $\mathbf{v} = \begin{pmatrix} 1 \\ 2 \\ 3 \end{pmatrix}$:

$$
P \mathbf{v} = \begin{pmatrix}
\frac{2}{3} & -\frac{1}{3} & -\frac{1}{3} \\
-\frac{1}{3} & \frac{2}{3} & -\frac{1}{3} \\
-\frac{1}{3} & -\frac{1}{3} & \frac{2}{3}
\end{pmatrix}
\begin{pmatrix}
1 \\
2 \\
3
\end{pmatrix}
= \begin{pmatrix}
1 \\
2 \\
3
\end{pmatrix}
$$

Note that in this case, the vector $\mathbf{v}$ already lies in the plane, so the projection is the vector itself.

## Summary

Orthogonal projections are linear transformations that map vectors onto a subspace while ensuring that the difference between the original vector and its projection is orthogonal to the subspace. They are essential for understanding vector decompositions and solving problems in various applications. The matrix representing an orthogonal projection can be computed using the basis vectors of the subspace and is often used to simplify and solve linear systems.
