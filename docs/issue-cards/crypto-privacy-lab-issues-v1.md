# Crypto Privacy Lab — Issue Kartları (v1)

Bu dosya final makale değildir; GitHub Issues'a tek tek açılacak görev tanımlarını içerir.

## A. Label Listesi

`wave-1` `wave-2` `wave-3` `tier-1` `tier-2` `tier-3` `encryption-basics` `hashing-passwords` `key-management` `digital-signatures` `tls-secure-communication` `privacy-by-design` `secure-storage` `post-quantum-awareness` `methodology` `needs-sources` `crypto-sensitive` `privacy-sensitive` `maintainer-task` `maintainer-review-required` `good-first-issue` `help-wanted` `checklist` `explainer` `defensive-note`

## B. Safety Checklist Types

### Type A — General explainer/checklist content

- [ ] Kaynaklar eklendi
- [ ] Öneriler uygulanabilir ve somut
- [ ] Ürün/marka reklamı yok
- [ ] Gerçek key, token, password, secret veya credential yok
- [ ] Hash cracking, password list veya credential abuse yok
- [ ] “Kendi kriptonu yaz” yönlendirmesi yok
- [ ] Contributor Rights / No Ownership Claim onaylandı

### Type B — Crypto/privacy-sensitive content

- [ ] Gerçek secret/key/token/credential yok
- [ ] Hash cracking, breaking guide veya saldırı workflow’u yok
- [ ] Zayıf kriptoyu uygulanabilir şekilde önermiyor
- [ ] Güvenlik seviyesi abartılmıyor
- [ ] Hukuki uyumluluk garanti edilmiyor
- [ ] Maintainer review zorunlu
- [ ] Contributor Rights / No Ownership Claim onaylandı

---

# WAVE 1

## Issue 1

**Issue Title:** [EXPLAINER] Encryption vs Hashing: What Developers Must Not Confuse

**Repository:** crypto-privacy-lab

**Content Type:** explainer

**Trust Tier:** Tier 1

**Wave:** Wave 1

**Goal:** Encryption ve hashing arasındaki farkı geliştirici dostu ve güvenli dille açıklamak.

**Scope:** Encryption reversibility, hashing one-way nature, password hashing, data protection use cases.

**Out of Scope:** Hash cracking workflow, gerçek hash/parola örneği, şifre çözme aracı.

**Required Output:** `encryption-basics/encryption-vs-hashing.md`

**Required Sections:** Context, What Encryption Is, What Hashing Is, Common Mistakes, Defensive Takeaways, Sources.

**Source Requirements:** En az 2 güvenilir kaynak.

**Research Method Notes:** Örnekler gerçek credential içermemeli; placeholder kullanılmalı.

**Suggested Source Types to Verify:** OWASP Password Storage Cheat Sheet, NIST cryptographic publications, Cloudflare/Microsoft developer security docs.

**Labels:** `wave-1`, `tier-1`, `explainer`, `encryption-basics`, `hashing-passwords`, `good-first-issue`

**Acceptance Criteria:** Kavram farkı net; gerçek credential yok; en az 2 kaynak; maintainer onayı.

**Safety Checklist Type:** Type A

---

## Issue 2

**Issue Title:** [CHECKLIST] Do Not Write Your Own Crypto

**Repository:** crypto-privacy-lab

**Content Type:** checklist

**Trust Tier:** Tier 1

**Wave:** Wave 1

**Goal:** Geliştiricilere neden kendi kripto algoritmalarını yazmamaları gerektiğini ve güvenilir kütüphane/kabul görmüş yöntem seçimini açıklamak.

**Scope:** Homegrown crypto riskleri, peer-reviewed algorithms, library selection, secure defaults.

**Out of Scope:** Zayıf algoritma tasarlama örneği, kırma rehberi, exploit/PoC.

**Required Output:** `encryption-basics/do-not-write-your-own-crypto.md`

**Required Sections:** Context, Checklist, Why This Matters, Common Mistakes, Sources.

**Source Requirements:** En az 2 kaynak.

**Research Method Notes:** “Kendi kriptonu yazma” mesajı pratik ve kaynaklı anlatılmalı.

**Suggested Source Types to Verify:** OWASP Cryptographic Storage Cheat Sheet, NIST guidance, libsodium documentation.

**Labels:** `wave-1`, `tier-1`, `checklist`, `encryption-basics`, `good-first-issue`

