---
title: "Blender Başlangıç Rehberi: Heykeltıraş Gibi 3D Model Yapın"
date: 2025-05-21T12:00:00+03:00
featured: false
draft: false
description: "Blender'ın Sculpt Mode (Heykel Modu) ile organik ve sanatsal 3D modeller tasarlayın. Dijital kil topundan heykelsi objelere adım adım Blender başlangıç rehberi."
tags: ["Blender", "3D Modelleme", "Sculpting", "Heykel Modu", "Ücretsiz 3D Programı", "Organik Modelleme", "Dijital Sanat", "Blender Rehberi", "Başlangıç Rehberi", "Beceri Geliştirme ve İleri Teknikler"]
categories: ["Tasarım"]
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
    image: "/images/blender-cover.jpg"
    alt: "Bir el, dijital bir kil topunu Blender arayüzünde şekillendiriyor"
    caption: "Kalıpları kırın, yaratıcılığınızı bir heykeltıraş gibi serbest bırakın."
    relative: false
---

**[Tinkercad Rehberimizle]({{< ref "posts/tinkercad-baslangic-rehberi.md" >}})** geometrik şekillerle harika tasarımlar yaptınız. Ama bir süre sonra fark ettiniz ki, küpleri ve silindirleri birleştirmek, aklınızdaki o organik, kıvrımlı ve sanatsal şekilleri yaratmak için her zaman yeterli değil. Bir canavarın kafasını, pürüzsüz bir heykeli veya doğadan ilham alan bir vazoyu nasıl yaparsınız?

İşte bu noktada, sizi bir 'inşaat mühendisinden' bir 'heykeltıraşa' dönüştürecek o güçlü ve tamamen ücretsiz araca merhaba deyin: **Blender**.

> Blender, Hollywood filmlerinden video oyunlarına kadar her alanda kullanılan devasa bir programdır ve ilk bakışta arayüzü sizi biraz korkutabilir. Ama endişelenmeyin! Biz bu okyanusa parmak ucundan gireceğiz ve sadece en eğlenceli ve en sezgisel özelliklerinden biri olan **Sculpt Mode (Heykel Modu)** üzerine odaklanacağız. Bu mod, önünüzde duran dijital bir kil topunu, farklı fırçalarla şekillendirerek hayalinizdeki objeyi yaratmanızı sağlar.

Bu **Blender başlangıç rehberi**, sizi programın tüm karmaşasından kurtarıp, doğrudan yaratıcılığın kalbine götürecek.

{{< tip-box title="💡 Sürekli Kaydetme Alışkanlığı (Ctrl+S)" >}}
Blender gibi kapsamlı programlarda çalışırken düzenli olarak kaydetmek çok önemlidir. Özellikle Sculpt Mode'da, ani program kapanmaları veya hatalar karşısında ilerlemenizi kaybetmemek için bunu bir refleks haline getirin!
{{< /tip-box >}}

### Atölyenizi Hazırlayın: Blender Arayüzü ve Simetri

