# Görev Yönetimi

Filarch Görev Modülü, ClickUp benzeri esnek durum sistemi, çok adımlı onay zincirleri ve Gantt görünümüyle proje görevlerini uçtan uca yönetmenizi sağlar.

Sol gezinme çubuğundaki **onay listesi simgesi** butonuna tıklayarak Görevler modülünü açın.

---

## Durum Grupları ve Özel Statüler

Çalışma Alanı düzeyinde kendi durum gruplarınızı oluşturun; her projenin iş akışını terminolojisiyle birlikte özelleştirin.

### Durum grubu oluşturma

1. **Task Settings → Durum Grupları** sekmesine gidin
2. **Yeni Durum Grubu** butonuna tıklayın
3. Gruba bir ad verin (örn. `Yazılım İş Akışı`)
4. Durum kalemleri ekleyin: her kalem için **ad**, **renk** ve kapanış bayrağı belirleyin

> **Kapanış statüsü:** `is_closing_status` bayrağı işaretlenen kaleme geçiş, görevi tamamlanmış sayar. Tamamlanma yüzdesi otomatik hesaplanır.

5. Durum grubunu ilgili projeye atayın

> **Ekran Görüntüsü:** Task Settings → Durum Grupları — durum kalemleri ve renk seçimi
> ![task-management-status-1.png](http://docs.filarch.com/media/uploads/task-management-status-1.png)

### Geçiş kuralları

- **Yasak Geçişler:** Belirli bir statüden hangi diğer statülere geçilemeyeceğini tanımlayın
- **Yasak Roller:** Belirli proje rollerindeki kullanıcıların bir statüye geçişini engelleyin

> **Ekran Görüntüsü:** Task Settings → Geçiş Kuralları — statüler arası geçişin kısıtlanması
> ![task-management-status-2.png](http://docs.filarch.com/media/uploads/task-management-status-2.png)

> **Ekran Görüntüsü:** Task Settings → Yetkilendirmeler — yetki kısıtlaması
> ![task-management-status-3.png](http://docs.filarch.com/media/uploads/task-management-status-3.png)

---

## Reddetme Sebepleri

Onay zincirinde bir statü geçişi reddedildiğinde onaylayıcı, önceden tanımlı listeden gerekçe seçmek zorundadır.

### Reddetme sebebi tanımlama

1. **Task Settings → Deny Reasons** sekmesine gidin
2. Çalışma Alanı ve durum grubunu seçin
3. **Yeni Sebep Ekle** → gerekçe metnini girin (örn. `Test başarısız`, `Eksik implementasyon`)
4. **Kaydet**

Her red, seçilen gerekçe ve zaman damgasıyla kayıt altına alınır.

> **Ekran Görüntüsü:** Task Settings → Reddetme Sebepleri — red sebebi oluşturma aşaması
> ![task-management-deny-reasons-1.png](http://docs.filarch.com/media/uploads/task-management-deny-reasons-1.png)

---

## Görev Öncelikleri

Her proje kendi öncelik setini bağımsız olarak tanımlar.

### Öncelik oluşturma

1. **Task Settings → Priorities** sekmesine gidin
2. Çalışma Alanı ve proje seçin
3. **Create Priority** → ad ve renk kodu (hex) girin
4. **Kaydet**

Görev oluştururken veya güncellerken bu liste öncelik alanından seçilir. Farklı projelerin öncelik isimleri ve renkleri birbirinden bağımsız tanımlanır.

> **Ekran Görüntüsü:** Task Settings → Öncelikler — öncelik oluşturma aşaması
> ![task-management-priorities-1.png](http://docs.filarch.com/media/uploads/task-management-priorities-1.png)

---

## Gantt Görünümü

Görev listesinden **Gantt** sekmesine geçerek görevleri zaman çizelgesinde görselleştirin.

### Görünüm modları

- **Gün** — günlük detay
- **Hafta** — sprint planlaması
- **Ay** — çeyreklik yol haritası

### Nasıl kullanılır?

- Alt görev içeren ana görevler **proje tipi** olarak işaretlenir; genişlet/daralt düğmesiyle hiyerarşi açılır
- Çubuk renkleri: ana görevler **mor**, alt görevler **mavi** ton alır
- Bir çubuğun üzerine gelin → başlangıç/termin tarihleri, atanan kullanıcılar ve anlık statü görünür
- Çubuğa veya satıra tıklayın → görev detay drawer'ı açılır; Gantt'tan çıkmadan düzenleme yapılır
- **Bugün çizgisi** morumsu şeffaf şeritle vurgulanır

> **Ekran Görüntüsü:** Gantt görünümü — ana/alt görev hiyerarşisi ve bugün çizgisi
> ![task-management-gantt-view.png](http://docs.filarch.com/media/uploads/task-management-gantt-view.png)

---

## Onay Zinciri (COA)

Belirli statülere geçiş için zorunlu kılınan çok adımlı onay mekanizması.

### COA nasıl çalışır?

1. Görev, COA tanımlı bir statüye geçmeye çalışır
2. Sistem onay zincirini otomatik başlatır
3. Her adım sırayla ilerler: önceki adım tamamlanmadan sonraki açılmaz
4. Onaylayıcı **Onayla** veya **Reddet** seçer
5. Reddetme durumunda tanımlı gerekçe listesinden seçim zorunludur
6. Tüm adımlar tamamlandığında statü değişimi gerçekleşir

### COA nasıl oluşturulur?

1. **Task Settings → Onay Akışları** sekmesine gidin
2. Çalışma Alanı ve proje seçin
3. **Akış Oluştur** → ad girin ve çalışma alanı seçin.
4. **Oluştur**

> **Ekran Görüntüsü:** COA onay zinciri timeline — adım durumları (beklemede / onaylandı / reddedildi)
> ![task-management-coa.png](http://docs.filarch.com/media/uploads/task-management-coa.png)

### Vekâlet (Proxy)

Onaylayıcı müsait değilse(izne çıkma durumu vb.) onay yetkisini başka bir kullanıcıya devredebilir:

1. Görev detayından **Vekâlet Ver** butonuna tıklayın
2. Hedef kullanıcıyı seçin
3. Hedef kullanıcı vekâleti **Kabul** veya **Reddeder**

> **Ekran Görüntüsü:** Vekâlet — oluşturma ekranı
> ![task-management-proxy.png](http://docs.filarch.com/media/uploads/task-management-proxy.png)

---

## Rol Bazlı Efor Tahmini

Her göreve proje rollerine göre ayrı planlanan süre girin; gerçekleşen efor bağımsız olarak kaydedilir.

### Tahmin girmek

1. Görev drawer'ını açın → **General** sekmesine gidin
2. **Planned** → proje rolünü ve dakika cinsinden süreyi girin
3. **Ekle**

Her rol için yalnızca bir tahmin girilebilir; aynı role çift tahmin girilmesi önlenir.

> **Ekran Görüntüsü:** Efor tahmini girme ekranı
> ![task-management-estimated.png](http://docs.filarch.com/media/uploads/task-management-estimated.png)

### Gerçekleşen efor kaydetmek

1. Görev drawer'ını açın → **General** sekmesine gidin
2. **Add Time** → Dakika cinsinden süreyi ve çalışma tarihini(isteğe bağlı) girin
3. **Kaydet**

Tamamlanma yüzdesi ve efor aşımı otomatik hesaplanır; aşım görsel uyarıyla işaretlenir.

> **Ekran Görüntüsü:** Gerçekleşen efor ekranı
> ![task-management-effort.png](http://docs.filarch.com/media/uploads/task-management-effort.png)

---

## Görev İçi Yorumlar

Görev drawer'ının **Aktivite** sekmesinde iş parçacıklı (threaded) yorum sistemi çalışır.

- Yoruma yanıt vermek için **Yanıtla**'ya tıklayın
- Yanıt, kimin yorumuna cevap verildiğini *"Şuna yanıt: [Ad Soyad]"* bağlamıyla gösterir
- **Enter** → yorum gönder
- **Shift+Enter** → yeni satır ekle
- **Escape** → yanıt formunu iptal et

Tüm yorumlar görev kaydında kalıcı olarak arşivlenir.

> **Ekran Görüntüsü:** Yorumlar — yorum yapma ekranı
> ![task-management-comment-1.png](http://docs.filarch.com/media/uploads/task-management-comment-1.png)

---

## Örnek İş Akışı

> Bir yazılım ekibi `Yapılacak → Geliştirmede → İncelemede → Test → Tamamlandı` statülerini tanımlar. `Test → Tamamlandı` geçişi COA ile korunur; test uzmanı onay vermeden görev kapanmaz. Test uzmanı geçişi reddederse `Test başarısız` veya `Eksik implementasyon` gerekçelerinden birini seçmek zorundadır.