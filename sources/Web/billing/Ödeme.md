# Fiyatlandırma ve Ödeme

## 1. Fiyatlandırma

![individual_pricing](https://i.hizliresim.com/bc6qew4.png) Şekil 1.1 – Bireysel Lisans Fiyatlandırma Sayfası

![corporate_pricing](https://i.hizliresim.com/55wszsp.png) Şekil 1.2 – Kurumsal Lisans Fiyatlandırma Sayfası

Kullanıcı, sol menüde yer alan **Fiyatlandırma** bağlantısına tıkladığında fiyatlandırma sayfasına yönlendirilir. Bu sayfada Filarch’ın bireysel ve kurumsal lisans paketleri; paketlere ait limitler ve özellikler listelenir.

Her paket için yer alan “Satın Al ve Başla” butonuna tıklandığında, seçilen paketin ödeme sayfasına yönlendirilir.

- **Depolama:** Lisansa ait toplam depolama alanını ifade eder. Yüklenen tüm dosyalar bu limiti kullanır.
- **Kullanıcılar:** Lisans kapsamında birlikte çalışabilecek kullanıcı sayısını ifade eder. Bireysel lisanslarda bu limit 1’dir, kurumsal lisanslarda birden fazla kullanıcı aynı lisans altında çalışabilir.
- **Depolamalar:** Lisansa eklenebilecek harici depolama (ör. Google Drive, S3) sayısını ifade eder.
- **Çalışma Alanları:** Lisans kapsamında oluşturulabilecek çalışma alanı sayısını ifade eder.
- **Projeler:** Lisans kapsamında oluşturulabilecek proje sayısını ifade eder.
- **Klasör Sayısı:** Lisans kapsamında oluşturulabilecek toplam klasör sayısını ifade eder.
- **Dosya Sayısı:** Lisans kapsamında yüklenebilecek toplam dosya sayısını ifade eder.
- **Dış Proje Kullanımı:** Kullanıcının, başka bir lisans altındaki projelerde mevcut lisans özelliklerini kullanabilmesini ifade eder.
- **Dış Klasör Kullanımı:** Kullanıcının, başka bir lisans altındaki klasörlerde mevcut lisans özelliklerini kullanabilmesini ifade eder.
- **Özel Şablon Kullanımı:** Lisans kapsamında oluşturulabilecek özel proje şablonu sayısını ifade eder.
- **Bulut + On-Premise:** Dosyaların Filarch Cloud’da veya kullanıcının kendi depolama servisinde saklanabilmesini sağlar.
- **Özel Mail Formatları:** Lisans kapsamında sistem e-postalarının özel mail şablonları ile gönderilebilmesini ifade eder.

## 2. Ödeme

Kullanıcı, seçtiği lisans paketini satın almak için ödeme sayfasına yönlendirilir. Ödeme işlemi üç adımda tamamlanır:

- **Bilgiler:** Fatura ve kullanıcı bilgileri girilir.
- **Ek Paketler:** İsteğe bağlı ek paketler seçilir.
- **Ödeme:** Ödeme bilgileri girilerek satın alma işlemi tamamlanır.

### a. Bilgiler

![purchase_information](https://i.hizliresim.com/9r34y3h.png) Şekil 1.3 – Satın Alma / Ödeme Akışı – Bilgiler Adımı

Bilgiler sekmesinde, sol tarafta satın alınacak pakete ait özellikler ve fiyat bilgileri görüntülenir. Sağ tarafta ise kullanıcıdan fatura bilgileri istenir.

Formda dikkat edilmesi gerekenler:

- Posta kodu alanı haricindeki tüm alanlar zorunludur.
- Ad ve soyad alanları yalnızca harf içermelidir.
- Geçerli bir e-posta adresi girilmelidir.
- Geçerli bir iletişim numarası girilmelidir.
- Bireysel satın alımlarda geçerli bir T.C. Kimlik Numarası, kurumsal satın alımlarda ise kurum adı, vergi dairesi ve vergi numarası girilmelidir.

Form başarılı şekilde doldurulduğunda “Devam Et” butonuna tıklanarak Ek Paketler sekmesine geçilir.

### b. Ek Paketler

![purchase_additional_packages](https://i.hizliresim.com/klyqg79.png) Şekil 1.4 – Satın Alma / Ödeme Akışı – Ek Paketler Adımı

Ek Paketler sekmesinde, sol tarafta seçilen paketin özellikleri ve güncel fiyatı görüntülenir. Sağ tarafta ise kullanıcıdan isteğe bağlı ek paket seçimleri alınır.

Ek paket eklemek istemeyen kullanıcılar “Devam Et” butonuna tıklayarak doğrudan Ödeme sekmesine geçebilir.

Formda dikkat edilmesi gerekenler:

- Bireysel satın alımlarda ek kullanıcı eklenemez. Ek kullanıcı seçeneği yalnızca kurumsal paketler için geçerlidir.
- Ek kullanıcı ücreti, paket ücreti × ek kullanıcı sayısı şeklinde hesaplanır.
- Ek depolama alanı, TB bazında artırılır.
- Ek kullanıcı ve ek depolama alanı alanları yalnızca pozitif sayısal değer kabul eder.
- Ekle butonuna tıklandığında, sol taraftaki fatura bilgileri güncellenir ve yeni toplam fiyat hesaplanır.
- Kullanıcı dilediği zaman eklediği paketleri kaldırabilir; fiyat buna göre yeniden hesaplanır.

Seçimler tamamlandıktan sonra “Devam Et” butonuna tıklanarak Ödeme sekmesine geçilir.

### c. Ödeme

![purchase](https://i.hizliresim.com/1cgvv9e.png) Şekil 1.5 – Satın Alma / Ödeme Akışı – Ödeme Adımı

Ödeme sekmesinde, sol tarafta satın alınacak pakete ait özellikler ve toplam fiyat görüntülenir. Sağ tarafta ise ödeme yapılacak banka bilgileri listelenir.

Kullanıcı, belirtilen banka hesabına ödemeyi gerçekleştirdikten sonra “Ödemeyi Tamamla” butonuna tıklayarak ödeme rezervasyonunu oluşturur.

İşlem tamamlandığında kullanıcıya bilgilendirme e-postası gönderilir.