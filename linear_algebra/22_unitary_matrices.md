# Unitary Matrices in Linear Algebra

In linear algebra, a **unitary matrix** is a complex square matrix whose conjugate transpose is also its inverse. Unitary matrices play a crucial role in quantum mechanics and signal processing due to their properties related to preserving vector norms and angles.

## Definition

A matrix $U$ is called **unitary** if it satisfies:

$$
U U^* = U^* U = I
$$

where $U^*$ denotes the conjugate transpose (or Hermitian transpose) of $U$, and $I$ is the identity matrix.

### Conjugate Transpose

The conjugate transpose of a matrix $U$, denoted by $U^*$, is obtained by taking the transpose of $U$ and then taking the complex conjugate of each entry. For a matrix $U = \begin{pmatrix} u_{ij} \end{pmatrix}$, its conjugate transpose $U^*$ is:

$$
U^* = \begin{pmatrix}
\overline{u_{11}} & \overline{u_{21}} & \cdots & \overline{u_{m1}} \\
\overline{u_{12}} & \overline{u_{22}} & \cdots & \overline{u_{m2}} \\
\vdots & \vdots & \ddots & \vdots \\
\overline{u_{1n}} & \overline{u_{2n}} & \cdots & \overline{u_{mn}}
\end{pmatrix}
$$

### Properties

1. **Preservation of Norm**: For any vector $x$,
   $$
   \| U x \| = \| x \|
   $$
   where $\| \cdot \|$ denotes the Euclidean norm.

2. **Preservation of Inner Product**: For any vectors $x$ and $y$,
   $$
   \langle U x, U y \rangle = \langle x, y \rangle
   $$
   where $\langle \cdot, \cdot \rangle$ denotes the inner product.

3. **Eigenvalues**: The eigenvalues of a unitary matrix lie on the unit circle in the complex plane.

4. **Norm Preservation**: Unitary matrices preserve the length of vectors and angles between vectors.

## Examples

### Example 1

Consider the matrix:

$$
U = \frac{1}{\sqrt{2}} \begin{pmatrix}
1 & 1 \\
-1 & 1
\end{pmatrix}
$$

**Step 1: Compute the Conjugate Transpose**

Since the matrix has real entries, the conjugate transpose is the same as the transpose:

$$
U^* = \frac{1}{\sqrt{2}} \begin{pmatrix}
1 & -1 \\
1 & 1
\end{pmatrix}
$$

**Step 2: Verify Unitarity**

Compute $U U^*$:

$$
U U^* = \frac{1}{2} \begin{pmatrix}
1 & 1 \\
-1 & 1
\end{pmatrix}
\begin{pmatrix}
1 & -1 \\
1 & 1
\end{pmatrix}
= \frac{1}{2} \begin{pmatrix}
2 & 0 \\
0 & 2
\end{pmatrix}
= I
$$

Since $U U^* = I$, the matrix $U$ is unitary.

### Example 2

Consider the matrix:

$$
V = \frac{1}{\sqrt{2}} \begin{pmatrix}
1 & i \\
i & -1
\end{pmatrix}
$$

**Step 1: Compute the Conjugate Transpose**

Compute the conjugate transpose:

$$
V^* = \frac{1}{\sqrt{2}} \begin{pmatrix}
1 & -i \\
-i & -1
\end{pmatrix}
$$

**Step 2: Verify Unitarity**

Compute $V V^*$:

$$
V V^* = \frac{1}{2} \begin{pmatrix}
1 & i \\
i & -1
\end{pmatrix}
\begin{pmatrix}
1 & -i \\
-i & -1
\end{pmatrix}
= \frac{1}{2} \begin{pmatrix}
2 & 0 \\
0 & 2
\end{pmatrix}
= I
$$

Since $V V^* = I$, the matrix $V$ is unitary.

### Example 3

Consider the matrix:

$$
W = \begin{pmatrix}
\frac{1}{2} & \frac{1}{2} \\
\frac{1}{2} & -\frac{1}{2}
\end{pmatrix}
$$

**Step 1: Compute the Conjugate Transpose**

Since the matrix has real entries, the conjugate transpose is the same as the transpose:

$$
W^* = \begin{pmatrix}
\frac{1}{2} & \frac{1}{2} \\
\frac{1}{2} & -\frac{1}{2}
\end{pmatrix}
$$

**Step 2: Verify Unitarity**

Compute $W W^*$:

$$
W W^* = \begin{pmatrix}
\frac{1}{2} & \frac{1}{2} \\
\frac{1}{2} & -\frac{1}{2}
\end{pmatrix}
\begin{pmatrix}
\frac{1}{2} & \frac{1}{2} \\
\frac{1}{2} & -\frac{1}{2}
\end{pmatrix}
= \begin{pmatrix}
1 & 0 \\
0 & 1
\end{pmatrix}
= I
$$

Since $W W^* = I$, the matrix $W$ is unitary.

## Summary

Unitary matrices are complex square matrices with the property that their conjugate transpose is also their inverse. They preserve vector norms and inner products, which makes them important in various applications including quantum mechanics and signal processing. Unitary matrices have eigenvalues on the unit circle in the complex plane and their properties are essential in many mathematical and engineering contexts.
