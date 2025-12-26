---
title: "Temel Slicer Ayarları: Baskı Kalitenizi Değiştirecek 5+1 Kritik Ayar"
date: 2025-08-05T11:00:00+03:00
featured: true
draft: false
description: "Slicer sadece 'Dilimle' butonuna basmak değildir. Gyroid dolgu, Arachne duvarlar, Z-Seam gizleme ve Ironing... Baskılarınızı amatörlükten profesyonelliğe taşıyacak ileri seviye ayarlar."
tags: ["Slicer Ayarları", "OrcaSlicer", "Bambu Studio", "Cura", "Arachne", "Gyroid Dolgu", "Z Seam", "Ironing", "Baskı Kalitesi", "Destek Ayarları"]
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
    image: "/images/slicer-ayar-cover.jpg"
    alt: "OrcaSlicer arayüzünde detaylı ayar menüleri ve yanında pürüzsüz bir baskı"
    caption: "Amatörler 'Yazdır'a basar, profesyoneller ayarları yönetir."
    relative: false
---

Harika bir 3D model indirdiniz, en kaliteli filamenti aldınız. Ama baskı bittiğinde sonuç hüsran: Duvarlar zayıf, üst yüzey pürüzlü, destekleri sökerken model kırıldı...

Suçu yazıcıya atmadan önce durun. Sorun %90 ihtimalle, dijital model ile fiziksel makine arasındaki tercümanda, yani **Dilimleyici (Slicer)** ayarlarındadır.

Slicer, sadece "Dilimle" butonuna basıp G-Code aldığınız bir araç değildir. O, yazıcının beynidir. Ben atölyemde aynı yazıcıyı kullanan iki kişinin baskılarına baktığımda kimin Slicer'a hakim olduğunu, kimin "varsayılan ayarlarda" gezindiğini hemen anlarım.

Bu rehberde, basit ayarları geçiyoruz. Sizi 2025 standartlarında profesyonel sonuçlara götürecek, **OrcaSlicer**, **Bambu Studio** ve **Cura**'nın derinliklerindeki o "sihirli" ayarları konuşacağız.

---

## 1. Katman Yüksekliği: "Adaptive" (Değişken) Katmanlar

Herkes `0.20mm` standart katman yüksekliğini bilir. Ama profesyonel bir sır vereyim: **Adaptive Layer Height (Değişken Katman Yüksekliği).**

Bir figür bastığınızı düşünün. Gövdesi düz bir silindir, kafası ise detaylı kıvrımlar içeriyor.
*   **Standart:** Her yeri 0.12mm basarsanız, baskı 20 saat sürer.
*   **Adaptive:** Slicer, düz duvarları 0.28mm (hızlı) basarken, kafadaki kıvrımlara geldiğinde otomatik olarak 0.08mm'ye (detaylı) düşer.

**Nasıl Yapılır?**
OrcaSlicer veya Bambu Studio'da sağ üstteki araç çubuğunda "Adaptive" ikonuna tıklayın. Yazılım, modelin eğimine göre katmanları otomatik ayarlar. Hem zamandan kazanırsınız hem kaliteden ödün vermezsiniz.

## 2. Duvarlar (Walls): "Arachne" Motoru ve Sağlamlık

Eskiden "Classic" duvar örücüler vardı. Şimdi **Arachne** var.
Arachne motoru, duvar kalınlığını dinamik olarak değiştirir. İnce bir boşluk varsa orayı doldurmak için nozzle akışını kısar veya artırır.
*   **Duvar Sayısı:** Sağlamlık istiyorsanız dolguyu (infill) artırmayın. **Duvar sayısını (Wall Loops) 3 veya 4 yapın.** Bir parçayı sağlam yapan şey kabuğudur, içi değil.

{{< tip-box title="💡 Usta İpucu: Dış Duvar Hızı" >}}
Baskı süresini kısaltmak için iç duvarları (Inner Wall) 150-200 mm/s basabilirsiniz. Ama **Dış Duvar (Outer Wall)** hızını her zaman **50-60 mm/s** seviyesinde tutun. Vitrine koyduğunuzda gördüğünüz tek yer orasıdır.
{{< /tip-box >}}

## 3. Dolgu (Infill): Grid Öldü, Yaşasın Gyroid ve Lightning!

