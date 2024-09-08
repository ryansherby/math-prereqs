# Matrix Multiplication in Linear Algebra

Matrix multiplication is a fundamental operation in linear algebra that combines two matrices to produce a new matrix. This operation is crucial in various applications including solving systems of linear equations, transformations, and more.

## Definition of Matrix Multiplication

Matrix multiplication involves multiplying two matrices $A$ and $B$ to produce a matrix $C$. The product of two matrices is defined as follows:

1. **Matrix Dimensions**: For two matrices $A$ and $B$ to be multiplied, the number of columns in $A$ must be equal to the number of rows in $B$. If $A$ is an $m \times n$ matrix and $B$ is an $n \times p$ matrix, then their product $C = AB$ will be an $m \times p$ matrix.

2. **Element Calculation**: Each element $c_{ij}$ of the product matrix $C$ is computed by taking the dot product of the $i$-th row of matrix $A$ and the $j$-th column of matrix $B$.

Mathematically, the element $c_{ij}$ of matrix $C$ is given by:
$$
c_{ij} = \sum_{k=1}^{n} a_{ik} b_{kj}
$$
where $a_{ik}$ is the element in the $i$-th row and $k$-th column of $A$, and $b_{kj}$ is the element in the $k$-th row and $j$-th column of $B$.

## Properties of Matrix Multiplication

1. **Associativity**: Matrix multiplication is associative. For matrices $A$, $B$, and $C$, the following holds:
   $$
   (AB)C = A(BC)
   $$

2. **Distributivity**: Matrix multiplication distributes over matrix addition. For matrices $A$, $B$, and $C$:
   $$
   A(B + C) = AB + AC
   $$
   and
   $$
   (A + B)C = AC + BC
   $$

3. **Non-Commutativity**: Matrix multiplication is generally not commutative. That is, $AB \neq BA$ in general.

4. **Identity Matrix**: Multiplying a matrix by the identity matrix results in the original matrix. If $I$ is the identity matrix:
   $$
   AI = IA = A
   $$

5. **Transpose**: The transpose of the product of two matrices is the product of their transposes in reverse order:
   $$
   (AB)^T = B^T A^T
   $$

## Examples of Matrix Multiplication

### Example 1: $2 \times 2$ Matrices

Consider matrices:
$$
A = \begin{pmatrix} 1 & 2 \\ 3 & 4 \end{pmatrix}, \quad B = \begin{pmatrix} 5 & 6 \\ 7 & 8 \end{pmatrix}
$$

To find the product $C = AB$:

1. Compute element $c_{11}$:
   $$
   c_{11} = (1 \cdot 5) + (2 \cdot 7) = 5 + 14 = 19
   $$

2. Compute element $c_{12}$:
   $$
   c_{12} = (1 \cdot 6) + (2 \cdot 8) = 6 + 16 = 22
   $$

3. Compute element $c_{21}$:
   $$
   c_{21} = (3 \cdot 5) + (4 \cdot 7) = 15 + 28 = 43
   $$

4. Compute element $c_{22}$:
   $$
   c_{22} = (3 \cdot 6) + (4 \cdot 8) = 18 + 32 = 50
   $$

Thus, the product matrix $C$ is:
$$
C = \begin{pmatrix} 19 & 22 \\ 43 & 50 \end{pmatrix}
$$

### Example 2: $3 \times 2$ and $2 \times 3$ Matrices

Consider matrices:
$$
A = \begin{pmatrix} 1 & 2 \\ 3 & 4 \\ 5 & 6 \end{pmatrix}, \quad B = \begin{pmatrix} 7 & 8 & 9 \\ 10 & 11 & 12 \end{pmatrix}
$$

To find the product $C = AB$:

1. Compute element $c_{11}$:
   $$
   c_{11} = (1 \cdot 7) + (2 \cdot 10) = 7 + 20 = 27
   $$

2. Compute element $c_{12}$:
   $$
   c_{12} = (1 \cdot 8) + (2 \cdot 11) = 8 + 22 = 30
   $$

3. Compute element $c_{13}$:
   $$
   c_{13} = (1 \cdot 9) + (2 \cdot 12) = 9 + 24 = 33
   $$

4. Compute element $c_{21}$:
   $$
   c_{21} = (3 \cdot 7) + (4 \cdot 10) = 21 + 40 = 61
   $$

5. Compute element $c_{22}$:
   $$
   c_{22} = (3 \cdot 8) + (4 \cdot 11) = 24 + 44 = 68
   $$

6. Compute element $c_{23}$:
   $$
   c_{23} = (3 \cdot 9) + (4 \cdot 12) = 27 + 48 = 75
   $$

7. Compute element $c_{31}$:
   $$
   c_{31} = (5 \cdot 7) + (6 \cdot 10) = 35 + 60 = 95
   $$

8. Compute element $c_{32}$:
   $$
   c_{32} = (5 \cdot 8) + (6 \cdot 11) = 40 + 66 = 106
   $$

9. Compute element $c_{33}$:
   $$
   c_{33} = (5 \cdot 9) + (6 \cdot 12) = 45 + 72 = 117
   $$

Thus, the product matrix $C$ is:
$$
C = \begin{pmatrix} 27 & 30 & 33 \\ 61 & 68 & 75 \\ 95 & 106 & 117 \end{pmatrix}
$$

## Conclusion

Matrix multiplication is a vital operation in linear algebra, used in numerous applications ranging from solving linear systems to performing transformations. Understanding how to multiply matrices and the properties of matrix multiplication is essential for various mathematical and practical problems.