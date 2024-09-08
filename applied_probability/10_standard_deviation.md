## Standard Deviation in Applied Probability

### Definition

The **standard deviation** is a measure of the dispersion or spread of a set of values. It quantifies how much individual values in a data set differ from the mean of the data set. In probability and statistics, it is used to understand the variability or uncertainty associated with a random variable.

### Formal Definition

For a random variable $X$, the standard deviation is defined as the square root of the variance. If $\sigma^2$ denotes the variance of $X$, then the standard deviation $\sigma$ is given by:

$$ \sigma = \sqrt{\text{Var}(X)} $$

The variance of $X$ is defined as:

$$ \text{Var}(X) = E[(X - \mu)^2] $$

where $\mu = E[X]$ is the expected value or mean of $X$, and $E[\cdot]$ denotes the expectation operator.

### Calculation

1. **For a Discrete Random Variable**

   If $X$ is a discrete random variable with possible values $x_i$ and corresponding probabilities $p_i$, the variance is:

   $$ \text{Var}(X) = \sum_{i} p_i (x_i - \mu)^2 $$

   and the standard deviation is:

   $$ \sigma = \sqrt{\text{Var}(X)} $$

2. **For a Continuous Random Variable**

   If $X$ is a continuous random variable with probability density function $f(x)$, the variance is:

   $$ \text{Var}(X) = \int_{-\infty}^{\infty} (x - \mu)^2 f(x) \, dx $$

   and the standard deviation is:

   $$ \sigma = \sqrt{\text{Var}(X)} $$

### Examples

1. **Example 1: Rolling a Die**

   Consider a fair six-sided die. The random variable $X$ represents the outcome of a roll. The mean of $X$ is:

   $$ \mu = \frac{1 + 2 + 3 + 4 + 5 + 6}{6} = 3.5 $$

   The variance is calculated as:

   $$ \text{Var}(X) = \frac{1}{6} \left[(1 - 3.5)^2 + (2 - 3.5)^2 + (3 - 3.5)^2 + (4 - 3.5)^2 + (5 - 3.5)^2 + (6 - 3.5)^2 \right] = 2.9167 $$

   Therefore, the standard deviation is:

   $$ \sigma = \sqrt{2.9167} \approx 1.71 $$

2. **Example 2: Exam Scores**

   Suppose a class of students took an exam, and their scores are as follows: 70, 75, 80, 85, and 90. The mean score is:

   $$ \mu = \frac{70 + 75 + 80 + 85 + 90}{5} = 80 $$

   The variance is:

   $$ \text{Var}(X) = \frac{1}{5} \left[(70 - 80)^2 + (75 - 80)^2 + (80 - 80)^2 + (85 - 80)^2 + (90 - 80)^2 \right] = 62.5 $$

   Therefore, the standard deviation is:

   $$ \sigma = \sqrt{62.5} \approx 7.91 $$

3. **Example 3: Heights of Plants**

   Imagine you are studying the heights of plants in a garden. Suppose the heights in centimeters are: 30, 35, 40, 45, and 50. The mean height is:

   $$ \mu = \frac{30 + 35 + 40 + 45 + 50}{5} = 40 $$

   The variance is:

   $$ \text{Var}(X) = \frac{1}{5} \left[(30 - 40)^2 + (35 - 40)^2 + (40 - 40)^2 + (45 - 40)^2 + (50 - 40)^2 \right] = 62.5 $$

   Therefore, the standard deviation is:

   $$ \sigma = \sqrt{62.5} \approx 7.91 $$

### Conclusion

The standard deviation is a fundamental concept in applied probability that helps measure the spread of data or the variability of a random variable. It is widely used in statistical analysis to assess how much the values of a random variable deviate from the mean, which is crucial for understanding the uncertainty and making informed decisions based on data.
