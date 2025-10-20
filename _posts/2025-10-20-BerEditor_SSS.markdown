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

<img src="https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdna%2Fbx1KnH%2FdJMb8XqO5vz%2FAAAAAAAAAAAAAAAAAAAAAMWHbSQp8SlGiWlVENpilQXRSDxJqhYyDT8ccprAd5ys%2Fimg.png%3Fcredential%3DyqXZFxpELC7KVnFOS48ylbz2pIh7yKj8%26expires%3D1761922799%26allow_ip%3D%26allow_referer%3D%26signature%3DcM8lO2qzIDm2muG0bk78MGZZc3o%253D" width="500" height="400">

Here are the example values:

- Total Count 5 Threshold 3 specified
- Prime number used: EB49EF05F639F07C36C7DF92903BF91F
- Key split value: 1122334455667788
- Result list

846FA728B2FC793315E247795E74960272F152F2D42DA6033417FCBAFC0E014F

56E36FBA82573B875C6309FF80770E1E86FC8D5DE6BC3AFF6F9C237752254B12

E46E9AE07ECC5F5BDFBADA7AB10DE5B6DEE31A7933C5504C5C116612FF7481A4

5737AFC3EDDD2A1833A986D6F757E332B35529CF2FCC1CE905AD439ECFAE3E89

2BD1D8A141A3247C48A18BAF94C0837DD8CB4ADD89655E36C2A1964A92DAB2C5

The Share value generated here is a coordinate value, so it is twice the length of the decimal value (X||Y coordinate value).

## Recovering the SSS Key

This time, let's insert 3 of the 5 split key values ​​into the secret value S.

1: Total number and Specify a threshold
2: Specify a prime number
3: Enter three split key values
4: Execute the merge
5: Result key Confirm

<img src="https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdna%2F3b6c4%2FdJMb9VzKTDY%2FAAAAAAAAAAAAAAAAAAAAAL_g88wk-x2jhSIxMMZ0nMMyOq6S_g4llfiZEnyLG6EX%2Fimg.png%3Fcredential%3DyqXZFxpELC7KVnFOS48ylbz2pIh7yKj8%26expires%3D1761922799%26allow_ip%3D%26allow_referer%3D%26signature%3DnxDD9AR%252FJNgV82uyeKyvvbnfMGc%253D" width="500" height="400">


- Total Count 5 Threshold 3 Specified
- Used decimals: EB49EF05F639F07C36C7DF92903BF91F
- Input key list of 3

846FA728B2FC793315E247795E74960272F152F2D42DA6033417FCBAFC0E014F

56E36FBA82573B875C6309FF80770E1E86FC8D5DE6BC3AFF6F9C237752254B12

5737AFC3EDDD2A1833A986D6F757E332B35529CF2FCC1CE905AD439ECFAE3E89
- Key result values: 1122334455667788

With these three inputs, we can obtain the original key value, 1122334455667788.

## Conclusion

Shamir Secret Sharing is a technology that can be used to decentralize encryption key management or to decentralize the storage of important passwords, thereby distributing the data to one or only one person.

