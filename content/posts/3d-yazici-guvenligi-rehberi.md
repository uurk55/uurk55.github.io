---
title: "3D Yazıcı Güvenliği Rehberi: Evde ve Atölyede Dikkat Edilmesi Gerekenler"
date: 2025-07-25T10:00:00+03:00
featured: false
draft: false
description: "Evinizin ortasında 260 dereceye ısınan bir cihaz çalışıyor. Peki ne kadar güvendesiniz? Termal kaçak, zehirli gazlar ve 'akıllı priz' gibi hayat kurtaran önlemler."
tags: ["3D Yazıcı Güvenliği", "Thermal Runaway", "Yangın Riski", "Reçine Zehirlenmesi", "ABS Kokusu", "Atölye Güvenliği", "Baskı Ortamı"]
categories: ["Temel Bilgi ve Kurulum"]
faz: ["Faz 1"]
series: ["3D Baskı Temelleri Serisi"]
author: "Uğur Kapancı"
showToc: true
TocOpen: true
comments: true
ShowReadingTime: true
ShowPostNavLinks: true
cover:
    image: "/images/guvenlik-rehberi-cover.jpg"
    alt: "Duman dedektörü ve yangın söndürücü yanında çalışan bir 3D yazıcı"
    caption: "Güvenlik, kaza olmadan önce alınan önlemdir. Sonrası pişmanlıktır."
    relative: false
---

Dürüst olalım: 3D yazıcıyı kurduk, ilk baskıyı aldık ve o hipnotize edici mekanik hareketi izlerken aklımıza gelen son şey "Güvenlik" oldu.

Ama size bir gerçeği hatırlatayım: Şu an odanızda, ucu 260 dereceye (fırınınızdan daha sıcak!), tablası 100 dereceye ısınan ve saatlerce gözetimsiz çalışan bir cihaz var.

Ben ilk Ender 3'ümü aldığımda, onu çalışma masamın altına koyup gece boyu çalıştırdım. Sabah uyandığımda odada ağır bir plastik kokusu ve baş ağrısı vardı. O gün anladım ki; bu makineler oyuncak değil, birer **mikro fabrikadır** ve her fabrika gibi güvenlik protokolleri gerektirir.

Bu rehberde sizi korkutmak istemiyorum ama "Bana bir şey olmaz" dememeniz için, evinizi ve sağlığınızı koruyacak hayati önlemleri anlatacağım.

## 1. Yangın Riski: "Termal Kaçak" (Thermal Runaway) Nedir?

Bu terimi sık duyacaksınız. Termal Kaçak, yazıcının sıcaklık sensörünün yerinden çıkması veya bozulması durumunda, yazıcının "Hala ısınamadım" sanarak ısıtıcıya sürekli güç vermesi ve sonunda kendini (ve evi) yakmasıdır.

*   **Benim Önlemim:** Yazıcınızın yazılımında (Marlin/Klipper) bu korumanın açık olduğundan emin olun.
*   **Akıllı Priz Hayat Kurtarır:** Ben tüm yazıcılarımı, telefondan kontrol edilebilen bir **Akıllı Priz'e (Smart Plug)** bağlarım. Evden çıktığımda uzaktan kamerayla bakar, bir terslik görürsem elektriği telefondan keserim. Bu 300 liralık parça, binlerce liralık hasarı önler.

![3D yazıcının üzerine monte edilmiş bir duman dedektörü](/images/smoke-detector.jpg "Basit bir duman dedektörü, en ucuz sigortanızdır.")

## 2. Görünmez Düşman: Hava Kalitesi ve Zehirli Gazlar

FDM yazıcılarda **PLA** basarken çıkan koku şekerli ve zararsızdır (mısır nişastası). Ancak işler **ABS** veya **ASA**'ya gelince değişir.

*   **ABS/ASA:** Eritildiğinde havaya "Stiren" gazı yayar. Bu gaz kanserojendir ve baş ağrısı yapar. Ben bir kere havalandırmasız odada ABS bastım, o baş ağrısını asla unutmam.
*   **SLA (Reçine):** Reçine buharı (VOC) sessizce ciğerlerinize işler.

