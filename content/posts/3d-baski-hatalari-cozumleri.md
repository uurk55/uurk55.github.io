---
title: "En Yaygın 10 3D Baskı Hatası ve Pratik Çözümleri (2025)"
date: 2025-08-08T10:00:00+03:00
featured: true
draft: false
description: "Spagettiye dönmüş bir model, kalkmış köşeler, ipliklenmiş detaylar... 3D baskı hatalarını sadece 'sorun' olarak görmeyin. Warping'den Z-Banding'e, Input Shaping'den Flow Rate'e kadar teknik derinlemesine analiz."
tags: ["3D Baskı Hataları", "Sorun Giderme", "Spagetti Hatası", "Warping", "Katman Kayması", "Heat Creep", "Stringing", "Baskı Kalitesi", "Z-Wobble", "Input Shaping"]
categories: ["Teknik İpuçları"]
faz: ["Faz 1"]
series: ["3D Baskı Temelleri Serisi"]
author: "Uğur Kapancı"
showToc: true
TocOpen: true
hidemeta: false
comments: true
disableShare: false
disableHLJS: false
hideSummary: false
searchHidden: false
ShowReadingTime: true
ShowPostNavLinks: true
cover:
    image: "/images/hata-rehberi-cover.jpg"
    alt: "Masada spagettiye dönmüş bir 3D baskı ve onu inceleyen teknik ekipmanlar"
    caption: "Her hata, makinenizin sizinle konuştuğu bir dildir. Onu tercüme edelim."
    relative: false
---

3D baskı yolculuğunda her şeyin mükemmel gitmesini beklemek, ilk sürüş dersinde Formula 1 aracına binmek gibidir; duvara toslamanız kaçınılmazdır.

Benim atölyemde, 10 yıllık tecrübeye rağmen hala baskılar bozuluyor. Ama artık o bozuk baskıya baktığımda "Bu neden oldu?" diye üzülmüyorum. "Ha, akış oranı %2 fazla gelmiş" veya "Soğutma fanı yetersiz kalmış" diyebiliyorum.

Bu rehber, basit bir "fişi çek tak" listesi değil. Sorunların **mekanik ve yazılımsal köklerine** indiğimiz, Slicer'ın derinliklerindeki ayarlarla çözüm ürettiğimiz ileri seviye bir teşhis kılavuzudur.

{{< tip-box title="💡 Altın Kural: Değişken Kontrolü" >}}
Bir sorunu çözerken **ASLA** aynı anda iki parametreyi değiştirmeyin. Hem sıcaklığı artırıp hem hızı düşürürseniz, hangisinin sorunu çözdüğünü (veya daha da bozduğunu) bilemezsiniz. Bilimsel yaklaşın: Tek ayar, bir test.
{{< /tip-box >}}

---

### 1. Spagetti Canavarı (Adhesion Failure)

![Baskı tablasının üzerinde karışık filament yığını](/images/hata-spagetti.jpg "Sabah uyandığınızda karşınızda bu varsa, günaydın!")

**Hikaye:** 12 saatlik bir baskıyı başlattınız, sabah heyecanla uyandınız. Odanın kapısını açtınız ve o acı manzara: Model yok, tabla üzerinde İtalyan mutfağından çıkmışçasına dolanmış bir plastik yumağı var.

**Teknik Analiz:**
Baskı, tabladan kopmuş. Ancak yazıcının bundan haberi olmadığı için (eğer AI destekli bir kameranız yoksa) havaya katman atmaya devam etmiş.
*   **Kök Neden 1 (Z-Offset):** Nozzle, ilk katmanda plastiği tablaya yeterince "ezmemiştir" (Squish).
*   **Kök Neden 2 (Yüzey):** PEI tablanızda parmak izi yağı kalmıştır.

**Profesyonel Çözüm:**
1.  **Temizlik:** Tablayı bulaşık deterjanı ve ılık suyla yıkayın (Evet, IPA yetmez, yağ için deterjan şarttır).
2.  **Slicer Ayarı:** İlk katman çizgi genişliğini (Initial Layer Line Width) **%120** yapın. Bu, ilk katmanı daha kalın basarak tutunmayı artırır.
3.  **Brim:** Modelin taban yüzeyi küçükse, Slicer'dan mutlaka **Brim (Geniş Kenarlık)** açın.

### 2. Warping (Köşelerin Kalkması ve Gerilme)

![Büyük bir kutunun köşelerinin tabladan yukarı kalkması](/images/hata-warping.jpg "Plastiğin büzülme kuvveti, yapışma kuvvetini yendiğinde.")

**Hikaye:** Büyük bir kutu basıyorsunuz. İlk saatler harika. Ama 3. saatte bir bakıyorsunuz, kutunun taban köşeleri tabladan ayrılmış, muz gibi yukarı kıvrılmış.