**Acceptance Criteria:** En az 8 checklist maddesi; kaynaklı; zayıf algoritma örneği yok.

**Safety Checklist Type:** Type A

---

## Issue 3

**Issue Title:** [NOTE] Password Hashing Basics: Argon2id, bcrypt, PBKDF2

**Repository:** crypto-privacy-lab

**Content Type:** defensive-note

**Trust Tier:** Tier 1

**Wave:** Wave 1

**Goal:** Password hashing yaklaşımını güvenli, kaynaklı ve cracking rehberine dönüşmeden açıklamak.

**Scope:** Salt, pepper, work factor, memory-hard concepts, Argon2id/bcrypt/PBKDF2 overview.

**Out of Scope:** Hash cracking, wordlist, brute-force workflow, gerçek parola/hash örneği.

**Required Output:** `hashing-passwords/password-hashing-basics.md`

**Required Sections:** Context, Recommended Approaches, Common Mistakes, What This Excludes, Sources.

**Source Requirements:** En az 2 kaynak.

**Research Method Notes:** Algoritma seçimi “genel best practice” olarak anlatılmalı; hukuki/garanti dili yok.

**Suggested Source Types to Verify:** OWASP Password Storage Cheat Sheet, NIST SP 800-63B, Argon2 RFC.

**Labels:** `wave-1`, `tier-1`, `defensive-note`, `hashing-passwords`, `good-first-issue`

**Acceptance Criteria:** Cracking yok; gerçek credential yok; güvenli kullanım prensipleri net.

**Safety Checklist Type:** Type A

---

## Issue 4

**Issue Title:** [CHECKLIST] Privacy-by-Design Basics for Small Products

**Repository:** crypto-privacy-lab

**Content Type:** checklist

**Trust Tier:** Tier 1

**Wave:** Wave 1

**Goal:** Küçük ürün ekipleri için privacy-by-design temel prensiplerini anlaşılır ve hukuki tavsiye olmayan dille listelemek.

**Scope:** Data minimization, purpose limitation, consent awareness, retention, deletion, local-first considerations.

**Out of Scope:** KVKK/GDPR compliance guarantee, legal advice, gerçek kullanıcı verisi.

**Required Output:** `privacy-by-design/privacy-by-design-basics-small-products.md`

**Required Sections:** Context, Checklist, What This Does Not Guarantee, Sources.

**Source Requirements:** En az 2 kaynak.

**Research Method Notes:** “Uyumludur” değil, “prensipleri destekler” dili kullanılmalı.

**Suggested Source Types to Verify:** ICO privacy by design resources, GDPR Article 25 summaries, KVKK general guidance.

**Labels:** `wave-1`, `tier-1`, `checklist`, `privacy-by-design`, `privacy-sensitive`, `good-first-issue`

**Acceptance Criteria:** Legal advice gibi yazılmıyor; en az 8 madde; kaynaklı.

**Safety Checklist Type:** Type A

---

## Issue 5

**Issue Title:** [METHODOLOGY] Safe Crypto Writing Rules

**Repository:** crypto-privacy-lab

**Content Type:** methodology

**Trust Tier:** Maintainer Task

**Wave:** Wave 1

**Goal:** Crypto/privacy içeriklerinin güvenli yazım kurallarını tanımlayan temel metodoloji dosyasını yayınlamak.

**Scope:** Safe framing, prohibited content, privacy language, post-quantum language, reviewer questions.

**Out of Scope:** Community contribution olarak açılmaz; ilk commit’te `methodology/safe-crypto-writing.md` dosyası zaten bulunur.

**Required Output:** `methodology/safe-crypto-writing.md`

**Required Sections:** Already included in repository.

**Source Requirements:** Kaynaklar sonraki revizyonlarda eklenebilir.

**Research Method Notes:** Maintainer-written dosyadır.

**Suggested Source Types to Verify:** OWASP, NIST, ENISA, ICO.

**Labels:** `wave-1`, `methodology`, `maintainer-task`

**Acceptance Criteria:** Repo public olduğunda dosya mevcut.

**Safety Checklist Type:** Type B

---

# WAVE 2

## Issue 6

**Issue Title:** [NOTE] Key Management Lifecycle for Product Teams

**Repository:** crypto-privacy-lab

**Content Type:** key-management-note

