---
layout: post
title: "[BerEditor] How to use MAC functions"
tags: [HMAC, CMAC, GMAC, MAC, Message Authentication Code, BerEditor]
category: Software
---

**\[This feature is a licensed version feature\]**
If you need a license, you can obtain a 30-day license from the [\[Program Key Issuance\]](https://jykim74.mycafe24.com/user_reg.php) page.

Let's use BerEditor to create a MAC function for authentication and forgery detection using encryption.

BerEditor supports the following three MACs:

1. HMAC (Hash-Based Message Authentication Code): A MAC created using a hash.
2. CMAC (Cipher-based Message Authentication Code): A MAC created using a block cipher.
3. GMAC (Galois Message Authentication Code): A MAC created using the GCM mode of a block cipher.

These three functions are supported.
To create a MAC function, select BerEditor->Crypto->Message Authentication Code

## Generate HMAC

First, let's create an HMAC value.
This example selects HMAC and uses SHA256 as the hash algorithm.

<img src="https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdna%2FkTnVT%2FdJMcafZhxau%2FAAAAAAAAAAAAAAAAAAAAAN8NRqrACrU9nXH5a1oSSbr8p1-VQ71SUkqMU3hN78dT%2Fimg.png%3Fcredential%3DyqXZFxpELC7KVnFOS48ylbz2pIh7yKj8%26expires%3D1764514799%26allow_ip%3D%26allow_referer%3D%26signature%3DhGUJeIclCt0d1FZEDrORYyYLw7A%253D">

1. Input value (Hex): 1122334455667788
2. Key (Hex): 1122334455667788 1122334455667788
3. Select Generate
4. Generate MAC value using SHA256 HMAC
5. HMAC (hex): 7B4F9C4CFD2FBCD7C1F89C6008942A0CD2CA09DC65060CAC5E36E5BC7D256470

You can obtain it like this.

You can verify it by selecting Verify here.

## Create CMAC

Let’s find CMAC, which is AES CBC mode.

<img src="https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdna%2FUckse%2FdJMcabP60RU%2FAAAAAAAAAAAAAAAAAAAAALE3oAR9dfxYMiwhyWEB3I5SZKc6cA1KXTtGEL2exchp%2Fimg.png%3Fcredential%3DyqXZFxpELC7KVnFOS48ylbz2pIh7yKj8%26expires%3D1764514799%26allow_ip%3D%26allow_referer%3D%26signature%3D5e9rD56q0GczwGNASfUE2qCZnFc%253D">

- Input Value (Hex): 1122334455667788
- Key (Hex): 1122334455667788 1122334455667788
- AES CMAC Generation
- CMAC (hex): F09EFF49A976F9BE70F5EC899F9E7466

## GMAC Generation

Calculate GMAC using the AES algorithm see

<img src="https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdna%2Fbv3ZaF%2FdJMcahQkxLw%2FAAAAAAAAAAAAAAAAAAAAABSRSrDkVW1OGmUYypvXZiS-DPPMAlxt-xhYkopQtmIp%2Fimg.png%3Fcredential%3DyqXZFxpELC7KVnFOS48ylbz2pIh7yKj8%26expires%3D1764514799%26allow_ip%3D%26allow_referer%3D%26signature%3DA0f6MAqJU6K0gEubPQEKM%252BRdL%252BU%253D">

- Input value (Hex) : 1122334455667788
- Key (Hex): 1122334455667788 1122334455667788
- IV (Hex): 8899aabbccddeeff8899aabbccddeeff
- AES GMAC Generation
- GMAC (hex): FFBDC632ABA3AD9AB803D91630368499

I calculated these three MAC values ​​using BerEditor.
