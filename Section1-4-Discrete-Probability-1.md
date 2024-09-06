# Discrete Probability and Randomized Algorithms Notes

## 1. Fundamentals of Discrete Probability

### 1.1 Probability Distribution

- Function P defined on a finite set U
- Assigns probability between 0 and 1 to each element in U
- Sum of all probabilities must equal 1

### 1.2 Common Probability Distributions

1. Uniform Distribution
   - Equal probability for each element: P(x) = 1/|U|
2. Point Distribution
   - Probability 1 at a single point x0, 0 elsewhere

### 1.3 Events

- Definition: Subset A of U
- Probability: P(A) = ∑(x∈A) P(x)

### 1.4 Union Bound

- P(A1 ∪ A2) ≤ P(A1) + P(A2)
- Equality holds when A1 and A2 are disjoint

## 2. Random Variables

### 2.1 Definition

- Function from U to a set V
- Induces a probability distribution on V

### 2.2 Uniform Random Variable

- Denoted as R ←R U
- For all a∈U, P(R=a) = 1/|U|

## 3. Randomized Algorithms

### 3.1 Characteristics

- Input: Message M and implicit random string R
- R is resampled each time the algorithm runs
- May produce different outputs for the same input

### 3.2 Output

- Defines a probability distribution over the set of possible outputs
- May yield different results each run

### 3.3 Example

- Encryption algorithm: Encrypts message M using random string R
- Output: Distribution of all possible encryptions of M

## 4. Key Concepts

- Modern cryptography is built on rigorous mathematical proofs
- Discrete probability is a crucial tool for describing cryptographic security
- Randomization plays a key role in cryptographic algorithms

Note: These concepts provide the foundation for understanding security analysis and randomization techniques in modern cryptography.
