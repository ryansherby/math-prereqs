# Marginal Distributions in Applied Probability

In applied probability, **marginal distributions** refer to the probability distributions of individual random variables derived from a joint distribution of multiple variables. They provide insights into the behavior of one random variable without considering the other variables.

## Definition

The **marginal distribution** of a random variable is obtained by summing or integrating the joint distribution over the values of the other random variables. It represents the distribution of a single random variable regardless of the values of the other variables in the joint distribution.

### Discrete Random Variables

For discrete random variables $X$ and $Y$, the marginal probability mass function (PMF) of $X$ is obtained by summing the joint PMF over all possible values of $Y$:

$$
P(X = x) = \sum_{y} P(X = x, Y = y)
$$

Similarly, the marginal PMF of $Y$ is obtained by summing the joint PMF over all possible values of $X$:

$$
P(Y = y) = \sum_{x} P(X = x, Y = y)
$$

### Continuous Random Variables

For continuous random variables $X$ and $Y$, the marginal probability density function (PDF) of $X$ is obtained by integrating the joint PDF over all possible values of $Y$:

$$
f_X(x) = \int_{-\infty}^{\infty} f_{X,Y}(x, y) \, dy
$$

Similarly, the marginal PDF of $Y$ is obtained by integrating the joint PDF over all possible values of $X$:

$$
f_Y(y) = \int_{-\infty}^{\infty} f_{X,Y}(x, y) \, dx
$$

## Examples

1. **Discrete Random Variables**:
   - Suppose $X$ and $Y$ represent the number of heads from flipping two fair coins. The joint PMF is:
     $$
     P(X = x, Y = y) = \frac{1}{4} \text{ for } x, y \in \{0, 1, 2\}
     $$
   - To find the marginal PMF of $X$:
     $$
     P(X = x) = \sum_{y} P(X = x, Y = y) = \frac{1}{4} \cdot 3 = \frac{3}{4} \text{ for } x \in \{0, 1, 2\}
     $$
   - To find the marginal PMF of $Y$, use the same summation.

2. **Continuous Random Variables**:
   - Let $X$ and $Y$ be random variables with a joint normal distribution. Suppose $X$ and $Y$ have the joint PDF:
     $$
     f_{X,Y}(x, y) = \frac{1}{2 \pi \sigma_X \sigma_Y \sqrt{1 - \rho^2}} \exp \left(-\frac{1}{2(1 - \rho^2)} \left[ \frac{(x - \mu_X)^2}{\sigma_X^2} - 2 \rho \frac{(x - \mu_X)(y - \mu_Y)}{\sigma_X \sigma_Y} + \frac{(y - \mu_Y)^2}{\sigma_Y^2} \right] \right)
     $$
   - The marginal PDF of $X$ is:
     $$
     f_X(x) = \int_{-\infty}^{\infty} f_{X,Y}(x, y) \, dy = \frac{1}{\sqrt{2 \pi \sigma_X^2}} \exp \left(-\frac{(x - \mu_X)^2}{2 \sigma_X^2} \right)
     $$
     which is a normal distribution with mean $\mu_X$ and variance $\sigma_X^2$.

3. **Application Example**:
   - Consider a bivariate distribution where $X$ and $Y$ represent the height and weight of individuals. If you have the joint PDF, you can find the marginal distributions of height and weight separately. For instance, if $f_{X,Y}(x, y)$ is known, integrating over weight $y$ will give the distribution of height $X$.

## Key Properties

- **Independence**: If $X$ and $Y$ are independent random variables, then the joint PDF is the product of the marginal PDFs:
  $$
  f_{X,Y}(x, y) = f_X(x) \cdot f_Y(y)
  $$
  And similarly for discrete random variables:
  $$
  P(X = x, Y = y) = P(X = x) \cdot P(Y = y)
  $$

- **Marginalization**: The process of obtaining marginal distributions from the joint distribution is known as marginalization. It simplifies the analysis of individual variables from a multivariate distribution.

## Conclusion

Marginal distributions provide valuable insights into the behavior of individual random variables within a joint distribution. By summing or integrating the joint distribution over the other variables, one can obtain the marginal distributions that reveal the probability characteristics of each variable independently.
