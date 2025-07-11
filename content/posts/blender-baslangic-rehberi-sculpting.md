---
title: "Blender Başlangıç Rehberi: Heykeltıraş Gibi 3D Model Yapın"
date: 2025-05-21T12:00:00+03:00
featured: false
draft: false
description: "Blender'ın Sculpt Mode (Heykel Modu) ile organik ve sanatsal 3D modeller tasarlayın. Dijital kil topundan heykelsi objelere adım adım Blender başlangıç rehberi."
tags: ["Blender", "3D Modelleme", "Sculpting", "Heykel Modu", "Ücretsiz 3D Programı", "Organik Modelleme", "Dijital Sanat", "Blender Rehberi"]
categories: ["Tasarım", "Başlangıç Rehberi", "Beceri Geliştirme ve İleri Teknikler"]
series: ["3D Baskı Rehberleri"]
author: "uurk55"
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

Tinkercad ile dijital LEGO oynamanın keyfini çıkardınız ve kendi tasarımlarınızı yarattınız. Harika! Ama bir süre sonra fark ettiniz ki, küpleri ve silindirleri birleştirmek, aklınızdaki o organik, kıvrımlı ve sanatsal şekilleri yaratmak için her zaman yeterli değil. Bir canavarın kafasını, pürüzsüz bir heykeli veya doğadan ilham alan bir vazoyu nasıl yaparsınız?

İşte bu noktada, sizi bir 'inşaat mühendisinden' bir 'heykeltıraşa' dönüştürecek o güçlü ve tamamen ücretsiz araca merhaba deyin: **Blender**.

> Blender, Hollywood filmlerinden video oyunlarına kadar her alanda kullanılan devasa bir programdır ve ilk bakışta arayüzü sizi biraz korkutabilir. Ama endişelenmeyin! Biz bu okyanusa parmak ucundan gireceğiz ve sadece en eğlenceli ve en sezgisel özelliklerinden biri olan **Sculpt Mode (Heykel Modu)** üzerine odaklanacağız. Bu mod, önünüzde duran dijital bir kil topunu, farklı fırçalarla çekip, ittirip, düzleştirerek hayalinizdeki şekli vermenizi sağlar.

Bu **Blender başlangıç rehberi**, sizi programın tüm karmaşasından kurtarıp, doğrudan yaratıcılığın kalbine götürecek. Hadi, dijital çamurumuzu yoğurmaya başlayalım!

{{< tip-box title="💡 Sürekli Kaydetme Alışkanlığı" >}}
Blender gibi kapsamlı programlarda çalışırken düzenli olarak kaydetmek çok önemlidir (Ctrl+S). Özellikle Sculpt Mode'da, ani program kapanmaları veya hatalar karşısında ilerlemenizi kaybetmemek için bunu alışkanlık haline getirin!
{{< /tip-box >}}

### Bölüm 1: Blender'a İlk Bakış - Sadece 3 Şeyi Bilin

