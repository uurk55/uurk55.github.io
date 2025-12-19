---
title: "FDM 3D Yazıcı İlk Kurulum Rehberi: Kutudan İlk Başarılı Baskıya"
date: 2025-07-18T10:00:00+03:00
featured: false
draft: false
description: "Yeni FDM 3D yazıcınızı kutudan çıkarıp ilk başarılı baskınızı almak için adım adım kurulum rehberi. Montaj, eksantrik somun ayarı, otomatik kalibrasyon (Z-Offset) ve ilk katman testi."
tags: ["FDM Kurulum", "3D Yazıcı Montaj", "Z-Offset Ayarı", "Auto Leveling", "İlk Baskı", "Eksantrik Somun", "Benchy", "Kurulum Hataları"]
categories: ["Başlangıç Rehberi"]
faz: ["Faz 1"]
series: ["3D Baskı Temelleri Serisi"]
author: "Uğur Kapancı"
showToc: true
TocOpen: true
comments: true
ShowReadingTime: true
ShowPostNavLinks: true
cover:
    image: "/images/kurulum-rehberi-cover.jpg"
    alt: "Kutudan yeni çıkmış ve montajı yapılan bir FDM 3D yazıcı"
    caption: "İyi bir baskı, doğru sıkılmış bir vidayla başlar."
    relative: false
---

Kapı çaldı, kurye o beklenen kutuyu bıraktı. Heyecan dorukta, biliyorum. Hemen bıçağı alıp kutuyu parçalamak, fişi takıp o meşhur gemiyi (Benchy) basmak istiyorsunuz.

**YAPMAYIN.**

Lütfen o bıçağı yavaşça yere bırakın.

3D yazıcılar, bir mikrodalga fırın gibi "fişi tak çalıştır" cihazlar değildir (Bambu Lab gibi yeni nesiller işi çok kolaylaştırsa da, temel mekanik kurallar değişmez). Yazıcının montajında yapacağınız 1 milimetrelik bir yamukluk veya gevşek bir vida, ileride "Neden bu baskı yamuk?", "Neden çizgiler var?" diye saçınızı başınızı yolmanıza sebep olur.

Ben ilk yazıcımı kurarken o kadar acele ettim ki, dikey profilleri tam gönyesinde (dik) sıkmadım. Sonuç? İlk 2 ay boyunca bastığım her kare prizma aslında hafif bir paralelkenardı. Bunu fark etmem aylarımı aldı.

Bu rehberde, kullanım kılavuzlarında detaylı anlatılmayan ama **hayati** olan montaj sırlarını vereceğim. Tornavidalar hazırsa başlıyoruz.

## Adım 1: Kutu Açılışı ve "Sakin" Kontrol

Kutuyu "kibarca" açın. İçinden çıkan köpükleri atmayın (ileride taşınırken veya servise gönderirken hayat kurtarır). Parçaları geniş bir masaya yayın. Vidaları boylarına göre ayırın.

*   **İlk Bakış:** Kayışlarda kopukluk var mı? Kablolarda ezilme var mı? Profiller düzgün mü?

## Adım 2: İskelet Montajı (Gönyesinde Kurmak)

Yazıcının dikey profillerini (Z ekseni) tabana monte ederken en kritik kural şudur: **Diklik.**
Vidaları hemen sonuna kadar sıkmayın. Önce hafifçe tutturun. Profillerin tam oturduğuna emin olduktan sonra çapraz sırayla sıkın.

{{< tip-box title="💡 Usta İpucu: Sallantı Testi" >}}
Yazıcıyı masaya koyduğunuzda, elinizle üstten hafifçe sallayın. Ayaklardan biri havada kalıyor mu? Yazıcı dans ediyor mu? Eğer ediyorsa, baskı sırasında oluşan titreşim (rezonans) tüm modellerinizi bozacaktır. Ayak vidalarını gevşetip, yazıcıyı düz zemine bastırıp tekrar sıkın.
{{< /tip-box >}}

## Adım 3: Eksantrik Somun Ayarı (Bunu Kimse Söylemez!)

Kullanım kılavuzlarında genelde minik bir not olarak geçer ama **en çok yapılan hata** buradadır.
Yazıcının hareket eden tekerleklerinin arkasında, diğerlerinden farklı görünen altıgen bir somun vardır. Buna **Eksantrik Somun** denir.

*   **Sorun:** Kafa (extruder) veya tabla elinizle dokunduğunuzda lakır lukur sallanıyorsa, baskınız kötü olur. Çok sıkıysa tekerlekler aşınır.
*   **Çözüm:** Kutudan çıkan anahtarla bu somunu yavaşça çevirin. Tekerlek profile tam öpüşmeli. **Testi şudur:** Tekerleği parmağınızla zorlayarak döndürebilmelisiniz ama tekerlek kendiliğinden boşa dönmemeli.

![Eksantrik somun ayarının yapılışını gösteren bir görsel](/images/kurulum-montaj.jpg "Sallanan bir kafa, dalgalı duvarlar demektir.")

