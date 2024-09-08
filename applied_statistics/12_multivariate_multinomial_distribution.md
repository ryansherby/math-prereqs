## Multivariate Multinomial Distribution in Applied Statistics

The **multivariate multinomial distribution** is a generalization of the multinomial distribution to the case where there are multiple groups of categorical outcomes, each with its own set of categories. It extends the multinomial distribution to situations where we are interested in the joint distribution of multiple sets of categorical counts.

### Definition

The multivariate multinomial distribution models the joint probabilities of multiple sets of categorical outcomes. Each set corresponds to a multinomial distribution with its own probability vector. It can be thought of as modeling the outcomes of several multinomial experiments simultaneously.

Consider $K$ independent multinomial experiments, where each experiment has $n_k$ trials and $m_k$ possible outcomes. Let $X_{k,j}$ denote the count of outcomes of category $j$ in the $k$-th experiment. The multivariate multinomial distribution is characterized by the following:

1. **Parameters**:
   - $n_k$: Number of trials in the $k$-th multinomial experiment.
   - $p_{k,j}$: Probability of outcome $j$ in the $k$-th multinomial experiment.
   - $X_{k,j}$: Number of times outcome $j$ occurs in the $k$-th multinomial experiment.

2. **Probability Mass Function (PMF)**:
   The joint probability mass function for observing counts $X_{k,j}$ for $k = 1, \ldots, K$ and $j = 1, \ldots, m_k$ is given by:

   $$
   P(X_{1,1}, \ldots, X_{1,m_1}, X_{2,1}, \ldots, X_{K,m_K}) = \prod_{k=1}^{K} \frac{n_k!}{X_{k,1}! \cdots X_{k,m_k}!} \prod_{j=1}^{m_k} p_{k,j}^{X_{k,j}}
   $$

   where $X_{k,1} + \cdots + X_{k,m_k} = n_k$ for each $k$.

### Example

Suppose we have two independent surveys with different sets of categorical responses:

1. **Survey 1**: Includes 3 categories (A, B, C) and 100 responses. Let $X_{1,A}$, $X_{1,B}$, and $X_{1,C}$ denote the counts of responses in categories A, B, and C, respectively.

2. **Survey 2**: Includes 2 categories (D, E) and 50 responses. Let $X_{2,D}$ and $X_{2,E}$ denote the counts of responses in categories D and E, respectively.

Assume the probabilities are:
- For Survey 1: $p_{1,A} = 0.4$, $p_{1,B} = 0.3$, $p_{1,C} = 0.3$.
- For Survey 2: $p_{2,D} = 0.6$, $p_{2,E} = 0.4$.

To find the joint probability of observing 40 responses in A, 30 in B, and 30 in C for Survey 1, and 30 responses in D and 20 in E for Survey 2, we use the PMF:

1. **Survey 1**:
   $$
   P(X_{1,A} = 40, X_{1,B} = 30, X_{1,C} = 30) = \frac{100!}{40! \cdot 30! \cdot 30!} \cdot (0.4)^{40} \cdot (0.3)^{30} \cdot (0.3)^{30}
   $$

2. **Survey 2**:
   $$
   P(X_{2,D} = 30, X_{2,E} = 20) = \frac{50!}{30! \cdot 20!} \cdot (0.6)^{30} \cdot (0.4)^{20}
   $$

The joint probability of these outcomes across both surveys is the product of the individual probabilities:

$$
P(X_{1,A}, X_{1,B}, X_{1,C}, X_{2,D}, X_{2,E}) = P(X_{1,A}, X_{1,B}, X_{1,C}) \cdot P(X_{2,D}, X_{2,E})
$$

### Applications

The multivariate multinomial distribution is useful in various fields, including:
- **Marketing**: Analyzing consumer preferences across multiple product categories.
- **Epidemiology**: Studying disease outcomes across different regions or demographic groups.
- **Social Sciences**: Examining survey responses with multiple sets of categories.

In summary, the multivariate multinomial distribution is a versatile tool for modeling and analyzing the joint distribution of multiple sets of categorical outcomes, providing insights into complex, multi-dimensional categorical data.
