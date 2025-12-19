---
title: "3D Yazıcı Kalibrasyonu: Mükemmel Baskılar İçin A'dan Z'ye Rehber"
date: 2025-07-29T10:00:00+03:00
featured: false
draft: false
description: "Baskılarınız ölçü tutmuyor mu? Yüzeyler pürüzlü mü? O meşhur 'E-Steps' nedir? Uğur Kapancı'nın atölye tecrübeleriyle adım adım kalibrasyon rehberi."
tags: ["3D Yazıcı Kalibrasyonu", "Baskı Kalitesi", "E-steps", "PID Ayarı", "Flow Kalibrasyonu", "Z-Offset", "3D Yazıcı Ayarları", "Baskı Hataları", "Input Shaping", "Basınç İlerlemesi"]
categories: ["Teknik İpuçları"]
faz: ["Faz 1"]
series: ["3D Baskı Temelleri Serisi"]
author: "Uğur Kapancı"
showToc: true
TocOpen: true
comments: true
ShowReadingTime: true
ShowPostNavLinks: true
cover:
    image: "/images/calibration-cover.png"
    alt: "Kumpas, G-code terminali ve kalibrasyon küpü ile bir çalışma masası"
    caption: "Kalibrasyon, yazıcının sizinle aynı dili konuşmasını sağlama sanatıdır."
    relative: false
---

İlk yazıcımı aldığımda bastığım o 20mm'lik kalibrasyon küpü 19.2mm çıkmıştı. "Ne olacak canım, 1mm'den bir şey olmaz" demiştim.

Sonra bir gün, tasarladığım bir kutu kapağını basıp yerine oturtmaya çalıştığımda acı gerçekle yüzleştim: Kapak girmiyordu. Zımparaladım, yine girmedi. Isıttım, yamuldu. Sonunda o baskıyı çöpe atıp, yazıcının başına "kalibrasyon" yapmak için oturdum.

Kalibrasyon, yazıcınızın "Ben 10cm gittim" dediğinde gerçekten 10cm gidip gitmediğini kontrol etmektir. Eğer bu ayarı yapmazsanız, vida delikleri oturmaz, dişliler dönmez ve parçalar birbirine geçmez.

Bu rehberde, internette kaybolmadan, en hayati 5 kalibrasyonu sırasıyla yapacağız.

### Başlamadan Önce: Çantanızda Neler Var?
Bu savaşa silahsız girmeyin. Şunlar elinizin altında olsun:
*   **📏 Dijital Kumpas:** Cetvelle olmaz. Kumpas şart.
*   **📄 A4 Kağıdı:** Z-Offset için.
*   **💻 Bir Terminal Programı:** Eğer yazıcınızda Klipper yoksa, "Pronterface" gibi bir programla USB'den bağlanmanız gerekebilir. (Bambu Lab veya Klipper'lı cihazlarda web arayüzü yeterli).

---

### Adım 1: Mekanik Kontrol (Vida Sıkma Sanatı)

Yazılım ayarına girmeden önce, makinenin fiziksel sağlığına bakalım. Gevşek bir vida, en iyi yazılım ayarını bile bozar.
*   **Eksantrik Somunlar:** Kurulum rehberinde bahsetmiştik. Tekerlekler ne çok sıkı ne çok gevşek olacak.
*   **Kayışlar:** Gitar teli gibi olmalı. Parmağınızla dokunduğunuzda tok bir ses gelmeli ama kopacak kadar da gergin olmamalı.

---

### Adım 2: E-Steps Kalibrasyonu (Motorun Adım Sayısı)

Bu, kalibrasyonun babasıdır. Siz makineye "10cm filament it" dediğinizde, o gerçekten 10cm itiyor mu? Yoksa 9cm itip "ittim abi" mi diyor?

1.  **İşaretle:** Extruder'ın (filamenti iten motorun) girişinden itibaren 120mm'yi cetvelle ölçüp filamentin üzerine kalemle çizik atın.
2.  **Komut Ver:** Menüden veya bilgisayardan `G1 E100 F100` komutuyla (veya menüden "Extrude 100mm" diyerek) 100mm itmesini söyleyin.
3.  **Ölç:** İşaretlediğiniz çizgi ile extruder girişi arasındaki mesafeyi ölçün.
    *   İdealde **20mm** kalmalı (120 - 100 = 20).
    *   Eğer 25mm kaldıysa, makine 5mm eksik itmiş demektir (Under-extrusion).
    *   Eğer 15mm kaldıysa, makine 5mm fazla itmiş demektir (Over-extrusion).
