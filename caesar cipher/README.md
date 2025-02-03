[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1O997K8XjNRT0nbiq70ZWMgzUkuaZHJqn?usp=sharing)

Caesar Cipher Implementation
This project demonstrates the Caesar Cipher, a simple and widely known encryption technique. It works by shifting each letter in the plaintext forward or backward by a fixed number of positions (key) in the alphabet.

How It Works
Encryption: Each letter in the plaintext is replaced by the letter positioned k places ahead in the alphabet.
Decryption: The ciphertext is converted back to the original text by shifting each letter k places backward.
Example
If the key is 3 and the plaintext is "hello", the encryption process shifts each letter forward by three positions, resulting in "khoor". Decrypting "khoor" with the same key restores the original text "hello".

Key Features
✔ Supports lowercase English letters (a-z).
✔ Uses modular arithmetic to ensure cyclic shifting.
✔ Simple and efficient implementation.

This method is historically significant and serves as an introduction to cryptography. However, it is not secure for modern applications.
