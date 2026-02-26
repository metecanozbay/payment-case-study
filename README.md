# payment-case-study

Payment domain odaklı Business Analysis mini-case çalışmalarım.

Bu repo; kartlı ödeme süreçlerini (özellikle 3D Secure ve Authorization akışları) iş analizi perspektifiyle ele alan örnek çıktıları içerir.

---

## Conceptual Case Study Note

Bu repo, payment domain’e yönelik kavramsal (conceptual) bir Business Analysis case study çalışmasıdır.

Akış ve iş kuralları; EMVCo 3DS 2.x prensipleri, ISO 8583 authorization mantığı ve Visa/Mastercard publicly available dokümantasyonları referans alınarak modellenmiştir.

Herhangi bir kurumun gerçek production sistemini temsil etmez.

---

## Case 1 – 3D Secure (3DS)

**Medium yazısı:**  
https://medium.com/@metecanozbay/3d-secureun-görünmeyen-dünyasına-kısa-bir-yolculuk-5d816dcabe1d

### Bu case kapsamında:

- 3DS karar noktaları (XOR / OR mantığı)
- Başarılı / başarısız / timeout senaryoları
- İş kuralları (business rules)
- Edge-case düşüncesi
- Authorization’a geçiş koşulları

---

## İçerik Yapısı

Yakında eklenecek:

- 3DS akış diyagramı
- Authorization süreci
- Basit ER veri modeli
- Business rules dokümanı
- Test senaryoları

---

## Amaç

Ödeme sistemleri tarafındaki saha deneyimimi, yapılandırılmış Business Analysis çıktılarıyla somutlaştırmak.
