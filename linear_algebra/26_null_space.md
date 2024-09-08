# Null Space in Linear Algebra

In linear algebra, the **null space** (or **kernel**) of a matrix is a crucial concept that represents the set of all vectors that are mapped to the zero vector when the matrix is applied. It provides insights into the solutions of homogeneous systems of linear equations.

## Definition

The **null space** of a matrix $A$ is the set of all vectors $\mathbf{x}$ that satisfy the equation:

$$
A \mathbf{x} = \mathbf{0}
$$

where $A$ is an $m \times n$ matrix and $\mathbf{0}$ is the zero vector in $\mathbb{R}^m$. The null space of $A$, denoted as $\text{Null}(A)$, is formally defined as:

$$
\text{Null}(A) = \{ \mathbf{x} \in \mathbb{R}^n \mid A \mathbf{x} = \mathbf{0} \}
$$

### Properties

1. **Dimension**: The dimension of the null space is called the **nullity** of the matrix $A$. It represents the number of free variables in the solution to the homogeneous system.
2. **Relationship to Rank**: The rank-nullity theorem states that for an $m \times n$ matrix $A$:

$$
\text{rank}(A) + \text{nullity}(A) = n
$$

where $\text{rank}(A)$ is the dimension of the column space of $A$.

3. **Consistency**: If the null space contains only the zero vector, the matrix is said to be of full column rank and its columns are linearly independent.

## Examples

### Example 1: Null Space of a 2x3 Matrix

Consider the matrix:

$$
A = \begin{pmatrix}
1 & 2 & 3 \\
4 & 5 & 6
\end{pmatrix}
$$

**Step 1: Set Up the System**

To find the null space, solve the equation:

$$
A \mathbf{x} = \mathbf{0}
$$

where $\mathbf{x} = \begin{pmatrix}
x_1 \\
x_2 \\
x_3
\end{pmatrix}$.

**Step 2: Form the Augmented Matrix and Row Reduce**

Construct the augmented matrix:

$$
\begin{pmatrix}
1 & 2 & 3 & | & 0 \\
4 & 5 & 6 & | & 0
\end{pmatrix}
$$

Perform Gaussian elimination:

$$
\begin{pmatrix}
1 & 2 & 3 & | & 0 \\
0 & -3 & -6 & | & 0
\end{pmatrix}
\sim \begin{pmatrix}
1 & 2 & 3 & | & 0 \\
0 & 1 & 2 & | & 0
\end{pmatrix}
$$

**Step 3: Solve for the Null Space**

The resulting system is:

$$
\begin{aligned}
x_1 + 2x_2 + 3x_3 &= 0 \\
x_2 + 2x_3 &= 0
\end{aligned}
$$

Solve for $x_2$ and $x_1$ in terms of $x_3$:

$$
x_2 = -2x_3 \\
x_1 = 7x_3
$$

Thus, the null space is:

$$
\text{Null}(A) = \left\{ \begin{pmatrix}
7x_3 \\
-2x_3 \\
x_3
\end{pmatrix} \mid x_3 \in \mathbb{R} \right\}
$$

### Example 2: Null Space of a 3x3 Matrix

Consider the matrix:

$$
B = \begin{pmatrix}
1 & 2 & 1 \\
2 & 4 & 2 \\
3 & 6 & 3
\end{pmatrix}
$$

**Step 1: Set Up the System**

To find the null space, solve:

$$
B \mathbf{x} = \mathbf{0}
$$

where $\mathbf{x} = \begin{pmatrix}
x_1 \\
x_2 \\
x_3
\end{pmatrix}$.

**Step 2: Form the Augmented Matrix and Row Reduce**

Construct the augmented matrix:

$$
\begin{pmatrix}
1 & 2 & 1 & | & 0 \\
2 & 4 & 2 & | & 0 \\
3 & 6 & 3 & | & 0
\end{pmatrix}
$$

Perform Gaussian elimination:

$$
\begin{pmatrix}
1 & 2 & 1 & | & 0 \\
0 & 0 & 0 & | & 0 \\
0 & 0 & 0 & | & 0
\end{pmatrix}
$$

**Step 3: Solve for the Null Space**

The resulting system is:

$$
x_1 + 2x_2 + x_3 = 0
$$

Solve for $x_1$ in terms of $x_2$ and $x_3$:

$$
x_1 = -2x_2 - x_3
$$

Thus, the null space is:

$$
\text{Null}(B) = \left\{ \begin{pmatrix}
-2x_2 - x_3 \\
x_2 \\
x_3
\end{pmatrix} \mid x_2, x_3 \in \mathbb{R} \right\}
$$

### Example 3: Null Space of a 2x2 Matrix

Consider the matrix:

$$
C = \begin{pmatrix}
1 & 2 \\
3 & 6
\end{pmatrix}
$$

**Step 1: Set Up the System**

To find the null space, solve:

$$
C \mathbf{x} = \mathbf{0}
$$

where $\mathbf{x} = \begin{pmatrix}
x_1 \\
x_2
\end{pmatrix}$.

**Step 2: Form the Augmented Matrix and Row Reduce**

Construct the augmented matrix:

$$
\begin{pmatrix}
1 & 2 & | & 0 \\
3 & 6 & | & 0
\end{pmatrix}
$$

Perform Gaussian elimination:

$$
\begin{pmatrix}
1 & 2 & | & 0 \\
0 & 0 & | & 0
\end{pmatrix}
$$

**Step 3: Solve for the Null Space**

The resulting system is:

$$
x_1 + 2x_2 = 0
$$

Solve for $x_1$ in terms of $x_2$:

$$
x_1 = -2x_2
$$

Thus, the null space is:

$$
\text{Null}(C) = \left\{ \begin{pmatrix}
-2x_2 \\
x_2
\end{pmatrix} \mid x_2 \in \mathbb{R} \right\}
$$

## Summary

The null space of a matrix is the set of all vectors that are mapped to the zero vector by the matrix. It is crucial for understanding the solutions to homogeneous systems of linear equations. The dimension of the null space, known as the nullity of the matrix, provides important insights into the matrix's structure and its transformations.
