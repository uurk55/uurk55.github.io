---
title: "Blender Başlangıç Rehberi: Heykeltıraş Gibi 3D Model Yapın"
date: 2025-08-22T10:00:00+03:00
featured: false
draft: false
description: "Tinkercad yetmiyor mu? Blender'ın 'Sculpt Mode'u ile dijital kili yoğurarak organik ve sanatsal modeller yapmayı öğrenin. Uğur Kapancı'nın 10 dakikada mantar yapım rehberi."
tags: ["Blender", "3D Modelleme", "Sculpting", "Heykel Modu", "Ücretsiz 3D Programı", "Organik Modelleme", "Dijital Sanat", "Blender Rehberi", "Tasarım Eğitimi"]
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

**[Tinkercad Rehberimizle]({{< ref "posts/tinkercad-baslangic-rehberi.md" >}})** geometrik şekillerle harika tasarımlar yaptınız. Ama bir süre sonra fark ettiniz ki; küpler ve silindirler, aklınızdaki o organik, kıvrımlı ve sanatsal şekilleri (bir insan yüzü, bir canavar veya fantastik bir vazo) yaratmak için yetersiz kalıyor.

Tinkercad bir inşaat mühendisiyse, **Blender** bir heykeltıraştır.

> Blender, Hollywood filmlerinden (Spider-Man gibi) video oyunlarına kadar her yerde kullanılan devasa, ücretsiz bir canavardır. Arayüzü başta sizi korkutabilir, beni de korkutmuştu. Ama korkmayın!

Biz bu okyanusa parmak ucundan gireceğiz ve sadece en eğlenceli kısmına odaklanacağız: **Sculpt Mode (Heykel Modu)**. Bu modda, ekranınızdaki dijital bir kil topunu, fırçalarla itip çekerek şekillendirirsiniz. Tıpkı gerçek çamurla oynar gibi.

Bu rehberde, Blender'ın karmaşık menülerini bir kenara bırakıp, doğrudan yaratıcılığın kalbine iniyoruz.

{{< tip-box title="💡 Sürekli Kaydetme Alışkanlığı (Ctrl+S)" >}}
Blender güçlüdür ama bazen çökebilir. Yaptığınız eseri kaybetmemek için her güzel hamleden sonra `Ctrl+S` yapmayı refleks haline getirin!
{{< /tip-box >}}

### Atölyenizi Hazırlayın: İlk Adımlar

1.  [blender.org](https://www.blender.org)'dan programı indirip kurun.
2.  Açtığınızda ortadaki meşhur küpü seçip `X` tuşuyla silin (Bu bir Blender geleneğidir).
3.  Üst menüden `Add > Mesh > UV Sphere` seçerek sahneye bir küre ekleyin. Bu bizim oyun hamurumuz.
4.  Küre seçiliyken sol üstteki `Object Mode` menüsünden **`Sculpt Mode`** seçeneğine geçin.

Ve işte! Sol tarafta fırçalarınız belirdi.

**Küçük Bir Sır (Simetri):** Sağ üstteki `X` simgesine tıklayın. Böylece modelin sağında ne yaparsanız, solunda da aynısı olur. (Göz yaparken çok işe yarar).

### Sanatçının Alet Çantası: 5 Sihirli Fırça

Yüzlerce fırça var ama ben %90 işimi sadece bu 5 tanesiyle yapıyorum:

1.  **Grab (Tut):** Kili tutup çekiştirmek için. (Kafayı uzatmak, kulak çekmek vb.)
2.  **Draw Sharp (Keski):** Keskin hatlar çizer. `Ctrl` basarak kullanırsanız dışa doğru sivri hat çizer.
3.  **Inflate (Şişir):** Balon gibi şişirir. Yanakları veya kasları yapmak için.
4.  **Crease (Kırışıklık):** İnce ve keskin yarıklar açar. Dudak çizgisi veya göz kapağı için.
5.  **Smooth (Düzleştir):** En iyi dostunuz. Yüzeydeki pürüzleri ütüler. (Kısayolu: Hangi fırçada olursanız olun `Shift` tuşuna basılı tutun).

**Kısayollar:** Fırça boyutu için `F`, gücü için `Shift + F`.

### İlk Eseriniz: Sevimli Bir Mantar Yontalım

Teori bitti, hadi elleri kirletelim.

**Adım 1: Ana Form**
*   **`Grab`** fırçasını alın (`F` ile büyütün). Kürenin altından tutup aşağı çekerek mantarın sapını oluşturun.

**Adım 2: Şapka**
*   **`Inflate`** fırçasıyla üst kısmı (şapkayı) biraz şişirin.
*   Tekrar **`Grab`** ile şapkanın kenarlarını aşağı doğru eğerek o klasik mantar formunu verin.

**Adım 3: Detaylar**
*   Mantarın altına bakın. **`Crease`** fırçasıyla merkezden dışarı doğru çizgiler çekerek mantarın alt dokusunu (lamelleri) yapın.
*   Sapına **`Draw Sharp`** ile küçük oyuklar ekleyerek doğal görünüm verin.

**Adım 4: Baskıya Hazırlık**
*   Sculpt bitince sol üstten `Object Mode`'a dönün.
*   Sağdaki menüden (İngiliz anahtarı ikonu) `Add Modifier > Solidify` ekleyin. `Thickness` değerini **2mm** yapın. (Bu, modelinizin içinin boş ama duvarlarının kalın olmasını sağlar, baskı için şarttır).
*   `File > Export > Stl` diyerek kaydedin.

{{< success-story-box title="✨ Kendi Deneyimim: İlk Heykelim Bir Patatesti" >}}
Blender'ı ilk açtığımda bir "Ork" kafası yapmak istemiştim. Sonuç, yamuk yumuk bir patatese benzedi. Pes etmedim. Sadece **Grab** ve **Smooth** fırçalarını kullanarak o patatesi yavaş yavaş şekillendirdim. Bir hafta sonra o patates, gerçekten bir yüze benzemeye başladı. Yetenek değil, sabır işi.
{{< /success-story-box >}}

## Sonuç: Yaratıcılığınızda Sınırları Kaldırın

Tinkercad ile "inşa ediyordunuz", Blender ile "yaratıyorsunuz". Artık sadece köşeli kutular değil, organik ve sanatsal eserler de yapabilirsiniz.

Ancak... Ya bir motor parçası, bir dişli kutusu veya milimetrik hassasiyet gerektiren bir kapak tasarlamak isterseniz? Heykel yapmak burada işe yaramaz. Mühendislik gerekir.

### Yolculuğun Bir Sonraki Durağı

Sanatsal özgürlükten, milimetrik mühendisliğe geçiş yapıyoruz. Profesyonellerin kullandığı, her vidasına kadar tasarlayabileceğiniz o güçlü araca adım atalım.

<div class="post-cta-box">
<h3>Sırada: Fusion 360 ile Mühendislik Tasarımı</h3>
<p>Parametrik tasarım nedir? Bir vida deliğini sonradan tek tıkla nasıl değiştirirsiniz? Profesyonel tasarımın kapılarını aralıyoruz.</p>
<a href="{{< ref "posts/fusion-360-baslangic-rehberi.md" >}}" class="cta-button">Fusion 360 Rehberine Git →</a>
</div>