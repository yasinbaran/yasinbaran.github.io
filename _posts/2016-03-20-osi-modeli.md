---
layout: post
title: OSI Modeli
excerpt:
categories: articles
comments: true
share: true
---
<span></span>

## İÇERİK

<li> <a>OSI Modeli</a></li>



## <a>OSI Modeli</a>

Ağ haberleşmesi için uluslararası bir standarttır. 1984 yılında **ISO (International Standarts Organizations)** tarafından **OSI (Open System Interconnection)** ismiyle tanımlanmıştır.

Ağ haberleşmesini yedi katman içerisinde bölümleyerek bir tanımlama yapar. Her katman farklı ağ aktiviteleri ve iletişim kuralları içerir.


<figure>
        <img src="http://yasinbaran.github.io/images/my-images/bilgisayar-aglari/16.jpg">
</figure>


**1)	Application Layer (Uygulama Katmanı)**

 Uygulamaların ağ servislerine erişimini ve uygulamalar arası yönetimi sağlar. Doğrudan kullanıcı uygulamalarını çalıştıran servisleri içerir. Genel ağ erişimini, akış kontrolünü ve hata kontrollerini de tutar. 

**2)	Presentation Layer (Sunum Katmanı)**

 Ağ içerisinde ki bilgisayarlarda karşılıklı olarak veri alışverişindeki formatı belirler. Bu katman **ağ çevirici (network translator)** olarak da isimlendirilir. **Redirector** isimli uygulama parçacığı da bu katmanda çalışır. **Redirector**, kullanıcı tarafından tetiklenen işlemlerin yerel bilgisayarı mı yoksa ağ üzerideki bir başka bilgisayarı mı ilgilendirdiğine karar verir.

**3)	Session Layer (Oturum Katmanı)**

 Güvenlik ile ilgili işlemler bu katmanda yönetilir. İletişime geçecek iki bilgisayar arasında bir iletişim kanalı oluşturur.

**4)	Transport Layer (Taşıma Katmanı)**

 Akış ve hata kontrolü, paketlerin alınması ve iletimi ile ilgili problemlerin çözümünü sağlar. Paketlerin hatalı teslim edilip edlimediğinin, pakette değişiklik olup olmadığının ve paketlerde bir kayıp olup olmadığının kontrolünü yapar.

Uzun mesajların paketlere bölünmesini ve küçük paketlerin tek bir paket içerisinde toplanmasını sağlar. Taşıma katmanında ki veri bloklarına **segment (bölüm)** adı verilir. 

Bilgiyi alan tarafta mesajların iletilmesini, orjinal mesajların paketlere bölündükten sonra tekrar birleştirilmesini sağlar. İletilen paketlerin kabul edildiğinin onayını gösterir.

**5)	Network Layer (Ağ Katmanı)**

 Mesajların adreslenmesinden sorumludur. Mantıksal adresi fiziksel adrese çevirir. Kaynak adresten hedef adrese ulaşırken kullanılacak yolu belirler. Verilerin ağ üzerinde hangi mevkilerde yer alacağının ve servis önceliklerinin kararını verir. Ağ üzerindeki trafik problemlerinin yönetimini üstlenir. Ağ katmanındaki veri bloklarına **packet (paket)** adı verilmektedir.

Hedef bilgisayar, kaynak bilgisayarın gönderdiği büyük paketlere cevap vermezse, ağ katmanı bu büyük verileri küçük parçacıklara ayırır.

**6)	Data Link Layer ( Veri Bağlantı Katmanı)**

 Veri çerçevelerini ağ katmanından fiziksel katmana gönderir. Verilerin yerleştirileceği organize edilmiş veri bloklarına **frame (çerçeve)** adı verilir.

Gönderilen paketin içeriği üzerinde işletim sistemi matematiksel bir işlem gerçekleştirir. Bu işleme **CRC (Cyclical Redundancy Check)** adı verilir. Her pakette **CRC** sonucu farklı çıkar. Paketi alan bilgisayar paketi aldıktan sonra paket üzerinde **CRC** işlemini tekrar yapar ve eğer sonuç aynı ise paketi kabul eder. Eğer sonuç farklı çıkarsa veri bozulmuş demektir ve veri bağlantı katmanı, taşıma katmanını bu durumdan haberdar ederek paketin tekrar gönderilmesini sağlar.

Veri katmanında iki alt tabaka bulunmaktadır.

- **Mantıksal Bağlantı Kontrolü (Logical Link Control (LLC)):** LLC veri bağlantısı işlemini kontrol eden bir alt katmandır.

- **Medya Erişim Kontrolü (Media Access Control (MAC)):** Bilgisayar içerisindeki fiziksel katmanın ağ kartına erişimini sağlar.

**7)	Physical Layer (Fiziksel Katman)**

Sinyalin dijital anlamının bozulmamasını sağlar. Sinyallerin kablo üzerine gönderilme işlemini yapar.



Yazımı burada sonlandırıyorum, umarım faydalı olmuştur.

Saygılarımla.


Kaynak: [Windows Server Sistem Yönetimi Kitabı](https://www.linkedin.com/pulse/windows-server-sistem-y%C3%B6netimi-cilt-i-kitab%C4%B1m%C4%B1z-%C3%A7ikti-mesut-aladag?published=u) 
