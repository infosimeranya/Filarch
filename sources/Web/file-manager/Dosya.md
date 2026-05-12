# Dosya
 
![file_manager](https://i.hizliresim.com/hwe2kxh.png) Şekil 1.1 – Dosya Yöneticisi Ana Ekranı (Dosyalar)

Bu dokümanda, Filarch uygulamasındaki dosya yöneticisinde bulunan dosyalar üzerinde gerçekleştirilebilen işlemler açıklanmaktadır.

## 1. Dosya Ekleme

![add_folder](https://i.hizliresim.com/1ynnrsd.png) Şekil 1.2 – Dosya Ekleme Menüsü

Kullanıcı, dosya yöneticisinde yer alan **Dosya Ekle** butonuna tıkladığında dosya yükleme menüsü açılır.

Bu menüde:

- Dosya seçilebilir veya sürükle-bırak yöntemiyle eklenebilir
- Dosya için açıklama ve yorum girilebilir
- Dosya bir milestone dosya ise işaretlenebilir

Yükle butonuna tıklandığında dosya yükleme işlemi başlatılır ve yükleme süreci bir ilerleme çubuğu ile gösterilir.
Yükleme tamamlandığında dosya, kullanıcının o anda bulunduğu klasöre eklenir.

Dosya ekleme formunda:

- Dosya seçilmesi
- Yorum alanının doldurulması

zorunludur.

Dosya ekleme işlemi **Maintainer** rolü ve üzerindeki kullanıcılar tarafından yapılabilir.

## 2. Dosya Menüsü

![file_drawer](https://i.hizliresim.com/t1xswcj.png) Şekil 1.3 – Dosya Detay Menüsü (Drawer)

Kullanıcı, dosya yöneticisindeki tabloda yer alan dosya detay butonuna tıkladığında dosya menüsü açılır. Bu menü üzerinden seçilen dosyaya ait işlemler gerçekleştirilir.

Menünün üst kısmından:

- Dosya dondurulabilir
- Dosyaya ait bir toplantı konusu eklenebilir

Dosya dondurulduğunda dosyaya ait işlemler pasif hâle gelir. Toplantı konusu eklendiğinde, toplantı oluşturulurken bu konu seçilebilir.

Dosya menüsü dört sekmeden oluşur:

- Versiyonlar
- Aktiviteler
- Dosya Bilgileri
- Toplantı Konuları

### a. Versiyonlar

![file_drawer_versions](https://i.hizliresim.com/t1xswcj.png) Şekil 1.4 – Dosya Versiyonları Sekmesi

Aynı klasör içerisine, aynı isimde bir dosya tekrar yüklendiğinde sistem bu dosyayı yeni bir versiyon olarak algılar ve mevcut dosyanın altında versiyon olarak kaydeder.

Bu sekmede dosyaya ait tüm versiyonlar tablo halinde listelenir.
Tabloda aşağıdaki bilgiler yer alır:



 ![file_drawer_comments](https://i.hizliresim.com/o964e39.png) Şekil 1.5 – Dosya Yorumlar / Commit Alanı
 
  Versiyon işlemleri şunlardır:

- **Yorum Yapma:** Yorum yapma butonuna tıklandığında bir pencere açılır. Bu alanda dosya üzerinde yetkisi bulunan kullanıcıların yorumları görüntülenir ve kullanıcı isterse yeni bir yorum ekleyebilir.
- **Paylaşma:** Dosya üzerinde yetkisi bulunan kullanıcılara, ilgili versiyonun yüklendiğine dair yeniden bilgilendirme e-postası gönderilir. Bu işlemi **Maintainer** rolü ve üzerindeki kullanıcılar yapabilir.
- **İndirme:** Seçilen versiyon indirilir.
- **Silme:** Seçilen versiyon silinir. Bu işlemi yalnızca **Admin** rolü ve üzerindeki kullanıcılar yapabilir.

Versiyonlar bölümünde yer alan “Son Versiyon Hariç Tüm Versiyonları Sil” butonuna tıklandığında:

- Son versiyon ve milestone olarak işaretlenmiş versiyonlar hariç tüm versiyonlar silinir

Kullanıcı isterse milestone dosyaları da silerek yalnızca son versiyonu bırakabilir. Bu işlemi sadece Admin rolü ve üzerindeki kullanıcılar gerçekleştirebilir.

### b. Aktiviteler

![file_drawer_activities](https://i.hizliresim.com/jjdtzbd.png)  Şekil 1.6 – Dosya Aktiviteleri Sekmesi

Bu sekmede dosya üzerinde gerçekleştirilen tüm işlem kayıtları listelenir. Çok sayıda kayıt bulunması durumunda sayfalar arasında geçiş yapılabilir.

### c. Dosya Bilgileri

![file_drawer_information](https://i.hizliresim.com/2u9w3e4.png) Şekil 1.7 – Dosya Bilgileri Sekmesi

Bu sekmede dosyaya ait bilgiler görüntülenir. Ayrıca dosyaya etiket atama işlemi bu bölümden yapılır. Etiket atama işlemi **Maintainer** rolü ve üzerindeki kullanıcılar tarafından yapılabilir.

### d. Toplantı Konuları

![file_drawer_meeting_topics](https://i.hizliresim.com/7mi44gc.png) Şekil 1.8 – Dosya Toplantı Konuları Sekmesi

Bu sekmede dosya ile ilişkilendirilmiş toplantı konuları listelenir.