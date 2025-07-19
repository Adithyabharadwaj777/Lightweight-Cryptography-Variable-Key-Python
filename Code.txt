import string
import random

# Generate a random key of given length using printable ASCII characters
def generate_key(length):
    return ''.join(random.choices(string.printable, k=length))

# Encrypt plaintext using the secret key
def encrypt(plaintext, key):
    encrypted = []
    for i in range(len(plaintext)):
        key_char = key[i % len(key)]
        encrypted_val = (ord(plaintext[i]) + ord(key_char)) % 256
        encrypted.append(chr(encrypted_val))
    return ''.join(encrypted)

# Decrypt ciphertext using the secret key
def decrypt(ciphertext, key):
    decrypted = []
    for i in range(len(ciphertext)):
        key_char = key[i % len(key)]
        decrypted_val = (ord(ciphertext[i]) - ord(key_char)) % 256
        decrypted.append(chr(decrypted_val))
    return ''.join(decrypted)

# Example usage
if __name__ == "__main__":
    plaintext = "This is a secret message."
    key_length = 10
    key = generate_key(key_length)
    print(f"Generated Key: {key}")

    encrypted_text = encrypt(plaintext, key)
    print(f"Encrypted Text: {encrypted_text}")

    decrypted_text = decrypt(encrypted_text, key)
    print(f"Decrypted Text: {decrypted_text}")
