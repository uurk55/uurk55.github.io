---
title: "SLA Yazıcı İlk Kurulum Rehberi: Reçine Dünyasına Güvenli Adımlar"
date: 2025-07-22T10:00:00+03:00
featured: false
draft: false
description: "SLA (reçine) yazıcınızı güvenli ve doğru bir şekilde kurun. Reçine hazırlığından tabla kalibrasyonuna, baskı sonrası yıkama ve kürleme adımlarına kadar her şeyi öğrenin. Güvenlik önceliklidir!"
tags: ["SLA Kurulum", "Reçine Yazıcı", "3D Baskı Güvenliği", "Yıkama ve Kürleme", "İlk Baskı SLA", "Reçine Bakımı", "UV Reçine", "Başlangıç Rehberi", "Teknik İpuçları"]
categories: ["Başlangıç Rehberi"]
faz: ["Faz 1"]
series: ["3D Baskı Temelleri Serisi"]
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
    image: "/images/sla-kurulum-cover.jpg"
    alt: "Modern bir SLA yazıcı, yanında koruyucu ekipmanlar ve bir reçine şişesi ile bir atölye masasında duruyor"
    caption: "Detayların dünyasına hoş geldiniz. İlk kural: Önce güvenlik."
    relative: false
---

Detayların ve pürüzsüz yüzeylerin peşine düşerek bir SLA (reçine) yazıcı tercih ettiniz. Tebrik ederim! FDM yazıcıların mekanik ve gürültülü dünyasından, SLA'nın sessiz ama "yapışkan" dünyasına geçiş yapıyoruz.

Burada bir teknisyenden çok, bir **kimyager** gibi düşünmeniz gerekecek. Çünkü artık elimizde katı plastik ipler yok; kokulu, akışkan ve cilde temas etmemesi gereken sıvılar var.

Ben ilk reçine yazıcımı kurarken eldiven takmaya üşenmiştim. "Bir damladan bir şey olmaz" dedim. O bir damla elime bulaştı, oradan telefonuma, oradan kapı koluna... Bir saat sonra tüm oda yapış yapıştı. Bu hataya düşmeyin.

Bu rehber, sadece makineyi kurmayı değil; atölyenizi bir laboratuvar titizliğinde hazırlamayı öğretecek.

## Önce Atölyeyi Kurun (Makineden Önce!)

SLA yazıcıyı kutudan çıkarmadan önce, masanızın hazır olması lazım. Bu işin şakası yok.

{{< tip-box title="⚠️ Güvenlik ve Hazırlık Listesi" >}}
**Masada Olmazsa Olmazlar:**
* **🏞️ Havalandırma:** Yazıcıyı asla yatak odasına veya havasız bir odaya kurmayın. Penceresi açık bir oda veya balkon şarttır.
* **🧤 Nitril Eldivenler:** Lateks değil, nitril kullanın. Reçineye çıplak elle ASLA dokunmayın.
* **👓 Koruyucu Gözlük:** Reçine sıçrayabilir. Gözünüzü koruyun.
* **😷 Maske:** Reçine kokusu ve buharı için (Aktif karbon filtreli maskeler en iyisidir).
* **💧 İzopropil Alkol (IPA):** Temizlik için bolca (%90 ve üzeri saflıkta). Kolonya yetmez.
* **🧻 Kağıt Havlu:** Rulolarca havluya ihtiyacınız olacak.
{{< /tip-box >}}

## Adım 1: Makine Kurulumu ve "Sıfırlama"

SLA yazıcıların mekanik kurulumu FDM'e göre çok daha basittir. Genelde tek parça gelir, sadece kapağı takarsınız. Ama **Tabla Kalibrasyonu** (Leveling) hayati önem taşır.

![Bir kişinin SLA yazıcının baskı tablası ile LCD ekranı arasına bir kalibrasyon kartı koyması](/images/sla-kurulum-kalibrasyon.jpg "Bu basit kağıt, mikron düzeyinde bir hassasiyet ayarı yapmanızı sağlar.")

**Kalibrasyon Ritüeli (Sırasıyla):**
1.  **Reçine Haznesini (Vat) Çıkarın:** Sadece çıplak LCD ekran üzerinde çalışacağız.
2.  **Baskı Tablasını Gevşetin:** Üzerindeki vidaları gevşetin, tabla sallanabilir durumda olsun.
3.  **Kağıdı Yerleştirin:** Üreticinin verdiği kalibrasyon kağıdını ekranın üzerine koyun.
4.  **"Home" Komutunu Verin:** Tabla en alta inip kağıdı sıkıştıracak.
5.  **Tablayı Sabitleyin:** Tabla kağıdın üzerine tam bastığında, elinizle hafifçe bastırırken vidaları sıkın.
6.  **"Z=0" Yapın:** Menüden "Set Z=0" diyerek makineye "Burası sıfır noktası" deyin.

