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

<img src="https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdna%2FrvtR5%2FdJMb9W6uCWR%2FAAAAAAAAAAAAAAAAAAAAAHb2UxFj3oCyUdB38qY8RXv4jFMFE-zEqRVZ7del4zHt%2Fimg.png%3Fcredential%3DyqXZFxpELC7KVnFOS48ylbz2pIh7yKj8%26expires%3D1761922799%26allow_ip%3D%26allow_referer%3D%26signature%3DhUO%252B67IBmavuO%252BsyMHw50k0uxY4%253D">

In the KeyPair window, enter the key pair name and select ML DSA in the PQC section.

For KeyLength, select one of the three options (DSA\_44, DSA\_65, DSA\_87). It becomes

<img src="https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdna%2Fqdeyi%2FdJMb9PTT0K4%2FAAAAAAAAAAAAAAAAAAAAAJRA_RsH7Uz2KZPUIiKoHAU_UTW5tpfibIStYu56XI7x%2Fimg.png%3Fcredential%3DyqXZFxpELC7KVnFOS48ylbz2pIh7yKj8%26expires%3D1761922799%26allow_ip%3D%26allow_referer%3D%26signature%3D%252FnJNwselnDtzZ4NHPaO2I9%252BQxiQ%253D">


Once the key pair is created, you can check it using the name you entered in the KeyPair Manager.

To view the key's detailed value, double-click the key.

<img src="https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdna%2Fewxg3Z%2FdJMb9OAGMNz%2FAAAAAAAAAAAAAAAAAAAAAP2mUw6n37wtFkegQ1Ti2ldZnl9PM-9j34T16vuHbErL%2Fimg.png%3Fcredential%3DyqXZFxpELC7KVnFOS48ylbz2pIh7yKj8%26expires%3D1761922799%26allow_ip%3D%26allow_referer%3D%26signature%3DGir%252BL3FPsSN29Rr4N6rnnEFGsA8%253D">


## Creating an ML-DSA Digital Signature

To create a digital signature using the generated ML-DSA key pair, select BerEditor->Cryptography->Sign/Verify.

In that window, click the Sign radio button (selected by default).

Note that for ML-DSA, there is no specific digest algorithm specified.

This is fixed within ML-DSA and is not specified.

After entering the input data and clicking the Sign button, select the previously generated ML-DSA key in the KeyPair Manager (double-click).

Selecting the key will display the signature value in the Signature field.

<img src="https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdna%2FbzgQX7%2FdJMb9jtRBBF%2FAAAAAAAAAAAAAAAAAAAAAI_AFpHBUCTd28sqJ10K72_eoiOheQlPe2AmWKCN21tz%2Fimg.png%3Fcredential%3DyqXZFxpELC7KVnFOS48ylbz2pIh7yKj8%26expires%3D1761922799%26allow_ip%3D%26allow_referer%3D%26signature%3DqNPLcy8uaEbTmPgcoXQk%252B%252Bb7df0%253D">

## Verifying an ML-DSA Digital Signature

To verify a digital signature using the generated ML-DSA key pair, select BerEditor->Cryptography->Sign/Verify.

In that window, click the "Verify" radio button.

Enter the input data and signature values, then click the "Verify" button. The signature verification results will be displayed.

<img src="https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdna%2FpN2EU%2FdJMb9bWTUlS%2FAAAAAAAAAAAAAAAAAAAAADUb3i_mdIv_MN4epRUhY5gc-xT9aKXFjr2oh66J7LBq%2Fimg.png%3Fcredential%3DyqXZFxpELC7KVnFOS48ylbz2pIh7yKj8%26expires%3D1761922799%26allow_ip%3D%26allow_referer%3D%26signature%3D96QVWAHBswbYkXW6B001C%252FKRdDI%253D">

## Conclusion

There seems to be a rapid demand for the current PQC algorithm and its modifications.
And OpenSSL 3.5 LTS includes ML-DSA, ML-KEM, and SLH-DSA.

Now, to familiarize yourself with PQC and verify its values, BerEditor supports it.

For reference, for SLH-DSA, select only SLH-DSA when selecting a key pair, and the key pair generation, digital signature, and verification are all the same.
