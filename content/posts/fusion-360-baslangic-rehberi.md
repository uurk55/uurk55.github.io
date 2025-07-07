---
title: "Fusion 360 Başlangıç Rehberi: Profesyonel 3D Parçalar Tasarlayın"
date: 2025-05-24T11:00:00+03:00
draft: false
cover:
    image: "/images/fusion360-cover.png"
    alt: "Bir mühendisin masasında açık olan Fusion 360 yazılımı ve yanında tasarlanan hassas mekanik parça"
    caption: "Bir mühendis gibi düşünün, bir sanatçı gibi yaratın. Fusion 360'a hoş geldiniz."
    relative: false
categories: ["Tasarım", "İleri Seviye"]
tags: ["fusion 360", "parametrik modelleme", "3d tasarım", "fonksiyonel parçalar", "cad"]
comments: true
---

Tinkercad ile ilk anahtarlığınızı, Blender ile ilk organik saksınızı tasarladınız. Harika! Ama bir noktada şu sorunla karşılaştınız: Yaptığınız bir kutunun ölçüsünü sonradan 5mm değiştirmek istediğinizde, tüm tasarımı baştan yapmanız gerekti. İşte bu, 'doğrudan modelleme'nin sınırıdır.

Profesyonel ve fonksiyonel parça tasarımının dünyasına hoş geldiniz: **Parametrik Modelleme** ve onun en erişilebilir kralı **Autodesk Fusion 360**.

**Parametrik modelleme nedir?** En basit haliyle, 'kurallara dayalı' tasarımdır. Bir kutu çizerken ona "Genişliğin her zaman yüksekliğinin iki katı olsun" gibi bir kural koyarsınız. Yüksekliği değiştirdiğinizde, genişlik de otomatik olarak değişir. Bu, tasarımlarınızı inanılmaz esnek, hassas ve kolayca düzenlenebilir kılar.

Bu **Fusion 360 başlangıç rehberi**, sizi programın karmaşık arayüzünden korkutmadan, bu güçlü düşünce yapısına ilk adımı atmanızı sağlayacak. Bir mühendis gibi düşünmeye ve gerçekten 'çalışan' parçalar tasarlamaya hazır mısınız?

### Bölüm 1: Fusion 360'ın Temel Mantığı: Sketch'ten 3D'ye

Fusion 360'ta her şey, bir kağıda kurşun kalemle çizim yapmak gibi başlar. Bu dijital çizimlere **'Sketch' (Taslak)** diyoruz. Temel iş akışı sadece iki adımdır:

1.  **Sketch Oluştur (2D Çizim):** Önce, objenin tabanını 2 boyutlu bir düzlemde çizersiniz.
2.  **Hacim Kazandır (3D İşlem):** Sonra, bu çizime **'Extrude' (Yükseltme)** gibi bir komutla kalınlık vererek 3 boyutlu bir katıya dönüştürürsünüz.

