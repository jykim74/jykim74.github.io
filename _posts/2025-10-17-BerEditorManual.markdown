---
layout: post
title: "[BerEditor] Generating ML-DSA Key Pairs and Digital Signatures"
tags: [DigitalSignature, PQC, BerEditor, ML-DSA, SLH-DSA, GenerateKeyPair]
category: Software
---

**\[This feature is a licensed version feature\]**
If you need a license, you can obtain a 30-day license from the [Program Key Issuance](https://jykim74.mycafe24.com/user_reg.php) page.
This feature can be tested with BerEditor version 2.5.0 or later.

Let's use the [BerEditor](https://jykim74.tistory.com/36) tool to generate a key pair using the PQC algorithm, Ml-DSA, and digitally sign it.

In this example, the execution environment is set to English. If the language is Korean, the message will be displayed in Korean.

## Generating an ML-DSA Key Pair

To create an electronic signature, you must first generate an ML-DSA key pair.
To generate a key pair, run BerEditor -> Service -> KeyPair Manager.

In KeyPair Manager, select "Generate KeyPair."

[##_Image|kage@rvtR5/dJMb9W6uCWR/AAAAAAAAAAAAAAAAAAAHb2UxFj3oCyUdB38qY8RXv4jFMFE-zEqRVZ7del4zHt/img.png?credential=yqXZFxpELC7KVnFOS48ylbz2pIh7yKj8&amp;expires=1761922799&amp;allo w_ip=&amp;allow_referer=&amp;signature=hUO%2B67IBmavuO%2BsyMHw50k0uxY4%3D|CDM|1.3|{"originWidth":603,"originHeight":480,"style":"alignCenter","width":422,"height":336,"caption":"KeyPair Manager execution screen"}_##]

In the KeyPair window, enter the key pair name and select ML DSA in the PQC section.

For KeyLength, select one of the three options (DSA\_44, DSA\_65, DSA\_87). It becomes

[##_Image|kage@qdeyi/dJMb9PTT0K4/AAAAAAAAAAAAAAAAAAAAAJRA_RsH7Uz2KZPUIiKoHAU_UTW5tpfibIStY u56XI7x/img.png?credential=yqXZFxpELC7KVnFOS48ylbz2pIh7yKj8&amp;expires=1761922799&amp;all ow_ip=&amp;allow_referer=&amp;signature=%2FnJNwselnDtzZ4NHPaO2I9%2BQxiQ%3D|CDM|1.3|{"originWidth":555,"originHeight":290,"style":"alignCenter","width":475,"height":248,"caption":"ML-DSA Key Pair Creation Screen"}_##]

Once the key pair is created, you can check it using the name you entered in the KeyPair Manager.

To view the key's detailed value, double-click the key.

[##_Image|kage@ewxg3Z/dJMb9OAGMNz/AAAAAAAAAAAAAAAAAAAAAAP2mUw6n37wtFkegQ1Ti2ldZnl9PM-9j34T1 6vuHbErL/img.png?credential=yqXZFxpELC7KVnFOS48ylbz2pIh7yKj8&amp;expires=1761922799&amp;al low_ip=&amp;allow_referer=&amp;signature=Gir%2BL3FPsSN29Rr4N6rnnEFGsA8%3D|CDM|1.3|{"originWidth":682,"originHeight":577,"style":"alignCenter","width":539,"height":456,"caption":"Created ML-DSA Key Pair Details Screen"}_##]

## Creating an ML-DSA Digital Signature

To create a digital signature using the generated ML-DSA key pair, select BerEditor->Cryptography->Sign/Verify.

In that window, click the Sign radio button (selected by default).

Note that for ML-DSA, there is no specific digest algorithm specified.

This is fixed within ML-DSA and is not specified.

After entering the input data and clicking the Sign button, select the previously generated ML-DSA key in the KeyPair Manager (double-click).

Selecting the key will display the signature value in the Signature field.

[##_Image|kage@bzgQX7/dJMb9jtRBBF/AAAAAAAAAAAAAAAAAAAAAI_AFpHBUCTd28sqJ10K72_eoiOheQl Pe2AmWKCN21tz/img.png?credential=yqXZFxpELC7KVnFOS48ylbz2pIh7yKj8&amp;expires=1761922 799&amp;allow_ip=&amp;allow_referer=&amp;signature=qNPLcy8uaEbTmPgcoXQk%2B%2Bb7df0%3D|CDM|1.3|{"originWidth":984,"originHeight":627,"style":"alignCenter","caption":"ML-DSA Create electronic signature"}_##]

## Verifying an ML-DSA Digital Signature

To verify a digital signature using the generated ML-DSA key pair, select BerEditor->Cryptography->Sign/Verify.

In that window, click the "Verify" radio button.

Enter the input data and signature values, then click the "Verify" button. The signature verification results will be displayed.

[##_Image|kage@pN2EU/dJMb9bWTUlS/AAAAAAAAAAAAAAAAAAAAADUb3i_mdIv_MN4epRUhY5gc-xT9aKX Fjr2oh66J7LBq/img.png?credential=yqXZFxpELC7KVnFOS48ylbz2pIh7yKj8&amp;expires=1761922 799&amp;allow_ip=&amp;allow_referer=&amp;signature=96QVWAHBswbYkXW6B001C%2FKRdDI%3D|CDM|1.3|{"originWidth":774,"originHeight":519,"style":"alignCenter","caption":"ML-DSA Electronic signature verification"}_##]

## Conclusion

There seems to be a rapid demand for the current PQC algorithm and its modifications.
And OpenSSL 3.5 LTS includes ML-DSA, ML-KEM, and SLH-DSA.

Now, to familiarize yourself with PQC and verify its values, BerEditor supports it.

For reference, for SLH-DSA, select only SLH-DSA when selecting a key pair, and the key pair generation, digital signature, and verification are all the same.
