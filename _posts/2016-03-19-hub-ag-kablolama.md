---
layout: post
title: HUB-Ağ Kablolama (Kablo Çeşitleri)
excerpt:
categories: articles
comments: true
share: true
---
<span></span>

## İÇERİK

<li> <a href="#hub">HUB</a></li>
<li> <a href="#ag-kablolamasi">Ağ Kablolaması</a> </li>
<li> <a href="#sinyal-iletim-metotlari">Sinyal İletim Metotları</a> </li>


## <a id="hub">HUB</a>

İki ya da daha fazla bilgisayarın birbirleri ile haberleşmesini sağlayan merkezi bağlantı komponentine hub adı verilir. 


<figure>
        <img src="http://yasinbaran.github.io/images/my-images/bilgisayar-aglari/10.jpg">
</figure>


Hub’lar üç çeşittir:

- Aktif Hub
- Pasif Hub
- Hybrid Hub

**Aktif Hublar**

Kendilerini gelen sinyali güçlendirerek hedefe tekrar gönderirler. Bundan dolayı **aktif hub** adını alırlar.  **Multiport repeater** da denilmektedir. Elektrik ile çalışırlar. Bağlantı portu sayısına göre ve veri iletim hızlarına göre çeşitlerine ayrılırlar. Bağlantı portuna göre 4’lü 8’li 16’lı gibi kategorilere ayrılırken, hızlarına göre 10’luk (10 Mpbs) 100’lük (100 Mpbs) şeklinde sınıflandırılırlar.

**Pasif Hublar**

Elektrik enerjisi olmadan çalışabilirler. Sadece bağlantı noktası görevindedirler. Sinyal güçlendirme özellikleri yoktur. Gelen sinyali iletken özelliği ile diğer tarafa geçirirler.

**Hybrid Hublar**

Farklı tipte kabloların kullanıldığı gelişmiş hub’lardır.
 
<figure>
        <img src="http://yasinbaran.github.io/images/my-images/bilgisayar-aglari/11.jpg">
</figure>


### <a id="ag-kablolamasi">Ağ Kablolaması</a>

Bilgisayarların birbiri ile sinyal iletişimini gerçekleştirmeleri için kablo kullanmaları gerekir. Topolojileri birbirlerinden ayıran önemli farklardan birisi de kullandıkları kablo tipidir.

**Kablo Çeşitleri**

Günümüzde çok sayıda kablo çeşidi üretilmektedir. Bilgisayar ağlarında kullanılan üç tip kablo çeşidi vardır.

- Koaksiyel Kablo (Coaxial Cable)
- Bükümlü Kablo (Twisted Pair Cable)
- Fiber Optik Kablo (Fiber Optic Cable)

**Koaksiyel Kablo (Coaxial Cable)**

Günümüzde neredeyse hiç kullanılmayan ancak eski ağlarda en yaygın olarak kullanılan kablo türüdür. Ucuz, hafif ve kurulumu kolay olması yaygın kullanımını sağlayan sebeplerdendir. Bus topolojisine sahip ağlarda kullanılır. Merkezde bir bakır tel ve onun etrafını kaplayan bir yalıtkan tabaka, yalıtkan tabakanın üstünde de metalden bir tel örgü koruması ve en dışta da kauçuktan yapılmış yalıtkan korumadan oluşur. Bilgiyi en içteki bakır tel taşır. Metal örgü, bakır tel için topraklama görevi görür ve **sinyal çakışmalarını (crostalk)** önler. **Crosstalk** yanyana iki kablodan, birinden diğerine sinyal taşması olayıdır. Bakır tel ve metal örgü birbirine temas etmemelidir. Ederse **kısa devre (short circuit)** meydana gelir ve sinyal bozulur. Koaksiyel kablo **sinyal bozulması (attenuation) karşı bükümlü (twisted-pair)** kabloya göre oldukça dayanıklıdır.


<figure>
        <img src="http://yasinbaran.github.io/images/my-images/bilgisayar-aglari/12.jpg">
</figure>


**Bükümlü (Twisted Pair) Kablolar**

