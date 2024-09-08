# Rank in Linear Algebra

The **rank** of a matrix is a fundamental concept in linear algebra that provides insight into the matrix's properties and the linear systems it represents. The rank of a matrix is closely related to the dimensions of vector spaces and the solutions to systems of linear equations.

## Definition of Matrix Rank

The **rank** of a matrix $A$ is defined as the maximum number of linearly independent rows or columns in the matrix. It is a measure of the dimension of the vector space generated by the rows or columns of the matrix.

### Formal Definition

1. **Row Rank**: The row rank of a matrix is the number of linearly independent rows in the matrix. 
2. **Column Rank**: The column rank of a matrix is the number of linearly independent columns in the matrix. 

For any matrix, the row rank and column rank are always equal. This common value is simply referred to as the rank of the matrix.

Mathematically, if $A$ is an $m \times n$ matrix, the rank of $A$, denoted as $\text{rank}(A)$, can be expressed as:
$$
\text{rank}(A) = \text{number of linearly independent rows} = \text{number of linearly independent columns}
$$

## Properties of Matrix Rank

1. **Rank and Dimensions**: For an $m \times n$ matrix $A$, the rank is at most $\min(m, n)$. This means:
   $$
   \text{rank}(A) \leq \min(m, n)
   $$

2. **Rank and Determinant**: If $A$ is a square matrix, then $A$ is invertible if and only if $\text{rank}(A) = n$, where $n$ is the size of the matrix.

3. **Rank and Solutions**: The rank of a matrix is related to the number of solutions to the system of linear equations represented by the matrix. For a system $Ax = b$, where $A$ is the coefficient matrix, the number of solutions depends on the rank of $A$ and the augmented matrix $[A|b]$.

4. **Rank Preservation**: The rank of a matrix is preserved under elementary row operations, such as row swapping, scaling, and adding multiples of rows.

## Examples of Matrix Rank

### Example 1: Determining Rank of a $2 \times 2$ Matrix

Consider the matrix:
$$
A = \begin{pmatrix} 1 & 2 \\ 3 & 4 \end{pmatrix}
$$

1. **Find Row Rank**:
   - The rows are $(1, 2)$ and $(3, 4)$. To check if these rows are linearly independent, note that no scalar multiple of $(1, 2)$ can produce $(3, 4)$.
   - Therefore, the rows are linearly independent.

2. **Find Column Rank**:
   - The columns are $(1, 3)$ and $(2, 4)$. To check if these columns are linearly independent, note that no scalar multiple of $(1, 3)$ can produce $(2, 4)$.
   - Therefore, the columns are linearly independent.

Thus, the rank of matrix $A$ is:
$$
\text{rank}(A) = 2
$$

### Example 2: Determining Rank of a $3 \times 3$ Matrix

Consider the matrix:
$$
B = \begin{pmatrix} 1 & 0 & 0 \\ 2 & 1 & 0 \\ 3 & 4 & 1 \end{pmatrix}
$$

1. **Row Reduction**:
   - Applying row operations to transform $B$ into row echelon form:
     $$
     \begin{pmatrix} 1 & 0 & 0 \\ 2 & 1 & 0 \\ 3 & 4 & 1 \end{pmatrix} \rightarrow \begin{pmatrix} 1 & 0 & 0 \\ 0 & 1 & 0 \\ 0 & 0 & 1 \end{pmatrix}
     $$

   - The matrix in row echelon form has 3 non-zero rows, indicating that all rows are linearly independent.

2. **Rank Calculation**:
   - Since there are 3 linearly independent rows, the rank of matrix $B$ is:
     $$
     \text{rank}(B) = 3
     $$

### Example 3: Determining Rank of a $3 \times 2$ Matrix

Consider the matrix:
$$
C = \begin{pmatrix} 1 & 2 \\ 3 & 4 \\ 5 & 6 \end{pmatrix}
$$

1. **Row Reduction**:
   - Applying row operations to transform $C$ into row echelon form:
     $$
     \begin{pmatrix} 1 & 2 \\ 3 & 4 \\ 5 & 6 \end{pmatrix} \rightarrow \begin{pmatrix} 1 & 2 \\ 0 & -2 \\ 0 & 0 \end{pmatrix}
     $$

   - The matrix in row echelon form has 2 non-zero rows.

2. **Rank Calculation**:
   - Since there are 2 linearly independent rows, the rank of matrix $C$ is:
     $$
     \text{rank}(C) = 2
     $$

## Conclusion

The rank of a matrix is a key concept in linear algebra that provides valuable information about the matrix's structure, the solutions of linear systems, and the dimensions of associated vector spaces. Understanding matrix rank is essential for solving many linear algebra problems and applications.