---
layout: post
title: "[BerEditor] View ASN.1 BER DER encoded data"
tags: [ASN.1 ASN.1 view, BER, DER, BEREDITOR, DEREDITOR]
category: Software
---

[BerEditor](https://jykim74.github.io/software/2023/04/13/BerEditor.html) is a tool for decoding and viewing ASN.1 files, specifically those encoded using DER or BER.

In practice, BerEditor is primarily used to view X.509 certificates or CRL files, or to decode and view detailed values ​​of DER or BER-encoded data, such as private keys.

However, ASN.1 data exists in many formats, not just the ones listed.

You can open them using BerEditor.

The example screen below shows a certificate.

BerEditor offers four ways to view encoded ASN.1 files:

1. Open
2. Enter BER data
3. Drag and drop
4. Import from URI

You can open them in these three ways.

## Open (File -> Open)

First, select an existing DER or BER binary file, or open a file written in PEM format. Run BerEditor -> File -> Open menu (run step 1 in the image below)

<img src="https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdna%2Fbg1vYd%2FdJMcajUNGRj%2FAAAAAAAAAAAAAAAAAAAAAONGBVDre6WFUweJcCH1Se_DiyX2rZpFm6PYknzQTqUv%2Fimg.png%3Fcredential%3DyqXZFxpELC7KVnFOS48ylbz2pIh7yKj8%26expires%3D1761922799%26allow_ip%3D%26allow_referer%3D%26signature%3Dzn6D9rIQJPUnwRvYmvhlZD6rBls%253D">

## BER Data Input (Tools -> Data Input)

This method requires a string input value. You can input it directly in hex-encoded or Base64-encoded format.
Run BerEditor -> Tool -> Decode BER (Run #2 in the image above).

The following figure shows the input method for BER data. The example shows hex data.

<img src="https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdna%2FG6ovd%2FdJMcafkyVax%2FAAAAAAAAAAAAAAAAAAAAABmozTFbgzunL-3dVNqYUE1Jc70crN07glMslotpo5Lt%2Fimg.png%3Fcredential%3DyqXZFxpELC7KVnFOS48ylbz2pIh7yKj8%26expires%3D1761922799%26allow_ip%3D%26allow_referer%3D%26signature%3DXKCHvy2d%252BdxfUoNLUyix5lGLlc4%253D">

## Mouse drag and drop

DER BER You can also drag and drop binary or PEM files.

This is the screen when opening the following data.

## Import from URI Address (Tools -> Get URI Data)

This menu accesses and retrieves URI data directly online.

Run BerEditor -> Tool -> Get BER from URI.

For HTTP addresses, the body data is processed as binary using the GET method.

For LDAP addresses, the filter and data type are retrieved by accessing the LDAP address.

The image below shows the URI import screen.

<img src="https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdna%2FwI5eD%2FdJMcagw0pqd%2FAAAAAAAAAAAAAAAAAAAAAG0HJWA7oe0t8UOgX_YiZwMych1uixfdur-VUQ7tVksy%2Fimg.png%3Fcredential%3DyqXZFxpELC7KVnFOS48ylbz2pIh7yKj8%26expires%3D1761922799%26allow_ip%3D%26allow_referer%3D%26signature%3Dr34hiBlUSZp%252Fibx26d4xycYrNS8%253D">

## Viewing BER Data

When you open the data as shown below, it is divided into three parts. It displays the data in a separate format.

Data formats can vary, including PEM, Base64, and binary, and these formats are automatically recognized internally.

- 1: Display the BER data tree structure
- 2: Represent data as hex values ​​(supports four display modes)
- 3: Detailed values ​​for the selected portion of the BER tree Display

<img src="https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdna%2FcX7rzv%2FdJMcad1lQFt%2FAAAAAAAAAAAAAAAAAAAAADDBl71tP4qDWJhkHLrEL92DJJwMDyIZCIlnFRe3MCLf%2Fimg.png%3Fcredential%3DyqXZFxpELC7KVnFOS48ylbz2pIh7yKj8%26expires%3D1761922799%26allow_ip%3D%26allow_referer%3D%26signature%3DpdZqTS7BBOuOEik8xXH07ZYw9QQ%253D">

If you enter data like this, In the center of the right screen, you'll see four tabs.

- Hexadecimal: Displays hexadecimal values ​​in hexadecimal format.
- XML: Displays XML-formatted data.
- String: Displays the structure of a text-formatted structure.
- JSON: Displays data in JSON format.

## Conclusion

Actually, the basic usage is simple and not difficult.
In this way, you can retrieve ASN.1 data encoded in BER or DER format in about four ways.
