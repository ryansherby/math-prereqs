# Eigenvalues and Eigenvectors in Linear Algebra

In linear algebra, **eigenvalues** and **eigenvectors** are fundamental concepts used in various applications, including stability analysis, vibration analysis, and principal component analysis. They provide insights into the properties of linear transformations and matrices.

## Definition of Eigenvalues and Eigenvectors

Given a square matrix $A$ of size $n \times n$, an eigenvalue $\lambda$ and its corresponding eigenvector $v$ are defined by the following equation:
$$
A v = \lambda v
$$

where:
- $A$ is a square matrix.
- $v$ is a non-zero vector (eigenvector).
- $\lambda$ is a scalar (eigenvalue).

In other words, when the matrix $A$ acts on the vector $v$, the result is a scaled version of $v$, with the scaling factor being the eigenvalue $\lambda$.

## Finding Eigenvalues and Eigenvectors

### 1. Eigenvalues

To find the eigenvalues of a matrix $A$, we need to solve the characteristic equation:
$$
\det(A - \lambda I) = 0
$$

where:
- $\det$ denotes the determinant of a matrix.
- $I$ is the identity matrix of the same size as $A$.
- $\lambda$ represents the eigenvalue.

### 2. Eigenvectors

Once the eigenvalues $\lambda$ are determined, the corresponding eigenvectors can be found by solving:
$$
(A - \lambda I) v = 0
$$

where $v$ is the eigenvector associated with the eigenvalue $\lambda$.

## Examples

### Example 1: 2x2 Matrix

Consider the matrix:
$$
A = \begin{pmatrix}
4 & 1 \\
2 & 3
\end{pmatrix}
$$

**1. Find the Eigenvalues**

1. Compute the characteristic polynomial:
   $$
   \text{det}(A - \lambda I) = \text{det}\begin{pmatrix}
   4 - \lambda & 1 \\
   2 & 3 - \lambda
   \end{pmatrix}
   $$
   Calculate the determinant:
   $$
   \text{det}\begin{pmatrix}
   4 - \lambda & 1 \\
   2 & 3 - \lambda
   \end{pmatrix} = (4 - \lambda)(3 - \lambda) - 2 \cdot 1
   $$
   Expand the product:
   $$
   (4 - \lambda)(3 - \lambda) = 12 - 4\lambda - 3\lambda + \lambda^2
   $$
   So:
   $$
   \text{det}\begin{pmatrix}
   4 - \lambda & 1 \\
   2 & 3 - \lambda
   \end{pmatrix} = \lambda^2 - 7\lambda + 12 - 2 = \lambda^2 - 7\lambda + 10
   $$
   Set the polynomial equal to zero and solve for $\lambda$:
   $$
   \lambda^2 - 7\lambda + 10 = 0
   $$
   Factor the quadratic equation:
   $$
   (\lambda - 2)(\lambda - 5) = 0
   $$
   Thus, the eigenvalues are:
   $$
   \lambda_1 = 2 \quad \text{and} \quad \lambda_2 = 5
   $$

**2. Find the Eigenvectors**

- For $\lambda_1 = 2$:
  $$
  (A - \lambda_1 I) = \begin{pmatrix}
  4 - 2 & 1 \\
  2 & 3 - 2
  \end{pmatrix} = \begin{pmatrix}
  2 & 1 \\
  2 & 1
  \end{pmatrix}
  $$
  Solve:
  $$
  \begin{pmatrix}
  2 & 1 \\
  2 & 1
  \end{pmatrix} \begin{pmatrix}
  x_1 \\
  x_2
  \end{pmatrix} = \begin{pmatrix}
  0 \\
  0
  \end{pmatrix}
  $$
  This simplifies to:
  $$
  2x_1 + x_2 = 0
  $$
  Solving for $x_2$:
  $$
  x_2 = -2x_1
  $$
  An eigenvector corresponding to $\lambda_1 = 2$ is:
  $$
  v_1 = \begin{pmatrix}
  1 \\
  -2
  \end{pmatrix}
  $$

