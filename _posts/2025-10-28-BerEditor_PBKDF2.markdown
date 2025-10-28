---
layout: post
title: "[BerEditor] How to use PBKDF2 (Password-Based Key Derivation Function)"
tags: [PBKDF2, PKCS#5, PBKDF, BerEditor]
category: Software
---

**\[This feature is a licensed version feature\]**
Those who require a license can obtain a 30-day license from the [\[Program Key Issuance\]](https://jykim74.mycafe24.com/user_reg.php) page.

Usually, block ciphers require the use of symmetric keys.

However, there are times when a password must be used to generate a key.

PBKDF is used to derive a key using a password.

For example, when using a certificate for internet banking, the user selects the certificate and enters a password.

The entered password is used to decrypt the certificate's private key.

Decrypting the encrypted private key is done using symmetric key encryption.

The key used is not directly derived from the password, but rather generated using PBKDF.

PBKDF stands for Password-Based Key Derivation Function, a key derivation function.

PBKDF1 and PBKDF2 are the two most widely known, and the technical standard for them is defined in [PKCS#5 (RFC8018)](https://www.rfc-editor.org/rfc/rfc8018).

In fact, PBKDF1 is being replaced by PBKDF2 due to its weak security.

The key extraction function in [BerEditor](https://jykim74.github.io/software/2023/04/13/BerEditor.html) covers PBKDF2.

## Key Derivation Process

```
DK = PBKDF2( PRF, Password, Salt, c, dkLen )

/* Each hLen-bit block Ti of the derived key DK is computed as follows (with + marking string concatenation): */
DK = T1 + T2 + ⋯ + Tdklen/hlen
Ti = F(Password, Salt, c, i)

/* Repeat c times. In other words, the more repetitions, the harder it becomes to find. */
F(Password, Salt, c, i) = U1 ^ U2 ^ ⋯ ^ Uc

U1 = PRF(Password, Salt + INT_32_BE(i))
U2 = PRF(Password, U1)
⋮
Uc = PRF(Password, Uc−1)
```

PRF: A pseudorandom function with two parameters (e.g., a keyed HMAC function).

Password: A master cipher used to derive a key.
Salt: A sequence of bits used to add complexity to the key.
c: Iteration count.
dkLen: The length of the key to be extracted.
DK: The generated derived key value.

This is how it's created.

## Generating a PBKDF2 Value

Let's create a simple example value.
In [BerEditor]([https://jykim74.tistory.com/36](https://jykim74.github.io/software/2023/04/13/BerEditor.html), open the Cryptography -> Key Management -> Key Derive tab and enter the following information.

- 1: Select PBKDF2 method
- 2: Specify the generated key length
- 3: Enter the password string
- 4: Enter the iteration counter
- 5: Specify the salt value
- 6: Specify the hash
- 7: Execute key derivation

The values ​​below are example input values.

PRF: HMAC-SHA256
Password: Hello
Salt: 11223344556677881122334455667788 (hex)
c: 1,024
Hash: SHA256
dkLen: 32 bytes

If you enter the input value and extract the key using [BerEditor]([https://jykim74.tistory.com/36](https://jykim74.github.io/software/2023/04/13/BerEditor.html), you get the following:

<img src="https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdna%2FwdWz4%2FdJMcafZaITi%2FAAAAAAAAAAAAAAAAAAAAABBplTtDjexTZPeDb7H7pXEHDnwcM2eUNujhz2oS_6l_%2Fimg.png%3Fcredential%3DyqXZFxpELC7KVnFOS48ylbz2pIh7yKj8%26expires%3D1761922799%26allow_ip%3D%26allow_referer%3D%26signature%3Dwa1tcd1Q1rZsnocqAyC%252BsFl4dwk%253D">

Extracted from here 523B536B7DBBE958E8F1FDD1F149CDD598B26917D325DC98CC6AC299FF4B8D47
This is the generated key value.

On the screen, the password is password, the additional value is salt, and the number of iterations is c.
The hash combo is the HMAC hash function used in the PRF.
The key length is dkLen.
