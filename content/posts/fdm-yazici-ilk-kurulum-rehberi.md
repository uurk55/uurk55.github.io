---
title: "FDM 3D Yazıcı İlk Kurulum Rehberi: Kutudan İlk Başarılı Baskıya"
date: 2025-04-05T10:00:00+03:00
draft: false
cover:
    image: "/images/kurulum-rehberi-cover.jpg"
    alt: "Bir masanın üzerinde yeni kurulmuş bir FDM 3D yazıcı ve yanında başarılı bir test baskısı duruyor"
    caption: "Bu yolculuktaki en heyecanlı an: Fikirden gerçeğe ilk adım."
    relative: false
categories: ["Başlangıç Rehberi", "Teknik İpuçları"]
tags: ["fdm kurulum", "3d yazıcı kurulum", "ilk baskı", "tabla kalibrasyonu", "montaj"]
comments: true
---

O an geldi çattı! Haftalarca araştırdınız, rehberler okudunuz ve sonunda o büyük, heyecan verici kutu kapınıza dayandı. Yeni FDM 3D yazıcınız karşınızda duruyor. Bu heyecanı ve bir an önce harika baskılar alma isteğinizi çok iyi anlıyoruz. Ancak, bu ilk birkaç saat, tüm 3D baskı serüveninizin kalitesini belirleyecek olan en kritik anlardır. Aceleci davranmak, ileride saatlerce sürecek baş ağrılarına ve başarısız baskılara neden olabilir.

İşte bu yüzden, **FDM 3D yazıcı ilk kurulum** sürecinde size adım adım eşlik edecek bu rehberi hazırladık. Amacımız, kutu açılımından o tatmin edici ilk başarılı baskıyı alana kadar olan tüm adımları, en basit ve en anlaşılır şekilde size sunmak. Bu rehberi bir kontrol listesi gibi kullanarak, yeni **FDM yazıcınızla** sorunsuz ve keyifli bir başlangıç yapmanızı sağlayacağız. Hazırsanız, o kutuyu birlikte açalım!

*(Not: Eğer bir SLA (reçine) yazıcı aldıysanız, endişelenmeyin! Yakında yayınlayacağımız size özel, detaylı kurulum rehberini bekleyin!)*

### Adım 1: Kontrollü Kutu Açılımı ve Mekanik Montaj

Kutuyu bir an önce yırtıp açma isteğinizi bastırın ve derin bir nefes alın. Başarılı bir **3D yazıcı montajı**, kontrollü bir başlangıçla olur. İlk olarak, kutu içinden çıkan kullanım kılavuzundaki parça listesiyle kutu içeriğini karşılaştırarak envanter kontrolü yapın. Eksik bir parça varsa, ilerlemeden satıcıyla iletişime geçin.

![Bir kişinin 3D yazıcı montaj kılavuzuna bakarak parçaları birleştirmesi](/images/kurulum-montaj.jpg)

Montaj sırasında hem basılı kılavuzu hem de üreticinin YouTube'daki montaj videosunu aynı anda takip etmek en iyi yöntemdir. Taşıma sırasında gevşeyebilecek vidaları, özellikle de ana iskeleti oluşturanları kontrol edin ve sıkın. **Altın Kural:** Eksen tekerlekleri ne çok sıkı ne de çok gevşek olmalı; hafif bir dirençle, takılmadan dönmelidir. Sağlam ve oynamayan bir iskelet, "katman kayması" gibi sorunları önlemenin ilk adımıdır.

### Adım 2: Tabla Kalibrasyonu - Başarının Temeli

Şimdi, tüm baskılarınızın kalitesini belirleyecek olan ayara geldik: **Tabla Kalibrasyonu (Bed Leveling).** Amaç, baskı ucunun (nozzle) baskı tablasının her noktasına eşit ve doğru mesafede olmasını sağlamaktır. Bu mesafe yanlışsa, baskınız ya tablaya yapışmaz ya da nozzle tıkanır.

![Bir kişinin tabla kalibrasyonu yaparken nozul ile tabla arasına bir A4 kağıt koyması](/images/kurulum-kalibrasyon.jpg)

Eğer yazıcınızda **Otomatik Tabla Kalibrasyonu (ABL)** varsa, bu işlemi başlatın ve ardından menüden "Z-Offset" ayarını yapın. Bir A4 kağıdını nozzle ile tabla arasına koyarak, kağıdın hafifçe sürtünerek hareket ettiği noktayı bulana kadar Z-Offset değerini ayarlayın. Eğer manuel kalibrasyon yapıyorsanız, bu kağıt testini tablanın dört köşesi ve ortası için, tekerlekleri çevirerek en az iki tur boyunca tekrarlayın.

### Adım 3: Filamenti Yükleme ve İlk Isıtma

Yazıcınızın iskeleti sağlam, tablası ise ayarlı. Artık ona, eserlerini yaratacağı "mürekkebi", yani filamenti verme zamanı.

**Altın Kural:** Filamentin ucunu **ASLA** serbest bırakmayın! Eğer ucu serbest bırakırsanız, makara kendi kendine gevşeyebilir ve baskının ortasında takılıp her şeyi mahvedecek bir düğüm oluşturabilir.

![Bir kişinin filamentin ucunu 3D yazıcının extruder mekanizmasına takması](/images/kurulum-filament-yukleme.jpg)

Yazıcınızın menüsünden "Preheat PLA" (PLA için Ön Isıtma) seçeneğiyle nozzle'ı ısıtın. Isındıktan sonra, filamenti extruder mekanizmasından yavaşça itin. Ucundan erimiş plastiğin düzgün bir şekilde aktığını gördüğünüzde ve rengi tamamen oturduğunda, yazıcınız baskıya hazırdır.

### Adım 4: İlk Test Baskısı - O Sihirli An

Artık o büyülü "yazdır" tuşuna basma zamanı. Kendi modelinizi dilimlemeden önce, genellikle yazıcının SD kartında gelen `calibration_cube.gcode` gibi hazır bir test dosyasını basarak makinenin doğruluğunu test etmek en iyi yoldur.

**EN KRİTİK AN: İLK KATMAN**
Baskıyı başlattıktan sonra gözünüzü ilk katmandan ayırmayın. Plastik tablaya güzelce yapışıyor mu? Çizgiler ne çok ezilmiş ne de çok yuvarlak mı? Eğer ilk katmanda bir sorun görürseniz, baskıyı durdurun ve Z-offset ayarınızı çok küçük bir miktar değiştirip tekrar deneyin.

![Bir 3D yazıcının ilk katmanı mükemmel bir şekilde çizmesi - yakın çekim makro fotoğraf](/images/kurulum-ilk-katman.jpg)

İlk 2-3 katman sorunsuz atıldıysa, artık arkanıza yaslanıp makinenizin sihrini izleyebilirsiniz. Baskı bittiğinde tablanın soğumasını bekleyin ve parçanızı alın.

Tebrikler! Elinizde tuttuğunuz o küçük nesne, sadece bir plastik parçası değil; o, sizin başarınızın ilk somut kanıtıdır. Şimdi bu test baskısından daha ileri gitmek için, **[Temel Slicer Ayarları Rehberimizi]({{< ref "posts/temel-slicer-ayarlari.md" >}})** okuyarak baskı kalitenizi nasıl artıracağınızı öğrenebilirsiniz. Eğer baskı sırasında bir sorun yaşarsanız, **[3D Baskı Hataları Kılavuzumuz]({{< ref "posts/3d-baski-hatalari-cozumleri.md" >}})** her zaman yanınızda!