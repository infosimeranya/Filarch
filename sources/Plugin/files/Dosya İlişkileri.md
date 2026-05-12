# Dosyalar Arası İlişkiler

Filarch'taki dosyalar arasında **Referans** ve **Bağımlılık** ilişkileri kurarak projenin bağlantı haritasını oluşturun. Bir dosya güncellendiğinde hangi diğer dosyaların etkilendiğini sistem bilir.

---

## İlişki Türleri

| Tür | Açıklama | Örnek |
|-----|----------|-------|
| **Tip 1 — Referans** | Bu dosya, hedef dosyayı referans alır | Mimari plan → Statik hesabı referans alır |
| **Tip 2 — Bağımlılık** | Bu dosya, hedef dosyaya bağımlıdır | Tesisat detayı → Genel plana bağımlıdır |

---

## İlişki Oluşturma

1. Kaynak dosyaya tıklayın → **İlişkiler** sekmesini açın
2. **Yeni İlişki Ekle** butonuna tıklayın
3. İlişki türünü seçin (Referans veya Bağımlılık)
4. Hedef dosyayı arama kutusundan bulun ve seçin
5. İsteğe bağlı: açıklama metni girin — *"Aks bilgileri bu plandan alınmaktadır"* gibi
6. **Kaydet**

> **Ekran Görüntüsü:** Yeni ilişki ekleme formu — tür seçimi ve hedef dosya arama
> ![relationships-1.png](http://docs.filarch.com/media/uploads/relationships-1.png)

---

## İlişkileri Görüntüleme

Bir dosyanın **İlişkiler** sekmesinde hem kaynak hem hedef taraftaki tüm bağlantılar listelenir:

- Bağlantı türü (Referans / Bağımlılık)
- Bağlı dosyanın adı ve konumu
- Açıklama metni
- İlişkinin oluşturulma tarihi

Mevcut ilişkiler üzerinde değişiklik yapılabilir (tür veya açıklama güncelleme) ve gereksiz bağlantılar kaldırılabilir.

> **Ekran Görüntüsü:** Dosya ilişkileri sekmesi — referans ve bağımlılık listesi
> ![relationships-2.png](http://docs.filarch.com/media/uploads/relationships-2.png)


---

## Değişiklik Etki Analizi

İlişkiler, koordinasyon sürecinde **"A dosyası değişirse hangi dosyaların güncellenmesi gerekir?"** sorusunu yanıtlar.

> **Senaryo:** MEP koordinatörü, tesisat çizimini mimari kat planına `Referans` tipiyle bağlar; açıklama alanına *"Aks bilgileri bu plandan alınmaktadır"* yazar. İki hafta sonra mimar kat planını revize eder. Koordinatör dosyanın ilişkiler sekmesini açar, bağımlı tesisat çizimini görür ve ekibine güncelleme talimatı verir.

---

## Sık Sorulan Sorular

**İki farklı formattaki dosya arasında ilişki kurulabilir mi?**
Evet. İlişki sistemi uygulama bağımsız çalışır; `.dwg` ile `.rvt` veya `.pdf` arasında da bağlantı tanımlanabilir.

**İlişkiler versiyon bazlı mı tutulur?**
İlişkiler dosya girişi düzeyinde tutulur; belirli bir versiyona değil, dosya kaydının tamamına bağlıdır.