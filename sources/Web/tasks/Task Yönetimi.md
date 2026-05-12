# Görev Modülü

Filarch'ın Görev Modülü, projeye özgü görevleri oluşturmanıza, organize etmenize, takip etmenize ve raporlamanıza imkân tanır. Görevler, dosya yöneticisiyle paylaşılan aynı klasör hiyerarşisine bağlıdır; bu sayede belge ve görev bağlamı her zaman aynı çatı altında tutulur.

---

## İçindekiler

1. Görev Listesi ve Navigasyon
   - Klasör Ağacıyla Navigasyon
   - Liste Görünümü
   - Gantt Görünümü
   - Filtre Paneli
2. Görev Detay (Drawer)
   - Onay Zinciri (COA)
   - Görev Bağımlılıkları
   - Rol Bazlı Efor Tahmini
   - Yorumlar ve Tartışma
3. Raporlama
   - Rapor Şablonları
   - Rapor Oluşturma ve Dışa Aktarma

---

## Görev Listesi ve Navigasyon

### Klasör Ağacıyla Navigasyon

Görevler, projenin dosya klasörü yapısıyla birebir örtüşen bir hiyerarşide organize edilir. Görev Modülü'nün sol panelinde proje klasör ağacı yer alır; buradan seçilen klasöre ait görevler sağ panelde anında listelenir.

**Nasıl Kullanılır**

1. Sol paneldeki klasör ağacında ilgili klasöre tıklayın.
2. Görev listesi o klasöre ait görevleri getirir; diğer disiplinlerin görevleri görünmez.
3. İç içe geçmiş klasörleri **▶** (genişlet) / **▼** (daralt) düğmeleriyle gezin.
4. Proje adına (ağacın köküne) tıklayarak projenin tüm görevlerini tek listede görüntüleyin.

![Klasör ağacı ve görev listesi](01_folder_tree_task_list.png)
*Şekil 1.0: Klasör ağacı ve görev listesi*

---

### Liste Görünümü

Görev listesi; görev başlığı, sorumlu kullanıcı, öncelik, statü, tamamlanma yüzdesi ve termin tarihi gibi sütunlarla görevlerin tablo formatında görüntülenmesini sağlar. Varsayılan görünüm budur.

![Görev listesi tablo görünümü](01_folder_tree_task_list.png)
*Şekil 1.1: Görev listesi tablo görünümü*

---

### Gantt Görünümü

Gantt görünümü, görevleri ve alt görevleri zaman çizelgesi üzerinde hiyerarşik çubuk grafiği olarak görselleştirir. **Gün**, **Hafta** ve **Ay** olmak üç farklı zaman çözünürlüğü desteklenir.

**Temel Özellikler**

| Özellik | Açıklama |
|---|---|
| Ana / Alt Görev Rengi | Ana görevler mor, alt görevler mavi |
| İlerleme Çubuğu | Kapanış statüsüne göre otomatik hesaplanır |
| Tooltip | Başlangıç/termin tarihi, ilk üç sorumlu ve anlık statü |
| Bugün Çizgisi | Morumsu şeffaf dikey şerit |
| Detay Drawer | Çubuğa tıklayarak görev detayını Gantt'tan çıkmadan açın |

**Gantt'a Geçme Adımları**

1. Görev listesinin sağ üstündeki **Gantt** görünüm düğmesine tıklayın.
2. Zaman çözünürlüğünü üst araç çubuğundan **Gün / Hafta / Ay** olarak seçin.
3. Alt görev barındıran ana görevlerde **▶** simgesine tıklayarak alt görevleri genişletin.
4. Herhangi bir çubukta üzerine gelerek tooltip'i görün; çubuğa tıklayarak detay drawer'ını açın.

