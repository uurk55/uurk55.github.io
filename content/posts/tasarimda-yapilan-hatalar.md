---
title: "Tasarımda Yapılan Hatalar ve Öğrenilen Dersler"
date: 2025-09-02T10:00:00+03:00
featured: false
draft: false
description: "Duvarlar neden kağıt gibi çıktı? Kapak neden kapanmıyor? 3D tasarımda en sık yapılan 5 teknik hata (Non-manifold, Tolerans, Oryantasyon) ve bunları önlemenin mühendislik kuralları."
tags: ["3D Tasarım Hataları", "Tolerans Ayarı", "Duvar Kalınlığı", "Non-Manifold", "Tasarım İpuçları", "Baskı Hataları", "Fusion 360 Hataları", "Tinkercad Hataları", "DFAM"]
categories: ["Tasarım"]
faz: ["Faz 2"]
series: ["3D Baskı Rehberleri"]
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
    image: "/images/tasarim-hatalari-cover.jpg"
    alt: "Hatalı basılmış, kırık ve birbirine uymayan 3D parçalar ile bilgisayar ekranındaki CAD çizimi"
    caption: "Bu hatalar yazıcıdan değil, çizim masasındaki kararlardan kaynaklanıyor."
    relative: false
---

3D modelleme programlarını (Tinkercad, Fusion 360) öğrendiniz, bir şeyler çizip bastınız. Ama elinize aldığınız parça ya elinizde kırıldı, ya kapağı kapanmadı ya da dilimleyici (Slicer) programı modeli "bozuk" olarak işaretledi.

Suçu hemen yazıcıda aramayın. Çoğu zaman suçlu, **tasarımın kendisidir.**

Sanal ortamda (CAD), fizik kuralları işlemez. 0.001mm kalınlığında bir duvar çizebilirsiniz ve program buna itiraz etmez. Ama gerçek dünyada o duvarı basacak nozzle 0.4mm'dir ve fiziksel limitleri vardır.

Bu yazıda, "Güzel görünen" değil, **"Üretilebilir"** tasarım yapmanın teknik kurallarını ve benim de öğrenirken yüzlerce gram filamenti çöpe atmama neden olan **en kritik 5 tasarım hatasını** inceleyeceğiz.

---

## 1. Hata: Nozzle Çapını Yok Saymak (İnce Duvarlar)

Tasarım yaparken estetik kaygılarla duvarları çok inceltirseniz, Slicer programı o duvarları "yok" sayar veya yazıcı oraya sadece kesik kesik noktalar bırakır.

*   **Teknik Gerçek:** Standart bir nozzle **0.4mm** çapındadır. Yazıcı bu çapın altındaki bir kalınlığı (örn: 0.3mm) fiziksel olarak basamaz.
*   **Çözüm:** Tasarımlarınızda duvar kalınlığı (Wall Thickness) her zaman nozzle çapının katları olmalıdır.
    *   **Minimum:** 0.8mm (2 Duvar geçişi - Perimeters).
    *   **İdeal:** 1.2mm (3 Duvar) veya 1.6mm (4 Duvar) sağlamlık için standarttır.
*   **Ders:** 1.0mm duvar çizerseniz, yazıcı 0.4 + 0.4 basar, ortada 0.2mm boşluk kalır (gap). Slicer bunu "gap fill" ile doldurmaya çalışır ama yapı zayıflar. Ölçülerinizi nozzle'a göre (0.4'ün katları) ayarlayın.

## 2. Hata: Sıfıra Sıfır Tasarım (Tolerans Yokluğu)

Bir vida ve somun tasarladınız. Vida çapı 10mm, somun deliği 10mm. Ekranda harika görünüyor.
**Sonuç:** O somun, o vidaya asla girmez.

Plastik soğurken büzülür (shrinkage), ayrıca nozzle'dan akan plastik hafifçe yayılır.
*   **Teknik Gerçek:** FDM yazıcılarda 0 tolerans imkansızdır.
*   **Çözüm:** İç içe geçecek parçalar arasında mutlaka **boşluk (Clearance/Tolerance)** bırakın.
    *   **Sıkı Geçme (Press Fit):** 0.1mm - 0.15mm toplam boşluk. (Çekiçle girer).
    *   **Rahat Geçme (Slide Fit):** 0.2mm - 0.3mm toplam boşluk. (Kapaklar için).
    *   **Serbest Hareket:** 0.4mm+ boşluk. (Menteşeler için).
*   **Uygulama:** 10mm'lik bir deliğe girecek pim tasarlıyorsanız, pimi 10mm değil, **9.7mm** çizin.

