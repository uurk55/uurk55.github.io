---
title: "Esnek Filament Rehberi: TPU, TPE ve Soft PLA Arasındaki Farklar"
date: 2025-09-05T12:45:00+03:00
featured: true
draft: false
description: "Sadece TPU yok! TPE, Soft PLA ve TPC nedir? Shore sertlik skalası (95A vs 85A) baskıyı nasıl etkiler? Esnek malzemelerin kimyası ve basım teknikleri."
tags: ["Esnek Filament", "TPU", "TPE", "Soft PLA", "Shore Hardness", "Shore Sertliği", "Slicer Ayarları", "Direct Drive", "Baskı Malzemeleri"]
categories: ["Beceri Geliştirme ve İleri Teknikler"]
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
    image: "/images/flexible-filament-cover.png"
    alt: "Farklı esneklik seviyelerindeki (TPU, TPE) baskı parçalarının bükülme testi"
    caption: "Esneklik tek tip değildir. Araba lastiğinden paket lastiğine kadar bir yelpazedir."
    relative: false
---

Şimdiye kadar PLA, PETG gibi sert plastiklerle çalıştık. Ancak mühendislik ve hobi dünyasında bazen "kırılmayan", "bükülen" veya "yumuşak dokulu" parçalara ihtiyaç duyarız.

Çoğu kişi esnek filament denince sadece **TPU**'yu bilir. Oysa esnek filamentler geniş bir ailedir. **TPE**, **Soft PLA** ve **TPC** gibi farklı kimyasal yapılara ve sertlik derecelerine sahip çeşitleri vardır.

Bir telefon kılıfı basmakla, bir drone tekerleği basmak aynı malzeme ile olmaz. Biri sertçe esnemeli, diğeri yumuşacık olmalıdır.

Bu rehberde, "Shore Sertlik Skalası"nı öğrenecek ve projenize en uygun esnek malzemeyi (ve onu nasıl basacağınızı) seçeceksiniz.

---

## 1. Esnekliğin Ölçüsü: Shore Sertlik Skalası (Shore Hardness)

Esnek filament alırken kutunun üzerinde **95A**, **85A** veya **60D** gibi kodlar görürsünüz. Bu, malzemenin ne kadar yumuşak olduğunu gösterir.

*   **98A - 95A (Sert Esnek):** Araba lastiği kıvamındadır. Piyasada bulacağınız standart TPU budur. Basması en kolay olanıdır.
*   **85A (Orta Yumuşak):** Ayakkabı topuğu kıvamındadır. Basması zordur, extruder içinde bükülebilir. Genelde TPE'ler bu aralıktadır.
*   **60A - 70A (Çok Yumuşak):** Paket lastiği gibidir. Sadece özel extruderlar ile basılabilir.

**Kural:** Sayı düştükçe yumuşaklık artar, ancak **basım zorluğu da artar.**

## 2. Malzeme Türleri: Hangisini Seçmeli?

### A. TPU (Termoplastik Poliüretan) - *Standart Savaşçı*
En yaygın ve ulaşılabilir olandır.
*   **Özellik:** Yağa, gres yağına ve aşınmaya çok dayanıklıdır. Genelde 95A sertliğindedir.
*   **Kullanım:** Telefon kılıfları, drone parçaları, contalar, koruyucu kapaklar.
*   **Basılabilirlik:** Orta seviye. Direct Drive ile kolay, Bowden ile zordur.

### B. TPE (Termoplastik Elastomer) - *Gerçek Lastik*
TPU'nun "babasıdır" ama genelde daha yumuşak versiyonları (85A ve altı) ifade etmek için kullanılır.
*   **Özellik:** TPU'dan daha yumuşaktır, dokunuşu daha "kadifemsi" ve lastik hissi verir. Daha iyi esner.
*   **Kullanım:** Giyilebilir teknolojiler, yumuşak tutamaklar (grip), titreşim sönümleyiciler.
*   **Basılabilirlik:** Zor. Filament extruder dişlisine dolanmaya çok meyillidir.

