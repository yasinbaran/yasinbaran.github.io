---
layout: post
title: Ağ Aygıtları
excerpt:
categories: articles
comments: true
share: true
---
<span></span>

## İÇERİK

<li> <a href="#ag-aygitlari">Ağ Aygıtları</a></li>



## <a id="ag-aygitlari">Ağ Aygıtları</a>


**1)	Güçlendiriciler (Repeater)**

Kablo üzerinde zayıflayan sinyallerin güçlendirilerek hedef adrese sinyallerin ulaşmasını sağlayan aygıttır. Kaynak adres ile hedef adres arası kullanılan kablonun taşıma mesafesini uzaklık aşıyorsa güçlendirici kullanılmalıdır.


<figure>
        <img src="http://yasinbaran.github.io/images/my-images/bilgisayar-aglari/18.jpg">
</figure>


**2)	Köprü (Bridge)**

Farklı topolojiler arasında ilişki kurulmasını sağlar. Ağ ortamında ki darboğazları (bottleneck) azaltır. Yönlendirilemeyen protokoller ile çalışırlar. OSI modeli içerisinde veri bağlantı katmanına ait olan medya erişim kontrolü alt katmanında işlem yapar. Üzerinde haberleştiği ağ segmentlerine ait adreslerin tutulduğu bir **yönlendirme tablosu (routing table)** bulunur. 


<figure>
        <img src="http://yasinbaran.github.io/images/my-images/bilgisayar-aglari/19.jpg">
</figure>


**3)	Yönlendirici (Router)**

Farklı segmentte bulunan bilgisayarların haberleşmesini sağlar. Yönlendirilebilen protokoller kullanır.(TCP/IP gibi) Farklı subnetler arası broadcast trafiğinin geçişini önler. OSI modeli içerisinde ağ katmanında işem görür. Verinin karşı tarafa gidip gitmediğinin kontrolünü yapar. Üzerinde yönlendirme tablosu bulunur. Statik ve dinamik olmak üzere iki tip yönlendirme yaparlar. Statik yönlendirme yönlendirici üzerinde ağ adreslerinin elle girilmesi ile oluşturulur. 

Dinamik yönlendirme ise, yönlendirme protokolleri konfigure edilerek otomatik yönlendirme tablosunu oluşturan yönlendirme tipidir. 


<figure>
        <img src="http://yasinbaran.github.io/images/my-images/bilgisayar-aglari/20.jpg">
</figure>



**4)	Köprü Yönlendirici (Brouter)**

Yönlendirilebilir ve yönlendirilemez protokoller arası iletişim kurmayı sağlar. OSI modeli içerisinde ağ katmanında işlem görür. Ağ geçidine fonksiyon olarak benzer ancak daha ucuzdur. Farklı ağ teknolojileri arasında haberleşmeyi sağlar. 


<figure>
        <img src="http://yasinbaran.github.io/images/my-images/bilgisayar-aglari/21.jpg">
</figure>



**5)	Ağ Geçidi (Gateway)**

Farklı protokoller arası çevirim işlemi yapar. OSI model içerisinde uygulama katmanında işlem yapar. Farklı ağ teknolojileri arasında haberleşmeyi sağlar. 


<figure>
        <img src="http://yasinbaran.github.io/images/my-images/bilgisayar-aglari/22.jpg">
</figure>




Yazımı burada sonlandırıyorum, umarım faydalı olmuştur.

Saygılarımla.


Kaynak: [Windows Server Sistem Yönetimi Kitabı](https://www.linkedin.com/pulse/windows-server-sistem-y%C3%B6netimi-cilt-i-kitab%C4%B1m%C4%B1z-%C3%A7ikti-mesut-aladag?published=u) 
