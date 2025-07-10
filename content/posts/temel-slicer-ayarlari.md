---
title: "Temel Slicer Ayarları: Baskı Kalitenizi Değiştirecek 5 Kritik Ayar"
date: 2025-05-03T11:00:00+03:00
draft: false
description: "3D baskı kalitenizi dramatik şekilde artıracak en kritik 5 temel dilimleyici (slicer) ayarını öğrenin. Katman yüksekliği, dolgu, hız, destekler ve tabla yapışması için uzman ipuçları."
tags: ["Slicer Ayarları", "Cura Ayarları", "PrusaSlicer", "3D Baskı Kalitesi", "Katman Yüksekliği", "Dolgu Ayarları", "Baskı Hızı", "Destek Yapıları", "Tabla Yapışması", "Teknik İpuçları"]
categories: ["Başlangıç Rehberi", "Teknik İpuçları"]
series: ["3D Baskı Temelleri Serisi"]
author: "uurk55"
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
    caption: "Mükemmel baskının sırrı, doğru tarifte gizlidir. Mutfağın kontrolünü elinize alın!"
    relative: false
---

Harika bir 3D model indirdiniz, en kaliteli filamenti aldınız ve yazıcınız baskıya hazır. "Yazdır" tuşuna basıyorsunuz ve sonuç... bir hayal kırıklığı. Eğri büğrü duvarlar, zayıf bir yapı, dağınık yüzeyler. Peki sorun ne? Sorun, büyük ihtimalle tarifte, yani **Dilimleyici (Slicer)** yazılımında.

> "Slicer nedir? En basit haliyle, o sizin 3D modelinizi alan ve onu 3D yazıcınız için bir 'yemek tarifine' dönüştüren şefinizdir. Modele, 'Hangi sıcaklıkta pişecek? İçini ne kadar doldurayım? Ne kadar hızlı hareket edeyim?' gibi tüm talimatları veren program budur."

Neyse ki, bu mutfağın kontrolü tamamen sizde! Bu rehberde, indirdiğiniz bir modeli baskıya nasıl hazırlayacağınızı ve sonuçlarınızı dramatik bir şekilde iyileştirecek **en kritik 5 temel slicer ayarını** öğreneceksiniz.

### İlk Adım: Modeli Dilimleyiciye Yükleme

Her şeyden önce, bir dilimleyici yazılımına ihtiyacımız var. Piyasada en popüler ve ücretsiz olan iki tanesi **Ultimaker Cura** ve **PrusaSlicer**'dır. İkisinden birini bilgisayarınıza kurup, kendi 3D yazıcı modelinizi seçerek bir profil oluşturun. Modeli yüklemek ise çok kolay: İndirdiğiniz STL dosyasını, farenizle tutup doğrudan açık olan dilimleyici programının penceresine **sürükleyip bırakın.**

![Bir STL dosyasının Cura veya PrusaSlicer arayüzüne sürüklenip bırakıldığı anı gösteren ekran görüntüsü](/images/slicer-import.jpg)

Modeliniz artık sanal baskı tablasının üzerinde duruyor. Şimdi, o karmaşık görünen ayarları anlamlandırma zamanı.

---

### 1. Katman Yüksekliği (Layer Height): Kalite vs. Hız

Bu ayarı, bir resmi çizerken kullandığınız kalemin ucu gibi düşünebilirsiniz.
* **Kalın Uçlu Kalem (Yüksek Değer, örn: 0.28mm):** Baskı çok hızlı biter ama katman çizgileri belirgin olur.
* **İnce Uçlu Kalem (Düşük Değer, örn: 0.12mm):** Baskı çok daha uzun sürer ama sonuç pürüzsüz ve detaylıdır.

![Aynı 3D modelin farklı katman yükseklikleriyle basılmış iki versiyonu yan yana: Biri pürüzsüz, diğeri belirgin katman çizgili](/images/slicer-layer-height.jpg)

**Pratik Kural:** Çoğu günlük baskı için `0.20mm` harika bir başlangıç noktasıdır. Hızlı bir prototip için değeri yükseltin, sergileyeceğiniz sanatsal bir obje için ise düşürün. Unutmayın: Katman yüksekliğini yarıya düşürmek, baskı süresini yaklaşık iki katına çıkarır!

### 2. Dolgu (Infill): Sağlamlık vs. Malzeme Tüketimi

Dolgu, baskınızın iç yapısını, yani iskeletini oluşturan destek ağıdır. Slicer'da bu ayarı genellikle yüzde olarak görürsünüz.

* **%10-20 (Standart Dolgu):** Üzerine yük binmeyecek çoğu dekoratif obje için fazlasıyla yeterlidir.
* **%25-50 (Fonksiyonel Dolgu):** Duvara asılacak bir braket veya sık kullanılacak bir alet gibi sağlamlık gerektiren parçalar için idealdir.

