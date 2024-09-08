## Gaussian Distributions in Applied Statistics

A **Gaussian distribution**, also known as the **normal distribution**, is a continuous probability distribution that is symmetric about its mean, describing how the values of a variable are distributed. It is one of the most important distributions in statistics due to its properties and applications.

### Definition

The Gaussian distribution is defined by its mean ($\mu$) and standard deviation ($\sigma$). The probability density function (PDF) of a Gaussian distribution is given by:

$$
f(x) = \frac{1}{\sigma \sqrt{2 \pi}} \exp \left( -\frac{(x - \mu)^2}{2 \sigma^2} \right)
$$

where:
- $x$ is the variable.
- $\mu$ is the mean or expectation of the distribution.
- $\sigma$ is the standard deviation, which measures the spread of the distribution.

### Properties

1. **Mean**: The mean $\mu$ is the center of the distribution. It is also the point where the distribution is symmetric.

2. **Variance**: The variance $\sigma^2$ measures the spread of the distribution around the mean. The standard deviation $\sigma$ is the square root of the variance.

3. **Symmetry**: The Gaussian distribution is symmetric around the mean. The probability of values falling within a certain distance from the mean follows the empirical rule (68-95-99.7 rule).

4. **68-95-99.7 Rule**: Approximately 68% of the data falls within one standard deviation of the mean, 95% within two standard deviations, and 99.7% within three standard deviations.

### Example

Consider a scenario where the heights of adult men in a city are normally distributed with a mean of 70 inches and a standard deviation of 3 inches. We want to determine the probability that a randomly selected man is taller than 73 inches.

1. **Mean ($\mu$)**: 70 inches
2. **Standard Deviation ($\sigma$)**: 3 inches
3. **Height of Interest**: 73 inches

To find the probability, we first convert the height to a standard normal variable (z-score):

$$
z = \frac{x - \mu}{\sigma} = \frac{73 - 70}{3} = 1
$$

Using the standard normal distribution table, or a calculator, we find the probability of a z-score greater than 1. The cumulative probability up to $z = 1$ is approximately 0.8413. Thus, the probability of a man being taller than 73 inches is:

$$
P(X > 73) = 1 - P(Z \leq 1) = 1 - 0.8413 = 0.1587
$$

Thus, there is approximately a 15.87% chance that a randomly selected man is taller than 73 inches.

### Applications

Gaussian distributions are widely used in various fields including:
- **Finance**: Modeling stock returns and risk.
- **Natural Sciences**: Describing measurements and errors.
- **Engineering**: Quality control and signal processing.
- **Social Sciences**: Analyzing survey data and test scores.

In summary, the Gaussian distribution is a foundational concept in statistics, used to model and understand the distribution of continuous data around a central mean with a defined variance.
