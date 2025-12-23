---
title: "Çok Renkli 3D Baskıya Giriş: Tek Yazıcıda Renk Cümbüşü Yaratın"
date: 2025-09-09T12:00:00+03:00
featured: true
draft: false
description: "Tek bir nozzle ile renkli baskı nasıl yapılır? M600 kodu, 'Z-Hop' ile kakma tekniği ve AMS sistemlerinin teknik karşılaştırması. Hangi yöntem sizin için uygun?"
tags: ["Çok Renkli 3D Baskı", "Renk Değişimi", "Otomatik Malzeme Sistemi", "AMS", "Bambu Lab AMS", "Prusa MMU", "Manuel Renk Değişimi", "Renkli Baskı İpuçları", "Teknik İpuçları", "M600"]
categories: ["Beceri Geliştirme ve İleri Teknikler"]
faz: ["Faz 2"]
series: ["3D Baskı Rehberleri"]
author: "Uğur Kapancı"
showToc: true
TocOpen: true
hidemeta: false
comments: true
disableShare: false
disableHLJS: true
hideSummary: false
searchHidden: false
ShowReadingTime: true
ShowPostNavLinks: true
cover:
    image: "/images/multi-color-printing-cover.png"
    alt: "Tek bir 3D yazıcıdan çıkan, canlı ve çok renkli bir 3D baskı objesi"
    caption: "Renk katmak için pahalı donanımlara değil, doğru tekniğe ihtiyacınız var."
    relative: false
---

3D baskı dünyasına girdiğimizde hepimiz tek renkli prototiplerle başlarız. Ancak bir süre sonra o tek düzelik yetmez. Logonuzu basarken zemininin siyah, harflerin beyaz olmasını istersiniz. Veya bastığınız bir uyarı levhasının gerçekten dikkat çekmesi için sarı ve siyah olması gerekir.

Çoğu kullanıcı, renkli baskı alabilmek için 20.000 TL ve üzeri fiyatlara satılan "Bambu Lab AMS" veya "Prusa MMU" gibi çoklu malzeme sistemlerine ihtiyacı olduğunu sanır.

Size net bir mühendis cevabı vereyim: **Hayır, ihtiyacınız yok.**

En ucuz, giriş seviyesi bir Ender 3 ile bile, doğru teknikleri kullanarak 4-5 renkli harika baskılar alabilirsiniz. Bu rehberde, işin teknik mantığını, G-Code komutlarını ve Slicer yazılımlarındaki (OrcaSlicer, Cura) yöntemleri, **karşılaştırmalı tablolarla** inceleyeceğiz.

---

### Neden Çok Renkli Baskı?

Sadece güzellik için değil, fonksiyonellik için de renge ihtiyacımız var:
1.  **Okunabilirlik:** Makine parçaları üzerindeki gömme yazıların okunması zordur. Farklı renkte basılan yazılar ise uzaktan bile okunur.
2.  **Markalama:** Şirket logoları, anahtarlıklar ve promosyon ürünlerinde kurumsal renkleri kullanmak zorundasınız.
3.  **Uyarı İşaretleri:** Sarı-Siyah veya Kırmızı-Beyaz gibi endüstriyel uyarı levhalarını tek seferde basabilirsiniz.

---

### Hangi Yöntemi Seçmelisiniz? (Yol Haritası)

Renkli baskı yapmanın tek bir yolu yoktur. Projenizin geometrisine ve elinizdeki donanıma göre **3 ana teknik** kullanırız. Yöntemlere geçmeden önce hangisine ihtiyacınız olduğunu belirleyin:

1.  **Katman Bazlı Değişim (Z Ekseni):** Eğer modeliniz bir tabela, anahtarlık veya madalya ise (renkler yükseklik değiştikçe değişiyorsa), en kolay ve ucuz yöntem **Manuel Değişim (M600)** yöntemidir.
2.  **Kakma Tekniği (Z-Hop):** Eğer ilk katmanda (tabanda) pürüzsüz, iki renkli bir desen istiyorsanız (kartvizit gibi), **Z-Hop** tekniğini kullanmalısınız.
3.  **Karmaşık Geometri (XY Ekseni):** Eğer bir Spider-Man figürü gibi aynı katmanda birden fazla renk varsa, işte o zaman **Otomatik Sistemler (AMS)** zorunludur.

Şimdi bu teknikleri sırasıyla inceleyelim.

---

### Yöntem 1: Manuel Filament Değişimi (M600 Kodu)

Bu yöntem, "Katman Bazlı" (Z ekseni boyunca) renk değişimleri için endüstri standardıdır. Tabela, anahtarlık, madalya gibi düz zeminli işlerde AMS sisteminden bile daha hızlı ve temiz sonuç verir.

**Teknik Mantık:**
Slicer programına, "X. katmana geldiğinde motorları durdur, kafayı kenara çek ve bekle" emrini veririz.

#### Adım Adım Uygulama (OrcaSlicer / Cura)
1.  **Dilimleme:** Modeli dilimleyin ve sağdaki çubuktan renk değişiminin başlayacağı katmanı bulun (Örn: Katman 25).
2.  **Komut Ekleme:**
    *   **OrcaSlicer:** Katman çubuğunda 25. katmana sağ tıklayın -> **"Change Filament" (M600)** seçin.
    *   **Cura:** *Extensions > Post Processing > Modify G-Code > Add a Script > Pause at Height.*
