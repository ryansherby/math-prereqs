# Column Space in Linear Algebra

In linear algebra, the **column space** (or **range**) of a matrix is a fundamental concept that represents the set of all possible linear combinations of the columns of the matrix. It provides important insights into the span of the matrix and its transformations.

## Definition

The **column space** of a matrix $A$ is the set of all possible vectors that can be expressed as a linear combination of the columns of $A$. Formally, if $A$ is an $m \times n$ matrix, the column space of $A$, denoted as $\text{Col}(A)$, is defined as:

$$
\text{Col}(A) = \{ A \mathbf{x} \mid \mathbf{x} \in \mathbb{R}^n \}
$$

where $\mathbf{x}$ is a vector in $\mathbb{R}^n$.

### Properties

1. **Span**: The column space of $A$ is the span of its column vectors.
2. **Dimension**: The dimension of the column space is called the **rank** of the matrix $A$.
3. **Consistency**: A system of linear equations $A \mathbf{x} = \mathbf{b}$ has a solution if and only if $\mathbf{b}$ is in the column space of $A$.

## Examples

### Example 1: Column Space of a 2x3 Matrix

Consider the matrix:

$$
A = \begin{pmatrix}
1 & 2 & 3 \\
4 & 5 & 6
\end{pmatrix}
$$

**Step 1: Identify the Columns**

The columns of $A$ are:

$$
\mathbf{c}_1 = \begin{pmatrix}
1 \\
4
\end{pmatrix},
\mathbf{c}_2 = \begin{pmatrix}
2 \\
5
\end{pmatrix},
\mathbf{c}_3 = \begin{pmatrix}
3 \\
6
\end{pmatrix}
$$

**Step 2: Form a Linear Combination**

Any vector in the column space can be expressed as:

$$
\mathbf{b} = a \mathbf{c}_1 + b \mathbf{c}_2 + c \mathbf{c}_3
$$

where $a$, $b$, and $c$ are scalars.

**Step 3: Determine the Span**

To find the span, consider the linear independence of the columns. Perform Gaussian elimination on $A$:

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

The resulting matrix shows that the column vectors $\mathbf{c}_1$ and $\mathbf{c}_2$ are linearly independent, so the column space of $A$ is spanned by these two vectors.

### Example 2: Column Space of a 3x3 Matrix

Consider the matrix:

$$
B = \begin{pmatrix}
1 & 0 & 2 \\
0 & 1 & 3 \\
0 & 0 & 1
\end{pmatrix}
$$

**Step 1: Identify the Columns**

The columns of $B$ are:

$$
\mathbf{d}_1 = \begin{pmatrix}
1 \\
0 \\
0
\end{pmatrix},
\mathbf{d}_2 = \begin{pmatrix}
0 \\
1 \\
0
\end{pmatrix},
\mathbf{d}_3 = \begin{pmatrix}
2 \\
3 \\
1
\end{pmatrix}
$$

**Step 2: Form a Linear Combination**

Any vector in the column space can be expressed as:

$$
\mathbf{b} = a \mathbf{d}_1 + b \mathbf{d}_2 + c \mathbf{d}_3
$$

**Step 3: Determine the Span**

The columns of $B$ are linearly independent, so the column space of $B$ is the entire $\mathbb{R}^3$, and it spans all possible vectors in $\mathbb{R}^3$.

### Example 3: Column Space of a 2x2 Matrix

Consider the matrix:

$$
C = \begin{pmatrix}
1 & 2 \\
3 & 6
\end{pmatrix}
$$

**Step 1: Identify the Columns**

The columns of $C$ are:

$$
\mathbf{e}_1 = \begin{pmatrix}
1 \\
3
\end{pmatrix},
\mathbf{e}_2 = \begin{pmatrix}
2 \\
6
\end{pmatrix}
$$

**Step 2: Form a Linear Combination**

Any vector in the column space can be expressed as:

$$
\mathbf{b} = a \mathbf{e}_1 + b \mathbf{e}_2
$$

**Step 3: Determine the Span**

Notice that $\mathbf{e}_2$ is a scalar multiple of $\mathbf{e}_1$:

$$
\mathbf{e}_2 = 2 \mathbf{e}_1
$$

Thus, the column space of $C$ is spanned by $\mathbf{e}_1$ and is a line through the origin in $\mathbb{R}^2$.

## Summary

The column space of a matrix is the set of all possible linear combinations of its column vectors. It provides insights into the span of the matrix and the solutions to systems of linear equations. The dimension of the column space, known as the rank of the matrix, is a key concept in understanding the matrix's properties and its transformations.
