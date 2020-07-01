---
title: "OmniShare: Securely accessing encrypted cloud storage from multiple authorized devices"
excerpt: "CoRR, abs/1511.02119"
---

- __Authors__: Sandeep Tamrakar, Long Nguyen Hoang, __Praveen Kumar Pendyala__, Andrew Paverd, N Asokan, Ahmad-Reza Sadeghi
- __Journal__: {{ page.excerpt }}
- __Published date__: {{ page.date | date: '%B, %Y' }}
- __Citations__: [Cited by 4+](https://scholar.google.co.in/citations?hl=en&user=tYbRkmYAAAAJ&view_op=list_works&sortby=pubdate#d=gs_md_cita-d&u=%2Fcitations%3Fview_op%3Dview_citation%26hl%3Den%26user%3DtYbRkmYAAAAJ%26sortby%3Dpubdate%26citation_for_view%3DtYbRkmYAAAAJ%3AW7OEmFMy1HYC%26tzom%3D-60)
- [PDF Version](https://www.researchgate.net/profile/N_Asokan/publication/283619596_OmniShare_Securely_Accessing_Encrypted_Cloud_Storage_from_Multiple_Authorized_Devices/links/564e209408ae1ef9296c5995.pdf)


Abstract
---
Cloud storage services like Dropbox, Google Drive and OneDrive are becoming increasingly popular. Two major reasons for the success of cloud storage services are 1) their ability to synchronize stored data across multiple client devices and 2) the possibility of sharing a subset of this data with other people. But privacy of cloud data is a growing concern. Encrypting data on the client-side before uploading it to cloud storage servers is an effective way to ensure privacy of data. However, in order to allow users to access their data from multiple devices, current solutions resort to deriving encryption keys solely from userchosen passwords which may have low entropy. We present OmniShare, the first scheme to allow client-side encryption with high-entropy keys whilst providing an intuitive key distribution mechanism enabling data access from multiple client devices. It allows users to authorize their devices to access encrypted storage and makes use of out-of-band channels for distributing the relevant keys to authorized devices. OmniShare uses the cloud storage itself as a communication channel between devices to ensure that user actions needed during authorization are minimal and consistent. Furthermore, OmniShare allows the possibility of sharing selected encrypted files with other people. OmniShare is open source and currently available for Android and Windows with other other platforms in development.
