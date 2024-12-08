# DESXEncryption

**DESXEncryption** is a pure Java implementation of the **DESX** encryption algorithm, an enhancement of the **Data Encryption Standard (DES)**. DESX mitigates the vulnerabilities of DES by incorporating additional key-mixing steps to strengthen its resistance against brute-force and cryptanalysis attacks.

---

## Features

- **Strengthened DES**: Provides better security than standard DES.
- **Pure Java Implementation**: No external dependencies required.
- **Lightweight and Simple**: Designed for educational and small-scale cryptographic applications.
- **Key-Mixing Technique**: Incorporates additional key-mixing layers for enhanced security.

---

## Use Cases

- **Secure Data Encryption**: Encrypt sensitive information with better security than DES.
- **Legacy Systems**: Support systems that use DES-based algorithms but require enhanced protection.
- **Educational Purposes**: Learn about symmetric encryption and key-mixing techniques.

---

## Installation

Copy the `DESXEncryption` class into your Java project. No additional libraries are required.

---

## Usage

### Basic Example
```java
public class Main {
    public static void main(String[] args) {
        String plaintext = "Hello, DESX!";
        String key = "12345678"; 
        String keyXOR1 = "abcdefgh"; 
        String keyXOR2 = "ABCDEFGH"; 

        DESXEncryption desx = new DESXEncryption(key, keyXOR1, keyXOR2);

        String ciphertext = desx.encrypt(plaintext);
        System.out.println("Ciphertext: " + ciphertext);

        String decryptedText = desx.decrypt(ciphertext);
        System.out.println("Decrypted Text: " + decryptedText);
    }
}
