## Variance in Applied Probability

### Definition

**Variance** is a measure of the dispersion or spread of a set of values. It quantifies how much the values of a random variable differ from their mean. In probability and statistics, variance is used to understand the variability or uncertainty associated with a random variable.

### Formal Definition

For a random variable $X$, the variance is defined as the expected value of the squared deviation of $X$ from its mean $\mu$. It is given by:

$$ \text{Var}(X) = E[(X - \mu)^2] $$

where:

- $E[\cdot]$ denotes the expectation operator.
- $\mu = E[X]$ is the mean or expected value of $X$.

### Calculation

1. **For a Discrete Random Variable**

   If $X$ is a discrete random variable with possible values $x_i$ and corresponding probabilities $p_i$, the variance is calculated as:

   $$ \text{Var}(X) = \sum_{i} p_i (x_i - \mu)^2 $$

   where $\mu$ is the mean of $X$:

   $$ \mu = \sum_{i} p_i x_i $$

2. **For a Continuous Random Variable**

   If $X$ is a continuous random variable with probability density function $f(x)$, the variance is given by:

   $$ \text{Var}(X) = \int_{-\infty}^{\infty} (x - \mu)^2 f(x) \, dx $$

   where $\mu$ is the mean of $X$:

   $$ \mu = \int_{-\infty}^{\infty} x f(x) \, dx $$

### Examples

1. **Example 1: Rolling a Die**

   Consider a fair six-sided die. The random variable $X$ represents the outcome of a roll. The mean of $X$ is:

   $$ \mu = \frac{1 + 2 + 3 + 4 + 5 + 6}{6} = 3.5 $$

   The variance is calculated as:

   $$ \text{Var}(X) = \frac{1}{6} \left[(1 - 3.5)^2 + (2 - 3.5)^2 + (3 - 3.5)^2 + (4 - 3.5)^2 + (5 - 3.5)^2 + (6 - 3.5)^2 \right] = 2.9167 $$

2. **Example 2: Exam Scores**

   Suppose a class of students took an exam, and their scores are as follows: 70, 75, 80, 85, and 90. The mean score is:

   $$ \mu = \frac{70 + 75 + 80 + 85 + 90}{5} = 80 $$

   The variance is:

   $$ \text{Var}(X) = \frac{1}{5} \left[(70 - 80)^2 + (75 - 80)^2 + (80 - 80)^2 + (85 - 80)^2 + (90 - 80)^2 \right] = 62.5 $$

3. **Example 3: Heights of Plants**

   Imagine you are studying the heights of plants in a garden. Suppose the heights in centimeters are: 30, 35, 40, 45, and 50. The mean height is:

   $$ \mu = \frac{30 + 35 + 40 + 45 + 50}{5} = 40 $$

   The variance is:

   $$ \text{Var}(X) = \frac{1}{5} \left[(30 - 40)^2 + (35 - 40)^2 + (40 - 40)^2 + (45 - 40)^2 + (50 - 40)^2 \right] = 62.5 $$

### Conclusion

Variance is a key concept in applied probability that measures the extent to which the values of a random variable spread out from the mean. It is essential for understanding the variability and uncertainty of data, and is widely used in statistical analysis and decision-making.
