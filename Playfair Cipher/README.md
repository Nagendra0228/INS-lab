## Run in Google Colab
[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1SQ3Kc-VBKZz_eAbKvTQah0tZpydDsg-O?usp=sharing)

Playfair Cipher Implementation in Python
How It Works:

Playfair Matrix:

The key is processed to remove duplicates.
A 5x5 matrix is formed using the key and remaining letters (excluding 'J').
Encryption:

Converts plaintext to uppercase, removes spaces, and replaces 'J' with 'I'.
If length is odd, 'X' is added as padding.
Letters are paired and encrypted using Playfair rules:
Same row: Shift right (wrap if needed).
Same column: Shift down (wrap if needed).
Rectangle rule: Swap column positions.
Decryption:

Reverse the encryption process (shift left/up instead).
This ensures secure encryption using a simple substitution technique.
