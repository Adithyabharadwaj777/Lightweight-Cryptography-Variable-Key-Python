#  Lightweight Cryptography Using Variable-Length Keys

This project demonstrates a **lightweight symmetric encryption algorithm** using **random variable-length ASCII keys**. The algorithm is implemented in Python and suitable for secure messaging, IoT, embedded systems, and educational cryptography learning.

---

##  Key Features

- Dynamically generated **random ASCII key**
- **Symmetric encryption**: Same key used for both encryption and decryption
- Uses **modular arithmetic** and ASCII manipulation
- **Linear time complexity** – efficient for real-time or constrained systems
- Easy to understand, making it ideal for educational purposes

---

##  How It Works

###  Encryption Process:
1. Generate a random ASCII key of user-defined length
2. Convert plaintext to ASCII values
3. Add corresponding key character ASCII (cyclically)
4. Use modulo 256 to keep values in ASCII range
5. Convert result back to characters to form ciphertext

###  Decryption Process:
1. Convert ciphertext to ASCII
2. Subtract corresponding key character ASCII (cyclically)
3. Use modulo 256
4. Convert values back to characters to restore original text

---

##  Example

**Input:**  
Message: `hello`  
Key: `XZ`  
Encrypted: `×úùåò`  
Decrypted: `hello`

---

##  Applications
1) Secure Messaging
2) IoT/Embedded System Encryption
3) Cloud Data Security
4) Educational cryptography demos
5) Lightweight wireless encryption

---

##  How to Run

1. Clone this repo:
```bash
git clone https://github.com/yourusername/Lightweight-Cryptography-Variable-Key-Python
cd Lightweight-Cryptography-Variable-Key-Python

2. Run the script:

- bash
- Copy
- Edit
- python encrypt_decrypt.py

3. Enter the message and desired key length. The script will:
- Generate a random key
- Encrypt your message
- Then decrypt it and display the original message