Eğer hala "Grid" (Izgara) veya "Triangles" kullanıyorsanız, yazıcınıza eziyet ediyorsunuz.
*   **Neden Grid Kullanmam?** Çizgiler her katmanda birbiriyle kesişir. Nozzle bu kesişimlere çarparak "tık tık" ses yapar ve modeli tabladan koparabilir.
*   **Kral: Gyroid:** Dalgalı bir yapıdır. Nozzle asla kendi yoluyla kesişmez. Her yöne eşit sağlamlık verir.
*   **Tasarrufçu: Lightning:** Eğer sadece görsel bir büst basıyorsanız ve sağlamlık önemsizse "Lightning" seçin. Sadece tavanı tutacak kadar, ağaç dalı gibi dolgu atar. %50 malzeme tasarrufu sağlar.

## 4. Destekler (Supports): Z-Distance Sırrı

Destekleri sökerken modelde iz kalıyor veya model kırılıyor mu? Sorun "Top Z Distance" ayarında.
*   **Ağaç (Tree) Destek:** Karakter ve organik modeller için standarttır.
*   **Kritik Ayar (Top Z Distance):** Destek ile model arasındaki boşluktur.
    *   Kolay sökülsün diyorsanız: **0.20mm** (veya katman yüksekliğiniz kadar).
    *   Yüzey çok temiz olsun (ama zor sökülür) diyorsanız: **0.12mm**.
*   **Support Interface:** Bunu açarsanız, desteğin tepesine yoğun bir çatı örer. Destek kalıp gibi çıkar, iz bırakmaz.

## 5. Dikiş İzi (Seam): O Çirkin Çizgiyi Gizlemek

Baskınızın bir yerinde, aşağıdan yukarıya doğru giden bir "fermuar izi" mi var? Buna **Z-Seam** denir. Nozzle'ın katmana başladığı ve bitirdiği yerdir.
*   **Random (Rastgele):** Yapmayın. Modelin her yerinde sivilce gibi noktalar olur.
*   **Aligned (Hizalı):** Tek bir çizgi halinde yapar.
*   **Pro Tercih (Scarf Joint):** OrcaSlicer'ın yeni özelliği. Dikiş izini yok etmek için başlangıç ve bitiş noktalarını birbirine kaynaştırır. Mutlaka deneyin.
*   **Manuel Boyama (Seam Painting):** Dikiş izini modelin arkasına, görünmeyen bir köşesine elle çizin.

## +1 Bonus: Ütüleme (Ironing)

Baskının en üst yüzeyi pürüzlü mü duruyor?
**Ironing (Ütüleme)** özelliğini açın.
Yazıcı en üst katmanı bitirdikten sonra, nozzle'ı çok az plastik akıtarak (veya hiç akıtmayarak) yüzeyin üzerinden tekrar geçirir. Tıpkı gömlek ütüler gibi, plastik pürüzsüzleşir. Düz, yassı modellerde (anahtarlık, kutu kapağı vb.) enjeksiyon kalıp kalitesi alırsınız.

---

{{< success-story-box title="✨ Kendi Tecrübem: Kırılan Drone Parçası" >}}
Bir drone için kol parçası basıyordum. %100 dolgu yapmama rağmen ilk düşüşte kırıldı. Sonra Slicer ayarlarını değiştirdim: Dolguyu %40'a düşürdüm ama **Duvar Sayısını 6'ya çıkardım**. Ayrıca **Gyroid** dolgu kullandım. Sonuç? O drone 5 kere daha düştü, parça hala sağlam. Slicer, malzemeden daha önemlidir.
{{< /success-story-box >}}

## Sonuç: Denemekten Korkmayın

Bu ayarlar başta karmaşık gelebilir. Tavsiyem; küçük bir test küpü alın ve her seferinde sadece **TEK BİR** ayarı değiştirerek basın.
*   Önce Gyroid'i deneyin.
*   Sonra Ironing'i açın.
*   Sonra Seam yerini değiştirin.

Farkı gözünüzle gördüğünüzde, "Ben daha önce baskı almıyormuşum" diyeceksiniz.

Peki, ayarları yaptık ama baskıda hala ipliklenme (stringing) var veya taban köşelerden kalkıyor (warping). Ayar mı yanlış, makine mi bozuk?

### Yolculuğun Bir Sonraki Durağı

Hastalığı teşhis etmeden ilacı veremeyiz. 3D baskıların en belalı 10 hastalığını, belirtilerini ve reçetelerini hazırladık.

<div class="post-cta-box">
<h3>Sırada: En Yaygın 10 Baskı Hatası ve Çözümleri</h3>
<p>Stringing, Warping, Layer Shift... Baskılarınızdaki sorunları bir doktor gibi teşhis edip çözme rehberi.</p>
<a href="{{< ref "posts/3d-baski-hatalari-cozumleri.md" >}}" class="cta-button">Hata Çözüm Rehberine Git →</a>
</div>