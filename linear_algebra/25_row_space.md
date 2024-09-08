# Row Space in Linear Algebra

In linear algebra, the **row space** of a matrix is a fundamental concept that represents the set of all possible linear combinations of the rows of the matrix. It provides insights into the span of the matrix rows and is related to the column space through the rank of the matrix.

## Definition

The **row space** of a matrix $A$ is the set of all possible vectors that can be expressed as a linear combination of the rows of $A$. Formally, if $A$ is an $m \times n$ matrix, the row space of $A$, denoted as $\text{Row}(A)$, is defined as:

$$
\text{Row}(A) = \{ \mathbf{y} \mid \mathbf{y} = A^T \mathbf{x}, \, \mathbf{x} \in \mathbb{R}^m \}
$$

where $\mathbf{x}$ is a vector in $\mathbb{R}^m$ and $A^T$ is the transpose of $A$.

### Properties

1. **Span**: The row space of $A$ is the span of its row vectors.
2. **Dimension**: The dimension of the row space is called the **rank** of the matrix $A$.
3. **Consistency**: The row space and column space of a matrix have the same dimension, which is the rank of the matrix.

## Examples

### Example 1: Row Space of a 2x3 Matrix

Consider the matrix:

$$
A = \begin{pmatrix}
1 & 2 & 3 \\
4 & 5 & 6
\end{pmatrix}
$$

**Step 1: Identify the Rows**

The rows of $A$ are:

$$
\mathbf{r}_1 = \begin{pmatrix}
1 & 2 & 3
\end{pmatrix},
\mathbf{r}_2 = \begin{pmatrix}
4 & 5 & 6
\end{pmatrix}
$$

**Step 2: Form a Linear Combination**

Any vector in the row space can be expressed as:

$$
\mathbf{b} = a \mathbf{r}_1 + b \mathbf{r}_2
$$

where $a$ and $b$ are scalars.

**Step 3: Determine the Span**

To find the span, perform Gaussian elimination on $A$:

$$
\text{Row reduction:} \quad \begin{pmatrix}
1 & 2 & 3 \\
4 & 5 & 6
\end{pmatrix}
\sim \begin{pmatrix}
1 & 2 & 3 \\
0 & -3 & -6
\end{pmatrix}
\sim \begin{pmatrix}
1 & 2 & 3 \\
0 & 1 & 2
\end{pmatrix}
$$

The resulting matrix shows that $\mathbf{r}_1$ and $\mathbf{r}_2$ are linearly dependent. The row space is spanned by the first row vector, $\mathbf{r}_1$.

### Example 2: Row Space of a 3x3 Matrix

Consider the matrix:

$$
B = \begin{pmatrix}
1 & 0 & 2 \\
0 & 1 & 3 \\
0 & 0 & 1
\end{pmatrix}
$$

**Step 1: Identify the Rows**

The rows of $B$ are:

$$
\mathbf{d}_1 = \begin{pmatrix}
1 & 0 & 2
\end{pmatrix},
\mathbf{d}_2 = \begin{pmatrix}
0 & 1 & 3
\end{pmatrix},
\mathbf{d}_3 = \begin{pmatrix}
0 & 0 & 1
\end{pmatrix}
$$

**Step 2: Form a Linear Combination**

Any vector in the row space can be expressed as:

$$
\mathbf{b} = a \mathbf{d}_1 + b \mathbf{d}_2 + c \mathbf{d}_3
$$

**Step 3: Determine the Span**

The rows of $B$ are linearly independent, so the row space of $B$ is $\mathbb{R}^3$.

### Example 3: Row Space of a 2x2 Matrix

Consider the matrix:

$$
C = \begin{pmatrix}
1 & 2 \\
3 & 6
\end{pmatrix}
$$

**Step 1: Identify the Rows**

The rows of $C$ are:

$$
\mathbf{e}_1 = \begin{pmatrix}
1 & 2
\end{pmatrix},
\mathbf{e}_2 = \begin{pmatrix}
3 & 6
\end{pmatrix}
$$

**Step 2: Form a Linear Combination**

Any vector in the row space can be expressed as:

$$
\mathbf{b} = a \mathbf{e}_1 + b \mathbf{e}_2
$$

**Step 3: Determine the Span**

Notice that $\mathbf{e}_2$ is a scalar multiple of $\mathbf{e}_1$:

$$
\mathbf{e}_2 = 3 \mathbf{e}_1
$$

Thus, the row space of $C$ is spanned by $\mathbf{e}_1$ and is a line through the origin in $\mathbb{R}^2$.

## Summary

The row space of a matrix is the set of all possible linear combinations of its row vectors. It provides insights into the span of the matrix rows and is closely related to the column space. The dimension of the row space, known as the rank of the matrix, is a key concept in understanding the matrix's properties and transformations.
