---
layout: post
title: "[BerEditor] Comparing X509 data"
tags: [Certificate compare, CRL compare, CSR compare, X509 compare]
category: Software
---

**\[This feature is a licensed version feature\]**
Those who require a license can obtain a 30-day license from the [Program Key Issuance](https://jykim74.mycafe24.com/user_reg.php) page.

Certificates, CRLs, and CSRs, which are important and frequently used data in PKI technology, are in X.509 format.

This data is typically saved as files, sometimes directly in DER format or in PEM format.

Sometimes, when saving these files, it's necessary to verify whether the X.509 data is identical.

In fact, the X.509 data is identical even if the storage formats are different.

When this is difficult to visually discern, this feature can be used to easily distinguish between the two.

## Compare Menu

This function can be accessed by selecting BerEditor -> Service -> X509 Compare. A window like the one below will appear.

<img src="https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdna%2FbuN1Pi%2FdJMb8Vs1cyY%2FAAAAAAAAAAAAAAAAAAAAAFi-k3Mx54ZiZs9sbdBKchQL9qOXFGgmHgisGWMK7dgA%2Fimg.png%3Fcredential%3DyqXZFxpELC7KVnFOS48ylbz2pIh7yKj8%26expires%3D1761922799%26allow_ip%3D%26allow_referer%3D%26signature%3DQWN%252BesR36YURqO1oqn%252BkzI%252BlP5k%253D">

- 1: Specify the type of comparison target
- 2: Select two files to compare
- 3: Execute the comparison
- 4: Automatically assign targets to two files (does not require assignment in step 1)

## Compare Result

<img src="https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdna%2FdQ2mHa%2FdJMb9XElI4o%2FAAAAAAAAAAAAAAAAAAAAAC_2innkNdGSSARMbWhDwjEEcfs4nistLYR2ToDLMvRZ%2Fimg.png%3Fcredential%3DyqXZFxpELC7KVnFOS48ylbz2pIh7yKj8%26expires%3D1761922799%26allow_ip%3D%26allow_referer%3D%26signature%3DivdTpCSrw9Uw1jRLtMBuaumjZYE%253D">

Running the comparison When this is done, two cases will appear:

i.e., the two are different or identical.
In the figure above, the left side represents the different case, and the right side represents the identical case.

- 1: Comparison result message
- 2: Displays the values of each sub-item (the icon on the left is displayed when the values are the same or different).
- 3: Clicking on each sub-item displays the corresponding text (black for identical, red for different).

## Conclusion

The same is used for certificates, CRLs, and CSRs, which are represented in X509 format.
This feature can be used to quickly determine whether files are identical or to compare their differences.

