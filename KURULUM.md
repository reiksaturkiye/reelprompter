# ReelPrompter – Kurulum Rehberi (Android)

Uygulama bir **PWA** (Progressive Web App): telefona ana ekran simgesiyle kurulur, tam ekran açılır, internet olmadan da çalışır (AI arka plan ilk kullanımda modeli indirir, sonra önbellekten çalışır). Kamera ve mikrofon için uygulamanın **https** adreste yayınlanması gerekir — bunun için ücretsiz GitHub Pages kullanıyoruz.

## Adım 1 — GitHub hesabı (5 dk, ücretsiz)
1. https://github.com/signup adresinden hesap aç.

## Adım 2 — Dosyaları yükle
1. Sağ üstte **+** → **New repository**.
2. Repository name: `reelprompter` · **Public** seç · **Create repository**.
3. Açılan sayfada **"uploading an existing file"** bağlantısına tıkla.
4. Zip'ten çıkan **tüm dosyaları** (index.html, manifest.json, sw.js, 3 adet .png) sürükle-bırak → **Commit changes**.

## Adım 3 — Yayına al
1. Repoda **Settings** → soldan **Pages**.
2. *Source*: **Deploy from a branch** · *Branch*: **main** / **(root)** → **Save**.
3. 1–2 dk sonra adresin hazır olur: `https://KULLANICIADIN.github.io/reelprompter/`

## Adım 4 — Telefona yükle
1. Android telefonda **Chrome** ile yukarıdaki adresi aç.
2. Sağ üst **⋮** menü → **Uygulamayı yükle** (veya **Ana ekrana ekle**).
3. Ana ekranda **ReelPrompter** simgesi oluşur. Açınca kamera ve mikrofon izni ver.

## (İsteğe bağlı) Adım 5 — Gerçek APK / Play Store
1. https://www.pwabuilder.com adresine GitHub Pages adresini yaz → **Start**.
2. **Package for stores → Android** → **Generate**. İndirilen zip'te imzalı `.apk` (telefona doğrudan kurulur) ve `.aab` (Play Store'a yüklenir) bulunur.
3. Play Store için Google Play Console hesabı gerekir (tek seferlik 25 USD).

## Güncelleme
`index.html` dosyasını değiştirip GitHub'a yeniden yükle. `sw.js` içindeki `VERSION` değerini artırırsan (ör. `rp-v2`) telefonlar yeni sürümü hemen alır.

## Kullanım ipuçları
- **Süre ayarı:** Ayarlar › Süre › "Hedef video süresi" gir → hız otomatik hesaplanır.
- **Sesle kaydırma:** Mikrofon düğmesi. Sen okudukça yazı ilerler, durursan bekler. (Chrome gerekir; bazı telefonlarda kayıt sırasında mikrofonu paylaşamayabilir — o durumda sabit hız modunu kullan.)
- **AI arka plan:** İnsan simgeli düğme. Bulanık / renk / hazır ortam / kendi fotoğrafın (ör. satılık evin salonu).
- **Logo ve alt bant:** Ayarlar › Logo. Kayda gömülür, filigran yok.
- **Göz teması:** Yazı alanını küçük tut (Yazı alanı yüksekliği %30–40), böylece gözün kameraya yakın kalır.
- **Kumanda:** Bluetooth sunum kumandası/klavye: Boşluk = başlat/duraklat, ↑/↓ = hız, Enter = kayıt.
