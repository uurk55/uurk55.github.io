---
title: "Fusion 360 Başlangıç Rehberi: Profesyonel 3D Parçalar Tasarlayın"
date: 2025-05-24T11:00:00+03:00
featured: false
draft: false
description: "Autodesk Fusion 360 ile parametrik modelleme öğrenin ve profesyonel, fonksiyonel 3D parçalar tasarlayın. Hassas ölçülerle çalışan mühendislik parçaları oluşturma rehberi."
tags: ["Fusion 360", "Parametrik Modelleme", "3D Tasarım", "Fonksiyonel Parçalar", "CAD Yazılımı", "Mühendislik Tasarımı", "Autodesk Fusion 360", "İleri Seviye", "Beceri Geliştirme ve İleri Teknikler"]
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
    image: "/images/fusion360-cover.png"
    alt: "Bir mühendisin masasında açık olan Fusion 360 yazılımı ve yanında tasarlanan hassas mekanik parça"
    caption: "Bir mühendis gibi düşünün, bir sanatçı gibi yaratın. Fusion 360'a hoş geldiniz."
    relative: false
---

**[Tinkercad]({{< ref "posts/tinkercad-baslangic-rehberi.md" >}})** ile ilk anahtarlığınızı, **[Blender]({{< ref "posts/blender-baslangic-rehberi-sculpting.md" >}})** ile ilk organik saksınızı tasarladınız. Harika! Artık dijital dünyada bir şeyler yaratabiliyorsunuz. Ama bir noktada şu sorunla karşılaştınız: Yaptığınız bir kutunun ölçüsünü sonradan 5mm değiştirmek istediğinizde, tüm tasarımı baştan yapmanız gerekti.

Profesyonel ve fonksiyonel parça tasarımının dünyasına hoş geldiniz: **Parametrik Modelleme** ve onun en erişilebilir kralı **Autodesk Fusion 360**.

> **Parametrik modelleme nedir?** En basit haliyle, 'kurallara dayalı' tasarımdır. Bir kutu çizerken ona "Genişliğin her zaman yüksekliğinin iki katı olsun" gibi bir kural koyarsınız. Yüksekliği değiştirdiğinizde, genişlik de otomatik olarak değişir. Bu, tasarımlarınızı inanılmaz esnek, hassas ve kolayca düzenlenebilir kılar.

Bu **Fusion 360 başlangıç rehberi**, sizi programın karmaşık arayüzünden korkutmadan, bu güçlü düşünce yapısına ilk adımı atmanızı sağlayacak. Bir mühendis gibi düşünmeye ve gerçekten 'çalışan' parçalar tasarlamaya hazır mısınız?

{{< tip-box title="💡 Zaman Çizelgesi (Timeline): Sizin Süper Gücünüz" >}}
Fusion 360'ın altındaki 'Zaman Çizelgesi' (Timeline), yaptığınız her işlemi kaydeder. Geri dönüp herhangi bir adımı (örneğin bir çizimin ölçüsünü) değiştirdiğinizde, tasarımınız sihirli bir şekilde otomatik olarak güncellenir. Bu özelliği aktif olarak kullanın!
{{< /tip-box >}}

### Hangi Alet Ne Zaman Kullanılır? Tasarım Felsefeleri
Bu üç program da harikadır, ancak farklı amaçlara hizmet ederler. İşte ne zaman hangisini seçeceğinize dair hızlı bir rehber:

<table class="summary-table">
    <thead>
        <tr>
            <th>Tasarım Programı</th>
            <th>Felsefesi</th>
            <th>En İyi Olduğu Alan</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><strong>Tinkercad</strong></td>
            <td>🧱 Dijital LEGO</td>
            <td>Hızlı, basit geometrik birleştirmeler ve başlangıç.</td>
        </tr>
        <tr>
            <td><strong>Blender (Sculpt Mode)</strong></td>
            <td>🎨 Dijital Heykeltıraşlık</td>
            <td>Organik, sanatsal ve karakter modelleme.</td>
        </tr>
        <tr>
            <td><strong>Fusion 360</strong></td>
            <td>⚙️ Mühendislik ve Parametreler</td>
            <td>Hassas ölçülü, fonksiyonel ve mekanik parçalar.</td>
        </tr>
    </tbody>
</table>

### Fusion 360 Arayüzünü Tanıyalım
Fusion 360'ta her şey, bir kağıda kurşun kalemle çizim yapmak gibi başlar. Bu dijital çizimlere **'Sketch' (Taslak)** diyoruz. Arayüzde şimdilik bilmeniz gereken dört ana alan var:

