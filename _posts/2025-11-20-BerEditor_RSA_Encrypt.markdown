---
layout: post
title: "[BerEditor] RSA Public Key Encryption and Decryption"
tags: [RSA Encrypt, RSA Decrypt, BerEditor]
category: Software
---

**\[This feature is a licensed version feature\]**
Those who require a license can obtain a 30-day license from the [\[Program Key Issuance\]](https://jykim74.mycafe24.com/user_reg.php) page.

RSA, an asymmetric key algorithm, allows encryption using the other party's public key,
and the recipient can then decrypt the encrypted data using their private key to obtain the plaintext.

Note that ECDSA is an algorithm for digital signatures only and does not support public key encryption.

However, SM2, a Chinese algorithm, does support public key algorithms.

Here, we'll demonstrate public key encryption using the RSA algorithm.
In RSA encryption, the options are V15 and V21 padding.

Simply put, V15 typically uses random padding,

while V21 is a more secure padding scheme that applies OAEP.

## Encrypting an RSA Public Key

Click BerEditor -> Password -> Encrypt/Decrypt Public Key.

<img src="https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdna%2FAM8vP%2FdJMcadtBrJd%2FAAAAAAAAAAAAAAAAAAAAALhih_jzSEvz26lsfLvpTWdotDiEmuI2ZLRKjBMDNpup%2Fimg.png%3Fcredential%3DyqXZFxpELC7KVnFOS48ylbz2pIh7yKj8%26expires%3D1764514799%26allow_ip%3D%26allow_referer%3D%26signature%3DewErF87S2%252F79Nadpku96JdhXTwY%253D">

1. Select Encrypt.
2. Enter the source value to be encrypted. 3. Select a certificate or public key for encryption.
4. Select an encryption method (V15 or OAEP).
5. Execute encryption.
6. Obtain the encrypted result.

## Decrypt with RSA private key Below

<img src="https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdna%2FkxqGP%2FdJMcabvPFWH%2FAAAAAAAAAAAAAAAAAAAAABCYyoFYisx5xZzKb0ga6Ohr21obGUV63vEpK0M-i41s%2Fimg.png%3Fcredential%3DyqXZFxpELC7KVnFOS48ylbz2pIh7yKj8%26expires%3D1764514799%26allow_ip%3D%26allow_referer%3D%26signature%3DvgBqdSbSluL0ZardHF8ynXlmA9g%253D">

1. Select Decrypt
2. Enter the encrypted data
3. Private key for decryption Select File
4. Select Encryption Method (V15 or OAEP)
5. Run Decryption
6. Table of Decrypted Original Values

Note: To send the encrypted value as an input value after encryption, press the ⬆ button.
