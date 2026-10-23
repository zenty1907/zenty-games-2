# Zenty Place

Zenty Place, gerçek dünya haritası üzerine piksel yerleştirme fikrinden esinlenen mobil uyumlu bir web prototipidir.

## Mevcut özellikler
- OpenStreetMap tabanlı sürüklenebilir ve yakınlaştırılabilir dünya haritası
- Şehir/ülke arama (OpenStreetMap Nominatim)
- 16 renkli palet ve haritada piksel bırakma
- En fazla 5 piksel hakkı; 30 saniyede bir hak yenilenmesi
- Tarayıcıda saklanan pikseller ve kişisel istatistikler
- Bu cihazda topluluk oluşturma, yerel takım kodu ve katkı sayacı
- Mobil ve masaüstü uyumlu arayüz

## Önemli: mevcut sürümün sınırları
Bu dağıtım **tek tarayıcıda çalışan bir prototiptir**, henüz çok kullanıcılı çevrimiçi servis değildir. Pikseller, topluluklar ve sıralama `localStorage` içinde tutulur; diğer ziyaretçilerle paylaşılmaz. Topluluk kodları başka cihazlarda çalışmaz. Sayfa bir sunucuya bağlanmış gibi davranmaz.

Gerçek Wplace benzeri çok oyunculu sürüm için ayrıca şunlar gerekir:
1. Supabase veya benzeri bir backend projesi (Postgres veritabanı ve Realtime).
2. Sunucu tarafında doğrulanan piksel hakkı/cooldown işlemi ve rate limiting; istemci saatine güvenilmemeli.
3. Kullanıcı kimliği ve topluluk üyelikleri; RLS politikalarıyla erişim kontrolü.
4. Pikseller için koordinat/ızgara anahtarı, kalıcı kayıt ve çakışma politikası.
5. Realtime yayınları, topluluklar, raporlama/moderasyon ve spam koruması.
6. Gerçek hesaplar/kimlik doğrulama ve yönetici araçları.

Backend erişimi ve yapılandırması olmadan GitHub Pages üzerinde yalnızca frontend ile tüm kullanıcılar arasında güvenilir ortak durum oluşturmak mümkün değildir. Gizli servis anahtarlarını hiçbir zaman tarayıcı koduna koymayın.

## Yayınlama
GitHub Pages ayarı: **Settings → Pages → Deploy from a branch → main → /(root)**.
Site: https://zenty1907.github.io/zenty-games-2/

## Harita ve hizmetler
- Harita verisi © OpenStreetMap contributors: https://www.openstreetmap.org/copyright
- Harita döşemeleri ve arama hizmeti üçüncü taraf kullanım politikalarına tabidir. Yoğun kullanımda uygun sağlayıcı veya kendi barındırma seçeneği değerlendirilmelidir.

## Lisans
Bu proje bağımsız bir Zenty prototipidir; Wplace veya Reddit ile bağlantılı değildir. Üçüncü taraf markaları ve hizmetleri kendi lisans ve koşullarına tabidir.