- For $\lambda_2 = 5$:
  $$
  (A - \lambda_2 I) = \begin{pmatrix}
  4 - 5 & 1 \\
  2 & 3 - 5
  \end{pmatrix} = \begin{pmatrix}
  -1 & 1 \\
  2 & -2
  \end{pmatrix}
  $$
  Solve:
  $$
  \begin{pmatrix}
  -1 & 1 \\
  2 & -2
  \end{pmatrix} \begin{pmatrix}
  x_1 \\
  x_2
  \end{pmatrix} = \begin{pmatrix}
  0 \\
  0
  \end{pmatrix}
  $$
  This simplifies to:
  $$
  -x_1 + x_2 = 0
  $$
  Solving for $x_2$:
  $$
  x_2 = x_1
  $$
  An eigenvector corresponding to $\lambda_2 = 5$ is:
  $$
  v_2 = \begin{pmatrix}
  1 \\
  1
  \end{pmatrix}
  $$

### Example 2: 3x3 Matrix

Consider the matrix:
$$
A = \begin{pmatrix}
2 & 1 & 0 \\
1 & 2 & 1 \\
0 & 1 & 2
\end{pmatrix}
$$

**1. Find the Eigenvalues**

1. Compute the characteristic polynomial:
   $$
   \text{det}(A - \lambda I) = \text{det}\begin{pmatrix}
   2 - \lambda & 1 & 0 \\
   1 & 2 - \lambda & 1 \\
   0 & 1 & 2 - \lambda
   \end{pmatrix}
   $$
   Calculate the determinant using cofactor expansion along the first row:
   $$
   \text{det}(A - \lambda I) = (2 - \lambda) \text{det}\begin{pmatrix}
   2 - \lambda & 1 \\
   1 & 2 - \lambda
   \end{pmatrix} - 1 \text{det}\begin{pmatrix}
   1 & 1 \\
   0 & 2 - \lambda
   \end{pmatrix}
   $$
   Compute the 2x2 determinants:
   $$
   \text{det}\begin{pmatrix}
   2 - \lambda & 1 \\
   1 & 2 - \lambda
   \end{pmatrix} = (2 - \lambda)^2 - 1
   $$
   Simplify:
   $$
   (2 - \lambda)^2 - 1 = \lambda^2 - 4\lambda + 4 - 1 = \lambda^2 - 4\lambda + 3
   $$
   And:
   $$
   \text{det}\begin{pmatrix}
   1 & 1 \\
   0 & 2 - \lambda
   \end{pmatrix} = 1 \cdot (2 - \lambda) - 0 = 2 - \lambda
   $$
   So:
   $$
   \text{det}(A - \lambda I) = (2 - \lambda)(\lambda^2 - 4\lambda + 3) - (2 - \lambda)
   $$
   Factor out $(2 - \lambda)$:
   $$
   \text{det}(A - \lambda I) = (2 - \lambda)\left[(\lambda^2 - 4\lambda + 3) - 1\right]
   $$
   Simplify:
   $$
   (\lambda^2 - 4\lambda + 3) - 1 = \lambda^2 - 4\lambda + 2
   $$
   Therefore:
   $$
   \text{det}(A - \lambda I) = (2 - \lambda)(\lambda^2 - 4\lambda + 2)
   $$
   Set the polynomial to zero and solve:
   $$
   (2 - \lambda)(\lambda^2 - 4\lambda + 2) = 0
   $$
   The eigenvalues are:
   $$
   \lambda_1 = 2
   $$
   Solve:
   $$
   \lambda^2 - 4\lambda + 2 = 0
   $$
   Using the quadratic formula:
   $$
   \lambda = \frac{-b \pm \sqrt{b^2 - 4ac}}{2a}
   $$
   For $a = 1$, $b = -4$, and $c = 2$:
   $$
   \lambda = \frac{4 \pm \sqrt{16 - 8}}{2} = \frac{4 \pm \sqrt{8}}{2} = \frac{4 \pm 2\sqrt{2}}{2} = 2 \pm \sqrt{2}
   $$
   So the eigenvalues are:
   $$
   \lambda_2 = 2 + \sqrt{2} \quad \text{and} \quad \lambda_3 = 2 - \sqrt{2}
   $$

**2. Find the Eigenvectors**

- For $\lambda_1 = 2$:
  $$
  (A - \lambda_1 I) = \begin{pmatrix}
  2 - 2 & 1 & 0 \\
  1 & 2 - 2 & 1 \\
  0 & 1 & 2 - 2
  \end{pmatrix} = \begin{pmatrix}
  0 & 1 & 0 \\
  1 & 0 & 1 \\
  0 & 1 & 0
  \end{pmatrix}
  $$
  Solve:
  $$
  \begin{pmatrix}
  0 & 1 & 0 \\
  1 & 0 & 1 \\
  0 & 1 & 0
  \end{pmatrix} \begin{pmatrix}
  x_1 \\
  x_2 \\
  x_3
  \end{pmatrix} = \begin{pmatrix}
  0 \\
  0 \\
  0
  \end{pmatrix}
  $$
  This simplifies to:
  $$
  x_2 = 0
  $$
  $$
  x_1 + x_3 = 0 \implies x_3 = -x_1
  $$
  Hence, an eigenvector corresponding to $\lambda_1 = 2$ is:
  $$
  v_1 = \begin{pmatrix}
  1 \\
  0 \\
  -1
  \end{pmatrix}
  $$

