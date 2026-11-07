# Bırakma Protokolü

Sigara bırakma takip uygulaması. Tek sayfa, sunucu gerektirmez, çevrimdışı çalışır (PWA).

## Özellikler
- Bırakma sayacı, temiz gün serisi, cebimde kalan para
- Sağlık iyileşme çizelgesi (saat bazlı ilerleme çubuğu)
- Her kriz için ayrı tetikleyici ve çözüm kaydı
- Acil fren: 3 dakikalık nefes sayacı ve titreşim (Android)
- Sigara günlüğü: neden, saat ve istek/alışkanlık analizi, yapay zekâ ile paylaşım metni
- JSON yedekleme ve geri yükleme

## GitHub Pages ile yayınlama
1. Bu klasördeki tüm dosyaları reponun ana dizinine yükle.
2. Settings → Pages → Source: `main` dalı, `/ (root)`.
3. Birkaç dakika sonra `https://KULLANICI.github.io/REPO/` adresinde açılır.

## Telefona yükleme
- **Android (Chrome):** menü → "Ana ekrana ekle" / "Uygulamayı yükle".
- **iPhone (Safari):** Paylaş → "Ana Ekrana Ekle".

## Veriler
Tüm veriler yalnızca o cihazdaki tarayıcıda (localStorage) saklanır, hiçbir yere gönderilmez.
Tarayıcı verisi silinirse kayıtlar gider; düzenli olarak Geçmiş sekmesinden "Verilerimi Yedekle" ile yedek al.
Farklı adres veya cihaza geçerken yedeği "Yedekten Geri Yükle" ile aktar.

## Güncelleme
`index.html` veya başka bir dosyayı değiştirirsen `sw.js` içindeki `CACHE` sürümünü artır (`birak-v2`), yoksa eski sürüm önbellekten gelmeye devam eder.

## Not
Sağlık çizelgesi genel popülasyon verilerine dayanır ve tıbbi tavsiye değildir. Nikotin replasmanı ve ilaçlar için doktor veya eczacıya danış.
