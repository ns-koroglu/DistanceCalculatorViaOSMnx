# Şehirdeki Noktalara Mesafe Hesaplama

## Harita İndirme ve Kontrol

### Harita İndirme
OSMnx ile merkez noktasının 10 km çevresindeki yol haritası indirilir.

### Ağ Yapısı
Harita, yolları ve kavşakları bir ağ gibi gösterir.

### Bağlantı Kontrolü
Haritadaki yolların birbirine bağlı olup olmadığı kontrol edilir.

---

## Noktaları Yerleştirme ve Mesafe Hesaplama

### Noktaları Yerleştirme
Merkez ve 240 noktanın haritadaki en yakın yol noktaları bulunur.

### Mesafe Hesaplama
Merkezden her noktaya, yolları takip ederek mesafe hesaplanır.

### Hata Kontrolü
Mesafe hesaplanamazsa (yol yoksa), hata mesajı yazılır.

---

## Kodun Çıktısı

Aşağıdaki tablo, hastaneden belirli evlere olan mesafeleri (metre cinsinden) göstermektedir. Enlem ve boylam bilgileri ile birlikte, her evin sırası ve ID numarası da belirtilmiştir. Mesafe hesaplamaları sırasında karşılaşılan hatalar da ayrıca not edilmiştir.

| Sıra | No    | Enlem     | Boylam    | Mesafe (metre) |
|------|-------|-----------|-----------|----------------|
| 1    | 21491 | 38.709714 | 35.552545 | 2500           |
| 2    | 32221 | 38.694468 | 35.549217 | 1800           |
| 3    | 32551 | 38.686098 | 35.544537 | 1200           |
| 4    | 45112 | 38.715225 | 35.561892 | 3100           |
| 5    | 29876 | 38.678911 | 35.570119 | 800            |

### Hata Örnekleri:
- **"Hata - Sıra 10":** Listedeki 10. sıradaki evin konumuna ulaşılırken bir sorun yaşandığını gösterir. Örneğin, evin koordinatları hatalı veya eksik olabilir.
- **"No 48815: Hedefe yol yok":** 48815 ID'li eve harita üzerinde bir yol bulunamadığı anlamına gelir. Bu, evin çok uzak bir konumda olmasından veya harita verisinde eksiklik olmasından kaynaklanabilir.

---

## Sorular ve Özet

### Bu kod başka şehirlerde çalışır mı?
Evet, koordinatları değiştirirseniz herhangi bir şehirde çalışabilir.

### Hatalar neden çıkar?
Yol yoksa, harita eksikse veya noktalar arasında bağlantı kurulamazsa hata verebilir.

### Kod ne kadar hassas ölçüm yapabilir?
Haritanın kalitesine bağlı olarak metre cinsinden oldukça hassas ölçümler yapabilir.

### Büyük şehirlerde performans nasıl olur?
Büyük şehirlerde harita daha karmaşık olacağından, hesaplama süresi artabilir.