Ayrıca **Dolgu Deseni (Infill Pattern)** de önemlidir. Hız için `Grid`, çok yönlü sağlamlık için `Cubic`, esneklik ve havalı bir görünüm için ise `Gyroid` en popüler seçeneklerdir. **Pratik Kural:** `15%` dolgu yoğunluğu ve `Cubic` deseni, çoğu proje için en iyi dengedir.

### 3. Hız (Print Speed): Acele İşe Şeytan Karışır mı?

Baskı hızını artırmak süreyi düşürür, ancak kaliteden ödün vermenize neden olabilir. Yüksek hız, "ringing" (yüzeyde dalgalanma) gibi hatalara, zayıf katman yapışmasına ve detay kaybına yol açabilir.

Modern dilimleyiciler, baskının farklı bölümleri için farklı hızlar ayarlamanıza olanak tanır. **Altın Kural:** Baskının görünen yüzü olan **Dış Duvar Hızını (Outer Wall Speed)** her zaman genel hızınızdan daha yavaş tutun. **Pratik Kural:** Yeni bir filamenti veya karmaşık bir modeli denerken, **50-60mm/s** gibi mütevazı bir genel hızla başlayın.

### 4. Destekler (Supports): Yer Çekimine Meydan Okuma

Bir katmanı, altında onu tutacak başka bir katman olmadan boşluğa basamazsınız. Slicer, modelinizin "havada kalacak" kısımlarını otomatik olarak tespit eder ve bu kısımların çökmemesi için altlarına geçici destek yapıları inşa eder. Genel kural olarak, bir çıkıntının açısı dikeyden itibaren **45-50 dereceyi** aştığında destek gerekir.

![Örnek görüntüsü](/images/slicer-supports.jpg)

* **Destek Tipi:** Karmaşık ve organik şekilli modeller (figürler gibi) için **Tree (Ağaç)** destekler harikadır. Daha az malzeme harcar ve sökmesi daha kolaydır.
* **Yerleşim:** Mümkün olduğunca **Touching Buildplate (Sadece Tablaya Değen)** seçeneğini kullanın. Bu, modelinizin yüzeyine en az zararı verir.

### 5. Tabla Yapışması (Bed Adhesion): İlk Katman Garantisi

Baskınızın tabladan ayrılıp bir "spagetti yığınına" dönüşmesini engellemek için bu ayarlara hakim olmalısınız.

1.  **Skirt (Etek):** Modele değmeyen, baskı başlamadan önce nozzle'ı temizleyen dış hatlardır. **Neredeyse her zaman kullanın.**
2.  **Brim (Kenarlık):** Modelin tabanına yapışık, yüzey alanını artırarak yapışmayı güçlendiren tek katmanlı bir kenarlıktır. Köşeleri kalkan veya devrilmeye müsait baskılarda hayat kurtarır.
3.  **Raft (Sal):** Modelin altına basılan kalın bir plastik "sal"dır. **Sadece son çare olarak kullanılır,** çünkü çok fazla malzeme ve zaman harcar.

![Örnek görüntüsü](/images/tabla-yapisma.jpg)

### Sonuç: Artık Kontrol Sizde!

Artık bir dilimleyici yazılımının en kritik 5 temel ayarını öğrendiniz. En iyi öğrenme yolu, bu temel ayarlarla korkmadan oynamak ve sonuçlarını gözlemlemektir. Eğer bu ayarlara rağmen baskılarınızda sorun yaşıyorsanız, **[En Yaygın 3D Baskı Hataları ve Çözümleri kılavuzumuza]({{< ref "posts/3d-baski-hatalari-cozumleri.md" >}})** mutlaka göz atın. Artık başkalarının modellerini dilimlemekte ustalaştığınıza göre, belki de **[Tinkercad ile kendi modelinizi tasarlamanın]({{< ref "posts/tinkercad-baslangic-rehberi.md" >}})** zamanı gelmiştir. Mutfağın kontrolü artık sizde!

{{< success-story-box title="✨ Başarı Hikayesi: İpliklenme Sorununa Slicer Çözümü" >}}
Can, aylarca 'stringing' (ipliklenme) sorunuyla boğuşuyordu. Her baskısı filament telleriyle doluydu. Bu rehberdeki 'Retraksiyon' ve 'Baskı Hızı' ayarlarını inceleyerek kendi slicer ayarlarında küçük değişiklikler yaptı. Sonuç: Kusursuz, tertemiz baskılar! Bu sayede figür satışları da ikiye katlandı.
{{< /success-story-box >}}

---

**Siz en çok hangi slicer ayarıyla oynuyorsunuz? Baskı kalitenizi artıran en büyük sırrınız neydi? Yorumlarda bizimle paylaşın!**