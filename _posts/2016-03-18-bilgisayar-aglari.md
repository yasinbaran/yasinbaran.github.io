---
layout: post
title: Bilgisayar Ağları
excerpt:
categories: articles
comments: true
share: true
---
<span></span>

## İÇERİK

<li> <a href="#ag-nedir">Ağ (Network) Nedir?</a></li>
<li> <a href="#nicin-kullanilir">Bilgisayar Ağları Niçin Kullanılır?</a> </li>
<li> <a href="#ag-cesitleri">Bilgisayar Ağ Çeşitleri</a> </li>
<li> <a href="#ag-bilesenleri">Ağ Bileşenleri</a></li>
<li> <a href="#ag-tipleri">Ağ Tipleri</a></li>



## <a id="ag-nedir">Ağ (Network) Nedir?</a>

Ağ tanımını yapmadan önce ağ’lara neden ihtiyaç duyulmuştur sorununun cevabına bakacak olursak, bilgisayarların her türlü bilgi, belge ve kaynak paylaşması için ağlara ihtiyaç duyulmuştur.  Ağlar arasında ki hızlı ve verimli paylaşım da, ağların önemini artırmıştır. Bilgisayarlar sayesinde öğrenmek istediğimiz bilgilere kolayca erişebilmekte, anlamlı veriler elde etmekte veya tecrübelerimizi paylaşabilmekteyiz. Bütün bu bilgi, kaynak ve belge paylaşımının karşılığı **networking**’dir. 

Daha teknik bir tanım yapacak olursak, iki veya daha bilgisayarın bilgi, belge ve kaynak paylaşmak amacıyla, donanımsal olarak birbirine uygun biçimde bağlanmasıdır. 

Bilgisayarların ilk çıktığı zamanlara bakacak olursak, bilgi, belge ve kaynak paylaşımları ilkel yönetemlerle sağlanmaktaydı. Örneğin: kişisel bilgisayarımızda (PC-Personal Computer)  bir belge hazırlayıp, bunun da çıktısını almak istediğimizde, eğer kendi kişisel bilgisayarımıza bağlı, sahip olduğumuz bir yazıcı yok ise bu belgeyi bir taşınabilir diske kopyalayıp, taşınabilir diskimiz ile yazıcıya sahip olan başka bir bilgisayara taşınabilir diskimizi takıp çıktımızı alıyorduk. Bu birbirinden bağımsız çalışma ortamına **stand-alone environment** denilmektedir.


<figure>
        <img src="http://yasinbaran.github.io/images/my-images/bilgisayar-aglari/1.jpg">
</figure>


Yukarıda gördüğümüz gibi bilgisayarların birbirine kablolar ile bağlandığı, bilgi, belge ve kaynak paylaşmaya imkan verdiği yapıya **ağ (network)** denir.  Bilgisayarlar arasında bilgi, belge ve kaynak paylaşılmasına da **ağ oluşturma (networking)** denir.

Bilgisayarlar arasında bilgi, belge ve kaynak paylaşımını gerçekleştirmek için fiziksel ve yazılımsal olarak iki önemli gereksinime ihtiyacımız vardır.

- **Fiziksel Bağlantı:** Bilgisayar üzerinde takılı olan veya harici olarak takılan fiziksel araçlara, bilgisayar ağı oluşturabilmek için gereksinim duyarız. Bilgisayarların birbirleri ile haberleşmesi için bilgisayar üzerinde ağ kartı veya ethernet kartı (NIC(Network Interface Card)-NAC(Network Adapter Card)) bulunmalıdır.

- **Yazılımsal Bağlantı:** Bilgisayarların sahip olacakları işletim sistemleri, işletim sistemlerinin kullanması gereken ağ yazılımlarının yapılandırılılmasıdır.

### <a id="nicin-kullanilir">Bilgisayar Ağları Niçin Kullanılır?</a>

- Bilgi Paylaşımı
- Donanım ve Yazılım Paylaşımı
- Yönetim ve Desteğin Merkezileştirilmesi

**Bilgi Paylaşımı**

Ağ teknolojisinin en önemli avantajı hızlı ve ucuz olmasıdır. Örneğin; Türkmenistan’da ki kuzeninize bir e-mail yazıp, sormak istediğinizi sorup, kuzeninizin de size cevap dönerek haberleşmenizi dakikalar içerisinde yapabiliyorsunuz.

Elektronik bilgi paylaşımının kullanılmaya başlanması ile birlikte, kağıt tüketimi azaltılmış, aynı anda birçok kişiye kısa sürede ulaşılmış ve bilgiler aynı anda birçok kişiyle paylaşılmış, toplantılar düzenlenmiş, uzak mesafelerde ki insanların kısa sürelerde haberleşmesi sağlanmıştır.

**Donanım ve Yazılımın Paylaşılması**

Çok sayıda kullanıcının aynı anda bilgi ve aygıtları kullanmasını, bilgisayar ağları mümkün kılar. Ağ üzerinde paylaşıma açılmış bir yazdırma aygıtını, ağda bulunan bütün bilgisayarlar kullanabilirler. Eğer stand-alone bir ortamda olsaydı bilgisayarlar, her bilgisayara ayrı bir yazıcı satın almak veya bilgisayarlarda bulunan verileri ilkel yöntemlerle yazıcıya sahip bilgisayarlardan çıktılar alacaklardı. Donanımın ve yazılımın paylaşılması sayesinde bu sorun ortadan kalkmıştır.

**Yönetim ve Desteğin Merkezileştirilmesi**

