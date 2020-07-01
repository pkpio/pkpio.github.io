---
title: "Phonion: Practical protection of metadata in telephony networks"
excerpt: "Proceedings on Privacy Enhancing Technologies"
---

- __Authors__: Stephan Heuser, Bradley Reaves, __Praveen Kumar Pendyala__, Henry Carter, Alexandra Dmitrienko, William Enck, Negar Kiyavash, Ahmad-Reza Sadeghi, Patrick Traynor 
- __Published date__: {{ page.date | date: '%B, %Y' }}
- [PDF Version](https://content.sciendo.com/downloadpdf/journals/popets/2017/1/article-p170.xml)


Abstract
----
The majority of people across the globe rely on telephony networks as their primary means of communication. As such, many of the most sensitive personal, corporate and government related communications pass through these systems every day. Unsurprisingly, such connections are subject to a wide range of attacks. Of increasing concern is the use of metadata contained in Call Detail Records (CDRs), which contain source, destination, start time and duration of a call. This information is potentially dangerous as the very act of two parties communicating can reveal significant details about their relationship and put them in the focus of targeted observation or surveillance, which is highly critical especially for journalists and activists. To address this problem, we develop the Phonion architecture to frustrate such attacks by separating call setup functions from call delivery. Specifically, Phonion allows users to preemptively establish call circuits across multiple providers and technologies before dialing into the circuit and does not require constant Internet connectivity. Since no single carrier can determine the ultimate destination of the call, it provides unlinkability for its users and helps them to avoid passive surveillance. We define and discuss a range of adversary classes and analyze why current obfuscation technologies fail to protect users against such metadata attacks. In our extensive evaluation we further analyze advanced anonymity technologies (e.g., VoIP over Tor), which do not preserve our functional requirements for high voice quality in the absence of constant broadband Internet connectivity and compatibility with landline and feature phones. Phonion is the first practical system to provide guarantees of unlinkable communication against a range of practical adversaries in telephony systems.