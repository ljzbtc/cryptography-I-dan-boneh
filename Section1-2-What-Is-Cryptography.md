# Cryptography Notes

## 1. Core Content: Secure Communication

- Secure key establishment
- Secure communication using shared keys

## 2. Cryptographic Applications

### 2.1 Digital Signatures

- Different from physical signatures; each signature is unique
- Signature is a function of the document content

### 2.2 Anonymous Communication

- Using mixnets
- Bi-directional anonymous communication through a sequence of proxies

### 2.3 Anonymous Digital Cash

- Challenge: Maintaining anonymity while preventing double-spending
- Solution: Anonymous for single use, identity exposed for multiple uses

### 2.4 Secure Multi-party Computation

- Examples: Election systems and private auctions
- Computing function results without revealing individual inputs

### 2.5 "Magical" Applications

1. Privately Outsourcing Computation
   - Computing on encrypted data (e.g., encrypted search queries)
2. Zero-Knowledge Proofs
   - Proving knowledge without revealing information (e.g., proving knowledge of large number factorization)

## 3. Modern Cryptography Methodology

1. Specify the threat model
2. Propose a construction
3. Provide a security proof

## 4. Key Concepts

- Encryption provides both confidentiality and integrity
- Secure multi-party computation can replace trusted third parties
- Zero-knowledge proofs applicable to various "puzzles"

## 5. Important Notes

- Some applications (like encrypted search) are still theoretical
- Cryptography relies on problems believed to be hard (e.g., large number factorization)
