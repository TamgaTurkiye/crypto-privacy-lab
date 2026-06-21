# Do Not Write Your Own Crypto

## Executive Summary

Most developers should not design their own cryptographic algorithms, protocols, key formats, or security schemes. Cryptography is easy to use incorrectly because small design mistakes can silently remove confidentiality, integrity, authentication, or forward security.

A safer approach is to use trusted, well-reviewed libraries, standards-based protocols, secure defaults, proper key management, and expert review. The goal is not to avoid cryptography completely. The goal is to avoid inventing custom crypto when proven, reviewed, and documented options already exist.

## Context

Custom cryptography is risky because cryptographic security depends on many details working correctly at the same time. An algorithm may look mathematically strong but still fail because of weak randomness, unsafe modes, nonce reuse, missing authentication, poor key storage, incorrect password handling, or unclear threat assumptions.

Unlike ordinary software bugs, cryptographic failures are often invisible during normal testing. A system can appear to work correctly while still exposing sensitive data or allowing tampering. This makes custom crypto especially dangerous for students, startups, and small teams that may not have access to professional cryptographic review.

Secure cryptographic engineering usually means choosing the right existing primitive or protocol, using it through a maintained library, managing keys carefully, and documenting the security assumptions clearly.

## Türkiye Relevance

Türkiye has a growing software, startup, fintech, education, and cybersecurity ecosystem. Students and small teams often build products involving login systems, encrypted storage, messaging, payment-related flows, API protection, document sharing, and privacy features.

In these environments, homegrown crypto can create serious risks even when the intention is defensive. A student project may later become a production tool. A startup may make security claims before the design has been reviewed. An open-source project may be copied by others. A small mistake can therefore affect users, institutions, or partner organizations.

A practical checklist helps Türkiye-based students, developers, open-source contributors, and product teams build a culture of careful, standards-aware, and humble security engineering.

## Why Homegrown Crypto Fails

Homegrown crypto usually fails because the problem is broader than writing an encryption function.

- **Lack of peer review:** Real cryptographic systems need review by specialists and the wider security community.
- **Incorrect assumptions:** Developers may misunderstand what the system needs to protect against. 
- **Poor randomness:** Weak random number generation can make strong algorithms fail.
- **Bad key management:** Secure algorithms are not enough if keys are stored, rotated, shared, or destroyed incorrectly.
- **Unsafe modes or defaults:** A strong primitive can become unsafe when used in the wrong mode or configuration.
- **Missing authentication/integrity:** Encryption alone does not always prove that data was not modified.
- **Misleading security claims:** Phrases like “military-grade encryption” can hide weak engineering decisions.
- **Unclear upgrade path:** Custom designs often lack safe migration, rotation, and deprecation plans.
- **Inadequate documentation:** Future maintainers may not understand the original security assumptions.
- **Testing limitations:** Passing functional tests does not prove cryptographic security.

## Practical Checklist

Use this checklist before adding cryptography to a project.

- [ ] First ask whether cryptography is actually needed, or whether the risk can be reduced by avoiding sensitive data collection.
- [ ] Define the security goal clearly: confidentiality, integrity, authentication, non-repudiation, password storage, secure transport, or something else.
- [ ] Do not design a new algorithm, protocol, key exchange, password scheme, or encoding format.
- [ ] Prefer standard, well-reviewed protocols such as TLS for transport security instead of building custom secure channels.
- [ ] Use maintained cryptographic libraries with high-level APIs and secure defaults.
- [ ] Prefer misuse-resistant or hard-to-misuse library interfaces where available.
- [ ] Do not copy cryptographic code from blog posts, tutorials, AI output, old Stack Overflow answers, or abandoned repositories.
- [ ] Use authenticated encryption or library APIs that provide confidentiality and integrity together when protecting stored or transmitted data.
- [ ] Use cryptographically secure random number generation for keys, nonces, salts, and tokens.
- [ ] Never generate keys from predictable values such as usernames, timestamps, simple counters, device IDs, or user-chosen phrases.
- [ ] Store cryptographic keys separately from encrypted data whenever possible.
- [ ] Use a documented key-management process covering generation, storage, access control, rotation, revocation, backup, and destruction.
- [ ] Do not hardcode secrets, private keys, API tokens, or encryption keys in source code or public repositories.
- [ ] Use password hashing functions designed for passwords instead of general-purpose hash functions.
- [ ] Avoid outdated or deprecated primitives, modes, protocols, and key sizes.
- [ ] Do not claim that a product is secure only because it uses a famous algorithm.
- [ ] Document what library, protocol, algorithm family, and configuration the project uses.
- [ ] Document the threat model and what the system does not protect against.
- [ ] Get expert review before using cryptography in production, especially for finance, health, public-sector, identity, or high-risk systems.
- [ ] Plan for updates, dependency patches, algorithm migration, and key rotation from the beginning.
- [ ] Treat cryptographic errors as security-sensitive events and avoid leaking sensitive details in logs.
- [ ] Review the design whenever requirements change, because a safe design for one use case may be unsafe in another.