## Adım 2: Reçineyi Hazırlama ve Dökme

Şişeyi elinize alın. Çalkalayın. Ama öyle böyle değil, **en az 1 dakika** boyunca iyice çalkalayın. Reçinenin pigmentleri dibe çöker, çalkalamazsanız baskınız başarısız olur.

Reçineyi hazneye (Vat) dökerken "MAX" çizgisini geçirmeyin. Taşan reçine LCD ekranın içine sızarsa, yazıcınız çöp olabilir (veya pahalı bir ekran değişimi gerekir).

## Adım 3: İlk Baskı ve Heyecanlı Bekleyiş

USB bellekteki test dosyasını seçin ve başlatın.
SLA yazıcılar sessiz çalışır. İlk 30 dakika hiçbir şey göremezsiniz çünkü baskı tablanın altında oluşur. Sadece "dıt-dıt" sesi duyarsınız. Bu ses, tablanın her katmanda yukarı kalkıp reçineyi sıyırma sesidir ve **iyi bir sestir.**

## Adım 4: "Pis" İşler: Yıkama ve Kürleme

Baskı bitti, tabla yukarı kalktı. Üzerinde harika (ama vıcık vıcık reçine kaplı) bir model asılı duruyor.

**Sakın Çıplak Elle Dokunmayın!**
1.  **Sökme:** Eldivenle tablayı çıkarın. Metal spatula ile modeli kazıyarak alın (Dikkat: Tablayı çizmeyin, modeli fırlatmayın).
2.  **Yıkama (Wash):** Modeli içi İzopropil Alkol dolu bir kaba atın. Fırçayla nazikçe yıkayın veya bir "Wash & Cure" makinesi kullanın. Üzerindeki tüm sıvı reçine gitmeli.
3.  **Kürleme (Cure):** Yıkanmış model hala yumuşaktır. Onu UV ışığı altında sertleştirmeniz gerekir. Güneşe koyabilirsiniz (bedava ama yavaş) veya UV Kürleme makinesi kullanabilirsiniz (hızlı ve net).

![Bir yıkama ve kürleme istasyonunun içinde dönen ve UV ışığı alan bir 3D model](/images/sla-wash-cure.jpg "Yıkama ve kürleme, baskınızın gerçek potansiyelini ortaya çıkarır.")

{{< success-story-box title="✨ Kendi Acemiliğim: Beyaz Lekelerin Sırrı" >}}
İlk reçine baskımda o kadar heyecanlıydım ki, modeli alkolden çıkarır çıkarmaz, kurumadan direkt UV ışığının altına koydum. Sonuç? Modelin üzerinde beyaz, kireç gibi lekeler oluştu ve detaylar kapandı. O gün öğrendim: Yıkamak yetmez, model tamamen **kurumadan** kürleme yapılmaz!
{{< /success-story-box >}}

## Sonuç: Artık Bir "Simyacı"sınız

Tebrikler! Kimyasal süreçleri yönettiniz, evi batırmadan (umarım) ilk baskınızı aldınız. O elinizdeki pürüzsüz model, FDM ile asla alamayacağınız bir kalitede.

Ancak bu macera burada bitmedi. Evinizde kimyasal maddelerle ve yüksek sıcaklıklarla çalışıyorsunuz. Peki, uzun vadede bu cihazlarla yaşamak ne kadar güvenli? Yangın riski var mı? O kokular zararlı mı?

### Yolculuğun Bir Sonraki Durağı

Yazıcıyı kurduk, bastık. Ama gece çalışırken içim rahat etmiyor diyorsanız, sıradaki rehber tam size göre.

<div class="post-cta-box">
<h3>Sırada: 3D Yazıcı Güvenliği</h3>
<p>Termal kaçak nedir? Reçine buharı zehirler mi? Yangın ve sağlık risklerine karşı almanız gereken 5 hayati önlem.</p>
<a href="{{< ref "posts/3d-yazici-guvenligi-rehberi.md" >}}" class="cta-button">Güvenlik Rehberine Git →</a>
</div>