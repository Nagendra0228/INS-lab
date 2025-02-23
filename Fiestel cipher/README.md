# Feistel Cipher - Python Implementation

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1mFK0OpH4W0G0swwKiJKwk_h2imdyOnaQ?usp=sharing)

## 📌 Introduction
This project implements a **single-round Feistel Cipher** in Python, demonstrating the fundamental concepts of **symmetric encryption**. The program converts text into binary, applies Feistel encryption using a key, and then decrypts it back to the original plaintext.

## 🚀 Features
✅ Converts **plaintext** into **binary format**  
✅ Performs **one round** of Feistel encryption  
✅ Uses **XOR operations** as the round function  
✅ Swaps halves as per Feistel structure  
✅ Converts **ciphertext back to plaintext** after decryption  

## 🛠 How It Works
### **1. Encryption Steps**
1. Convert plaintext to **8-bit binary representation**.
2. **Divide** the binary text into **left and right halves**.
3. Convert the key into **binary** and adjust its length.
4. Apply **XOR operation** between the right half and the key.
5. Swap the halves and apply XOR again.
6. The resulting binary string is the **ciphertext**.

### **2. Decryption Steps**
1. Split the ciphertext into **left and right halves**.
2. Reverse the Feistel function (undo XOR operations).
3. Swap halves back to their original position.
4. Convert the decrypted binary back to plaintext.

## 📜 Code Explanation
### **`to_binary(text)`**
Converts a string into its **8-bit binary representation**.

### **`from_binary(binary_str)`**
Converts an **8-bit binary string** back into plaintext.

### **`adjust_key(binary_key, length)`**
Ensures that the **key size matches** the right half of the text.

### **`feistel_encrypt(plain_text, key)`**
- Converts plaintext to **binary**.
- Splits binary text into **left and right halves**.
- Performs **XOR operations** using the key.
- Swaps halves to generate the **ciphertext**.

### **`feistel_decrypt(cipher_text, key)`**
- Splits ciphertext into **left and right halves**.
- Reverses the **XOR operations**.
- Swaps halves back to reconstruct the **original plaintext**.

## 🏃‍♂️ Running the Code
### **1️⃣ Clone the Repository**
```bash
git clone https://github.com/your-username/feistel-cipher.git
cd feistel-cipher
```
## Run the Program
```
python feistel_cipher.py
```
## Example Output
```
Enter a string: hi
Enter a key: hello
Plaintext (Binary): 0110100001101001
Cipher (Binary): 1100100101101000
Decrypted (Binary): 0110100001101001
Decrypted Text: hi
```
## 🔐 Feistel Cipher Concept
Feistel Ciphers are block ciphers that split the input into two halves and apply encryption rounds with a round function. This design is used in well-known ciphers like DES (Data Encryption Standard).
##📌 Next Steps
1.Implement multiple rounds for stronger encryption.
2.Add different key scheduling techniques.
3.Support larger block sizes.
##📄 License
This project is open-source under the MIT License.
