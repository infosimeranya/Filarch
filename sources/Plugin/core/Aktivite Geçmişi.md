# Aktivite Geçmişi ve Denetim İzi

Filarch, proje genelinde gerçekleşen tüm işlemleri kimin ne zaman yaptığını gösteren zaman damgalı bir aktivite akışı tutar. Başarısız işlemler de kayıt altına alınır.

---

## Kayıt Altına Alınan İşlem Türleri

Her aktivite kaydında şunlar yer alır:

- **İşlem tipi:** Yükleme, indirme, yorum, silme, klasör oluşturma, taşıma, güncelleme, dondurma, dondurma kaldırma
- **Nesne:** İşlem yapılan dosya, klasör, proje veya çalışma alanı adı ve türü
- **Kullanıcı:** İşlemi gerçekleştiren kişinin adı, soyadı ve e-postası
- **Zaman:** Tarihi ve saati
- **Sonuç:** HTTP durum kodu (başarılı ve başarısız işlemler ayrışır)

---

## Aktivite Geçmişine Erişim

Sol gezinme çubuğunun alt kısmındaki **saat simgesi** butonuna tıklayın. Aktivite geçmişi paneli açılır; yetkili olduğunuz tüm çalışma alanı, proje, klasör ve dosyalardaki işlemleri görürsünüz — önceden herhangi bir proje veya çalışma alanı seçmeniz gerekmez.

Kayıtlar en yeniden en eskiye doğru listelenir; sayfalama ile büyük geçmişler performanstan ödün vermeden gezilir.

> **Ekran Görüntüsü:** Aktivite geçmişi akışı — işlem tipi, kullanıcı ve zaman damgası sütunları
> ![activity-history.png](http://docs.filarch.com/media/uploads/activity-history.png)


---

## Dondurma (Freeze) Geçmişi

Kritik bir dosyayı kim dondurdu? Ne zaman açıldı? Bu bilgilerin tamamı aktivite akışında bağımsız olaylar olarak kayıtlıdır.

Dondurma ve dondurma kaldırma işlemleri diğer aktivitelerden ayrı tür olarak etiketlenir; uyumluluk denetimlerinde kolayca filtrelenebilir.

---

## Başarısız İşlem Kaydı

Bir işlem başarısız olduğunda (örn. yetersiz yetki, sunucu hatası) bu deneme de geçmişe yazılır. HTTP hata kodu ve kullanıcı bilgisi kayıtlıdır.

Bu sayede:
- Erişim sorunlarını sistem loguna bakmadan anlayabilirsiniz
- Yetkisiz erişim girişimlerini tespit edebilirsiniz

---

## Örnek Kullanım — Hukuki Kanıt

> İhale sonrası anlaşmazlık sürecinde proje müdürü, belirli bir teknik şartname dosyasının ihale tarihinden sonra değiştirilip değiştirilmediğini kanıtlamak zorundadır.

1. Aktivite geçmişini açın
2. Dosya adına göre filtreleyin
3. İlgili tarih aralığında hiçbir yükleme veya güncelleme olmadığını zaman damgalarıyla belgeleyin

Bu çıktı hukuki süreçte kanıt niteliği taşır.

---

## Sık Sorulan Sorular

**Aktivite geçmişine kim erişebilir?**
Proje yöneticisi düzeyindeki kullanıcılar aktivite geçmişini doğrudan arayüzden görüntüleyebilir; IT yöneticisi veya sistem erişimi gerekmez.

**Geçmiş kayıtlar silinebilir mi?**
Hayır. Aktivite kayıtları değiştirilemez ve silinemez; denetim bütünlüğü korunur.