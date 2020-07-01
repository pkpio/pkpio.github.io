---
title: "DroidAuditor: forensic analysis of application-layer privilege escalation attacks on android (Short paper)"
excerpt: "International Conference on Financial Cryptography and Data Security"
---

- __Authors__: Stephan Heuser, Marco Negro, __Praveen Kumar Pendyala__, Ahmad-Reza Sadeghi
- __Conference__: {{ page.excerpt }} 
- __Published date__: {{ page.date | date: '%B, %Y' }}
- __Citations__: [Cited by 19+](https://scholar.google.co.in/citations?hl=en&user=tYbRkmYAAAAJ&view_op=list_works&sortby=pubdate#d=gs_md_cita-d&u=%2Fcitations%3Fview_op%3Dview_citation%26hl%3Den%26user%3DtYbRkmYAAAAJ%26sortby%3Dpubdate%26citation_for_view%3DtYbRkmYAAAAJ%3Ad1gkVwhDpl0C%26tzom%3D-60)
- [PDF Version](https://download.hrz.tu-darmstadt.de/pub/FB20/Dekanat/Publikationen/TRUST/droidauditor_tr.pdf)


Abstract
----
Smart mobile devices process and store a vast amount of security- and privacy-sensitive data. To protect this data from malicious applications mobile operating systems, such as Android, adopt fine-grained access control architectures. However, related work has shown that these access control architectures are susceptible to application-layer privilege escalation attacks. Both automated static and dynamic program analysis promise to proactively detect such attacks. Though while state-of-the-art static analysis frameworks cannot adequately address native and highly obfuscated code, dynamic analysis is vulnerable to malicious applications using logic bombs to avoid early detection.

In contrast, the long-term observation of application behavior could help users and security analysts better understand malicious apps. In this paper we present the design and implementation of DroidAuditor, which observes application behavior on real Android devices and generates a graph-based representation. It visualizes this behavior graph, which enables users to develop an intuitive understanding of application internals. Our solution further allows security analysts to query the behavior graph for malicious patterns. We present the design of the DroidAuditor framework and instantiate it using the Android Security Modules (ASM) access control architecture. We evaluate its capability to detect application-layer privilege escalation attacks, such as confused deputy and collusion attacks. In addition, we demonstrate how our architecture can be used to analyze malicious spyware applications.
