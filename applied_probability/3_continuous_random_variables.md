# Continuous Random Variables in Applied Probability

In applied probability, a **continuous random variable** is a key concept used to model scenarios where outcomes can take any value within a continuous range. Continuous random variables are essential for analyzing and interpreting data in various real-world contexts.

## Definition

A **continuous random variable** is a variable that can take any value within a continuous range or interval. Unlike discrete random variables, continuous random variables can assume an infinite number of values within a given range.

- **Probability Density Function (PDF)**: The probability density function $f_X(x)$ defines the likelihood of a continuous random variable $X$ taking a specific value $x$. It provides the density of probability rather than the probability of a specific outcome. The probability that $X$ falls within a certain range is given by the integral of the PDF over that range:
  $$
  P(a \leq X \leq b) = \int_a^b f_X(x) \, dx
  $$

- **Sample Space ($\Omega$)**: The sample space for a continuous random variable is an interval or union of intervals on the real number line, such as $(a, b)$ or $(-\infty, \infty)$.

## Examples

1. **Height of Individuals**:
   - Let $X$ be the height of a randomly selected individual.
   - Sample Space: $(-\infty, \infty)$ (though practically limited to a reasonable range)
   - If $X$ follows a normal distribution with mean $\mu$ and standard deviation $\sigma$, the PDF is:
     $$
     f_X(x) = \frac{1}{\sigma \sqrt{2 \pi}} \exp \left(-\frac{(x - \mu)^2}{2\sigma^2}\right)
     $$

2. **Time Until a Bus Arrives**:
   - Let $Y$ be the time (in minutes) until the next bus arrives.
   - Sample Space: $[0, \infty)$
   - If $Y$ follows an exponential distribution with rate parameter $\lambda$, the PDF is:
     $$
     f_Y(y) = \lambda e^{-\lambda y}
     $$
     for $y \geq 0$.

3. **Temperature Measurements**:
   - Let $Z$ be the temperature in degrees Celsius measured over a day.
   - Sample Space: $(-\infty, \infty)$ (though practical measurements are within a certain range)
   - Suppose $Z$ follows a normal distribution with mean $\mu$ and variance $\sigma^2$, then the PDF is:
     $$
     f_Z(z) = \frac{1}{\sigma \sqrt{2 \pi}} \exp \left(-\frac{(z - \mu)^2}{2\sigma^2}\right)
     $$

## Key Properties

- **Expectation (Mean)**: The expected value $E[X]$ of a continuous random variable $X$ is given by:
  $$
  E[X] = \int_{-\infty}^{\infty} x \cdot f_X(x) \, dx
  $$

- **Variance**: The variance $\text{Var}(X)$ of a continuous random variable $X$ measures the spread of its values around the mean. It is given by:
  $$
  \text{Var}(X) = E[(X - E[X])^2] = \int_{-\infty}^{\infty} (x - E[X])^2 \cdot f_X(x) \, dx
  $$

- **Cumulative Distribution Function (CDF)**: The cumulative distribution function $F_X(x)$ gives the probability that a continuous random variable $X$ takes a value less than or equal to $x$:
  $$
  F_X(x) = P(X \leq x) = \int_{-\infty}^{x} f_X(t) \, dt
  $$

## Conclusion

Continuous random variables are used to model situations where outcomes can take any value within a range. They are characterized by a probability density function that provides the density of probability over intervals. Understanding continuous random variables is essential for analyzing and interpreting data in various practical applications.