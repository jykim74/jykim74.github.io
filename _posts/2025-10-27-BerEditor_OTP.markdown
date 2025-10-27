---
layout: post
title: "[BerEditor] Generate OTP (One Time Password)"
tags: [OneTimePassword, OTP, TOTP, BerEditor]
category: Software
---

**\[This feature is a licensed version feature\]**
If you need a license, you can obtain a 30-day license from the [\[Program Key Issuance\]](https://jykim74.mycafe24.com/user_reg.php) page.

Let's learn about OTP, which is commonly used for online banking or as an additional authentication feature.
OTP stands for One Time Password, a one-time password.



The feature provided by [BerEditor](https://jykim74.tistory.com/36) is Time-Based One Time Password.
This is a standard technology defined in [RFC 6238](https://www.rfc-editor.org/rfc/rfc6238).
In fact, one of the most important aspects of Time-Based OTP is the time.

In reality, the time on the OTP device is inaccurate.
Even if the OTP time error decreases, the server side that verifies the OTP value considers the difference between the forward and backward times.


The server then records the error corrections to ensure continued use.
However, if the error exceeds a certain amount of time, the OTP time must be reset.
The time set in BerEditor is localTime.

That is, it can be viewed as +9 hours from UTC time.
For example, if UTC time is 1970.01.01 00:00:01, the local time would be 1970.01.01 09:00:01.

## Executing the OTP

Let's use [BerEditor](https://jykim74.github.io/software/2023/04/13/BerEditor.html) to obtain the OTP value specified in RFC 6238.
In BerEditor, go to Password->Generate OTP. Let's do this.

<img src="https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdna%2FderHbX%2FdJMb9Xj3sad%2FAAAAAAAAAAAAAAAAAAAAAFa10TDEInqZ1ToE2tXeL9aR9Ce_vMlSiiNDA-6K2ndY%2Fimg.png%3Fcredential%3DyqXZFxpELC7KVnFOS48ylbz2pIh7yKj8%26expires%3D1761922799%26allow_ip%3D%26allow_referer%3D%26signature%3DZfK1g%252FwgIRnkCTBsyZaDkrBxfAM%253D">

- 1: Execution Time Setting
- 2: Set the hash used during generation
- 3: Set the time interval (seconds)
- 4: OTP generation number length
- 5: Set the OTP generation key
- 6: Execute OTP generation

## Example OTP result

- Input time: 2025-10-27 11:48:28
- Hash Mode: SHA256
- Time Interval: 60 (sec)

- OTP length: 6
- Key: 12345678901234567890 (Hex)

Result Screen

<img src="https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdna%2FmWBFF%2FdJMb89dJUFt%2FAAAAAAAAAAAAAAAAAAAAAEFyuXL1vgWK3bf6XR1bqhGWeU4FB_FJ2Alkfanm3-Kf%2Fimg.png%3Fcredential%3DyqXZFxpELC7KVnFOS48ylbz2pIh7yKj8%26expires%3D1761922799%26allow_ip%3D%26allow_referer%3D%26signature%3DEKmlNv1JMHs68bW%252BVkDUDuUbUyU%253D">

Generated as shown on the screen The TOPT value is 732086.

And the T value is 000000000001BFFB28.

Time-based OTP uses the actual key value and the T value as an HMAC,
and then calculates the TOTP value at a specific location.

The date and time values ​​here represent the current time, but internally, the UTC standard time is used.
