# Dosya Yöneticisi

Kullanıcı, **Dosya Yöneticisi** sayfasında yetkili olduğu projeye ait klasörlere, dosyalara ve versiyonlara erişebilir. Kullanıcı, sahip olduğu yetkiye bağlı olarak dosya ve klasörler üzerinde oluşturma, güncelleme ve silme işlemlerini gerçekleştirebilir. **Dosya Yöneticisi** sayfasına erişmek için kullanıcı, çalışma alanı ve proje seçim ekranında ilgili projeyi seçmelidir.

## 1. Çalışma Alanı ve Proje Seçimi

![file_manager_selection](https://i.hizliresim.com/btsbbn3.png) Şekil 1.1 – Dosya Yöneticisi Çalışma Alanı ve Proje Seçim Ekranı

Kullanıcı, sol menüde yer alan **Dosya Yöneticisi** bağlantısına tıkladığında **Çalışma Alanı** ve **Proje Seçim** ekranına yönlendirilir.
Bu sayfanın üst kısmında bulunan **Proje Oluştur** butonuna tıklandığında kullanıcı **Proje Oluştur** sayfasına yönlendirilir. Ekranın sol tarafında kullanıcının yetkili olduğu çalışma alanları listelenir. Sağ tarafta ise seçilen çalışma alanı içerisinde yetkili olunan projeler ve proje bilgileri tablo halinde görüntülenir.

Kullanıcı bu ekranda:
-Çalışma alanı ve projeler arasında arama yapabilir,
-Liste ve kart görünümleri arasında geçiş yapabilir,
-Bir çalışma alanı seçerek o alana ait projeleri görüntüleyebilir,
-Bir projeye tıklayarak ilgili projenin Dosya Yöneticisi sayfasını açabilir.
Çok sayıda çalışma alanı veya proje bulunması durumunda kullanıcı sayfalar arasında geçiş yapabilir.

Tabloda yer alan bilgiler:

- **Proje:** Projeye ait logo ve dosya yöneticisi bağlantısını ifade eder. Bu bağlantıya tıklandığında ilgili projenin dosya yöneticisi açılır.
- **Çalışma Alanı Adı:** Projenin ait olduğu çalışma alanının adını ifade eder.
- **Etiketler:** Projeye atanmış etiketleri ifade eder.
- **Mail Durumu:** Proje kullanıcılarına hangi durumlarda e-posta gönderileceğini ifade eder.
- **Mail Şablonu:** Proje kullanıcılarına gönderilen e-postalarda kullanılan şablonu ifade eder.
- **Yetkili Kullanıcı Sayısı:** Projede yetkili olan kullanıcı sayısını ifade eder.
- **İşlemler:** Detay butonu üzerinden ilgili projenin dosya yöneticisine erişilebilir.

## 2. Dosya Yöneticisi

![file_manager](https://i.hizliresim.com/hwe2kxh.png) Şekil 2.1 – Dosya Yöneticisi Ana Ekranı (Dosyalar Sekmesi)

Kullanıcı, çalışma alanı ve proje seçim ekranından bir proje seçtiğinde ilgili projenin **Dosya Yöneticisi** sayfası açılır. Sayfanın üst kısmından seçilen projenin Güncelleme sayfasına erişilebilir.

Dosya Yöneticisi sayfası üç sekmeden oluşur:

- Dosyalar
- Yetkili Kullanıcılar
- Proje Bilgileri

### a. Dosyalar

![file_manager](https://i.hizliresim.com/hwe2kxh.png)Şekil 2.2 – Dosya Yöneticisi Ana Ekranı (Dosyalar Sekmesi)
(Şekil 2.1 ile aynı görsel – dokümanda ikinci kullanım)

Bu sekmede projeye ait klasörler, dosyalar ve versiyonlar yönetilir.

Üst kısımda yer alan butonlar:

- **Projeler:** Çalışma alanı ve proje seçim ekranına geri yönlendirir.
- **Oluştur:** Klasör oluşturma butonudur. Maintainer rolü ve üzerindeki kullanıcılar tarafından görüntülenebilir.
- **Dosya Ekle:** Dosya yükleme butonudur. Maintainer rolü ve üzerindeki kullanıcılar tarafından görüntülenebilir.
- **Dosya Adlarında Arama:** Açık olan klasör içerisindeki klasör ve dosyalarda arama yapar. Arama sonuçlarına göre tablo güncellenir.
- **Detaylı Ara:** Projedeki klasör ve dosyalar için detaylı arama, filtreleme ve sıralama yapılabilen Detaylı Arama sayfasına yönlendirir.
- **Liste Görünümü:** Klasör ve dosyaları tablo görünümünde listeler.
- **Kart Görünümü:** Klasör ve dosyaları kart görünümünde listeler.

Üst kısımdaki butonların hemen altında, kullanıcının hangi klasör içerisinde olduğunu gösteren bir dizin yolu yer alır.
Ekranın sol tarafında, projedeki klasörlerin listelendiği bir klasör ağacı bulunur. Kullanıcı, klasör ağacı üzerinden projedeki klasörleri görüntüleyebilir ve istediği klasöre tıklayarak o klasör içindeki klasör ve dosyalara tabloda erişebilir.

![file_manager_context_menu](https://i.hizliresim.com/l6at5gm.png) Şekil 2.3 – Klasör Ağacı Sağ Tık (İçerik) Menüsü

Klasör ağacı yapısında bir klasöre sağ tıklandığında bir içerik menüsü açılır.
Bu menüde yer alan butonlar aracılığıyla klasöre ait işlemler gerçekleştirilebilir.

İçerik menüsünde yer alan seçenekler:

- **Detay:** Klasöre ait detay menüsünde Genel Bakış sekmesini açar.
- **Yeniden Adlandır:** Klasör adını değiştirmek için bir düzenleme alanı açar.
- **Ayarlar:** Klasöre ait detay menüsünde Ayarlar sekmesini açar.
- **Oluştur:** Klasör içerisinde yeni bir klasör oluşturmak için bir menü açar. Maintainer rolü ve üzerindeki kullanıcılar tarafından görüntülenebilir.
- **Yükle:** Klasör içerisine yeni bir dosya yüklemek için bir menü açar. Maintainer rolü ve üzerindeki kullanıcılar tarafından görüntülenebilir.
- **Dondur:** Klasörü, üzerinde herhangi bir işlem yapılamayacak şekilde dondurur. Maintainer rolü ve üzerindeki kullanıcılar tarafından görüntülenebilir.
- **Sil:** Klasörü siler. Admin rolü ve üzerindeki kullanıcılar tarafından görüntülenebilir.

Klasör ağacı yapısının alt bölümünde, projenin kapladığı depolama alanı ile kullanıcı lisansına ait toplam depolama alanı bilgileri görüntülenir.

Ekranın sağ kısmında, açık olan klasörün içerisindeki klasörler ve dosyalar bilgileriyle birlikte tabloda listelenir.
Dosya yöneticisi ilk açıldığında varsayılan olarak proje adına ait kök klasör açık durumda görüntülenir. Kullanıcı, kök klasör içerisinde kendi klasör yapısını oluşturabilir ve dosyalarını yükleyerek dosya yöneticisini ihtiyaçlarına göre şekillendirebilir.

Tabloda yer alan bilgiler şunlardır:

- **Klasör / Dosya Adı:** Klasör veya dosyanın adını ifade eder. Dosya son versiyon ise veya milestone dosya niteliği taşıyorsa, bu bilgi adının yanında belirtilir.
- **Boyut:** Dosyalar için dosya boyutunu, klasörler için ise içerdiği klasör ve dosyaların toplam boyutunu ifade eder. İçeriği olmayan klasörlerde boyut bilgisi gösterilmez.
- **Etiketler:** Klasör veya dosyaya atanmış etiketleri ifade eder.
- **Yetki:** Kullanıcının klasör üzerindeki yetkisini gösterir. Dosyaların yetkisi, ait oldukları klasörün yetkisi ile aynıdır.
- **Oluşturulma Tarihi:** Klasör veya dosyanın oluşturulduğu tarihi ifade eder.
- **İşlemler:** Klasör ve dosyaya ait işlemleri içerir. Detay işlemi klasör için klasörü açarak içerisindeki klasör ve dosyaları gösterir, dosya için ise dosya detay menüsünü açar. Güncelleme işlemi klasör detay menüsünü açar. İndirme işlemi dosyayı indirir. Silme işlemi ise klasör veya dosyayı siler ve admin rolü ve üzerindeki kullanıcılar tarafından gerçekleştirilebilir.

Klasör ağacı yapısında veya tablo üzerinde sürükle-bırak yöntemiyle klasör ve dosya taşıma işlemleri gerçekleştirilebilir. Bu işlemi **Maintainer** rolü ve üzerindeki kullanıcılar yapabilir.

Bu işlem sırasında dikkat edilmesi gerekenler şunlardır:

- Taşıma işlemi, klasörün tüm alt klasörlerini ve dosyalarını da kapsar. Taşınan klasöre ve alt öğelerine ait roller hedef klasöre aktarılır. Hedef klasöre ait kullanıcılar, rollerine göre taşınan klasör üzerinde yetki kazanır.
- Bir klasör, bir dosyanın içine taşınamaz.
- Bir üst klasör, kendi altındaki bir klasörün içine taşınamaz.
- Bir alt klasör, bulunduğu üst klasörün içerisine taşınamaz.

### b. Yetkili Kullanıcılar

![project_users](https://i.hizliresim.com/t3yybmt.png) Şekil 2.4 – Proje Yetkili Kullanıcılar Listesi

Bu sekmede projeye ait yetkili kullanıcılar tabloda listelenir. Kullanıcı bu tabloda yetkili kullanıcıları arayabilir, kullanıcı bilgilerine ulaşabilir, güncelleme yapabilir, projeye tekrar davet gönderebilir veya kullanıcıyı silebilir. Güncelleme işlemi **Updater** rolü ve üzerindeki kullanıcılar tarafından yapılabilir. Davet gönderme işlemi **Maintainer** rolü ve üzerindeki kullanıcılar tarafından yapılabilir. Silme işlemi ise **Admin** rolü ve üzerindeki kullanıcılar tarafından gerçekleştirilebilir.

![add_project_users](https://i.hizliresim.com/m7jxtu6.png) Şekil 2.5 – Projeye Yetkili Kullanıcı Ekleme Ekranı

**Yetkili Kullanıcı Ekle** butonuna tıklandığında yetkili kullanıcı ekleme menüsü açılır. Bu menü üzerinden projede görev alacak yetkili kullanıcılar eklenir. Eklenecek kullanıcı, e-posta adresi aranarak çalışma alanındaki kullanıcılar arasından seçilebilir veya harici bir e-posta adresi girilerek eklenebilir. Ardından rol seçimi yapılır.

Filarch uygulamasında proje kullanıcıları için aşağıdaki roller bulunmaktadır:

- **Milestone Viewer:**  Projede bulunan milestone dosyalarını görüntüleyebilir. Dosya oluşturma, güncelleme veya silme yetkisi yoktur.
- **Viewer:** Projede bulunan dosyaları görüntüleyebilir. Dosya oluşturma, güncelleme veya silme yetkisi yoktur.
- **Updater:** Projede bulunan dosyaları görüntüleyebilir ve güncelleyebilir. Dosya oluşturma veya silme yetkisi yoktur.
- **Maintainer:** Projede bulunan dosyaları görüntüleyebilir, oluşturabilir ve güncelleyebilir. Dosya silme yetkisi yoktur.
- **Admin:** Projede bulunan dosyaları görüntüleyebilir, oluşturabilir, güncelleyebilir ve silebilir. Owner rolünü düzenlemek dışında tüm yetkilere sahiptir.
- **Owner:** Projenin kurucusudur. Projede bulunan tüm dosyalar üzerinde tam yetkiye sahiptir.

Menü kaydedildiğinde yetkili kullanıcı ekleme işlemi tamamlanır ve tablo güncellenir.

### c. Proje Bilgileri

![project_information](https://i.hizliresim.com/gremzvk.png) Şekil 2.6 – Proje Bilgileri Ekranı

Bu sekmede projeye ait bilgiler listelenir. Kullanıcı bu alanda projeye etiket atayabilir, projeyi dondurabilir veya toplantı konusu ekleyebilir. Proje dondurulduğunda, projeye ait tüm işlemler pasif hâle getirilir. Toplantı konusu eklendiğinde ise toplantı oluşturma sırasında bu konu seçilebilir. Bu işlemler Maintainer rolü ve üzerindeki kullanıcılar tarafından gerçekleştirilebilir.