![Fusion 360'ta bir 2D karenin çizildiği (Sketch) ve ardından Extrude komutuyla bir 3D küpe dönüştürüldüğü iki aşamalı bir diyagram](/images/fusion360-sketch-extrude.png)

Arayüzde şimdilik bilmeniz gereken üç alan var: **Sol taraftaki Tarayıcı** (tasarımınızın içindekiler listesi), **üstteki Araç Çubuğu** (komutlarınız) ve **alttaki Zaman Çizelgesi** (yaptığınız her işlemin kaydedildiği sihirli geri sarma bandı).

### Bölüm 2: İlk Proje - Ölçüleri Belli Bir Telefon Standı

Şimdi bu mantığı, ölçüleri hassas bir telefon standı tasarlayarak pekiştirelim.

#### Adım 1: İlk Sketch'i Oluşturma
Üst araç çubuğundan **`Create Sketch`**'e tıklayın ve yerdeki düzlemi (XY plane) seçin. **`2-Point Rectangle`** aracını seçip merkezden başlayarak bir dikdörtgen çizin. Ölçüleri girmek için hemen `70mm` yazın, `Tab` tuşuna basın, `80mm` yazın ve `Enter`'a basın. **`Finish Sketch`** diyerek 3D moda geri dönün.

![Fusion 360'ta bir dikdörtgen çizildiği ve ölçülerinin (70mm x 80mm) girildiği anı gösteren bir ekran görüntüsü](/images/fusion360-ilk-sketch.png)

#### Adım 2: Hacim Kazandırma (Extrude)
Oluşturduğunuz profili seçin ve klavyeden `E` tuşuna basarak **`Extrude`** komutunu çalıştırın. Kalınlık olarak `15mm` girip `OK`'a tıklayın. Artık 3 boyutlu bir katı gövdeniz var.

#### Adım 3: Telefonun Yaslanacağı Yüzeyi Çizme
Tekrar **`Create Sketch`**'e tıklayın ve bu sefer çizim düzlemi olarak kutunuzun **yan yüzeyini** seçin. **`Line`** aracıyla, kutunun altından başlayıp yukarı ve geriye doğru eğimli, standın yan profilini oluşturan kapalı bir şekil çizin. `Finish Sketch` ile 3D moda dönün.

![Fusion 360'ta kutunun yan yüzeyine, standın yan profilini oluşturan eğimli bir çizimin yapıldığı an](/images/fusion360-yan-sketch.png)

#### Adım 4: Profili Keserek Şekil Verme
Yeni çizdiğiniz profili seçin, `E` tuşuyla **`Extrude`** komutunu tekrar çalıştırın. Oku, tüm kutuyu kesecek şekilde dışarı doğru sürükleyin. `Operation` (İşlem) kısmının otomatik olarak **`Cut` (Kes)** olarak değiştiğini göreceksiniz. `OK`'a tıklayın.

![Fusion 360'ta yan profilin seçilip, Extrude-Cut komutuyla katı gövdeden çıkarıldığı ve standın son şeklinin ortaya çıktığı an](/images/fusion360-cut.png)

#### Adım 5: Son Dokunuşlar (Fillet) ve Dışa Aktarma
Tasarımınızın keskin kenarlarını daha şık hale getirmek için, **`Fillet`** (Kenar Yuvarlatma) komutunu seçin. Yuvarlatmak istediğiniz kenarları seçip `2mm` gibi bir değer girin. Modeliniz hazır! Sol taraftaki Tarayıcıdan `Bodies` klasörünün altındaki `Body1`'e sağ tıklayın, **`Save as Mesh`**'i ve format olarak **STL**'i seçip kaydedin.

### Sonuç: Artık Bir Mühendis Gibi Düşünüyorsunuz

Tebrikler! Az önce yaptığınız şey, sadece bir 3D model çizmekten çok daha fazlasıydı. Siz, **parametrik modellemenin** temel felsefesine ilk adımı attınız. Artık tasarımlarınız, kurallara göre yaşayan, kolayca değiştirilebilen ve birbiriyle mükemmel uyum içinde çalışan dinamik sistemlerdir.

Unutmayın, Fusion 360'ın gücü, alttaki **zaman çizelgesinde (timeline)** gizlidir. Yaptığınız her adımı geri dönüp düzenleyebilme özgürlüğü, sizi bir probleme mühendislik çözümleri üreten bir probleme çözücüye dönüştürür.

Peki, bu harika tasarımları yapıp bastıktan sonra, onları pürüzlü ve katman çizgileriyle mi bırakacağız? Elbette hayır! Bir sonraki rehberimizde, **"Baskılarınızı Profesyonel Gösterecek 5 Yüzey İşleme Tekniği"** ile zımparalamadan boyamaya, baskılarınıza o "satışa hazır" görünümü nasıl vereceğinizi anlatacağız. Takipte kalın!