---
layout: post
title: "[BerEditor] How to use the KeyWrap feature"
tags: [KeyWrap, KeyUnwrap, RFC3394, BerEditor]
category: Software
---

**\[This feature is a licensed version feature\]**
Those who require a license can obtain a 30-day license from the [\[Program Key Issuance\]](https://jykim74.mycafe24.com/user_reg.php) page.

KeyWrap is a type of symmetric key cryptography algorithm designed to encrypt (encapsulate) a cryptographic key.

In other words, it is a [standard technology (RFC3394)](https://www.rfc-editor.org/rfc/rfc3394) that encrypts a key to protect it on a common device.

This feature is a standard method for encrypting keys.

RFC3394 specifies the AES Key Wrap Algorithm, which uses AES for internal encryption.

Note that other block ciphers can also be used, but they don't appear to be standardized yet.

There are two key wrap methods: KW and KWP, which differ in the presence or absence of padding for the source key.

Then, you can obtain the KeyWrap value by using the key encryption function in [BerEditor](https://jykim74.github.io/software/2023/04/13/BerEditor.html).
To access the key encryption function, select Encryption -> Key Management -> Key Encryption.

### KeyWrap Encryption

Encrypting the key value Let's try it.

<img src="https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdna%2FPTtCg%2FdJMcagDNZ1a%2FAAAAAAAAAAAAAAAAAAAAAPI2kWb0b5Ke46JSuCzEKpcQgv9Gea1iVnaIio2dvELA%2Fimg.png%3Fcredential%3DyqXZFxpELC7KVnFOS48ylbz2pIh7yKj8%26expires%3D1764514799%26allow_ip%3D%26allow_referer%3D%26signature%3D6MUENZc6X%252FI0nMf3zO4K0v6iZr0%253D">

- 1 First, select the key encryption method. : KW
  - * There are two methods, KW and KWP, and you can choose whether to use padding.
- 2 Enter the key value to be encrypted.
- 3 KEK stands for Key Encryption Key. Enter the key value used for encryption.
- 4 Select Encryption (KeyWrap).
- 5 Execute.
- 6 This is the resulting key value after KeyWrap.

### KeyUnwrap Decryption

Decrypts the encrypted key value. Let's try it.

<img src="https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdna%2FlBx42%2FdJMcac2ts48%2FAAAAAAAAAAAAAAAAAAAAAD6E_SmgePQ5v6eQ4HzLPydA27TbN4nXyPNLqelZa319%2Fimg.png%3Fcredential%3DyqXZFxpELC7KVnFOS48ylbz2pIh7yKj8%26expires%3D1764514799%26allow_ip%3D%26allow_referer%3D%26signature%3DB93h3EVBshKNjVtbfhLrrgXo9lQ%253D">


- 1 Select KW. Select the same option as when encrypting.
- 2 Enter the KeyWrapped encryption key.
- 3 Enter the same KEK value used for encryption.
- 4 Select Unwrap to decrypt.
- 5 Execute Run.
- 6 Displays the decrypted key value.

Enter the 24-byte KeyWrap generated during encryption as the input value.

Enter the same KEK value and click "Decrypt."

The resulting 16-byte key value will be displayed.

### Conclusion

Usually, keys are used during encryption/decryption. To safely store these keys, we used the standard KeyWrap/KeyUnwrap.

For reference, the internal key algorithm used is the AES algorithm.
