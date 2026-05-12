# Filarch Sync - Kurulum Kılavuzu

Bu kılavuz, Filarch Sync uygulamasını bilgisayarınıza kurmanız için adım adım talimatlar içerir.

---

## Sistem Gereksinimleri

- **Windows**: Windows 10 veya üzeri (64-bit)
- **macOS**: macOS 10.13 (High Sierra) veya üzeri
- **Linux**: Ubuntu 18.04+, Fedora 30+ veya benzeri dağıtımlar (64-bit)

**Donanım**: 4 GB RAM, 200 MB disk alanı + senkronize edilecek dosyalar için ek alan

---

## Windows Kurulumu

1. **İndir**
   - `Filarch Sync Setup.exe` dosyasını [filarch.com](https://filarch.com) adresinden indirin

2. **Kurulumu Başlat**
   - İndirilen dosyaya çift tıklayın
   - Güvenlik uyarısı çıkarsa "Yine de çalıştır" seçeneğine tıklayın

3. **Adımları İzle**
   - Lisans sözleşmesini kabul edin
   - "Kur" düğmesine tıklayın
   - Yönetici izni isterse "Evet" deyin

4. **Uygulamayı Aç**
   - Kurulum tamamlandığında "Uygulamayı şimdi başlat" seçeneğini işaretleyin
   - Veya masaüstündeki kısayolu kullanın

---

## macOS Kurulumu

1. **İndir**
   - `Filarch Sync.pkg` dosyasını indirin

2. **Kurulumu Başlat**
   - İndirilen dosyaya çift tıklayın
   - Güvenlik uyarısı çıkarsa: Sistem Ayarları → Gizlilik ve Güvenlik → "Yine de aç"

3. **Kurulumu Tamamla**
   - "Devam" ve ardından "Yükle" düğmelerine tıklayın
   - Yönetici şifrenizi girin

4. **Uygulamayı Aç**
   - Applications klasöründen "Filarch Sync" uygulamasına çift tıklayın
   - Veya Spotlight'ta (Cmd+Space) "Filarch Sync" aratın

---

## Linux Kurulumu

### Ubuntu / Debian

1. `Filarch Sync.deb` dosyasını indirin
2. Dosyaya çift tıklayarak paket yöneticisi ile yükleyin
   
   Veya terminal ile:
   ```
   sudo dpkg -i "Filarch Sync.deb"
   ```

### Fedora / RHEL

1. `Filarch Sync.rpm` dosyasını indirin
2. Terminal ile:
   ```
   sudo rpm -i "Filarch Sync.rpm"
   ```

### Diğer Dağıtımlar (AppImage)

1. `Filarch Sync.AppImage` dosyasını indirin
2. Sağ tıklayın → Özellikler → "Çalıştırılabilir olarak izin ver" seçeneğini işaretleyin
3. Dosyaya çift tıklayarak çalıştırın