[![Open in Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1CuYHhilhSZwQIyeoiIcPONLRO1evz3qg?usp=sharing)


# **Elliptic Curve Cryptography (ECC) Key Exchange using Python**

## **Overview**
This project demonstrates **Elliptic Curve Diffie-Hellman (ECDH) key exchange** using the **BrainpoolP256r1** elliptic curve.  
It generates key pairs for a sender and a receiver, derives encryption keys, and displays the compressed public keys.

## **Technologies Used**
- **Python** (>= 3.6)
- **tinyec** (Tiny Elliptic Curve Cryptography Library)
- **secrets** (for secure random number generation)

## **Installation**
Ensure you have Python installed and install the required library:

```bash
pip install tinyec

