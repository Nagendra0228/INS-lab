# Playfair Cipher Implementation in Python
This repository contains an implementation of the Playfair cipher in Python. The Playfair cipher is a classical encryption technique that encrypts pairs of letters using a 5x5 matrix derived from a keyword.

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1SQ3Kc-VBKZz_eAbKvTQah0tZpydDsg-O?usp=sharing)

## How It Works
1.Create the Playfair Matrix:
  a.The 5x5 matrix is generated using a keyword.
  b.The alphabet (excluding 'J', which is merged with 'I') is used to fill the matrix.
  c.Duplicate letters are removed from the keyword.
2.Encrypting a Message:
  a.The plaintext is converted to uppercase, replacing 'J' with 'I'.
  b.Spaces are removed, and if the length is odd, 'X' is appended as padding.
  c.Pairs of letters are encrypted based on the Playfair cipher rules:
    i.If both letters are in the same row, shift right.
    ii.If both letters are in the same column, shift down.
    iii.Otherwise, swap their columns within the rectangle they form.
3.Decrypting a Message:
  a.The ciphertext is processed in pairs using the reverse of the encryption rules.
  b.The original message is reconstructed.

## Code Implementation

### Functions:
  1.create_playfair_matrix(key): Generates the 5x5 Playfair cipher matrix.
  2.find_position(matrix, char): Finds the position of a character in the matrix.
  3.playfair_encrypt(plaintext, key): Encrypts a given plaintext.
  4.playfair_decrypt(ciphertext, key): Decrypts a given ciphertext.

## Example Usage:
```
# Define plaintext and key
plaintext = "HELLO"
key = "KEYWORD"

# Encrypt the plaintext
ciphertext = playfair_encrypt(plaintext, key)
print("Encrypted:", ciphertext)

# Decrypt the ciphertext
print("Decrypted:", playfair_decrypt(ciphertext, key))
```

## Output Example:
```
Encrypted: GATLMZ
Decrypted: HELXLO
```

## Requirements
1.Python 3.x

## How to Run
  1.Clone the repository:
  ```
  git clone https://github.com/Nagendra0228/playfair-cipher.git
  ```
  2.Navigate to the directory:
  ```
  cd playfair-cipher
  ```
  3.Run the script:
  ```
  python playfair_cipher.py
  ```
## License
This project is open-source and available under the MIT License.
