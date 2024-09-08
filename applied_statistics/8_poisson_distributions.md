## Poisson Distributions in Applied Statistics

A **Poisson distribution** is a discrete probability distribution that expresses the probability of a given number of events occurring in a fixed interval of time or space, given that these events happen with a known constant mean rate and independently of the time since the last event. It is named after the French mathematician Siméon Denis Poisson.

### Definition

A Poisson distribution is characterized by a single parameter $\lambda$ (lambda), which represents the average rate or mean number of events in the interval. The probability mass function (PMF) of a Poisson random variable $X$ is given by:

$$
P(X = k) = \frac{\lambda^k e^{-\lambda}}{k!}
$$

where:
- $k$ is the number of events (a non-negative integer: $k = 0, 1, 2, \ldots$).
- $\lambda$ is the average rate or mean number of events in the interval.
- $e$ is the base of the natural logarithm (approximately 2.71828).

### Properties

1. **Mean**: The mean or expected value of a Poisson random variable $X$ is:
   $$
   E[X] = \lambda
   $$

2. **Variance**: The variance of a Poisson random variable $X$ is:
   $$
   \text{Var}(X) = \lambda
   $$

### Examples

1. **Call Center**:
   - Suppose a call center receives an average of 5 calls per hour. The number of calls per hour can be modeled using a Poisson distribution with $\lambda = 5$.
   - The probability of receiving exactly 3 calls in a given hour is:
     $$
     P(X = 3) = \frac{5^3 e^{-5}}{3!} \approx 0.1404
     $$

2. **Traffic Flow**:
   - Imagine that a busy intersection experiences an average of 10 cars passing through it every 15 minutes. The number of cars passing through in a 15-minute interval can be modeled using a Poisson distribution with $\lambda = 10$.
   - The probability of observing exactly 7 cars in this interval is:
     $$
     P(X = 7) = \frac{10^7 e^{-10}}{7!} \approx 0.0900
     $$

### Applications

Poisson distributions are commonly used in various fields, including:
- **Queueing Theory**: Modeling the number of customers arriving at a service point.
- **Biology**: Estimating the number of mutations occurring in a fixed region of DNA.
- **Epidemiology**: Modeling the occurrence of rare diseases or events.

### Conclusion

The Poisson distribution is a powerful tool for modeling the occurrence of events in fixed intervals of time or space when the events happen at a constant rate and independently of each other. Its properties make it useful for a wide range of applications in statistics and data analysis.

