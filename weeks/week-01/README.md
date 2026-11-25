<!-- Bu dosya real-app-lab/scripts/build_readme.py ile üretilir, elle düzenlemeyin. -->

# Hafta 1

**Detaylı anlatım:** Yakında

> Bu çalışma Mobbin ya da incelenen uygulamaların sahipleriyle bağlantılı değildir. Markalar sahiplerine aittir. Yorumlar akışlara bakılarak yapılmıştır; teknik dersler çıkarımdır, uygulamaların gerçek altyapısını göstermez. Ekran görüntüleri paylaşılmaz; Mobbin linkleri üyelik isteyebilir.

## AllTrails

**[Mobbin'de tüm akışlar ↗](https://mobbin.com/apps/all-trails-ios-66ac61f7-f9ea-4c45-b512-b2fadf7e027b/9d2ea5c9-3431-4fd3-9098-df867890782a/flows)**

- **Ne yapıyor:** Doğa yürüyüşü, bisiklet ve koşu rotalarını keşfettiren; rotayı indirip şebeke yokken de takip ettiren harita uygulaması.
- **Kimin için:** Hafta sonu yürüyüşçüleri, milli park gezginleri, patika koşucuları, dağ bisikletçileri.
- **Ana döngü:** Rota keşfet → indir → yürü → yorum ve fotoğraf ekle → sıradaki kullanıcı bu veriye güvenir.
- **Gelir modeli:** Freemium: Free, Plus ve Peak katmanları; hediye kartı.

### Önemli akışlar

1. **[İlk açılış](https://mobbin.com/flows/4c552a20-55b9-43f4-9627-97cccc7bd74f)**: Uygulamanın değerini ilk dakikada nasıl anlattığını gösterir.
   - _Teknik ders (çıkarım):_ Onboarding'i ayrı bir adım makinesi olarak kurgula.
2. **[Onboarding paywall](https://mobbin.com/flows/b74a637a-9986-4f12-ae5a-9fe2297e74fd)**: Ücretli pakete ilk davet burada.
   - _Teknik ders (çıkarım):_ Satın alma ve yetki (entitlement) durumunu tek bir yerden yönet.
3. **[Rota detayı](https://mobbin.com/flows/33d54cbf-bd8c-4100-afb8-62d544b1c5a6)**: Ürünün merkezi ekranı: karar ve çoğu aksiyon buradan başlar.
   - _Teknik ders (çıkarım):_ Yoğun detay ekranını bağımsız bölümlere ayır.
4. **[Çevrimdışı harita indirme](https://mobbin.com/flows/327ef1db-14ba-4733-9bea-359e74603f38)**: Dağda sinyal olmaması sorununu çözen temel özellik.
   - _Teknik ders (çıkarım):_ Harita parçaları için indirme kuyruğu ve yerel depo gerekir.
5. **[Navigasyon ve rotayı bitirme](https://mobbin.com/flows/0e8b3765-acf9-46a0-8c75-7ac38d7fe42e)**: Uygulamanın asıl kullanım anı.
   - _Teknik ders (çıkarım):_ Arka planda konum takibi ve pil tüketimi ana mühendislik konusu.
6. **[Yürüyüş sonrası yorum](https://mobbin.com/flows/a1e9d86f-92d8-491f-b716-bb2329a3b514)**: Topluluk verisi döngüsünü besleyen adım.
   - _Teknik ders (çıkarım):_ Katkıyı kullanıcının en istekli olduğu anda iste.
7. **[Park damgası toplama](https://mobbin.com/flows/4fa85fa7-fca4-4e4f-be12-d8305ad48408)**: Geri dönmek için oyunlaştırma nedeni.
   - _Teknik ders (çıkarım):_ Rozet kurallarını istemciden ayrı, veriyle tanımla.

## Muse

**[Mobbin'de tüm akışlar ↗](https://mobbin.com/apps/muse-ios-8e6481b3-fcd5-43b4-a9e6-abeea1fb0cdc/cecf076d-e88c-452b-bb7e-77c311324106/flows)**

- **Ne yapıyor:** Sohbetin ötesine geçen kişisel AI ajanı: Gmail'e bağlanır, uzak tarayıcıda iş yapar, hedef takip eder ve çıktı üretir.
- **Kimin için:** Yoğun bilgi çalışanları, kurucular, içerik üreticileri, erken benimseyenler.
- **Ana döngü:** Hesaplarını bağla → ajana iş ver → onayla → sonucu Feed ve Library'de gör.
- **Gelir modeli:** Abonelik (Muse Maximum) ve ek token satışı.

### Önemli akışlar

1. **[İlk açılış](https://mobbin.com/flows/e5a8e1bd-c38b-4775-b4bd-bf713e3afe38)**: Form yerine ajanla tanışarak kurulum.
   - _Teknik ders (çıkarım):_ Uzun onboarding'de yarıda kalan durumu sakla.
2. **[Gmail bağlama](https://mobbin.com/flows/d3852bc8-f6c1-4f0d-b3e2-4dd0dcf2aed3)**: Ajan kullanıcıyı tanımaya burada başlar; boş ekran sorunu azalır.
   - _Teknik ders (çıkarım):_ OAuth token'ları sunucu tarafında ve en az yetkiyle tutulmalı.
3. **[Uzak tarayıcı](https://mobbin.com/flows/bb0ee698-1ca6-4ab8-9c44-a9a3b500dec9)**: Konuşmadan aksiyona geçişin görüldüğü an.
   - _Teknik ders (çıkarım):_ Uzun süren ajan işini canlı durum akışıyla göster.
4. **[Ödeme onayı](https://mobbin.com/flows/d0feac4a-3899-46e0-84fc-95b87887ffc3)**: Ajana para harcatırken güveni sağlayan adım.
   - _Teknik ders (çıkarım):_ Geri dönüşü olmayan işlemler insan onayından geçsin.
5. **[Hedef oluşturma](https://mobbin.com/flows/5aaa272c-b4a4-4337-a378-ba9e9e551158)**: Sohbeti kalıcı takibe çevirir.
   - _Teknik ders (çıkarım):_ Hedefi sohbet mesajı değil, ayrı bir veri modeli yap.
6. **[Çıktı yayınlama](https://mobbin.com/flows/fbf862ce-d9dc-4115-9388-fd92be8a5857)**: Üretilen işi dışarı taşır; büyüme kanalı olabilir.
   - _Teknik ders (çıkarım):_ Yayınlamada görünürlük ve geri çekme kontrolü gerekir.
7. **[Ek token satın alma](https://mobbin.com/flows/2ab35844-ba45-4888-b257-2fc3994a791a)**: Ağır kullanımın maliyetini gelire bağlar.
   - _Teknik ders (çıkarım):_ Kredi bakiyesini sunucuda defter (ledger) olarak tut.

## stoic.

**[Mobbin'de tüm akışlar ↗](https://mobbin.com/apps/stoic-ios-621f0be7-8046-45cd-b667-97add5f9c3c7/fd166e24-39ab-43ac-96ad-1095935c93fe/flows)**

- **Ne yapıyor:** Sabah ve akşam rutinleriyle günlük tutturan; ses, çizim ve AI mentorla destekleyen zihinsel iyi oluş uygulaması.
- **Kimin için:** Kendini tanımak isteyenler, odaklanma sorunu yaşayanlar, boş sayfada tıkananlar.
- **Ana döngü:** Check-in yap → günlük yaz → AI analizi al → trendlerini gör → ertesi gün dön.
- **Gelir modeli:** İki katmanlı abonelik (Premium, Premium Plus/AI) ve hediye abonelik.

### Önemli akışlar

1. **[Premium paywall](https://mobbin.com/flows/dcfb6b10-37f2-4bd1-ad76-c34d61c78a69)**: İki paketin nasıl sunulduğunu gösterir.
   - _Teknik ders (çıkarım):_ Katmanlı abonelikte yetkileri özellik bazında kontrol et.
2. **[Günlük check-in kurulumu](https://mobbin.com/flows/64fe4566-9666-4303-87a5-0c5905935890)**: Alışkanlığı kullanıcıya göre şekillendirir.
   - _Teknik ders (çıkarım):_ Check-in adımlarını yapılandırılabilir veri olarak tasarla.
3. **[Sesli günlük](https://mobbin.com/flows/74ec906f-380a-4080-874c-d769f1878f3f)**: Yazma zorluğunu azaltır.
   - _Teknik ders (çıkarım):_ Kayıt, izin ve yerel dosya yönetimi ayrı ele alınmalı.
4. **[AI derin analiz](https://mobbin.com/flows/ce487bc0-91eb-461d-81ca-db1e2d74f6d7)**: Yazılanı geri bildirime çeviren AI özelliği.
   - _Teknik ders (çıkarım):_ Hassas veride açık rıza ve minimum veri gönderimi şart.
5. **[Trendler](https://mobbin.com/flows/fec9e20b-3070-4306-96fd-5d42bf18ab84)**: Biriken veriyi görünür kılar; geri dönme nedeni.
   - _Teknik ders (çıkarım):_ Özet metrikleri önceden hesaplayıp sakla.
6. **[Stoic Shield](https://mobbin.com/flows/bd010f3e-40ba-44be-b97a-3aa2df04f6b3)**: Günlük yazmayı uygulama engellemeye bağlayan en ayırt edici fikir.
   - _Teknik ders (çıkarım):_ iOS'ta Screen Time API'leri ve özel izin gerektirir.
7. **[Alıntı paylaşma](https://mobbin.com/flows/20aa8528-6cce-4cc0-a747-3049ac6b4264)**: Basit bir organik yayılma kancası.
   - _Teknik ders (çıkarım):_ Paylaşım görselini cihazda üret.