Ağ ortamında ki bilgisayarlara aynı uygulamaların kurulması , aynı işletim sistemlerinin kurulması veya bilgisayarlarda oluşan sorunlara, destek ve yardım konusunda personellere de kolaylık sağlar.


### <a id="ag-cesitleri">Bilgisayar Ağ Çeşitleri</a>

Bilgisayar ağları iki gruba ayrılır.

- **Local Area Network(LAN):** Yerel ağ anlamına gelmektedir. Aynı ortamda bulunan bilgisayarların oluşturduğu ağ yapısına verilen isimdir. LAN’da sınırlı bir coğrafi alan ve kullanılan aygıtların sınırlılığı söz konusudur. En az iki bilgisayarın oluşturduğu yapıdır.     


<figure>
        <img src="http://yasinbaran.github.io/images/my-images/bilgisayar-aglari/2.jpg">
</figure>


- **Wide Area Network(WAN):** Geniş ağlar anlamına gelmektedir. LAN’dan farklı olarak, coğrafi herhangi bir sınırı yoktur ve farklı coğrafi bölgeleri içerir.  Birbirine bağlı LAN yapılarından oluşur. Dünya üzerinde farklı konumlarda bulunan bilgisayar ve aygıtların haberleşmesini sağlar.


<figure>
        <img src="http://yasinbaran.github.io/images/my-images/bilgisayar-aglari/3.jpg">
</figure>


**WAN bağlantılarında kullanılan teknolojiler:**

- Analog Hatlar

- X.25

- WAN-ATM

- ISDN

- Frame Relay

- Kablolu TV Hatları

- xDSL (VDSL, ADSL)

WAN ağları da kendi içerisinde ikiye ayrılırlar:

- **Municipal Area Network(MAN):** İlçe veya belediye sınırları içerisinde oluşturulmuş ağa verilen isimdir.

- **Campus Area Network(CAN):** Üniversite kampüsü içerisinde oluşturulmuş olan ağa verilen isimdir.



### <a id="ag-bilesenleri">Ağ Bileşenleri</a>

- **Sunucu (Server) bilgisayarları:** Ağ ortamındaki kullanıcılara paylaştırılmış kaynakları sunan ve yöneten bilgisayarlardır.

- **İstemci (Client) bilgisayarları:** Sunucularda paylaştırılmış olan kaynakları kullanan bilgisayarlardır.

- **İletişim Aracı (Media):**  Fiziksel bağlantıyı sağlayan ekipmanlardır.

- **Paylaştırılmış Bilgi (Shared Data):** Ağ ortamındaki kullanıcılara sunulan dosyalardır.

- **Paylaştırılmış Kaynaklar (Shared Resources):** Dosya, yazıcı ve diğer aygıtların bulunduğu gruptur



### <a id="ag-tipleri">Ağ Tipleri</a>

**Ağ tipini seçerken dikkat edilmesi gerekenler:**

- Tasarlanan bilgisayar ağının büyüklüğü

- Tasarlanan bilgisayar ağı için güvenlik önlemleri

- Bilgisayar ağı üzerinde oluşması beklenen tahmini trafik yoğunluğu

- Bilgisayar ağı üzerinde yer alacak kullanıcıların gereksinimleri

- Kurulacak olan bilgisayar ağına ayrılacak bütçe

- İleriye dönük bilgisayar ağının büyüme olasılığı

**İki tip bilgisayar ağı vardır:**

- Eş-Eşe (Peer—to-peer) ağlar
- Sunucu tabanlı ağlar

### Eş-Eşe (Peer-To-Peer) Ağlar

Merkezi yönetimin olmadığı ağlardır. Bilgisayarlar kendi kendilerinin hem sunucusu hem de istemcileridir. Her sunucu kendi kaynaklarının paylaşımını kendisi yönetir. En fazla on ya da daha az bilgisayarın bir araya getirilmesiyle oluşur. Eş-Eşe ağlar çalışma grubu (workgroup) olarak da bilinmektedir. Bu ağların büyümesi sınırılıdır.

### Sunucu (Server) Tabanlı Ağlar

Bilgisayar ve kaynakların merkezi olarak yönetildiği ağ yapılarıdır.  Ağ’da yönetimden sorumlu server bulunur. Bilgisayar sayısında herhangi bir kısıtlama yoktur. Sistemin güvenliği merkezi olarak takip edilir. Bilgilerin merkezi olarak yedeklemesi (backup) yapılabilir. Merkezi bir veritabanı içerisinde ağda bulunan tüm kullanıcı ve bilgisayarların hesapları tutulur.Veritabanı sunucu bilgisayarında bulunur ve buradan yönetilir. Bu tarz sunucu tabanlı ağ yapıları domain olarak adlandırılır. Sunucu tabanlı ağlara örnek verecek olursak:

Dosya ve Yazdırma Sunucuları (File and Print Server)

E-Posta Sunucuları (E-Mail Server)

Faks Sunucuları (Fax Server)

Dizin Servisi Sunucuları (Directory Service Server)’dır.

**Avantajları:**
Kaynak Paylaşımı, Güvenlik, Yedekleme, Bilgi Kurtarma ve Koruma, Binlerce Kullanıcıya Destek Verme, Donanımsal Avantajlar olarak sıralayabiliriz.


Yazımı burada sonlandırıyorum, umarım faydalı olmuştur.

Saygılarımla.


Kaynak: [Windows Server Sistem Yönetimi Kitabı](https://www.linkedin.com/pulse/windows-server-sistem-y%C3%B6netimi-cilt-i-kitab%C4%B1m%C4%B1z-%C3%A7ikti-mesut-aladag?published=u) 
