---
layout: post
title: "[BerEditor] DER BER data format check"
tags: [ASN.1 ASN.1 Format check, BER format, DER format, X509 format]
category: Software
---

**\[This feature is a licensed version feature\]**

If you need a license, you can obtain a 30-day license from the [Program Key Issuance](https://jykim74.mycafe24.com/user_reg.php) page.

ASN.1 data is stored by encoding files in DER or BER format. 
In fact, understanding the format of ASN.1 encoded data requires understanding the actual encoded data. 
However, this format itself is often unfamiliar, so even if you're not familiar with the format, we believe it's necessary to be able to identify it. 
Even if you know the format, it can be used to confirm the correct format when it's difficult to immediately identify it. 
While all format identification has its limitations, 
this feature allows you to identify the data format among key data.


## Check Format List

- Certificate: Certificate format created in X.509 format
- CRL: Certificate Revocation List format created in X.509 format
- CSR: Certificate issuance request format created in X.509 format when requesting certificate issuance
- PublicKey: Public key format containing public key information
- PrivateKey: Private key format containing private key information
- PrivateKeyInfo: PrivateKeyInfo format not encrypted in PKCS#8 format from a private key
- EncPrivateKey: Private key format encrypted in PKCS#8 format from a private key
- CMS: Cryptography Message Syntax, encrypted message syntax format
- PKCS7: PKCS7 format is identical to CMS format.

## Format Check Method

To perform this function, select the BerEditor -> Tool -> Check BER menu. The following screen will appear. It comes out

<img src="https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdna%2FMIwOn%2FdJMb9LYiAIH%2FAAAAAAAAAAAAAAAAAAAAAGxkCYXJuvDCGxY4GKlgepoKecaCso85EANsTWEVUY2n%2Fimg.png%3Fcredential%3DyqXZFxpELC7KVnFOS48ylbz2pIh7yKj8%26expires%3D1761922799%26allow_ip%3D%26allow_referer%3D%26signature%3DKIJPdOik%252FwuAlOJkMduLAsKXPKM%253D">

- 1: Specify the file to check or enter the value in the Source section. Enter.
- 2: Clicking the BER Type Check button will display a format message or error message.
- 3: After checking the data type, double-check the format.

Here, the "V" symbol indicates a detailed view, and the "D" symbol decodes the data.

The screen below shows the results of searching for a certificate file.

<img src="https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdna%2FbdwMHJ%2FdJMb81UiQic%2FAAAAAAAAAAAAAAAAAAAAAGGuGoX9XcTlPDV3SKS4Tp32MPJBuTMSPH9uVwUhfP8G%2Fimg.png%3Fcredential%3DyqXZFxpELC7KVnFOS48ylbz2pIh7yKj8%26expires%3D1761922799%26allow_ip%3D%26allow_referer%3D%26signature%3D3fIUAgidS7A6JMluxpJj8BA9rhw%253D">

- 1: Certificate format information
- 2: Result of clicking the V button
- 3: Result of clicking the D button

## Conclusion

Working with PKI-related technologies often involves handling various DER format data.
Then, necessary data is saved in files or other formats.

This function is useful when the stored data grows in size or becomes outdated and requires verification.
