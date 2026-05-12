# Arama

Filarch'ta arama çubuğundan tek sorguda birden fazla nesne türü aranabilir: **çalışma alanı, proje, klasör, dosya ve etiket**. Gelişmiş Arama ise dosya sonuçlarını yedi filtre boyutuyla daraltır.

---

## Hızlı Arama

Hangi çalışma alanı veya projede olduğunu bilmeden arama yapın.

### Nasıl kullanılır?

1. Üst çubukta arama kutusuna tıklayın
2. Aramak istediğiniz terimi yazmaya başlayın
3. Sonuçlar tüm yetkili içerik genelinde anlık olarak listelenir

### Aranabilir nesne türleri

| Tür | Açıklama |
|-----|----------|
| **Çalışma Alanı** | Adına göre çalışma alanı bulun |
| **Proje** | Proje adına göre arama yapın |
| **Klasör** | Klasör adına göre arama yapın |
| **Dosya** | Dosya adına göre arama yapın |
| **Etiket** | Etiket adına göre arama yapın |

Her sonuç satırında nesne türü, ad ve bulunduğu konum (**Çalışma Alanı → Proje → Klasör**) gösterilir.

Sonuçları ada, boyuta, tarihe veya dosya türüne göre artan ya da azalan sırada sıralayabilirsiniz.

> **Ekran Görüntüsü:** Hızlı arama sonuç listesi — farklı nesne türleri ve konum sütunları
> ![search-1.png](http://docs.filarch.com/media/uploads/search-1.png)

---

## Gelişmiş Arama

Dosya sonuçlarını daraltmak için birden fazla kriteri aynı anda uygulayın.

### Nasıl kullanılır?

1. Üst çubukta gelişmiş arama butonuna tıklayın
2. Aramak yapmak Çalışma Alanı ve Projeyi seçin
3. Sonuçlar tüm yetkili içerik genelinde anlık olarak listelenir

> **Ekran Görüntüsü:** Gelişmiş arama panelinin açılış şekli
> ![advanced-search-1.png](http://docs.filarch.com/media/uploads/advanced-search-1.png)

### Filtre seçenekleri

| Filtre | Açıklama |
|--------|----------|
| **Çalışma Alanı** | Arama yapılacak çalışma alanlarını seçin |
| **Proje** | Belirli projelere odaklanın |
| **Dosya Türü** | `.dwg`, `.rvt`, `.pdf` gibi dosya türleri |
| **Kullanıcı** | Belirli kişilerin yüklediği dosyaları bulun |
| **Etiketler** | Atanmış etiketlere göre daraltın |
| **Son Güncelleme** | Son 1 Saat / Son 24 Saat / Son 7 Gün / Son 14 Gün / Son 30 Gün |
| **Boyut** | Minimum / maksimum KB değeri girin |

Tüm filtreler aynı anda uygulanabilir ve her değişiklik otomatik olarak yeni arama başlatır.

> **Ekran Görüntüsü:** Gelişmiş arama paneli — filtre seçenekleri açık
> ![advanced-search-2.png](http://docs.filarch.com/media/uploads/advanced-search-2.png)

### Fuzzy (Benzerlik) Arama

**Fuzzy Arama** modunu açarak dosya adını tam bilmeden veya yazım hatasıyla da arama yapabilirsiniz.

- Sistem girdiğiniz terimi dosya adlarıyla karşılaştırır ve her sonuca benzerlik skoru atar
- En yüksek skorlu eşleşmeler listenin üstüne yerleşir
- Eşleşen kelime ve yüzdelik benzerlik skoru sonuç satırında gösterilir
- Yazım hatasını fark eden sistem **"Did you mean?"** butonu ile doğru terimi önerir

> **Ekran Görüntüsü:** Fuzzy arama — `arh-elevtion` sorgusu, `ARC-ELEVATION-NORTH.dwg` eşleşmesi ve "Did you mean?" önerisi
> ![advanced-search-3(didyoumean).png](http://docs.filarch.com/media/uploads/advanced-search-3didyoumean.png)

### Örnek kullanım

> **Senaryo:** Son 30 günde A. Yılmaz tarafından yüklenen, 5000 KB üzerinde `.rvt` türündeki dosyaları bulmak istiyorsunuz.

1. Gelişmiş Arama panelini açın
2. **Kullanıcı** filtresinden **A. Yılmaz**'ı seçin
3. **Son Güncelleme** altından **Son 30 Gün**'ü işaretleyin
4. **Boyut** alanına Min KB değerini girin
5. **Dosya Türü** filtresinden **`.rvt`** seçin
6. **Search** butonuna tıklayın