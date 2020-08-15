---
description: '"Secret writing" circa 1900 B.C., Egypt'
---

# Cryptography

We have a secret that we may or may not want to share. When employing a non-trusted medium to communicate, we protect the unencrypted data \(plaintext\) by encrypting it with a cryptography scheme and a key that can be used to decrypt the data back into plaintext.

* **cryptography**: development/creation of mathematical algorithms used to encrypt/decrypt data.
* **cryptanalysis**: analyzing/breaking encryption schemes
* **cryptology**: broad study of secret creation, encompasses cryptography and cryptanalysis.

### "Features"

Cryptography provides methods to preserve the confidentiality \(privacy\) of the unaltered \(integrity\) secrets from unauthenticated \(authentication\) third parties \(adversaries\).

The sender and receiver perform a key exchange of crypto keys. Cryptography provides verification that the sender is who they claim to be \(non-repudiation\).

### Types of Algorithms

#### SKC - Secret Key Cryptography

A single key is used for encryption by the sender and decryption by the receiver. Hence the name, Symmetric encryption a single key is used for encryption/decryption - Most common in privacy/confidentiality applications. Two most common types:

**Stream Ciphers**

Encrypts 1 bit/byte of the unencrypted data at a time. A "stream" of pseudorandom bits \(that should never be reused to ensure secrecy\) are the key. 

**Alert:** If the "One-time Pad" or key used to generate the pseudorandom is not at least as long as the plaintext, perfect-secrecy.

Most common example in Software Development is **RC4 - Rivest Cipher 4.** Used in WEP/WPA as well as TLS. [RFC 7465](http://tools.ietf.org/html/rfc7465) forbids use of RC4 in TLS. 

**Block Ciphers**

Its biggest drawback is the key distribution process that would need to be protected as well.

#### PKC - Public Key Cryptography

Asymmetric encryption that is commonly used for key exchange, non-repudiation and authentication

#### Hash Functions

Data is transformed mathematically in an irreversible manner, the result is a digital fingerprint. This application ensures integrity of the data.

### Trust Models

### Cryptographic Algorithms applied



Interesting Resources for deeper understanding:

{% embed url="https://www.cryptomuseum.com/crypto/list.htm" %}

[http://www.quadibloc.com/crypto/jscrypt.htm](http://www.quadibloc.com/crypto/jscrypt.htm)

