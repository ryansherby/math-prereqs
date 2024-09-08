# Subspaces in Linear Algebra

A **subspace** in linear algebra is a subset of a vector space that is itself a vector space under the operations of vector addition and scalar multiplication defined on the larger vector space. In simpler terms, if you have a vector space $V$, a subspace $W$ is a smaller collection of vectors from $V$ that satisfies the same rules and properties as $V$ does.

## Definition of a Subspace

A subset $W$ of a vector space $V$ over a field $F$ is called a **subspace** if $W$ satisfies the following three conditions:

1. **The Zero Vector Condition**: The zero vector of $V$ is in $W$.
   
   $$
   \mathbf{0} \in W
   $$

2. **Closed Under Vector Addition**: For any two vectors $\mathbf{u}, \mathbf{v} \in W$, their sum is also in $W$.
   
   $$
   \mathbf{u} + \mathbf{v} \in W
   $$

3. **Closed Under Scalar Multiplication**: For any vector $\mathbf{v} \in W$ and any scalar $c \in F$, the product $c\mathbf{v}$ is also in $W$.
   
   $$
   c\mathbf{v} \in W
   $$

## Implications of the Definition

These conditions ensure that any subspace $W$ is a vector space in its own right, following the same rules as the parent space $V$. Because a subspace must contain the zero vector, it cannot be empty. Additionally, closure under addition and scalar multiplication means that combining elements of a subspace through these operations will never take you outside the subspace.

## Examples of Subspaces

1. **The Zero Subspace**: The simplest example of a subspace is the set containing only the zero vector, denoted by $\{\mathbf{0}\}$. This is called the **trivial subspace**.

   - **Example**: In the vector space $\mathbb{R}^3$, the set $\{(0, 0, 0)\}$ is a subspace.

2. **The Entire Space**: The vector space itself is always a subspace. In this case, the subspace is not smaller than the original space.

   - **Example**: The entire space $\mathbb{R}^2$ is a subspace of itself.

3. **Line Through the Origin**: Any line that passes through the origin in a vector space is a subspace. This line must include the zero vector and be closed under vector addition and scalar multiplication.

   - **Example**: In $\mathbb{R}^2$, the set of all vectors of the form $(t, 2t)$ where $t \in \mathbb{R}$ is a subspace. This set represents a line through the origin with a slope of 2.

   - **Verification**:
     - The zero vector $(0, 0)$ is in the set since $t = 0$ gives $(0, 0)$.
     - If $\mathbf{u} = (t_1, 2t_1)$ and $\mathbf{v} = (t_2, 2t_2)$, then $\mathbf{u} + \mathbf{v} = (t_1 + t_2, 2(t_1 + t_2))$, which is also of the form $(t, 2t)$.
     - For any scalar $c$ and vector $\mathbf{u} = (t, 2t)$, $c\mathbf{u} = (ct, 2ct)$, which is also in the set.

4. **Plane Through the Origin**: Any plane that passes through the origin in $\mathbb{R}^3$ is a subspace. Like the line, it must contain the zero vector and be closed under addition and scalar multiplication.

   - **Example**: The set of vectors $(x, y, 0)$ in $\mathbb{R}^3$ where $x, y \in \mathbb{R}$ forms a subspace. This is the $xy$-plane in $\mathbb{R}^3$.

   - **Verification**:
     - The zero vector $(0, 0, 0)$ is in the set.
     - If $\mathbf{u} = (x_1, y_1, 0)$ and $\mathbf{v} = (x_2, y_2, 0)$, then $\mathbf{u} + \mathbf{v} = (x_1 + x_2, y_1 + y_2, 0)$, which lies in the $xy$-plane.
     - For any scalar $c$ and vector $\mathbf{u} = (x, y, 0)$, $c\mathbf{u} = (cx, cy, 0)$, which is also in the $xy$-plane.

5. **Column Space of a Matrix**: The set of all possible linear combinations of the columns of a matrix forms a subspace called the **column space**.

   - **Example**: Consider the matrix
     $$
     A = \begin{pmatrix} 1 & 2 \\ 3 & 4 \\ 5 & 6 \end{pmatrix}.
     $$
     The column space of $A$ is the span of its columns:
     $$
     \text{Col}(A) = \text{Span}\left\{ \begin{pmatrix} 1 \\ 3 \\ 5 \end{pmatrix}, \begin{pmatrix} 2 \\ 4 \\ 6 \end{pmatrix} \right\}.
     $$

## Conclusion

Subspaces are important structures in linear algebra because they allow us to study smaller, more manageable parts of vector spaces while preserving the essential properties of the entire space. Understanding subspaces is crucial for topics such as solving linear systems, understanding matrix transformations, and more.