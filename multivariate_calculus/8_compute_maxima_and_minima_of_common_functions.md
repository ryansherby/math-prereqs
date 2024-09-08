## Computing Maxima and Minima of Common Functions in Multivariate Calculus

In multivariate calculus, finding the maxima and minima of functions of several variables involves analyzing critical points where the first derivatives vanish and then using the second derivatives to classify these points. This process extends the single-variable concept of optimization to functions of multiple variables.

### Definition

1. **Critical Points**:
   - **Definition**: A point $(x_0, y_0, \ldots, z_0)$ is called a critical point of a function $f(x, y, \ldots)$ if the gradient of $f$ is zero at that point. The gradient $\nabla f = (f_x, f_y, \ldots)$ is a vector of the first partial derivatives.
   - **Finding Critical Points**: Solve the system of equations given by setting each partial derivative to zero:
   
     $$
     \frac{\partial f}{\partial x} = 0, \quad \frac{\partial f}{\partial y} = 0, \quad \ldots
     $$

2. **Second Derivative Test**:
   - **Definition**: To classify the nature of the critical points, use the second derivatives to form the Hessian matrix. The Hessian matrix $H$ is a square matrix of second-order partial derivatives:
   
     $$
     H = \begin{bmatrix}
     \frac{\partial^2 f}{\partial x^2} & \frac{\partial^2 f}{\partial x \partial y} \\
     \frac{\partial^2 f}{\partial y \partial x} & \frac{\partial^2 f}{\partial y^2}
     \end{bmatrix}
     $$

   - **Classification**:
     - **Local Maximum**: If the Hessian determinant $D > 0$ and $\frac{\partial^2 f}{\partial x^2} < 0$.
     - **Local Minimum**: If the Hessian determinant $D > 0$ and $\frac{\partial^2 f}{\partial x^2} > 0$.
     - **Saddle Point**: If the Hessian determinant $D < 0$.
     - **Inconclusive**: If $D = 0$.

### Examples

1. **Example 1: Function of Two Variables**

   Consider the function $f(x, y) = x^2 + y^2$.

   - **Find Critical Points**:
     Compute the partial derivatives:
     
     $$
     \frac{\partial f}{\partial x} = 2x, \quad \frac{\partial f}{\partial y} = 2y
     $$
     
     Set these derivatives to zero:
     
     $$
     2x = 0 \implies x = 0
     $$
     $$
     2y = 0 \implies y = 0
     $$
     
     So, the critical point is $(0, 0)$.

   - **Second Derivative Test**:
     Compute the second partial derivatives:
     
     $$
     \frac{\partial^2 f}{\partial x^2} = 2, \quad \frac{\partial^2 f}{\partial y^2} = 2, \quad \frac{\partial^2 f}{\partial x \partial y} = 0
     $$
     
     Form the Hessian matrix:
     
     $$
     H = \begin{bmatrix}
     2 & 0 \\
     0 & 2
     \end{bmatrix}
     $$
     
     The determinant is:
     
     $$
     D = (2 \times 2) - (0 \times 0) = 4
     $$
     
     Since $D > 0$ and $\frac{\partial^2 f}{\partial x^2} > 0$, the point $(0, 0)$ is a local minimum.

2. **Example 2: Function with Saddle Point**

   Consider the function $f(x, y) = x^3 - 3xy^2$.

   - **Find Critical Points**:
     Compute the partial derivatives:
     
     $$
     \frac{\partial f}{\partial x} = 3x^2 - 3y^2, \quad \frac{\partial f}{\partial y} = -6xy
     $$
     
     Set these derivatives to zero:
     
     $$
     3x^2 - 3y^2 = 0 \implies x^2 = y^2
     $$
     $$
     -6xy = 0 \implies xy = 0
     $$
     
     So, the critical points are $(0, 0)$ and $(\pm 1, \pm 1)$.

   - **Second Derivative Test**:
     Compute the second partial derivatives:
     
     $$
     \frac{\partial^2 f}{\partial x^2} = 6x, \quad \frac{\partial^2 f}{\partial y^2} = -6x, \quad \frac{\partial^2 f}{\partial x \partial y} = -6y
     $$
     
     Form the Hessian matrix:
     
     $$
     H = \begin{bmatrix}
     6x & -6y \\
     -6y & -6x
     \end{bmatrix}
     $$
     
     At $(0, 0)$:
     
     $$
     H = \begin{bmatrix}
     0 & 0 \\
     0 & 0
     \end{bmatrix}
     $$
     
     The determinant is $D = 0$, which is inconclusive. For $(\pm 1, \pm 1)$, you would find $D < 0$, indicating saddle points.

### Applications

1. **Optimization Problems**: Finding local maxima and minima is crucial in optimization tasks in fields such as economics, engineering, and machine learning.
2. **Surface Analysis**: Understanding the shape of surfaces in 3D graphics and data visualization involves finding critical points and classifying them.

In summary, computing maxima and minima in multivariate calculus involves finding critical points by setting first derivatives to zero and using the second derivative test to classify these points. This process extends the optimization techniques from single-variable calculus to functions of multiple variables.
