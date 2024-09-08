# Linear Independence in Linear Algebra

In linear algebra, a set of vectors is said to be **linearly independent** if no vector in the set can be written as a linear combination of the others. In other words, each vector in a linearly independent set adds a new dimension to the space spanned by the vectors, and none of the vectors can be expressed as a "mix" of the others.

## Definition of Linear Independence

Consider a set of vectors $\{\mathbf{v}_1, \mathbf{v}_2, \dots, \mathbf{v}_k\}$ in a vector space $V$. The set is **linearly independent** if the only solution to the equation

$$
c_1\mathbf{v}_1 + c_2\mathbf{v}_2 + \dots + c_k\mathbf{v}_k = \mathbf{0}
$$

is when all the scalars $c_1, c_2, \dots, c_k$ are zero:

$$
c_1 = c_2 = \dots = c_k = 0
$$

If there exists a non-trivial solution (i.e., at least one $c_i \neq 0$) to this equation, then the vectors are **linearly dependent**.

## Intuition Behind Linear Independence

- **Geometric Interpretation**: In $\mathbb{R}^2$, two vectors are linearly independent if they are not collinear; that is, they do not lie on the same line. In $\mathbb{R}^3$, three vectors are linearly independent if they do not all lie in the same plane.

- **Dimensionality**: The number of linearly independent vectors in a set corresponds to the dimension of the span of those vectors. For instance, two linearly independent vectors in $\mathbb{R}^3$ span a plane, while three linearly independent vectors span the entire space $\mathbb{R}^3$.

## Examples of Linear Independence

1. **Two Vectors in $\mathbb{R}^2$**: Consider the vectors $\mathbf{v}_1 = (1, 2)$ and $\mathbf{v}_2 = (3, 4)$ in $\mathbb{R}^2$. To check if they are linearly independent, we set up the equation:

   $$
   c_1(1, 2) + c_2(3, 4) = (0, 0)
   $$

   This gives us the system of equations:

   $$
   c_1 + 3c_2 = 0 \\
   2c_1 + 4c_2 = 0
   $$

   Solving this system, we find that the only solution is $c_1 = 0$ and $c_2 = 0$, so the vectors are linearly independent.

2. **Three Vectors in $\mathbb{R}^3$**: Consider the vectors $\mathbf{v}_1 = (1, 0, 0)$, $\mathbf{v}_2 = (0, 1, 0)$, and $\mathbf{v}_3 = (0, 0, 1)$ in $\mathbb{R}^3$. The equation

   $$
   c_1(1, 0, 0) + c_2(0, 1, 0) + c_3(0, 0, 1) = (0, 0, 0)
   $$

   leads to the system:

   $$
   c_1 = 0 \\
   c_2 = 0 \\
   c_3 = 0
   $$

   The only solution is $c_1 = c_2 = c_3 = 0$, so these vectors are linearly independent.

3. **Dependent Vectors**: Now, consider the vectors $\mathbf{v}_1 = (1, 2, 3)$, $\mathbf{v}_2 = (2, 4, 6)$, and $\mathbf{v}_3 = (3, 6, 9)$ in $\mathbb{R}^3$. Notice that $\mathbf{v}_2 = 2\mathbf{v}_1$ and $\mathbf{v}_3 = 3\mathbf{v}_1$. This means that $\mathbf{v}_2$ and $\mathbf{v}_3$ can be expressed as linear combinations of $\mathbf{v}_1$, so the vectors are linearly dependent.

## Conclusion

Linear independence is a fundamental concept in linear algebra, as it is crucial for understanding the structure of vector spaces, determining the basis of a space, and analyzing the solutions of linear systems. Linearly independent vectors form the building blocks of vector spaces, with each independent vector contributing uniquely to the span of the set.