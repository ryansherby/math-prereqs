## Bernoulli Distributions in Applied Statistics

A **Bernoulli distribution** is a discrete probability distribution that models a single experiment or trial with exactly two possible outcomes: success (usually denoted by 1) and failure (usually denoted by 0). It is named after the Swiss mathematician Jacob Bernoulli and is a fundamental distribution in probability theory and statistics.

### Definition

A Bernoulli distribution is characterized by a single parameter $p$, which represents the probability of success. The probability mass function (PMF) of a Bernoulli random variable $X$ is given by:

$$
P(X = x) = p^x (1 - p)^{1 - x}
$$

where:
- $x \in \{0, 1\}$ is the outcome of the trial.
- $p$ is the probability of success (i.e., $P(X = 1)$).
- $(1 - p)$ is the probability of failure (i.e., $P(X = 0)$).

### Properties

1. **Mean**: The mean or expected value of a Bernoulli random variable $X$ is:
   $$
   E[X] = p
   $$

2. **Variance**: The variance of a Bernoulli random variable $X$ is:
   $$
   \text{Var}(X) = p(1 - p)
   $$

### Examples

1. **Coin Toss**:
   - Consider a fair coin toss where heads is considered a success and tails is a failure. If $p$ is the probability of landing heads (e.g., $p = 0.5$ for a fair coin), then the outcome of the coin toss can be modeled using a Bernoulli distribution with $p = 0.5$.
   - In this case, the probability mass function is:
     $$
     P(X = x) = 0.5^x \cdot (1 - 0.5)^{1 - x} = 0.5^x \cdot 0.5^{1 - x} = 0.5
     $$

2. **Quality Control**:
   - Suppose a factory produces light bulbs and each bulb has a probability $p = 0.02$ of being defective. Here, the outcome of whether a specific bulb is defective (success) or not (failure) follows a Bernoulli distribution with parameter $p = 0.02$.
   - For a given bulb, the probability that it is defective is $0.02$, and the probability that it is not defective is $0.98$. 

### Applications

Bernoulli distributions are widely used in various fields, including:
- **Quality control**: Modeling whether a product meets quality standards.
- **Medical testing**: Determining whether a patient has a particular condition based on test results.
- **Marketing**: Assessing the probability of a customer responding to a promotional offer.

### Conclusion

The Bernoulli distribution is a fundamental concept in probability and statistics, representing binary outcomes in single trials. Its simplicity makes it a building block for more complex distributions, such as the binomial distribution, which models the number of successes in multiple Bernoulli trials.

