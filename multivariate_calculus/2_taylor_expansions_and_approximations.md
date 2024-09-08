## Taylor Expansions and Approximations in Multivariate Calculus

In multivariate calculus, Taylor expansions are used to approximate functions near a point by polynomials. The Taylor series of a function provides an approximation based on the function's derivatives at a specific point. This approximation becomes more accurate as more terms are included in the series.

### Definition

The **Taylor series** of a function $f(\mathbf{x})$ around a point $\mathbf{a}$ in $\mathbb{R}^n$ is an infinite sum of terms calculated from the values of the function's derivatives at $\mathbf{a}$. For a function $f: \mathbb{R}^n \to \mathbb{R}$, the Taylor series expansion around the point $\mathbf{a} = (a_1, a_2, \ldots, a_n)$ is given by:

$$
f(\mathbf{x}) \approx f(\mathbf{a}) + \sum_{i=1}^n \frac{\partial f}{\partial x_i} (\mathbf{a}) (x_i - a_i) + \frac{1}{2!} \sum_{i=1}^n \sum_{j=1}^n \frac{\partial^2 f}{\partial x_i \partial x_j} (\mathbf{a}) (x_i - a_i)(x_j - a_j) + \cdots
$$

where:
- $\mathbf{x} = (x_1, x_2, \ldots, x_n)$ is a point near $\mathbf{a}$.
- $f(\mathbf{a})$ is the value of the function at $\mathbf{a}$.
- $\frac{\partial f}{\partial x_i} (\mathbf{a})$ is the first partial derivative of $f$ with respect to $x_i$ at $\mathbf{a}$.
- $\frac{\partial^2 f}{\partial x_i \partial x_j} (\mathbf{a})$ is the second partial derivative of $f$ with respect to $x_i$ and $x_j$ at $\mathbf{a}$.

### Taylor Expansion Up to Second Order

For practical applications, we often use the Taylor expansion up to the second-order terms:

$$
f(\mathbf{x}) \approx f(\mathbf{a}) + \sum_{i=1}^n \frac{\partial f}{\partial x_i} (\mathbf{a}) (x_i - a_i) + \frac{1}{2} \sum_{i=1}^n \sum_{j=1}^n \frac{\partial^2 f}{\partial x_i \partial x_j} (\mathbf{a}) (x_i - a_i)(x_j - a_j)
$$

### Examples

1. **Function of Two Variables**:
   - Consider the function $f(x, y) = e^{x+y}$.
   - To approximate $f(x, y)$ around the point $(0, 0)$, we compute:
     - $f(0, 0) = e^0 = 1$.
     - The first partial derivatives are $\frac{\partial f}{\partial x} = e^{x+y}$ and $\frac{\partial f}{\partial y} = e^{x+y}$.
     - At $(0, 0)$, $\frac{\partial f}{\partial x}(0, 0) = 1$ and $\frac{\partial f}{\partial y}(0, 0) = 1$.
     - The second partial derivatives are $\frac{\partial^2 f}{\partial x^2} = e^{x+y}$, $\frac{\partial^2 f}{\partial y^2} = e^{x+y}$, and $\frac{\partial^2 f}{\partial x \partial y} = e^{x+y}$.
     - At $(0, 0)$, $\frac{\partial^2 f}{\partial x^2}(0, 0) = 1$, $\frac{\partial^2 f}{\partial y^2}(0, 0) = 1$, and $\frac{\partial^2 f}{\partial x \partial y}(0, 0) = 1$.

     Therefore, the second-order Taylor expansion of $f(x, y)$ around $(0, 0)$ is:

     $$
     f(x, y) \approx 1 + x + y + \frac{1}{2} (x^2 + y^2 + 2xy) = 1 + x + y + \frac{1}{2} (x^2 + y^2 + 2xy)
     $$

2. **Quadratic Approximation**:
   - For a function $f(x, y) = \sin(x) \cos(y)$, let’s approximate around $(0, 0)$.
     - $f(0, 0) = \sin(0) \cos(0) = 0$.
     - First derivatives: $\frac{\partial f}{\partial x} = \cos(x) \cos(y)$ and $\frac{\partial f}{\partial y} = -\sin(x) \sin(y)$.
     - At $(0, 0)$: $\frac{\partial f}{\partial x}(0, 0) = 1$ and $\frac{\partial f}{\partial y}(0, 0) = 0$.
     - Second derivatives: $\frac{\partial^2 f}{\partial x^2} = -\sin(x) \cos(y)$, $\frac{\partial^2 f}{\partial y^2} = -\sin(x) \cos(y)$, and $\frac{\partial^2 f}{\partial x \partial y} = -\cos(x) \sin(y)$.
     - At $(0, 0)$: $\frac{\partial^2 f}{\partial x^2}(0, 0) = 0$, $\frac{\partial^2 f}{\partial y^2}(0, 0) = 0$, and $\frac{\partial^2 f}{\partial x \partial y}(0, 0) = 0$.

     Therefore, the second-order Taylor expansion of $f(x, y)$ around $(0, 0)$ is simply:

     $$
     f(x, y) \approx 0 + x + 0 = x
     $$

### Applications

1. **Optimization**: Taylor expansions help approximate functions to find local minima or maxima by analyzing the function's behavior around critical points.
2. **Numerical Methods**: Used to approximate solutions to differential equations and perform interpolation.
3. **Error Analysis**: Provides insight into how errors in approximations propagate and how accurate an approximation is.

### Conclusion

Taylor expansions are a powerful tool in multivariate calculus for approximating functions near a point. By using derivatives to build polynomial approximations, they offer valuable insights and facilitate various applications in analysis, optimization, and numerical methods.

