# Symmetric Matrices in Linear Algebra

A **symmetric matrix** is a square matrix that is equal to its transpose. Symmetric matrices have several important properties and applications in linear algebra, particularly in optimization problems and quadratic forms.

## Definition

A matrix $A$ is said to be symmetric if it is equal to its transpose:

$$
A = A^T
$$

where $A^T$ denotes the transpose of matrix $A$. This means that for every element $a_{ij}$ in the matrix, it satisfies:

$$
a_{ij} = a_{ji}
$$

In other words, the element at row $i$ and column $j$ is equal to the element at row $j$ and column $i$.

## Properties

1. **Diagonal Elements**: All diagonal elements of a symmetric matrix can be any real numbers, but the off-diagonal elements are symmetric with respect to the diagonal.
2. **Eigenvalues**: All eigenvalues of a symmetric matrix are real numbers.
3. **Orthogonality**: The eigenvectors corresponding to distinct eigenvalues of a symmetric matrix are orthogonal.

## Examples

### Example 1

Consider the matrix:

$$
A = \begin{pmatrix}
1 & 2 & 3 \\
2 & 4 & 5 \\
3 & 5 & 6
\end{pmatrix}
$$

**Step 1: Check Symmetry**

Compute the transpose $A^T$:

$$
A^T = \begin{pmatrix}
1 & 2 & 3 \\
2 & 4 & 5 \\
3 & 5 & 6
\end{pmatrix}
$$

Since $A^T = A$, the matrix $A$ is symmetric.

### Example 2

Consider the matrix:

$$
B = \begin{pmatrix}
7 & -1 & 2 \\
-1 & 5 & 0 \\
2 & 0 & 3
\end{pmatrix}
$$

**Step 1: Check Symmetry**

Compute the transpose $B^T$:

$$
B^T = \begin{pmatrix}
7 & -1 & 2 \\
-1 & 5 & 0 \\
2 & 0 & 3
\end{pmatrix}
$$

Since $B^T = B$, the matrix $B$ is symmetric.

### Example 3

Consider the matrix:

$$
C = \begin{pmatrix}
2 & 1 \\
3 & 4
\end{pmatrix}
$$

**Step 1: Check Symmetry**

Compute the transpose $C^T$:

$$
C^T = \begin{pmatrix}
2 & 3 \\
1 & 4
\end{pmatrix}
$$

Since $C^T \neq C$, the matrix $C$ is not symmetric.

## Summary

Symmetric matrices are a special class of square matrices that are equal to their transposes. They possess properties such as having real eigenvalues and orthogonal eigenvectors. Symmetric matrices are commonly used in various applications, including optimization problems, physics, and engineering.
