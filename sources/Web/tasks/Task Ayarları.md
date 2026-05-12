# Görev Ayarları (Task Settings)

Bu doküman, Filarch uygulamasındaki **Task Settings** sayfasının işlevselliğini açıklar.
Bu sayfa; görev yönetiminde kullanılan roller, statü yapıları, onay akışları, öncelikler, reddetme sebepleri ve sistem tanımlarını merkezi olarak yönetmenizi sağlar.

## Sayfa Bileşenleri

### 1. Proje Özel Rolleri (Project Roles)
![task-settings-rolles.png](http://docs.filarch.com/media/uploads/task-settings-rolles.png)

Bu bölümde, namespace (çalışma alanı) bazlı proje özel rollerini oluşturabilir, arayabilir, düzenleyebilir ve silebilirsiniz.

- **Merkezi Rol Kataloğu:** Aynı rol, namespace içindeki birden fazla projede yeniden kullanılabilir.
- **Rol Oluşturma/Düzenleme:** Name (max 255 karakter) ve Namespace alanları ile yapılır.
- **Güvenli Silme:** Rol silmeden önce COA hiyerarşileri, efor tahminleri ve rol atamaları gibi bağlı kullanımlar kontrol edilir.

### 2. Statü Grupları (Status Groups)
![task-settings-status-groups.png](http://docs.filarch.com/media/uploads/task-settings-status-groups.png)

Görev akışlarını tanımlayan statü gruplarını yönetmenizi sağlar.

- **Grup Oluşturma:** Grup adı ve namespace ile yapılır.
- **Statü Öğeleri Yönetimi:** Her grup altında statü adı, süreç tipi, renk ve sıralama bilgileri tanımlanır.
- **Akış Davranışı:** Kapanış tipi statüler görev ilerlemesini otomatik olarak %100'e çekebilir.
- 
### 3. Onay Akışları (Approval Flows / COA)
![task-settings-coa-hierarchie.png](http://docs.filarch.com/media/uploads/task-settings-coa-hierarchie.png)

Çok adımlı onay zincirlerini namespace seviyesinde tanımlamak için kullanılır.

- Her adım için **rol**, **onay stratejisi**, **sıra** ve **gün limiti** belirlenebilir.
- İsteğe bağlı olarak, atanmamış rol durumunda adımın otomatik onaylı sayılması ayarlanabilir.
- Hiyerarşi detayları zaman çizgisi (timeline) görünümünde izlenebilir.

### 4. Öncelikler (Priorities)
![task-settings-priority.png](http://docs.filarch.com/media/uploads/task-settings-priority.png)

Proje bazlı öncelik listesini (ör. Düşük, Orta, Yüksek, Kritik) renk kodlarıyla yönetir.

- Namespace ve proje seçimine göre çalışır.
- Her öncelik için ad ve hex renk kodu tanımlanır.
- Oluşturma/düzenleme işlemleri doğrulama kurallarıyla güvence altına alınır.

### 5. Reddetme Sebepleri (Rejection Reasons)
![task-settings-deny-reasons.png](http://docs.filarch.com/media/uploads/task-settings-deny-reasons.png)

COA onay süreçlerinde kullanılacak standart reddetme sebeplerini, statü grubu bazında yönetir.

- Sebepler, seçili statü grubuna bağlı olarak listelenir.
- Düzenleme sırasında statü grubu alanı kilitli tutulur.
- Böylece onay geçmişindeki bağlam ve veri tutarlılığı korunur.

### 6. Sistem Tanımları (System Definitions)
![task-settings-system-defination.png](http://docs.filarch.com/media/uploads/task-settings-system-defination.png)

Görev modülünün çekirdek sistem tiplerini salt-okunur şekilde referans olarak sunar.

- **Status Process Types**
- **Approval Strategy Types**
- **Dependency Types (FS / SS / FF)**

Her kartta bilgi (info) modalları bulunur; kullanıcılar kavramların anlamını ekrandan hızlıca öğrenebilir.