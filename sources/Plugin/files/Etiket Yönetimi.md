# Etiket Yönetimi

Etiketler, klasör yapısından bağımsız olarak dosyaları yatay gruplamanızı sağlar. Farklı klasörlerdeki dosyaları aynı etiketle bir araya getirin; büyük arşivlerde hedef dosya grubuna anında ulaşın.

---

## Etiket Oluşturma

Etiketler proje düzeyinde tanımlanır; her etiket yalnızca ait olduğu projenin dosyalarına atanabilir.

### Yeni etiket eklemek

1. Sol gezinme çubuğunun alt kısmındaki **etiket simgesi** butonuna tıklayarak Etiket Yönetimi panelini açın
2. **Yeni Etiket Oluştur** butonuna tıklayın
3. Etiket adını girin (örn. `İhale Onaylı`, `Revizyon Bekliyor`)
4. İsteğe bağlı olarak açıklama girebilirsiniz
5. **Etiket Oluştur**

Oluşturulan etiketler listede görüntülenir; üzerine tıklayarak düzenleyebilir, kullanımda olmayan etiketleri silebilirsiniz.

> **Ekran Görüntüsü:** Etiket yönetimi listesi — ad sütunları
> ![tag-1.png](http://docs.filarch.com/media/uploads/tag-1.png)

---

## Dosyaya Etiket Atama

Bir dosyaya birden fazla etiket atanabilir.

1. Dosyaya sağ tıklayın → Etiketleri Aç/Kapat
2. İstediğiniz etiketleri açın veya kapatın.
3. **Kaydet**

> **Ekran Görüntüsü:** Dosya üzerinde sağ tık bağlam menüsü — Enable/Disable Tags seçeneği
> ![tag-2.png](http://docs.filarch.com/media/uploads/tag-2.png)

> **Ekran Görüntüsü:** Enable/Disable Tags modali — etiket toggle listesi
> ![tag-3.png](http://docs.filarch.com/media/uploads/tag-3_1CDPKxE.png)

---

## Etiketle Filtreleme

Etiket filtresi, seçilen etikete sahip dosyaları anlık olarak listeler.

- Dosya ağacının filtre alanından **Etiket** seçeneğini seçin
- Arama kutucuğuna etiketin adını yazın
- **Gelişmiş Arama** panelinde etiket bir filtre kriteri olarak da kullanılabilir

> **Ekran Görüntüsü:** Dosya listesi — etiket filtresi aktif
> ![tag-4.png](http://docs.filarch.com/media/uploads/tag-4.png)

> **Örnek:** `İhale Onaylı` + `Mekanik` etiketlerini birlikte seçtiğinizde yalnızca her iki etiketi de taşıyan dosyalar listelenir.

---

## Örnek Kullanım

> Büyük bir mimarlık projesinde doküman kontrolörü `İhale Onaylı`, `Revizyon Bekliyor` ve `Arşiv` etiketlerini oluşturur. Her dosyayı inceledikçe uygun etiketi atar. İhale paketi hazırlanırken `İhale Onaylı` filtresiyle yalnızca onaylı dosyaları görür; `Revizyon Bekliyor` filtresiyle revize edilmesi gerekenleri anında listeler.