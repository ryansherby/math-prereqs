# Solving Systems of Linear Equations in Linear Algebra

A system of linear equations is a collection of one or more linear equations involving the same set of variables. Solving such systems involves finding the values of the variables that satisfy all the equations simultaneously. There are various methods for solving systems of linear equations, including substitution, elimination, and matrix methods.

## Definition of a System of Linear Equations

A system of linear equations can be expressed in the general form:
$$
\begin{cases}
a_{11} x_1 + a_{12} x_2 + \cdots + a_{1n} x_n = b_1 \\
a_{21} x_1 + a_{22} x_2 + \cdots + a_{2n} x_n = b_2 \\
\vdots \\
a_{m1} x_1 + a_{m2} x_2 + \cdots + a_{mn} x_n = b_m
\end{cases}
$$
where $a_{ij}$ are the coefficients, $x_j$ are the variables, and $b_i$ are the constants on the right-hand side of the equations.

## Methods for Solving Systems of Linear Equations

### 1. Substitution Method

In the substitution method, you solve one of the equations for one variable and then substitute this expression into the other equations.

**Steps**:
1. Solve one of the equations for one of the variables.
2. Substitute this expression into the other equations.
3. Solve the resulting equations, and back-substitute to find the values of all variables.

**Example**:
Solve the system:
$$
\begin{cases}
x + y = 5 \\
2x - y = 1
\end{cases}
$$

1. Solve the first equation for $y$:
   $$
   y = 5 - x
   $$

2. Substitute $y = 5 - x$ into the second equation:
   $$
   2x - (5 - x) = 1
   $$
   $$
   2x - 5 + x = 1
   $$
   $$
   3x - 5 = 1
   $$
   $$
   3x = 6
   $$
   $$
   x = 2
   $$

3. Substitute $x = 2$ back into $y = 5 - x$:
   $$
   y = 5 - 2 = 3
   $$

   Solution: $x = 2$, $y = 3$.

### 2. Elimination Method

In the elimination method, you eliminate one variable by adding or subtracting equations.

**Steps**:
1. Arrange the equations with the same variables in a column.
2. Add or subtract equations to eliminate one of the variables.
3. Solve the resulting simpler system and back-substitute to find the values of all variables.

**Example**:
Solve the system:
$$
\begin{cases}
3x + 4y = 14 \\
2x - y = 1
\end{cases}
$$

1. Multiply the second equation by 4 to match the coefficients of $y$:
   $$
   8x - 4y = 4
   $$

2. Add this to the first equation:
   $$
   (3x + 4y) + (8x - 4y) = 14 + 4
   $$
   $$
   11x = 18
   $$
   $$
   x = \frac{18}{11}
   $$

3. Substitute $x = \frac{18}{11}$ into the second equation:
   $$
   2 \left(\frac{18}{11}\right) - y = 1
   $$
   $$
   \frac{36}{11} - y = 1
   $$
   $$
   y = \frac{36}{11} - 1
   $$
   $$
   y = \frac{25}{11}
   $$

   Solution: $x = \frac{18}{11}$, $y = \frac{25}{11}$.

### 3. Matrix Method (Gaussian Elimination)

In the matrix method, you represent the system of equations as an augmented matrix and use row operations to reduce it to row-echelon form or reduced row-echelon form.

**Steps**:
1. Write the augmented matrix for the system.
2. Use row operations to simplify the matrix to row-echelon form.
3. Solve the system using back substitution.

**Example**:
Solve the system:
$$
\begin{cases}
x + 2y - z = 4 \\
2x - y + 3z = 1 \\
3x + 4y + 2z = 7
\end{cases}
$$

1. Write the augmented matrix:
   $$
   \begin{pmatrix}
   1 & 2 & -1 & | & 4 \\
   2 & -1 & 3 & | & 1 \\
   3 & 4 & 2 & | & 7
   \end{pmatrix}
   $$

2. Perform row operations to achieve row-echelon form:
   - Subtract 2 times the first row from the second row.
   - Subtract 3 times the first row from the third row.

   After simplifications:
   $$
   \begin{pmatrix}
   1 & 2 & -1 & | & 4 \\
   0 & -5 & 5 & | & -7 \\
   0 & -2 & 5 & | & -5
   \end{pmatrix}
   $$

   - Add 2 times the second row to the third row.

   After simplifications:
   $$
   \begin{pmatrix}
   1 & 2 & -1 & | & 4 \\
   0 & -5 & 5 & | & -7 \\
   0 & 0 & 0 & | & -1
   \end{pmatrix}
   $$

3. Solve using back substitution. Here, you will find that the system has no solutions because the last row suggests an inconsistency.

## Conclusion

Solving systems of linear equations involves finding values for variables that satisfy all given equations simultaneously. Various methods, including substitution, elimination, and matrix approaches, can be used depending on the system's complexity and the number of equations and variables.
