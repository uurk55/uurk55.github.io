---
title: "Temel Slicer Ayarları: Baskı Kalitenizi Değiştirecek 5 Kritik Ayar"
date: 2025-05-03T11:00:00+03:00
featured: false
draft: false
description: "3D baskı kalitenizi dramatik şekilde artıracak en kritik 5 temel dilimleyici (slicer) ayarını öğrenin. Katman yüksekliği, dolgu, hız, destekler ve tabla yapışması için uzman ipuçları."
tags: ["Slicer Ayarları", "Cura Ayarları", "PrusaSlicer", "3D Baskı Kalitesi", "Katman Yüksekliği", "Dolgu Ayarları", "Baskı Hızı", "Destek Yapıları", "Tabla Yapışması", "Başlangıç Rehberi"]
categories: ["Teknik İpuçları"]
faz: ["Faz 1"]
series: ["3D Baskı Temelleri Serisi"]
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
    image: "/images/slicer-ayar-cover.jpg"
    alt: "Bir bilgisayar ekranında 3D slicer yazılımı ve yanında mükemmel basılmış bir 3D obje"
    caption: "Mükemmel baskının sırrı, doğru ayarlarda gizlidir. Kontrolü elinize alın!"
    relative: false
---

Harika bir 3D model indirdiniz, en kaliteli filamenti aldınız ve yazıcınız baskıya hazır. "Yazdır" tuşuna basıyorsunuz ve sonuç... bir hayal kırıklığı. Eğri büğrü duvarlar, zayıf bir yapı, dağınık yüzeyler. Peki sorun ne? Sorun, büyük ihtimalle dijital model ile fiziksel yazıcı arasındaki en önemli köprüde, yani **Dilimleyici (Slicer)** yazılımında.

Slicer, 3D modelinizi alan ve onu katman katman nasıl basılacağını anlatan talimatlar bütününe, yani G-Code'a dönüştüren programdır. Yazıcınıza, "Hangi sıcaklığı kullan? İçini ne kadar doldur? Ne kadar hızlı hareket et?" gibi tüm komutları veren odur. Bu komutlar yanlışsa, sonuç kaçınılmaz olarak **[kötü bir baskı]({{< ref "posts/3d-baski-hatalari-cozumleri.md" >}})** olur.

Neyse ki, bu sürecin kontrolü tamamen sizde! Bu rehberde, bir modeli baskıya nasıl hazırlayacağınızı ve sonuçlarınızı dramatik bir şekilde iyileştirecek **en kritik 5 temel slicer ayarını** öğreneceksiniz.

### İlk Adım: Modeli Dilimleyiciye Yükleme

Her şeyden önce, bir dilimleyici yazılımına ihtiyacımız var. Piyasada en popüler ve ücretsiz olan iki tanesi **Ultimaker Cura** ve **PrusaSlicer**'dır. İkisinden birini bilgisayarınıza kurup, kendi 3D yazıcı modelinizi seçerek bir profil oluşturun. Modeli yüklemek ise çok kolay: İndirdiğiniz STL dosyasını, farenizle tutup doğrudan açık olan dilimleyici programının penceresine **sürükleyip bırakın.**

![Bir STL dosyasının Cura veya PrusaSlicer arayüzüne sürüklenip bırakıldığı anı gösteren ekran görüntüsü](/images/slicer-import.jpg "Modeliniz artık sanal baskı tablasının üzerinde, talimatlarınızı bekliyor.")

Modeliniz artık sanal baskı tablasının üzerinde duruyor. Şimdi, o karmaşık görünen ayarları anlamlandırma zamanı.

## 1. Katman Yüksekliği (Layer Height): Kalite ve Hızın Dengesi

Bu ayar, baskınızın dikey çözünürlüğünü belirler.
* **Düşük Değer (örn: 0.12mm):** Baskı çok daha uzun sürer ama sonuç pürüzsüz ve detaylıdır. Katman çizgileri neredeyse görünmez olur.
* **Yüksek Değer (örn: 0.28mm):** Baskı çok hızlı biter ama katman çizgileri daha belirgin olur.

![Aynı 3D modelin farklı katman yükseklikleriyle basılmış iki versiyonu yan yana: Biri pürüzsüz, diğeri belirgin katman çizgili](/images/slicer-layer-height.jpg "Solda düşük katman yüksekliği (kaliteli), sağda yüksek katman yüksekliği (hızlı).")

{{< tip-box title="💡 Pratik Kural" >}}
Çoğu günlük baskı için `0.20mm` harika bir başlangıç noktasıdır. Hızlı bir prototip için değeri yükseltin, sergileyeceğiniz sanatsal bir obje için ise düşürün. Unutmayın: Katman yüksekliğini yarıya düşürmek, baskı süresini yaklaşık iki katına çıkarır!
{{< /tip-box >}}

## 2. Dolgu (Infill): Sağlamlık ve Malzeme Tasarrufu

Dolgu, baskınızın iç yapısını, yani iskeletini oluşturan destek ağıdır ve yüzde olarak ayarlanır.

* **%10-20 (Standart Dolgu):** Üzerine yük binmeyecek çoğu dekoratif obje için fazlasıyla yeterlidir.
* **%25-50 (Fonksiyonel Dolgu):** Duvara asılacak bir braket veya sık kullanılacak bir alet gibi sağlamlık gerektiren parçalar için idealdir.

Ayrıca **Dolgu Deseni (Infill Pattern)** de önemlidir. Hız için `Grid`, çok yönlü sağlamlık için `Cubic` en popüler seçeneklerdir.

