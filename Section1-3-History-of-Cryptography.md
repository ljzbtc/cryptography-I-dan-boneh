# Cryptography Notes

## Basic Concepts

- Cryptography involves Alice and Bob trying to communicate securely while an attacker attempts to eavesdrop
- Uses encryption algorithm (E) and decryption algorithm (D)
- Symmetric ciphers: same key K used for encryption and decryption

## Historical Cipher Systems

### 1. Substitution Cipher

- Uses a substitution table to map each letter to another letter
- Example: A→C, B→W, C→N, etc.
- Key space size: 26! ≈ 2^88
- Easily broken: using letter frequency analysis

### 2. Caesar Cipher

- Fixed substitution cipher, shifting the alphabet 3 places to the right
- Not a true cipher as there's no key

### 3. Vigenère Cipher (16th century)

- Uses a keyword as the key (e.g., "CRYPTO")
- Keyword is repeated under the plaintext
- Encryption: add plaintext letter to key letter (mod 26)
- Breaking method:
  1. Assume key length
  2. Group ciphertext
  3. Analyze letter frequencies in each position within groups

### 4. Rotor Machines (19th century)

- Hebern machine: single rotor, rotates one notch per keypress
- Enigma machine: 3-5 rotors, initial setting as key
- Key space: 26^4 = 2^18 (for 4 rotors)
- Broken by British cryptographers during WWII

## Modern Cryptography

### 1. Data Encryption Standard (DES, 1974)

- Developed by IBM, became federal standard
- Key space: 2^56
- Encrypts 64 bits (8 characters) at a time
- Now considered insecure, shouldn't be used in new projects

### 2. Advanced Encryption Standard (AES)

- Uses 128-bit keys
- Modern secure encryption standard

### 3. Other Modern Ciphers

- Salsa20, etc.

Note: Cryptography has evolved from single-character encryption to block encryption, with increasing key space sizes and algorithm complexity.
