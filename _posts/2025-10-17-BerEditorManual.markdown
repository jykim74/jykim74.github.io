---
layout: post
title: "[BerEditor] Generating ML-DSA Key Pairs and Digital Signatures"
tags: [DigitalSignature, PQC, BerEditor, ML-DSA, SLH-DSA, GenerateKeyPair]
category: Software
---

**\[This feature is a licensed version feature\]**
If you need a license, you can obtain a 30-day license from the [Program Key Issuance](https://jykim74.mycafe24.com/user_reg.php) page.
This feature can be tested with BerEditor version 2.5.0 or later.

Let's use the [BerEditor](https://jykim74.tistory.com/36) tool to generate a key pair using the PQC algorithm, Ml-DSA, and digitally sign it.

In this example, the execution environment is set to English. If the language is Korean, the message will be displayed in Korean.

## Generating an ML-DSA Key Pair

To create an electronic signature, you must first generate an ML-DSA key pair.
To generate a key pair, run BerEditor -> Service -> KeyPair Manager.

In KeyPair Manager, select "Generate KeyPair."

<img src="https://github.com/user-attachments/assets/571b1fb1-dde7-4573-b0a0-fd9c27959304">

In the KeyPair window, enter the key pair name and select ML DSA in the PQC section.

For KeyLength, select one of the three options (DSA\_44, DSA\_65, DSA\_87). It becomes

<img src="https://github.com/user-attachments/assets/cc50d925-46e9-4766-9090-c0ee002d3337">


Once the key pair is created, you can check it using the name you entered in the KeyPair Manager.

To view the key's detailed value, double-click the key.

<img src="https://github.com/user-attachments/assets/4c06acf6-d515-4e84-b325-f32cbee91a7d">


## Creating an ML-DSA Digital Signature

To create a digital signature using the generated ML-DSA key pair, select BerEditor->Cryptography->Sign/Verify.

In that window, click the Sign radio button (selected by default).

Note that for ML-DSA, there is no specific digest algorithm specified.

This is fixed within ML-DSA and is not specified.

After entering the input data and clicking the Sign button, select the previously generated ML-DSA key in the KeyPair Manager (double-click).

Selecting the key will display the signature value in the Signature field.

<img src="https://github.com/user-attachments/assets/ad4b59c4-c7c5-4117-8be7-68b3f4b6dea4">

## Verifying an ML-DSA Digital Signature

To verify a digital signature using the generated ML-DSA key pair, select BerEditor->Cryptography->Sign/Verify.

In that window, click the "Verify" radio button.

Enter the input data and signature values, then click the "Verify" button. The signature verification results will be displayed.

<img src="https://github.com/user-attachments/assets/5f411630-9eff-4190-9d59-6a805cfdb338">

## Conclusion

There seems to be a rapid demand for the current PQC algorithm and its modifications.
And OpenSSL 3.5 LTS includes ML-DSA, ML-KEM, and SLH-DSA.

Now, to familiarize yourself with PQC and verify its values, BerEditor supports it.

For reference, for SLH-DSA, select only SLH-DSA when selecting a key pair, and the key pair generation, digital signature, and verification are all the same.
