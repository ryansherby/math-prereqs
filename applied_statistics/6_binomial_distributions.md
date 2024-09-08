## Binomial Distributions in Applied Statistics

A **binomial distribution** is a discrete probability distribution that models the number of successes in a fixed number of independent Bernoulli trials, each with the same probability of success. It is used in scenarios where there are two possible outcomes for each trial: success or failure.

### Definition

A random variable $X$ follows a binomial distribution if it represents the number of successes in $n$ independent trials, where each trial has a success probability of $p$. The probability mass function (PMF) of a binomial distribution is given by:

$$
P(X = k) = \binom{n}{k} p^k (1-p)^{n-k}
$$

where:
- $n$ is the number of trials.
- $k$ is the number of successes.
- $p$ is the probability of success in a single trial.
- $\binom{n}{k}$ is the binomial coefficient, representing the number of ways to choose $k$ successes from $n$ trials, and is calculated as:

$$
\binom{n}{k} = \frac{n!}{k!(n-k)!}
$$

### Properties

1. **Mean**: The mean of a binomial distribution is:

   $$
   \mu = np
   $$

2. **Variance**: The variance of a binomial distribution is:

   $$
   \sigma^2 = np(1-p)
   $$

3. **Standard Deviation**: The standard deviation is:

   $$
   \sigma = \sqrt{np(1-p)}
   $$

### Example

Consider a scenario where a factory produces light bulbs, and each bulb has a 90% chance of passing a quality control test. We want to determine the probability of finding exactly 8 defective bulbs out of 10 tested.

1. **Number of Trials (n)**: 10 bulbs.
2. **Number of Successes (k)**: 8 defective bulbs.
3. **Probability of Success (p)**: 0.10 (since a defective bulb is a success in this context).

To find the probability of exactly 8 defective bulbs, use the binomial probability formula:

$$
P(X = 8) = \binom{10}{8} (0.10)^8 (1-0.10)^{10-8}
$$

First, calculate the binomial coefficient:

$$
\binom{10}{8} = \frac{10!}{8!2!} = 45
$$

Then, compute the probability:

$$
P(X = 8) = 45 \times (0.10)^8 \times (0.90)^2
$$

Perform the calculations:

$$
P(X = 8) \approx 45 \times 1.00 \times 10^{-8} \times 0.81 \approx 3.65 \times 10^{-8}
$$

The probability of finding exactly 8 defective bulbs out of 10 tested is approximately $3.65 \times 10^{-8}$.

### Applications

Binomial distributions are commonly used in quality control, medical research, and any situation involving a fixed number of trials with binary outcomes. They help model the likelihood of various numbers of successes in repeated experiments or trials.

In summary, the binomial distribution is a fundamental tool in statistics for modeling binary outcomes over a fixed number of trials, providing insights into probabilities and variability associated with success rates in various applications.