4.  **Hesapla:** `Yeni E-Step = (Eski E-Step * 100) / (120 - Kalan Mesafe)` formülüyle yeni değeri bulup makineye kaydedin.

![Bir kişinin elinde mezura ile 3D yazıcının ekstrüderinden çıkan filamenti ölçtüğü yakın çekim.](/images/e-steps-calibration.png "E-Steps: Makinenin ne kadar yediğini kontrol etmektir.")

---

### Adım 3: Flow (Akış) Kalibrasyonu

E-Steps motorun ne kadar döndüğünü ayarlar. Flow ise o plastiğin nozzle'dan ne kadar şişerek çıktığını ayarlar.
1.  **Küp Bas:** İçi boş, tek duvarlı (vase mode değil, 0% infill, 0 top layer) bir küp basın.
2.  **Ölç:** Kumpasla duvar kalınlığını ölçün. Slicer'da "0.4mm" ayarladıysanız ve kumpasta "0.45mm" görüyorsanız, makine fazla malzeme basıyor demektir.
3.  **Ayarla:** Slicer'daki "Flow Ratio" (Akış Oranı) ayarını düşürün. Genelde **0.95 ile 0.98** arası idealdir.

![Bir kişinin elinde kumpas ile tek duvarlı bir 3D baskı küpünün duvar kalınlığını ölçtüğü yakın çekim.](/images/flow-calibration.png "Flow ayarı, parçaların birbirine geçmesini sağlar.")

---

### Adım 4: PID Tuning (Sıcaklık Dansı)

Nozzle sıcaklığınız baskı sırasında 200°C -> 195°C -> 205°C diye dalgalanıyorsa, katmanlarınızda çizgiler oluşur. PID ayarı, bu dalgalanmayı önler.
*   **Nasıl Yapılır:** Terminalden `M303 E0 S200 C5` komutunu gönderin. Makine 5 kere ısınıp soğuyarak kendini test edecek ve size `Kp, Ki, Kd` değerleri verecek. Bu değerleri `M301` komutuyla kaydedin. (Çoğu modern yazıcıda menüden "PID Autotune" seçeneği vardır).

---

### Adım 5: Z-Offset (Yine ve Yeniden)

Her kalibrasyondan sonra Z-Offset (ilk katman yüksekliği) değişebilir. En son mutlaka bir "First Layer Test" basarak, ilk katmanın o pürüzsüz, tek parça halini görün. Tırnağınızla kazıdığınızda gelmemeli.

---

## Sonuç: Artık Makineye Hükmediyorsunuz

Tebrikler! Artık "Umarım düzgün çıkar" diye dua eden bir kullanıcı değil, "Düzgün çıkacak çünkü ben ayarladım" diyen bir operatörsünüz. Bu ayarları bir kere yaptığınızda, o ucuz Çin malı yazıcınızın bile nasıl binlerce dolarlık makineler gibi bastığına şaşıracaksınız.

Peki makineyi ayarladık, şimdi içine ne koyacağız? PLA mı, PETG mi yoksa o kokulu ABS mi? Hangi malzeme ne işe yarar?

### Yolculuğun Bir Sonraki Durağı

Yazıcınız hazır, peki ya malzemeniz? Her flament her işe yaramaz. Telefon kılıfı için TPU, araba parçası için ASA... Gel, doğru malzemeyi seçelim.

<div class="post-cta-box">
<h3>Sırada: 3D Baskı Malzeme Rehberi</h3>
<p>Hangi plastik nerede kullanılır? PLA neden güneşte erir? PETG neden en iyi dostunuz olacak? Malzeme dünyasının sırları.</p>
<a href="{{< ref "posts/3d-baski-malzeme-rehberi.md" >}}" class="cta-button">Malzeme Rehberine Git →</a>
</div>