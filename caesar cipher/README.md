# Caesar Cipher Implementation

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1O997K8XjNRT0nbiq70ZWMgzUkuaZHJqn?usp=sharing)



## Description
This script implements the Caesar Cipher for encryption and decryption. The Caesar Cipher is a simple substitution cipher where each letter in the plaintext is shifted a fixed number of places in the alphabet.

## Implementation
The function caesar_cipher takes three parameters:
1.text: The input string to be encrypted or decrypted.
2.shift: The number of positions each letter is shifted.
3.encrypt (default True): A boolean indicating whether to encrypt (True) or decrypt (False).

Code
```
# Function to perform Caesar Cipher encryption and decryption
def caesar_cipher(text, shift, encrypt=True):
    result = ""  # Initialize an empty string for the result

    # If decryption is required, reverse the shift
    if not encrypt:
        shift = -shift

    for char in text:
        # Check if the character is a letter (ignoring numbers and symbols)
        if char.isalpha():
            # Determine the ASCII base value (uppercase or lowercase)
            shift_base = ord('A') if char.isupper() else ord('a')

            # Shift the character within the 26-letter alphabet and append to result
            result += chr((ord(char) - shift_base + shift) % 26 + shift_base)
        else:
            # Keep non-alphabetic characters unchanged
            result += char

    return result  # Return the final encrypted or decrypted text

# Example usage:
text = "Hello, World!"  # Input text to be encrypted
shift = 3  # Shift value for encryption

# Encrypt the text
encrypted_text = caesar_cipher(text, shift, encrypt=True)

# Decrypt the text back to original form
decrypted_text = caesar_cipher(encrypted_text, shift, encrypt=False)

# Display results
print("Encrypted:", encrypted_text)  # Output encrypted text
print("Decrypted:", decrypted_text)  # Output decrypted text
```

## Example Output
```
Encrypted: Khoor, Zruog!
Decrypted: Hello, World!
```

## Usage Instructions
1.Modify the text variable to the desired input string.
2.Set the shift value to control how much letters shift.
3.Call caesar_cipher(text, shift, encrypt=True) to encrypt the text.
4.Call caesar_cipher(encrypted_text, shift, encrypt=False) to decrypt the text back.

## Notes
1.This implementation maintains case sensitivity.
2.Non-alphabetic characters (e.g., numbers, punctuation) remain unchanged.
3.The shift wraps around using the modulo operator to stay within the 26-letter alphabet.

## Applications
1.Basic encryption for learning purposes.
2.Simple obfuscation of text data.
3.Historical cryptographic studies.
