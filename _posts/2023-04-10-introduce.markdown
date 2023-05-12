---
layout: post
title: "About BerEditor, CertMan and CryptokiMan"
tags: [BerEditor, CertMan, CryptokiMan]
category: Software
---
It's a program I made as a side project,
For those of you wondering what the tools are, here is a brief explanation.


[* What is BerEditor?]( https://jykim74.github.io/software/2023/04/13/BerEditor.html "BerEditor" ) 

BerEditor is a data viewer tool made with Basic Encoding Rule.
Of course, DER is a subset of BER, so you can see DER by default as well.
For reference, BER editing is also possible, but the test is still lacking.
  The file format supports all binary, PEM, and Hex encodings.

The name is BerEditor tool, but if you develop PKI related
There are various cryptographic functions such as key management, encryption/decryption, electronic signature, etc.
I made this function using OpenSSL API.
When developing encryption functions, this tool is used to create and compare data
This is for API testing.


[* What is CertMan?](https://jykim74.github.io/software/2023/04/13/CertMan.html "CertMan")

CertMan is a tool for creating X.509 certificates and CRLs of various profiles in relation to RSA and ECDSA.
Of course, key pair generation and request letter (CSR) generation are also supported.
This tool is for creating various certificates and CRLs and testing the generated certificates rather than actually using them as a service.
The focus of this tool is to support X.509 certificates and CRL profiles in various format settings.


[* What is CryptokiMan?](https://jykim74.github.io/software/2023/04/13/CryptokiMan.html "CryptokiMan")

When dealing with HSM devices, PKCS#11 standard API is provided.
It is a tool to manage the function of the corresponding HSM using this standard API.
If any device is provided with PKCS#11 library, you can use this tool to test encryption and digital signature, and to manage internal objects.
Of course, you can use it when creating a PKCS#11 library.


I made these tools because I needed these tools while developing PKI.
I hope that there might be someone who needs it.



