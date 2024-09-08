# Expectations in Applied Probability

In applied probability, the **expectation** (or expected value) is a fundamental concept that provides a measure of the central tendency of a random variable. It represents the average value that one would expect to obtain from a random experiment if it were repeated many times.

## Definition

The **expectation** (or **expected value**) of a random variable is a weighted average of all possible values that the random variable can take, where the weights are the probabilities associated with each value. It provides a single summary measure of the central location of the distribution of the random variable.

### Discrete Random Variables

For a discrete random variable $X$ with possible values $x_1, x_2, x_3, \ldots$ and corresponding probabilities $P(X = x_i)$, the expectation $E[X]$ is given by:

$$
E[X] = \sum_{i} x_i \cdot P(X = x_i)
$$

### Continuous Random Variables

For a continuous random variable $X$ with probability density function (PDF) $f_X(x)$, the expectation $E[X]$ is given by:

$$
E[X] = \int_{-\infty}^{\infty} x \cdot f_X(x) \, dx
$$

## Examples

1. **Discrete Random Variable**:
   - Let $X$ be the outcome of rolling a fair six-sided die.
   - The possible values of $X$ are $\{1, 2, 3, 4, 5, 6\}$, each with probability $\frac{1}{6}$.
   - The expectation of $X$ is:
     $$
     E[X] = \sum_{i=1}^{6} i \cdot \frac{1}{6} = \frac{1}{6} (1 + 2 + 3 + 4 + 5 + 6) = \frac{21}{6} = 3.5
     $$
     So, the expected value of rolling a fair die is 3.5.

2. **Continuous Random Variable**:
   - Let $X$ be a random variable uniformly distributed between 0 and 1.
   - The PDF of $X$ is $f_X(x) = 1$ for $0 \leq x \leq 1$.
   - The expectation of $X$ is:
     $$
     E[X] = \int_{0}^{1} x \cdot 1 \, dx = \left[ \frac{x^2}{2} \right]_{0}^{1} = \frac{1}{2}
     $$
     So, the expected value of a uniformly distributed random variable between 0 and 1 is $\frac{1}{2}$.

3. **Normal Distribution**:
   - Let $X$ be a random variable following a normal distribution with mean $\mu$ and variance $\sigma^2$.
   - The expectation of $X$ is simply the mean $\mu$:
     $$
     E[X] = \mu
     $$
     This tells us that the expected value of a normally distributed random variable is the mean of the distribution.

## Key Properties

- **Linearity of Expectation**: The expectation operator is linear, which means for any random variables $X$ and $Y$, and constants $a$ and $b$:
  $$
  E[aX + bY] = aE[X] + bE[Y]
  $$

- **Expectation of a Function**: If $g(X)$ is a function of the random variable $X$, then the expectation of $g(X)$ is:
  $$
  E[g(X)] = \sum_{i} g(x_i) \cdot P(X = x_i) \text{ for discrete } X
  $$
  $$
  E[g(X)] = \int_{-\infty}^{\infty} g(x) \cdot f_X(x) \, dx \text{ for continuous } X
  $$

## Conclusion

The expectation is a crucial concept in probability theory that provides the average or mean value of a random variable. It is calculated differently for discrete and continuous random variables but serves the same purpose of summarizing the central tendency of the distribution. Understanding expectations helps in various applications, including decision-making, risk assessment, and statistical analysis.