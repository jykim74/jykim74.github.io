---
layout: post
title: "[BerEditor] How to use the Message Digest (Hash) function"
tags: [Hash, Digest, SHA1, SHA2, SHA3, SM3, SHAKE, BerEditor]
category: Software
---

**\[This feature is a licensed version feature\]**
If you need a license, you can obtain a 30-day license from the [\[Program Key Issuance\]](https://jykim74.mycafe24.com/user_reg.php) page.

For the hash function, refer to the link below if you are using OpenSSL to obtain it.
[\[OpenSSL\] Message Digest (Hash function) command](https://jykim74.tistory.com/141)
This time, let's obtain the hash, a function that creates a message digest, using [BerEditor](https://jykim74.tistory.com/36).

Run the BerEditor -> Cryptography -> Hash command.

## Calculating the hash value Order

<img src="https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdna%2FzBKHW%2FdJMcahW1hWC%2FAAAAAAAAAAAAAAAAAAAAALDYBRhRqmbi9NQFb31Yte8vjYdMVVJWJC9von_QOJMN%2Fimg.png%3Fcredential%3DyqXZFxpELC7KVnFOS48ylbz2pIh7yKj8%26expires%3D1764514799%26allow_ip%3D%26allow_referer%3D%26signature%3D2Q8X99UiolOewt2iE3CBZl7mJ1c%253D">

- 1 Enter the original message to be hashed. Enter
- 2 Select a hash algorithm
- 3 Execute the hash
- 4 Check the hash value in the result data

You can see the results screen like this.

In simple terms, when the hex value "11223344" is hashed with SHA256,
the hash value is "1A835ED8734F86355CA5B835D824D486993AABF1913CD3A011B7446C0514B7C9".

SHA256 results in a fixed-length 32-byte value.

## How to Split Hash Data and Enter

If the data is long or you want to split it into multiple entries,

use the Init, Update, and Final buttons.

- Init: Initialize the hash algorithm (run once)
- Update: Add data continuously (you can continuously change the input data)
- Final: Calculate the resulting hash value (run once)

You can also obtain the original message by splitting it like this.

Currently, BerEditor supports MD5, SHA1, SHA224, SHA256, SHA384, SHA512, SM3, SHA3, and SHAKE.

Note that SM3 is a Chinese-developed hash algorithm that produces a 32-byte result.
