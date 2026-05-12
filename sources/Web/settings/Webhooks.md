# Webhooks

## 1. Webhooks

![Endpoint Listesi.png](http://docs.filarch.com/media/uploads/Endpoint_Listesi.png) Şekil 1.1 – Webhooks Sayfası

Sol menüden Webhooks bağlantısına tıklandığında webhooks sayfasına yönlendirilir. Sayfa başlığının yanında yer alan **Endpoint Ekle** butonu ile yeni endpoint oluşturma ekranına geçilebilir.

Webhooks sayfası iki sekmeden oluşur:

- **Endpoints** — Oluşturulmuş webhook uç noktalarını listeler
- **Triggers** — Filarch'ta tanımlı olayları listeler

### a. Endpoints

Sayfa açıldığında bu sekme varsayılan olarak görüntülenir. Sistemde tanımlanmış tüm endpointler tablo halinde listelenir. Tablonun üzerindeki arama kutusu ile endpointler isim, hedef URL, HTTP metodu veya kimlik doğrulama türüne göre anlık olarak filtrelenebilir.

Tabloda yer alan bilgiler:

- **Name:** Endpointin adıdır. Tıklandığında endpoint detay sayfasına yönlendirilir.
- **Target URL:** Bildirimin gönderileceği adrestir. Uzun adresler kısaltılarak gösterilir; tam adres üzerine gelindiğinde görünür.
- **Method:** Kullanılan HTTP metodudur (GET, POST, PUT, PATCH, DELETE vb.).
- **Auth Type:** Kimlik doğrulama yöntemidir. None, Bearer, Basic, API Key (Header), API Key (Query) veya Custom Header olabilir.
- **Status:** Endpointin aktif ya da pasif olduğunu gösterir.
- **Namespace:** Endpointin bağlı olduğu çalışma alanıdır.
- **Project:** Endpointin bağlı olduğu projedir.
- **Created Date:** Endpointin oluşturulma tarihidir.
- **Actions:** Her satırda detay görüntüleme (göz ikonu), düzenleme (kalem ikonu) ve silme (çöp kutusu ikonu) işlemleri yer alır.

### b. Triggers

![Tetikleyiciler.png](http://docs.filarch.com/media/uploads/Tetikleyiciler.png) Şekil 1.2 – Triggers Sekmesi

Bu sekmede Filarch'ta webhook tetikleyebilecek tüm olaylar listelenir. Arama kutusu ile olay adına göre anlık filtreleme yapılabilir.

Tabloda yer alan bilgiler:

- **Name:** Olayın adıdır. Tıklandığında tetikleyici detay sayfasına yönlendirilir.
- **Description:** Olayın ne zaman tetiklendiğine dair açıklamadır.
- **Status:** Olayın aktif ya da pasif olduğunu gösterir.
- **Actions:** Yalnızca detay görüntüleme işlemi mevcuttur; olaylar bu ekrandan düzenlenemez veya silinemez.

---

## 2. Endpoint Oluştur

![Endpoint Oluşturma.png](http://docs.filarch.com/media/uploads/Endpoint_Olusturma.png) Şekil 1.3 – Endpoint Oluştur Ekranı

**Endpoint Ekle** butonuna tıklandığında Endpoint Oluştur sayfasına yönlendirilir. Bu sayfa üç bölümden oluşur: Temel Ayarlar, Güvenlik ve Kapsam.

### Temel Ayarlar

| Alan | Açıklama | Zorunlu |
|------|----------|---------|
| **Name** | Endpointin tanımlayıcı adıdır. | Evet |
| **Target URL** | Bildirimin gönderileceği tam adrestir. Geçerli bir URL formatında girilmelidir (örn. `https://example.com/webhook`). | Evet |
| **HTTP Method** | Bildirim gönderilirken kullanılacak HTTP metodudur. GET, POST, PUT, PATCH, DELETE, HEAD ve OPTIONS seçenekleri mevcuttur. | Evet |
| **Status** | Endpointin oluşturulur oluşturulmaz aktif olup olmayacağını belirler. Varsayılan olarak aktiftir. | — |

### Güvenlik

| Alan | Açıklama | Zorunlu |
|------|----------|---------|
| **Auth Type** | Hedef adresin gerektirdiği kimlik doğrulama yöntemidir. Seçime göre ek alanlar belirir. | — |
| **Secret** | İsteğe bağlı bir imzalama anahtarıdır. Hedef servis bu anahtar aracılığıyla bildirimin Filarch'tan geldiğini doğrulayabilir. | — |

Seçilen kimlik doğrulama türüne göre görünen ek alanlar:

- **None:** Ek alan gerekmez.
- **Bearer:** Token alanı görünür.
- **Basic:** Kullanıcı adı ve şifre alanları görünür.
- **API Key (Header) / API Key (Query):** Anahtar adı ve anahtar değeri alanları görünür.
- **Custom Header:** Özel başlık adı ve değeri alanları görünür.

Aynı bölümde gönderim davranışını etkileyen gelişmiş ayarlar da bulunur:

| Alan | Açıklama | Varsayılan |
|------|----------|------------|
| **Retry Count** | Başarısız gönderim sonrası kaç kez yeniden deneneceğini belirtir. | 3 |
| **Retry Delay (sn)** | Yeniden denemeler arasında beklenecek süreyi saniye cinsinden ifade eder. | 60 |
| **Timeout (sn)** | Gönderimin zaman aşımına uğrayacağı süredir. 5 ile 30 saniye arasında bir değer girilmelidir. | 15 |

### Kapsam

| Alan | Açıklama | Zorunlu |
|------|----------|---------|
| **Namespace** | Endpointin bağlı olduğu çalışma alanıdır. | Evet |
| **Project** | Endpointin bağlı olduğu projedir. Önce çalışma alanı seçilmeden proje seçilemez. | Evet |

Form eksiksiz doldurulduktan sonra **Save** butonuna tıklandığında endpoint oluşturulur ve webhooks sayfasına yönlendirilir.

---

## 3. Endpoint Detayı

![Endpoint Detay.png](http://docs.filarch.com/media/uploads/Endpoint_Detay.png) Şekil 1.4 – Endpoint Detayı Sayfası

Endpoint listesinde bir kaydın adına ya da göz ikonuna tıklandığında Endpoint Detayı sayfasına yönlendirilir. Bu sayfa; endpointin temel bilgilerini, bağlı tetikleyicileri, alan eşlemelerini, test aracını ve gönderim loglarını tek ekranda sunar.

Sayfanın üst bölümündeki bilgi kartında şu bilgiler yer alır:

- **Name, Target URL, HTTP Method, Auth Type, Status**
- **Retry Attempts:** Yeniden deneme sayısı ve bekleme süresi (örn. `3 × (60s)`)
- **Timeout:** Zaman aşımı süresi (örn. `15s`)
- **Created / Updated Date**

Kartın sağ üst köşesinde **Logs**, sol alt köşesinde **Test** butonu bulunur. Endpoint pasif durumdayken Test butonu kullanılamaz.

### a. Tetikleyiciler

Sol kolonda, bu endpointe bağlı tetikleyiciler listelenir. Her satırda olayın adı, HTTP metodu rozeti ve durum rozeti görüntülenir.

Bu alanda yapılabilecek işlemler:

- **"+" butonu** ile yeni tetikleyici eklenebilir.
- Her tetikleyicinin yanındaki **toggle** ile tetikleyici aktif ya da pasif yapılabilir.
- **Çöp kutusu** ikonu ile tetikleyici silinebilir.

Bir tetikleyiciye tıklandığında sağ kolondaki alan eşlemeleri o tetikleyiciye ait bilgilerle güncellenir.

### b. Tetikleyici Ekleme

![Tetikleyici Ekleme.png](http://docs.filarch.com/media/uploads/Tetikleyici_Ekleme_DfbktYV.png) Şekil 1.5 – Tetikleyici Ekleme

**"+"** butonuna tıklandığında tetikleyici ekleme modalı açılır.

| Alan | Açıklama | Zorunlu |
|------|----------|---------|
| **Event Category** | Olayın kategorisidir. Önce kategori seçilmesi gerekir; aksi hâlde olay listesi pasif kalır. | Evet |
| **Event Name** | Seçilen kategoriye ait olayları listeler. | Evet |
| **HTTP Method** | Bu tetikleyici için endpointin varsayılan metodunu geçersiz kılmak istendiğinde seçilir. Boş bırakılırsa endpointin varsayılan metodu kullanılır. | — |
| **Trigger Status** | Tetikleyicinin hemen aktif olup olmayacağını belirler. | — |

**Add** butonuna tıklandığında tetikleyici kaydedilir ve listeye eklenir.

### c. Alan Eşlemeleri

Sağ kolonda, seçili tetikleyiciye ait alan eşlemeleri görüntülenir ve düzenlenir. Alan eşlemeleri; Filarch'ın göndereceği bildirim içinde hangi verinin, hangi anahtar adıyla yer alacağını belirler.

Kaydedilmiş her eşleme satırında üç bilgi yer alır:

- **Payload Key:** Bildirim JSON'ında kullanılacak alan adıdır (örn. `file_name`).
- **Field Definition:** Bu anahtara eşlenen Filarch alanıdır (örn. Dosya Adı).
- **Format:** Veriye uygulanan dönüşüm bilgisidir.

Yeni bir eşleme eklemek için **Add Field** butonuna tıklanır. Açılan taslak satırda şu alanlar doldurulur:

| Alan | Açıklama |
|------|----------|
| **Payload Key** | Bildirimde görünecek anahtar adı girilir. |
| **Field Definition** | Listeden bir Filarch alanı seçilir. |
| **Format Preset** | İsteğe bağlıdır. Tip dönüşümü (`string`, `int`, `float`) veya tarih biçimi (`%Y-%m-%d`, `%d/%m/%Y` vb.) seçilebilir. |

Payload Key ve Field Definition alanları doldurulunca satırın kaydet butonu aktif hale gelir ve eşleme kaydedilebilir. Kaydedilmeden başka bir tetikleyiciye geçilirse taslak kaybolur.

Her kayıtlı satırın yanındaki çöp kutusu ikonu ile eşleme silinebilir.

### d. Test ve Önizleme

![Test İsteği Gönderme ve Önizleme.png](http://docs.filarch.com/media/uploads/Test_Istegi_Gonderme_ve_Onizleme.png) Şekil 1.6 – Test ve Önizleme

**Test** butonuna tıklandığında test modalı açılır. Bu ekranda önce gönderim içeriği incelenebilir, ardından gerçek bir test isteği gönderilebilir.

1. **Tetikleyici seçimi:** Açılır menüden test edilecek tetikleyici seçilir.
2. **Payload önizleme:** Seçim yapıldığı anda Filarch'ın göndereceği tam JSON içeriği önizleme alanında otomatik olarak görünür. Hiçbir istek gönderilmeden içerik bu şekilde incelenebilir.
3. **Gönderim:** **Send** butonuna tıklandığında seçili tetikleyici için gerçek bir test isteği gönderilir. Sonuç daha sonra Loglar ekranında görüntülenebilir.

### e. Loglar

![Loglar.png](http://docs.filarch.com/media/uploads/Loglar.png) Şekil 1.7 – Gönderim Logları

**Logs** butonuna tıklandığında log modalı açılır. Bu ekranda endpointe ait tüm gönderim geçmişi listelenir.

Üst kısımdaki filtre butonlarıyla loglar daraltılabilir:

- **All** — Tüm gönderimler
- **Success** — Başarılı gönderimler
- **Retrying** — Yeniden deneme sürecindeki gönderimler
- **Failed** — Başarısız gönderimler

Log tablosunda yer alan bilgiler:

- **Date:** Gönderimin gerçekleştiği tarih ve saattir.
- **Trigger:** Bildirimi tetikleyen olaydır.
- **Status:** Gönderimin sonucudur.
- **Response Code:** Hedef sunucunun döndürdüğü HTTP durum kodudur.
- **Error:** Varsa hata mesajının kısa hâlidir; tam metin üzerine gelindiğinde görünür.

Bir satıra tıklandığında o gönderime ait ayrıntılar genişler:

- **Request Payload:** Filarch'ın gönderdiği tam JSON içeriğidir.
- **Response Payload:** Hedef sunucudan dönen yanıt içeriğidir.
- **Error Message:** Varsa tam hata açıklaması kırmızı kutu içinde gösterilir.

---

## 4. Endpoint Güncelle

Endpoint listesinde bir kaydın kalem ikonuna tıklandığında Endpoint Güncelle sayfasına yönlendirilir. Sayfa, Endpoint Oluştur formuyla aynı yapıdadır; tüm alanlar mevcut bilgilerle dolu şekilde açılır.

Değiştirilmek istenen alanlar düzenlenip **Update** butonuna tıklandığında değişiklikler kaydedilir ve webhooks sayfasına yönlendirilir.

---

## 5. Tetikleyici Detayı

![Tetikleyici Detay.png](http://docs.filarch.com/media/uploads/Tetikleyici_Detay.png) Şekil 1.8 – Tetikleyici Detayı Sayfası

Triggers sekmesinde bir olayın adına ya da göz ikonuna tıklandığında Tetikleyici Detayı sayfasına yönlendirilir. Sayfanın üst bölümünde olayın adı, açıklaması ve durumu gösterilir.

### a. Bağlı Endpointler

Sol kolonda bu olayın bağlı olduğu tüm endpointler listelenir. Her satırda endpointin adı, HTTP metodu rozeti ve durum rozeti görüntülenir. Bir endpointe tıklandığında sağ kolondaki alan eşlemeleri o endpointe ait bilgilerle güncellenir.

### b. Alan Eşlemeleri

Sağ kolonda seçili endpointe ait alan eşlemeleri görüntülenir ve yönetilir. Yeni alan ekleme, kaydetme ve silme işlemleri, Endpoint Detayı sayfasındaki alan eşlemeleriyle aynı şekilde çalışır.