- For $\lambda_2 = 2 + \sqrt{2}$:
  $$
  (A - \lambda_2 I) = \begin{pmatrix}
  2 - (2 + \sqrt{2}) & 1 & 0 \\
  1 & 2 - (2 + \sqrt{2}) & 1 \\
  0 & 1 & 2 - (2 + \sqrt{2})
  \end{pmatrix} = \begin{pmatrix}
  -\sqrt{2} & 1 & 0 \\
  1 & -\sqrt{2} & 1 \\
  0 & 1 & -\sqrt{2}
  \end{pmatrix}
  $$
  Solve:
  $$
  \begin{pmatrix}
  -\sqrt{2} & 1 & 0 \\
  1 & -\sqrt{2} & 1 \\
  0 & 1 & -\sqrt{2}
  \end{pmatrix} \begin{pmatrix}
  x_1 \\
  x_2 \\
  x_3
  \end{pmatrix} = \begin{pmatrix}
  0 \\
  0 \\
  0
  \end{pmatrix}
  $$
  This simplifies to:
  $$
  -\sqrt{2}x_1 + x_2 = 0 \implies x_2 = \sqrt{2}x_1
  $$
  $$
  x_1 - \sqrt{2}x_2 + x_3 = 0 \implies x_3 = -x_1 + \sqrt{2}x_2
  $$
  Substituting $x_2 = \sqrt{2}x_1$ into the equation for $x_3$:
  $$
  x_3 = -x_1 + \sqrt{2}(\sqrt{2}x_1) = -x_1 + 2x_1 = x_1
  $$
  Hence, an eigenvector corresponding to $\lambda_2 = 2 + \sqrt{2}$ is:
  $$
  v_2 = \begin{pmatrix}
  1 \\
  \sqrt{2} \\
  1
  \end{pmatrix}
  $$

- For $\lambda_3 = 2 - \sqrt{2}$:
  $$
  (A - \lambda_3 I) = \begin{pmatrix}
  2 - (2 - \sqrt{2}) & 1 & 0 \\
  1 & 2 - (2 - \sqrt{2}) & 1 \\
  0 & 1 & 2 - (2 - \sqrt{2})
  \end{pmatrix} = \begin{pmatrix}
  \sqrt{2} & 1 & 0 \\
  1 & \sqrt{2} & 1 \\
  0 & 1 & \sqrt{2}
  \end{pmatrix}
  $$
  Solve:
  $$
  \begin{pmatrix}
  \sqrt{2} & 1 & 0 \\
  1 & \sqrt{2} & 1 \\
  0 & 1 & \sqrt{2}
  \end{pmatrix} \begin{pmatrix}
  x_1 \\
  x_2 \\
  x_3
  \end{pmatrix} = \begin{pmatrix}
  0 \\
  0 \\
  0
  \end{pmatrix}
  $$
  This simplifies to:
  $$
  \sqrt{2}x_1 + x_2 = 0 \implies x_2 = -\sqrt{2}x_1
  $$
  $$
  x_1 + \sqrt{2}x_2 + x_3 = 0 \implies x_3 = -x_1 - \sqrt{2}x_2
  $$
  Substituting $x_2 = -\sqrt{2}x_1$ into the equation for $x_3$:
  $$
  x_3 = -x_1 - \sqrt{2}(-\sqrt{2}x_1) = -x_1 + 2x_1 = x_1
  $$
  Hence, an eigenvector corresponding to $\lambda_3 = 2 - \sqrt{2}$ is:
  $$
  v_3 = \begin{pmatrix}
  1 \\
  -\sqrt{2} \\
  1
  \end{pmatrix}
  $$

## Conclusion

Eigenvalues and eigenvectors are crucial in understanding the behavior of linear transformations and matrices. Eigenvalues provide insight into how the matrix scales space, while eigenvectors indicate directions that are scaled by the matrix. These concepts are widely used in various fields, including physics, computer science, and engineering.
