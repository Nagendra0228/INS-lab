[![Open in Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1DgL3-ueBftGFHrVfHMts2YleHkOawvSl?usp=sharing)


# Diffie-Hellman Key Exchange in Python

This project demonstrates the **Diffie-Hellman Key Exchange (D-H)** algorithm, a cryptographic method used to securely exchange cryptographic keys over a public channel.

## 🚀 How It Works

1. **Public Parameters:**
   - A prime number `p` and its primitive root `g` are chosen.
   
2. **Private Keys:**
   - Each participant (A & B) selects a private key randomly.

3. **Public Keys:**
   - Each participant computes a public key using `g^private_key mod p`.

4. **Shared Secret Calculation:**
   - Each participant derives the shared secret using the other’s public key.

5. **Verification:**
   - Both participants arrive at the same shared secret.

## 🛠 Installation & Usage

1. Clone the repository:
   ```sh
   git clone https://github.com/yourusername/diffie-hellman.git
   cd diffie-hellman

