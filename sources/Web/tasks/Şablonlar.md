# Şablonlar (Templates)

Bu doküman, Filarch uygulamasındaki Şablonlar modülünün amacını ve işlevselliğini açıklar.
Şablonlar, yeni projeler oluşturulurken tutarlı ve hazır bir başlangıç yapısı sunmak için kullanılır. Bu sayede her proje için klasör yapısını baştan oluşturma ihtiyacı ortadan kalkar.

![templates.png](http://docs.filarch.com/media/uploads/templates.png) Şekil 1.1 – Şablonlar (Templates) Ekranı

## Şablon Türleri

Filarch’ta iki ana şablon türü bulunur:

1.**Hazır Şablon Grupları (Built-in)**
   Bu şablonlar Filarch tarafından sistemle birlikte sunulur ve standart proje yapıları içerir.
   
   * **Architectural:** Mimari projeler için hazırlanmış standart klasör yapılarını içerir.
   * **Software:** Yazılım geliştirme projeleri için hazırlanmış standart klasör yapılarını içerir.

   ***Hazır şablon özellikleri:***
   * Sistem tarafından sağlanır.
   * Kullanıcılar tarafından düzenlenemez veya silinemez.

2.**Özel Şablonlar Grubu (Custom)**
   * **Custom:** Bu grup, kullanıcıların kendi oluşturduğu tüm şablonları içerir. Mevcut bir projenin klasör yapısı şablon olarak kaydedildiğinde, bu şablon otomatik olarak Custom grubuna eklenir.

## Özel Şablon Oluşturma (Create Template)

Create Template butonu, mevcut bir projenin klasör yapısını yeniden kullanılabilir bir şablona dönüştürmenizi sağlar. Oluşturulan tüm şablonlar Custom grubuna kaydedilir.

Özel şablon oluşturma süreci şu şekildedir:
1.  **Şablon Adı Girin:** Oluşturulacak şablon için açıklayıcı bir isim girilir.
2.  **Kaynak Proje Seçin:** Açılır listeden, klasör yapısı kopyalanacak mevcut proje seçilir.
3.  **Kaydet:** "Kaydet" butonuna tıklandığında, seçilen projenin klasör hiyerarşisi yeni bir Custom şablon olarak oluşturulur.

## Şablonların Kullanımı

Şablonlar, Projeler modülünde yeni bir proje oluşturulurken kullanılır.
Proje oluşturma sayfasında:

- Öncelikle bir şablon grubu seçilir (Architectural, Software veya Custom)
- Ardından seçilen gruba ait bir şablon belirlenerek proje, bu hazır yapı ile oluşturulur
- Bu sayede projeler hızlı ve standart bir yapı ile başlatılır.

## Şablon Listesi ve Aksiyonlar

- **Şablon Listesi:** Sayfanın ana bölümünde tüm şablonlar (hazır ve özel) listelenir. Group Name sütunu, şablonun hangi gruba ait olduğunu gösterir.
- **Arama (Search by Template):** Şablonlar arasında isme göre hızlı arama yapılmasını sağlar.
- **Detaylar (Göz İkonu):** Bir şablonun klasör yapısını ve detaylarını görüntülemenizi sağlar.