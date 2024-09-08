## Posteriors in Applied Statistics

In applied statistics, **posteriors** refer to the posterior probability distribution of a parameter given the observed data. This concept is central to Bayesian statistics, which provides a framework for updating our beliefs about a parameter in light of new evidence.

### Definition

The posterior distribution is the probability distribution that represents our updated beliefs about a parameter after considering the evidence provided by the data. It is derived from Bayes' Theorem, which relates the prior distribution, the likelihood of the observed data, and the posterior distribution.

Bayes' Theorem is expressed as:

$$
P(\theta | \text{data}) = \frac{P(\text{data} | \theta) \cdot P(\theta)}{P(\text{data})}
$$

where:
- $P(\theta | \text{data})$ is the **posterior** distribution of the parameter $\theta$ given the data.
- $P(\text{data} | \theta)$ is the **likelihood** of the observed data given the parameter $\theta$.
- $P(\theta)$ is the **prior** distribution of the parameter $\theta$.
- $P(\text{data})$ is the **marginal likelihood** or **evidence**, which normalizes the distribution.

### Example

Let's consider a practical example of estimating the probability of success in a series of Bernoulli trials, such as flipping a biased coin.

**Scenario**: Suppose you want to estimate the probability $p$ that a coin lands heads. You start with a prior belief that the probability of heads is uniformly distributed between 0 and 1 (a Beta(1,1) distribution).

1. **Prior Distribution**: Assume the prior is $P(p) \sim \text{Beta}(1,1)$, which is equivalent to a uniform distribution over $[0,1]$.

2. **Likelihood**: After flipping the coin 10 times and observing 7 heads, the likelihood of observing 7 heads given a probability $p$ is given by:

   $$
   P(\text{data} | p) = p^7 (1-p)^3
   $$

3. **Posterior Distribution**: Using Bayes' Theorem, the posterior distribution combines the prior and the likelihood:

   $$
   P(p | \text{data}) \propto p^7 (1-p)^3 \cdot \text{Beta}(1,1)
   $$

   Since the Beta distribution is a conjugate prior for the Bernoulli likelihood, the posterior distribution is also a Beta distribution:

   $$
   P(p | \text{data}) \sim \text{Beta}(8,4)
   $$

   Here, the parameters of the Beta distribution are updated to reflect the observed data.

### Interpretation

The posterior distribution $P(p | \text{data})$ represents our updated belief about the probability of heads after observing the data. The mean of this Beta(8,4) distribution provides an estimate of the probability of heads, and the spread (variance) reflects the uncertainty about this estimate.

In summary, the posterior distribution allows statisticians to make probabilistic statements about parameters after accounting for observed data, offering a powerful tool for statistical inference.
