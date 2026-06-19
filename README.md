# Crypto Privacy Lab

Uygulamalı kriptografi, güvenli veri saklama, anahtar yönetimi ve privacy-by-design konularını geliştirici dostu ve savunma odaklı ele alan açık kaynak araştırma deposu.

Bu repo kriptografiyi “sihirli güvenlik” gibi değil, doğru kullanılan bir mühendislik disiplini olarak ele alır. Amaç; geliştiricilerin, güvenlik araştırmacılarının ve ürün ekiplerinin güvenli yöntemleri doğru seçmesine, yanlış güvenlik algısından kaçınmasına ve mahremiyet odaklı ürün tasarlamasına yardımcı olmaktır.

## Bu Repo Ne Yapar

| Klasör | Odak |
|---|---|
| `encryption-basics/` | Simetrik/asimetrik şifreleme, doğru kullanım prensipleri |
| `hashing-passwords/` | Hashing vs encryption, Argon2id/bcrypt/PBKDF2, salt/pepper |
| `key-management/` | Key lifecycle, generation, rotation, storage, KMS/HSM mantığı |
| `digital-signatures/` | Dijital imza, kod imzalama, integrity ve authenticity |
| `tls-secure-communication/` | TLS, HTTPS, certificate validation ve güvenli iletişim |
| `privacy-by-design/` | Data minimization, retention, local-first design, PII handling |
| `secure-storage/` | Local storage, encrypted vault, secrets at rest, mobile/app storage |
| `post-quantum-awareness/` | Crypto agility, post-quantum migration readiness, doğru risk dili |

## Bu Repo Ne Değildir

Bu repo hash cracking rehberi, parola listesi deposu, credential abuse rehberi, şifre kırma aracı, “kendi kriptonu yaz” yönlendirmesi veya gerçek secret/key/token örnekleri deposu değildir.

Çalışan saldırı akışı, cracking workflow, gerçek credential, gerçek key/token, sızdırılmış veri, exploit/PoC veya zayıf kriptonun uygulanabilir kötüye kullanım adımları kabul edilmez. Detaylar için `CONTENT_POLICY.md`.

Temel çizgi: **Do not write your own crypto. Learn how to use trusted cryptographic building blocks safely.**

## Trust Tier Mantığı

| Tier | İçerik | Açıklama |
|---|---|---|
| Tier 1 | Kavramsal açıklamalar, geliştirici checklistleri, güvenli kullanım prensipleri | Katkıcı dostu, düşük risk |
| Tier 2 | Secure storage, key management, TLS, privacy design notes | Daha dikkatli kaynak ve review gerekir |
| Tier 3 | Key leakage, cryptographic failure, post-quantum migration risk, incident-style analiz | Crypto-sensitive; maintainer review zorunlu |

## Wave Sistemi

Wave 1 güvenli başlangıç issue’larıdır. Wave 2 ürün güvenliği ve privacy tasarımına geçer. Wave 3 ise yanlış yazıldığında kötüye kullanım veya yanlış güvenlik algısı doğurabilecek hassas konuları içerir.

Detaylar: `docs/issue-cards/crypto-privacy-lab-issues-v1.md`.

## Diğer Tamga Repolarıyla Sınır

- `siber-savunma-atlas`: genel siber risk, sektör notları ve savunma dersleri.
- `malware-threat-analysis`: malware davranış kalıpları ve tespit notları.
- `ai-safety-lab`: AI ürün güvenliği, agent güvenliği ve LLM safety.
- `crypto-privacy-lab`: kriptografi, mahremiyet ve güvenli veri tasarımı.

## Nasıl Katkı Verilir

Bkz. `CONTRIBUTING.md`. İlk görevler için `docs/issue-cards/crypto-privacy-lab-issues-v1.md` dosyasına bakın.

## Contributors

Katkı sağlayanlar bu listede ve ilgili Pull Request geçmişinde görünür. Liste manuel güncellenir; en güncel ve kalıcı kayıt için repo'nun PR geçmişine bakın.

## Lisans ve Haklar

Bu repodaki tüm içerik CC BY 4.0 lisansı ile yayınlanır — bkz. `LICENSE`. Tamga'nın marka, yönetişim ve türev ürün geliştirme hakları için bkz. `NOTICE.md`.

Open-source digital security research, from Türkiye.
