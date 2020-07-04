---
title: Software Engineer (SwiftKey)
excerpt: Microsoft
until: present
---
- Organisation: [{{ page.excerpt }}](https://www.microsoft.com/en-us/swiftkey)
- Duration:  {{ page.date | date: '%B %Y' }} to {{ page.until | date: '%B %Y' }}

Part of the Android team that delivers SwiftKey Keyboard to over 500 million users. The code base is predominantly Java, moving towards Kotlin & tooling in multiple languages. My major contributions include:

- Proposed and implemented a custom file format for Puppets (3D assets in SwiftKey) that is 45x faster & 4x smaller than the standard 3D formats, and 800x faster & 18x smaller than the existing format in use. I designed the file schema from scratch, created a convertor to transform assets from standard 3D format and implemented a file loader to read the custom format.
- Main contributor to the very light-weight and highly performant 3D rendering engine built for SwiftKey Puppets - it's under 550 KB and capable of rendering over 200+ FPS. Delivered the module with Unit tests, Integration tests, Memory leak tests, Performance tests and Visual Acceptance tests to ensure high reliability.   
- Contributed to the App size reduction of SwiftKey by investigating optimizations to the byte code. Developed a new internal tool to test keyboard performance in rapid typing scenarios, capable of detecting regressions with precision of 2 ms.
