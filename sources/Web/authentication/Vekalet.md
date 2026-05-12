COA Proxy (Vekalet Merkezi) sayfası, kullanıcıların Chain of Approval (Onay Zinciri) yetkilerini belirli bir tarih aralığı için başka bir kullanıcıya devretmesini sağlar. Tatil, izin veya yoğunluk gibi durumlarda onay bekleyen görevlerin takılı kalmaması için tasarlanmış, iki taraflı onaylı (2-way handshake) bir yetki devir sistemidir.
## Vekalet oluşturma 
![vekalet_olusturma.png](http://docs.filarch.com/media/uploads/vekalet_olusturma.png)

Proje seçip başlangıç/bitiş tarihi girerek başka bir kullanıcıya onay yetkisi devredilir.

## Verdiğim vekaletler 

![verilen_vekalet.png](http://docs.filarch.com/media/uploads/verilen_vekalet.png)
Gönderilen vekalet talepleri listelenir.
Aktif olanlar erken sonlandırılabilir.

## Aldığım vekaletler 
![alinan_vekalet.png](http://docs.filarch.com/media/uploads/alinan_vekalet.png)
Gelen vekalet talepleri görüntülenir.
Bekleyenler kabul veya reddedilebilir.

## Kullanıcıya Sağlanan Faydalar

- **Onay akışları durmuyor:** Tatil, hastalık veya yoğunluk durumlarında görevler beklemede kalmaz; vekil kullanıcı onay yetkisini devralır.
- **Zaman kontrollü vekalet:** Başlangıç ve bitiş tarihi tanımlanarak yetki tam olarak ihtiyaç duyulan süreyle sınırlandırılır.
- **Güvenli iki taraflı onay (2-way handshake):** Vekalet, receiver onaylamadan aktif olmaz; yetkisiz devir söz konusu değildir.
- **Tam şeffaflık:** Verilen, alınan ve bekleyen tüm vekalet istekleri tek ekranda görülebilir.
- **Bildirim sistemi:** Talep, kabul, red ve süre dolumu olaylarında ilgili taraflar otomatik olarak bilgilendirilir.
- **Geçmiş korunur:** Reddedilen veya sonlandırılan vekaletler silinmez; denetim izleri (audit trail) için tutulur.

---

## Diğer Uygulamalarda Bulunmayan Özellikler

### Zincirleme (Transitive) Vekalet
Filarch'ın en ayırt edici özelliğidir. Klasik vekalet sistemleri yalnızca doğrudan A→B devrini destekler. Filarch'ta:

```
Recep → Mücahit → Ahmet
```

Ahmet, hem Mücahit'in hem de (dolaylı olarak) Recep'in onay yetkilerine sahip olur. Zincirleme 10 seviyeye kadar desteklenir ve döngüsel referanslar sistematik olarak engellenir.

**Efektif Tarih Aralığı Kesişimi:** Zincirleme vekaletlerde her bir bağlantının tarih aralıkları kesiştirilir. Örneğin A→B (2–7 Ocak) ve C→A (3–10 Ocak) zincirinde, C için efektif yetki aralığı **3–7 Ocak** olarak hesaplanır.

### COA Hiyerarşisi ile Derin Entegrasyon
Vekalet sistemi, Filarch'ın onay hiyerarşileri (CoaHierarchy), özel roller (ProjectSpecialRoles) ve proje bazlı status group'larıyla tam entegredir. Vekalet veren kullanıcı COA yetkisi olmadan vekalet oluşturamaz; bu, sistemin yetkisiz delegasyonlara karşı korumalı olmasını sağlar.

### Proje Bazlı Kapsam
Her vekalet bir projeye özeldir. Aynı kişi farklı projelerde farklı vekaletler verebilir; bir projedeki yetki devri diğer projeleri etkilemez.

### Otomatik Süre Dolumu Kontrolü
Celery arka plan görevi periyodik olarak süresi dolan vekalet detaylarını tespit eder ve ilgili taraflara bildirim gönderir. Kullanıcının manuel takip etmesine gerek yoktur.

---

## Kullanım Senaryosu

**Senaryo: Finans Müdürü İzne Çıkıyor**

Filarch'ta bir inşaat firmasının finans projesinde, tüm ödeme belgelerinin Finans Müdürü Ahmet tarafından onaylanması gerekmektedir (COA adımı). Ahmet 1–15 Mayıs arasında yıllık izne çıkacaktır.

**Adım 1 — Vekalet Talebi:**  
Ahmet, Mali İşler Uzmanı Zeynep'i 1–15 Mayıs tarih aralığı için vekil olarak atar.

**Adım 2 — Vekalet Kabulü:**  
Zeynep, sistemden gelen bildirimle talebi görür ve kabul eder. Ahmet'e "vekaletiniz kabul edildi" bildirimi gönderilir.

**Adım 3 — Aktif Vekalet:**  
1 Mayıs itibarıyla Zeynep, Ahmet'in onay yetkisini kullanarak bekleyen tüm ödeme belgelerini onaylayabilir. 

**Adım 4 — Zincirleme Senaryo:**  
Zeynep'in de meşguliyeti olduğunda, Zeynep başka bir meslektaşa vekalet verebilir (Zeynep → Mehmet). Mehmet, hem Zeynep'in hem de dolaylı olarak Ahmet'in onay yetkilerine sahip olur; efektif tarih aralığı otomatik olarak hesaplanır.

**Adım 5 — Erken Dönüş:**  
Ahmet izinden erken döndüğünde vekaleti anında sonlandırır; Zeynep'e bildirim gönderilir ve yetki Ahmet'e geri döner.