Birbirinden yalıtılmış ve birbirine örülmüş iki bakır telden oluşmaktadır. Teller kablo içerisinde helix şeklinde birbirine sarılmış durumdadırlar. Bunun sebebi kablo içerisinde ki tellerin birbirinden etkilenmemeleridir. İkiye ayrılır:

**1.Korumasız Bükümlü Kablo**

En sık kullanılan kablolamalardan biridir. En fazla 100 metre mesafeye kadar sinyal bozulmadan taşınabilir. Kendi içerisinde altıya ayrılır. CAT1, CAT2, CAT3, CAT4, CAT5, CAT6 olarak. CAT1 telefon kablolarında kullanılan çeşittir. Bağlantı için RJ-11 konnektör kullanılır. 

Korumasız kabloların en büyük problemi crosstalk (sinyal taşması)’tır. Bükümlü olmasının sebebi de sinyal taşmasını önlemektir.

**2.Korumalı Bükümü Kablo**

Her kablo çifti ve kablonun kendisi için bir kaplama kullanılır. Bundan dolayı sinyal taşmasından en az zarar görmek üzere tasarlanmıştır. Aynı zamanda yüksek mesafelere veri transferinide desteklemektedir.


<figure>
        <img src="http://yasinbaran.github.io/images/my-images/bilgisayar-aglari/13.jpg">
</figure>


**Fiber Optik (Fiber Optic) Kablolar**

Merkezde cam bir tüpten oluşan fiber optiklerin ayrıca merkezi plastikten oluşan çeşitleri de vardır. Çok pahalı bir kablo türüdür. 100 Mpbs ile 1000 Mpbs arası veri iletim hızlarına kadar destekler. Elektrik ile iletim yapmadığından crosstalk etkisinden zarar görmez. Bir kablo parçası en fazla 2800 metreye kadar iletimi destekler. Fiber optik kablo pahalıdır ve bakımını yapacak teknik ekibin iyi bir eğitim alması gerekir.


<figure>
        <img src="http://yasinbaran.github.io/images/my-images/bilgisayar-aglari/14.jpg">
</figure>


Kablo seçerken dikkat etmemiz gerekenler:

- Ağ trafiğinin yoğunluğu
- Ağ güvenlik ihtiyaçları
- Kablonun uzaması gereken mesafe
- Kullanılabilecek kablo seçenekleri
- Ağ kablo alt yapısı için ayrılan bütçe


### <a id="sinyal-iletim-metotlari">Sinyal İletim Metotları</a>

İletişimde kullanılabilecek en düşük ve en yüksek frekanslar arasında kalan aralığa **bant genişliği (bandwith)** adı verilmektedir. 

**Baseband Mimarisini Kullanan İletim Metodu**

Sadece bir tek kanaldan dijital sinyallerin kullanılmasına izin veren haberleşme standardıdır. Baseband iletişim yapan bir ağ üzerinde tüm aygıtlar çift yönlü iletim yapmaktadırlar. Bazıları hem yayın yaparken hem de veri alabilirler. Bu mimaride çalışan sistemler zayıflayan sinyalleri güçlendirmek için repeater adı verilen güçlendiriciler kullanırlar.

**Broadband Mimarisini Kullanan İletim Metodu**

Analog sinyaller kullanırlar. Sadece belli frekans aralıklarını kullanmaktadırlar. Sinyaller kablo üzerinden aralıksız eloktromanyetik veya optik dalgalar halinde ilerlerler. Bu mimariye örnek olarak evlerimizde ki kablolu televizyonları verebiliriz. Aynı anda pek çok kanal tek kablo üzerinden yayın yapmaktadır ve seyretmek istediğimiz kanalı seçerek seyrederiz.



Yazımı burada sonlandırıyorum, umarım faydalı olmuştur.

Saygılarımla.


Kaynak: [Windows Server Sistem Yönetimi Kitabı](https://www.linkedin.com/pulse/windows-server-sistem-y%C3%B6netimi-cilt-i-kitab%C4%B1m%C4%B1z-%C3%A7ikti-mesut-aladag?published=u) 
