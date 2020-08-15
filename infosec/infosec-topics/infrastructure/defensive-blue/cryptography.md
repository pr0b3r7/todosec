---
description: '"Secret writing" circa 1900 B.C., Egypt'
---

# Cryptography

We have a secret that we may or may not want to share. When employing a non-trusted medium to communicate, we protect the unencrypted data \(plaintext\) by encrypting it into ciphertext \(encrypted data\) with a cryptography scheme and a key that can be used to decrypt the data back into plaintext.

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

It is important to note that stream ciphers employ feedback mechanisms that result in the key constantly changing. 2 main stream ciphers:

**Self-Synchronizing stream ciphers** 

Each bit is calculated as a function of the previous n bits in the keystream.

The encryption process stays synchronized with the decryption process by the length of the n-bit keystream being processed. 

For this reason also, error propagation is a concern. Keystreams are generated independently of the message stream by employing the same keystream generation function by sender and receiver. 

Since they are periodic the keystream repeats eventually. 

**Alert:** If the "One-time Pad" or key used to generate the pseudorandom is not at least as long as the plaintext, perfect-secrecy.

Most common example in Software Development is **RC4 - Rivest Cipher 4.** Used in WEP/WPA as well as TLS. [RFC 7465](http://tools.ietf.org/html/rfc7465) forbids use of RC4 in TLS. 

**Block Ciphers**

These algorithms encrypt a fixed size of n-bits of data \(block\) at once. 256 bits of unencrypted data can be encrypted into 256 bits of ciphertext - Padding schemes can be employed to _fill in_ when the plaintext is smaller than the logical block size \(56 bits of plaintext would be encrypted in a 64 bits sized block\).

Common implementations are DES, 3DES, AES, IDEA and Blowfish

Its biggest drawback is the key distribution process that would need to be protected as well. 

Its main difference with Stream Ciphers is that Block Ciphers always encrypt plaintext to the same ciphertext

#### PKC - Public Key Cryptography

Asymmetric encryption that is commonly used for key exchange, non-repudiation and authentication

#### Hash Functions

Data is transformed mathematically in an irreversible manner, the result is a digital fingerprint. This application ensures integrity of the data.

### Trust Models

#### PGP

#### Kerberos

#### Public Key Certificates and Certification Authorities

### Cryptographic Algorithms applied

#### Password Protection

#### Diffie-Hellman Key Exchange

#### RSA Public Key Cryptography

#### DES, Compromising DES, and DES flavors

#### Pretty Good Privacy

#### IP Security \(IPsec\) Protocol

#### Secure Transactions with SSL and TLS

#### Elliptic Curve Cryptography \(ECC\)

#### Advanced Encryption Standard and Rijndael

#### Cisco's Stream Cipher

#### TrueCrypt

#### Encrypting File System \(EFS\)

#### RC4 minutiae

#### Challenge-Handshake Authentication Protocol \(CHAP\)

#### Encryption in eMail and S/MIME

#### Interesting Resources for deeper understanding:

{% embed url="https://www.cryptomuseum.com/crypto/list.htm" %}

[http://www.quadibloc.com/crypto/jscrypt.htm](http://www.quadibloc.com/crypto/jscrypt.htm)

