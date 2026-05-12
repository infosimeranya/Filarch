## Çakışma Yönetimi (Conflict Management)

Senkronizasyon sırasında, aynı dosyanın hem sunucuda hem de yerel bilgisayarınızda değiştirilmesi durumunda çakışmalar (conflicts) oluşabilir. FilArch Sync, bu çakışmaları yönetmeniz için özel bir arayüz sunar.

### Adım 1: Çakışmalar Sekmesine Git

![Ekran Görüntüsü (Çakışmalar Ekranı)](http://docs.filarch.com/media/uploads/conflicts_screen.png) Şekil 1.7 – Çakışmalar Ekranı

> Bu alana uygun ekran görüntüsünü ekleyin. Önerilen dosya adı: `assets/screenshots/conflicts_screen.png`.

- Sol menüden "Çakışmalar" (Conflicts) seçeneğine tıklayın.
- Eğer çözülmemiş çakışmalar varsa, menü simgesinin yanında bir uyarı işareti görebilirsiniz.

### Adım 2: Çakışma Listesini İnceleyin

- Sol taraftaki listede tüm çakışan dosyalar görüntülenir.
- Her öğe şunları içerir:
  - Dosya adı ve yolu
  - Çakışma tarihi
  - Dosya türü simgesi

### Adım 3: Çakışmayı Önizleyin

![Ekran Görüntüsü (Çakışmalar Ekranı)](http://docs.filarch.com/media/uploads/conflicts_screen_compare.png) Şekil 1.8 – Çakışma Karşılaştırma Görünümü (Local / Remote)

- Sol menüden "Çakışmalar" (Conflicts) seçeneğine tıklayın.
- Eğer çözülmemiş çakışmalar varsa, menü simgesinin yanında bir uyarı işareti görebilirsiniz.
- Listeden bir çakışmaya tıklayın.
- Sağ tarafta karşılaştırma görünümü açılır:
  - **Metin Dosyaları:** Sol tarafta yerel (Local), sağ tarafta sunucu (Remote) içeriği yan yana gösterilir. Farklılıklar renkli olarak vurgulanır.
  - **Görseller:** Yerel ve sunucu görselleri karşılaştırılabilir.
  - **Diğer Dosyalar:** Dosya boyutu ve değişiklik tarihi gibi meta veriler gösterilir.

### Adım 4: Çakışmayı Çözün

Çakışmayı çözmek için iki seçenekten birini kullanın:

1.**Yerel Olanı Kullan (Use Local):** Yerel bilgisayarınızdaki versiyonu geçerli kabul eder. Sunucudaki versiyonun üzerine yazılır.

2.**Sunucudakini Kullan (Use Remote):** Sunucudaki versiyonu geçerli kabul eder. Yerel dosyanız sunucudaki versiyonla değiştirilir.

> **Dikkat:** Çözüm işlemi geri alınamaz. Seçiminizi yapmadan önce değişiklikleri dikkatlice inceleyin.

---