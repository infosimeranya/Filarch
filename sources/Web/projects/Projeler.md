# Projeler (Projects)

Bu doküman, Filarch uygulamasındaki Projeler sayfasının işlevselliğini açıklar. Projeler, belirli bir hedef doğrultusunda dosyaların, belgelerin ve ilgili çalışmaların bir araya getirildiği temel çalışma birimleridir.

![projects.png](http://docs.filarch.com/media/uploads/projects.png) Şekil 1.1 – Projeler Sayfası Ana Ekranı

## 1. Yeni Proje Oluşturma (Create Project)

Sayfanın sağ üst köşesinde yer alan Create Project butonu, yeni bir proje oluşturma ekranına yönlendirir.
Bu ekranda projeyi oluşturmak için aşağıdaki bilgiler girilir:

- **Proje Adı (Project Name):** Projeniz için açıklayıcı ve ayırt edici bir isim girilir.
- **Çalışma Alanı (Workspace):** Projenin hangi çalışma alanına ait olacağı seçilir. Bu seçim, projenin hangi ekip ve depolama alanı ile ilişkili olduğunu belirler.
- **Etiketler (Tags):** Projeyi kategorize etmek ve daha sonra kolayca bulabilmek için etiketler eklenebilir (ör. Önemli, Tasarım, İnşaat).
- **Mail Şablonu (Mail Template:** Proje ile ilgili bildirimlerde kullanılacak e-posta şablonu seçilir.

## 2. Filtreleme ve Arama

Projeler sayfasında, proje listesini yönetmeyi kolaylaştırmak için filtreleme ve arama araçları bulunur:

- **Search by name:** Proje adına göre hızlı arama yapılmasını sağlar. Yazdıkça liste otomatik olarak filtrelenir.
- **Workspace:** Yalnızca belirli bir çalışma alanına ait projeleri görüntülemek için kullanılır. Birden fazla çalışma alanı bulunan kullanıcılar için kolaylık sağlar.

## 3. Proje Listesi

Sayfanın ana bölümünde tüm projeler tablo halinde listelenir.
Bu tabloda aşağıdaki bilgiler yer alır:

- **Project Name:** Projenin adı ve varsa küçük bir önizleme görseli.
- **Workspace Name:** Projenin bağlı olduğu çalışma alanının adı.
- **Tags:** Projeye atanmış etiketler.
- **Mail Status:** Proje ile ilgili e-posta bildirimlerinin genel durumunu gösterir (ör. All Mails).
- **Mail Template:** Proje için atanmış varsayılan e-posta şablonu.
- **Actions:** Proje ile ilgili hızlı işlemlerin yapılabildiği ikonları içerir.

## 4. Proje Aksiyonları (Actions)

Her projenin "Actions" sütununda üç temel işlem bulunur:

### Projeye Git (Göz İkonu)

Bu ikona tıklandığında, proje içeriğini görüntülemek ve yönetmek için doğrudan **Dosya Yöneticisi** ekranına yönlendirilirsiniz. Bu ekran, projeye ait tüm klasörleri ve dosyaları içerir. Dosya yönetimi ile ilgili detaylı bilgiye Dosya Yöneticisi dokümanından ulaşılabilir.

### Proje Ayarlarını Düzenle (Kalem İkonu)

Bu ikon, projenin temel bilgilerini düzenleyebileceğiniz ekranı açar. Buradan proje adı, etiketler ve mail şablonu güncellenebilir.

### Projeyi Dondur (Kilit İkonu)

Bu ikona tıklandığında, işlemi onaylamanız için bir uyarı penceresi açılır.

Bir proje dondurulduğunda:

- Proje salt okunur (read-only) hâle gelir
- Yeni dosya yüklenemez
- Mevcut dosyalar düzenlenemez veya silinemez
- Kullanıcı yetkileri değiştirilemez

Ancak yetkisi olan kullanıcılar:

- Proje içeriğini görüntülemeye
- Dosyaları indirmeye devam edebilir.

Dondurma işlemi, tamamlanmış veya korunması gereken projeleri güvenli şekilde arşivlemek için kullanılır.
Bu sayede proje, ileride referans alınabilecek sabit ve güvenilir bir dijital kayıt hâline gelir.