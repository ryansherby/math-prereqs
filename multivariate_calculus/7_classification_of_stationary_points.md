## Classification of Stationary Points in Multivariate Calculus

In multivariate calculus, stationary points (or critical points) of a function are where the gradient of the function is zero. These points can be classified to understand their nature, whether they correspond to local minima, local maxima, or saddle points. The classification is typically done using the second derivative test, involving the Hessian matrix.

### Definition

A stationary point of a function $f: \mathbb{R}^n \to \mathbb{R}$ is a point $\mathbf{x}^*$ where the gradient of $f$ is zero:

$$
\nabla f(\mathbf{x}^*) = \mathbf{0}
$$

To classify these points, we use the Hessian matrix, which contains all second-order partial derivatives of $f$.

### Hessian Matrix

The Hessian matrix $H_f$ of a function $f(x_1, x_2, \ldots, x_n)$ is defined as:

$$
H_f(\mathbf{x}) = \begin{pmatrix}
\frac{\partial^2 f}{\partial x_1^2} & \frac{\partial^2 f}{\partial x_1 \partial x_2} & \cdots & \frac{\partial^2 f}{\partial x_1 \partial x_n} \\
\frac{\partial^2 f}{\partial x_2 \partial x_1} & \frac{\partial^2 f}{\partial x_2^2} & \cdots & \frac{\partial^2 f}{\partial x_2 \partial x_n} \\
\vdots & \vdots & \ddots & \vdots \\
\frac{\partial^2 f}{\partial x_n \partial x_1} & \frac{\partial^2 f}{\partial x_n \partial x_2} & \cdots & \frac{\partial^2 f}{\partial x_n^2}
\end{pmatrix}
$$

### Classification of Stationary Points

1. **Local Minimum**:
   - **Condition**: A stationary point $\mathbf{x}^*$ is a local minimum if the Hessian matrix $H_f(\mathbf{x}^*)$ is positive definite.
   - **Positive Definiteness**: All eigenvalues of the Hessian are positive, meaning that for any non-zero vector $\mathbf{v}$:

     $$
     \mathbf{v}^T H_f(\mathbf{x}^*) \mathbf{v} > 0
     $$

   - **Example**: For $f(x, y) = x^2 + y^2$, the Hessian matrix is:

     $$
     H_f = \begin{pmatrix}
     2 & 0 \\
     0 & 2
     \end{pmatrix}
     $$

     Since the Hessian matrix is positive definite, $(0,0)$ is a local minimum.

2. **Local Maximum**:
   - **Condition**: A stationary point $\mathbf{x}^*$ is a local maximum if the Hessian matrix $H_f(\mathbf{x}^*)$ is negative definite.
   - **Negative Definiteness**: All eigenvalues of the Hessian are negative, meaning that for any non-zero vector $\mathbf{v}$:

     $$
     \mathbf{v}^T H_f(\mathbf{x}^*) \mathbf{v} < 0
     $$

   - **Example**: For $f(x, y) = -x^2 - y^2$, the Hessian matrix is:

     $$
     H_f = \begin{pmatrix}
     -2 & 0 \\
     0 & -2
     \end{pmatrix}
     $$

     Since the Hessian matrix is negative definite, $(0,0)$ is a local maximum.

3. **Saddle Point**:
   - **Condition**: A stationary point $\mathbf{x}^*$ is a saddle point if the Hessian matrix $H_f(\mathbf{x}^*)$ is neither positive definite nor negative definite (i.e., it has both positive and negative eigenvalues).
   - **Example**: For $f(x, y) = x^2 - y^2$, the Hessian matrix is:

     $$
     H_f = \begin{pmatrix}
     2 & 0 \\
     0 & -2
     \end{pmatrix}
     $$

     Since the Hessian matrix has both positive and negative eigenvalues, $(0,0)$ is a saddle point.

4. **Inconclusive**:
   - **Condition**: If the Hessian matrix is singular (i.e., its determinant is zero) or if the test cannot determine definitively, the classification of the stationary point is inconclusive. Further analysis or methods are required to classify the point.

### Determinant of Hessian

To simplify classification, the determinant of the Hessian matrix $D$ is often used:
- **Local Minimum**: $D > 0$ and $\frac{\partial^2 f}{\partial x_i^2} > 0$ for all $i$.
- **Local Maximum**: $D > 0$ and $\frac{\partial^2 f}{\partial x_i^2} < 0$ for all $i$.
- **Saddle Point**: $D < 0$.

### Applications

1. **Optimization**: Identifying local minima and maxima is crucial in optimization problems to find the best solutions.
2. **Economics and Engineering**: In modeling and analysis, understanding the nature of stationary points helps in decision-making and system design.

In summary, the classification of stationary points involves analyzing the Hessian matrix at critical points to determine if they are local minima, local maxima, or saddle points. This classification is essential for understanding the behavior of multivariable functions and solving optimization problems.
