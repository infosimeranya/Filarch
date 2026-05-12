## Filarch Sync'i Bilgisayarınızdan Kaldırma (Uninstall)

Uygulamayı bilgisayarınızdan kaldırmak için:

### Windows

**Yöntem 1: Kontrol Paneli Üzerinden**

1. **Kontrol Paneli** → **Programlar** → **Programları Kaldır**'ı açın
2. Listeden **"Filarch Sync"** bulun
3. Sağ tıklayıp **"Kaldır"** seçeneğini tıklayın
4. Onay mesajında **"Evet"** seçeneğini tıklayın
5. Kaldırma işlemi tamamlanana kadar bekleyin

**Yöntem 2: Ayarlar Uygulaması Üzerinden**

1. **Başlat Menüsü** → **Ayarlar** (⚙️) → **Uygulamalar** → **Uygulamalar ve özellikler**
2. Listeden **"Filarch Sync"** bulun
3. **"Kaldır"** butonuna tıklayın
4. Onay mesajında **"Kaldır"** ı tıklayın

**Yöntem 3: Kurulum Dosyası Üzerinden**

- Orijinal `Filarch Sync Setup.exe` dosyasını çalıştırın
- Kaldırma seçeneğini seçin

### macOS

Uygulama arka planda çalışan bir sistem servisi (Daemon) içerdiğinden, sadece Uygulamalar klasöründen silmek yeterli değildir. Tamamen kaldırmak için Terminal uygulamasını açın ve aşağıdaki komutları sırasıyla uygulayın:

```bash
# 1. Servisi durdurun ve kaldırın
sudo launchctl bootout system/com.filarch.sync.daemon
sudo rm /Library/LaunchDaemons/com.filarch.sync.daemon.plist

# 2. Daemon ve Uygulama dosyalarını silin
sudo rm /usr/local/bin/filarch-sync-daemon
sudo rm -rf /Applications/Filarch\ Sync.app
```

### Linux

**Yöntem 1: AppImage Dosyasını Sil**

```bash
rm ~/Filarch\ Sync.AppImage
```

**Yöntem 2: Paket Yöneticisi Üzerinden** (Eğer paket olarak yüklendi ise)

```bash
# Debian/Ubuntu
sudo apt-get remove filarch-sync

# Fedora
sudo dnf remove filarch-sync

# Arch
sudo pacman -R filarch-sync
```

### Verilerin Silinmesi

**Uygulamayı Tamamen Kaldırmak İçin:**

Uygulamaya ait ayarlar ve önbellek dosyalarını da silmek istiyorsanız:

**Windows:**

```
C:\Users\[YourUsername]\AppData\Local\Filarch Sync
C:\Users\[YourUsername]\AppData\Roaming\Filarch Sync
```

**macOS:**

```
~/Library/Application Support/Filarch Sync
~/Library/Preferences/com.filarch.sync.plist
```

**Linux:**

```
~/.config/Filarch Sync
~/.local/share/Filarch Sync
```

Kullandığınız işletim sistemine göre terminale bu kodları yazabilirsiniz (**İleri Seviye**)

---