Maceraya başlamak için [blender.org](https://www.blender.org) adresine gidin ve programın en son sürümünü ücretsiz olarak indirin. Programı açtığınızda ortadaki küp seçiliyken `X` tuşuna basıp silin ve üst menüden `Add > Mesh > UV Sphere` seçerek sahneye pürüzsüz bir küre ekleyin. Bu bizim dijital kilimiz olacak.

Küre seçiliyken, sol üstteki `Object Mode` yazan menüye tıklayın ve **`Sculpt Mode`** seçeneğini seçin. Arayüz değişecek ve sol tarafta bir sürü fırça belirecek.

Heykeltıraşlığın en büyük sırlarından biri **simetridir**. Sağ tarafta yaptığınız bir hareketin, sol tarafta da ayna gibi yansımasını sağlamak için, sağ üstteki `Symmetry` menüsünden **`X`** harfinin seçili olduğundan emin olun. Artık modelinizin üzerinde iki tane imleç göreceksiniz.

### Sanatçının Alet Çantası: Başlangıç İçin 5 Temel Fırça

O uzun fırça listesinden korkmayın. Başlangıçta sadece bu beş tanesiyle harikalar yaratabilirsiniz. Unutmayın: Fırça boyutunu **'F'** ile, gücünü ise **'Shift + F'** ile ayarlayabilirsiniz.

1.  **Grab (Tut) Fırçası:** Modelinizin ana silüetini oluşturmak için kullanılır. Kilin büyük bir parçasını tutup çekiştirmenizi sağlar.
2.  **Draw Sharp Fırçası (Keski):** Keskin hatlar ve oyuklar oluşturur. **Ctrl** tuşuna basılı tutarsanız tam tersini yapar ve sivri çıkıntılar yaratır.
3.  **Inflate (Şişir) Fırçası:** Dokunduğu yeri bir balon gibi şişirir. Bir alana genel bir hacim eklemek için kullanılır.
4.  **Crease (Kırışıklık) Fırçası:** `Draw Sharp` fırçasının daha ince ve zarif versiyonudur. İnce çizgiler ve keskin kenarlar oluşturmak için idealdir.
5.  **Smooth (Düzleştir) Fırçası:** En iyi dostunuz. Yüzeydeki istenmeyen pürüzleri ve topaklanmaları sihirli bir şekilde zımparalar ve pürüzsüzleştirir.

### İlk Eseriniz: Adım Adım Sevimli Bir Mantar Yontmak

Şimdi bu fırçalarla sevimli ve stilize bir mantar heykeli yapalım.

**Adım 1: Ana Formu Oluşturma**
* Sahneye bir küre ekleyip `Sculpt Mode`'a geçin ve `X` simetrisini açın.
* **`Grab`** fırçasını seçin ve `F` ile oldukça büyütün. Kürenin alt kısmını tutup yavaşça aşağı çekerek mantarın gövdesini (sapını) oluşturun. Üst kısım şapka olarak kalacak.

**Adım 2: Şapkayı ve Gövdeyi Şekillendirme**
* **`Inflate`** fırçasını seçin. Mantarın şapkasının alt kısımlarına ve ortasına dokunarak daha hacimli ve yuvarlak bir görünüm verin.
* Tekrar **`Grab`** fırçasına geçin. Bu sefer daha küçük bir fırça boyutuyla, şapkanın kenarlarını hafifçe aşağı doğru çekiştirerek o klasik mantar şapkası eğimini verin.

**Adım 3: Detay Ekleme (İşin Zevkli Kısmı!)**
* **`Crease`** fırçasını seçin. `Shift+F` ile gücünü biraz azaltın. Mantarın şapkasının altına gelin ve `Ctrl` tuşuna basılı tutarak, merkezden dışarıya doğru çizgiler çekerek mantarın lamellerini (altındaki çizgileri) oluşturun.
* **`Draw Sharp`** fırçasıyla, mantarın gövdesine birkaç ince oyuk ekleyerek doku kazandırın.

**Adım 4: Son Dokunuşlar ve Baskıya Hazırlık**
* **`Smooth`** fırçasını seçin, gücünü çok düşürün ve fırçayı modelin yüzeyinde nazikçe gezdirerek çok keskin olan yerleri yumuşatın ve daha doğal bir görünüm kazandırın.
* `Object Mode`'a geri dönün. Sağdaki ingiliz anahtarı menüsünden **`Solidify`** modifier'ını ekleyin ve `Thickness` (Kalınlık) değerini en az `2mm` yapıp `Apply` deyin.
* Üst menüden `File > Export > Stl (.stl)` ile modelinizi kaydedin!

{{< success-story-box title="✨ Dijital Kilden Sanata" >}}
Deniz, Tinkercad'den sonra Blender'ın arayüzünü görünce biraz gözü korkmuştu. Ama Sculpt Mode rehberimizdeki temel fırçaları kullanarak, sevdiği bir video oyunu karakterinin minyatür büstünü yonttu. İlk denemesi mükemmel olmasa da, çıkan sonucu görünce heveslendi ve şimdi kendi tasarladığı figürleri online platformlarda satıyor. Unutmayın, dijital heykeltıraşlık düşündüğünüzden daha kolay!
{{< /success-story-box >}}

## Sonuç: Yaratıcılığınızda Sınırları Kaldırın

Az önce yaptığınız şey, sadece sevimli bir mantar tasarlamak değildi. Tinkercad'in geometrik dünyasından, Blender'ın organik ve sanatsal dünyasına başarılı bir geçiş yaptınız. Artık sadece küpleri birleştirmekle kalmıyor, dijital bir kile şekil verebiliyorsunuz.

### Yolculuğun Bir Sonraki Durağı

Artık hem geometrik (Tinkercad) hem de sanatsal (Blender) modelleme hakkında temel bir bilgiye sahipsiniz. Peki ya bir mühendis gibi düşünmenin zamanı geldiyse?

<div class="post-cta-box">
<h3>Şimdi Sırada Ne Var?</h3>
<p>Sanatsal özgürlükten, milimetrik hassasiyete geçiş yapın. Bir sonraki adımınız, profesyoneller gibi fonksiyonel parçalar tasarlamak!</p>
<a href="{{< ref "posts/fusion-360-baslangic-rehberi.md" >}}" class="cta-button">Fusion 360 ile Tasarıma Başla →</a>
</div>