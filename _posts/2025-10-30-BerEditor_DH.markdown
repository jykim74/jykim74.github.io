---
layout: post
title: "[BerEditor] DH (Diffie-Hellman) Key Agreement function"
tags: [DH, Diffie Hellman, Key Agreement, BerEditor]
category: Software
---

**\[This feature is a licensed version feature\]**
Those who require a license can obtain a 30-day license from the [\[Program Key Issuance\]](https://jykim74.mycafe24.com/user_reg.php) page.

Let's learn about the DH (Diffie-Hellman) algorithm, a key exchange algorithm.

## DH Algorithm Concept

The DH algorithm is a key agreement or key exchange algorithm that uses your private key and the other party's public key to obtain the same symmetric key.

In other words, rather than one party unilaterally determining the key value, both parties agree on the key value and share it.

## DH Algorithm Vulnerabilities

The DH algorithm is vulnerable to man-in-the-middle attacks.

To protect against man-in-the-middle attacks, it is used in conjunction with a certificate-based digital signature.

Also, excessively short parameters should not be used.

## Obtaining S (a symmetric key) using DH

Alice computes A $$ A = g^a mod p $$

Bob computes B $$ B = g^b mod p $$

Alice obtains S using B $$ S = B^a mod p $$

Bob obtains S using A $$ S = A^b mod p $$

This is the algorithm for Alice and Bob to obtain symmetric values ​​using the same S.

- Here, the values ​​g and p represent the DH parameter information.
- a : Alice's private key
- A : Alice's public key
- b : Bob's private key
- B : Bob's public key

## How to Use BerEditor

Select BerEditor -> Cryptography -> Key Agreement, then select the DH tab.

<img src="https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdna%2FSGY2a%2FdJMcai2FKxW%2FAAAAAAAAAAAAAAAAAAAAALbuirTRbnykk5xdot4v2VKBcfzN_40XOiDAOg3TFagP%2Fimg.png%3Fcredential%3DyqXZFxpELC7KVnFOS48ylbz2pIh7yKj8%26expires%3D1761922799%26allow_ip%3D%26allow_referer%3D%26signature%3DFzFS7FpBH3KOXMY62wZiY1mgIDk%253D">

- 1. First, create parameters (g and p values)
- 2. A Specify DH public and private key values
- 3. Specify B DH public and private key values
- 4. Specify the location for calculating the secret value between A and B
- 5. Execute the secret value calculation
- 6. Display the secret key value

Here, the activation of the public and private key sections varies depending on whether you select "calculate A" or "calculate B."

When calculating each value, the secret values ​​for A and B are the same.

Note that if you use the key generation function without generating a private key, both the private and public keys are generated.

For testing purposes, all values ​​for A and B are shown here.

In reality, these are the values ​​A needs to obtain A's private key using A's private key and B's public key.

Otherwise, B needs B's private key and A's public key to obtain B's secret key.

Both sides generate the same secret key, allowing key agreement.

This is a brief overview of the DH algorithm.

The DH algorithm is used in protocols such as TLS.
