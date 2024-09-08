## Limits and Sequences of Functions in Multivariate Calculus

### Limits of Functions

In multivariate calculus, the concept of limits extends to functions of multiple variables. The limit of a function as the variables approach certain values is a fundamental idea used to understand the behavior of functions in higher dimensions.

#### Definition

Let $f(x_1, x_2, \ldots, x_n)$ be a function of $n$ variables. We say that the limit of $f$ as $(x_1, x_2, \ldots, x_n)$ approaches $(a_1, a_2, \ldots, a_n)$ is $L$, and we write:

$$ \lim_{(x_1, x_2, \ldots, x_n) \to (a_1, a_2, \ldots, a_n)} f(x_1, x_2, \ldots, x_n) = L $$

if for every $\epsilon > 0$, there exists a $\delta > 0$ such that whenever:

$$ \sqrt{(x_1 - a_1)^2 + (x_2 - a_2)^2 + \cdots + (x_n - a_n)^2} < \delta $$

and $(x_1, x_2, \ldots, x_n) \neq (a_1, a_2, \ldots, a_n)$, it follows that:

$$ |f(x_1, x_2, \ldots, x_n) - L| < \epsilon $$

#### Example

Consider the function:

$$ f(x, y) = \frac{x^2 y}{x^2 + y^2} $$

We want to find the limit of $f(x, y)$ as $(x, y) \to (0, 0)$. To find this limit, we examine $f$ along different paths approaching $(0, 0)$.

1. **Along the $x$-axis ($y = 0$):**

   $$ f(x, 0) = \frac{x^2 \cdot 0}{x^2 + 0^2} = 0 $$

2. **Along the $y$-axis ($x = 0$):**

   $$ f(0, y) = \frac{0 \cdot y}{0 + y^2} = 0 $$

3. **Along the line $y = x$:**

   $$ f(x, x) = \frac{x^2 \cdot x}{x^2 + x^2} = \frac{x^3}{2x^2} = \frac{x}{2} $$

   As $x \to 0$, $\frac{x}{2} \to 0$.

Since the limit is 0 along different paths, we conclude:

$$ \lim_{(x, y) \to (0, 0)} \frac{x^2 y}{x^2 + y^2} = 0 $$

### Sequences of Functions

A sequence of functions is a list of functions indexed by natural numbers. It is essential to study their convergence properties to understand how functions behave as their indices increase.

#### Definition

Let $\{f_n\}$ be a sequence of functions defined on a domain $D$. We say that $\{f_n\}$ converges pointwise to a function $f$ on $D$ if:

$$ \lim_{n \to \infty} f_n(x) = f(x) \text{ for all } x \in D $$

In other words, for each fixed $x \in D$, the sequence $\{f_n(x)\}$ converges to $f(x)$ as $n \to \infty$.

#### Example

Consider the sequence of functions:

$$ f_n(x) = \frac{x}{n} $$

where $n$ is a positive integer and $x$ is in the domain $[0, 1]$. We want to find the limit function $f(x)$ as $n \to \infty$.

For each fixed $x \in [0, 1]$:

$$ \lim_{n \to \infty} f_n(x) = \lim_{n \to \infty} \frac{x}{n} = 0 $$

Thus, the sequence $\{f_n\}$ converges pointwise to the zero function:

$$ f(x) = 0 $$

### Uniform Convergence

A stronger form of convergence is uniform convergence, which requires that:

$$ \lim_{n \to \infty} \sup_{x \in D} |f_n(x) - f(x)| = 0 $$

Uniform convergence means that the rate of convergence of $f_n(x)$ to $f(x)$ is uniform over the entire domain $D$.

#### Example

Consider the sequence of functions:

$$ f_n(x) = \frac{x}{n} $$

on the domain $[0, 1]$. We previously determined that $f_n(x) \to 0$ pointwise. To check for uniform convergence:

$$ \sup_{x \in [0, 1]} |f_n(x) - 0| = \sup_{x \in [0, 1]} \frac{x}{n} = \frac{1}{n} $$

As $n \to \infty$, $\frac{1}{n} \to 0$, which indicates uniform convergence to the zero function.

### Conclusion

Understanding limits and sequences of functions is crucial in multivariate calculus, as these concepts help analyze the behavior of functions in higher dimensions and understand convergence properties. Limits provide insights into the function’s behavior near a point, while sequences and their convergence illustrate how functions evolve with increasing indices.
