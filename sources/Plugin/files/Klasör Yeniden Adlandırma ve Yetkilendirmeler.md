# Klasör Erişim Yönetimi

Filarch'ta erişim yönetimi klasör granülaritesinde çalışır. Aynı proje içindeki farklı klasörlere farklı kullanıcı listeleri atayabilir; yetkisiz üyeler o klasörü sol panelde göremez.

---

## Erişim Listesi Düzenleme

### Klasör izinlerini açmak

1. Sol panelde klasöre **sağ tıklayın** → **İzinleri Düzenle**'yi seçin
2. Ya da klasörün detay ekranındaki **İzinler** sekmesine gidin

### Kullanıcı eklemek

1. **Kullanıcı Ekle** alanına e-posta adresini girin
2. Erişim tipini seçin (Okuma / Yazma)
3. **Ekle** butonuna tıklayın

E-posta bazlı davet yöntemi sayesinde kullanıcıyı sisteme kayıt ettirmeden de klasöre erişim tanımlanabilir.

> **Ekran Görüntüsü:** Klasör izin paneli — kullanıcı listesi ve erişim tipi seçimi
> ![]()


### Kullanıcı çıkarmak

Mevcut erişim listesindeki kullanıcının yanındaki **Kaldır** butonuna tıklayın. Tüm değişiklikler tek API isteğiyle uygulanır.

---

## Gizlilik Prensibi

Erişim listesi dışındaki kullanıcılar klasörü **hiç göremez** — "izin yok" mesajı yerine klasör sol panelden tamamen kaybolur. Kullanıcı erişemeyeceği içeriklerin varlığından haberdar olmaz.

---

## Örnek Yapılandırmalar

### Alt yüklenici erişimi

> Proje konsorsiyumunda üç şirket var. Her şirketin yalnızca kendi iş paketi klasörüne erişmesi gerekiyor.

1. `Altyapı/Firma-A` klasörünü açın → izinleri düzenleyin
2. Firma A çalışanlarının e-postalarını girin
3. Aynı adımı `Firma-B` ve `Firma-C` için tekrarlayın

Her şirketin kullanıcısı giriş yaptığında yalnızca kendi klasörünü görür; diğer şirketlerin dosyaları tamamen gizli kalır.

### Dış danışman erişimi

Bir dış danışmana yalnızca `Raporlar/Danışman-Gözden Geçirme` klasörüne okuma erişimi tanımlayın; danışman projenin geri kalanını göremez.

---

## Sık Sorulan Sorular

**Alt klasörler üst klasörün erişim listesini miras alır mı?**
Hayır. Her klasörün erişim listesi bağımsız yönetilir. Bir üst klasöre erişim vermek otomatik olarak alt klasörlere yayılmaz.

**Klasör sahibi kendi izin listesini düzenleyebilir mi?**
Evet. Klasör sahibi rolüne sahip kullanıcı kendi izin listesini düzenleyebilir; proje yöneticisi müdahalesi gerekmez.