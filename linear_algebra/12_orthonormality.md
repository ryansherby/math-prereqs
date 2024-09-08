# Orthonormality in Linear Algebra

In linear algebra, orthonormality refers to a set of vectors that are both orthogonal (perpendicular) to each other and normalized (having unit length). This concept is crucial in various applications, including simplifying matrix computations, solving systems of equations, and analyzing vector spaces.

## Definition of Orthonormality

A set of vectors $\{v_1, v_2, \ldots, v_n\}$ in an inner product space is called **orthonormal** if:

1. **Orthogonality**: Each pair of distinct vectors is orthogonal. That is, the inner product (dot product) between any two distinct vectors is zero:
   $$
   \langle v_i, v_j \rangle = 0 \text{ for } i \neq j
   $$
   where $\langle \cdot, \cdot \rangle$ denotes the inner product.

2. **Normalization**: Each vector has unit length. That is, the inner product of each vector with itself is one:
   $$
   \langle v_i, v_i \rangle = 1
   $$

In the context of Euclidean space, the inner product is simply the dot product, and the condition for orthonormality translates to:
$$
v_i \cdot v_j = 0 \text{ for } i \neq j
$$
$$
\|v_i\| = 1
$$
where $\|v_i\|$ denotes the Euclidean norm (or length) of the vector $v_i$.

## Properties of Orthonormal Sets

1. **Orthogonal Projection**: Orthonormal vectors are useful in simplifying projections. If $\{v_1, v_2, \ldots, v_n\}$ is an orthonormal basis, then the projection of a vector $x$ onto this basis is straightforward to compute.

2. **Matrix Representation**: When the columns of a matrix are orthonormal vectors, the matrix is called an orthogonal matrix if it is square. An orthogonal matrix $Q$ satisfies:
   $$
   Q^T Q = Q Q^T = I
   $$
   where $Q^T$ denotes the transpose of $Q$, and $I$ is the identity matrix.

3. **Simplified Computations**: Orthonormal bases simplify various matrix operations, including finding matrix inverses and solving linear systems. For example, if $Q$ is an orthogonal matrix, its inverse is simply its transpose:
   $$
   Q^{-1} = Q^T
   $$

## Examples of Orthonormal Vectors

### Example 1: Orthonormal Vectors in $\mathbb{R}^2$

Consider the vectors:
$$
v_1 = \begin{pmatrix} 1 \\ 0 \end{pmatrix}, \quad v_2 = \begin{pmatrix} 0 \\ 1 \end{pmatrix}
$$

1. **Orthogonality**:
   $$
   v_1 \cdot v_2 = 1 \cdot 0 + 0 \cdot 1 = 0
   $$
   Since $v_1 \cdot v_2 = 0$, the vectors are orthogonal.

2. **Normalization**:
   $$
   \|v_1\| = \sqrt{1^2 + 0^2} = 1
   $$
   $$
   \|v_2\| = \sqrt{0^2 + 1^2} = 1
   $$

Since both vectors have unit length and are orthogonal, $\{v_1, v_2\}$ is an orthonormal set.

### Example 2: Orthonormal Vectors in $\mathbb{R}^3$

Consider the vectors:
$$
v_1 = \begin{pmatrix} 1 \\ 0 \\ 0 \end{pmatrix}, \quad v_2 = \begin{pmatrix} 0 \\ 1 \\ 0 \end{pmatrix}, \quad v_3 = \begin{pmatrix} 0 \\ 0 \\ 1 \end{pmatrix}
$$

1. **Orthogonality**:
   $$
   v_1 \cdot v_2 = 1 \cdot 0 + 0 \cdot 1 + 0 \cdot 0 = 0
   $$
   $$
   v_1 \cdot v_3 = 1 \cdot 0 + 0 \cdot 0 + 0 \cdot 1 = 0
   $$
   $$
   v_2 \cdot v_3 = 0 \cdot 0 + 1 \cdot 0 + 0 \cdot 1 = 0
   $$

2. **Normalization**:
   $$
   \|v_1\| = \sqrt{1^2 + 0^2 + 0^2} = 1
   $$
   $$
   \|v_2\| = \sqrt{0^2 + 1^2 + 0^2} = 1
   $$
   $$
   \|v_3\| = \sqrt{0^2 + 0^2 + 1^2} = 1
   $$

Since all vectors are orthogonal and have unit length, $\{v_1, v_2, v_3\}$ is an orthonormal set.

## Conclusion

Orthonormal sets of vectors are fundamental in linear algebra due to their useful properties, which simplify many computations and analyses. Understanding orthonormality is crucial for working with vector spaces, orthogonal matrices, and various linear algebra applications.