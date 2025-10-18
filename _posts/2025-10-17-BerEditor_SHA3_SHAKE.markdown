---
layout: post
title: "[BerEditor] Obtaining the SHA3 SHAKE digest"
tags: [PQC, SHA3, SHA3-224, SHA3-256, SHA3-384, SHA3-512, SHAKEE, SHAKE128, SHAKE256, XOF Length]
category: Software
---

Let's use BerEditor to calculate the SHA3 and SHAKE digests used in the PQC algorithm.
For SHA3, there are four methods: SHA3-224, SHA3-256, SHA3-384, and SHA3-512. Each produces a result length of 24, 32, 48, and 64 bytes, the same as SHA2.
For SHAKE, two methods are supported: SHAKE128 and SHAKE256.
To calculate the hash value in BerEditor, select BerEditor -> Cryptography -> Hash. This will bring up a window for calculating the hash value.


## Calculating SHA3-256


To obtain a SHA3-256 hash, enter the desired input value in the Input field, select SHA3-256 from the Algorithm section, and press the Digest button. The resulting value will be displayed in the Digest Value field. The example input value is 11223344 in hex, resulting in 32 bytes.

<img src="https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdna%2FbBXBng%2FdJMb9OAHbPA%2FAAAAAAAAAAAAAAAAAAAAAJE3JZxisocLBH4VGW2P8rfBU2UBfd7kbvLm1iKTP8m2%2Fimg.png%3Fcredential%3DyqXZFxpELC7KVnFOS48ylbz2pIh7yKj8%26expires%3D1761922799%26allow_ip%3D%26allow_referer%3D%26signature%3Dzct1gaVy%252BzZvYDkkQSItnn9Uykg%253D">

There are two ways to obtain the actual Digest value. The first is to use the Init Update Final method, which is a method for dividing the input value into multiple parts and entering it, and Digest is for obtaining the result for the current input value.

## Calculating SHAKE128

In the case of SHAKE128, you must enter the desired input value and select SHAKE128 from the algorithm. In the case of SHAKE, there is another option and you must specify the result length. In the example screen below, 64 bytes is specified.


<img src="https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdna%2Fb4KV3f%2FdJMb9WSXGoa%2FAAAAAAAAAAAAAAAAAAAAADFTSpZr8XtbD_MgtLrM5rGNbAatEbAUE5WTspjeslIV%2Fimg.png%3Fcredential%3DyqXZFxpELC7KVnFOS48ylbz2pIh7yKj8%26expires%3D1761922799%26allow_ip%3D%26allow_referer%3D%26signature%3D%252FoHz2L%252B8Ixtk640%252Floa4xbgjfgs%253D">

Both SHAKE128 and SHAKE256 require a Request Length value to be specified.


## Conclusion

The PQC algorithm uses SHA2, SHA3, and SHAKE as hash algorithms. SHA2 is currently the primary algorithm used even if it's not PQC. Here, we simply calculate SHA3 and SHAKE values. While this example only shows input values, you can also obtain a file hash by selecting the Input File tab.

Now, to familiarize yourself with PQC and verify its values, BerEditor supports it.

For reference, for SLH-DSA, select only SLH-DSA when selecting a key pair, and the key pair generation, digital signature, and verification are all the same.
