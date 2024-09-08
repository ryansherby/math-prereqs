# Linear Transformations in Linear Algebra

A **linear transformation** is a mapping between two vector spaces that preserves the operations of vector addition and scalar multiplication. Linear transformations are fundamental in understanding how vectors are manipulated and transformed in various applications.

## Definition of Linear Transformations

A linear transformation $T$ from a vector space $V$ to a vector space $W$ is a function:
$$
T: V \to W
$$
that satisfies the following properties for all vectors $u, v \in V$ and scalars $c$:

1. **Additivity**:
   $$
   T(u + v) = T(u) + T(v)
   $$

2. **Homogeneity**:
   $$
   T(cu) = cT(u)
   $$

In other words, a transformation $T$ is linear if it preserves vector addition and scalar multiplication.

## Matrix Representation of Linear Transformations

If $V$ and $W$ are finite-dimensional vector spaces, a linear transformation $T$ can be represented by a matrix $A$. If $x$ is a vector in $V$, then:
$$
T(x) = Ax
$$
where $A$ is the matrix representation of the transformation $T$ with respect to some basis.

### Example 1: Rotation in 2D

Consider a linear transformation $T$ that rotates vectors in $\mathbb{R}^2$ by an angle $\theta$. The matrix representation of this rotation transformation is:
$$
A = \begin{pmatrix}
\cos \theta & -\sin \theta \\
\sin \theta & \cos \theta
\end{pmatrix}
$$

For $\theta = 90^\circ$ (or $\pi/2$ radians), the matrix becomes:
$$
A = \begin{pmatrix}
0 & -1 \\
1 & 0
\end{pmatrix}
$$

If we apply this transformation to the vector $x = \begin{pmatrix}1 \\ 0\end{pmatrix}$:
$$
T\left(\begin{pmatrix}1 \\ 0\end{pmatrix}\right) = \begin{pmatrix}
0 & -1 \\
1 & 0
\end{pmatrix} \begin{pmatrix}1 \\ 0\end{pmatrix} = \begin{pmatrix}0 \\ 1\end{pmatrix}
$$

Thus, the vector $\begin{pmatrix}1 \\ 0\end{pmatrix}$ is rotated to $\begin{pmatrix}0 \\ 1\end{pmatrix}$.

### Example 2: Scaling in 3D

Consider a linear transformation $T$ that scales vectors in $\mathbb{R}^3$ by a factor of $k$. The matrix representation of this scaling transformation is:
$$
A = \begin{pmatrix}
k & 0 & 0 \\
0 & k & 0 \\
0 & 0 & k
\end{pmatrix}
$$

For $k = 2$, the matrix becomes:
$$
A = \begin{pmatrix}
2 & 0 & 0 \\
0 & 2 & 0 \\
0 & 0 & 2
\end{pmatrix}
$$

If we apply this transformation to the vector $x = \begin{pmatrix}1 \\ 2 \\ 3\end{pmatrix}$:
$$
T\left(\begin{pmatrix}1 \\ 2 \\ 3\end{pmatrix}\right) = \begin{pmatrix}
2 & 0 & 0 \\
0 & 2 & 0 \\
0 & 0 & 2
\end{pmatrix} \begin{pmatrix}1 \\ 2 \\ 3\end{pmatrix} = \begin{pmatrix}2 \\ 4 \\ 6\end{pmatrix}
$$

Thus, the vector $\begin{pmatrix}1 \\ 2 \\ 3\end{pmatrix}$ is scaled to $\begin{pmatrix}2 \\ 4 \\ 6\end{pmatrix}$.

### Example 3: Shear Transformation

Consider a linear transformation $T$ that shears vectors in $\mathbb{R}^2$ horizontally. The matrix representation of this shear transformation is:
$$
A = \begin{pmatrix}
1 & k \\
0 & 1
\end{pmatrix}
$$

For $k = 2$, the matrix becomes:
$$
A = \begin{pmatrix}
1 & 2 \\
0 & 1
\end{pmatrix}
$$

If we apply this transformation to the vector $x = \begin{pmatrix}1 \\ 1\end{pmatrix}$:
$$
T\left(\begin{pmatrix}1 \\ 1\end{pmatrix}\right) = \begin{pmatrix}
1 & 2 \\
0 & 1
\end{pmatrix} \begin{pmatrix}1 \\ 1\end{pmatrix} = \begin{pmatrix}3 \\ 1\end{pmatrix}
$$

Thus, the vector $\begin{pmatrix}1 \\ 1\end{pmatrix}$ is sheared to $\begin{pmatrix}3 \\ 1\end{pmatrix}$.

## Conclusion

Linear transformations provide a way to understand how vectors are mapped from one space to another while preserving the operations of addition and scalar multiplication. Matrix representations of linear transformations allow for practical computation and visualization of these mappings. Understanding these transformations is crucial in fields ranging from computer graphics to engineering and physics.
