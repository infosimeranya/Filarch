# Depolama (Storages)

Bu doküman, Filarch uygulamasındaki Depolama sayfasının işlevselliğini açıklar.
Bu sayfa, verilerinizin saklandığı depolama çözümlerini görüntülemenizi ve yönetmenizi sağlar.

![storages.png](http://docs.filarch.com/media/uploads/storages.png)  
*Şekil 1 – Depolama Alanları (Storages) Ekranı*

## Sayfa Bileşenleri

### 1. Depolama Alanı Listesi
Sayfanın ana bölümünde, mevcut tüm depolama alanlarınız liste halinde görüntülenir. Her bir depolama alanı için aşağıdaki bilgiler yer alır:
- **Storage Name:** Depolama alanına verdiğiniz özel isim.
- **Storage Type:** Depolama alanının türünü gösterir (ör. Filarch Cloud, Amazon S3, Google Drive).
- **Created Date:** Depolama alanının oluşturulduğu tarihi ifade eder.

### 2. Depolama Alanı Oluştur (Storage Create)
Sayfanın üst kısmında yer alan **Storage Create** butonu, yeni bir depolama alanı oluşturmanızı sağlar. Bu butona tıklandığında süreç şu adımlarla ilerler:

1. **Depolama Türü Seçimi:** Öncelikle kullanılacak servis (ör. Google Drive) seçilir.
2. **Bağlantı Yöntemi Belirleme:** Google Drive gibi servisler için iki farklı erişim yöntemi sunulur:
    - **Google ile bağlan (Önerilen):** Hızlı ve kullanıcı dostu yöntemdir. Doğrudan Google hesabınızla yetkilendirme yaparak bağlantı kurulur.
    - **Service account kullan (Gelişmiş):** Teknik yapılandırma gerektiren, servis hesabı anahtarları (JSON) ile kurulan profesyonel bağlantı yöntemidir.

![google-drive-baglanti.png](https://i.hizliresim.com/dm8hr67.png)  
*Şekil 2 – Google Drive Bağlantı Yöntemi ve Klasör Seçimi*

3. **Hesap Yetkilendirme ve Kök Klasör Seçimi:**
    - Bağlantı kurulduktan sonra ("Google Drive bağlandı" onayı görülür), depolama alanı olarak kullanılacak **Kök Klasör** seçilir.
    - Seçilen klasör altındaki veriler Filarch üzerinde yönetilebilir hale gelir.
4. **Kaydet:** Tüm bilgiler girildikten sonra "Kaydet" butonu ile işlem tamamlanır.

### 3. Arama (Search by name)
Depolama alanı sayısı arttığında, aradığınız depolamayı hızlıca bulmak için **Search by Name** alanı kullanılabilir. Yazmaya başladığınızda liste otomatik olarak filtrelenir.

### 4. Sayfalama (Pagination)
Listenin sağ alt kısmında yer alan kontroller sayesinde sayfalar arası geçiş yapılabilir ve sayfa başına gösterilecek öğe sayısı (ör. 10 / page) ayarlanabilir.