# Positive (Semi-) Definite Matrices in Linear Algebra

In linear algebra, the concepts of positive definite and positive semi-definite matrices are important for understanding various matrix properties and their applications, particularly in optimization, statistics, and quadratic forms.

## Positive Definite Matrix

A matrix $A$ is called **positive definite** if it is symmetric and for all non-zero vectors $x$, the following inequality holds:

$$
x^T A x > 0
$$

### Definition

A symmetric matrix $A$ is positive definite if:

1. **Symmetry**: $A = A^T$.
2. **Positive Definiteness**: For any non-zero vector $x$,
   $$
   x^T A x > 0
   $$

### Properties

1. **Eigenvalues**: All eigenvalues of a positive definite matrix are positive.
2. **Cholesky Decomposition**: A positive definite matrix can be decomposed into the product of a lower triangular matrix and its transpose, i.e., $A = LL^T$ where $L$ is a lower triangular matrix.

### Example

Consider the matrix:

$$
A = \begin{pmatrix}
2 & 1 \\
1 & 2
\end{pmatrix}
$$

**Step 1: Check Symmetry**

Compute the transpose $A^T$:

$$
A^T = \begin{pmatrix}
2 & 1 \\
1 & 2
\end{pmatrix}
$$

Since $A^T = A$, the matrix $A$ is symmetric.

**Step 2: Check Positive Definiteness**

For any non-zero vector $x = \begin{pmatrix} x_1 \\ x_2 \end{pmatrix}$, compute $x^T A x$:

$$
x^T A x = \begin{pmatrix}
x_1 & x_2
\end{pmatrix}
\begin{pmatrix}
2 & 1 \\
1 & 2
\end{pmatrix}
\begin{pmatrix}
x_1 \\
x_2
\end{pmatrix}
$$

Expanding this:

$$
x^T A x = 2x_1^2 + 2x_1x_2 + 2x_2^2
$$

Since $2x_1^2 + 2x_1x_2 + 2x_2^2 > 0$ for any non-zero vector $x$, matrix $A$ is positive definite.

## Positive Semi-Definite Matrix

A matrix $A$ is called **positive semi-definite** if it is symmetric and for all vectors $x$, the following inequality holds:

$$
x^T A x \geq 0
$$

### Definition

A symmetric matrix $A$ is positive semi-definite if:

1. **Symmetry**: $A = A^T$.
2. **Positive Semi-Definiteness**: For any vector $x$,
   $$
   x^T A x \geq 0
   $$

### Properties

1. **Eigenvalues**: All eigenvalues of a positive semi-definite matrix are non-negative.
2. **Cholesky Decomposition**: A positive semi-definite matrix can be decomposed as $A = B B^T$ where $B$ is not necessarily invertible.

### Example

Consider the matrix:

$$
B = \begin{pmatrix}
1 & 0 \\
0 & 0
\end{pmatrix}
$$

**Step 1: Check Symmetry**

Compute the transpose $B^T$:

$$
B^T = \begin{pmatrix}
1 & 0 \\
0 & 0
\end{pmatrix}
$$

Since $B^T = B$, the matrix $B$ is symmetric.

**Step 2: Check Positive Semi-Definiteness**

For any vector $x = \begin{pmatrix} x_1 \\ x_2 \end{pmatrix}$, compute $x^T B x$:

$$
x^T B x = \begin{pmatrix}
x_1 & x_2
\end{pmatrix}
\begin{pmatrix}
1 & 0 \\
0 & 0
\end{pmatrix}
\begin{pmatrix}
x_1 \\
x_2
\end{pmatrix}
$$

Expanding this:

$$
x^T B x = x_1^2
$$

Since $x_1^2 \geq 0$ for any vector $x$, matrix $B$ is positive semi-definite.

## Summary

Positive definite and positive semi-definite matrices are central concepts in linear algebra. Positive definite matrices have all positive eigenvalues and are used in optimization problems where strict positivity is required. Positive semi-definite matrices have non-negative eigenvalues and are used in contexts where non-negativity is sufficient. Both types of matrices are symmetric, which is a key property for their analysis and decomposition.
