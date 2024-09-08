## Central Limit Theorem in Applied Probability

### Definition

The **Central Limit Theorem (CLT)** is a fundamental theorem in probability theory that describes the distribution of the sample mean of a large number of independent and identically distributed (i.i.d.) random variables. It states that, regardless of the original distribution of the random variables, the distribution of the sample mean will tend to be approximately normally distributed as the sample size becomes large.

### Formal Definition

Let $X_1, X_2, \ldots, X_n$ be a random sample of size $n$ from a population with mean $\mu$ and variance $\sigma^2$. The sample mean $\bar{X}_n$ is given by:

$$ \bar{X}_n = \frac{1}{n} \sum_{i=1}^{n} X_i $$

The Central Limit Theorem states that as $n$ approaches infinity, the distribution of the standardized sample mean approaches a standard normal distribution. Mathematically:

$$ \frac{\bar{X}_n - \mu}{\sigma / \sqrt{n}} \xrightarrow{d} N(0, 1) $$

where $N(0, 1)$ denotes the standard normal distribution with mean 0 and variance 1, and $\xrightarrow{d}$ denotes convergence in distribution.

### Key Points

- **Sample Size**: The theorem holds for sufficiently large sample sizes. In practice, a sample size of 30 or more is often considered large enough for the CLT to apply.
- **Independence and Identically Distributed**: The random variables must be independent and identically distributed (i.i.d.), though there are extensions of the theorem that relax these conditions.

### Examples

1. **Example 1: Dice Rolls**

   Suppose you roll a fair six-sided die 50 times and calculate the average outcome. Each roll is an i.i.d. random variable with mean $\mu = 3.5$ and variance $\sigma^2 = 2.9167$. According to the CLT, the distribution of the sample mean will be approximately normal with mean 3.5 and variance $\sigma^2 / 50$. Thus, the average of the 50 rolls will be close to 3.5, and the distribution of these averages will be approximately normal.

2. **Example 2: Survey of Heights**

   Imagine you conduct a survey of 100 adults and record their heights. Even if the distribution of heights in the population is not perfectly normal, the average height computed from your sample of 100 adults will be approximately normally distributed due to the CLT. This allows you to use normal distribution techniques to estimate confidence intervals and conduct hypothesis tests about the average height.

3. **Example 3: Stock Returns**

   Consider analyzing the average daily return of a stock over a period of 60 days. Each day's return is an i.i.d. random variable. According to the CLT, the distribution of the average daily return will approximate a normal distribution, even if the returns themselves do not follow a normal distribution. This property is useful for making statistical inferences and predictions about stock performance.

### Conclusion

The Central Limit Theorem is a powerful result in probability theory that explains why normal distributions are commonly encountered in practice. It provides a foundation for making inferences about population means based on sample data and underpins many statistical methods and hypothesis tests. By ensuring that the sample mean approximates a normal distribution, the CLT facilitates the analysis of data and the application of statistical techniques.
