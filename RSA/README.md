[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1xj6WcN9EFYUNWVX2AY-qK5bCfWACV0Sl?usp=sharing)

# RSA Implementation in Python

This repository contains a simple implementation of the RSA encryption and decryption algorithm in Python. The script allows users to input two prime numbers (`p` and `q`) and a message (as an integer). It then generates public and private keys, encrypts the message, and decrypts it to verify the correctness of the algorithm.

## How It Works

1. **Calculate `n` and `phi(n)`**  
   - `n = p * q`  
   - `phi(n) = (p - 1) * (q - 1)`

2. **Find a Public Key `e`**  
   - `e` is chosen such that it is co-prime with `phi(n)`

3. **Find a Private Key `d`**  
   - `d` is the modular inverse of `e` modulo `phi(n)`

4. **Encrypt the Message (`msg`)**  
   - `c = (msg^e) % n`

5. **Decrypt the Encrypted Message (`c`)**  
   - `decrypted_msg = (c^d) % n`

## Usage

Run the script and enter two prime numbers and a message (integer):

```bash
python rsa.py
