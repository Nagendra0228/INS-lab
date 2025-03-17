[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1mI2RU0cimBe0l-QMkvz5s2eNNbbFqazn?usp=sharing)

# Binary String Encryption with Key Generation

This project encrypts a user-provided string by converting it into binary, applying bitwise operations, and generating unique keys.

## 🔹 How It Works

1. **Convert to Binary:** The input string is converted into its binary representation.
2. **Remove Leading Bits:** The first bit of each 8-bit segment is removed.
3. **Split into Two Parts:** The resulting binary string is split into `left` and `right` halves.
4. **Bitwise Shift & Key Generation:** 
   - Each half undergoes bitwise shifts based on predefined values.
   - Random indices are removed to generate secure encryption keys.
5. **Output Keys:** A set of 8 unique encryption keys is generated.

## 🔹 Prerequisites

- Python 3.x
- `random` module (pre-installed in Python)

##🔹 Example Output
```
Enter a string: Hello
Key 1 =  11010011100101101100
Key 2 =  10100101101001011010
Key 3 =  11010100101101001010
Key 4 =  11010110010110100101
Key 5 =  10011010100101101001
Key 6 =  11010110010110100110
Key 7 =  11010010110100101101
Key 8 =  10101101001011010010