1.  **Sol Taraftaki Tarayıcı (Browser):** Tasarımınızın içindekiler listesi. Tüm çizimleriniz ve katı cisimleriniz burada listelenir.
2.  **Üstteki Araç Çubuğu (Toolbar):** Tüm komutlarınızın bulunduğu yer (`Sketch`, `Extrude`, `Fillet` vb.).
3.  **Ortadaki Kanvas (Canvas):** Sizin 3 boyutlu çalışma alanınız.
4.  **Alttaki Zaman Çizelgesi (Timeline):** Yaptığınız her işlemin kaydedildiği sihirli geri sarma bandı.

### İlk Projeniz: Ölçüleri Belli Bir Telefon Standı

Şimdi bu mantığı, ölçüleri hassas bir telefon standı tasarlayarak pekiştirelim.

#### Adım 1: İlk Taslağı (Sketch) Oluşturma
Her şey 2D bir çizimle başlar. Standımızın tabanını çizeceğiz.

* Üst araç çubuğundan **`Create Sketch`**'e tıklayın ve yerdeki düzlemi (mavi ve kırmızı çizgilerin kesiştiği XY düzlemi) seçin.
* Araç çubuğundan **`2-Point Rectangle`** aracını seçin. İmleci tam merkeze (orijin noktasına) getirin, bir kez tıklayın ve bir dikdörtgen çizin.
* Ölçüleri girmek için klavyeden hemen `70` yazın, `Tab` tuşuna basın, `80` yazın ve `Enter`'a basın. Çiziminiz şimdi tam olarak ölçülendirilmiş ve siyaha dönmüş olmalı.
* Sağ üstteki **`Finish Sketch`** butonuna tıklayarak 3D moda geri dönün.

#### Adım 2: Hacim Kazandırma (Extrude)
Şimdi 2D çizimimizi 3D bir katıya dönüştürelim.

* Oluşturduğunuz mavi profili seçin ve klavyeden `E` tuşuna basarak **`Extrude`** komutunu çalıştırın.
* Açılan pencerede, `Distance` (Mesafe) olarak `15` girip `OK`'a tıklayın. Artık 3 boyutlu bir katı gövdeniz var.

#### Adım 3: Yan Profili Çizme ve Kesme (Cut)
Standımızın o karakteristik eğimli şeklini vereceğiz.

* Tekrar **`Create Sketch`**'e tıklayın ve bu sefer çizim düzlemi olarak kutunuzun **dar yan yüzeyini** seçin.
* **`Line`** (Çizgi) aracıyla, kutunun altından başlayıp yukarı ve geriye doğru eğimli, telefonun yaslanacağı profili oluşturan kapalı bir şekil çizin.
* **`Finish Sketch`** ile 3D moda dönün.
* Yeni çizdiğiniz profili seçin, `E` tuşuyla **`Extrude`** komutunu tekrar çalıştırın. Oku, tüm kutuyu kesecek şekilde dışarı doğru sürükleyin. `Operation` (İşlem) kısmının otomatik olarak **`Cut` (Kes)** olarak değiştiğini göreceksiniz. `OK`'a tıklayın.

#### Adım 4: Son Dokunuşlar (Fillet) ve Dışa Aktarma
Tasarımımızı daha şık ve kullanışlı hale getirelim.

* Klavyeden `F` tuşuna basarak **`Fillet`** (Kenar Yuvarlatma) komutunu seçin. Telefonun yaslanacağı ve masaya değen keskin kenarları seçip `2mm` gibi bir değer girin.
* Modeliniz hazır! Sol taraftaki Tarayıcıdan `Bodies` klasörünün altındaki `Body1`'e sağ tıklayın, **`Save as Mesh`**'i ve format olarak **STL**'i seçip kaydedin.

## Sonuç: Artık Bir Mühendis Gibi Düşünüyorsunuz

Tebrikler! Az önce yaptığınız şey, sadece bir 3D model çizmekten çok daha fazlasıydı. Siz, **parametrik modellemenin** temel felsefesine ilk adımı attınız. Artık tasarımlarınız, kurallara göre yaşayan, kolayca değiştirilebilen ve birbiriyle mükemmel uyum içinde çalışan dinamik sistemlerdir. Bu, sizi bir probleme mühendislik çözümleri üreten bir probleme çözücüye dönüştürür.

### Yolculuğun Bir Sonraki Durağı

Harika ve fonksiyonel tasarımlar yapmayı öğrendiniz. Ancak bazen en iyi tasarımlar bile, yer çekimine karşı koymak için küçük yardımcılara ihtiyaç duyar. Karmaşık modelleri basarken başarının anahtarı nedir?

<div class="post-cta-box">
<h3>Şimdi Sırada Ne Var?</h3>
<p>En karmaşık modelleri bile sorunsuzca basmanızı sağlayacak 'Destek Yapıları'nın sırlarını öğrenin. Hangi desteği, nerede ve nasıl kullanmalısınız?</p>
<a href="{{< ref "posts/destek-yapilari-supports-rehberi.md" >}}" class="cta-button">Destek Yapıları Rehberine Git →</a>
</div>