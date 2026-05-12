# Dosya Eskalasyonu

## 1. Eskalasyon Sekmesi
![Dosya Eskalasyonu.png](http://docs.filarch.com/media/uploads/Dosya_Eskalasyonu_pZyRAfv.png) Şekil 1.1 – Eskalasyon sekmesine dair örnek görünüm

Dosya Yöneticisi'nde bir dosyanın üzerine tıklandığında sağ tarafta açılan çekmecenin **Eskalasyon** sekmesi, o dosyaya ait tüm eskalasyon kurallarını listeler ve yönetmeye olanak tanır.

Sekme başlığının yanında mevcut kural sayısı ve maksimum kapasite gösterilir (örn. `1/3`). Admin yetkisine sahip kullanıcılar bu sekme üzerinden kural ekleyebilir, düzenleyebilir ve silebilir; izleme yetkisindeki kullanıcılar yalnızca kuralları görüntüleyebilir.

Sekmede yer alan bilgiler:

- **Rol:** Bildirimin gideceği proje rolüdür.
- **Tetiklenme Süresi:** Dosyanın kaç dakika boyunca güncellenmemesi durumunda bildirimin tetikleneceğini gösterir. Dakika değeri okunabilir bir biçimde (gün / saat / dakika) de görüntülenir.
- **Tekrar Aralığı:** Alanda değer varsa ilk bildirimden sonra kaç dakikada bir tekrar gönderileceğini gösterir. Alan boş bırakılmışsa (yani `null`) **Tek seferlik** olarak görünür.
- **Sonraki Kontrol:** Sistemin bu kural için bir sonraki ne zaman kontrol yapacağını gösterir.
- **Durum rozetleri:** Kural pasifse **Pasif**, bildirim gönderilmiş ve hâlâ bekleniyorsa **Bildirim Gönderildi** rozeti görünür.

---

## 2. Kural Ekle

**Kural Ekle** butonuna tıklandığında sekmenin alt kısmında yeni kural formu açılır.

| Alan | Açıklama | Zorunlu |
|------|----------|---------|
| **Rol** | Bildirimin gönderileceği proje rolüdür. Açılır menüden projede tanımlı roller seçilir. | Evet |
| **Tetiklenme Süresi (dakika)** | Dosyanın güncellenmeden kaç dakika geçmesi durumunda bildirimin tetikleneceğidir. 1 veya daha büyük bir tam sayı girilmelidir. | Evet |
| **Tekrar Aralığı (dakika)** | Doldurulursa ilk bildirimden sonra her N dakikada bir tekrar bildirim gönderilir. **Boş bırakılırsa bildirim tek seferlik olur**; ayrı bir seçenek yoktur. | Hayır |
| **Aktif** | Kuralın oluşturulur oluşturulmaz izlemeye alınıp alınmayacağını belirler. Varsayılan olarak işaretlidir. | — |

Dakika değeri girildiğinde alanın altında okunabilir karşılığı otomatik olarak gösterilir (örn. `1440` girince `= 1 gün` çıkar).

**Oluştur** butonuna tıklandığında kural kaydedilir ve listede görünür. Bir dosyaya en fazla 3 kural eklenebilir; bu sayıya ulaşıldığında **Kural Ekle** butonu gizlenir ve bilgi mesajı gösterilir.

---

## 3. Kural Düzenle

Her kuralın sağ tarafında yer alan kalem ikonuna tıklandığında kural satırı, mevcut değerlerin dolu olduğu bir düzenleme formuna dönüşür. Form alanları Kural Ekle ile aynıdır.

Değişiklikler yapıldıktan sonra **Kaydet** butonuna tıklanır; form kapanır ve kural listede güncellenmiş değerleriyle yeniden görünür. **İptal** butonuna tıklanırsa değişiklikler kaybolur ve kural görüntüleme moduna geri döner.

---

## 4. Kural Sil

Bir kuralın çöp kutusu ikonuna tıklandığında silme onay mesajı görünür:

> Bu kuralı silmek istediğinize emin misiniz?

**Evet, Sil** butonuna tıklandığında kural kalıcı olarak silinir ve listeden kaldırılır. **İptal** butonuyla işlemden vazgeçilebilir.

---

## 5. Durum Rozetleri

Her kural kartında aşağıdaki rozetler gösterilebilir:

| Rozet | Anlam |
|-------|-------|
| *(Rozet yok)* | Kural aktif ve henüz tetiklenmedi. |
| **Pasif** | Kural izleme dışı bırakılmış; bildirim gönderilmez. |
| **Bildirim Gönderildi** | Tetiklenme süresi doldu ve bildirim gönderildi; dosya hâlâ güncellenmedi. |

---

## 6. Kapasite Sınırı

Bir dosya için en fazla **3 eskalasyon kuralı** tanımlanabilir. Bu sayıya ulaşıldığında:

- **Kural Ekle** butonu gizlenir.
- Sekme başlığında `3/3` gösterilir.
- Mavi bilgi kutusunda *"Bu dosya için maksimum 3 kural tanımlanmıştır."* mesajı görünür.

Yeni kural eklemek için mevcut kurallardan birinin silinmesi gerekir.

---

## 7. Yetki Gereksinimleri

Eskalasyon sekmesi tüm kullanıcılara görünürdür; ancak kural ekleme, düzenleme ve silme işlemleri yalnızca **Admin** yetkisine sahip kullanıcılar tarafından yapılabilir. Daha düşük yetkili kullanıcılar kuralları görüntüleyebilir fakat değiştiremez.