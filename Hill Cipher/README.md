## Hill Cipher Encryption and Decryption
[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1ePOop-W29ANubz623x-XR4niOzAPBKvF?usp=sharing)

# Overview
This repository contains a Python implementation of the Hill Cipher, a classical cryptographic algorithm for encrypting and decrypting text using matrix multiplication.

# Requirements
Python 3.x
NumPy library

#Installation
Ensure you have NumPy installed. You can install it using:
```
pip install numpy
```

# Usage
## Encryption
The script encrypts a given plaintext using a specified key matrix.
```
plaintext = "HELLO"
key_matrix = np.array([[6, 24, 1], [13, 16, 10], [20, 17, 15]])
encrypted_text = hill_cipher_encrypt(plaintext, key_matrix)
print("Encrypted:", encrypted_text)
```
## Decryption
The encrypted text can be decrypted using the same key matrix.
```
decrypted_text = hill_cipher_decrypt(encrypted_text, key_matrix)
print("Decrypted:", decrypted_text)
```
## Functions
mod_inverse(a, m)
Finds the modular inverse of a under modulo m using a brute-force approach.
hill_cipher_encrypt(plaintext, key_matrix)
Encrypts a given plaintext using the Hill Cipher encryption method.
hill_cipher_decrypt(ciphertext, key_matrix)
Decrypts a given ciphertext using the Hill Cipher decryption method.

## Example Execution
```
$ python hill_cipher.py
Encrypted: ZEBBXX
Decrypted: HELLOX
```
## Notes
The plaintext is converted to uppercase and padded with 'X' if needed.
The key matrix must be invertible under mod 26.

## License
This project is licensed under the MIT License.