## Adım 4: Otomatik Kalibrasyon ve Z-Offset Ayarı

Satın alma rehberimizde "Otomatik Seviyeleme (Auto-Leveling) olmayan cihaz almayın" demiştik. Sözümüzü tuttuk, şimdi işin kolay kısmındayız. Artık kağıtla, tekerlekle uğraşmak yok.

1.  Filamenti takmadan önce menüden **"Leveling"** veya **"Auto-Calibration"** seçeneğini başlatın.
2.  Yazıcı tablanın çeşitli noktalarına dokunarak kendi haritasını çıkaracak. Bırakın yapsın.
3.  **Kritik Nokta (Z-Offset):** Makine düzlüğü anlar ama "nozzle'ın tablaya ne kadar yakın olması gerektiğini" tam bilemeyebilir. Buna **Z-Offset** denir.
    *   İlk baskıyı başlatırken menüde "Z-Offset" ayarını göreceksiniz.
    *   Nozzle tablaya çok uzaksa (plastik havada kalıyorsa) değeri eksiye (-) indirin.
    *   Çok yakınsa (plastik çıkamıyor, kazıyorsa) artıya (+) çıkarın.

![Bir kişinin tabla kalibrasyonu yaparken ekran görüntüsü](/images/kurulum-kalibrasyon.jpg "Z-Offset ayarı, ilk katmanın kaderini belirler.")

## Adım 5: Filament Yükleme ve O Kritik Düğüm

Filamenti (PLA) paketten çıkarın.
*   **Kural 1:** Ucunu yan keskiyle **45 derece açıyla sivri** kesin.
*   **Kural 2:** Filamanın ucunu makaradan kaçırmayın! Eğer ucu bir kez elinizden kaçırıp makaraya dolanmasına izin verirseniz, o filament 5 saat sonraki baskının tam ortasında düğümlenir ve baskınız çöp olur.

Extruder mandalına basıp filamenti ittirin (veya menüden "Load Filament" deyin). Nozzle sıcaklığının 200°C olduğundan emin olun. Ucundan plastik akana kadar bekleyin.

![Bir kişinin filamentin ucunu 3D yazıcının extruder mekanizmasına takması](/images/kurulum-filament-yukleme.jpg "Doğru filament yüklemesi, baskının kesintisiz sürmesini sağlar.")

## Adım 6: İlk Baskı (Kutsal Benchy)

Genelde SD kartın içinde "Test Dog" veya "Owl" gibi modeller gelir. Siz gerçek bir test istiyorsanız, internetten meşhur **3DBenchy** gemisini indirin ve slicer'da standart ayarlarla dilimleyip basın.

### Gözünüzü İlk Katmandan Ayırmayın
Baskı başladığında eğilin ve nozzle'ın ucuna bakın.
*   Plastik havada mı kalıyor? -> **Z-Offset'i biraz daha düşürün.**
*   Plastik cama çok mu eziliyor, şeffaflaşıyor mu? -> **Z-Offset'i biraz artırın.**
*   Mükemmel ilk katman, hafifçe ezilmiş yassı bir çizgi gibi görünmelidir.

![İlk katmanı atılan bir baskı](/images/kurulum-ilk-katman.jpg "O ilk katmanın yapıştığını görmek, dünyanın en güzel hissidir.")

{{< success-story-box title="✨ Benim İlk 'Spagetti' Deneyimim" >}}
İlk yazıcımı kurduğumda, Z-Offset ayarını yapmadan baskıyı başlatıp odadan çıkmıştım. 1 saat sonra döndüğümde masanın üzerinde bir gemi değil, kocaman bir plastik yumağı (spagetti) vardı. O gün öğrendim ki: Otomatik seviyeleme olsa bile, **ilk katmanı gözünle görmeden odadan çıkma.**
{{< /success-story-box >}}

## Sonuç: Artık Bir "Maker"sınız

Eğer o ilk baskı tabladan, spagettiye dönüşmeden çıktıysa, derin bir nefes alabilirsiniz. En zor kısmı atlattınız. Artık o makine sizin hayal gücünüzün emrinde.

Ancak makineyi kurmak yetmez. Bu cihazlar yüksek sıcaklıklara çıkar ve hareketli parçalara sahiptir. Evinizde küçük bir fabrika kurdunuz, peki bu fabrikanın iş güvenliği ne durumda?

### Yolculuğun Bir Sonraki Durağı

Yazıcı çalışıyor ama onu gece çalıştırıp uyumak güvenli mi? Yangın riski var mı? Çocuklardan nasıl koruruz? Gel, güvenliği şansa bırakmayalım.

<div class="post-cta-box">
<h3>Sırada: 3D Yazıcı Güvenliği</h3>
<p>Termal kaçak nedir? Yazıcıyı evde nereye koymalı? Yangın ve sağlık risklerine karşı almanız gereken 5 hayati önlem.</p>
<a href="{{< ref "posts/3d-yazici-guvenligi-rehberi.md" >}}" class="cta-button">Güvenlik Rehberine Git →</a>
</div>