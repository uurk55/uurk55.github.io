---
title: "Sipariş Bazlı 3D Baskı: Stok Tutmadan Satış Yapmak"
date: 2025-10-10T10:00:00+03:00
featured: false
draft: false
description: "Stok maliyeti olmadan satış yapmanın (Print on Demand) avantajları ve gizli tehlikeleri. Üretim kuyruğu yönetimi, makine arızası riskleri ve 'Hibrit Stok' stratejisi."
tags: ["Sipariş Bazlı Üretim", "Print on Demand", "Stoksuz E-Ticaret", "Üretim Planlama", "3D Baskı Yönetimi", "Batch Üretim", "Kriz Yönetimi"]
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
  image: "/images/siparis-bazli-uretim-cover.png"
  alt: "3D yazıcı, bekleyen sipariş listesi ve zaman baskısını simgeleyen saat"
  caption: "Stok tutmamak özgürlüktür, ancak zamana karşı yarış başlatır."
  relative: false
---

E-ticaretin en büyük kabusu "Stok Maliyeti"dir. Binlerce liralık ürün basarsınız, rafa koyarsınız ve satılmazsa o para çöp olur.

3D baskı teknolojisinin en büyük devrimi işte buradadır: **Sipariş Üzerine Üretim (Print on Demand - PoD).**

Müşteri siparişi verir, ödemeyi yapar; siz makineyi çalıştırırsınız. Cebinizden para çıkmadan satış yapmış olursunuz. Kulağa harika geliyor, değil mi?

Ancak bu modelin, tecrübesiz satıcıları batıran gizli bir tuzağı vardır: **Zaman Baskısı ve Makine Arızası.** Sipariş geldiği an, saat işlemeye başlar. O an nozzle tıkanırsa veya elektrik kesilirse, müşteriye ne diyeceksiniz?

Bu rehberde, stoksuz satışın teknik yönetimini, kriz senaryolarını ve benim uyguladığım **"Hibrit Stok"** sistemini inceleyeceğiz.

---

### 1. Sipariş Bazlı Modelin (PoD) Avantajları

Neden herkes stok yapmıyor? Çünkü PoD modelinin finansal özgürlüğü çok yüksektir.

*   **Sıfır Sermaye Riski:** Ürün satılmadan filament harcamazsınız. "Elimde kaldı" derdi yoktur.
*   **Sınırsız Varyasyon:** Stok tutmadığınız için müşteriye 50 farklı renk veya isim yazma seçeneği sunabilirsiniz. Stoklu çalışsaydınız her renkten 10 tane basmak zorunda kalırdınız.
*   **Depo Derdi Yok:** Evinizin bir köşesi deponuzdur. Binlerce kutuya ihtiyacınız yoktur.

![Sipariş geldiğinde üretimin başlaması](/images/siparis-geldi-an.png)

---

### 2. Madalyonun Diğer Yüzü: Operasyonel Riskler ⚠️

"Sipariş gelince basarım" demek kolaydır. Ama Cuma akşamı 10 sipariş birden gelirse ve Pazartesi kargoya vermeniz gerekirse ne olacak?

#### A. Darboğaz (Bottleneck) Riski
Tek bir yazıcınız varsa, üretim kapasiteniz bellidir.
*   **Örnek:** Ürününüz 4 saatte basılıyor. Günde maksimum 6 tane basabilirsiniz (uyumazsanız).
*   **Kriz:** Kampanya döneminde 20 sipariş gelirse, son müşterinin ürününü basmanız 4 gün sürer. Geç kargo = Kötü yorum.

![Tek yazıcıyla biriken siparişler](/images/tek-yazici-darbogaz.png)

#### B. Tek Nokta Hatası (Single Point of Failure)
Stoklu çalışırken makine bozulursa, raftan alıp gönderirsiniz. Ama PoD modelinde makine bozulursa, dükkan kapanır.
*   **Benim Kuralım:** Eğer tek yazıcınız varsa, asla %100 kapasiteyle sipariş almayın. Ya yedek bir makineniz olmalı ya da kritik parçaları stoklamalısınız.

---

### 3. Çözüm: "Hibrit Stok" ve "Batch" Stratejisi 🛡️

Benim atölyemde uyguladığım ve size de önerdiğim yöntem şudur: **Yarı Stoklu Çalışmak.**