### C. Soft PLA (Esnek PLA) - *Yalancı Bahar*
PLA'nın kimyasal yapısının esnetilmiş halidir.
*   **Özellik:** TPU kadar esnemez, daha çok "bükülebilir sert plastik" gibidir. Kırılmadan bükülür ama lastik gibi uzamaz.
*   **Kullanım:** Darbe alacak ama formunu koruması gereken parçalar (RC araba tamponları).
*   **Basılabilirlik:** Standart PLA ayarlarıyla (biraz yavaşlatarak) basılabilir. En kolayıdır.

---

## 3. Basım Teknikleri: Başarının 3 Altın Kuralı

Malzemeyi seçtik. Peki makineyi tıkamadan, o pahalı filamenti çöp etmeden nasıl basacağız? İster TPU ister TPE olsun, kurallar benzerdir ancak **yumuşaklık arttıkça kurallar katılaşır.**

### Kural 1: Hız Felakettir (Yavaşlayın!)
Sert bir çubuğu (PLA) hızlıca itebilirsiniz ama pişmiş bir spagettiyi (TPE) hızlı iterseniz, tüpün içinde bükülür.
*   **TPU (95A):** 30-40 mm/s.
*   **TPE (85A):** 15-20 mm/s. (Sabırlı olun).

### Kural 2: Retraction (Geri Çekme) Ayarı
Sert plastiği geri çekebilirsiniz ama lastiği çekerseniz uzar ve çapı incelir.
*   **Direct Drive:** 0.5mm - 1.0mm arası, çok düşük hızda (20mm/s).
*   **Bowden:** Retraction'ı **tamamen kapatın** (0mm). Biraz ipliklenme (stringing) olacaktır ama tıkanmasından iyidir. O iplikleri sonra yakarsınız.

### Kural 3: Extruder Tipi ve Baskı Yolu
*   **Direct Drive Şart mı?** TPU (95A) için şart değil ama çok tavsiye edilir. TPE (85A) için ise **zorunludur.**
*   **Filament Yolu:** Filament makarası rahat dönmeli. Gerekirse makarayı rulmanlı bir tutucuya koyun. Extruder motoru filamenti çekerken zorlanmamalı.

{{< tip-box title="💡 Nem Uyarısı" >}}
Tüm esnek filamentler (TPU, TPE, TPC) havadaki nemi sünger gibi çeker. Nemli filament basarken "çıtırtı" sesi çıkarır ve yüzey delik deşik olur. Baskıdan önce **mutlaka kurutun.** (50-55°C, 4-6 Saat).
{{< /tip-box >}}

---

## Sonuç: Hangi Malzeme Sizin İçin?

*   **Yeni Başlıyorum:** **Soft PLA** veya **95A TPU** (Marka: eSun, SainSmart) alın.
*   **Telefon Kılıfı Basacağım:** **95A TPU** idealdir.
*   **Yumuşak Conta/Lastik Basacağım:** **85A TPE** (Marka: Recreus FilaFlex) gerekir ama yazıcınızın Direct Drive olduğundan emin olun.

Malzemeyi tanıdık, ayarları yaptık. Artık tek renkli dünyadan çıkıp biraz renklenelim mi? Bambu Lab AMS gibi pahalı sistemleriniz olmasa bile, tek bir yazıcıyla nasıl çok renkli baskılar alabilirsiniz?

### Yolculuğun Bir Sonraki Durağı

Pahalı ekipmanlar olmadan, **katman değiştirme (Layer Swap)** yöntemiyle renkli tabelalar, logolar ve anahtarlıklar basmanın sırları.

<div class="post-cta-box">
<h3>Sırada: Çok Renkli 3D Baskıya Giriş</h3>
<p>Tek nozzle ile renk cümbüşü. M600 kodu nedir? Katmanlarda renk değişimi nasıl yapılır? Basit tekniklerle profesyonel renkli baskılar.</p>
<a href="{{< ref "posts/cok-renkli-3d-baski-rehberi.md" >}}" class="cta-button">Renkli Baskı Rehberine Git →</a>
</div>