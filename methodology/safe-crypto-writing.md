# Safe Crypto Writing Rules

Bu dosya, Crypto Privacy Lab içeriklerinin nasıl güvenli, doğru ve sorumlu yazılacağını tanımlar.

## Core Principle

Kriptografi içerikleri “nasıl kırılır?” değil, “güvenli ve kabul görmüş yöntemler nasıl doğru kullanılır?” sorusuna cevap vermelidir.

## What This Content Deliberately Excludes

Her crypto/privacy içeriğinde gerekiyorsa açıkça şu sınırlar belirtilmelidir:

- Gerçek secret/key/token/password/credential yok
- Hash cracking veya password list yok
- Breaking guide veya saldırı workflow yok
- Zayıf kriptonun uygulanabilir kötüye kullanım adımı yok
- “Kendi algoritmanı yaz” yönlendirmesi yok
- Hukuki uyumluluk garantisi yok
- Post-quantum panik dili yok

## Safe Framing Examples

### Hashing

Unsafe:

> Şu hash’i şu araçla kırabilirsiniz.

Safe:

> Password hashing, offline guessing riskine karşı yavaş ve tercihen memory-hard algoritmalarla tasarlanmalıdır. Argon2id, bcrypt ve PBKDF2 gibi kabul görmüş yaklaşımlar kaynaklı şekilde karşılaştırılabilir.

### Encryption

Unsafe:

> Kendi basit şifreleme algoritmanızı şöyle yazın.

Safe:

> Ürün ekipleri kendi kripto algoritmalarını tasarlamamalı; güvenilir kütüphaneler ve kabul görmüş modlar kullanılmalıdır.

### Key Management

Unsafe:

> API key’i örnekte şu formatla yazın.

Safe:

> Örneklerde gerçek key/token kullanılmamalıdır. Placeholder kullanın: `EXAMPLE_API_KEY_DO_NOT_USE`.

### Privacy-by-Design

Unsafe:

> Bu tasarım KVKK/GDPR uyumludur.

Safe:

> Bu tasarım data minimization ve retention kontrolü gibi privacy-by-design prensiplerini destekler. Hukuki uyumluluk ayrıca değerlendirilmelidir.

### Post-Quantum

Unsafe:

> Kuantum bilgisayarlar tüm kriptoyu kırdı.

Safe:

> Post-quantum risk, crypto agility ve migration readiness açısından takip edilmelidir. Panik dili yerine planlama dili kullanılmalıdır.

## Required Reviewer Questions

- İçerik gerçek secret veya credential içeriyor mu?
- İçerik hash cracking veya breaking workflow’a dönüşüyor mu?
- İçerik “kendi kriptonu yaz” mesajı veriyor mu?
- Güvenlik seviyesi abartılmış mı?
- Hukuki uyumluluk garanti edilmiş mi?
- Kaynaklar güvenilir mi?
- Contributor Rights / No Ownership Claim onaylanmış mı?
