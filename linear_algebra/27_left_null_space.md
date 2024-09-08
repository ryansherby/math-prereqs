# Left Null Space in Linear Algebra

The **left null space** (or **cokernel**) of a matrix is a concept in linear algebra that extends the idea of the null space. It refers to the set of all vectors that, when multiplied by the matrix from the left, produce the zero vector. It provides insights into the orthogonal complement of the row space of the matrix.

## Definition

The **left null space** of a matrix $A$ is the set of all vectors $\mathbf{y}$ in $\mathbb{R}^m$ such that:

$$
\mathbf{y}^T A = \mathbf{0}
$$

where $A$ is an $m \times n$ matrix, and $\mathbf{0}$ is the zero vector in $\mathbb{R}^n$. Formally, the left null space of $A$, denoted as $\text{LeftNull}(A)$, is defined as:

$$
\text{LeftNull}(A) = \{ \mathbf{y} \in \mathbb{R}^m \mid \mathbf{y}^T A = \mathbf{0} \}
$$

### Properties

1. **Orthogonality**: The left null space is orthogonal to the row space of the matrix $A$.
2. **Dimension**: The dimension of the left null space is equal to the number of rows minus the rank of the matrix, i.e., $\text{dim}(\text{LeftNull}(A)) = m - \text{rank}(A)$.
3. **Relationship to Row Space**: The left null space can also be thought of as the null space of $A^T$.

## Examples

### Example 1: Left Null Space of a 3x2 Matrix

Consider the matrix:

$$
A = \begin{pmatrix}
1 & 2 \\
3 & 4 \\
5 & 6
\end{pmatrix}
$$

**Step 1: Form the Transpose and Solve**

First, find the left null space by solving:

$$
\mathbf{y}^T A = \mathbf{0}
$$

where $A^T$ is:

$$
A^T = \begin{pmatrix}
1 & 3 & 5 \\
2 & 4 & 6
\end{pmatrix}
$$

We need to solve:

$$
\begin{pmatrix}
y_1 & y_2 & y_3
\end{pmatrix}
\begin{pmatrix}
1 & 2 \\
3 & 4 \\
5 & 6
\end{pmatrix}
= \begin{pmatrix}
0 & 0
\end{pmatrix}
$$

**Step 2: Solve for $\mathbf{y}$**

Form the augmented matrix and perform Gaussian elimination:

$$
\begin{pmatrix}
1 & 3 & 5 & | & 0 \\
2 & 4 & 6 & | & 0
\end{pmatrix}
\sim \begin{pmatrix}
1 & 3 & 5 & | & 0 \\
0 & -2 & -4 & | & 0
\end{pmatrix}
\sim \begin{pmatrix}
1 & 3 & 5 & | & 0 \\
0 & 1 & 2 & | & 0
\end{pmatrix}
$$

The resulting system is:

$$
y_2 + 2y_3 = 0
$$

Solving this gives:

$$
y_2 = -2y_3
$$

Thus, the left null space is:

$$
\text{LeftNull}(A) = \left\{ \begin{pmatrix}
1 \\
-2 \\
1
\end{pmatrix} \mid \text{where } y_3 \text{ is free} \right\}
$$

### Example 2: Left Null Space of a 2x2 Matrix

Consider the matrix:

$$
B = \begin{pmatrix}
1 & 1 \\
2 & 2
\end{pmatrix}
$$

**Step 1: Form the Transpose and Solve**

Find the left null space by solving:

$$
\mathbf{y}^T B = \mathbf{0}
$$

where $B^T$ is:

$$
B^T = \begin{pmatrix}
1 & 2 \\
1 & 2
\end{pmatrix}
$$

We need to solve:

$$
\begin{pmatrix}
y_1 & y_2
\end{pmatrix}
\begin{pmatrix}
1 & 1 \\
2 & 2
\end{pmatrix}
= \begin{pmatrix}
0 & 0
\end{pmatrix}
$$

**Step 2: Solve for $\mathbf{y}$**

Form the augmented matrix and perform Gaussian elimination:

$$
\begin{pmatrix}
1 & 2 & | & 0 \\
1 & 2 & | & 0
\end{pmatrix}
\sim \begin{pmatrix}
1 & 2 & | & 0 \\
0 & 0 & | & 0
\end{pmatrix}
$$

The resulting system is:

$$
y_1 + 2y_2 = 0
$$

Solving this gives:

$$
y_1 = -2y_2
$$

Thus, the left null space is:

$$
\text{LeftNull}(B) = \left\{ \begin{pmatrix}
-2 \\
1
\end{pmatrix} \mid \text{where } y_2 \text{ is free} \right\}
$$

### Example 3: Left Null Space of a 4x3 Matrix

Consider the matrix:

$$
C = \begin{pmatrix}
1 & 0 & 0 \\
0 & 1 & 0 \\
0 & 0 & 1 \\
0 & 0 & 0
\end{pmatrix}
$$

**Step 1: Form the Transpose and Solve**

Find the left null space by solving:

$$
\mathbf{y}^T C = \mathbf{0}
$$

where $C^T$ is:

$$
C^T = \begin{pmatrix}
1 & 0 & 0 & 0 \\
0 & 1 & 0 & 0 \\
0 & 0 & 1 & 0
\end{pmatrix}
$$

We need to solve:

$$
\begin{pmatrix}
y_1 & y_2 & y_3
\end{pmatrix}
\begin{pmatrix}
1 & 0 & 0 \\
0 & 1 & 0 \\
0 & 0 & 1 \\
0 & 0 & 0
\end{pmatrix}
= \begin{pmatrix}
0 & 0 & 0
\end{pmatrix}
$$

**Step 2: Solve for $\mathbf{y}$**

Form the augmented matrix and perform Gaussian elimination:

$$
\begin{pmatrix}
1 & 0 & 0 & | & 0 \\
0 & 1 & 0 & | & 0 \\
0 & 0 & 1 & | & 0
\end{pmatrix}
$$

This system has no non-trivial solutions, as all rows are already in their reduced form.

Thus, the left null space is:

$$
\text{LeftNull}(C) = \left\{ \mathbf{0} \right\}
$$

## Summary

The left null space of a matrix is the set of all vectors that, when multiplied by the matrix from the left, yield the zero vector. It is orthogonal to the row space of the matrix and provides valuable insights into the matrix's structure. The dimension of the left null space is equal to the number of rows of the matrix minus the rank of the matrix.
