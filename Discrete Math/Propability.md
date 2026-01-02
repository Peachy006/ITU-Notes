
In a sample space s, the propability of a given event lets call it A will be 0 <= P(A) <= 1;


## Exercise:
##### Whats the propability of getting at least one 6 in 10 rolls?

First we find the opposite since it will be easier to compute, we know that not(A) is no 6 in 10 rolls
This means we find the chance of not getting a 6 but in 10 rolls, this will be 5/6¹⁰
this is 0.1615, so the chance of getting at least 1 six is 1 - 0.1615 = 0.8385

When we say $$P(A|B)$$
This means the amout of B is also in A, so this is assuming that B has already happened, what proportion of this is also in A, so essentially how much of B is:
Ergo, the union
$$A \cap B$$

This is calculated as:

$$
P(B|A) = \frac{P(A \cap B)}{P(A)}
$$

So if we ask:
##### Whats the propability of you rolling an odd number granted we roll a prime number

So essentially whats the propability of:

$$P(odd | prime)$$

We know the odd numbers on a dice are 1,3,5 and the prime numbers are 2,3,5
This means its 2/3 or 0.666 recurring

## Bayes Theorem:

$$P(B|A) = [P(A|B) × P(B)] / P(A)$$

General version:

$$P(Bₖ|A) = [P(A|Bₖ) × P(Bₖ)] / [P(A|B₁)P(B₁) + P(A|B₂)P(B₂) + ... + P(A|Bₙ)P(Bₙ)]$$

