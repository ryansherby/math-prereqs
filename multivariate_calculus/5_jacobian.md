## Jacobian in Multivariate Calculus

### Definition

The **Jacobian** is a matrix of first-order partial derivatives of a vector-valued function. It generalizes the concept of the derivative to functions of multiple variables and provides information about the rate of change and the local behavior of the function. Specifically, it is used to describe how changes in the input variables of a multivariable function affect the output variables.

Given a function $\mathbf{F} : \mathbb{R}^n \to \mathbb{R}^m$, where:

$$ \mathbf{F}(x_1, x_2, \ldots, x_n) = (f_1(x_1, x_2, \ldots, x_n), f_2(x_1, x_2, \ldots, x_n), \ldots, f_m(x_1, x_2, \ldots, x_n)) $$

the Jacobian matrix $J$ of $\mathbf{F}$ is defined as:

$$ J = \begin{bmatrix}
\frac{\partial f_1}{\partial x_1} & \frac{\partial f_1}{\partial x_2} & \cdots & \frac{\partial f_1}{\partial x_n} \\
\frac{\partial f_2}{\partial x_1} & \frac{\partial f_2}{\partial x_2} & \cdots & \frac{\partial f_2}{\partial x_n} \\
\vdots & \vdots & \ddots & \vdots \\
\frac{\partial f_m}{\partial x_1} & \frac{\partial f_m}{\partial x_2} & \cdots & \frac{\partial f_m}{\partial x_n}
\end{bmatrix} $$

### Interpretation

- **Local Linearity**: The Jacobian matrix provides a linear approximation of the function $\mathbf{F}$ near a point. In other words, it approximates how small changes in the input variables affect the output variables in the neighborhood of that point.
- **Determinant**: The determinant of the Jacobian matrix, known as the Jacobian determinant, is crucial in many applications, including change of variables in multiple integrals. It measures the scaling factor of the volume when the function maps an infinitesimal volume from the input space to the output space.

### Examples

1. **Example 1: Two-dimensional Function**

   Consider the function:

   $$ \mathbf{F}(x, y) = (x^2 y, \sin(x + y)) $$

   The Jacobian matrix of $\mathbf{F}$ is:

   $$ J = \begin{bmatrix}
   \frac{\partial}{\partial x}(x^2 y) & \frac{\partial}{\partial y}(x^2 y) \\
   \frac{\partial}{\partial x}(\sin(x + y)) & \frac{\partial}{\partial y}(\sin(x + y))
   \end{bmatrix} = \begin{bmatrix}
   2xy & x^2 \\
   \cos(x + y) & \cos(x + y)
   \end{bmatrix} $$

   Here, $2xy$ is the partial derivative of $x^2 y$ with respect to $x$, and $\cos(x + y)$ is the partial derivative of $\sin(x + y)$ with respect to $x$.

2. **Example 2: Change of Variables in Integration**

   Suppose we want to change variables in a double integral using:

   $$ \mathbf{F}(x, y) = (u, v) = (x^2 - y^2, 2xy) $$

   The Jacobian matrix of this transformation is:

   $$ J = \begin{bmatrix}
   \frac{\partial u}{\partial x} & \frac{\partial u}{\partial y} \\
   \frac{\partial v}{\partial x} & \frac{\partial v}{\partial y}
   \end{bmatrix} = \begin{bmatrix}
   2x & -2y \\
   2y & 2x
   \end{bmatrix} $$

   The Jacobian determinant, which is:

   $$ \text{det}(J) = (2x \cdot 2x) - (-2y \cdot 2y) = 4x^2 + 4y^2 $$

   is used to adjust the integrand when transforming the variables in the integral.

### Conclusion

The Jacobian matrix is an essential tool in multivariate calculus, providing insights into how functions of multiple variables behave locally. It is widely used in optimization, numerical analysis, and when performing transformations in integration. Understanding the Jacobian helps in analyzing the effects of variable changes and the geometric properties of functions.
