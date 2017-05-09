---
layout: post
title: Ağ Uygulamaları
excerpt:
categories: articles
comments: true
share: true
---
<span></span>

## İÇERİK

<li> <a href="#windows-soket-uygulamalari">Windows Soket Uygulamaları</a></li>
<li> <a href="#netbios-uygulamalari">Netbios Uygulamaları</a> </li>




## <a id="windows-soket-uygulamalari">Windows Soket Uygulamarı</a>

Bu uygulamalar hem internet üzerinde hem de windows işletim sitemleri arasında kullanılmaktadır.

**ping:** Bilgisayarlar ya da aygıtlar arası bağlantı kontrolünü gerçekleştirmek için kullanılan komuttur.

**ipconfig:** Bilgisayarımıza ait olan TCP/IP bilgilerini listeler. Ip adresimiz, alt ağ maskemiz ve varsa varsayılan ağ geçidini getirir. Daha detaylı bilgi görüntülemek için **ipconfig /all** komutunu kullanırız. Ek olarak MAC adresi, host adımız, DNS sunucu adresi, DHCP sunucu adresi vs. bilgileri gösterir.

**tracert:** Bir adrese hangi yönlendiriciler üzerinden geçilerek ulaşılıdığını listeler.


### <a id="netbios-uygulamalari">Netbios Uygulamaları</a>

Sadece windows işletim sistemleri arasında kullanılırlar.

**net start:** İşletim sistemi üzerinde bulunan bir servisi başlatmak için kullanılır.

**net stop:** İşletim sistemi üzerinde bulunan bir servisi durdurmak için kullanılır.

**net view:** Ağ içerisinde bulunan bir bilgisayar üzerindeki paylaştırılmış olan kaynakları listelemek için kullanılır.

**net share:** Kendi bilgisayarımız üzerinde bulunan paylaştırılmış kaynakları görüntülemek için kullanıldığı gibi, aynı zamanda bilgisayarımızdaki bir klasörü ya da yazıcıyı da paylaşıma açmak için de kullanılır.

**net send:** Ağ üzerindeki bir bilgisayara komut satırı üzerinden mesaj göndermek için kullanılır.

**net use:** Ağ üzerindeki bir bilgisayarda bulunan paylaştırılmış herhangi bir kaynağı bilgisayarımıza bağlamak için kullanılır. Bağlanan kaynak bilgisayarımızda Computer içerisinde bir disk sürücüsü şeklinde yer alacaktır.

Örnek Kullanımlar:

- ping 192.168.2.1
- ipconfig /all
- tracert www.yasinbaran.com
- net start dhcpserver
- net stop dnsserver
- net view 192.168.2.1
- net share
- net send pcadi selam!!
	net use k: \\yasinbaran\CİHAD (yasinbaran isimli bilgisayar üzerinde bulunan CİHAD isimli paylaştırılmış ağ kaynağını bilgisayarımıza bağlanmasını sağlar.)



Yazımı burada sonlandırıyorum, umarım faydalı olmuştur.

Saygılarımla.


Kaynak: [Windows Server Sistem Yönetimi Kitabı](https://www.linkedin.com/pulse/windows-server-sistem-y%C3%B6netimi-cilt-i-kitab%C4%B1m%C4%B1z-%C3%A7ikti-mesut-aladag?published=u) 
