# Gelişmiş Arama Modülü

Filarch'ın Gelişmiş Arama Modülü, tüm namespace ve projeler genelinde dosya ve klasörleri tek ekrandan aratmanızı, çok boyutlu filtrelerle daraltmanızı ve sonuçlar üzerinde doğrudan işlem yapmanızı sağlar. Standart dosya yöneticisi navigasyonuna alternatif olarak, herhangi bir projeye gitmeden içerik bulmayı mümkün kılar.

---

## İçindekiler

1. [Arama Çubuğu ve Bulanık Arama](#arama-çubuğu-ve-bulanık-arama)
2. [Filtre Paneli](#filtre-paneli)
   - [Dosya Türü](#dosya-türü)
   - [Etiketler](#etiketler)
   - [Namespace](#namespace)
   - [Proje](#proje)
   - [Son Güncelleme](#son-güncelleme)
   - [Kullanıcı](#kullanıcı)
   - [Dosya Boyutu](#dosya-boyutu)
   - [Tüm Filtreleri Uygula / Temizle](#tüm-filtreleri-uygula--temizle)
3. [Sonuçlar Tablosu](#sonuçlar-tablosu)
   - [Sütunlar](#sütunlar)
   - [Sıralama](#sıralama)
   - [Eşleşme Detayı Rozeti](#eşleşme-detayı-rozeti)
   - [Milestone Etiketi](#milestone-etiketi)
   - [Lisans Kısıtlaması](#lisans-kısıtlaması)
4. [Satır Aksiyonları](#satır-aksiyonları)
   - [Görüntüle / Klasöre Git](#görüntüle--klasöre-git)
   - [İndir](#i̇ndir)
   - [Sil](#sil)
5. [Sayfalama](#sayfalama)
6. [URL ile Ön Filtre](#url-ile-ön-filtre)

---

## Arama Çubuğu ve Bulanık Arama

Sayfanın üst kısmında yer alan arama çubuğu, dosya ve klasör adlarında tam metin araması yapar. Arama metni yerel state'te tutulur; **Enter** tuşuna veya "Ara" düğmesine basıldığında API çağrısı tetiklenir (her tuş vuruşunda arama yapılmaz).

**Nasıl Kullanılır**

1. Arama kutusuna aradığınız dosya/klasör adını yazın.
2. **Enter** tuşuna basın ya da sağdaki **Ara** düğmesine tıklayın.
3. Sonuçlar anında tabloda güncellenir; her filtre değişikliğinde sayfa 1'e döner.

**Bulanık Arama (Trigram)**

Arama çubuğunun hemen altında yer alan toggle, yazım yanlışlarını ve yakın eşleşmeleri tolere eden **bulanık arama (Trigram)** modunu açar. Aktif olduğunda toggle mavi renge döner.

| Mod | Davranış |
|---|---|
| Kapalı (varsayılan) | Tam metin eşleşmesi — daha hızlı, kesin sonuçlar |
| Açık (Trigram) | Benzerlik tabanlı eşleşme — yazım hatalarına karşı toleranslı |

Toggle'a tıklanır tıklanmaz arama otomatik olarak yeniden çalışır.

![Arama çubuğu ve bulanık arama toggle](http://docs.filarch.com/media/uploads/01_search_bar.png)
*Şekil 1.0: Arama çubuğu, Ara düğmesi ve bulanık arama toggle*

---

## Filtre Paneli

Arama çubuğunun altında, sol bölümde **Filtre Paneli** yer alır. Her filtre bölümü bağımsız olarak daraltılıp genişletilebilir. Seçimler önce yerel "bekleyen" (pending) state'e alınır; **Uygula** düğmesiyle veya panelin altındaki **Tüm Filtreleri Uygula** düğmesiyle API'ye gönderilir. Her bölümde aktif filtre varsa bir **Temizle** bağlantısı belirir.

![Filtre paneli genel görünüm](http://docs.filarch.com/media/uploads/02_filters_panel.png)
*Şekil 2.0: Filtre paneli — dosya türü, etiket, namespace, proje, son güncelleme, kullanıcı ve dosya boyutu bölümleri*

![Filtre paneli aktif filtreler](http://docs.filarch.com/media/uploads/03_filters_panel.png)
*Şekil 2.1: Aktif filtreler ve Uygula / Temizle bağlantıları*

---

### Dosya Türü

API'den dönen `file_extensions` listesine göre dinamik olarak oluşturulur. Her seçeneğin yanında mevcut sonuç kümesindeki eşleşme sayısı gösterilir.

Desteklenen özel değerler:

| Değer | Açıklama |
|---|---|
| `folder` | Sadece klasörleri göster |
| `tag` | En az bir etikete sahip dosyaları göster |
| `.dwg`, `.pdf`, `.xlsx`, … | Uzantıya göre filtrele |

Birden fazla uzantı seçilebilir (çoklu checkbox). Seçim yapıldıktan sonra bölüm altındaki **Uygula** düğmesine tıklayın.

---

### Etiketler

Projeye özgü etiketler (tags) varsa bu bölüm görünür. Her etiketin yanında mevcut sonuç kümesindeki eşleşme sayısı gösterilir. Birden fazla etiket seçilebilir.

---

### Namespace

Kullanıcının erişimi olan tüm namespace'ler listelenir. Namespace seçimi değiştiğinde Proje filtresi otomatik sıfırlanır (namespace → proje hiyerarşisi korunur). Birden fazla namespace seçilebilir.

---

### Proje

**Yalnızca en az bir namespace seçildiğinde** projeler görünür; listede sadece seçili namespace(ler)e ait projeler yer alır. Birden fazla proje seçilebilir.

---

### Son Güncelleme

Dört sabit zaman aralığı radio-benzeri tek seçim olarak sunulur:

| Seçenek | Zaman Aralığı |
|---|---|
| Son 1 Saat | `last_1_hour` |
| Son 24 Saat | `last_24_hours` |
| Son 7 Gün | `last_7_days` |
| Son 30 Gün | `last_30_days` |

Seçili seçenek tekrar tıklanarak devre dışı bırakılabilir.

---

### Kullanıcı

Proje seçiliyse sadece o projedeki kullanıcılar listelenir; yalnızca namespace seçiliyse namespace kullanıcıları; hiçbiri seçilmemişse tüm kullanıcılar gösterilir. Kullanıcı isimleri `first_name + last_name` formatında; profil tamamlanmamışsa e-posta adresi görünür.

---

### Dosya Boyutu

Minimum ve maksimum boyut (KB cinsinden) girilebilen iki sayısal alan. Alan doldurulduktan sonra **Uygula** düğmesine tıklayarak filtreyi devreye alın.

---

### Tüm Filtreleri Uygula / Temizle

Filtrelerin altında sayfaya yapışık iki düğme bulunur:

| Düğme | İşlev |
|---|---|
| **Tüm Filtreleri Uygula** | Bekleyen tüm filter seçimlerini tek seferde API'ye gönderir |
| **Tüm Filtreleri Temizle** | Namespace ve Proje dahil tüm filtreleri sıfırlar, URL'yi `/advanced-search`'e döndürür |

---

## Sonuçlar Tablosu

### Sütunlar

Sonuçlar yatay kaydırılabilir bir tabloda listelenir. Aksiyon sütunu sağ tarafa sabitlenmiştir (sticky), yatay kaydırmada her zaman görünür kalır.

| Sütun | İçerik |
|---|---|
| **Ad** | Dosya/klasör simgesi + adı; fuzzy aramada eşleşme rozeti |
| **Namespace** | Öğenin ait olduğu namespace adı |
| **Proje** | Öğenin ait olduğu proje adı |
| **Boyut** | Dosya boyutu (KB / MB); klasörler için `—` |
| **Son Değişiklik** | `gg.aa.yyyy ss:dd` formatında yerel saate çevrilmiş tarih |
| **Etiketler** | Renkli badge'ler; etiket yoksa `—` |
| **Aksiyonlar** | İndir / Görüntüle / Sil ikon düğmeleri |

Dosya simgeleri uzantıya göre otomatik seçilir (dwg, rvt, skp, rfa, pdf, xlsx, png, zip, psd vb.). Klasörler klasör simgesiyle gösterilir.

![Sonuçlar tablosu genel görünüm — ad, etiket, aksiyon sütunları ve satır detayları](http://docs.filarch.com/media/uploads/03_results_table.png)
*Şekil 3.0: Sonuçlar tablosu — dosya simgesi, etiket badge'leri, eşleşme rozeti ve aksiyon butonları*

---

### Sıralama

Tablonun üst çubuğunda iki açılır liste bulunur:

- **Sıralama Kriteri:** Ad, Tarih, Boyut, Tür
- **Sıralama Yönü:** Artan (asc), Azalan (desc)

Seçim değiştirildiğinde liste anında yeniden sorgulanır ve sayfa 1'e döner.

---

### Eşleşme Detayı Rozeti

Bulanık arama (trigram) aktifken, her sonuç satırında dosya adının altında eşleşme rozeti görünür:

| Alan | Açıklama |
|---|---|
| Tip etiketi | `FUZZY` (mor) veya `EXACT` (mavi) |
| Eşleşen kelime | Orijinal metin tırnak içinde; uzun kelimeler kısaltılır |
| Benzerlik yüzdesi | Yeşil ≥ %90, Turuncu ≥ %70, Kırmızı < %70 |

---

### Milestone Etiketi

Dosya `is_milestone: true` döndürdüğünde satırda yıldız simgesi (★) ve sarı "Milestone" badge'i gösterilir.

---

### Lisans Kısıtlaması

Kısıtlı öğelerde:

- Dosya simgesi %50 gri filtresi ve %60 opaklıkla soluklaşır.
- Satırın sol üstünde **RestrictionBadge** rozeti belirir.
- İndir ve Sil butonları devre dışı bırakılır (opaklık 0.5, cursor: not-allowed).
- İndir veya Sil butonuna tıklanırsa AlertModal ile uyarı gösterilir.

---

## Satır Aksiyonları

Her satırın sağ tarafında üç aksiyon ikonu bulunur.

### Görüntüle / Klasöre Git

- **Dosya ise:** Sağdan kayan FileDrawer açılır; dosya detayları, meta veriler ve versiyonlar görüntülenebilir.
- **Klasör ise:** Dosya yöneticisinde ilgili klasöre `/file-manager/namespace/:nsId/project/:projId/folder/:folderId` URL'siyle yönlendirilir.

### İndir

- Yalnızca `object_type === "file"` olan ve lisans kısıtı olmayan öğeler için aktiftir.
- İndirme sırasında simge dönen yükleyici animasyonuna döner, düğme devre dışı kalır.
- İndirme tamamlanınca tarayıcının standart dosya indirme mekanizması devreye girer.

### Sil

- Lisans kısıtı olmayan öğeler için aktiftir.
- Tıklandığında **Silme Onay Modalı** (DeleteConfirmModal) açılır.
- Onaylanınca API'ye DELETE isteği gönderilir; başarılıysa sonuç listesi yenilenir.

---

## Sayfalama

Tablonun altında pagination kontrolü bulunur:

| Kontrol | Açıklama |
|---|---|
| ◀ / ▶ | Önceki / sonraki sayfaya git |
| Sayfa numaraları | İlk 5 sayfa + `...` + son sayfa gösterimi |
| Sayfa başı kayıt | Açılır listeden 20 / 40 / 60 seçimi |
| Sonuç sayısı | `X–Y / Z sonuç gösteriliyor` formatında üst çubukta |

Sayfa veya sayfa boyutu değiştiğinde sayfa başına otomatik kaydırma yapılır.

---

## URL ile Ön Filtre

Gelişmiş Arama sayfası üç URL formatını destekler:

| URL | Davranış |
|---|---|
| `/advanced-search` | Filtresiz açılır |
| `/advanced-search/namespace/:namespaceId` | İlgili namespace önceden seçili açılır |
| `/advanced-search/project/:projectId` | İlgili proje önceden seçili açılır |

Diğer modüllerden "Bu namespace/projede ara" bağlantılarıyla doğrudan ön filtreli arama açılabilir. Namespace veya proje filtresi silindiğinde URL de uygun rotaya geri döner.

---

## Karşılaştırmalı Avantajlar

| Özellik | Filarch | Google Drive | SharePoint | Box |
|---|---|---|---|---|
| Namespace + proje çapraz arama | ✅ Tek ekrandan | ❌ Drive bazlı | ❌ Site bazlı | ❌ |
| Bulanık / trigram arama | ✅ Toggle ile | ❌ | ❌ | ❌ |
| Eşleşme tipi + benzerlik skoru gösterimi | ✅ Rozet ile | ❌ | ❌ | ❌ |
| Etiket + uzantı + boyut + tarih kombinasyonu | ✅ | Kısmi | Kısmi | Kısmi |
| Sonuç üzerinden doğrudan silme / indirme | ✅ | ❌ | ❌ | ❌ |
| Lisans kısıtı entegrasyonu | ✅ Otomatik | N/A | N/A | N/A |
| URL ile ön filtre desteği | ✅ | ❌ | ❌ | ❌ |