**Çözüm:**
1.  ABS/ASA basacaksanız yazıcınız ya kapalı kasa olsun ya da penceresi açık bir odada basın.
2.  SLA yazıcı kullanıyorsanız, odada aktif hava sirkülasyonu şarttır.

## 3. Mekanik Tehlikeler: Parmaklar ve Yanıklar

Yazıcı çalışırken "Şuradaki çapağı elimle alıvereyim" dediğiniz an, nozzle'ın elinize değmesiyle derinizin yanması bir olur. 220 derece şaka değildir.

Ayrıca hareket eden eksenler, özellikle çocuklar ve evcil hayvanlar için büyük risktir.
*   **Kural:** Yazıcı çalışırken, nozzle sıcakken asla elinizi tabla alanına sokmayın. Uzun cımbız kullanın.
*   **Kediler:** Kediler sıcak tablaları sever. Eğer kediniz varsa, yazıcıyı mutlaka kapalı bir kabine (Enclosure) alın. Tüyler fana kaçabilir veya kedi yanabilir.

## 4. Elektrik Tesisatı: "Kablo Isındı mı?"

Özellikle eski veya ucuz kitlerde, anakart üzerindeki güç girişleri (klemensler) gevşeyebilir. Gevşek kablo = Ark (Kıvılcım) = Yangın.

{{< success-story-box title="✨ Benim Ucuz Atlattığım An" >}}
Bir gün baskı sırasında yanık plastik kokusu aldım. Nozzle sandım ama koku anakarttan geliyordu. Kutuyu açtığımda, ısıtıcı tablanın kablosunun girdiği yeşil soketin eridiğini ve karardığını gördüm. Eğer evde olmasaydım, o erime yangına dönüşebilirdi.
**Ders:** İlk 1 ay, belirli aralıklarla kabloları ve soketleri kontrol edin. Isınma veya kararma varsa hemen durdurun.
{{< /success-story-box >}}

## 5. Uğur Hoca'nın "Güvenli Alan" Kontrol Listesi

Baskıya başlamadan önce şu 5 maddeye "Evet" diyor musunuz?

1.  ✅ Yazıcının çevresinde yanıcı madde (perde, kağıt havlu, alkol şişesi) yok.
2.  ✅ Oda havalandırılıyor (Özellikle Reçine/ABS ise).
3.  ✅ İlk katman yapışana kadar başında bekledim.
4.  ✅ Duman dedektörü çalışıyor (Yazıcının tepesine pilli bir dedektör yapıştırın).
5.  ✅ Evde yoksam kamera ile izleyebiliyorum ve elektriği kesebilirim.

## Sonuç: Korkmayın, Saygı Duyun

Bu yazı gözünüzü korkutmasın. Araba kullanmak da tehlikelidir ama kurallara uyarsanız sizi hedefe götürür. 3D yazıcılar da böyledir. Onlara bir oyuncak gibi değil, güçlü bir üretim aracı gibi davranırsanız, size harika hizmet ederler.

Güvenliği sağladık, makineyi kurduk. Ama bir sorun var... Bastığınız küp 20mm olması gerekirken 19.5mm çıkıyor. Daireler yumurta gibi basılıyor. Makine güvenli ama "doğru" basmıyor.

Neden? Çünkü kalibrasyon yapmadık.

### Yolculuğun Bir Sonraki Durağı

Yazıcıyı sadece "seviyelemek" (leveling) yetmez. E-step, Akış (Flow) ve Boyut (Dimensional) kalibrasyonlarını yaparak o milimetrik hassasiyeti yakalamamız lazım.

<div class="post-cta-box">
<h3>Sırada: Mükemmel Baskılar İçin Kalibrasyon Rehberi</h3>
<p>Baskılarınız ölçü tutmuyor mu? Yüzeyler pürüzlü mü? Yazıcınıza ince ayar çekmenin ve "E-Step" kalibrasyonunun tam zamanı.</p>
<a href="{{< ref "posts/3d-yazici-kalibrasyonu-rehberi.md" >}}" class="cta-button">Kalibrasyon Rehberine Git →</a>
</div>