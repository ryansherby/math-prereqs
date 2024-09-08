# Singular Value Decomposition (SVD) in Linear Algebra

**Singular Value Decomposition (SVD)** is a fundamental matrix factorization technique used in linear algebra. It decomposes a matrix into three other matrices, providing insight into its structure and properties. SVD is particularly useful in numerical analysis, signal processing, and statistics.

## Definition

Given an $m \times n$ matrix $A$, SVD decomposes $A$ into the product of three matrices:

$$
A = U \Sigma V^T
$$

where:
- $U$ is an $m \times m$ orthogonal matrix (its columns are called left singular vectors),
- $\Sigma$ is an $m \times n$ diagonal matrix (its diagonal entries are the singular values of $A$),
- $V^T$ (the transpose of $V$) is an $n \times n$ orthogonal matrix (its rows are called right singular vectors).

### Properties

1. **Orthogonality**: The columns of $U$ and $V$ are orthonormal vectors. This means $U^T U = I$ and $V^T V = I$.
2. **Singular Values**: The entries of $\Sigma$ are non-negative and are arranged in descending order. These singular values represent the "size" or "strength" of the matrix's effect along the principal directions.

## Example

Consider the matrix:

$$
A = \begin{pmatrix}
1 & 2 \\
3 & 4
\end{pmatrix}
$$

**Step 1: Compute the Singular Values**

1. Compute $A^T A$ and $A A^T$:
   $$
   A^T A = \begin{pmatrix}
   1 & 3 \\
   2 & 4
   \end{pmatrix}
   \begin{pmatrix}
   1 & 2 \\
   3 & 4
   \end{pmatrix} = \begin{pmatrix}
   10 & 14 \\
   14 & 20
   \end{pmatrix}
   $$

   $$
   A A^T = \begin{pmatrix}
   1 & 2 \\
   3 & 4
   \end{pmatrix}
   \begin{pmatrix}
   1 & 3 \\
   2 & 4
   \end{pmatrix} = \begin{pmatrix}
   5 & 11 \\
   11 & 25
   \end{pmatrix}
   $$

2. Find the eigenvalues of $A^T A$ and $A A^T$:
   For $A^T A$:
   $$
   \text{det}(A^T A - \lambda I) = \text{det} \begin{pmatrix}
   10 - \lambda & 14 \\
   14 & 20 - \lambda
   \end{pmatrix}
   $$
   Calculate the determinant:
   $$
   (10 - \lambda)(20 - \lambda) - 14^2 = \lambda^2 - 30\lambda + 16
   $$
   Solve the characteristic polynomial:
   $$
   \lambda^2 - 30\lambda + 16 = 0
   $$
   The eigenvalues are approximately:
   $$
   \lambda_1 \approx 29.77 \quad \text{and} \quad \lambda_2 \approx 0.23
   $$

   The singular values are the square roots of these eigenvalues:
   $$
   \sigma_1 = \sqrt{29.77} \approx 5.46
   $$
   $$
   \sigma_2 = \sqrt{0.23} \approx 0.48
   $$

**Step 2: Compute the Matrices $U$, $\Sigma$, and $V$**

1. Compute the matrix $U$ from the eigenvectors of $A A^T$:
   For $A A^T$:
   $$
   \text{det}(A A^T - \lambda I) = \text{det} \begin{pmatrix}
   5 - \lambda & 11 \\
   11 & 25 - \lambda
   \end{pmatrix}
   $$
   Solve the characteristic polynomial to find the eigenvectors:
   $$
   \text{Eigenvectors} \approx \begin{pmatrix}
   -0.40 & -0.82 \\
   -0.82 & 0.57
   \end{pmatrix}
   $$
   Normalize these eigenvectors to form $U$.

2. Matrix $\Sigma$:
   $$
   \Sigma = \begin{pmatrix}
   5.46 & 0 \\
   0 & 0.48
   \end{pmatrix}
   $$

3. Compute the matrix $V$ from the eigenvectors of $A^T A$:
   $$
   \text{Eigenvectors} \approx \begin{pmatrix}
   -0.40 & -0.82 \\
   -0.82 & 0.57
   \end{pmatrix}
   $$
   Normalize these eigenvectors to form $V$.

**Step 3: Verify the Decomposition**

Verify:
$$
A = U \Sigma V^T
$$
Calculate:
$$
U \Sigma V^T
$$

## Summary

Singular Value Decomposition (SVD) provides a powerful method for matrix factorization, revealing the intrinsic properties of matrices. The decomposition $A = U \Sigma V^T$ simplifies many matrix computations and is fundamental in applications such as data reduction, signal processing, and solving systems of linear equations.