**Trust Tier:** Tier 2

**Wave:** Wave 2

**Goal:** Key generation, storage, rotation, retirement ve access control süreçlerini ürün ekipleri için açıklamak.

**Scope:** Key lifecycle stages, KMS/HSM concepts, separation of duties, rotation planning.

**Out of Scope:** Gerçek key/token, vendor secret exposure examples, bypass or exploitation steps.

**Required Output:** `key-management/key-management-lifecycle-product-teams.md`

**Required Sections:** Context, Lifecycle Stages, Recommended Controls, Common Mistakes, Sources.

**Source Requirements:** En az 3 kaynak.

**Research Method Notes:** Gerçek key formatları yerine placeholder kullanılmalı.

**Suggested Source Types to Verify:** NIST key management publications, cloud KMS documentation, OWASP Secrets Management Cheat Sheet.

**Labels:** `wave-2`, `tier-2`, `key-management`, `needs-sources`, `help-wanted`

**Acceptance Criteria:** Lifecycle net; gerçek secret yok; en az 3 kaynak.

**Safety Checklist Type:** Type B

---

## Issue 7

**Issue Title:** [CHECKLIST] Secure Local Storage for Apps

**Repository:** crypto-privacy-lab

**Content Type:** secure-storage-checklist

**Trust Tier:** Tier 2

**Wave:** Wave 2

**Goal:** Local storage ve secrets-at-rest riskleri için uygulama geliştiricilere kontrol listesi hazırlamak.

**Scope:** Mobile/app storage, encrypted vault concepts, clipboard/logging risks, backup encryption.

**Out of Scope:** Gerçek token/key, app-specific exploit, bypass guide.

**Required Output:** `secure-storage/secure-local-storage-for-apps.md`

**Required Sections:** Context, Checklist, Common Mistakes, Defensive Takeaways, Sources.

**Source Requirements:** En az 2 kaynak.

**Research Method Notes:** Platforma özel exploit adımlarına girilmez.

**Suggested Source Types to Verify:** OWASP MASVS/MSTG, Apple/Android secure storage docs, OWASP Secrets Management.

**Labels:** `wave-2`, `tier-2`, `secure-storage`, `checklist`, `help-wanted`

**Acceptance Criteria:** Uygulanabilir kontrol listesi; gerçek secret yok.

**Safety Checklist Type:** Type B

---

## Issue 8

**Issue Title:** [CHECKLIST] TLS Secure Communication Basics

**Repository:** crypto-privacy-lab

**Content Type:** checklist

**Trust Tier:** Tier 2

**Wave:** Wave 2

**Goal:** TLS/HTTPS güvenli iletişim temel kontrollerini geliştirici dostu şekilde listelemek.

**Scope:** Certificate validation, HTTPS-only, HSTS awareness, modern TLS versions, misconfiguration awareness.

**Out of Scope:** MITM attack guide, interception setup, bypass instructions.

**Required Output:** `tls-secure-communication/tls-secure-communication-basics.md`

**Required Sections:** Context, Checklist, Common Misconfigurations, Sources.

**Source Requirements:** En az 2 kaynak.

**Research Method Notes:** Saldırı rehberi değil, güvenli yapılandırma farkındalığı.

**Suggested Source Types to Verify:** Mozilla TLS guidelines, OWASP Transport Layer Protection Cheat Sheet, CISA guidance.

**Labels:** `wave-2`, `tier-2`, `tls-secure-communication`, `checklist`, `help-wanted`

**Acceptance Criteria:** MITM rehberi yok; güvenli kontrol listesi var.

**Safety Checklist Type:** Type B

---

## Issue 9

**Issue Title:** [NOTE] Digital Signatures and Code Signing: Defensive Importance

**Repository:** crypto-privacy-lab

**Content Type:** defensive-note

**Trust Tier:** Tier 2

**Wave:** Wave 2

**Goal:** Digital signatures ve code signing kavramlarının integrity/authenticity açısından önemini açıklamak.

**Scope:** Signing, verification, code signing key protection, release integrity.

**Out of Scope:** Key theft, signing bypass, malware signing tactics.

**Required Output:** `digital-signatures/digital-signatures-code-signing-defensive-importance.md`

**Required Sections:** Context, What It Protects, Key Protection Notes, Common Mistakes, Sources.

**Source Requirements:** En az 2 kaynak.

