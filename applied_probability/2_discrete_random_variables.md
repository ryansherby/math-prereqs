# Discrete Random Variables in Applied Probability

In applied probability, a **discrete random variable** is a fundamental concept used to model scenarios where outcomes are distinct and countable. Discrete random variables play a crucial role in probability theory, statistical analysis, and various practical applications.

## Definition

A **discrete random variable** is a variable that can take on a countable number of distinct values. Each value has an associated probability, and the sum of all probabilities for all possible values must equal 1.

- **Probability Mass Function (PMF)**: The probability mass function $P(X = x)$ defines the probability that a discrete random variable $X$ takes on the value $x$. It maps each possible value of $X$ to its probability.

- **Sample Space ($\Omega$)**: The set of all possible values that a discrete random variable can take. For a discrete random variable $X$, the sample space is $\{x_1, x_2, x_3, \ldots\}$.

## Examples

1. **Rolling a Fair Die**:
   - Let $X$ be the outcome of rolling a fair six-sided die.
   - Sample Space: $\{1, 2, 3, 4, 5, 6\}$
   - PMF: $P(X = x) = \frac{1}{6}$ for $x = 1, 2, 3, 4, 5, 6$.

2. **Number of Heads in Coin Tosses**:
   - Let $Y$ be the number of heads obtained when flipping a fair coin three times.
   - Sample Space: $\{0, 1, 2, 3\}$
   - PMF:
     - $P(Y = 0) = \frac{1}{8}$ (all tails)
     - $P(Y = 1) = \frac{3}{8}$ (one head, two tails)
     - $P(Y = 2) = \frac{3}{8}$ (two heads, one tail)
     - $P(Y = 3) = \frac{1}{8}$ (all heads)

3. **Number of Goals Scored in a Soccer Match**:
   - Let $Z$ be the number of goals scored by a soccer team in a match.
   - Sample Space: $\{0, 1, 2, 3, \ldots\}$ (potentially infinite, but practically limited)
   - PMF: Suppose the probability of scoring $k$ goals follows a Poisson distribution with parameter $\lambda$. The PMF is given by:
     $$
     P(Z = k) = \frac{\lambda^k e^{-\lambda}}{k!}
     $$
     where $\lambda$ is the average number of goals scored per match.

## Key Properties

- **Expectation (Mean)**: The expected value $E[X]$ of a discrete random variable $X$ is the sum of each possible value of $X$ multiplied by its probability:
  $$
  E[X] = \sum_{x \in \text{Sample Space}} x \cdot P(X = x)
  $$

- **Variance**: The variance $\text{Var}(X)$ of a discrete random variable $X$ measures the spread of its values around the mean. It is given by:
  $$
  \text{Var}(X) = E[(X - E[X])^2] = \sum_{x \in \text{Sample Space}} (x - E[X])^2 \cdot P(X = x)
  $$

## Conclusion

Discrete random variables are essential for modeling scenarios with countable outcomes. They are characterized by a probability mass function that assigns probabilities to each possible value. Understanding discrete random variables helps in calculating expected values, variances, and solving various probability problems.