3.  **Baskı:** Yazıcı durduğunda eski rengi çıkarın, yenisini takın ve **en az 50mm** boşa akıtarak (purge) eski rengin tamamen temizlendiğinden emin olun.

---

### Yöntem 2: Z-Hop ile "Kakma" (Inlay) Tekniği

Elinizde AMS yok ama ilk katmanda (tabanda) iki renkli, dümdüz bir desen (örneğin kartvizit) istiyorsunuz. Manuel değişim bunu yapamaz çünkü o sadece üst üste basar.

**Mantık:**
Önce deseni basarsınız. Sonra deseni tabladan **sökmeden**, etrafındaki zemini basarsınız.
*   **Kritik Ayar:** Slicer'da **"Z-Hop When Retracted"** ayarını, ilk baskının yüksekliğinden (örn: 0.4mm) daha fazla (örn: 0.6mm) yapın. Böylece nozzle hareket ederken yukarı kalkar ve tabladaki desene çarpmaz.

---

### Yöntem 3: Otomatik Sistemler (AMS / MMU)

Eğer katman katman değil de, aynı katman içinde karmaşık renk geçişleri (Örn: Spider-Man figürü) basacaksanız, manuel yöntem imkansızdır. Burada AMS devreye girer.

**Teknik Detaylar ve Ayarlar:**
1.  **Flushing Volumes (Temizleme Miktarı):** Siyah renkten Beyaza geçerken, nozzle içindeki siyah boyanın temizlenmesi gerekir. Slicer'da bu değeri artırın (Multiplier: 1.0 -> 1.5), yoksa beyazlarınız gri çıkar.
2.  **Prime Tower:** Yazıcı, renk değişiminden sonra nozzle basıncını dengelemek için modelin yanına bir kule basar. Bunu kapatmayın.
3.  **Flush into Infill (Dolguya Temizleme):** AMS çok atık üretir. Bu ayarı açarsanız, yazıcı atık plastiği modelin **görünmeyen iç dolgusuna** basar. Hem atık azalır hem model sağlamlaşır.

---

### ☢️ Karşılaştırma Tablosu: Hangi Yöntem Sizin İçin?

Hangi yöntemi kullanacağınıza karar veremiyor musunuz? İşte teknik ve maliyet karşılaştırması:

| Özellik | Manuel Değişim (M600) | Z-Hop Kakma Tekniği | Otomatik Sistem (AMS) |
| :--- | :--- | :--- | :--- |
| **Maliyet** | 0 TL (Sadece Yazılım) | 0 TL (Sadece Yazılım) | 15.000 TL - 30.000 TL |
| **Zorluk** | ⭐ (Çok Kolay) | ⭐⭐⭐ (Riskli) | ⭐⭐ (Ayar gerektirir) |
| **Atık (Fire)** | Yok Denecek Kadar Az | Yok | ⚠️ Çok Yüksek (Kaka Kulesi) |
| **Baskı Süresi** | Hızlı | Orta | Yavaş (Değişim süresi eklenir) |
| **Renk Sınırı** | Sınırsız (Elle değiştirin) | Genelde 2 Renk | 4 - 16 Renk |
| **İdeal Proje** | Tabela, Anahtarlık, Logo | Kartvizit, Kutu Kapağı | Karmaşık Figürler |

---

### ✅ Son Karar: Hangisini Seçmeli?

Tecrübelerime dayanarak size net tavsiyelerim şunlardır:

1.  **Ticari İş Yapıyorsanız (Anahtarlık, Kapı Numarası):** Kesinlikle **Manuel Değişim (M600)** kullanın. AMS bu işler için yavaştır ve çok atık çıkarır. Elle değiştirmek hem daha hızlıdır hem de yüzey kalitesi (Z ekseninde) daha iyidir.
2.  **Figür ve Hobi Basıyorsanız:** Eğer bütçeniz varsa **AMS** alın. Figürlerde manuel boyama yapmak istemiyorsanız tek çare budur. Atığı göze almalısınız.
3.  **İlk Katman Deseni İstiyorsanız:** **Z-Hop** tekniğini öğrenin. Pürüzsüz, tek parça gibi duran iki renkli yüzeyler için en profesyonel yöntem budur.

---

## Sonuç: Sınırları Kaldırın

Renkli baskı, ürününüze "profesyonel" havası katar. İster basit bir M600 koduyla, ister gelişmiş bir AMS sistemiyle olsun; renk kullanmaktan korkmayın.

Baskı bitti, renkler harika. Ama yüzeyde hala o karakteristik "3D yazıcı çizgileri" (katman izleri) var. Bu plastik parçayı, sanki fabrikadan kalıpla çıkmış gibi pürüzsüz ve parlak bir hale getirmek mümkün mü?

### Yolculuğun Bir Sonraki Durağı

Plastiği sanata dönüştüren son aşama: **Yüzey İşleme (Post-Processing).**
Zımpara numaraları (Grit), astar boya teknikleri ve tehlikeli ama etkili kimyasal yumuşatma (Aseton/Kloroform) yöntemleri.

<div class="post-cta-box">
<h3>Sırada: 3D Baskı Yüzey İşleme Teknikleri</h3>
<p>Zımpara, macun, astar ve kimyasal buhar... Baskı izlerini yok edip pürüzsüz ve parlak yüzeyler elde etmenin kimyası.</p>
<a href="{{< ref "posts/3d-baski-yuzey-isleme-teknikleri.md" >}}" class="cta-button">Yüzey İşleme Rehberine Git →</a>
</div>