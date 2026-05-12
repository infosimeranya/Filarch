# Rol Yönetimi

Bu doküman, Filarch uygulamasındaki Roller sayfasının işlevselliğini açıklar. Bu sayfa üzerinden kullanıcıların belirli çalışma alanları, projeler, klasörler ve dosyalar üzerindeki yetkileri ayrıntılı şekilde yönetilebilir.

![roles.png](http://docs.filarch.com/media/uploads/roles.png) Şekil 1.1 – Rol Yönetimi Ana Ekranı (Roles Sayfası)

## 1. Çalışma Alanı Seçimi (Select Workspace)

Rol yönetimine başlamak için ilk adım, işlem yapmak istediğiniz çalışma alanını seçmektir. Sayfanın üst kısmında yer alan açılır menüden ilgili çalışma alanını seçebilirsiniz.

## 2. Kullanıcılar (Users)

Bir çalışma alanı seçildikten sonra, sol tarafta yer alan Users panelinde bu alana dahil olan tüm kullanıcılar listelenir. Rollerini yönetmek istediğiniz kullanıcıyı bu listeden seçebilirsiniz. Seçilen kullanıcı, mavi bir çerçeve ile vurgulanır.

## 3. Klasör Ağacı (Folder Tree)

Sayfanın orta bölümünde, seçilen çalışma alanına ait proje ve klasör yapısı hiyerarşik bir ağaç görünümü şeklinde sunulur.

- **Genişletme/Daraltma:**“+” ve “−” ikonlarını kullanarak klasörlerin içeriğini genişletebilir veya daraltabilirsiniz.
- **Yetki Atama:** Ağaç yapısından bir proje, klasör veya dosya seçerek, Users panelinde seçili olan kullanıcının bu öğe üzerindeki yetkisini belirleyebilirsiniz.
- **Mevcut Roller:** Her öğenin yanında, seçili kullanıcının o öğe üzerindeki mevcut rolünü gösteren bir etiket bulunur (ör. OWNER, EDITOR).

## 4. Rol Bilgileri (Role Information)

Bu panel, sayfanın sağ tarafında yer alır ve yaptığınız seçimlere göre dinamik olarak güncellenir.

- **User:** Kullanıcılar listesinden seçilen kullanıcının e-posta adresini gösterir.
- **Selected Item:** Klasör ağacından seçilen öğenin (proje, klasör veya dosya) adını gösterir.
- **Current Role:** Seçili kullanıcının, seçili öğe üzerindeki mevcut rolünü belirtir.
- **Update Role:** Bu açılır menü üzerinden kullanıcıya yeni bir rol atanabilir. Örneğin, bir kullanıcı bir projede **Görüntüleyici** (Viewer) veya bir klasörde **Editör** (Editor) olarak yetkilendirilebilir.
- **Update Role Butonu:** Yeni rol seçildikten sonra, değişikliği uygulamak için bu butona tıklanması gerekir.
- **Role Summary:** Panelin alt kısmında, yapılan atamayı özetleyen bir bilgi yer alır (ör. a.aktas@simeranya.com.tr - OWNER - Güler Toki Evleri 2). Bu özet, işlemi onaylamadan önce seçimlerin doğruluğunu kontrol etmenize yardımcı olur.