![Gantt görünümü ana ve alt görevler](http://docs.filarch.com/media/uploads/gantt.png)
*Şekil 1.2: Gantt görünümü ana ve alt görevler*
![Gantt tooltip görev detayları](http://docs.filarch.com/media/uploads/gantt_tooltip.png)
*Şekil 1.3: Gantt tooltip görev detayları*

---

### Filtre Paneli

Görev listesinin üstünde yer alan filtre paneli; **statü**, **öncelik**, **atanan kullanıcı** ve **serbest metin arama** boyutlarında eş zamanlı filtreleme yapar. Aktif filtreler renk değiştirerek devrede olduğunu belirtir; filtreler korunarak liste ve Gantt görünümleri arasında geçiş yapılabilir.

**Filtre Uygulamak**

1. **Arama kutusu:** Yazmaya başladığınızda görev başlıkları anlık filtrelenir.
2. **Statü:** Projeye özgü statüler listelenir; seçilen statüdeki görevler görüntülenir.
3. **Öncelik:** Projeye özel öncelik seçeneklerini seçin.
4. **Atanan Kullanıcı:** Sorumluya göre daraltın.
5. Aktif filtreyi kaldırmak için ilgili filtrenin üzerindeki **×** simgesine tıklayın.

![Filtre paneli aktif filtre](http://docs.filarch.com/media/uploads/filter_rN3ygWn.png)
*Şekil 1.4: Filtre paneli aktif filtre*

---

## Görev Detay (Drawer)

Bir görev satırına tıklandığında sağ taraftan kayan detay drawer'ı açılır. Drawer içinde birden fazla sekme yer alır: **Genel Bilgiler**, **Onay Zinciri (COA)**, **Bağımlılıklar**, **Efor Tahmini** ve **Aktivite (Yorumlar)**.

![Görev detay drawer genel bilgiler sekmesi](http://docs.filarch.com/media/uploads/task_drawer_general.png)
*Şekil 1.5: Görev detay drawer genel bilgiler sekmesi*

---

### Onay Zinciri (COA)

Görev Onay Zinciri (COA — Chain of Approval), bir görev belirli bir statüye geçtiğinde otomatik devreye giren, proje rolü hiyerarşisine bağlı sıralı onay mekanizmasıdır. Her adım tamamlanmadan bir sonraki açılmaz.

**COA Nasıl Çalışır**

| Adım | Açıklama |
|---|---|
| Otomatik Tetikleme | Görev hedef statüye geçtiğinde COA zinciri başlar |
| Sıralı İlerleme | Adımlar sırayla açılır; önceki onaylanmadan sonraki beklemede kalır |
| Zaman Limiti | Her adım için tanımlı gün limiti; gecikme görsel uyarıyla belirtilir |
| Onay Verme | Yetkili kullanıcı drawer'daki COA sekmesinde onaylar |
| Red Gerekçesi | Tanımlı listeden reddetme sebebi seçilerek zincir reddedilir |

**Onay Süreci — Adım Adım**

1. Drawer'da **COA / Onay Zinciri** sekmesini açın.
2. Zincir timeline'ında mevcut adımın durumunu (beklemede, onaylandı, reddedildi) görün.
3. Onay bekleniyor ise **Onayla** düğmesine tıklayın.
4. Reddetmek için **Reddet** düğmesine tıklayın ve açılan listeden gerekçeyi seçin.

![COA onay zinciri timeline](task_coa.png)
*Şekil 1.6: COA onay zinciri timeline*
![Reddetme gerekçe seçim listesi](http://docs.filarch.com/media/uploads/task_reject.png)
*Şekil 1.7: Reddetme gerekçe seçim listesi*

---

### Görev Bağımlılıkları

Görevler arasındaki mantıksal önkoşul ilişkileri üç bağımlılık tipiyle tanımlanabilir: **FS** (Finish-to-Start), **SS** (Start-to-Start) ve **FF** (Finish-to-Finish). İsteğe bağlı gecikme süresi (lag) dakika cinsinden girilebilir.

**Bağımlılık Tipleri**

| Tip | Açıklama | Örnek Kullanım |
|---|---|---|
| FS | Önceki görev bitince bu görev başlayabilir | Temel atma → Duvar örme |
| SS | Önceki görev başlayınca bu görev başlayabilir | Şantiye hazırlık → Malzeme siparişi |
| FF | Önceki görev bitince bu görev bitebilir | Test → Dokümantasyon güncelleme |

**Bağımlılık Ekleme**

1. Görev drawer'ında **Bağımlılıklar** sekmesini açın.
2. **Yeni Bağımlılık Ekle** düğmesine tıklayın.
3. **Yön** seçin: *Bu görev başka bir görevi engelliyor mu* (**Blocking**) yoksa *başka bir görevi mi bekliyor* (**Waiting**)?
4. **Bağımlılık tipini** seçin (FS / SS / FF).
5. Hedef görevi ID veya konu aramasıyla bulun.
6. (İsteğe bağlı) **Lag** süresini dakika cinsinden girin.
7. **Kaydet** ile bağımlılığı ekleyin.

![Bağımlılık ekleme formu ve kayıtlı bağımlılıklar listesi](http://docs.filarch.com/media/uploads/task_bagimlilik.png)
*Şekil 1.8: Bağımlılık ekleme formu ve kayıtlı bağımlılıklar listesi*

---

### Rol Bazlı Efor Tahmini

Her göreve dahil olacak proje rolleri için bağımsız planlanan süre (tahmin) girilebilir. Gerçekleşen efor ve toplantı eforu ayrı kaydedilir; tamamlanma yüzdesi bu verilerden otomatik hesaplanır.

**Kavramlar**

| Kavram | Açıklama |
|---|---|
| Planlanan Süre | Her proje rolü için öngörülen süre (dakika) |
| Gerçekleşen Efor | Ekip üyelerinin fiilen kaydettiği çalışma süresi |
| Toplantı Eforu | Koordinasyon kaynaklı süre (görev eforundan ayrı) |
| Tamamlanma % | Planlanan / gerçekleşen efor oranından otomatik hesaplanır |

**Tahmin Girme**

1. Drawer'da **Efor / Zaman Takibi** sekmesini açın.
2. **Tahmin Ekle** bölümünde proje rolünü seçin.
3. Planlanan süreyi dakika cinsinden girin ve kaydedin.
4. Aynı rol için yalnızca bir tahmin girilebilir; mevcut tahminler düzenlenebilir veya silinebilir.

![Rol bazlı planlanan süreler listesi](http://docs.filarch.com/media/uploads/task_planned_roles.png)
*Şekil 1.9: Rol bazlı planlanan süreler listesi*
![Gerçekleşen efor ve toplantı eforu karşılaştırması](http://docs.filarch.com/media/uploads/task_effort.png)
*Şekil 1.10: Gerçekleşen efor ve toplantı eforu karşılaştırması*

---

### Yorumlar ve Tartışma

Görev drawer'ının **Aktivite** sekmesi, her göreve özgü iş parçacıklı (threaded) yorum sistemi sunar. Yorumlar zaman damgası ve yazar bilgisiyle kalıcı olarak kaydedilir; kararlar ve tartışmalar görev üzerinde arşivlenir.

**Yorum Gönderme**

1. Drawer'da **Aktivite** sekmesini açın.
2. Alttaki metin kutusuna yorumunuzu yazın.
3. **Enter** tuşuyla gönderin (Shift+Enter yeni satır açar).

**Yoruma Yanıt Verme (Thread)**

1. Yanıtlamak istediğiniz yorumun üzerindeki **Yanıtla** düğmesine tıklayın.
2. Yanıt formu açılır; yanıtınızı yazın ve **Enter** ile gönderin.
3. Yanıt, "Şuna yanıt: [Yazar Adı]" bağlamıyla iş parçacığı oluşturur.
4. Yanıt formunu iptal etmek için **Escape** tuşuna basın.

![Aktivite sekmesi iş parçacıklı yorum sistemi](http://docs.filarch.com/media/uploads/task_activity_sCRTf1L.png)
*Şekil 1.11: Aktivite sekmesi iş parçacıklı yorum sistemi*

---

## Raporlama

Görev raporları **Ayarlar → Raporlama** bölümünden yönetilir. İki aşamalı çalışır: önce yeniden kullanılabilir şablon oluşturulur, ardından şablon veya anlık filtrelerle rapor çalıştırılır.

---

### Rapor Şablonları

Şablonlar, sıkça kullanılan rapor filtre kombinasyonlarını isimlendirip kaydederek tek tıkla tutarlı raporlar çalıştırmanızı sağlar.

**Şablon İçinde Tanımlanabilecek Filtreler**

- Dahil edilecek projeler (çoklu seçim)
- Öncelik grupları
- Sorumlu kullanıcılar
- Başlangıç / bitiş tarih aralığı
- Alt görevlerin rapora dahil edilip edilmeyeceği

**Şablon Oluşturma**

1. **Ayarlar → Raporlama → Şablonlar** sayfasına gidin.
2. **Yeni Şablon** düğmesine tıklayın.
3. Şablona benzersiz bir ad verin (örn. *Haftalık Gecikme Takibi*).
4. Proje, öncelik, sorumlu ve tarih aralığı filtrelerini yapılandırın.
5. Alt görev dahil/hariç tercihini belirleyin.
6. **Kaydet** ile şablonu oluşturun.

**Favori İşaretleme**

Şablon listesinde yıldız simgesine tıklayarak sık kullandığınız şablonları listeye sabitleyin.

![Rapor şablonları listesi ve yeni şablon oluşturma formu](http://docs.filarch.com/media/uploads/create_report_template.png)
*Şekil 1.12: Rapor şablonları listesi ve yeni şablon oluşturma formu*

---

### Rapor Oluşturma ve Dışa Aktarma

Rapor motoru iki modda çalışır: **Şablon Modu** (kayıtlı şablonu seç, tek tıkla çalıştır) ve **Anlık Filtre Modu** (filtreler manuel olarak girilir).

**Rapor İçeriği**

Oluşturulan rapor aşağıdaki bölümlerden oluşur:

| Bölüm | İçerik |
|---|---|
| Üst Başlık | Proje adı, yönetici bilgisi, tarih aralığı |
| Özet | Toplam, tamamlanan, devam eden ve başlamayan görev sayısı |
| Efor Özeti | Toplam görev eforu ve toplantı kaynaklı efor (ayrı ayrı) |
| Durum Dağılımı | Statü bazında görev sayısı ve yüzdesi (renk kodlu) |
| Öncelik Dağılımı | Öncelik bazında görev sayısı ve yüzdesi |
| Otomatik Açıklama | Rapor verilerinden üretilen hazır özet metni |
| Detay Tablosu | Görev başlığı, sorumlu, öncelik, statü, tamamlanma %, efor, gecikme durumu ve tarihler |

**Rapor Çalıştırma**

1. **Ayarlar → Raporlama → Rapor Oluştur** sayfasına gidin.
2. **Şablon Modu:** Listeden bir şablon seçin; filtreler otomatik dolar, **Çalıştır** düğmesine tıklayın.
   **Anlık Filtre Modu:** Proje, öncelik, sorumlu, tarih aralığı ve alt görev tercihini manuel girin, ardından **Çalıştır** düğmesine tıklayın.
3. Rapor sonuçları ekranda görüntülenir.
4. **Excel** veya **PDF** olarak dışa aktarmak için sağ üstteki dışa aktar düğmesini kullanın.

![Rapor çalıştırma ekranı şablon seçimi](http://docs.filarch.com/media/uploads/generate_task_report.png)
*Şekil 1.13: Rapor çalıştırma ekranı şablon seçimi*
![Rapor sonuçları özet ve durum dağılımı](http://docs.filarch.com/media/uploads/generated_task_report1.png)
*Şekil 1.14: Rapor sonuçları özet ve durum dağılımı*
![Rapor detay tablosu](http://docs.filarch.com/media/uploads/task_report_detail.png)
*Şekil 1.15: Rapor detay tablosu*
![Excel ve PDF dışa aktarım butonları](http://docs.filarch.com/media/uploads/generated_task_report2.png)
*Şekil 1.16: Excel ve PDF dışa aktarım butonları*

---

## Karşılaştırmalı Avantajlar

| Özellik | Filarch | Jira | Asana | ClickUp |
|---|---|---|---|---|
| Klasör bazlı görev navigasyonu | ✅ Dosya yöneticisiyle ortak | ❌ | ❌ | ❌ |
| Gantt — kutudan çıkar, ek lisans yok | ✅ | ❌ Ek lisans | ✅ | ✅ |
| FS/SS/FF + Lag bağımlılık desteği | ✅ | ✅ (lag yok) | ❌ | Kısmi |
| Çok adımlı COA onay zinciri | ✅ | ❌ | ❌ | ❌ |
| Rol bazlı efor tahmini | ✅ | ❌ | ❌ | ❌ |
| Toplantı eforu ayrı takip | ✅ | ❌ | ❌ | ❌ |
| Threaded (iş parçacıklı) yorumlar | ✅ | ❌ Düz liste | ❌ | ❌ |
| Rapor şablonu + anlık filtre modları | ✅ | Kısmi | ❌ | Kısmi |
| Excel + PDF rapor çıktısı | ✅ | ❌ | ❌ | ✅ |