**Teknik Analiz:**
Bu bir fizik sorunudur: **Termal Büzülme.** Plastik soğudukça hacmi küçülür. Üst katmanlar soğuyup büzülürken, alttaki (tablaya yapışık) katmanları yukarı doğru çeker. Bu çekme kuvveti, yapışma kuvvetinden büyükse Warping olur.

**Profesyonel Çözüm:**
1.  **Draft Shield (Rüzgar Kalkanı):** Slicer'da bu özelliği açın. Yazıcı, modelin etrafına geçici bir duvar örer ve içerideki sıcak havayı hapseder.
2.  **Mouse Ears (Fare Kulağı):** Slicer'da (özellikle OrcaSlicer'da) modelin keskin köşelerine sağ tıklayıp "Add Primitive > Disc" diyerek sadece köşelere ince diskler ekleyin. Bu, Brim'den daha etkili ve temizlemesi daha kolaydır.
3.  **Sıcaklık:** Tablayı ilk katmanda sıcak (65°C), sonraki katmanlarda biraz daha düşük (60°C) tutun.

### 3. Katman Kayması (Layer Shift & Vref)

**Hikaye:** Baskınızın yarısı kusursuz, ama bir noktadan sonra sanki bina depremde kaymış gibi 5mm sağdan devam ediyor.

**Teknik Analiz:**
Step motoru "adım kaçırmış". Yazıcı "100 adım git" demiş, motor zorlanmış ve sadece 80 adım gidebilmiş.
*   **Sebep 1:** Nozzle baskı sırasında modele çarpmıştır (Curling).
*   **Sebep 2:** Motor sürücü voltajı (Vref) düşüktür veya motor aşırı ısınıp korumaya geçmiştir.

**Profesyonel Çözüm:**
1.  **Z-Hop:** Slicer'da **"Z-Hop When Retracted"** ayarını açın. Nozzle hareket ederken 0.2mm yukarı kalkar, böylece modele çarpmaz.
2.  **İvme (Acceleration):** Eğer çok yüksek hızlarda (300mm/s+) basıyorsanız, motor torku yetmiyor olabilir. İvmeyi düşürün.
3.  **Kayışlar:** Kayışları gitar teli gerginliğinde ayarlayın.

### 4. Stringing (Retraction Mekaniği)

![İki kule arasında ince iplikler](/images/hata-stringing.jpg "Basınç kontrol edilemediğinde sızıntı kaçınılmazdır.")

**Hikaye:** Modeliniz bitti ama üzerinde örümcek ağları var. Her yer incecik plastik tüylerle kaplı. Çakmakla yakarak temizlemekten bıktınız.

**Teknik Analiz:**
Nozzle içinde erimiş plastik basınçlıdır. Hareket (travel) sırasında bu basınç alınmazsa, yerçekimi ve iç basınçla plastik "sızar" (oozing).

**Profesyonel Çözüm:**
1.  **Islak Filament:** %90 ihtimalle filamentiniz nemli. Nemli filament ısınıca içindeki su buharlaşır ve "patlayarak" plastiği dışarı iter. Filamenti kurutun.
2.  **Retraction Tower:** Slicer ayarlarını ezbere girmeyin. Bir "Retraction Tower" testi basarak en doğru mesafeyi (Direct Drive için 0.4-1.0mm) bulun.
3.  **Wipe While Retracting:** Slicer'da bu ayarı açın. Nozzle geri çekme yaparken hafifçe içeri doğru bir hareket yapar ve sızıntıyı modelin içine siler.

### 5. Heat Creep (Isı Yığılması ve Tıkanıklık)

**Hikaye:** Baskı harika başlıyor. 2 saat sonra nozzle tıkanıyor. Temizleyip tekrar başlatıyorsunuz, yine tam 2. saatte tıkanıyor. Delirmek üzeresiniz.

**Teknik Analiz:**
Buna **Heat Creep** denir. Hotend'i soğutan fan yetersiz kalıyordur veya ortam çok sıcaktır (kapalı kasa PLA basmak gibi). Isı, nozzle'dan yukarıdaki soğuk bölgeye (heatsink) tırmanır. Filament, erimemesi gereken yerde yumuşar ve şişer.

**Profesyonel Çözüm:**
1.  **Ortam:** PLA basıyorsanız yazıcının kapağını/kapısını AÇIK tutun.
2.  **Fan:** Hotend soğutma fanının tozlanmadığından emin olun.
3.  **Retraction:** Geri çekme mesafesini düşürün. Çok fazla geri çekmek, sıcak plastiği soğuk bölgeye taşır ve donmasına neden olur.

### 6. Fil Ayağı (Elephant's Foot)

**Hikaye:** Kalibrasyon küpü bastınız. Üstü 20mm ama en altı 20.5mm geliyor. Parçalar birbirine geçmiyor.

**Teknik Analiz:**
Ağır modelin ve sıcak tablanın etkisiyle, ilk katmanlar "ezilir".

