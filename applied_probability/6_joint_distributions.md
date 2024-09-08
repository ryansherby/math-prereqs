# Joint Distributions in Applied Probability

In applied probability, **joint distributions** describe the probability distribution of two or more random variables considered together. They provide a comprehensive view of the relationships and dependencies between random variables.

## Definition

A **joint distribution** describes the probability distribution of multiple random variables simultaneously. It provides the probability of different combinations of outcomes for the random variables.

### Joint Probability Mass Function (PMF)

For discrete random variables $X$ and $Y$, the joint probability mass function $P(X = x, Y = y)$ gives the probability that $X$ takes the value $x$ and $Y$ takes the value $y$ simultaneously. The joint PMF must satisfy:
$$
\sum_{x} \sum_{y} P(X = x, Y = y) = 1
$$
for all possible values of $x$ and $y$.

### Joint Probability Density Function (PDF)

For continuous random variables $X$ and $Y$, the joint probability density function $f_{X,Y}(x, y)$ describes the density of probability at a particular point $(x, y)$. The joint PDF must satisfy:
$$
\int_{-\infty}^{\infty} \int_{-\infty}^{\infty} f_{X,Y}(x, y) \, dx \, dy = 1
$$
The probability that $(X, Y)$ falls within a region $A$ is given by:
$$
P((X, Y) \in A) = \int \int_{A} f_{X,Y}(x, y) \, dx \, dy
$$

## Examples

1. **Discrete Random Variables**:
   - Suppose $X$ and $Y$ represent the number of heads obtained from flipping two fair coins.
   - The sample space is $(0, 1, 2)$ for both $X$ and $Y$, with probabilities:
     $$
     P(X = x, Y = y) = \frac{1}{4} \text{ for all } x, y \text{ (assuming independence)}
     $$
   - The joint PMF can be represented in a table showing the probability for each combination of $x$ and $y$.

2. **Continuous Random Variables**:
   - Let $X$ and $Y$ be two random variables with a joint normal distribution, where $X$ and $Y$ have means $\mu_X$ and $\mu_Y$, variances $\sigma_X^2$ and $\sigma_Y^2$, and correlation $\rho$.
   - The joint PDF is:
     $$
     f_{X,Y}(x, y) = \frac{1}{2 \pi \sigma_X \sigma_Y \sqrt{1 - \rho^2}} \exp \left(-\frac{1}{2(1 - \rho^2)} \left[ \frac{(x - \mu_X)^2}{\sigma_X^2} - 2 \rho \frac{(x - \mu_X)(y - \mu_Y)}{\sigma_X \sigma_Y} + \frac{(y - \mu_Y)^2}{\sigma_Y^2} \right] \right)
     $$

3. **Joint Distribution of a Sum and Difference**:
   - Let $X$ and $Y$ be independent random variables where $X$ follows a uniform distribution on $[0, 1]$ and $Y$ follows an exponential distribution with rate $\lambda$.
   - Define $Z = X + Y$ and $W = X - Y$. The joint distribution of $(Z, W)$ can be derived using transformations and the joint density of $X$ and $Y$.

## Key Properties

- **Marginal Distributions**: The marginal distribution of a single variable can be obtained by summing or integrating out the other variables from the joint distribution.
  - For discrete variables:
    $$
    P(X = x) = \sum_{y} P(X = x, Y = y)
    $$
  - For continuous variables:
    $$
    f_X(x) = \int_{-\infty}^{\infty} f_{X,Y}(x, y) \, dy
    $$

- **Conditional Distributions**: The conditional distribution of $X$ given $Y = y$ describes the distribution of $X$ when $Y$ is known to be $y$.
  - For discrete variables:
    $$
    P(X = x \mid Y = y) = \frac{P(X = x, Y = y)}{P(Y = y)}
    $$
  - For continuous variables:
    $$
    f_{X \mid Y}(x \mid y) = \frac{f_{X,Y}(x, y)}{f_Y(y)}
    $$

## Conclusion

Joint distributions provide a comprehensive view of the relationships between multiple random variables. By analyzing joint probability mass functions or density functions, one can gain insights into the dependencies and interactions between variables. Understanding joint distributions is crucial for modeling complex systems and performing multivariate statistical analyses.
