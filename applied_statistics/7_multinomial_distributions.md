## Multinomial Distributions in Applied Statistics

### Definition

The **Multinomial Distribution** is a generalization of the binomial distribution to cases where each trial can result in more than two outcomes. It models the probabilities of counts of each outcome in a series of experiments, where each experiment can result in one of several possible categories. The multinomial distribution is useful for scenarios where the outcome of each trial falls into one of several discrete categories.

### Formal Definition

Consider an experiment that can result in one of $k$ possible outcomes, with probabilities $p_1, p_2, \ldots, p_k$, where:

$$ p_1 + p_2 + \cdots + p_k = 1 $$

Let $n$ be the number of trials, and let $X_i$ be the number of times outcome $i$ occurs. The vector $(X_1, X_2, \ldots, X_k)$ follows a multinomial distribution if the joint probability mass function (PMF) is given by:

$$ P(X_1 = x_1, X_2 = x_2, \ldots, X_k = x_k) = \frac{n!}{x_1! x_2! \cdots x_k!} p_1^{x_1} p_2^{x_2} \cdots p_k^{x_k} $$

where $x_i$ are non-negative integers and $x_1 + x_2 + \cdots + x_k = n$. The term $\frac{n!}{x_1! x_2! \cdots x_k!}$ is the multinomial coefficient, representing the number of ways to arrange $x_1$ occurrences of outcome 1, $x_2$ occurrences of outcome 2, and so on, in $n$ trials.

### Key Points

- **Categories**: The multinomial distribution deals with outcomes that fall into multiple categories (more than two).
- **Multinomial Coefficient**: Represents the number of ways to distribute $n$ items into $k$ categories with specified counts for each category.
- **Probability Mass Function (PMF)**: Provides the probability of observing a specific count for each category in a fixed number of trials.

### Examples

1. **Example 1: Rolling a Die**

   Suppose you roll a fair six-sided die 10 times. Each roll has 6 possible outcomes, with each outcome having a probability of $\frac{1}{6}$. Let $X_i$ be the number of times face $i$ appears. The counts $(X_1, X_2, \ldots, X_6)$ follow a multinomial distribution with parameters $n = 10$ and $p_1 = p_2 = \cdots = p_6 = \frac{1}{6}$. The probability of observing a specific set of counts, say $(2, 3, 1, 0, 2, 2)$, is given by:

   $$ P(X_1 = 2, X_2 = 3, X_3 = 1, X_4 = 0, X_5 = 2, X_6 = 2) = \frac{10!}{2! 3! 1! 0! 2! 2!} \left(\frac{1}{6}\right)^{10} $$

2. **Example 2: Survey Responses**

   Suppose you conduct a survey with three possible responses: "Yes", "No", and "Maybe". If you survey 200 people, let $X_1$, $X_2$, and $X_3$ be the number of "Yes", "No", and "Maybe" responses, respectively. If the probabilities of "Yes", "No", and "Maybe" are 0.4, 0.3, and 0.3, respectively, then $(X_1, X_2, X_3)$ follows a multinomial distribution with parameters $n = 200$ and $p_1 = 0.4$, $p_2 = 0.3$, and $p_3 = 0.3$. The probability of observing, for example, 80 "Yes", 60 "No", and 60 "Maybe" responses is:

   $$ P(X_1 = 80, X_2 = 60, X_3 = 60) = \frac{200!}{80! 60! 60!} (0.4)^{80} (0.3)^{60} (0.3)^{60} $$

3. **Example 3: Voting Preferences**

   In an election with four candidates, suppose you survey 500 voters. Let $X_i$ be the number of votes for candidate $i$. If each candidate has an equal chance of receiving a vote, then $p_i = \frac{1}{4}$. The counts $(X_1, X_2, X_3, X_4)$ follow a multinomial distribution with parameters $n = 500$ and $p_1 = p_2 = p_3 = p_4 = \frac{1}{4}$. To find the probability of each candidate receiving exactly 125 votes, you would use:

   $$ P(X_1 = 125, X_2 = 125, X_3 = 125, X_4 = 125) = \frac{500!}{125! 125! 125! 125!} \left(\frac{1}{4}\right)^{500} $$

### Conclusion

The multinomial distribution extends the binomial distribution to cases with more than two possible outcomes per trial. It is used to model the probabilities of different counts for multiple categories over a fixed number of trials and is applicable in various fields such as survey analysis, genetics, and voting behavior.
