# Vigenère Cipher Implementation

## Introduction
The Vigenère cipher is a method of encrypting alphabetic text by using a series of Caesar ciphers based on the letters of a keyword. It is a form of polyalphabetic substitution.

## Encryption and Decryption
This section provides the implementation of the Vigenère cipher in Python.

```python
  # Vigenère Cipher Implementation

  def vigenere_encrypt(plaintext, key):
    """Encrypts the plaintext using the Vigenère cipher."""
    
    key = key.upper()  # Convert key to uppercase for consistency
    ciphertext = ""  # Stores the encrypted text
    key_index = 0  # Tracks position in the key

    for char in plaintext.upper():  # Convert plaintext to uppercase and iterate
        if char.isalpha():  # Encrypt only alphabetic characters
            shift = ord(key[key_index]) - ord('A')  # Compute shift value from key
            ciphertext += chr((ord(char) - ord('A') + shift) % 26 + ord('A'))  # Apply shift and wrap around within A-Z
            key_index = (key_index + 1) % len(key)  # Move to the next letter in the key (cyclic)
        else:
            ciphertext += char  # Non-alphabetic characters remain unchanged

    return ciphertext  # Return the encrypted text


def vigenere_decrypt(ciphertext, key):
    """Decrypts the ciphertext using the Vigenère cipher."""
    
    key = key.upper()  # Convert key to uppercase for consistency
    plaintext = ""  # Stores the decrypted text
    key_index = 0  # Tracks position in the key

    for char in ciphertext.upper():  # Convert ciphertext to uppercase and iterate
        if char.isalpha():  # Decrypt only alphabetic characters
            shift = ord(key[key_index]) - ord('A')  # Compute shift value from key
            plaintext += chr((ord(char) - ord('A') - shift) % 26 + ord('A'))  # Reverse shift to get original character
            key_index = (key_index + 1) % len(key)  # Move to the next letter in the key (cyclic)
        else:
            plaintext += char  # Non-alphabetic characters remain unchanged

    return plaintext  # Return the decrypted text


# Example usage
plaintext = "HELLO"  # Input message
key = "KEY"  # Encryption key

# Encrypt the plaintext
encrypted_text = vigenere_encrypt(plaintext, key)
# Decrypt the ciphertext
decrypted_text = vigenere_decrypt(encrypted_text, key)

# Display results
print("Encrypted:", encrypted_text)  # Output encrypted text
print("Decrypted:", decrypted_text)  # Output decrypted text (should match original plaintext)
```
# Conclusion
The Vigenère cipher is a classical encryption technique that enhances security by using a keyword for multiple shifts. The Python implementation above demonstrates both encryption and decryption functionalities effectively.
