# Densities in Applied Probability

In applied probability, **densities** refer to the probability density functions (PDFs) associated with continuous random variables. Densities provide a way to describe the likelihood of a continuous random variable falling within a certain range. Understanding densities is crucial for analyzing and interpreting continuous probability distributions.

## Definition

A **probability density function (PDF)** is a function that describes the relative likelihood of a continuous random variable taking on a particular value. Unlike discrete probability distributions, which use probabilities for specific outcomes, continuous distributions use densities to describe the distribution of probability over an interval.

- **Probability Density Function (PDF)**: For a continuous random variable $X$, the PDF $f_X(x)$ is defined such that:
  - The PDF is non-negative: $f_X(x) \geq 0$ for all $x$.
  - The total area under the PDF over the entire range is equal to 1:
    $$
    \int_{-\infty}^{\infty} f_X(x) \, dx = 1
    $$

- **Probability Calculation**: The probability that $X$ falls within an interval $[a, b]$ is given by the integral of the PDF over that interval:
  $$
  P(a \leq X \leq b) = \int_a^b f_X(x) \, dx
  $$

## Examples

1. **Uniform Distribution**:
   - Let $X$ be a random variable uniformly distributed between $a$ and $b$.
   - PDF: 
     $$
     f_X(x) = \frac{1}{b - a} \text{ for } a \leq x \leq b
     $$
     The PDF is constant over the interval $[a, b]$, indicating equal likelihood across this range.

2. **Normal Distribution**:
   - Let $X$ be a random variable following a normal distribution with mean $\mu$ and standard deviation $\sigma$.
   - PDF:
     $$
     f_X(x) = \frac{1}{\sigma \sqrt{2 \pi}} \exp \left(-\frac{(x - \mu)^2}{2\sigma^2}\right)
     $$
     This bell-shaped curve describes the likelihood of $X$ taking on different values around the mean $\mu$.

3. **Exponential Distribution**:
   - Let $X$ be a random variable following an exponential distribution with rate parameter $\lambda$.
   - PDF:
     $$
     f_X(x) = \lambda e^{-\lambda x} \text{ for } x \geq 0
     $$
     This distribution describes the time between events in a Poisson process, where $\lambda$ represents the rate of occurrences.

## Key Properties

- **Normalization**: The integral of the PDF over the entire range must be 1, ensuring that the total probability is 1:
  $$
  \int_{-\infty}^{\infty} f_X(x) \, dx = 1
  $$

- **Non-Negativity**: The PDF is always non-negative:
  $$
  f_X(x) \geq 0 \text{ for all } x
  $$

- **Cumulative Distribution Function (CDF)**: The CDF $F_X(x)$ is the integral of the PDF from $-\infty$ to $x$:
  $$
  F_X(x) = \int_{-\infty}^x f_X(t) \, dt
  $$
  It represents the probability that the random variable $X$ is less than or equal to $x$.

## Conclusion

Densities, or probability density functions, are essential for describing continuous random variables in probability theory. They provide a way to compute probabilities over intervals and understand the distribution of values for continuous variables. By integrating the PDF, one can determine the probability of different outcomes and analyze the behavior of continuous distributions.