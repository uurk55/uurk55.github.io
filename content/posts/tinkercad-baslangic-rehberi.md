---
title: "Tinkercad Rehberi: Sıfırdan Kendi 3D Modelinizi Yapın (En Kolay Yol)"
date: 2025-08-19T11:00:00+03:00
featured: true
draft: false
description: "Mühendis olmanıza gerek yok! Tinkercad ile dijital LEGO oynar gibi kendi 3D modelinizi tasarlayın. 10 dakikada isminize özel anahtarlık yapımı ve Uğur Kapancı'nın tasarım ipuçları."
tags: ["Tinkercad", "3D Modelleme", "Ücretsiz 3D Programı", "STL Yapma", "Başlangıç 3D Tasarım", "Online 3D Tasarım", "Kolay 3D Modelleme", "Tasarım Eğitimi"]
categories: ["Tasarım"]
faz: ["Faz 2"]
series: ["3D Baskı Rehberleri"]
author: "Uğur Kapancı"
showToc: true
TocOpen: true
comments: true
ShowReadingTime: true
ShowPostNavLinks: true
cover:
    image: "/images/tinkercad-cover.jpg"
    alt: "Bir bilgisayar ekranında Tinkercad arayüzü ve basit geometrik şekiller"
    caption: "3D modelleme zor olmak zorunda değil. Yaratıcılığınızın kilidini açma zamanı!"
    relative: false
---

Şimdiye kadar hep başkalarının tasarladığı modelleri bastınız. Thingiverse'ten indirdiniz, Printables'tan buldunuz. Peki ya aklınızdaki o mükemmel telefon standını, isminizin yazdığı o anahtarlığı veya mutfaktaki o küçük ama dahiyane aparatı kendiniz yapsaydınız?

Çoğu insan "3D modelleme" kelimesini duyduğunda, aklına karmaşık mühendislik programları, siyah ekranlar ve kodlar gelir. "Ben yapamam" der ve kaçar.

Size bir sır vereyim: **Bunların hiçbirine gerek yok.**

Karşınızda **Autodesk Tinkercad**: 3D modellemenin en basit, en eğlenceli ve en erişilebilir hali.

> Tinkercad'i, **dijital LEGO oynamak** gibi düşünebilirsiniz. Çizim yapmazsınız; hazır küpleri, silindirleri, küreleri birleştirerek veya birbirinden çıkarerek şekil verirsiniz.

Bu rehberde, hiçbir ön bilgiye sahip olmadan, 10 dakika içinde 3D yazıcınızda basmaya hazır **ilk özgün modelinizi** yaratacağız.

{{< tip-box title="💡 Ücretsiz ve Tarayıcı Tabanlı" >}}
Tinkercad tamamen ücretsizdir ve bilgisayarınıza bir şey kurmanıza gerek yoktur. Sadece internet tarayıcınızdan (Chrome, Edge vb.) girip çalışırsınız.
{{< /tip-box >}}

## Tinkercad Dünyasına İlk Adımlar: Oyun Alanını Tanıyalım

