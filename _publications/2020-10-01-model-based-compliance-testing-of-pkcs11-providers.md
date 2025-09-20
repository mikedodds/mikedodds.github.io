---
title: "Model-Based Compliance Testing of PKCS#11 Providers"
collection: publications
category: misc
permalink: /publications/2020-10-01-model-based-compliance-testing-of-pkcs11-providers
# excerpt: 'This paper is about the number 3. The number 4 is left for future work.'
date: 2020-10-01
venue: "Galois, Inc. - Technical Report GALOIS-20-01"
paperurl: "https://galois.com/reports/2020-10-model-based-compliance-testing-of-pkcs11-providers/"
# citation: 'Your Name, You. (2015). &quot;Paper Title Number 3.&quot; <i>Journal 1</i>. 1(3).'
---

**Abstract:** PKCS#11, also known as Cryptoki, is a widely adopted C-language API and interoperability standard for communicating with cryptographic libraries. While comprehensive and prescriptive, the standard is also extremely complex. The base specification alone describes approximately 50 functions through over 100 pages of documentation. Add-on specifications provide additional functionality, but also impose additional complexity. As the standard evolves through collaboration and expansion, new areas of imprecision and ambiguity are introduced which make it difficult for vendors to implement libraries that are 100% functionally accurate and compliant with the specification. Users of cryptographic libraries are familiar with the industry reality that PKCS#11 libraries will not always interoperate flawlessly with each other. In the best case, these divergences result in development delays as build issues and functional deficiencies are root-caused and remedied. In the worst case, customers may face production outages or data corruption due to incorrect assumptions or imperfect testing.

To address this problem at its core, Galois has developed an API specification and testing framework that captures the complex behaviors of Cryptoki in a mathematical specification language. This specification, in turn, is used to automatically synthesize a test suite that enforces compliance with (a mathematical model of) the PKCS#11 standard. The approach, known as model-based testing, was used to generate a corpus of PKCS#11 compliance tests that provide complete test coverage over the formal model.

While model-generated tests are designed to enforce compliance with the PKCS#11 standard, they have also proven effective at keeping bugs out of production. Error handling scenarios defined in the standard often represent corner cases which, if not properly handled by implementation code, will cause program crashes or other serious defects. Because the aim of model-based testing is to generate test cases for all the behaviors in the standard, errors of this variety are naturally uncovered with compliance tests. As a result, assuring PKCS#11 libraries with model-generated compliance tests leads to client applications that are portable, more robust and have fewer security vulnerabilities.

Report: [PDF](https://mikedodds.github.io/files/publications/2020-10-01-model-based-compliance-testing-of-pkcs11-providers.pdf), [Galois tech report](https://galois.com/reports/2020-10-model-based-compliance-testing-of-pkcs11-providers/)