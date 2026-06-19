# Content Policy

Crypto Privacy Lab, kriptografi ve mahremiyet konularını savunma, doğru kullanım ve güvenli ürün tasarımı açısından ele alır.

## Allowed Content

- Encryption vs hashing gibi temel kavram açıklamaları
- Güvenli kripto kullanım prensipleri
- Password hashing best-practice notları
- Key management lifecycle açıklamaları
- Secure storage checklistleri
- TLS ve certificate validation farkındalığı
- Digital signature ve code signing savunma notları
- Privacy-by-design prensipleri
- Post-quantum awareness ve crypto agility notları

## Prohibited Content

Bu repo aşağıdaki içerikleri kabul etmez:

- Gerçek secret, private key, API token, parola, credential veya leaked data
- Hash cracking workflow, parola listesi, credential abuse rehberi
- Şifre kırma, saldırı veya bypass adım adım akışı
- Exploit/PoC veya çalışan kötüye kullanım komutu
- “Kendi kriptonu yaz” yönlendirmesi
- Bilerek zayıf kripto yöntemi önerisi
- Gerçek kuruma/kişiye ait hassas veri örneği
- Hukuki uyumluluk garantisi veya avukatlık tavsiyesi gibi yazılmış KVKK/GDPR iddiaları
- Post-quantum konusunda panik, abartı veya “her şey kırıldı” dili

## Safe Language Rule

Yazılar “nasıl kırılır?” değil, “güvenli nasıl tasarlanır?” sorusuna cevap vermelidir.

Kötü örnek:

> Bu hash’i kırmak için şu aracı şu şekilde kullanın.

Doğru yaklaşım:

> Password hashing, offline guessing riskine karşı yavaş ve memory-hard algoritmalarla tasarlanmalıdır. Ürün ekipleri Argon2id/bcrypt/PBKDF2 gibi kabul görmüş yaklaşımları değerlendirmelidir.

## Privacy Notice

KVKK, GDPR veya benzeri çerçeveler yalnızca genel privacy-by-design prensipleri bağlamında ele alınır. Bu repo hukuki tavsiye sağlamaz.
