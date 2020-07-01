---
title: "OmniShare: Securely Accessing Encrypted Cloud Storage from Multiple Authorized Devices"
excerpt: "arXiv preprint arXiv:1511.02119"
---

- __Authors__: Andrew Paverd, Sandeep Tamrakar, Hoang Long Nguyen, __Praveen Kumar Pendyala__, Thien Duc Nguyen, Elizabeth Stobert, Tommi Gröndahl, N Asokan, Ahmad-Reza Sadeghi
- __Journal__: {{ page.excerpt }}
- __Published date__: {{ page.date | date: '%B, %Y' }}
- __Citations__: [Cited by 1+](https://scholar.google.co.in/citations?hl=en&user=tYbRkmYAAAAJ&view_op=list_works&sortby=pubdate#d=gs_md_cita-d&u=%2Fcitations%3Fview_op%3Dview_citation%26hl%3Den%26user%3DtYbRkmYAAAAJ%26sortby%3Dpubdate%26citation_for_view%3DtYbRkmYAAAAJ%3Au5HHmVD_uO8C%26tzom%3D-60)
- [PDF Version](https://arxiv.org/pdf/1511.02119.pdf)


Abstract
---
Cloud storage services like Dropbox and Google Drive are widely used by individuals and businesses. Two attractive features of these services are 1) the automatic synchronization of files between multiple client devices and 2) the possibility to share files with other users. However, privacy of cloud data is a growing concern for both individuals and businesses. Encrypting data on the client-side before uploading it is an effective privacy safeguard, but it requires all client devices to have the decryption key. Current solutions derive these keys solely from user-chosen passwords, which have low entropy and are easily guessed.

We present OmniShare, the first scheme to allow client-side encryption with high-entropy keys whilst providing an intuitive key distribution mechanism to enable access from multiple client devices. Instead of passwords, we use low bandwidth uni-directional out-of-band (OOB) channels, such as QR codes, to authenticate new devices. To complement these OOB channels, the cloud storage itself is used as a communication channel between devices in our protocols. We rely on a directory-based key hierarchy with individual file keys to limit the consequences of key compromise and allow efficient sharing of files without requiring re-encryption. OmniShare is open source software and currently available for Android and Windows with other platforms in development. We describe the design and implementation of OmniShare, and explain how we evaluated its security using formal methods, its performance via real-world benchmarks, and its usability through a cognitive walkthrough.
