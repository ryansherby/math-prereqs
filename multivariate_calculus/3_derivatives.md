## Derivatives in Multivariate Calculus

In multivariate calculus, derivatives extend the concept of the derivative from single-variable calculus to functions of multiple variables. They provide insights into how a function changes as its input variables change, and are crucial for analyzing and optimizing multivariable functions.

### Definition

For a function $f: \mathbb{R}^n \to \mathbb{R}$, where $f$ maps from $n$-dimensional space to real numbers, the derivative measures how the function $f$ changes with respect to changes in its input variables.

1. **Partial Derivatives**:
   - **Definition**: The partial derivative of $f$ with respect to the variable $x_i$ is the derivative of $f$ while keeping all other variables constant. It is denoted as $\frac{\partial f}{\partial x_i}$.
   - **Formula**: If $f(x_1, x_2, \ldots, x_n)$ is a function of $n$ variables, then the partial derivative with respect to $x_i$ is:

     $$
     \frac{\partial f}{\partial x_i} = \lim_{h \to 0} \frac{f(x_1, \ldots, x_i + h, \ldots, x_n) - f(x_1, \ldots, x_i, \ldots, x_n)}{h}
     $$

   - **Example**: For the function $f(x, y) = x^2 y + 3xy^2$, the partial derivatives are:

     $$
     \frac{\partial f}{\partial x} = 2xy + 3y^2
     $$

     $$
     \frac{\partial f}{\partial y} = x^2 + 6xy
     $$

2. **Gradient**:
   - **Definition**: The gradient of $f$, denoted as $\nabla f$ or $\text{grad}\ f$, is a vector of all partial derivatives. It points in the direction of the steepest ascent of the function.
   - **Formula**: For a function $f(x_1, x_2, \ldots, x_n)$, the gradient is:

     $$
     \nabla f = \left( \frac{\partial f}{\partial x_1}, \frac{\partial f}{\partial x_2}, \ldots, \frac{\partial f}{\partial x_n} \right)
     $$

   - **Example**: For $f(x, y) = x^2 + y^2$, the gradient is:

     $$
     \nabla f = \left( \frac{\partial f}{\partial x}, \frac{\partial f}{\partial y} \right) = (2x, 2y)
     $$

3. **Directional Derivatives**:
   - **Definition**: The directional derivative of $f$ in the direction of a vector $\mathbf{v}$ measures the rate of change of $f$ as one moves in the direction of $\mathbf{v}$. It is denoted as $D_{\mathbf{v}} f$.
   - **Formula**: The directional derivative is given by:

     $$
     D_{\mathbf{v}} f = \nabla f \cdot \frac{\mathbf{v}}{\|\mathbf{v}\|}
     $$

   - **Example**: For the function $f(x, y) = x^2 + y^2$, and direction vector $\mathbf{v} = (1, 1)$, the directional derivative is:

     $$
     D_{\mathbf{v}} f = \nabla f \cdot \frac{\mathbf{v}}{\|\mathbf{v}\|} = (2x, 2y) \cdot \frac{(1, 1)}{\sqrt{2}} = \frac{2x + 2y}{\sqrt{2}}
     $$

4. **Jacobian Matrix**:
   - **Definition**: For vector-valued functions, the Jacobian matrix represents all first-order partial derivatives of a vector-valued function with respect to its input variables.
   - **Formula**: If $\mathbf{F}(\mathbf{x}) = \left( f_1(x_1, \ldots, x_n), f_2(x_1, \ldots, x_n), \ldots, f_m(x_1, \ldots, x_n) \right)$, the Jacobian matrix $J_{\mathbf{F}}$ is:

     $$
     J_{\mathbf{F}} = \begin{pmatrix}
     \frac{\partial f_1}{\partial x_1} & \frac{\partial f_1}{\partial x_2} & \cdots & \frac{\partial f_1}{\partial x_n} \\
     \frac{\partial f_2}{\partial x_1} & \frac{\partial f_2}{\partial x_2} & \cdots & \frac{\partial f_2}{\partial x_n} \\
     \vdots & \vdots & \ddots & \vdots \\
     \frac{\partial f_m}{\partial x_1} & \frac{\partial f_m}{\partial x_2} & \cdots & \frac{\partial f_m}{\partial x_n}
     \end{pmatrix}
     $$

   - **Example**: For $\mathbf{F}(x, y) = \left( x^2 y, xy^2 \right)$, the Jacobian matrix is:

     $$
     J_{\mathbf{F}} = \begin{pmatrix}
     y & x^2 \\
     y^2 & 2xy
     \end{pmatrix}
     $$

### Applications

1. **Optimization**: Derivatives are used to find local maxima and minima of functions, which is crucial in various fields including economics and engineering.
2. **Modeling and Analysis**: Derivatives help in understanding the behavior of functions, such as rates of change and sensitivities.
3. **Physics and Engineering**: Derivatives are used to model physical phenomena such as motion and forces.

In summary, derivatives in multivariate calculus extend the concept of a derivative to functions of multiple variables, providing a framework for analyzing changes in functions with respect to several inputs. Understanding partial derivatives, gradients, directional derivatives, and the Jacobian matrix is essential for solving complex problems in various fields.
