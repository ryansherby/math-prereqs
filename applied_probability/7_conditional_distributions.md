## Conditional Distributions in Applied Probability

### Definition

A **conditional distribution** provides the probability distribution of a random variable given that another random variable takes on a specific value. In other words, it describes how the distribution of one variable is influenced by the value of another variable.

### Formal Definition

Let $X$ and $Y$ be two random variables. The **conditional distribution** of $Y$ given $X = x$ is the distribution of $Y$ when $X$ is known to be equal to $x$. This is denoted as $P(Y \mid X = x)$.

In terms of probability density functions (pdfs) for continuous variables, the conditional distribution is given by:

$$ f_{Y \mid X}(y \mid x) = \frac{f_{X, Y}(x, y)}{f_X(x)} $$

where $f_{X, Y}(x, y)$ is the joint pdf of $X$ and $Y$, and $f_X(x)$ is the marginal pdf of $X$.

For discrete variables, the conditional probability mass function (pmf) is given by:

$$ P(Y = y \mid X = x) = \frac{P(X = x, Y = y)}{P(X = x)} $$

where $P(X = x, Y = y)$ is the joint pmf of $X$ and $Y$, and $P(X = x)$ is the marginal pmf of $X$.

### Examples

1. **Example 1: Coin Tossing**

   Suppose we have two random variables:
   
   - $X$: the number of heads obtained in 3 coin tosses
   - $Y$: the number of heads obtained in the first 2 coin tosses

   To find the conditional distribution of $Y$ given $X = x$, we need to determine the distribution of $Y$ for a fixed value of $X$. If $X = 2$, then $Y$ could be 1 or 2. We can calculate the probabilities of these outcomes based on the binomial distribution.

2. **Example 2: Exam Scores**

   Suppose we have:
   
   - $X$: the score on a math test
   - $Y$: the score on a science test

   If we know that a student scored 80 on the math test (i.e., $X = 80$), the conditional distribution of the science test score $Y$ given $X = 80$ can be modeled if we have data indicating how science scores are distributed given math scores.

3. **Example 3: Weather and Sales**

   Let:
   
   - $X$: the temperature on a given day
   - $Y$: the number of ice cream cones sold

   The conditional distribution of $Y$ given $X = x$ describes how the number of ice cream cones sold changes with temperature. For example, if the temperature is 30°C, the distribution of ice cream sales might follow a particular pattern that can be analyzed to understand how sales are influenced by temperature.

### Conclusion

Conditional distributions are a crucial concept in applied probability as they allow us to understand and model how one variable affects another. They are used extensively in various fields such as statistics, economics, engineering, and data science to make informed decisions and predictions based on given conditions.
