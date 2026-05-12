# Gerçek Zamanlı CAD İşbirliği

Filarch Collab Room, aynı dosya versiyonu üzerinde birden fazla kullanıcının eş zamanlı çizim yapmasını sağlar. Oda sahibi, katılım isteklerini ve çizim operasyonlarını onay mekanizmasıyla yönetir.

**Desteklenen uygulamalar:** AutoCAD, ZWCAD, GstarCAD

---

## Collab Room Başlatma

1. Filarch uygulamasında versiyona gidin ve indirip açın
3. İndirdiğiniz versiyonda yeşil renkteki **İşbirliği Başlat** butonuna tıklayın
4. **Oda Oluştur** butonuna tıklayın
5. Oda adını girin → **Oluştur**

Oda bu versiyona bağlı olarak oluşturulur. Oda sahibi siz olursunuz.

> **Ekran Görüntüsü:** Oda oluşturma ekranı
> ![realtime-collaboration-create.png](http://docs.filarch.com/media/uploads/realtime-collaboration-create.png)

---

## Odaya Katılma

Davet alan kullanıcılar şu adımları izler:

1. Filarch'ta ilgili versiyonu açın
2. **Odaya Katıl** butonuna tıklayın
3. Katılım isteği oda sahibine bildirim olarak iletilir
4. Oda sahibi isteği **kabul** ya da **reddedebilir**

Kabul edilen kullanıcılar aktif üye olarak odaya dahil edilir ve CAD uygulamalarında çizim senkronizasyonu başlar.

> **Ekran Görüntüsü:** Odaya katılma isteği
> ![realtime-collaboration-join.png](http://docs.filarch.com/media/uploads/realtime-collaboration-join.png)

---

## Çizim Senkronizasyonu

- Her kullanıcının çizim değişiklikleri (nesne ekleme, düzenleme, silme) diğer kullanıcılara gerçek zamanlı iletilir
- Master kullanıcı 5 saniyede bir heartbeat göndererek varlığını bildirir
- Oda sahipliği değişirse master rolü otomatik devredilir

---

## CollabRoom Paneli

CAD uygulaması içinde çalışan panel şunları gösterir:

- **Bağlı kullanıcılar** ve rolleri (oda sahibi / kullanıcı)
- **Aktivite geçmişi:** katılma, ayrılma, çizme, değiştirme, silme olayları
- **Bekleyen katılım istekleri**

> **Ekran Görüntüsü:** CollabRoom paneli — aktif kullanıcılar ve aktivite akışı
> ![realtime-collaboration-host.png](http://docs.filarch.com/media/uploads/realtime-collaboration-host.png)

---

## Odayı Kapatma

Oda sahibi odayı kalıcı olarak kapatabilir:

1. CollabRoom panelinden **Odadan Ayrıl** butonuna tıklayın
2. Tüm aktif üyeler odadan çıkarılır

---

## Sık Sorulan Sorular

**İnternet bağlantısı şart mı?**
Filarch Collab Room yerel daemon mimarisiyle çalışır; aynı ağ üzerindeki kullanıcılar internet bağlantısı olmadan da işbirliği yapabilir.

**Bağlantım koptu, odadan çıktım mı?**
Socket.IO otomatik yeniden bağlantı (reconnection) desteği sayesinde kısa süreli bağlantı kopmaları kullanıcıyı odadan atmaz.

**Oturum öncesinde var olan nesneler senkronize edilir mi?**
Hayır. Collab Room yalnızca oturum başladıktan sonra yapılan değişiklikleri iletir; önceden var olan nesneler senkronizasyon dışında kalır.