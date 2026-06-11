# Taschte – Café & Frühstück Website

İki dilli (Almanca/İngilizce) statik web sitesi — **Taschte Cafe und Frühstück**, Engerstraße 41, 33824 Werther (Westfalen).

## Dosyalar

| Dosya | Açıklama |
|---|---|
| `index.html` | Ana sayfa (hero, hikaye, menü, galeri, yorumlar, iletişim + harita) |
| `css/style.css` | Tüm tasarım sistemi |
| `js/main.js` | DE/EN dil değiştirici (tüm çeviriler burada), mobil menü, scroll animasyonları |
| `impressum.html` | Yasal künye — **yayınlamadan önce doldurulmalı** (Almanya'da zorunlu) |
| `datenschutz.html` | Gizlilik bildirimi taslağı — **yayınlamadan önce kontrol edilmeli** |

## Çalıştırma

Build gerekmez. Yerelde görüntülemek için:

```bash
cd /Users/emrahidman/Projects/Taschte
python3 -m http.server 8000
# http://localhost:8000
```

Yayınlamak için klasörü Netlify, Vercel, GitHub Pages veya herhangi bir hosting'e sürükleyip bırakmak yeterli.

## Yayınlamadan önce yapılacaklar (ÖNEMLİ)

1. ~~**Fotoğraflar:**~~ ✅ Tamamlandı — sitedeki tüm görseller `images/` klasöründeki gerçek kafe fotoğraflarıyla değiştirildi (optimize edildi; orijinaller `images/originals/` içinde).
2. ~~**Fiyatlar:**~~ ✅ Gerçek menü fiyatlarıyla güncellendi (Haziran 2026). Fiyatı doğrulanmamış iki kart (Sucuk mit Rührei, Hausgemachte Kuchen) fiyatsız gösteriliyor — fiyat öğrenilince eklenebilir. Classic Frühstück (14,50 €) ve Veganes Frühstück (17,90 €) menüde var ama uygun fotoğraf olmadığı için sitede öne çıkarılmadı.
3. ~~**Çalışma saatleri:**~~ ✅ Sahibi onayladı: Pazartesi–Pazar 08:00–17:00 olarak güncellendi.
4. ~~**Impressum & Datenschutz:**~~ ✅ Tamamlandı. Impressum sahibinin nihai metniyle (sorumlu: Selvi Kaptan); Datenschutz gerçek teknik duruma göre yazıldı (çerez/izleme yok, Google Maps + Google Fonts + Gmail). Fontlar artık yerel barındırılıyor (`fonts/` içinde woff2; Google sunucularına istek yok) — Datenschutz'taki Google Fonts bölümü buna göre kaldırıldı.
5. **Alan adı:** `index.html` içindeki `canonical` ve JSON-LD `url` alanlarını gerçek alan adınızla değiştirin (şu an `taschte-cafe.de` varsayıldı).
6. **Google Business Profile:** Siteyi yayınlayınca Google İşletme Profili'ne web sitesi olarak ekleyin — yerel aramada görünürlük için en etkili adım.

## Görünürlük (SEO) için yapılanlar

- `CafeOrCoffeeShop` JSON-LD yapılandırılmış veri (adres, saatler, telefon, mutfak türü) → Google'da zengin sonuç
- Almanca meta title/description, anahtar kelimeler ("Frühstück Werther", "Türkisches Frühstück")
- Mobil öncelikli, hızlı, tek sayfalık tasarım; `loading="lazy"` görseller
- Tıklanabilir telefon (`tel:`), sabit "Reservieren" butonu (mobil), Google Maps yol tarifi
- Instagram'a güçlü yönlendirme (sosyal kanıt döngüsü)