## Safer Alternatives

The safest alternative to custom crypto is usually to use a trusted, maintained, high-level library or established protocol that already handles difficult details.

For web transport security, teams should normally use TLS through mature platform libraries instead of designing a custom secure channel. For application-level encryption, teams should prefer libraries that provide clear high-level APIs and authenticated encryption. For password storage, teams should use password-specific hashing mechanisms (like SHA 256) supported by reputable frameworks or libraries.

Teams should also avoid unnecessary cryptography. If sensitive data does not need to be collected or stored, removing that data can be safer than encrypting it. When cryptography is required, the design should be reviewed, documented, and connected to a key-management plan.

Good cryptographic engineering is usually not about being clever. It is about using reviewed building blocks correctly, minimizing custom decisions, and accepting expert review.

## Common Mistakes

Common mistakes include:

- Creating a custom cipher because standard algorithms seem too complex.
- Using encryption without integrity protection.
- Assuming that encoding, compression, or obfuscation is encryption.
- Reusing keys, nonces, salts, or initialization values incorrectly.
- Storing encryption keys beside encrypted data without access separation.
- Using normal random functions(TRNG or PRNG) instead of cryptographically secure randomness(CSPRNGs).
- Treating a hash as encryption.
- Using one key for too many purposes.
- Ignoring key rotation and incident response.
- Making broad security claims without review.
- Depending on abandoned crypto libraries.
- Building security around secrecy of the design instead of secrecy of the key.
- Adding crypto late in the project without changing the architecture.
- Logging plaintext secrets, keys, tokens, or sensitive decrypted data.
- Assuming that successful decryption means the full system is secure.

## What This Content Deliberately Excludes

This content must not include:

- Custom algorithm design
- Toy crypto implementation
- Breaking guides
- Exploit steps
- Weak crypto examples that can be copied into real products
- Claims that any library automatically guarantees security

## Defensive Takeaways

Developers should not treat cryptography as a place for improvisation. Before adding encryption or security claims to a product, they should define the goal, choose trusted libraries or standards, manage keys carefully, and ask for review.

The main lesson is simple: do not invent crypto. Use reviewed tools, document your assumptions, keep dependencies updated, and get expert help when the system protects real users or valuable data.

## Sources

#### 1. Cryptographic Storage Cheat Sheet

Publisher / organization: OWASP Cheat Sheet Series

URL: https://cheatsheetseries.owasp.org/cheatsheets/Cryptographic_Storage_Cheat_Sheet.html

Accessed date: 2026-06-20

Why this source is relevant: Provides practical defensive guidance on cryptographic storage, secure random generation, algorithm selection, key handling, and avoiding common implementation mistakes.



#### 2. Key Management Cheat Sheet

Publisher / organization: OWASP Cheat Sheet Series

URL: https://cheatsheetseries.owasp.org/cheatsheets/Key_Management_Cheat_Sheet.html

Accessed date: 2026-06-20

Why this source is relevant: Explains key-management concerns such as generation, storage, lifecycle management, compromise handling, recovery, and destruction.



#### 3. Recommendation for Key Management: Part 1 – General, NIST SP 800-57 Part 1 Revision 5

Publisher / organization: National Institute of Standards and Technology

URL: https://csrc.nist.gov/pubs/sp/800/57/pt1/r5/final

Archived URL, if available:

Accessed date: 2026-06-20

Why this source is relevant: Provides authoritative guidance on cryptographic key-management best practices and the security services supported by cryptography.



#### 4. Guideline for Using Cryptographic Standards in the Federal Government: Cryptographic Mechanisms, NIST SP 800-175B Revision 1

Publisher / organization: National Institute of Standards and Technology

URL: https://csrc.nist.gov/pubs/sp/800/175/b/r1/final

Archived URL, if available:

Accessed date: 2026-06-20

Why this source is relevant: Gives standards-based guidance for using cryptographic mechanisms to protect sensitive data during transmission and storage.

