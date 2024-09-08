## Bayes' Rule in Applied Statistics

### Definition

**Bayes' Rule** (or Bayes' Theorem) is a fundamental principle in probability theory and statistics that describes how to update the probability of a hypothesis based on new evidence. It provides a way to revise existing predictions or theories in light of new data. Bayes' Rule relates the conditional probability of an event given another event to the inverse conditional probability.

### Formal Definition

Bayes' Rule is expressed mathematically as:

$$ P(A \mid B) = \frac{P(B \mid A) \cdot P(A)}{P(B)} $$

where:

- $P(A \mid B)$ is the **posterior probability**: the probability of event $A$ given that event $B$ has occurred.
- $P(B \mid A)$ is the **likelihood**: the probability of event $B$ given that event $A$ is true.
- $P(A)$ is the **prior probability**: the initial probability of event $A$ before considering event $B$.
- $P(B)$ is the **marginal likelihood** or **evidence**: the total probability of event $B$.

### Key Points

- **Posterior Probability**: This is the updated probability of an event after considering new evidence.
- **Prior Probability**: This is the initial assessment of the probability of an event before taking into account the new evidence.
- **Likelihood**: This measures how probable the new evidence is assuming the hypothesis is true.
- **Marginal Likelihood**: This normalizes the posterior probability to ensure that the probabilities sum to 1.

### Examples

1. **Example 1: Medical Diagnosis**

   Suppose you are testing for a rare disease that affects 1% of the population (prior probability $P(D) = 0.01$). The test for this disease is 99% accurate, meaning:
   
   - If a person has the disease, the test will correctly identify it 99% of the time ($P(T \mid D) = 0.99$).
   - If a person does not have the disease, the test will correctly identify this 95% of the time ($P(T \mid \neg D) = 0.95$).

   If a person tests positive, what is the probability that they actually have the disease?

   First, calculate $P(T)$, the total probability of testing positive:

   $$ P(T) = P(T \mid D) \cdot P(D) + P(T \mid \neg D) \cdot P(\neg D) $$
   $$ P(T) = (0.99 \cdot 0.01) + (0.05 \cdot 0.99) = 0.0099 + 0.0495 = 0.0594 $$

   Now, use Bayes' Rule to find the posterior probability $P(D \mid T)$:

   $$ P(D \mid T) = \frac{P(T \mid D) \cdot P(D)}{P(T)} $$
   $$ P(D \mid T) = \frac{0.99 \cdot 0.01}{0.0594} \approx 0.1667 $$

   Thus, even with a positive test result, there is about a 16.67% chance of actually having the disease.

2. **Example 2: Email Spam Filtering**

   Suppose you are building a spam filter and you know the following:

   - 20% of emails are spam ($P(S) = 0.20$).
   - If an email is spam, 70% of the time it contains the word "sale" ($P(W \mid S) = 0.70$).
   - If an email is not spam, 10% of the time it still contains the word "sale" ($P(W \mid \neg S) = 0.10$).

   If an email contains the word "sale," what is the probability that it is spam?

   First, calculate $P(W)$, the total probability of the word "sale":

   $$ P(W) = P(W \mid S) \cdot P(S) + P(W \mid \neg S) \cdot P(\neg S) $$
   $$ P(W) = (0.70 \cdot 0.20) + (0.10 \cdot 0.80) = 0.14 + 0.08 = 0.22 $$

   Now, use Bayes' Rule to find the posterior probability $P(S \mid W)$:

   $$ P(S \mid W) = \frac{P(W \mid S) \cdot P(S)}{P(W)} $$
   $$ P(S \mid W) = \frac{0.70 \cdot 0.20}{0.22} \approx 0.6364 $$

   Thus, if an email contains the word "sale," there is about a 63.64% chance that it is spam.

### Conclusion

Bayes' Rule is a powerful tool for updating probabilities based on new evidence. It has wide applications in various fields, including medical diagnosis, spam filtering, and decision-making under uncertainty. By integrating prior knowledge with new data, Bayes' Rule helps refine predictions and improve decision-making processes.
