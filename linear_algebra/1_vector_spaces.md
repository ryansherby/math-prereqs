# Vector Spaces

A **vector space** is a fundamental concept in linear algebra, consisting of a set of vectors that can be added together and multiplied by scalars, satisfying a specific set of axioms. These spaces are defined over a field, commonly the real numbers $\mathbb{R}$ or the complex numbers $\mathbb{C}$.

## Vector Space Definition

A vector space $V$ over a field $F$ (e.g., $\mathbb{R}$ or $\mathbb{C}$) is a set equipped with two operations:
1. **Vector Addition**: For any two vectors $\mathbf{u}, \mathbf{v} \in V$, their sum $\mathbf{u} + \mathbf{v} \in V$.
2. **Scalar Multiplication**: For any scalar $c \in F$ and any vector $\mathbf{v} \in V$, the product $c\mathbf{v} \in V$.

## Axioms of Vector Spaces

A set $V$ is a vector space if the following conditions are satisfied for all $\mathbf{u}, \mathbf{v}, \mathbf{w} \in V$ and $a, b \in F$:

1. **Associativity of Addition**:
   $$
   \mathbf{u} + (\mathbf{v} + \mathbf{w}) = (\mathbf{u} + \mathbf{v}) + \mathbf{w}
   $$

2. **Commutativity of Addition**:
   $$
   \mathbf{u} + \mathbf{v} = \mathbf{v} + \mathbf{u}
   $$

3. **Identity Element of Addition**: There exists an element $\mathbf{0} \in V$ such that:
   $$
   \mathbf{v} + \mathbf{0} = \mathbf{v}
   $$
   (Here, $\mathbf{0}$ is the zero vector.)

4. **Inverse Elements of Addition**: For each $\mathbf{v} \in V$, there exists a $\mathbf{-v} \in V$ such that:
   $$
   \mathbf{v} + \mathbf{-v} = \mathbf{0}
   $$

5. **Distributivity of Scalar Multiplication with Respect to Vector Addition**:
   $$
   a(\mathbf{u} + \mathbf{v}) = a\mathbf{u} + a\mathbf{v}
   $$

6. **Distributivity of Scalar Multiplication with Respect to Field Addition**:
   $$
   (a + b)\mathbf{v} = a\mathbf{v} + b\mathbf{v}
   $$

7. **Associativity of Scalar Multiplication**:
   $$
   a(b\mathbf{v}) = (ab)\mathbf{v}
   $$

8. **Identity Element of Scalar Multiplication**: There exists an element $1 \in F$ such that:
   $$
   1\mathbf{v} = \mathbf{v}
   $$

## Examples of Vector Spaces

1. **Euclidean Space** $\mathbb{R}^n$:
   The set of all $n$-tuples of real numbers $(x_1, x_2, \dots, x_n)$ forms a vector space under the standard operations of addition and scalar multiplication.

   **Example**: The set of all 2D vectors $\mathbb{R}^2$:
   $$
   \mathbb{R}^2 = \{(x, y) \mid x, y \in \mathbb{R}\}
   $$
   is a vector space where vector addition and scalar multiplication are defined as:
   $$
   (x_1, y_1) + (x_2, y_2) = (x_1 + x_2, y_1 + y_2)
   $$
   $$
   c(x, y) = (cx, cy)
   $$

2. **Polynomial Space** $P_n$:
   The set of all polynomials of degree less than or equal to $n$ forms a vector space. For example, the set of all polynomials of degree at most 2:
   $$
   P_2 = \{a_0 + a_1x + a_2x^2 \mid a_0, a_1, a_2 \in \mathbb{R}\}
   $$

3. **Matrix Space** $M_{m \times n}$:
   The set of all $m \times n$ matrices with entries from a field $F$ is a vector space. For example, the set of all $2 \times 2$ matrices:
   $$
   M_{2 \times 2} = \left\{ \begin{pmatrix} a & b \\ c & d \end{pmatrix} \mid a, b, c, d \in \mathbb{R} \right\}
   $$

## Subspaces

A **subspace** is a subset of a vector space that is itself a vector space under the same operations.

**Example**: The set of vectors of the form $(x, 0)$ in $\mathbb{R}^2$ is a subspace of $\mathbb{R}^2$.

## Conclusion

Vector spaces are foundational structures in linear algebra, providing a framework for analyzing vectors, matrices, functions, and more. They allow for the study of linear transformations, eigenvectors, and other key concepts.