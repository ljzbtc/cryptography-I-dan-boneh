# Section1-1-Courese-Overview

## Course Objectives

- Learn how cryptographic primitives work
- Learn how to use cryptographic primitives correctly
- Learn how to reason about the security of constructions
- Be able to analyze the security of cryptographic systems and identify insecure ones

## Learning Recommendations

- Take notes while watching lectures
- Pause videos periodically to reflect on the material
- Answer pop-up questions in the videos

## Applications of Cryptography

1. Network Communication Security
   - HTTPS (SSL/TLS)
   - Wi-Fi (WPA2)
   - Mobile communication (GSM)
   - Bluetooth
2. File Encryption
3. Content Protection
   - DVD (CSS)
   - Blu-Ray (AACS)
4. User Authentication

## Basics of Secure Communication

- Goals: Prevent eavesdropping and tampering
- Protocol: TLS (SSL)
  1. Handshake protocol: Establish shared key
  2. Use shared key for secure communication

## Symmetric Encryption Systems

- Components: Encryption algorithm (E) and Decryption algorithm (D)
- Important: Algorithms are public, only the key is secret

### One-time Keys vs Many-time Keys

- One-time keys: Each key used to encrypt only one message
- Many-time keys: Require additional mechanisms to ensure security

## Important Reminders

1. Cryptography is not a solution to all security problems
2. Incorrect implementation can render cryptographic systems completely insecure
3. Don't invent or design cryptographic primitives yourself; use standardized ones
4. Avoid using proprietary encryption algorithms; prefer publicly reviewed standard algorithms

## Case Study

- WEP: Used as a negative example to show how not to use cryptography correctly