## 3. Hata: Yanlış Oryantasyon (Z Ekseni Zayıflığı)

Bir parçanın sağlamlığı, basıldığı yöne göre değişir. FDM baskılar, tıpkı ahşabın damarları gibi, katmanların yapıştığı yönde (Z ekseni) zayıftır.

*   **Senaryo:** Dikey duran ince, uzun bir çubuk tasarladınız. Bunu elinizle büktüğünüzde "çıt" diye katman yerlerinden kopar.
*   **Çözüm:** Aynı çubuğu yatay olarak tasarlayıp basarsanız, plastik lifleri boylu boyunca uzanır ve kırılması çok zorlaşır.
*   **Ders:** Tasarımı yaparken, parçanın maruz kalacağı kuvveti düşünün. Yük binecek yön, katman çizgilerine **dik** olmamalıdır.

![Dikey ve yatay basılmış iki parçanın kırılma testini gösteren grafik](/images/layer-orientation.jpg "Yatay basılan parça, dikey basılana göre kat kat daha sağlamdır.")

## 4. Hata: Fil Ayağını Unutmak (Elephant's Foot)

İlk katman, tablaya iyi yapışması için nozzle tarafından biraz fazla ezilir (Squish). Bu da tabanda dışa doğru hafif bir taşma (şişkinlik) yaratır. Eğer iki parça birleşecekse veya bir kutuya kapak girecekse, bu şişkinlik montajı engeller.

*   **Çözüm (Chamfer):** Tasarımınızın tabana değen kenarlarına **Pah (Chamfer)** verin.
*   **Neden Fillet Değil?** Yuvarlama (Fillet) tabanda çok dik başlar ve destek gerektirebilir. 45 derecelik bir Chamfer (örneğin 0.5mm veya 1mm), fil ayağı etkisini absorbe eder ve parça tam oturur.

## 5. Hata: "Non-Manifold" (Su Geçirmez Olmayan) Geometri

Bu, özellikle Blender veya Tinkercad'de karmaşık şekillerle çalışırken olur. Bir modelin basılabilmesi için matematiksel olarak "su geçirmez" (watertight) olması gerekir. Yüzeyinde delik, ters dönmüş yüzeyler (normals) veya hacmi olmayan çizgiler bulunmamalıdır.

*   **Belirti:** Slicer programında modelinizde garip boşluklar oluşuyor, içini dolu sanıyor veya "Model hatalı, onarılsın mı?" uyarısı veriyor.
*   **Çözüm:**
    *   Tinkercad/Fusion'da parçaları sadece "yan yana" koymayın, mutlaka **"Combine" / "Group" / "Boolean Union"** komutlarıyla tek bir gövde haline getirin.
    *   İç içe geçmiş yüzeyleri temizleyin.

{{< tip-box title="💡 Hızlı Onarım Aracı" >}}
Windows kullanıyorsanız, şüpheli STL dosyasını **"3D Builder"** (Windows ile gelen ücretsiz program) ile açın. Hata varsa sağ altta "Onarmak için tıklayın" der ve otomatik düzeltir. Bu basit araç, Slicer'ların düzeltemediği birçok bozuk tasarımı kurtarır.
{{< /tip-box >}}

---

## Sonuç: Hata Yapın, Ama Not Alın

Bu hataların hepsi, tasarım sürecinin doğal bir parçasıdır. Önemli olan, "Yazıcı bozuk" demek yerine "Tasarımda nerede hata yaptım?" diyebilmektir. Tasarım masasında harcanan fazladan 10 dakika, baskı masasında harcanacak saatleri kurtarır.

Tasarımımız teknik olarak kusursuz olsa bile, bazen fizik kuralları (yer çekimi) bizi zorlar. Havada duran bir kolu veya 90 derecelik bir çıkıntıyı nasıl basacağız? Tasarımı değiştiremiyorsak, yazıcıdan ve Slicer'dan yardım almalıyız.

### Yolculuğun Bir Sonraki Durağı

Yer çekimine meydan okumanın yolu: **Destek Yapıları (Supports).**
Hangi destek türü nerede kullanılır? "Ağaç" (Tree) destek mi, normal destek mi? İz bırakmadan destek sökmenin sırları neler?

<div class="post-cta-box">
<h3>Sırada: Destek Yapıları (Supports) Rehberi</h3>
<p>Her model desteksiz basılamaz. Karmaşık tasarımları çökmeden basmak ve destekleri temizlerken modeli kırmamak için teknik rehber.</p>
<a href="{{< ref "posts/destek-yapilari-supports-rehberi.md" >}}" class="cta-button">Destek Rehberine Git →</a>
</div>