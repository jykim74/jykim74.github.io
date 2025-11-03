---
layout: post
title: "[BerEditor] ECDH (Elliptic Curve Diffie-Hellman) algorithm"
tags: [ECDH, Key Agreement, BerEditor]
category: Software
---

**\[This feature is a licensed version feature\]**
Those who require a license can obtain a 30-day license from the [\[Program Key Issuance\]](https://jykim74.mycafe24.com/user_reg.php) page.

ECDH is a key exchange or key agreement algorithm, similar to the [DH](https://jykim74.tistory.com/163) algorithm.

This algorithm uses an ECC key pair to obtain a symmetric key between the user and the peer.

Compared to the DH algorithm, DH uses separate parameters,
and instead of parameter generation, you can simply select the domain parameters used in the ECC you wish to use.

ECDH uses the parameter curve in the ECC key pair.

In other words, ECDH can use the same key used in ECDSA.

## ECDH Algorithm Description

ECDH is created using the following formula: The mathematics of ECC itself is difficult, but the math needed to understand the concept of ECDH is simple.^^

$$( a \* G ) \* b = ( b \* G ) \* a$$
$$secret = ( a \* G ) = ( b \* G ) \* a$$

G : ECC elliptice curve

In this way, the secret value can be obtained by finding the same value for a and b.

1. Alice generates an ECC key pair: {alicePrivKey, alicePubKey = alicePrivKey \* G}
2. Bob generates an ECC key pair: {bobPrivKey, bobPubKey = bobPrivKey \* G}
3. Alice and Bob exchange public keys through a separate channel
4. Alice computes a shared key = bobPubKey \* alicePrivKey
5. Bob computes a shared key = alicePubKey \* bobPrivKey
6. Alice and Bob obtain the same shared key ( bobPubKey \* alicePrivKey == alicePubKey \* bobPrivKey )

## ECDH Key Exchange Value Get it

<img src="https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdna%2FNWy1V%2FdJMcagjvgMW%2FAAAAAAAAAAAAAAAAAAAAAIGRWPNTZIJGg7k-Y8va-AktNpAuTEOXoeBBk8Zyrgo-%2Fimg.png%3Fcredential%3DyqXZFxpELC7KVnFOS48ylbz2pIh7yKj8%26expires%3D1764514799%26allow_ip%3D%26allow_referer%3D%26signature%3D0W%252Fib6VvYiSIqjl78jlEGb9V5lQ%253D">

Then, ECDH Let's use [BerEditor](https://jykim74.github.io/software/2023/04/13/BerEditor.html) to find the values.

Launch BerEditor and select Cryptography->Key Agreement->ECDH tab.

1. Create ECC parameters
2. Enter A's private key (can be created using either Key Pair Generation or Private Key Generation)
3. Create B's public key (can be created using either Key Pair Generation or Public Key Generation)
4. Display the Y value in the generated Secret value
5. Select and execute Calculate A (Note: For B, only Calculate B must be selected)
6. Create A's secret key

If you execute the steps in this order, A's secret key and B's secret key will be the same.
In fact, A's secret key can be found with just A's private key and B's public key.
And B's secret key can be found with just B's private key and A's public key.

For reference, the functions of the buttons, regardless of the order, are as follows:
Public Key Check: Checks if the public key matches the previously generated private key.
Key Pair Check: Checks if the private and public key pairs match.
Key Pair Generation: Simultaneously generates private and public key values.

## Understanding ECDH and ECDHE in TLS

When using TLS, you'll encounter the terms ECDH and ECDHE in cipher suites.

ECDH actually exchanges keys using the server's ECDSA certificate key.

This means the same key is used for each connection.

(In fact, even if the client uses ECDH, it still generates a new ECDH key.)

Since using the same key on the server weakens security,

ECDHE requires the server to generate a new key pair each time.

This is how I easily implemented the ECDH function using BerEditor.