#### A. Çok Satanlar Rafta (Pareto Kuralı)
Satışlarınızın %80'i, ürünlerinizin %20'sinden gelecektir.
*   **Strateji:** En çok satan "Siyah Telefon Standı"ndan elinizde her zaman 5-10 tane hazır olsun.
*   **PoD:** Nadir satılan "Pembe Stand"ı sipariş geldikçe basın.

#### B. Batch (Grup) Üretim Tekniği
Her sipariş için makineyi ısıtıp soğutmak zaman ve elektrik israfıdır.
*   **Yanlış:** Sabah 1 sipariş geldi bas, öğlen 1 sipariş geldi bas.
*   **Doğru:** Siparişleri biriktir (Platformun kargo süresine göre). Akşam 5 siparişi tek seferde, tek tablada (Plate) bas.

![Aynı üründen toplu baskı alma](/images/batch-uretim-3d-baski.png)

{{< tip-box title="💡 Teknik İpucu: İşlem Süresi (Processing Time)" >}}
Etsy veya Trendyol'da ürün açarken "Kargoya Veriliş Süresi"ni asla **1 gün** yapmayın.
Yazıcınız bozulabilir, elektrik kesilebilir. Kendinize her zaman **"Üretim Süresi + 2 Gün"** opsiyon bırakın. Müşteri erken gelince sevinir, geç gelince kızar.
{{< /tip-box >}}

---

### 📊 Karşılaştırma Tablosu: Hangi Model Sizin İçin?

<table class="summary-table">
    <thead>
        <tr>
            <th>Özellik</th>
            <th>Stoklu Satış</th>
            <th>Sipariş Bazlı (PoD)</th>
            <th>Hibrit (Önerilen)</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><strong>Sermaye İhtiyacı</strong></td>
            <td>Yüksek (Filament bağlarsınız)</td>
            <td>Düşük (Sattıkça alırsınız)</td>
            <td>Orta</td>
        </tr>
        <tr>
            <td><strong>Kargo Hızı</strong></td>
            <td>🚀 Çok Hızlı (Aynı gün)</td>
            <td>🐢 Yavaş (2-3 gün)</td>
            <td>Hızlı</td>
        </tr>
        <tr>
            <td><strong>Kişiselleştirme</strong></td>
            <td>Yok</td>
            <td>✅ Sınırsız</td>
            <td>Kısmi</td>
        </tr>
        <tr>
            <td><strong>Risk (Makine Arızası)</strong></td>
            <td>Düşük (Stok kurtarır)</td>
            <td>⚠️ Çok Yüksek (İptal gerekir)</td>
            <td>Yönetilebilir</td>
        </tr>
    </tbody>
</table>

---

## Sonuç: Zamana Karşı Yarış

Sipariş bazlı üretim, 3D baskının en büyük lütfudur. Ancak bu lütuf, doğru yönetilmezse strese dönüşür.
*   Tek yazıcınız varsa, kargo sürelerinizi uzun tutun (3-5 gün).
*   En çok giden ürünlerden (özellikle siyah/beyaz) kenarda 3-5 tane "acil durum stoku" bulundurun.

Sistemi kurduk, dükkanı açtık, ilk sipariş "Çınn!" sesiyle telefonumuza düştü. O an yaşanan heyecanla yapılan hatalar, dükkanın puanını daha ilk günden düşürebilir.

### Yolculuğun Bir Sonraki Durağı

İlk sipariş geldiğinde eliniz ayağınıza dolaşmasın. Paketlemeden kargo etiketine, müşteriye not yazmaktan "kargo kırık geldi" krizine kadar... İlk 10 siparişte yapılan acemi hataları ve çözümleri.

<div class="post-cta-box">
<h3>Sırada: İlk 10 Siparişte Yapılan Hatalar (Gerçek Deneyimler)</h3>
<p>Yanlış paketleme, eksik adres, unutulan hediyeler... İlk siparişlerinizi felakete değil, 5 yıldızlı bir deneyime dönüştürme rehberi.</p>
<a href="{{< ref "posts/ilk-10-sipariste-yapilan-hatalar.md" >}}" class="cta-button">Hata ve Çözüm Rehberine Git →</a>
</div>

<div class="post-cta-box">
<h3>3D Baskı Maliyetini Hemen Hesapla</h3>
<p>Sipariş bazlı çalışırken her işin gerçek maliyetini bilmek ve teklif verirken sürpriz yaşamamak için 3D Baskı Maliyet Hesaplama aracını kullanabilirsin.</p>
<a href="/maliyet-hesaplama/" class="cta-button">Maliyet Hesaplayıcıyı Aç →</a>
</div>
