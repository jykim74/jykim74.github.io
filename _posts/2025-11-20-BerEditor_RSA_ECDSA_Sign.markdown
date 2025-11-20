---
layout: post
title: "[BerEditor] RSA ECDSA digital signature and verification"
tags: [Digital Signature, RSA, ECDSA, Verify, BerEditor]
category: Software
---

**\[This feature is a licensed version feature\]**
Those who require a license can obtain a 30-day license from the [\[Program Key Issuance\]](https://jykim74.mycafe24.com/user_reg.php) page.

Let's try digital signing and verification using the [BerEditor](https://jykim74.github.io/software/2023/04/13/BerEditor.html) tool.
To digitally sign with BerEditor, you first need the corresponding certificate and private key.

There are two things to consider when signing with RSA.

First, the hash algorithm for the original text to be used for the digital signature.

Secondly, there are two padding methods for digital signatures: the existing V15 method and the V21 method, also known as PSS (OAEP).

V15 is generally used for certificates,
and recently, the more secure V21 method is recommended.

For ECDSA, simply select the hash algorithm for digital signatures.

Now, let's try creating an RSA digital signature using BerEditor.

## Creating an RSA Digital Signature

Select BerEditor->Crypto->Sign/Verify.

The default selection is "Sign."

<img src="https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdna%2FwpaL0%2FdJMcabJmYL8%2FAAAAAAAAAAAAAAAAAAAAAMTQYQyE5czlFBQOzelYTyCFC5a1qtwNi1RYczleg6VT%2Fimg.png%3Fcredential%3DyqXZFxpELC7KVnFOS48ylbz2pIh7yKj8%26expires%3D1764514799%26allow_ip%3D%26allow_referer%3D%26signature%3Dk5kYtYNJJIRaCLCbiFZxX5sSRc0%253D">

1. Input Data (Hex): "1122334455667788"
2. Select the RSA private key file
3. Hash and Method: Select SHA256 and V15
4. Sign: Create a digital signature
5. Signature value

For RSA, you can select V15 and PSS for the Hash and Signature methods.

## RSA Digital Signature Verification

<img src="https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdna%2Fxe4UL%2FdJMcacBvzu2%2FAAAAAAAAAAAAAAAAAAAAAP9X2Ut39bwwGSG-3xXFqCWA4q3psKHbeCzUMhcaPhS1%2Fimg.png%3Fcredential%3DyqXZFxpELC7KVnFOS48ylbz2pIh7yKj8%26expires%3D1764514799%26allow_ip%3D%26allow_referer%3D%26signature%3DXRzqBH5%252Bh3BplA15eMiiCFcl3o4%253D">

1. Click the Verify radio button.
2. Enter the original text.
3. Select the signature verification certificate.
4. Select the signature hash and method.
5. Enter the signature value.
6. Run the signature verification.

Following the above steps, the signature value will appear on the screen.

## ECDSA Digital Signature

ECDSA uses the same method as RSA, but with an ECDSA private key.

<img src="https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdna%2FcM2xDZ%2FdJMcaiuUuk0%2FAAAAAAAAAAAAAAAAAAAAADJFTGhdUR8EOl-v-MyUd6otXUgLnvAt_WDh9WTTVNdK%2Fimg.png%3Fcredential%3DyqXZFxpELC7KVnFOS48ylbz2pIh7yKj8%26expires%3D1764514799%26allow_ip%3D%26allow_referer%3D%26signature%3DN1XoyMn4wHJfMO0wHiR8CL0Sqa0%253D">

1. Select Sign
2. Enter original text
3. Select electronic signature private key file
4. Electronic Select a Signature Hash
5. Execute the Signature
6. Display the Signature Value

For ECDSA, only specify the Hash Algorithm.

## ECDSA Digital Signature Verification

Using a public key or certificate for ECDSA uses the same method as RSA.

<img src="https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdna%2FdTP3Fo%2FdJMcacBvzDC%2FAAAAAAAAAAAAAAAAAAAAAHTjFum6KFH6TsP7oshY3gmuN450djmC0-qFgZaB-LRX%2Fimg.png%3Fcredential%3DyqXZFxpELC7KVnFOS48ylbz2pIh7yKj8%26expires%3D1764514799%26allow_ip%3D%26allow_referer%3D%26signature%3DQAldTDdAIWbuFsIMm40g7KsReso%253D">

1. Select Verify
2. Enter the original text
3. Select the digital signature verification certificate file
4. Select the digital signature hash
5. Enter the digital signature value
6. Run verification

## Additional feature description

- Key pair check: Checks whether the private and public keys are paired correctly.
- Init, Update, Final: Use these buttons to enter the original text multiple times during signing and verification.

(Note: Init and Final are performed only once, while Update is used to continuously input the original text.)
- V button: View certificate
- D button: View BER decoding for the certificate or private key
- T button: Verify the certificate or private key algorithm (Supported in Version 1.2.3 or later)
