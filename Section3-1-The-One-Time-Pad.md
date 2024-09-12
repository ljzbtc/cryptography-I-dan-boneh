

# Cryptography Lecture Summary

## 1. Definition of a Cipher

- A cipher consists of two algorithms:
  - Encryption (E)
  - Decryption (D)
- Defined over a triple:
  - Key space (K)
  - Message space (M)
  - Ciphertext space (C)
- E and D must be efficient algorithms
- Must satisfy consistency: For any message m and key k, `D(k,E(k,m)) = m`

## 2. One-Time Pad (OTP)

- Designed by Vernam in the early 20th century
- M = C = K = set of all n-bit binary strings
- Encryption: `c = k XOR m`
- Decryption: `m = k XOR c`
- Very fast, but key length equals message length, making it impractical

## 3. Shannon's Perfect Secrecy

- Definition: For any two equal-length messages m0 and m1, and any ciphertext c, `P(E(k,m0)=c) = P(E(k,m1)=c)`
- Implies no information about the plaintext can be gained from the ciphertext alone
- One-Time Pad achieves perfect secrecy
- Shannon proved: Any cipher with perfect secrecy must have a key space at least as large as the message space

## 4. Limitations of One-Time Pad

- Theoretically secure but difficult to use in practice
- Key distribution problem: If you can securely transmit a key as long as the message, you could just transmit the message itself
- Perfect secrecy is insufficient for ensuring the security of practical ciphers

## 5. Future Developments

- Need to explore other security definitions and practical cipher systems
- The idea behind the One-Time Pad remains valuable and can be used to design more practical systems

This lecture introduced fundamental concepts in cryptography and its early development, laying the groundwork for discussing more modern and practical cipher systems.

Would you like me to modify or expand on any part of this Markdown summary?
