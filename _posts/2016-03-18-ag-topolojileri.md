---
layout: post
title: Ağ Topolojileri
excerpt:
categories: articles
comments: true
share: true
---
<span></span>

## İÇERİK

<li> <a href="#ag-topolojileri">Ağ Topolojileri</a></li>
<li> <a href="#bus-topoloji">BUS Topoloji</a> </li>
<li> <a href="#star-topoloji">Star Topoloji</a> </li>
<li> <a href="#ring-topoloji">Ring Topoloji</a></li>
<li> <a href="#star-bus-topolojisi">Star Bus Topoloji</a></li>
<li> <a href="#mesh-topoloji">Mesh Topoloji</a></li>


## <a id="ag-topolojileri">Ağ Topolojileri</a>

Bir ağ ortamında ki bilgisayarların, kabloların ve diğer bileşenlerin fiziksel görünümüne verilen isimdir. Topoloji, ağ mühendislerinin ağın tasarımı ve fiziksel yapısı için kullandıkları standart bir terimdir. Ağ tasarımında kullanılan diğer terimler:

- **Pysical Layout:** Fiziksel görünüm.

- **Design:** Ağ şemasının tasarımı veya dizaynı.

- **Diagram:** Ağ şemasının genel hatlarıyla şekil olarak dökülmüş hali veya diyagramı.

- **Map:** Ağ haritası.

Topoloji ağ içerisinde ki bilgisayarların nasıl haberleşeceğini de belirler.

**Standart Topolojiler**

Network tasarımlarında kullanılan dört adet temel topoloji vardır.

- BUS Topoloji
- Star Topoloji
- Ring Topoloji
- Mesh Topoloji

 Ortak kullanılan paylaşılmış bir kabloya bağlı aygıtların oluşturduğu yapıya **Bus topoloji**; bütün bilgisayarların hub veya switch isimli bağlantı elemanları üzerinden haberleştiği yapıya **Star topoloji**; dairesel olarak bütün bilgisayarların bir kablo üzerinden haberleşme yaptığı topolojiye **Ring topoloji**; ağ üzerinde ki her bilgisayarın birbirine ayrı bir kablo ile bağlantı yapıldığı topolojiye de **Mesh topoloji** adı verilmektedir. 

### <a id="bus-topoloji">BUS Topoloji</a>

Bilgisayarlar düz bir hat üzerinde birbirlerine bağlanmışlardır. En basit bağlantı yöntemidir.


<figure>
        <img src="http://yasinbaran.github.io/images/my-images/bilgisayar-aglari/4.jpg">
</figure>


Bus topolojide haberleşme mantığına bakacak olursak; aynı anda hattı sadece bir bilgisayar kullanabilir. Bilgisayarlar arası haberleşmede bilgiler kablo üzerinden eloktronik sinyaller olarak gönderilir.

**Sinyalin Gönderilmesi**

Bilgiler elektronik sinyal formatında gönderilir. Gönderilen sinyali sadece adreslenen bilgisayar alır. Diğer bilgisayarlar kendilerine gelen sinyali reddederler. Bus topolojide, ağ üzerinde aynı anda sadece bir bilgisayar sinyal gönderebilir. Ağa bağlı bilgisayar sayısı arttıkça ağın performansı düşer. Sinyal göndermek isteyen bilgisayarlar sıraya geçer, bu da veri yolunda yoğunluğa sebep olur.


**Sinyal Sıçraması (Signal Bounce)**

Kaynak bilgisayar sinyal gönderir, bu sinyal ağ üzerinde bir ucundan diğer ucuna doğru hareket eder. Sinyal kablonun ucuna ulaştığında eğer sonladırılmazsa, kablonun ucundan geri dönmeye çalışır. Sinyalin geri dönmesine, **sinyal sıçraması** denir. Sinyal sıçramasından dolayı ağ üzerinde sinyal çakışması meydana gelir ve sinyaller birbirlerini ortadan kaldırırlar. Bu durumda da bilgisayarlar arası haberleşme başarılı bir şekilde gerçekleşmez. Bu sorunu ortadan kaldırmak için, yani sinyallerin çakışmasını önlemek amacıyla, bus topolojiye sahip ağlarda, kablonun bağlı olduğu her iki uca **terminator** adı verilen sonlandırıcı takarak, sinyallerin dönüşü önlenir ve ağ üzerinde sorunsuz bir haberleşme olması sağlanır.


<figure>
        <img src="http://yasinbaran.github.io/images/my-images/bilgisayar-aglari/5.jpg">
</figure>


Bus topoloji de kullanılan barrel connector ve sinyal güçlendirici (repeater)’den de bahsedecek olursak; barrel connector, iki ayrı kabloyu birleştirmeye yarayan bir bileşendir; repeater ise kendisine gelen sinyali güçlendirerek hedefe gönderir.


