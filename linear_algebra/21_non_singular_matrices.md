# Non-Singular Matrices in Linear Algebra

In linear algebra, a **non-singular matrix** is a matrix that is invertible, meaning it has an inverse. Non-singular matrices are crucial for solving systems of linear equations and various applications in numerical analysis.

## Definition

A matrix $A$ is called **non-singular** (or **invertible**) if there exists a matrix $A^{-1}$ such that:

$$
A A^{-1} = A^{-1} A = I
$$

where $I$ is the identity matrix of the same dimension as $A$.

### Properties

1. **Determinant**: A matrix is non-singular if and only if its determinant is non-zero. That is:
   $$
   \text{det}(A) \neq 0
   $$

2. **Row and Column Independence**: A matrix is non-singular if its rows and columns are linearly independent. This means there is no way to express one row (or column) as a linear combination of the others.

3. **Invertibility**: If $A$ is non-singular, its inverse $A^{-1}$ exists and is unique.

4. **Solution of Linear Systems**: For a system of linear equations $Ax = b$, if $A$ is non-singular, there is a unique solution given by:
   $$
   x = A^{-1} b
   $$

## Examples

### Example 1

Consider the matrix:

$$
A = \begin{pmatrix}
4 & 2 \\
3 & 1
\end{pmatrix}
$$

**Step 1: Compute the Determinant**

Calculate the determinant of $A$:

$$
\text{det}(A) = (4 \times 1) - (2 \times 3) = 4 - 6 = -2
$$

Since $\text{det}(A) \neq 0$, matrix $A$ is non-singular.

**Step 2: Compute the Inverse**

To find the inverse of $A$, use the formula for the inverse of a $2 \times 2$ matrix:

$$
A^{-1} = \frac{1}{\text{det}(A)} \begin{pmatrix}
d & -b \\
-c & a
\end{pmatrix}
$$

where $A = \begin{pmatrix} a & b \\ c & d \end{pmatrix}$. Applying this formula:

$$
A^{-1} = \frac{1}{-2} \begin{pmatrix}
1 & -2 \\
-3 & 4
\end{pmatrix} = \begin{pmatrix}
-0.5 & 1 \\
1.5 & -2
\end{pmatrix}
$$

### Example 2

Consider the matrix:

$$
B = \begin{pmatrix}
1 & 0 & 0 \\
0 & 2 & 0 \\
0 & 0 & 3
\end{pmatrix}
$$

**Step 1: Compute the Determinant**

Calculate the determinant of $B$:

$$
\text{det}(B) = 1 \times 2 \times 3 = 6
$$

Since $\text{det}(B) \neq 0$, matrix $B$ is non-singular.

**Step 2: Compute the Inverse**

Since $B$ is a diagonal matrix, its inverse can be computed by taking the reciprocal of each diagonal element:

$$
B^{-1} = \begin{pmatrix}
1 & 0 & 0 \\
0 & \frac{1}{2} & 0 \\
0 & 0 & \frac{1}{3}
\end{pmatrix}
$$

### Example 3

Consider the matrix:

$$
C = \begin{pmatrix}
1 & 2 \\
2 & 4
\end{pmatrix}
$$

**Step 1: Compute the Determinant**

Calculate the determinant of $C$:

$$
\text{det}(C) = (1 \times 4) - (2 \times 2) = 4 - 4 = 0
$$

Since $\text{det}(C) = 0$, matrix $C$ is singular and not non-singular.

## Summary

A non-singular matrix is an invertible matrix with a non-zero determinant. It is characterized by having linearly independent rows and columns, and its inverse exists and is unique. Non-singular matrices are essential in solving linear systems and various applications across mathematics and engineering.