Maceraya başlamak için [blender.org](https://www.blender.org) adresine gidin ve programın en son sürümünü ücretsiz olarak indirin. Programı açtığınızda sizi bir hoş geldin ekranı ve ortasında meşhur bir küp karşılayacak. Şimdilik sadece üç temel navigasyon hareketini bilmeniz yeterli:

* **Farenin Orta Tekerleği (Basılı Tutarak):** Sahnenin etrafında 360 derece dönersiniz (orbit).
* **Shift + Farenin Orta Tekerleği (Basılı Tutarak):** Sahneyi kaydırırsınız (pan).
* **Farenin Orta Tekerleğini Kaydırmak:** Yakınlaşıp uzaklaşırsınız.


**Sculpt Mode'a Nasıl Geçilir?**
1.  Üst menüden `Add > Mesh > UV Sphere` seçerek sahneye bir küre ekleyin. Bu bizim dijital kilimiz olacak.
2.  Küre seçiliyken, sol üstteki `Object Mode` yazan menüye tıklayın ve **`Sculpt Mode`** seçeneğini seçin. Arayüz değişecek ve sol tarafta bir sürü fırça belirecek.

### Bölüm 2: En Temel 3 Heykel Fırçası

O uzun fırça listesinden korkmayın. Başlangıçta sadece üç tanesiyle harikalar yaratabilirsiniz. Fırça boyutunu klavyeden **'F' tuşuna basıp fareyi hareket ettirerek**, fırçanın gücünü ise **'Shift + F'** ile ayarlayabilirsiniz.

1.  **Draw / Draw Sharp Fırçası (Kil Ekle/Çıkar):** Ana fırçanız. Yüzeye kil ekleyerek **yükseltiler** oluşturur. **Ctrl** tuşuna basılı tutarsanız tam tersini yapar ve **oyuklar** açar.
2.  **Smooth (Düzleştir) Fırçası (Zımpara Kağıdınız):** Yüzeydeki istenmeyen pürüzleri ve topaklanmaları sihirli bir şekilde zımparalar ve pürüzsüzleştirir. En çok kullanacağınız yardımcınızdır.
3.  **Inflate/Blob (Şişir/Damla) Fırçası (Hacim Kazandırma):** Dokunduğu yeri bir balon gibi şişirir. Bir alana genel bir hacim eklemek için kullanılır.

### Bölüm 3: İlk Organik Proje - Basit Bir Heykelsi Saksı Yapımı

Şimdi bu fırçalarla gerçek bir şey üretelim: Modern ve heykelsi görünümlü bir sukulent saksısı.

**Adım 1: Temel Formu Oluşturma**
Sahneye bir küre ekleyip Sculpt Mode'a geçin. Fırçanızı `F` ile büyütün ve `Grab` (Tut) fırçasını seçin. Kürenin üst kısmını tutup yavaşça yukarı çekerek bir vazo şekli verin. Altını da tutup hafifçe düzleştirerek bir taban oluşturun.

**Adım 2: Yüzeye Doku Kazandırma**
`Draw Sharp` fırçasını seçin. Gücünü biraz azaltın. Saksının yan yüzeylerinde, `Ctrl` tuşuna basılı tutarak rastgele, dikey oluklar ve girintiler oluşturun. Ardından, bazı yerlere de `Inflate` fırçasıyla hafifçe dokunarak küçük şişkinlikler yaratın.

**Adım 3: Yüzeyi Pürüzsüzleştirme**
`Smooth` (Düzleştir) fırçasını seçin, gücünü çok düşürün ve fırçayı yüzeyde nazikçe gezdirerek keskin kenarları yumuşatın ve daha doğal bir görünüm kazandırın.

**Adım 4: İçini Boşaltma ve Baskıya Hazırlama**
1.  Sol üst menüden tekrar `Object Mode`'a geri dönün.
2.  Sağdaki özellikler panelinden ingiliz anahtarı ikonuna (Modifier Properties) tıklayın.
3.  `Add Modifier`'a tıklayın ve listeden `Solidify` (Katılaştır) seçeneğini seçin.
4.  Açılan menüde `Thickness` (Kalınlık) değerini `3mm` veya `4mm` gibi bir değere getirin.
5.  Modifier'ın yanındaki küçük ok işaretine tıklayıp **`Apply`** (Uygula) deyin.

Tebrikler! Üst menüden `File > Export > Stl (.stl)` seçeneğini seçerek modelinizi kaydedebilir ve dilimleyici programınıza atabilirsiniz.

### Sonuç: Yaratıcılığınızın Kilidi Açıldı

Az önce yaptığınız şey, sadece bir saksı tasarlamak değildi. Tinkercad'in geometrik dünyasından, Blender'ın organik ve sanatsal dünyasına başarılı bir geçiş yaptınız. Artık sadece küpleri birleştirmekle kalmıyor, dijital bir kile şekil verebiliyorsunuz.

Bu, 3D modelleme yolculuğunuzda yepyeni bir kapı araladı. Unutmayın, Blender devasa bir program ve biz bugün sadece bir fırça darbesi attık. Gelecekteki rehberlerimizde, bu güçlü aracın diğer sırlarını da keşfetmeye devam edeceğiz. Artık dijital heykeltıraşlığa ilk adımı attığınıza göre, belki de bir mühendis gibi düşünmenin zamanı gelmiştir. Ölçüleri hassas, birbiriyle mükemmel uyumlu ve kolayca değiştirilebilen fonksiyonel parçalar tasarlamak isterseniz, bir sonraki durağınız **[Fusion 360 Başlangıç Rehberimizdir]({{< ref "posts/fusion-360-baslangic-rehberi.md" >}})**.

{{< success-story-box title="✨ Başarı Hikayesi: Dijital Kilden Sanata" >}}
Deniz, Tinkercad'den sonra Blender'ın arayüzünü görünce biraz gözü korkmuştu. Ama Sculpt Mode rehberimizdeki temel fırçaları kullanarak, sevdiği bir video oyunu karakterinin minyatür büstünü yonttu. İlk denemesi mükemmel olmasa da, çıkan sonucu görünce heveslendi ve şimdi kendi tasarladığı figürleri online platformlarda satıyor. Unutmayın, dijital heykeltıraşlık düşündüğünüzden daha kolay!
{{< /success-story-box >}}

Ama şimdilik, kendi ellerinizle 'yonttuğunuz' o ilk organik modelin baskısını almanın tadını çıkarın!