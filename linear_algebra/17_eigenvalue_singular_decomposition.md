# Eigenvalue Decomposition in Linear Algebra

**Eigenvalue decomposition** (or spectral decomposition) is a technique in linear algebra used to simplify the analysis of linear transformations. It is particularly useful for understanding matrix properties and solving systems of linear equations.

## Definition

Given a square matrix $A$ of size $n \times n$, the matrix can be decomposed into a product of three matrices if $A$ is diagonalizable. Specifically:

$$
A = PDP^{-1}
$$

where:
- $P$ is a matrix whose columns are the eigenvectors of $A$,
- $D$ is a diagonal matrix containing the eigenvalues of $A$,
- $P^{-1}$ is the inverse of the matrix $P$.

### Conditions for Eigenvalue Decomposition

For a matrix $A$ to be decomposed into $PDP^{-1}$:
1. $A$ must be a square matrix.
2. $A$ must have $n$ linearly independent eigenvectors, which means $A$ must be diagonalizable.

## Example

Consider the matrix:

$$
A = \begin{pmatrix}
4 & 1 \\
2 & 3
\end{pmatrix}
$$

**Step 1: Find the Eigenvalues**

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
   Thus:
   $$
   \text{det}(A - \lambda I) = \lambda^2 - 7\lambda + 10
   $$
   Set the polynomial to zero and solve for $\lambda$:
   $$
   \lambda^2 - 7\lambda + 10 = 0
   $$
   Factor the quadratic equation:
   $$
   (\lambda - 2)(\lambda - 5) = 0
   $$
   So, the eigenvalues are:
   $$
   \lambda_1 = 2 \quad \text{and} \quad \lambda_2 = 5
   $$

**Step 2: Find the Eigenvectors**

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

**Step 3: Form the Matrix $P$ and $D$**

- Matrix $P$ (columns are eigenvectors):
  $$
  P = \begin{pmatrix}
  1 & 1 \\
  -2 & 1
  \end{pmatrix}
  $$
- Diagonal matrix $D$ (eigenvalues on the diagonal):
  $$
  D = \begin{pmatrix}
  2 & 0 \\
  0 & 5
  \end{pmatrix}
  $$

**Step 4: Compute $P^{-1}$**

Compute the inverse of $P$:
$$
P^{-1} = \frac{1}{\text{det}(P)} \text{adj}(P)
$$
Where $\text{det}(P) = 1 \cdot 1 - (-2 \cdot 1) = 3$, and $\text{adj}(P)$ is the adjugate of $P$.

Thus:
$$
P^{-1} = \frac{1}{3} \begin{pmatrix}
1 & -1 \\
2 & 1
\end{pmatrix}
$$

**Step 5: Verify the Decomposition**

Verify:
$$
A = PDP^{-1}
$$
Calculate:
$$
PDP^{-1} = \begin{pmatrix}
1 & 1 \\
-2 & 1
\end{pmatrix}
\begin{pmatrix}
2 & 0 \\
0 & 5
\end{pmatrix}
\frac{1}{3} \begin{pmatrix}
1 & -1 \\
2 & 1
\end{pmatrix}
$$

Perform the matrix multiplication to confirm the equality.

## Summary

Eigenvalue decomposition is a powerful tool for matrix analysis, particularly useful in simplifying matrix operations and understanding matrix properties. The decomposition $A = PDP^{-1}$ allows us to express matrix $A$ in terms of its eigenvalues and eigenvectors, facilitating easier computation and insight into the matrix's behavior.
