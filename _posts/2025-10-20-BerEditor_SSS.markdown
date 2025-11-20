---
layout: post
title: "[BerEditor] About SSS (Shamir's Secret Sharing) Scheme"
tags: [sss, ssss, BerEditor, Shamir Secret Sharing, Shamir threshold scheme]
category: Software
---

**\[This feature is a licensed version feature\]**

If you need a license, you can obtain a 30-day license from the [Program Key Issuance](https://jykim74.mycafe24.com/user_reg.php) page.

Sharmir Secret Sharing is an algorithm for dividing and sharing secret data.
In other words, it is a secret sharing algorithm that distributes secret values ​​by partitioning them.

Even if an attacker steals some of the shared values, they cannot reconstruct the secret values ​​unless they obtain the required amount.

Sharmir's Secret Sharing Scheme is also known as Sharmir's Threshold Scheme.

## Basic Concepts

- The Shamir Secret Sharing Scheme is a threshold secret sharing algorithm proposed by Adi Shamir in 1979.
- It divides secret information S into N pieces and reconstructs S using K pieces (K is less than or equal to N).
- It requires K (threshold) shared keys to reconstruct S.

## How to Use

- Basically, a prime number is required when splitting or obtaining a key value (a number larger than the private key).
- Specify the number of splits and recovery points for the private key.

## Splitting an SSS Key

In [BerEditor](https://jykim74.github.io/software/2023/04/13/BerEditor.html), go to Cryptography -> Shamir Secret Sharing.

Here, let's create a value with a Share of 5 and a Threshold of 3.
This example creates 5 split values ​​and requires 3 values ​​to recover the original key.

1: Specify the total number and threshold.
2: Specify the prime number.
3: Enter the key value to be divided and execute the division.
4: Check the resulting Share value list.

Follow the order numbers shown in the image below. Here is the result.

<img src="https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdna%2FbrsNaj%2FdJMcadtBmiC%2FAAAAAAAAAAAAAAAAAAAAAC5_brxA4NaI9DhEbqKbBHfQk_UYISxMO_HWO_98Dmyl%2Fimg.png%3Fcredential%3DyqXZFxpELC7KVnFOS48ylbz2pIh7yKj8%26expires%3D1764514799%26allow_ip%3D%26allow_referer%3D%26signature%3DpmDLmqpFKO13E6aePjfm6ZCSe4Q%253D">

Here are the example values:

- Total Count 5 Threshold 3 specified
- Prime number used: CA009D7B164CB7ACB6BFAC76A39D9069
- Key split value: 1122334455667788
- Result list

054DC474FCB47254DCC54FA2CF71D3A65C

0493EDADBFBF68DF64BBE7715553F7DDED

0372A1A8C978F4E51207F54CE6C44FC9B4

02B3E10394F7631D916038E1FA6678FA1A

018DAB20A72466D1360DF2841996D5DEB6

The Share value generated here is a coordinate value, so it is twice the length of the decimal value (X||Y coordinate value).

## Recovering the SSS Key

This time, let's insert 3 of the 5 split key values ​​into the secret value S.

1: Total number and Specify a threshold
2: Specify a prime number
3: Enter three split key values
4: Execute the merge
5: Result key Confirm

<img src="https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdna%2FV8Bwc%2FdJMcaiBF0Hg%2FAAAAAAAAAAAAAAAAAAAAANKCLcgkAXTOIKZCST-IliLkhexIYhqjXIrdPf6-JiWa%2Fimg.png%3Fcredential%3DyqXZFxpELC7KVnFOS48ylbz2pIh7yKj8%26expires%3D1764514799%26allow_ip%3D%26allow_referer%3D%26signature%3DpLWufkmIpGBz8D7VUA6eiwaWSrs%253D">


- Total Count 5 Threshold 3 Specified
- Used decimals: CA009D7B164CB7ACB6BFAC76A39D9069
- Input key list of 3

054DC474FCB47254DCC54FA2CF71D3A65C

0372A1A8C978F4E51207F54CE6C44FC9B4

02B3E10394F7631D916038E1FA6678FA1A

- Key result values: 1122334455667788

With these three inputs, we can obtain the original key value, 1122334455667788.

## Conclusion

Shamir Secret Sharing is a technology that can be used to decentralize encryption key management or to decentralize the storage of important passwords, thereby distributing the data to one or only one person.

