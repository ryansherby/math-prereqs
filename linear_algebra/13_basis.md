# Basis in Linear Algebra

In linear algebra, a **basis** of a vector space is a set of vectors that are both linearly independent and span the entire space. The concept of a basis is fundamental because it provides a way to uniquely represent every vector in the space as a linear combination of the basis vectors.

## Definition of a Basis

A set of vectors $\{v_1, v_2, \ldots, v_n\}$ in a vector space $V$ is called a **basis** for $V$ if it satisfies the following two conditions:

1. **Linear Independence**: The vectors are linearly independent, meaning that no vector in the set can be expressed as a linear combination of the others. Mathematically, the set $\{v_1, v_2, \ldots, v_n\}$ is linearly independent if:
   $$
   c_1 v_1 + c_2 v_2 + \cdots + c_n v_n = 0
   $$
   implies that $c_1 = c_2 = \cdots = c_n = 0$, where $c_i$ are scalars.

2. **Spanning**: The vectors span the vector space $V$, meaning that any vector in $V$ can be written as a linear combination of the basis vectors. Formally, for any vector $v \in V$, there exist scalars $c_1, c_2, \ldots, c_n$ such that:
   $$
   v = c_1 v_1 + c_2 v_2 + \cdots + c_n v_n
   $$

## Properties of a Basis

1. **Uniqueness of Representation**: Each vector in the space has a unique representation as a linear combination of the basis vectors.

2. **Dimensionality**: The number of vectors in any basis for a vector space is equal to the dimension of that space. For example, $\mathbb{R}^n$ has a basis consisting of $n$ vectors.

3. **Coordinate Systems**: The coefficients in the linear combination of a vector with respect to a basis are called the coordinates of the vector in that basis.

## Examples of Bases

### Example 1: Basis for $\mathbb{R}^2$

Consider the vectors:
$$
v_1 = \begin{pmatrix} 1 \\ 0 \end{pmatrix}, \quad v_2 = \begin{pmatrix} 0 \\ 1 \end{pmatrix}
$$

1. **Linear Independence**:
   - To check linear independence, we solve:
     $$
     c_1 \begin{pmatrix} 1 \\ 0 \end{pmatrix} + c_2 \begin{pmatrix} 0 \\ 1 \end{pmatrix} = \begin{pmatrix} 0 \\ 0 \end{pmatrix}
     $$
     This gives:
     $$
     \begin{pmatrix} c_1 \\ c_2 \end{pmatrix} = \begin{pmatrix} 0 \\ 0 \end{pmatrix}
     $$
     Hence, $c_1 = 0$ and $c_2 = 0$, showing the vectors are linearly independent.

2. **Spanning**:
   - Any vector $v = \begin{pmatrix} x \\ y \end{pmatrix}$ in $\mathbb{R}^2$ can be written as:
     $$
     v = x \begin{pmatrix} 1 \\ 0 \end{pmatrix} + y \begin{pmatrix} 0 \\ 1 \end{pmatrix}
     $$
   - Thus, $\{v_1, v_2\}$ spans $\mathbb{R}^2$.

   Hence, $\{v_1, v_2\}$ forms a basis for $\mathbb{R}^2$.

### Example 2: Basis for $\mathbb{R}^3$

Consider the vectors:
$$
v_1 = \begin{pmatrix} 1 \\ 0 \\ 0 \end{pmatrix}, \quad v_2 = \begin{pmatrix} 0 \\ 1 \\ 0 \end{pmatrix}, \quad v_3 = \begin{pmatrix} 0 \\ 0 \\ 1 \end{pmatrix}
$$

1. **Linear Independence**:
   - To check linear independence, we solve:
     $$
     c_1 \begin{pmatrix} 1 \\ 0 \\ 0 \end{pmatrix} + c_2 \begin{pmatrix} 0 \\ 1 \\ 0 \end{pmatrix} + c_3 \begin{pmatrix} 0 \\ 0 \\ 1 \end{pmatrix} = \begin{pmatrix} 0 \\ 0 \\ 0 \end{pmatrix}
     $$
     This gives:
     $$
     \begin{pmatrix} c_1 \\ c_2 \\ c_3 \end{pmatrix} = \begin{pmatrix} 0 \\ 0 \\ 0 \end{pmatrix}
     $$
     Hence, $c_1 = 0$, $c_2 = 0$, and $c_3 = 0$, showing the vectors are linearly independent.

2. **Spanning**:
   - Any vector $v = \begin{pmatrix} x_1 \\ x_2 \\ x_3 \end{pmatrix}$ in $\mathbb{R}^3$ can be written as:
     $$
     v = x_1 \begin{pmatrix} 1 \\ 0 \\ 0 \end{pmatrix} + x_2 \begin{pmatrix} 0 \\ 1 \\ 0 \end{pmatrix} + x_3 \begin{pmatrix} 0 \\ 0 \\ 1 \end{pmatrix}
     $$
   - Thus, $\{v_1, v_2, v_3\}$ spans $\mathbb{R}^3$.

   Hence, $\{v_1, v_2, v_3\}$ forms a basis for $\mathbb{R}^3$.

### Example 3: Basis for a Subspace

Consider the subspace of $\mathbb{R}^3$ defined by the plane $x + y + z = 0$. A basis for this subspace can be:
$$
u = \begin{pmatrix} 1 \\ -1 \\ 0 \end{pmatrix}, \quad v = \begin{pmatrix} 1 \\ 0 \\ -1 \end{pmatrix}
$$

1. **Linear Independence**:
   - To check linear independence, solve:
     $$
     c_1 \begin{pmatrix} 1 \\ -1 \\ 0 \end{pmatrix} + c_2 \begin{pmatrix} 1 \\ 0 \\ -1 \end{pmatrix} = \begin{pmatrix} 0 \\ 0 \\ 0 \end{pmatrix}
     $$
     This gives:
     $$
     \begin{pmatrix} c_1 + c_2 \\ -c_1 \\ -c_2 \end{pmatrix} = \begin{pmatrix} 0 \\ 0 \\ 0 \end{pmatrix}
     $$
     Hence, $c_1 = 0$ and $c_2 = 0$, showing the vectors are linearly independent.

2. **Spanning**:
   - Any vector in the plane $x + y + z = 0$ can be expressed as a linear combination of $u$ and $v$.

   Hence, $\{u, v\}$ forms a basis for the subspace defined by $x + y + z = 0$ in $\mathbb{R}^3$.

## Conclusion

A basis is a fundamental concept in linear algebra, providing a way to uniquely represent all vectors in a vector space as linear combinations of a set of basis vectors. Understanding bases helps in analyzing vector spaces, solving linear systems, and performing various linear algebra operations.
