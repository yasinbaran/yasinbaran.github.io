---
layout: post
title: Ağ Kartı - Kablosuz Ağlar
excerpt:
categories: articles
comments: true
share: true
---
<span></span>

## İÇERİK

<li> <a href="#ag-karti">Ağ Kartı (Ethernet)</a></li>
<li> <a href="#kablosuz-aglar">Kablosuz Ağlar (Wireless Networks)</a> </li>


## <a id="ag-karti">Ağ Kartı (Ethernet)</a>

Ethernet kartı aynı zamanda ağ arabirim kartı (network interface card) olarak da bilinir. Bilgisayar ile ağ kablosu arasındaki fiziksel arabirime verilen isimdir. Her bilgisayarda uygun boş slotlara takılır. Kart takıldıktan sonra ağ kablosu kartın bağlantı yuvasına takılarak bilgisayarın ağ ile bağlantısı sağlanır.

**Genel Özellikleri:**

- Bilgisayar içerisinde işlenen sinyallerin ağ kablosuna getirilmesi
- Sinyallerin diğer bilgisayarlara gönderilmesi
- Kablo sistemleri ile bilgisayarlar arası sinyal akışını sağlaması

Ağ kartı bilgiyi gönderen bilgisayarda bilgiyi kabloya yerleştirirken, alan bilgisayar tarafında da kablodan gelen bilgiyi CPU’da işlenecek şekilde byte’lara dönüştürür. Yani Ethernet kartı bilgiyi göndermeden önce diğer bilgisayarların anlayabileceği dile çevirmeyi sağlar. Bilgi bilgisayar içerisinde **BUS** adı verilen yollardan taşınır. 

Ethernet kartı, bilgisayarın içerisinde kendisine gelen dijital sinyalleri, elektiriksel ve optik sinyallere dönüştürerek ağ kablosundan taşınmasını sağlar.Bu dönüştürme işleminden sorumlu aygıta **transceiver (dönüştürücü)** adı verilir.

Ethernet kartı aynı zamanda sinyalin gideceği adreside belirler. Her Ethernet kartının kendine özgü MAC adresi olarak isimlendirilen bir adresleme şekli vardır. **MAC** adresleri dünya üzerinde tektir.
 
##Konfigürasyon Seçenekleri ve Ayarları

Ethernet kartları daha verimli ve uygun çalışması için ayarlanması gereken konfigurasyon ayarlarına sahiptir.

**1.	Interrupt (IRQ) (Kesme İsteği)**

Bilgisayar üzerine takılı olan her aygıtın kendisine ait kullanmış olduğu bir iletim yolu vardır. Bu iletim yolları IRQ 1 – IRQ 5 arası numaralandırılır. Bu numaralar vasıtasıyla işlemcinin aygıtları tanınması sağlanmaktadır. Eğer iki aygıt aynı numarayı kullanıyorsa çakışma meydana gelir ve aygıtlar işlemci tarafından algılanamaz.

**2.	Base I/O Port Address**

Aygıtların işlemci ile iletişim sağlayacakları kanalın adresine verilen isimdir.

**3.	Base Memory Address**

Aygıtın işlemek üzere hafızada bekleteceği verilerin hafıza üzerinde nerede bekletilecekleridir.

**4.	Transceiver (Alıcı-Verici)**

Dijital sinyalleri analog, elektriksel veya optik sinyallere dönüştüren aynı şekilde analog, elektriksel veya optik sinyalleri de dijital sinyallere dönüştüren çeviricilere **transceiver** adı verilir.


### <a id="kablosuz-aglar">Kablosuz Ağlar (Wireless Networks)</a>

Kablolama yapılmadan ve kablo kullanmadan bilgisayarların birbirleri ile iletişiminin sağlandığı yapılardır. 

Kullanıcılar kablosuz yerel ağlar sayesinde bulundukları ortamlarda diğer sistemlere sürekli bağlantı sağlayabilirler. Kablosuz ağlar sayesinde, laptomuz ile kablo çıkartıp takmadan bina içerisinde istediğimiz mekana gidebiliriz. Kablosuz yerel ağlar herhangi bir kablolamaya gerek kalmadan kolayca büyütülebilir ve taşınabilirler. 


<figure>
        <img src="http://yasinbaran.github.io/images/my-images/bilgisayar-aglari/15.jpg">
</figure>


Kablolu ağlarda, bilgisayarlar ve diğer haberleşme aygıtları birbirlerine hub’lar ya da switch’ler vasıtasıyla bağlantı sağlarlar. Kablosuz yerel ağlarda ise hub’lar ve switch’lerin yerini **Access Points (Erişim Noktası)** adı verilen cihazlar alır. Access Point’ler aynı zamanda kablolu ağ ve kablosuz ağın birleşme noktasıdır.

Acces point’ler sayesinde kablosuz ağın iletim mesafesi büyütülebilir. 40 metreye kadar 11 Mpbs, 100 metreye kadar 1 Mpbs hızında veri aktarımı sağlarlar.


Yazımı burada sonlandırıyorum, umarım faydalı olmuştur.

Saygılarımla.


Kaynak: [Windows Server Sistem Yönetimi Kitabı](https://www.linkedin.com/pulse/windows-server-sistem-y%C3%B6netimi-cilt-i-kitab%C4%B1m%C4%B1z-%C3%A7ikti-mesut-aladag?published=u) 
