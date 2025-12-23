---
title: "Parça Birleştirme Teknikleri: Büyük Modelleri ve Mekanik Parçaları Birleştirme Sanatı"
date: 2025-09-02T10:00:00+03:00
featured: true
draft: false
description: "Yazıcınızın hacmine sığmayan dev projeler mi yapıyorsunuz? Siyanoakrilat, epoksi, sürtünme kaynağı ve sıcak gömme somun (heat-set insert) teknikleriyle profesyonel montaj rehberi."
tags: ["3D Model Birleştirme", "Parçalı Baskı", "Japon Yapıştırıcısı", "Epoksi", "Plastik Kaynak", "Heat Set Insert", "Cosplay Yapımı", "Model Kesme", "Dowel", "Mıknatıs"]
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
    image: "/images/parca-birlestirme-cover.jpg"
    alt: "İki parçaya ayrılmış bir 3D modelin birleştirilme aşaması, yapıştırıcılar ve sıcak somun uygulama aletleri"
    caption: "Yazıcınızın boyutu 22cm olabilir ama hayalleriniz 2 metre olabilir. Sırrı: Doğru birleştirmede."
    relative: false
---

Standart bir 3D yazıcının baskı hacmi genellikle 22x22x25 cm civarındadır. Ancak hayallerimiz genelde bu kutuya sığmaz. Tam boy bir kask (Cosplay), 1 metrelik bir RC uçak kanadı veya devasa bir mimari maket basmak istediğinizde tek bir seçeneğiniz kalır: **Modeli parçalara bölmek ve sonra birleştirmek.**

Çoğu yeni başlayan kullanıcı, parçaları sadece "keser" ve uç uca Japon yapıştırıcısı ile tutturmaya çalışır. Sonuç? En ufak darbede kırılan ek yerleri, beyazlaşmış yapıştırıcı izleri ve hizalanmamış yamuk modeller.

Bu rehberde, plastikleri birbirine sadece yapıştırmayı değil, onları **mekanik ve kimyasal olarak kaynaştırmayı** öğreneceğiz. İster bir heykel yapın, ister yük taşıyan bir robot kolu; her senaryo için farklı bir teknik vardır.

---

## 1. Tasarım Aşamasında Birleştirme (Slicer Cut Tool)

Birleştirmeyi, baskı bittikten sonra değil, daha dilimleme (Slicing) aşamasında düşünmelisiniz. İki düz yüzeyi birbirine yapıştırmak zordur; kayarlar.

**OrcaSlicer ve Bambu Studio'nun Gücü:**
Modern dilimleyicilerde "Cut" (Kes) aracı içinde **"Add Connectors" (Bağlantı Ekle)** özelliği vardır. Bunu mutlaka kullanın.
*   **Snap (Çıtçıt):** Küçük, yük binmeyen modeller için.
*   **Dowel (Pim):** En sağlam yöntemdir. Yazılım, kesilen yüzeylere otomatik delikler açar. Siz de ayrıca "Pim" basarsınız.
    *   **Teknik İpucu:** Pimleri (Dowels) her zaman **yatay** basın. Dikey basılan pimler katman yerlerinden kolayca kırılır. Yatay basılan pimler ise yükü lifleri boyunca taşır.

## 2. Kimyasal Birleştirme (Yapıştırıcılar)

Hangi plastiği neyle yapıştıracaksınız? PLA'yı tutan şey, ABS'yi tutmayabilir.

### A. Siyanoakrilat (Hızlı Yapıştırıcı / Japon) + Aktivatör
PLA, PETG ve çoğu plastik için en pratik çözümdür.
*   **Nasıl Kullanılır:** Bir yüzeye yapıştırıcıyı sürün, diğer yüzeye **Aktivatör Spreyi** sıkın. Birleştirdiğiniz an (1-2 saniye içinde) taş gibi donar.
*   **Dezavantajı:** Kırılgandır (Darbe alırsa çatlar). Ayrıca kururken etrafa beyaz bir buhar (blooming) yayar ve modelin rengini bozabilir. Görünür yüzeylerde dikkatli olun.

### B. Epoksi (İki Bileşenli) Yapıştırıcı
Eğer yaptığınız parça yük taşıyacaksa (örneğin bir raf ayağı veya kılıç sapı) Japon yapıştırıcısı yetmez. Epoksi kullanmalısınız.
*   **Avantajı:** Boşluk doldurur. İki parça arasında 1mm boşluk kalsa bile epoksi orayı doldurur ve beton gibi olur.
*   **Süre:** Donması 5-30 dakika sürer. Bu süre size parçaları hizalamak için zaman kazandırır.

### C. Solvent Kaynağı (Sadece ABS/ASA İçin)
Bu bir yapıştırma değil, **eritme** işlemidir.
*   **Aseton:** ABS parçaların birleşim yüzeylerine aseton sürerseniz, plastik erir. Birleştirdiğinizde iki parça tek bir parça gibi kaynar. En sağlam yöntem budur ama PLA ve PETG'de işe yaramaz.