### <a id="star-topoloji">Star Topoloji</a>


Tüm bilgisayarlar merkezi bir bileşene (hub veya switch) kablo ile bağlanmıştır. Bir bilgisayar başka bir bilgisayar ile haberleşmek için sinyal gönderdiği zaman, sinyal hub veya switch üzerinden geçerek, hedef bilgisayara ulaşır. Bu haberleşme hub ve switche göre farklılık gösterir. Eğer hub kullanılmışsa gönderen bilgisayardan gelen sinyal hub’ın bütün portlarına gönderilir. Sinyali sadece adreslenen bilgisayar alır. Bu haberleşme yöntemine broadcast (yayın) adı verilir. 



<figure>
        <img src="http://yasinbaran.github.io/images/my-images/bilgisayar-aglari/6.jpg">
</figure>


3 numaralı bilgisayarın 5 numaralı bilgisayara sinyal gönderdiği senaryoyu düşünelim. 3 numaralı bilgisayardan gelen sinyaller hub’a gider ve hub bu sinyalleri broadcast eder. Yani bütün bilgisayarlara yönlendirir. Sinyali sadece adreslenen 5 numaralı bilgisayar kabul eder. Diğer bilgisayarlar sinyali reddederler.

Herhangi bir bilgisayarın arızalanması, sistemde bir sorun oluşturmaz; fakat hub’ın bozulması sistemin haberleşmesini durdurur.

### <a id="ring-topoloji">Ring Topoloji</a>

Bilgisayarların haberleşmesi dairesel bir şekilde gerçekleşmektedir. Sinyaller saat yönünde dairesel (ring) şeklinde ilerler ve her bilgisayarın üzerinden geçerler. Bus topolojiden farkı ise her bilgisayar sinyalleri güçlendirerek gönderir.

Her bilgisayardan gelen kablolar merkezi bağlantı bileşeni üzerinde toplanır. Bütün mesajlar hedef bilgisayara gitmeden önce merkezi bağlantı bileşeni üzerinden geçmektedir.


<figure>
        <img src="http://yasinbaran.github.io/images/my-images/bilgisayar-aglari/7.jpg">
</figure>


Baktığımız zaman star topolojisine benzemektedir; fakat ring mantıksal bir döngüdür ve ring ifadesi sinyal akışının nasıl olduğunu ifade eder.

**Token Passing**

Ring topolojisinin haberleşme teknolojisine verilen isimdir. Sinyaller ring etrafında token adı verilen boş bir bilgi paketi tarafından taşınmaktadır. Bir bilgisayar başka bir bilgisayara sinyal göndereceği zaman token bu sinyali kaynak bilgisayardan alır ve hedef bilgisayara ulaştırır. Sinyalin karşı tarafa ulaştığı bilgisini kaynak bilgisayar aldıktan sonra token artık sistemde başka sinyalleri taşımak için boş olarak dolaşmaya devam eder.

Herhangi bir bilgisayarın arızalanması bütün ağ sisteminin çökmesine sebep olacaktır. Bunun için de token’ın bir özelliği bulunmaktadır. Token ağ üzerinde ki arızalı bilgisayarı tespit ettiği zaman ağdan düşürür ve sistem çalışmaya devam eder.

### <a id="star-bus-topoloji">Star Bus Topoloji</a>

Her ağ kendi içerisinde bir star topoloji yapısında çalışırken, hub’lar arasında ise bus topoloji yapısı vardır.


<figure>
        <img src="http://yasinbaran.github.io/images/my-images/bilgisayar-aglari/8.jpg">
</figure>


Bir bilgisayar arızalanırsa, diğer bilgisayarlar iletişime devam eder; fakat hub/switch’ler arızalanırsa, o hub/switch’e bağlı olan bilgisayarlarla iletişim kurulamaz. Diğer bilgisayarlar iletişime devam ederler.


### <a id="mesh-topoloji">Mesh Topoloji</a>

En sağlam ve sağlıklı olan topolojidir. Her bilgisayar bütün diğer bilgisayarlara ayrı kablo ile bağlanır. Eğer kablolardan biri arızalanırsa, diğer kablolar üzerinden trafiğin geçişi sağlanır. Çok fazla kablo masrafı olması ve karmaşıklığından dolayı yaygın olarak kullanılmamaktadır.

<figure>
        <img src="http://yasinbaran.github.io/images/my-images/bilgisayar-aglari/9.jpg">
</figure>


Yazımı burada sonlandırıyorum, umarım faydalı olmuştur.

Saygılarımla.


Kaynak: [Windows Server Sistem Yönetimi Kitabı](https://www.linkedin.com/pulse/windows-server-sistem-y%C3%B6netimi-cilt-i-kitab%C4%B1m%C4%B1z-%C3%A7ikti-mesut-aladag?published=u) 