Maceraya başlamak için [Tinkercad.com](https://www.tinkercad.com) adresine gidin ve ücretsiz bir hesap oluşturun. "Yeni Tasarım Oluştur" butonuna tıkladığınızda, sizi meşhur mavi ızgaralı "Çalışma Düzlemi" karşılayacak.

Panik yapmayın! Ekranda bilmeniz gereken sadece 3 temel alan var:

1.  **Sağdaki Şekiller Paneli (Kutu):** Sizin dijital LEGO kutunuz. Küpler, silindirler, metinler burada. Buradan bir şekli tutup Çalışma Düzlemi'ne sürüklersiniz.
2.  **Ortadaki Çalışma Düzlemi (Masa):** Sizin oyun alanınız, 3D yazıcınızın sanal tablası.
3.  **Sol Üstteki Küp (Kamera):** Bakış açınızı değiştirir. Farenin sağ tuşuna basılı tutarak modeli döndürebilirsiniz.

## İlk Projeniz: İsminize Özel Anahtarlık Yapalım

Teori yeterli, pratiğe geçelim. Üzerinde isminizin (veya sevdiğinizin isminin) yazdığı basit ama şık bir anahtarlık yapacağız. Bu proje, Tinkercad'in iki temel mantığını size öğretecek: **Birleştirme (Katı)** ve **Çıkarma (Delik).**

### Adım 1: Gövdeyi Oluşturun
Sağdaki panelden kırmızı **'Kutu'** (Box) şeklini Çalışma Düzlemi'ne sürükleyin.
*   Şeklin köşelerindeki beyaz kareleri çekerek onu yassı bir dikdörtgene dönüştürün (Anahtarlık tabanı olacak).
*   Üstündeki beyaz kareyi aşağı çekerek kalınlığını yaklaşık **4mm** yapın.

### Adım 2: İsminizi Yazın
Panelden **'Metin' (Text)** şeklini alın ve düzleme sürükleyin.
*   Sağda açılan pencerede 'Text' yazan yere isminizi yazın.
*   Rengini değiştirebilirsiniz ama asıl numara şu: Metni, tabanın üzerine sürükleyip oturtun.

### Adım 3: Delik Açma (Sihirli Kısım)
Anahtarlık halkasının geçeceği deliği yapalım.
*   Panelden **'Silindir' (Cylinder)** şeklini alın ama dikkat: **Gri çizgili (şeffaf)** olanı alın. Bu "Delik" (Hole) demektir.
*   Bu silindiri küçültüp anahtarlığın köşesine yerleştirin.

### Adım 4: Gruplama (Birleştirme)
Şu an masada 3 ayrı parça var: Taban, Yazı ve Delik. Bunları tek parça yapmalıyız.
*   Farenizle tüm şekilleri içine alacak bir kutu çizin (veya `Ctrl+A` yapın).
*   Sağ üst köşedeki **'Grupla' (Group)** butonuna (veya `Ctrl+G`) basın.

**BOOM!** ✨
Yazı tabanla birleşti, delik silindiri ise tabanı oyup kayboldu. İşte Tinkercad'in mantığı bu kadar basittir: **Katı ekle, delik çıkar.**

### Adım 5: İndir ve Bas
Tebrikler! Sağ üst köşedeki **'Dışa Aktar' (Export)** butonuna tıklayın ve **.STL** formatını seçerek dosyanızı indirin. Artık bu dosyayı Slicer'a atıp basabilirsiniz.

{{< success-story-box title="✨ Kendi Anım: O İlk Yamuk Anahtarlık" >}}
Tinkercad ile ilk yaptığım tasarım, eşimin ismi yazılı bir anahtarlıktı. Delik yerini yanlış ayarlamışım, basınca halka sığmadı. Matkapla delmek zorunda kaldım ve çatlattım. Ama o yamuk, çatlak anahtarlık benim için dünyanın en değerli parçasıydı. Çünkü onu **ben yapmıştım.** O hissi hiçbir hazır model veremez.
{{< /success-story-box >}}

## Sonuç: Yaratıcılığınızın Kilidi Açıldı

Az önce yaptığınız şey, sadece basit bir anahtarlık tasarlamak değildi. 3D modellemenin temel mantığını öğrendiniz: **Geometrik şekilleri birleştir ve çıkar.**

Artık masanızdaki kırık bir parçayı ölçüp, Tinkercad'de silindir ve kutularla aynısını yapıp basabilirsiniz. Özgürlük budur.

Ancak... Tinkercad köşeli ve geometrik şekiller için harika olsa da, bir insan yüzü, bir ejderha veya organik kıvrımları olan sanatsal bir eser yapmak istediğinizde yetersiz kalabilir.

### Yolculuğun Bir Sonraki Durağı

Geometrik şekiller buraya kadar. Şimdi dijital kili elimize alma ve "heykeltıraş" olma vakti. Ücretsiz ve profesyonel Blender dünyasına adım atıyoruz.

<div class="post-cta-box">
<h3>Sırada: Blender ile Organik Tasarım</h3>
<p>Tinkercad'in yetmediği yerde Blender başlar. Dijital heykel (sculpting) sanatı ve organik modelleme rehberi.</p>
<a href="{{< ref "posts/blender-baslangic-rehberi-sculpting.md" >}}" class="cta-button">Blender Rehberine Git →</a>
</div>