**Profesyonel Çözüm:**
Slicer'da **"Elephant Foot Compensation"** (veya Initial Layer Horizontal Expansion) ayarını bulun. Buraya **-0.2mm** değerini girin. Yazılım, ilk katmanı bilerek küçük basacak, ezilince tam ölçüye gelecektir.

### 7. Yastıklama (Pillowing)

**Hikaye:** Modelin üst yüzeyi pürüzsüz değil, içinde hava kabarcıkları patlamış gibi delikler veya çukurlar var.

**Teknik Analiz:**
İç dolgunun (infill) üzerine attığınız tavan katmanları, alttaki boşluğa sarkıyor. Sıcak hava içeride hapsolup yukarı doğru bombe yapıyor.

**Profesyonel Çözüm:**
1.  **Katman Sayısı:** Top Shell Layers (Üst Kabuk Katmanları) en az **4 veya 5** olsun.
2.  **Dolgu:** İnfill oranını artırın veya **"Gradual Infill"** kullanarak sadece tavana yakın yerlerde dolguyu sıklaştırın.

### 8. Ghosting (Ringing ve Input Shaping)

![Yüzeyde dalgalanma](/images/hata-ghosting.jpg "Mekanik titreşimin plastik üzerindeki imzası.")

**Hikaye:** Modelin yüzeyinde, özellikle yazıların veya keskin köşelerin yanında "eko" yapmış gibi tekrarlayan dalgalar var.

**Teknik Analiz:**
Yazıcı kafası ağır bir kütledir. Hızlı hareket edip aniden durduğunda (köşelerde), şasi titremeye devam eder (Jerk). Bu titreşim plastiğe yansır.

**Profesyonel Çözüm (2025 Metodu):**
*   **Mekanik:** Kayışları gerin, yazıcıyı sağlam bir masaya koyun.
*   **Yazılım (Klipper/Marlin):** **Input Shaping** kalibrasyonu yapın. Bu teknoloji, titreşimi ölçer ve motorlara "anti-titreşim" sinyali göndererek bu dalgaları %100 yok eder.

### 9. Z-Banding (Vidalı Mil Sorunu)

**Hikaye:** Modelin yan duvarlarında düzenli aralıklarla (örneğin her 2mm'de bir) tekrar eden çizgiler var.

**Teknik Analiz:**
Z eksenini kaldıran vidalı mil (Lead Screw) hafifçe yamuktur veya motor kaplini mili "yalpalamalı" döndürüyordur (Z-Wobble).

**Profesyonel Çözüm:**
*   Vidalı mili söküp düz bir masada yuvarlayın, yamuksa değiştirin.
*   Motor ile mili bağlayan **esnek kaplinin** vidalarını gevşetip, mili düzeltip tekrar sıkın.
*   **PID Tuning:** Bazen bu çizgiler mekanik değil, sıcaklık dalgalanmasıdır (Thermal Banding). Tablanıza PID kalibrasyonu yapın.

### 10. Eksik Ekstrüzyon (Under-Extrusion & Flow)

**Hikaye:** Katmanların arası tam yapışmamış, model süngerimsi ve zayıf.

**Teknik Analiz:**
Slicer "100 birim plastik bas" diyor ama nozzle'dan 90 birim çıkıyor.

**Profesyonel Çözüm:**
1.  **Mekanik:** Extruder dişlisine bakın. Dişli toz dolmuşsa filamenti kavrayamaz, kaydırır. Temizleyin.
2.  **Volumetrik Hız:** Çok hızlı basıyorsanız, hotend plastiği eritmeye yetişemiyor olabilir (Max Volumetric Speed limiti). Hızı düşürün veya sıcaklığı artırın.
3.  **Flow Rate:** Slicer'dan "Flow Ratio"yu artırın (Örn: 0.98'den 1.05'e).

---

## Sonuç: Hata Yoktur, Veri Vardır

Gördüğünüz gibi, "Baskım bozuldu" demek yerine "Flow yetersiz kaldı" veya "Input Shaping ayarım kaçmış" dediğiniz an, artık bir amatör değil, bir operatörsünüz demektir.

Makinemizin dilini çözdük, hastalıklarını tedavi ettik. Peki bu hastalıklar hiç oluşmasın diye ne yapabiliriz? Tıpkı arabanızın yağını değiştirdiğiniz gibi, yazıcınızın da bir bakım takvimi olmalı.

### Yolculuğun Bir Sonraki Durağı

Yazıcıyı ne sıklıkla yağlamalı? Nozzle ne zaman değişmeli? Kayışların ömrü ne kadar? Makinenizi ilk günkü performansında tutacak bakım sırları.

<div class="post-cta-box">
<h3>Sırada: 3D Yazıcı Bakım Rehberi</h3>
<p>Kriz anını bekleme, önlemini al. Haftalık, aylık ve yıllık bakım rutinleri ile yazıcını 'sıfır' kondisyonunda tut.</p>
<a href="{{< ref "posts/3d-yazici-bakim-rehberi.md" >}}" class="cta-button">Bakım Rehberine Git →</a>
</div>