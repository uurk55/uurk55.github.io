---
title: "Fiyatlandırma Stratejisi: Ürünlerinize Nasıl Değer Biçmelisiniz?"
date: 2025-09-30T13:30:00+03:00
featured: false
draft: false
description: "3D baskı ürünlerinizi doğru fiyatlandırmak, kârlılığınız için hayati öneme sahiptir. Malzeme, elektrik, işçilik maliyetlerini hesaplamayı ve rekabetçi fiyatlandırma stratejilerini öğrenin."
tags: ["3D Baskı Fiyatlandırma", "Maliyet Hesaplama", "Kâr Marjı", "Fiyatlandırma Stratejileri", "E-ticaret", "Amortisman", "3D Baskı İşletme", "Girişimcilik"]
categories: ["Para Kazanma"]
faz: ["Faz 3"]
series: ["3D Baskı ile Para Kazanma"]
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
    image: "/images/pricing-strategy-cover.png"
    alt: "3D baskı ürünleri fiyatlandırma stratejisi"
    caption: "Emeğinizin değerini belirleme sanatı: Doğru fiyat, sürdürülebilir bir işin temelidir."
    relative: false
---

3D yazıcınızda harika bir ürün tasarladınız ve bastınız. Belki de şimdiye kadarki en iyi baskınız oldu! Slicer programına baktınız, "Maliyet: 20 TL" yazıyor. "Harika, 50 TL'ye satarsam %150 kâr ederim" dediniz.

**Durun.** Eğer böyle düşünüyorsanız, aslında **zarar ediyorsunuz** ve bunun farkında bile değilsiniz.

Birçok 3D baskı girişimcisi, sadece filament parasını maliyet sanarak işe başlar ve ay sonunda "Neden param yok?" diye sorar. Çok ucuz fiyat verirseniz emeğinizin karşılığını alamaz, çok pahalı fiyat verirseniz müşterilerinizi kaybedersiniz. Doğru dengeyi bulmak, kârlılığınız ve işinizin sürdürülebilirliği için hayati öneme sahiptir.

Bu **fiyatlandırma stratejisi rehberi** ile, "bakkal hesabı" yapmayı bırakıp, bir mühendis gibi maliyet hesaplamayı öğreneceğiz.

---

### Fiyatlandırmanın Temeli: Tüm Maliyetlerinizi Bilin

Bir ürünün fiyatı, maliyetinin altında olamaz. Gerçek maliyeti belirleyen ve genelde gözden kaçan 5 temel kalemi detaylandıralım:

#### 1. Malzeme Maliyeti (Filament / Reçine)
Bu en bariz olanıdır ama Slicer'ın verdiği "tahmini" gramaj bazen yanıltıcı olabilir.
*   **Hesaplama:** `(Filament KG Fiyatı / 1000) * Harcanan Gram`.
*   **Fire Payı:** Her baskı başarılı olmaz. Başarısız baskıları ve destek (support) atıklarını karşılamak için bu maliyete mutlaka **%10-15 Fire Payı** ekleyin.
*   **Örnek:** 1000 TL'lik bir filamentten 50g kullandıysanız, maliyet 50 TL'dir. %10 fire ile **55 TL** olarak hesaplayın.

![Farklı filament makaraları veya reçine şişeleri, yanında bir dijital terazi ve bir not defteri.](/images/material-cost.png "Malzeme Maliyetinin Hesaplanması")

#### 2. Elektrik Tüketimi
"Yazıcı ne yakacak ki?" demeyin. Isıtmalı tabla (Bed) ve Nozzle saatlerce çalışıyor.
*   **Teknik Veri:** Ortalama bir Ender 3 veya Bambu Lab, saatte yaklaşık **0.15 - 0.3 kWh** elektrik tüketir.
*   **Formül:** `Baskı Saati * 0.2 kWh * Elektrik Birim Fiyatı`.
*   10 saatlik bir baskı, faturanıza sandığınızdan fazla yansıyabilir. Bunu kuruşu kuruşuna ekleyin.

