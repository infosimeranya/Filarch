## Kurulum

### Windows

1. **Kurulum Dosyasını İndirin** — Resmi web sitesinden `Filarch Sync Setup.exe` dosyasını indirin.
2. **Kurulum Sihirbazını Çalıştırın** — İndirilen `Filarch Sync Setup.exe` dosyasına çift tıklayın, kurulum sihirbazı açılacaktır.
3. **Talimatları Takip Edin** — Kurulum klasörünü seçin (varsayılan: `C:\Program Files\Filarch Sync`) ve "Kur" seçeneğine tıklayın.
4. **Kurulum Tamamlandı** — Kurulum tamamlanınca uygulamayı başlatabilir, masaüstü kısayolunu kullanabilirsiniz.

### macOS

1. **PKG Dosyasını İndirin** — Resmi web sitesinden `Filarch Sync.pkg` dosyasını indirin.
2. **Kurulumu Başlatın** — İndirilen `.pkg` dosyasına çift tıklayın ve kurulum sihirbazını açın.
3. **Yükleme Adımları** — Talimatları izleyin, arka plan servisi kurulumu için yönetici şifresi istenebilir, "Yükle" butonuna basın.
4. **Uygulamayı Çalıştırın** — Applications klasöründen "Filarch Sync" uygulamasını açın.

### Linux

1. **DEB Dosyasını İndirin** — Resmi web sitesinden `Filarch Sync.deb` dosyasını indirin.
2. **Uygulamayı Yükleyin** — Dosyaya çift tıklayarak paket yöneticisi ile yükleyin.
3. **Uygulamayı Çalıştırın** — Uygulama menüsünde "Filarch Sync" uygulamasını bulun ve açın.

## İmzalanmamış Uygulamalar için Güvenlik Bildirimi

Filarch Sync, bazı işletim sistemlerinde dijital olarak imzalanmamış bir uygulama olarak algılanabilir. Bu durumda Windows ve macOS, varsayılan güvenlik politikaları gereği kurulum veya çalıştırma işlemini engelleyebilir. Aşağıda belirtilen adımlar, uygulamanın kullanıcının açık onayıyla kurulabilmesini sağlamaktadır.

> **Önemli:** Aşağıdaki işlemler yalnızca uygulamanın resmi Filarch web sitesinden indirildiğinden emin olunması halinde uygulanmalıdır.

### Windows (Microsoft Defender SmartScreen)

1. `Filarch Sync Setup.exe` dosyası çalıştırıldığında Microsoft Defender SmartScreen uyarısı görüntülenebilir.
2. Uyarı ekranında **“Daha fazla bilgi”** bağlantısına tıklayın.
3. **“Yine de çalıştır”** seçeneğini seçerek kuruluma devam edin.
4. Kurulum sihirbazı normal şekilde başlatılacaktır.

> Not: Bazı sistemlerde dosya özellikleri altında **“Engellemeyi kaldır”** seçeneği bulunabilir. Bu seçenek işaretlenerek uyarı devre dışı bırakılabilir.

### macOS (Apple Gatekeeper)

1. `Filarch Sync.pkg` dosyası çalıştırıldığında geliştirici doğrulamasına ilişkin bir uyarı görüntülenebilir.
2. **Sistem Ayarları → Gizlilik ve Güvenlik** menüsüne gidin.
3. Güvenlik bölümünde, engellenen uygulamaya ilişkin bir bildirim görüntülenecektir.
4. **“Yine de Aç”** seçeneğini tıklayın.
5. Yönetici kimlik doğrulamasını tamamlayarak kurulumu sürdürün.

> Alternatif olarak, `.pkg` dosyası **Ctrl + tıklama → Aç** yöntemiyle başlatılarak aynı onay süreci tetiklenebilir.

---