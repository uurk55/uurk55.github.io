---
title: "Fusion 360 Başlangıç Rehberi: Profesyonel 3D Parçalar Tasarlayın"
date: 2025-08-26T11:00:00+03:00
featured: false
draft: false
description: "Tinkercad yetmediğinde ne yapacaksınız? Vida delikleri, hassas kapaklar ve parametrik tasarım. Uğur Kapancı'nın Fusion 360'a 'korkmadan' başlama rehberi."
tags: ["Fusion 360", "Parametrik Modelleme", "3D Tasarım", "Fonksiyonel Parçalar", "CAD Yazılımı", "Mühendislik Tasarımı", "Autodesk Fusion 360", "İleri Seviye", "Tasarım Eğitimi"]
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

**[Tinkercad]({{< ref "posts/tinkercad-baslangic-rehberi.md" >}})** ile ilk anahtarlığınızı, **[Blender]({{< ref "posts/blender-baslangic-rehberi-sculpting.md" >}})** ile ilk heykeli tasarladınız. Harika! Artık dijital dünyada bir şeyler yaratabiliyorsunuz.

Ama bir noktada şu sorunla karşılaştınız:
*"Tasarladığım kutunun kapağı tam oturmuyor"* veya *"Vida deliğinin çapını 3mm'den 4mm'ye çıkarmak için her şeyi baştan çizmem lazım."*

Profesyonel dünyanın kapısına hoş geldiniz. Karşınızda: **Parametrik Modelleme** ve onun kralı **Autodesk Fusion 360**.

> **Parametrik modelleme nedir?**
> En basit haliyle, 'akıllı' tasarımdır. Fusion 360'a şunu diyebilirsiniz: "Bu deliğin çapı ne olursa olsun, kenara uzaklığı hep 5mm kalsın."
> Sonra deliği büyüttüğünüzde, program her şeyi otomatik düzeltir.

Bu rehberde, o karmaşık arayüzden korkmadan, basit ama milimetrik hassasiyette bir parça tasarlayacağız.

{{< tip-box title="💡 Zaman Çizelgesi (Timeline): Sizin Süper Gücünüz" >}}
Fusion 360'ın altındaki 'Timeline', yaptığınız her işlemi kaydeder. Geri dönüp "Adım 1'deki kutu 50mm değil 60mm olsun" dediğinizde, sonraki tüm adımlar otomatik güncellenir. Bu, tasarımın zaman makinesidir.
{{< /tip-box >}}

### Hangi Alet Ne Zaman Kullanılır?

Kafanız karışmasın, her programın uzmanlık alanı farklıdır:

| Program | Felsefesi | En İyi Olduğu Alan |
| :--- | :--- | :--- |
| **Tinkercad** | 🧱 Dijital LEGO | Basit, geometrik ve hızlı başlangıç. |
| **Blender** | 🎨 Dijital Kil | Karakter, heykel ve organik yüzeyler. |
| **Fusion 360** | ⚙️ Dijital Mühendislik | Kutu, kapak, dişli, vida ve montaj. |

### Fusion 360'a İlk Bakış

Fusion 360'ta her şey, bir kağıda teknik çizim yapmakla başlar.
1.  **Sketch (Eskiz):** Kağıda 2 boyutlu çizimi yaparsınız.
2.  **Extrude (Yükseltme):** O çizimi çekip uzatarak 3 boyutlu katı (Body) yaparsınız.

### İlk Projeniz: Hassas Ölçülü Telefon Standı

Lafı uzatmadan, masanıza koyabileceğiniz, açısı ve ölçüsü belli bir stand yapalım.

#### Adım 1: Kağıdı Koyun (Create Sketch)
*   Sol üstten **`Create Sketch`**'e tıklayın.
*   Program "Hangi düzleme çizeceksin?" diye sorar. Yerdeki düzlemi (Alt tabanı) seçin.

#### Adım 2: Çizin ve Ölçün (Rectangle & Dimension)
*   **`2-Point Rectangle`** (Kare) aracını alın. Merkeze tıklayıp rastgele bir kare çizin.
*   Şimdi sihir geliyor: Klavyeden **`D`** tuşuna basın (Dimension/Ölçü).
*   Kenarlara tıklayıp ölçü girin: Genişlik **70mm**, Derinlik **80mm**. Çizgiler siyah olduysa (Fully Constrained), ölçüler kilitlendi demektir.
*   **`Finish Sketch`** diyerek çizimi bitirin.

#### Adım 3: Hacim Verin (Extrude)
*   Mavi profili seçin ve **`E`** tuşuna basın (Extrude).
*   Ok işaretini yukarı çekin veya **15mm** yazın. `Enter`. Artık bir takozunuz var.

#### Adım 4: Yan Profili Kesme (Cut)
Standın eğimli durması lazım.
*   Takozun **yan yüzeyine** tıklayın ve tekrar **`Create Sketch`** deyin.
*   **`Line`** (Çizgi) aracıyla (`L` tuşu), takozun içinden geçecek şekilde bir üçgen profil çizin.
*   **`Finish Sketch`** deyin.
*   Çizdiğiniz üçgeni seçip **`E`** (Extrude) yapın. Bu sefer oku takozun içine doğru itin. Program otomatik olarak "Kırmızı" yanacak, yani **`Cut` (Kes)** işlemi yapacak.

#### Adım 5: Yumuşatın (Fillet)
Keskin köşeler ele batar.
*   Klavyeden **`F`** tuşuna basın (Fillet).
*   Sivri kenarları seçin ve **2mm** yazın. Hepsi yumuşacık oldu.

#### Adım 6: Dışa Aktar (STL/3MF)
*   Soldaki menüden (Browser), `Bodies` klasörünü açın.
*   `Body1`'e sağ tıklayın -> **`Save as Mesh`**. Formatı **STL** (veya daha modern olan **3MF**) seçin ve kaydedin.

---

## Sonuç: Artık Bir Mühendis Gibi Düşünüyorsunuz

Tebrikler! Az önce rastgele bir çizim yapmadınız. "70mm olsun" dediniz ve o 70mm oldu.
Fusion 360'ın gücü budur: **Kontrol.**

Artık 3 temel silahınız var:
1.  **Tinkercad** ile hızlı fikirler.
2.  **Blender** ile sanatsal heykeller.
3.  **Fusion 360** ile teknik parçalar.

Peki bu yetenekleri nasıl paraya çevirebilirsiniz? İnsanlar hangi modelleri satın alır? "Güzel" bir model ile "Satılabilir" bir model arasındaki fark nedir?

### Yolculuğun Bir Sonraki Durağı

Çizmeyi öğrendik. Şimdi "ne çizersem satılır?" sorusuna cevap bulma vakti. Tasarımın estetik ve ticari tarafını konuşacağız.

<div class="post-cta-box">
<h3>Sırada: Satılabilir 3D Model Tasarımı</h3>
<p>Her model satılmaz. İnsanların para ödediği tasarımların ortak özellikleri nelerdir? Estetik ve fonksiyonu birleştiren tasarım sırları.</p>
<a href="{{< ref "posts/satilabilir-3d-model-tasarimi.md" >}}" class="cta-button">Satılabilir Tasarım Rehberine Git →</a>
</div>