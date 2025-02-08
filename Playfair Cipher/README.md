## Run in Google Colab
[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1SQ3Kc-VBKZz_eAbKvTQah0tZpydDsg-O?usp=sharing)

Playfair Cipher Implementation in Python
This Python script implements the Playfair Cipher, a classical encryption technique that enciphers pairs of letters based on a 5x5 matrix generated using a given key.

How It Works
Creating the Playfair Matrix

The key is processed to remove duplicate letters.
The English alphabet (excluding J) is appended to the key.
A 5x5 matrix is constructed from the key and remaining alphabet letters.
Encryption Process

The plaintext is converted to uppercase and spaces are removed.
If J appears, it is replaced with I.
If the length of plaintext is odd, an "X" is appended as padding.
The plaintext is split into letter pairs and encrypted using the Playfair Cipher rules:
Same row → Replace with letters to the right (wrap around if needed).
Same column → Replace with letters below (wrap around if needed).
Rectangle rule → Swap column positions of the letters.
Decryption Process

The ciphertext is processed using the same Playfair matrix.
Instead of shifting right/down, letters are shifted left/up.
The decrypted text is returned.

Playfair Cipher Implementation in Python
This Python script implements the Playfair Cipher, a classical encryption technique that enciphers pairs of letters based on a 5x5 matrix generated using a given key.

How It Works
Creating the Playfair Matrix

The key is processed to remove duplicate letters.
The English alphabet (excluding J) is appended to the key.
A 5x5 matrix is constructed from the key and remaining alphabet letters.
Encryption Process

The plaintext is converted to uppercase and spaces are removed.
If J appears, it is replaced with I.
If the length of plaintext is odd, an "X" is appended as padding.
The plaintext is split into letter pairs and encrypted using the Playfair Cipher rules:
Same row → Replace with letters to the right (wrap around if needed).
Same column → Replace with letters below (wrap around if needed).
Rectangle rule → Swap column positions of the letters.
Decryption Process

The ciphertext is processed using the same Playfair matrix.
Instead of shifting right/down, letters are shifted left/up.
The decrypted text is returned.
