
# Detailed Summary of Discrete Probability and Related Concepts

## 1. Foundations of Discrete Probability

- Defined over a finite set U, typically the set of all N-bit binary strings: (0^1)^N
- A probability distribution P is a function from U to [0,1]
  - For each element x in U, 0 ≤ P(x) ≤ 1
  - The sum of P(x) over all x in U equals 1
- An event is a subset of U
  - Probability of an event A is the sum of P(x) for all x in A
  - 0 ≤ P(A) ≤ 1 for any event A
  - P(U) = 1 (the probability of the entire universe is 1)

## 2. Random Variables

- Formally, a function from U to some other set V
- Intuitively, a variable that takes values in V according to some distribution
- The random variable induces a probability distribution on V
- Example: Let U be the set of all possible outcomes when rolling two dice. A random variable X could be the sum of the numbers on the dice, taking values in V = {2, 3, ..., 12}

## 3. Independence

### For Events:

- Events A and B are independent if knowing A occurred provides no information about whether B occurred
- Formal definition: P(A and B) = P(A) * P(B)

### For Random Variables:

- Random variables X and Y are independent if knowing the value of X provides no information about the value of Y
- Formal definition: For all a and b, P(X=a and Y=b) = P(X=a) * P(Y=b)

### Example:

- Consider U as the set of 2-bit strings: {00, 01, 10, 11}
- Let X be the least significant bit and Y the most significant bit
- X and Y are independent because P(X=0 and Y=0) = 1/4 = P(X=0) * P(Y=0) = 1/2 * 1/2

## 4. Important Property of XOR

- XOR (exclusive or) is denoted by ⊕
- For bits: 0⊕0=0, 0⊕1=1, 1⊕0=1, 1⊕1=0
- For bit strings: XOR is applied bitwise

### Key Property:

- Let Y be a random variable with any distribution over (0^1)^n
- Let X be an independent, uniformly distributed random variable over (0^1)^n
- Then Z = X ⊕ Y is uniformly distributed, regardless of Y's distribution

### Proof Sketch (for 1-bit case):

- Let P(Y=0) = p0, P(Y=1) = p1
- P(X=0) = P(X=1) = 1/2 (uniform distribution)
- P(Z=0) = P(X⊕Y=0) = P(X=Y) = P(X=0)*P(Y=0) + P(X=1)*P(Y=1) = p0/2 + p1/2 = 1/2

This property makes XOR very useful in cryptography for masking data.

## 5. Birthday Paradox

- If we choose approximately sqrt(|U|) random elements from a set U, there's a good chance that two of them will be the same
- More precisely, if we choose about 1.2 * sqrt(|U|) elements, the probability of a collision is greater than 1/2

### Example:

- In a set of 2^128 elements (e.g., 128-bit strings)
- Sampling about 2^64 times is likely to produce a collision

### Classic Birthday Problem:

- In a room of 23 people, the probability that two share a birthday is about 50%
- This is surprising because 23 << 365 (number of days in a year)

### Convergence:

- The probability of a collision converges quickly to 1 as the number of samples increases beyond sqrt(|U|)
- For |U| ≈ 1 million:
  - 1200 samples: ~50% chance of collision
  - 2200 samples: ~90% chance of collision
  - 3000 samples: nearly 100% chance of collision

## 6. Applications in Cryptography

- XOR is widely used in many cryptographic algorithms for its uniform distribution property
- The Birthday Paradox is crucial in analyzing the security of cryptographic hash functions and other schemes
- Understanding these concepts is fundamental for designing secure cryptographic systems and for cryptanalysis
