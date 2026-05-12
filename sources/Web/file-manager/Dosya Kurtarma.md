# Dosya Kurtarma (File Recovery)

Bu doküman, Filarch uygulamasındaki Dosya Kurtarma sayfasının işlevselliğini açıklar. Bu sayfa, silinmiş dosyalarınızı belirli bir süre boyunca saklar ve bu dosyaları orijinal konumlarına geri yüklemenize imkân tanır.

![file_recovery.png](http://docs.filarch.com/media/uploads/file_recovery.png) Şekil 1.1 – Dosya Kurtarma (File Recovery) Ana Ekranı

## Sayfanın Amacı

Yanlışlıkla silinen bir dosyayı geri getirmek veya daha önce silinmiş bir dosyanın eski bir versiyonuna erişmek istediğinizde bu modülü kullanabilirsiniz. Dosyalar, kalıcı olarak silinmeden önce burada bir **güvenlik katmanı** olarak bekletilir.

## 1. Filtreleme ve Arama

Silinmiş yüzlerce dosya arasından aradığınızı kolayca bulabilmek için aşağıdaki arama ve filtreleme araçlarını kullanabilirsiniz:

- **Search by file name:** Kurtarmak istediğiniz dosyanın adını biliyorsanız, bu alana dosya adını yazarak listeyi anında filtreleyebilirsiniz.
- **Workspace:** Yalnızca belirli bir çalışma alanına ait silinmiş dosyaları görüntülemek için bu açılır menüyü kullanabilirsiniz.
- **Project:** Listeyi daha da daraltarak yalnızca belirli bir projeye ait silinmiş dosyaları görmek için bu açılır menüyü kullanabilirsiniz.

## 2. Silinmiş Dosyalar Listesi

Sayfanın ana bölümü, silinmiş tüm dosyaları tablo formatında listeler. Bu tablo, dosyayı kolayca tanımlamanıza yardımcı olacak ayrıntılı bilgiler içerir:

- **File Name:** Silinen dosyanın adını gösterir.
- **Version:** Dosyanın silindiği andaki versiyon numarasını ifade eder.
- **Version Date:** Bu versiyonun oluşturulduğu veya en son güncellendiği tarihi belirtir.
- **Size:** Dosyanın boyutunu gösterir.
- **Deleted Date:** Dosyanın silindiği kesin tarih ve saati ifade eder.
- **Milestone:** Dosyanın silindiği sırada bir kilometre taşı (milestone) olarak işaretlenip işaretlenmediğini belirtir.
- **Upload User:** Dosyayı sisteme ilk yükleyen kullanıcıyı gösterir.
- **Project:** Dosyanın ait olduğu projenin adını ifade eder.
- **Actions:** Dosya üzerinde gerçekleştirilebilecek işlemleri içerir.

## 3. Dosya Kurtarma İşlemi (Actions)

Her dosya satırının sonunda yer alan Actions sütununda dairesel bir ok ikonu (🔄) bulunur.

- **Kurtar (Restore):** Bu ikona tıklandığında dosya, silindiği andaki versiyonuyla birlikte ait olduğu projedeki orijinal konumuna geri yüklenir. Kurtarma işlemi başarıyla tamamlandığında dosya bu listeden kaldırılır ve projede tekrar erişilebilir hâle gelir.