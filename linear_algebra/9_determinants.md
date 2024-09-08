# Determinants in Linear Algebra

The **determinant** is a scalar value that can be computed from a square matrix. It is a key concept in linear algebra with numerous applications, including solving linear systems, understanding matrix properties, and computing area/volume scaling factors.

## Definition of Determinant

For a square matrix $A$ of size $n \times n$, the determinant, denoted as $\det(A)$ or $|A|$, is a scalar value that encapsulates certain properties of the matrix. 

### Determinant of a $2 \times 2$ Matrix

For a $2 \times 2$ matrix:
$$
A = \begin{pmatrix} a & b \\ c & d \end{pmatrix}
$$

The determinant is calculated as:
$$
\det(A) = ad - bc
$$

### Determinant of a $3 \times 3$ Matrix

For a $3 \times 3$ matrix:
$$
A = \begin{pmatrix} a & b & c \\ d & e & f \\ g & h & i \end{pmatrix}
$$

The determinant is given by:
$$
\det(A) = a(ei - fh) - b(di - fg) + c(dh - eg)
$$

### Determinant of an $n \times n$ Matrix

For larger matrices, the determinant can be computed using methods such as expansion by minors or row reduction. The determinant involves summing over permutations of the matrix elements multiplied by their corresponding minors and signs.

#### Expansion by Minors

The determinant of an $n \times n$ matrix $A$ can be calculated using the formula:
$$
\det(A) = \sum_{j=1}^{n} (-1)^{i+j} a_{ij} \det(A_{ij})
$$
where $A_{ij}$ is the $(n-1) \times (n-1)$ submatrix obtained by deleting the $i$-th row and $j$-th column of $A$, and $(-1)^{i+j}$ is the sign factor.

## Properties of Determinants

1. **Invertibility**: A matrix $A$ is invertible if and only if $\det(A) \neq 0$. If $\det(A) = 0$, the matrix is singular and does not have an inverse.

2. **Multiplicative Property**: The determinant of the product of two matrices is the product of their determinants:
   $$
   \det(AB) = \det(A) \cdot \det(B)
   $$

3. **Transpose**: The determinant of the transpose of a matrix is equal to the determinant of the matrix:
   $$
   \det(A^T) = \det(A)
   $$

4. **Row Operations**: Determinant values change in specific ways under row operations:
   - **Row Swapping**: Swapping two rows multiplies the determinant by $-1$.
   - **Row Scaling**: Multiplying a row by a scalar $k$ multiplies the determinant by $k$.
   - **Row Addition**: Adding a multiple of one row to another row does not change the determinant.

5. **Matrix of Ones**: For an $n \times n$ matrix where all entries are 1, the determinant is zero for $n > 1$.

## Examples of Determinants

### Example 1: Determinant of a $2 \times 2$ Matrix

Consider the matrix:
$$
A = \begin{pmatrix} 3 & 4 \\ 2 & 5 \end{pmatrix}
$$

The determinant is:
$$
\det(A) = (3 \cdot 5) - (4 \cdot 2) = 15 - 8 = 7
$$

### Example 2: Determinant of a $3 \times 3$ Matrix

Consider the matrix:
$$
B = \begin{pmatrix} 1 & 2 & 3 \\ 4 & 5 & 6 \\ 7 & 8 & 9 \end{pmatrix}
$$

The determinant is:
$$
\det(B) = 1 \cdot (5 \cdot 9 - 6 \cdot 8) - 2 \cdot (4 \cdot 9 - 6 \cdot 7) + 3 \cdot (4 \cdot 8 - 5 \cdot 7)
$$
$$
\det(B) = 1 \cdot (45 - 48) - 2 \cdot (36 - 42) + 3 \cdot (32 - 35)
$$
$$
\det(B) = 1 \cdot (-3) - 2 \cdot (-6) + 3 \cdot (-3)
$$
$$
\det(B) = -3 + 12 - 9 = 0
$$

### Example 3: Determinant of a $4 \times 4$ Matrix

Consider the matrix:
$$
C = \begin{pmatrix}
1 & 2 & 3 & 4 \\
0 & 1 & 0 & 0 \\
0 & 0 & 1 & 0 \\
0 & 0 & 0 & 1
\end{pmatrix}
$$

The determinant can be directly computed as 1 because it is an upper triangular matrix (with ones on the diagonal):
$$
\det(C) = 1 \cdot 1 \cdot 1 \cdot 1 = 1
$$

## Conclusion

Determinants provide critical insights into the properties of matrices, including their invertibility and the geometric transformations they represent. Understanding how to compute and interpret determinants is essential for various applications in linear algebra and related fields.