#### 3. Yazıcı Amortismanı ve Bakım Maliyeti
Yazıcınız sonsuza kadar çalışmayacak. Nozzle aşınacak, kayış kopacak, fan bozulacak.
*   **Amortisman:** Bir yazıcının verimli ömrünü ortalama **3000 saat** (baskı saati) olarak kabul edin.
*   **Formül:** `Yazıcı Fiyatı / 3000 = Saatlik Yıpranma Bedeli`.
*   **Örnek:** 30.000 TL'lik bir makineniz varsa, saatte **10 TL** kenara koymalısınız ki makine öldüğünde yenisini alabilesiniz.

#### 4. İşçilik ve Zaman Maliyeti
**Sizin zamanınız en değerli varlığınızdır!** Hobiciyken zaman bedavadır ama ticarette değildir.
*   **Hesaplanacak Süreler:** Tasarım, dilimleme (slicing), baskı başlatma, tabladan sökme, destek temizleme, zımparalama ve paketleme.
*   **Öneri:** Kendinize bir "Saatlik Ücret" belirleyin (Örn: Asgari ücretin 2 katı). Ürünle *aktif* olarak ilgilendiğiniz süreyi (makinenin çalıştığı süreyi değil, sizin çalıştığınız süreyi) bu ücretle çarpın.

![Bir kişinin 3D baskı ürününü zımparaladığı veya boyadığı, yanında paketleme malzemeleri.](/images/labor-post-processing.png "İşçilik ve Baskı Sonrası İşlemler")

#### 5. İşletme Giderleri (Gizli Giderler)
Bunlar genellikle başlangıçta unutulan ama kârlılığı kemiren giderlerdir.
*   **Pazar Yeri Komisyonları:** Etsy (~%15), Shopier veya Amazon komisyonlarını fiyata dahil etmezseniz, kârınızdan yersiniz.
*   **Paketleme:** Kutu, patpat naylon, bant, etiket. Her kargo ortalama 10-20 TL paketleme masrafı demektir.
*   **Vergi:** Şirketiniz varsa KDV ve Gelir Vergisi'ni fiyata eklemelisiniz.

---

### Fiyat Belirleme Sanatı: Stratejinizi Geliştirin

Tüm maliyetleri (Malzeme + Elektrik + Amortisman + İşçilik + Giderler) topladık. Bu sizin **Taban Fiyatınız**. Bunun altına satarsanız batarsınız. Şimdi kâr ekleme zamanı.

#### 1. Maliyet Artı Kâr (Cost-Plus Pricing)
En basit ve güvenli yöntemdir.
*   **Formül:** `Satış Fiyatı = Toplam Maliyet * (1 + Kar Marjı Yüzdesi)`
*   **Örnek:** Maliyetiniz 100 TL ise ve %50 kâr istiyorsanız, 150 TL'ye satarsınız.
*   **Kimler İçin İdeal?** Yeni başlayanlar ve "garantici" olanlar için. Batma riskini sıfırlar.

#### 2. Rekabetçi Fiyatlandırma (Piyasayı Okuma)
Rakipleriniz ne yapıyor? Benzer bir ürün Etsy'de 200 TL ise, siz maliyetinize göre 150 TL bulsanız bile 190 TL'ye satabilirsiniz.
*   **Risk:** Eğer rakipler "fiyat kırma" savaşına girerse, siz de düşmek zorunda kalırsınız ve kârınız erir.
*   **Kimler İçin İdeal?** Çok satıcılı, rekabetin bol olduğu (telefon standı, saksı vb.) pazarlarda gereklidir.

![Bir bilgisayar ekranında Etsy gibi bir e-ticaret sitesinde benzer 3D baskı ürünlerinin fiyatlarının karşılaştırılması.](/images/competitive-pricing.png "Rekabetçi Fiyatlandırma Analizi")

#### 3. Değer Bazlı Fiyatlandırma (Ustalığınızı Fiyata Yansıtmak)
Bu strateji, "Maliyeti ne?" diye sormaz, **"Müşteri buna ne kadar öder?"** diye sorar.
*   Örneğin; kişiye özel, ismi yazılı, el boyaması bir figürün maliyeti 50 TL olabilir. Ama müşteri için manevi değeri yüksektir ve 500 TL ödeyebilir.
*   **Kimler İçin İdeal?** Tasarım yeteneği olan, niş ve özgün ürünler satanlar için en kârlı yöntemdir.