---

## 3. Isıl Birleştirme (Plastik Kaynağı)

Kimyasal yok, sadece ısı ve fizik var. Özellikle büyük Cosplay zırhları ve kaskları için vazgeçilmezdir.

### A. Havya ile Dikiş Atmak (Soldering)
Parçaları iç taraftan birleştirmenin en ucuz yoludur.
1.  Eski, gözden çıkardığınız bir havya ucunu takın.
2.  Ek yerini ısıtarak plastiği birbirine karıştırın.
3.  Sağlamlaştırmak için, erimiş plastiğin içine küçük metal zımba telleri veya tel parçaları gömün. Bu, parçanın esnediğinde ayrılmasını engeller.

### B. Sürtünme Kaynağı (Friction Welding)
Dremel (döner alet) kullanıyorsanız harika bir tekniktir.
1.  Dremel'in ucuna kısa bir parça filament (modelinizle aynı malzeme) takın.
2.  Yüksek devirde dönerken, filamenti ek yerine bastırın.
3.  Sürtünme ısısı hem filamenti hem de modeli eritir ve ortaya mükemmel bir kaynak dikişi çıkar. Epoksiden bile sağlam olabilir.

---

## 4. Mekanik Montaj: Profesyonelliğin Zirvesi (Heat Set Inserts)

Eğer tasarladığınız parçalar sökülüp takılacaksa (örneğin bir pil kapağı veya elektronik kutusu), plastiğe vida atamazsınız. Plastik vida yuvası 3-4 sökmeden sonra yalama olur.

Çözüm: **Sıcak Gömme Somun (Heat Set Insert).**

Bu, dışı tırtıklı, içi dişli pirinç bir somundur.
*   **Uygulama:**
    1.  Tasarımda vida deliğini somundan biraz küçük çizin.
    2.  Havyanızı 250-300°C'ye ısıtın.
    3.  Somunu deliğin üzerine koyun ve havya ile bastırın.
    4.  Isınan pirinç, plastiği eriterek tereyağı gibi içeri kayar.
    5.  Soğuduğunda, plastik somunun tırtıklarına kilitlenir. Artık o somunu oradan atom bombası gelse çıkaramaz.

Bu teknik, parçalarınızı "oyuncak" seviyesinden "endüstriyel ürün" seviyesine taşır.

![Bir havya kullanılarak 3D baskı parçaya pirinç vida yuvasının (heat set insert) yerleştirilmesi](/images/heat-set-insert.jpg "Plastiğe metal gücü katmak: Heat Set Insert uygulaması.")

---

## 5. Görünmez Ek Yerleri (Post-Processing)

Birleştirmeyi yaptık, parça sağlam. Ama ortada kocaman bir çizgi var. Bunu nasıl yok edeceğiz?

1.  **Zımpara:** Önce kaba (120-180 kum), sonra ince (240-400 kum) zımpara ile ek yerindeki yüksekliği alın.
2.  **Macun (Filler):** Çizgi hala oradadır çünkü çukurdur. Orayı "Model Macunu" veya "Çelik Macun" ile doldurun.
3.  **Tekrar Zımpara:** Macun kuruyunca tekrar zımparalayın. Parmak ucunuzla dokunduğunuzda ek yerini hissetmemelisiniz.
4.  **Astar (Primer):** Astar boya, tüm yüzeyi eşitler ve kalan mikro hataları gösterir.

---

## Sonuç: Parçalar Bütünden Büyüktür

Gördüğünüz gibi birleştirme işlemi, sadece "yapıştırıcı sıkıp bastırmak" değildir.
*   Yük binecekse **Pim + Epoksi** kullanın.
*   Sökülüp takılacaksa **Heat Set Insert** kullanın.
*   Cosplay yapıyorsanız **Havya ile Kaynak** yapın.

Doğru teknikle birleştirilmiş bir model, tek parça basılmış bir modelden bile daha sağlam olabilir.

Şimdiye kadar hep sert plastikleri (PLA, PETG, ABS) konuştuk. Kesiyoruz, zımparalıyoruz, yapıştırıyoruz... Peki ya malzeme sert değilse? Ya lastik gibi esniyorsa?

### Yolculuğun Bir Sonraki Durağı

3D baskının en "inatçı" ama en eğlenceli malzemesi: **TPU (Esnek Filament).**
Extruder dişlisine dolanan, borularda sıkışan bu malzemeyle nasıl başa çıkılır? Telefon kılıfı, conta veya tekerlek basmanın sırları neler?

<div class="post-cta-box">
<h3>Sırada: Esnek Filamentlerle (TPU) Baskı Rehberi</h3>
<p>Lastik gibi esneyen parçalar üretmenin püf noktaları. Yavaş baskı, retraction ayarları ve 'Direct Drive'ın önemi.</p>
<a href="{{< ref "posts/esnek-filament-baski-rehberi.md" >}}" class="cta-button">TPU Baskı Rehberine Git →</a>
</div>