## 3. Baskı Hızı (Print Speed): Kaliteden Ödün Vermeden Zaman Kazanmak

Baskı hızını artırmak süreyi düşürür, ancak kaliteden ödün vermenize neden olabilir. Yüksek hız, yüzeyde dalgalanmalara ("ringing"), zayıf katman yapışmasına ve detay kaybına yol açabilir.

{{< tip-box title="🔑 Altın Kural" >}}
Baskının görünen yüzü olan **Dış Duvar Hızını (Outer Wall Speed)** her zaman genel hızınızdan daha yavaş tutun (genellikle %50'si kadar). Bu, pürüzsüz ve temiz bir dış yüzey elde etmenin en büyük sırrıdır.
{{< /tip-box >}}

## 4. Destek Yapıları (Supports): Yer Çekimine Meydan Okumak

Bir katmanı, altında onu tutacak başka bir katman olmadan boşluğa basamazsınız. Slicer, modelinizin "havada kalacak" kısımlarını otomatik olarak tespit eder ve bu kısımların çökmemesi için altlarına geçici destek yapıları inşa eder. Genel kural olarak, bir çıkıntının açısı dikeyden itibaren **45-50 dereceyi** aştığında destek gerekir.

![Bir ejderha modelinin altında ağaç (tree) tipi destek yapıları gösteriliyor](/images/slicer-supports.jpg "Ağaç destekler, karmaşık modeller için hem verimli hem de sökmesi kolay bir çözümdür.")

* **Destek Tipi:** Karmaşık ve organik şekilli modeller (figürler gibi) için **Tree (Ağaç)** destekler harikadır.
* **Yerleşim:** Mümkün olduğunca **Touching Buildplate (Sadece Tablaya Değen)** seçeneğini kullanın. Bu, modelinizin yüzeyine en az zararı verir.

## 5. Tabla Yapışması (Adhesion): Başarılı Bir Başlangıcın Garantisi

Baskınızın tabladan ayrılıp bir "spagetti yığınına" dönüşmesini engellemek için bu ayarlara hakim olmalısınız.

1.  **Skirt (Etek):** Modele değmeyen, baskı başlamadan önce nozzle'ı temizleyen dış hatlardır. **Neredeyse her zaman kullanın.**
2.  **Brim (Kenarlık):** Modelin tabanına yapışık, yüzey alanını artırarak yapışmayı güçlendiren tek katmanlı bir kenarlıktır. Köşeleri kalkan veya devrilmeye müsait baskılarda hayat kurtarır.
3.  **Raft (Sal):** Modelin altına basılan kalın bir plastik "sal"dır. **Sadece son çare olarak kullanılır.**

![Skirt, Brim ve Raft seçeneklerinin 3D model etrafındaki görsel karşılaştırması](/images/tabla-yapisma.jpg "Soldan sağa: Skirt, Brim ve Raft.")

### Hızlı Ayar Tablosu: Yeni Başlayanlar İçin Öneriler

| Ayar | Ne İşe Yarar? | Başlangıç Tavsiyesi |
| :--- | :--- | :--- |
| **Katman Yüksekliği** | Detay seviyesini belirler. | ⚙️ `0.20mm` (Standart Kalite) |
| **Dolgu (Infill)** | İç sağlamlığı oluşturur. | 🧱 `15%` (Cubic Desen) |
| **Baskı Hızı** | Baskı süresini etkiler. | 🚀 `50 mm/s` (Genel Hız) |
| **Destekler** | Boşluktaki kısımları tutar. | 🌳 `Ağaç (Tree)` (Organik modellerde) |
| **Tabla Yapışması** | Baskının tutunmasını sağlar. | ✅ `Etek (Skirt)` (Her Zaman) |

## Sonuç: Artık Kontrol Sizde!

Artık bir dilimleyici yazılımının en kritik 5 temel ayarını öğrendiniz. En iyi öğrenme yolu, bu temel ayarlarla korkmadan oynamak ve sonuçlarını gözlemlemektir. Her model, farklı ayarlar gerektirebilir ve en iyi sonuçları deneyerek bulacaksınız.

### Yolculuğun Bir Sonraki Durağı

Ayarlarınızı yaptınız ama baskı sırasında beklenmedik bir sorun mu çıktı? Endişelenmeyin, en iyi kullanıcıların bile başına gelir.

<div class="post-cta-box">
<h3>Şimdi Sırada Ne Var?</h3>
<p>Eğer bu ayarlara rağmen baskılarınızda sorun yaşıyorsanız, en sık karşılaşılan problemlerin çözümlerini öğrenme zamanı!</p>
<a href="{{< ref "posts/3d-baski-hatalari-cozumleri.md" >}}" class="cta-button">3D Baskı Hataları ve Çözümleri Rehberine Git →</a>
</div>

{{< success-story-box title="✨ Başarı Hikayesi: İpliklenme Sorununa Slicer Çözümü" >}}
Can, aylarca 'stringing' (ipliklenme) sorunuyla boğuşuyordu. Her baskısı filament telleriyle doluydu. Bu rehberdeki **Geri Çekme (Retraction)** ve **Baskı Hızı** ayarlarını inceleyerek kendi slicer ayarlarında küçük değişiklikler yaptı. Sonuç: Kusursuz, tertemiz baskılar! Bu sayede figür satışları da ikiye katlandı.
{{< /success-story-box >}}

### Deneyimlerinizi Paylaşın!
Siz en çok hangi slicer ayarıyla oynuyorsunuz? Baskı kalitenizi artıran en büyük sırrınız neydi? Yorumlarda bizimle paylaşın!