{{< tip-box title="💡 En İyi Strateji: Hibrit Yaklaşım" >}}
Genellikle en iyi yaklaşım, bu üç stratejinin bir kombinasyonudur. Önce **Maliyet Artı Kâr** ile "ölüm çizginizi" (asla altına düşmeyeceğiniz fiyatı) belirleyin. Sonra **Rekabetçi Fiyatlandırma** ile pazarın tavanını görün. Son olarak, ürününüzün kalitesine göre **Değer Bazlı** bir dokunuşla son fiyatı belirleyin.
{{< /tip-box >}}

### Fiyatlandırma Kontrol Listesi

Fiyatınızı belirlemeden önce bu tabloyu doldurun:

<table class="summary-table pricing-checklist">
    <thead>
        <tr>
            <th>Adım</th>
            <th>Eylem</th>
            <th>Neden Önemli?</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><strong>1. Maliyetleri Çıkar</strong></td>
            <td>✍️ Malzeme + Elektrik + Amortisman + İşçilik.</td>
            <td>Taban fiyatı bilmezseniz zarar edersiniz.</td>
        </tr>
        <tr>
            <td><strong>2. Gizli Giderleri Ekle</strong></td>
            <td>📦 Kargo kutusu, bant, platform komisyonu (%15-20).</td>
            <td>Cebinize giren net parayı görmek için.</td>
        </tr>
        <tr>
            <td><strong>3. Piyasayı Araştır</strong></td>
            <td>🔍 Rakipler kaça satıyor?</td>
            <td>Pazarın dışında kalmamak için.</td>
        </tr>
        <tr>
            <td><strong>4. Değer Ekle</strong></td>
            <td>✨ "Kişiye Özel", "El Boyaması" gibi değerler ekleyin.</td>
            <td>Kâr marjını artırmanın tek yolu budur.</td>
        </tr>
        <tr>
            <td><strong>5. Test Et ve Ayarla</strong></td>
            <td>🚀 Fiyatı belirleyin, satışı izleyin. Satmıyorsa indirin, çok satıyorsa artırın.</td>
            <td>Fiyat, yaşayan bir mekanizmadır.</td>
        </tr>
    </tbody>
</table>

---

## Sonuç: Değer Biçme Sanatında Ustalaşmak

3D baskı ürünlerinizi fiyatlandırmak, sadece bir hesap makinesi işi değildir; psikolojik bir süreçtir. Emeğinizi ucuza satmayın. Unutmayın, ucuza satılan malın "değersiz" algılanma riski vardır.

Maliyetlerimizi hesapladık, kârımızı koyduk ve satış fiyatımızı belirledik. Artık dükkanı açma vakti! Peki, bu ürünleri nerede satacağız? Sadece Etsy mi, yoksa sosyal medya veya yerel pazaryerleri mi?

### Yolculuğun Bir Sonraki Durağı

Dükkan açmak kolay, doğru platformu seçmek zordur. Etsy'de döviz kazanmak, Shopier ile yerel satış yapmak veya Amazon'a girmek... Hangi platformun komisyonu ne kadar? Hangi kitleye hitap ediyor?

<div class="post-cta-box">
<h3>Sırada: 3D Baskı Satışı İçin En İyi Pazaryerleri</h3>
<p>Etsy, Shopier, Amazon ve Dolap... Komisyon oranları, trafik kaynakları ve başlangıç için en doğru platformu seçme rehberi.</p>
<a href="{{< ref "posts/3d-baski-pazaryerleri-rehberi.md" >}}" class="cta-button">Pazaryeri Rehberine Git →</a>
</div>

<div class="post-cta-box">
<h3>3D Baskı Maliyetini Hemen Hesapla</h3>
<p>Filament, elektrik, bakım ve işçilik kalemlerini tek seferde görmek için 3D Baskı Maliyet Hesaplama aracını kullanabilirsin.</p>
<a href="/maliyet-hesaplama/" class="cta-button">Maliyet Hesaplayıcıyı Aç →</a>
</div>