**Research Method Notes:** Signing abuse değil, savunma ve bütünlük dili.

**Suggested Source Types to Verify:** NIST, Microsoft code signing docs, Sigstore documentation.

**Labels:** `wave-2`, `tier-2`, `digital-signatures`, `defensive-note`, `help-wanted`

**Acceptance Criteria:** Abuse workflow yok; key protection vurgusu var.

**Safety Checklist Type:** Type B

---

# WAVE 3

## Issue 10

**Issue Title:** [AWARENESS] Post-Quantum Migration Planning Without Panic

**Repository:** crypto-privacy-lab

**Content Type:** awareness-note

**Trust Tier:** Tier 3

**Wave:** Wave 3

**Goal:** Post-quantum cryptography riskini panik dili olmadan, crypto agility ve migration readiness açısından açıklamak.

**Scope:** PQC awareness, crypto inventory, migration planning, hybrid transition awareness.

**Out of Scope:** “Her şey kırıldı” iddiası, unsupported fear claims, implementation guide for experimental crypto.

**Required Output:** `post-quantum-awareness/post-quantum-migration-planning-without-panic.md`

**Required Sections:** Context, What Is Changing, What Is Not Changing, Migration Readiness, Sources.

**Source Requirements:** En az 3 kaynak.

**Research Method Notes:** Abartı yok; kaynaklı ve ölçülü dil.

**Suggested Source Types to Verify:** NIST PQC resources, ENISA PQC guidance, CISA PQC roadmap.

**Labels:** `wave-3`, `tier-3`, `post-quantum-awareness`, `crypto-sensitive`, `maintainer-review-required`

**Acceptance Criteria:** Panik dili yok; crypto agility net; maintainer review.

**Safety Checklist Type:** Type B

---

## Issue 11

**Issue Title:** [SENSITIVE] Key Leakage Prevention for Product Teams

**Repository:** crypto-privacy-lab

**Content Type:** crypto-sensitive-note

**Trust Tier:** Tier 3

**Wave:** Wave 3

**Goal:** Key leakage riskini ürün ekipleri açısından önleme ve response perspektifiyle açıklamak.

**Scope:** Key storage mistakes, rotation planning, detection, revocation, incident response at high level.

**Out of Scope:** Gerçek leaked key örneği, dork listesi, abuse workflow, active exploitation.

**Required Output:** `key-management/key-leakage-prevention-product-teams.md`

**Required Sections:** Context, Common Risk Categories, Prevention Controls, Response Principles, Sources.

**Source Requirements:** En az 3 kaynak.

**Research Method Notes:** Gerçek secret formatı veya keşif yöntemi verilmez.

**Suggested Source Types to Verify:** OWASP Secrets Management, GitHub secret scanning docs, cloud KMS docs.

**Labels:** `wave-3`, `tier-3`, `key-management`, `crypto-sensitive`, `maintainer-review-required`

**Acceptance Criteria:** Abuse yok; prevention/response dili; maintainer review.

**Safety Checklist Type:** Type B

---

## Issue 12

**Issue Title:** [SENSITIVE] Cryptographic Failure Case Studies: Defensive Lessons Only

**Repository:** crypto-privacy-lab

**Content Type:** crypto-sensitive-note

**Trust Tier:** Tier 3

**Wave:** Wave 3

**Goal:** Kriptografik hata örneklerinden savunma dersi çıkarmak; saldırı/kırma rehberine dönüşmeden risk sınıflarını açıklamak.

**Scope:** High-level failure categories: weak randomness, bad key storage, insecure defaults, broken protocols at concept level.

**Out of Scope:** Exploit reproduction, attack math walk-through, real target details, code-level breaking guide.

**Required Output:** `encryption-basics/cryptographic-failure-case-studies-defensive-lessons.md`

**Required Sections:** Context, Failure Categories, Defensive Lessons, What This Deliberately Excludes, Sources.

**Source Requirements:** En az 3 kaynak.

**Research Method Notes:** Case study savunma odaklı ve yüksek seviyede kalmalı.

**Suggested Source Types to Verify:** NIST, academic retrospectives, OWASP, well-documented public postmortems.

**Labels:** `wave-3`, `tier-3`, `crypto-sensitive`, `maintainer-review-required`

**Acceptance Criteria:** Reproduction yok; breaking guide yok; maintainer review.

**Safety Checklist Type:** Type B
