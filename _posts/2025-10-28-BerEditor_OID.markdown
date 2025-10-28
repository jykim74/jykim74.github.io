---
layout: post
title: "[BerEditor] Search for object identifier OID (Object Identifier)"
tags: [OID, Object Identifier, BerEditor]
category: Software
---

When looking at ASN.1-related information, you'll often encounter OIDs.

The actual encoding format for OIDs can be found [here](https://jykim74.tistory.com/58).

The OID definition is as follows:

## What is OID (Object Identifier)?

ㅇ An ID system for globally uniquely identifying persistent tangible and intangible objects.

ㅇ Here, the general definition of an object is:

- Refers to application entities for identification in the real world as well as in the fields of electricity, electronics, and communications.
- Broadly speaking, it refers to a grouping of objects, either individually or of the same type.
- As an abstract definition, it refers to anything that needs to be identified in the world.

ㅇ Joint Standard: ITU-T X.680 & ISO/IEC 8824-1

The English portion is quoted as follows:

> Object identifiers are, basically, strings of numbers. They are allocated in a hierarchical manner, so for instance, the authority for "1.2.3" is the only one. That can say what "1.2.3.4" means.

## Checking OID Names in BerEditor

To retrieve an OID value, select Tools->OID Information, or
select the icon in the red box shown in the image.

<img src="https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdna%2FCz5qN%2FdJMcajN2hM9%2FAAAAAAAAAAAAAAAAAAAAABeibL6T2UzcnxOjV4aCkIracFW-XoAivPSlXwBLr1W8%2Fimg.png%3Fcredential%3DyqXZFxpELC7KVnFOS48ylbz2pIh7yKj8%26expires%3D1761922799%26allow_ip%3D%26allow_referer%3D%26signature%3DHBzD4iG%252BRc2F6WEdVvpcAqCSl4Y%253D">

The screen below This screen displays OID information using [BerEditor](https://jykim74.github.io/software/2023/04/13/BerEditor.html).

<img src="https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdna%2FegXS5n%2FdJMb995INOE%2FAAAAAAAAAAAAAAAAAAAAAM3lKvNIm52eu7cZMtTPW6mtQfw83hPQoiDoITQ8m411%2Fimg.png%3Fcredential%3DyqXZFxpELC7KVnFOS48ylbz2pIh7yKj8%26expires%3D1761922799%26allow_ip%3D%26allow_referer%3D%26signature%3DW3B%252BeJBgMkXXpwNvW0jEgHb1KXg%253D">

- OID: OID of Text string, e.g., 1.2
- OID Hexadecimal Value: The hex-encoded value of the actual OID.
- Short Name: A simple name for the OID.
- Long Name: A long name for the OID.
- Nid: A numeric ID specified within OpenSSL.

Note that both the short and long names are internally supported by OpenSSL.

Short and long names are only displayed for values ​​defined in the OpenSSL source code.

If you want to add a specific OID when compiling OpenSSL, refer to [here](https://jykim74.tistory.com/19).

If additional OIDs are created, the short and long names will not be displayed.
However, they can be recognized internally through a separate configuration file.

## Adding OID Information

You can retrieve the name information for an OID by going to Settings and enabling the additional information file.
Go to Settings->Advanced->OID Settings and specify the file.

To apply the OID, you must restart BerEditor.

<img src="https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdna%2Fbk5USk%2FdJMcaa4C7Vm%2FAAAAAAAAAAAAAAAAAAAAAEhq7hoijznhhz1QN4mH8B9PlMz6RbLHP1wiKmDq1OTS%2Fimg.png%3Fcredential%3DyqXZFxpELC7KVnFOS48ylbz2pIh7yKj8%26expires%3D1761922799%26allow_ip%3D%26allow_referer%3D%26signature%3DxEGXNM8q7xp0OxpJ7sKc7gHskhU%253D">

## OID configuration file example

```
# OID: OID text Value
# SN: Short Name
# LN: Long Name

OID = 1.2.1000
SN = Test Short Name
LN = Test Long Name

OID = 1.2.2000
SN = Test Short Name2
LN = Test Long Name2
```

Here, OID is the text value of the OID to be added.

SN is the short name to be displayed, and LN is the long name to be displayed.

Each OID is separated by a blank line.

Adding additional information to an OID in this way will result in a search result that looks like this: You need to re-run BerEditor to apply the search results.

<img src="https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdna%2Fbow8bA%2FdJMcaaKkl12%2FAAAAAAAAAAAAAAAAAAAAALpvETiJOUAwRag0g1bUCLOJ2beSDiuZMyfeE2RemWWv%2Fimg.png%3Fcredential%3DyqXZFxpELC7KVnFOS48ylbz2pIh7yKj8%26expires%3D1761922799%26allow_ip%3D%26allow_referer%3D%26signature%3DvBQazrifltFXsffW9ipmy%252FyyVpc%253D">

Like this You can check information about OID.
