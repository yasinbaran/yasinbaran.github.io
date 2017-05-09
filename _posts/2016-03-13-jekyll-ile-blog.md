---
layout: post
title: Jekyll ile Blog Oluşturma
excerpt:
categories: articles
comments: true
share: true
---

<span></span>

## İÇERİK

<li> <a href="#jekyll-nedir">Jekyll Nedir?</a></li>
<li> <a href="#nasıl-kurulur"> Nasıl Kurulur? </a> </li>




## <a id="jekyll-nedir"> Jekyll Nedir? </a>

Jekyll, güçlü bir altyapıya sahip Ruby tabanlı bir uygulamadır. Statik site üreticisi diye geçer. Mantığı çok basittir. Biz yazılarımızı Markdown formatında yazıyoruz ve Jekyll bunu statik bir web sitesine çeviriyor. 

Markdown yazı formatından bahsedelim. Örnek olarak:


---
layout: post  
title: Jekyll ile Blog Oluşturma   
excerpt:     
categories: articles   
comments: true  
share: true

---

Şeklinde başlığımızı, kategorimizi vs. eklediğimiz bir kısım var. Sonra bu kısmın altına geçip, yazımızı yazmaya başlıyoruz. Basit olarak bu şekilde bir kullanımı var. Daha detaylı kullanımları için: [tıklayınız.](https://daringfireball.net/projects/markdown/syntax) 


### <a id="nasıl-kurulur"> Nasıl Kurulur?</a>

Arkadaşlar öncelikle, kurulumları ve blog oluşturmayı Windows işletim sistemi üzerinden anlatmaya çalışacağım. Farklı bir işletim sistemi kullanıyorsanız, bunun için biraz araştırma yapmanız gerekebilir.

Gelelim kurulumlarımıza. Öncelikle:

Ruby indirmek için: [tıklayınız.](http://rubyinstaller.org/)

Ptyhon indirmek için: [tıklayınız.](https://www.python.org/)

Ruby ve Ptyhon'nu ilgili linklerden indirip, kurulumu tamamlayın. Kurulum bittikten sonra, **Bilgisayarım/Özellikler/Gelişmiş Sistem Ayarları/Gelişmiş/Ortam Değişkenleri**'nden Path'e eklenip eklenmediğinin kontrolünü yapın ve eğer path'te yoksa path'e ekleyin.


Ruby Development Kit indirmek için: [tıklayınız.](http://rubyinstaller.org/downloads/)

Development Kit'i indirdirkten sonra, C diskimize, devkit isimli bir klasör oluşturup, onun içerisine açalım.

Şimdi Başlat/Çalıştır'a cmd yazıp konsolu açıyoruz. Eğer kurulumlarımızı doğru yaptıysak;
Konsola **ruby -v** yazdığımız zaman kurulu ruby versionumuzu görüyor olmalıyız.

Şimdi C diskimize açtığımız devkit klasörüne gitmek için: **cd C:\devkit** komutunu çalıştırıyoruz. Devkit klasöründeyken sırasıyla aşağıda ki komutları çalıştırıyoruz:

**ruby dk.rb init**

**ruby dk.rb install**

Şimdi de jekyll'i indirmek için konsola:

**gem install jekyll**

yazıp, entera bastığımız zaman indirilmeye başlayacaktır. İndirme tamamlandıktan sonra: 

**gem install rdiscount**

**gem install kramdown**
 
komutlarını çalıştırıyoruz. Kurulumlarımız tamamlandı, ancak yapmamız gereken küçük birşey kaldı.Konsola **gem list** yazdığımız zaman karşımıza gelen listeden pygments.rb dosyasının versiyonu 0.5.0 değilse, bunu silip, 0.5.0 versiyonunu yüklemeliyiz. Bunun için:

**gem uninstall pygments.rb**

**gem install pygements.rb --version "=0.5.0"**


komutlarını çalıştırdığımız zaman , başarılı bir şekilde yüklenecektir.

Evet şimdi gelelim, blog oluşturmaya, öncelikle seçtiğiniz herhangi bir konuma (Ben belgelerin altına oluşturdum.) bir klasör oluşturup, ismine web_sitem verebilirsiniz. Klasörü oluşturduktan sonra, klasörün içerisine girin ve farenizle sağ tıklayıp **open command window here**'e tıklayın. Siz dilersiniz cmd'den de gidebilirsiniz. Klasörün içersindeyken başarılı bir şekilde konsolu açtıysanız, konsola: 

**jekyll new ilk-sitem**

yazdıktan sonra konsoldan **cd ilk-sitem** şeklinde klasörün içerisine girelim ve **jekyll serve** komutunu çalıştıralım. Şimdi tarayıcımızı açıp, http:\localhost:4000 yazıp enterladığımız zaman sitemiz bizi karşılayacaktır. Default olarak 4000 portunu kullanmaktadır. 

Sitemiz oluşturuldu ancak biz nasıl yazı ekleyeceğiz, yayınlayacağız?

Öncelikle sitemizi oluşturduğumuz klasörün içerisine gidip, ilk başta bizim işimize yarayacak dosyaları inceleyecek olursak:

_posts: Yazılarımızı yazdığımız ve build ettiğimiz, klasördür. Yani yazılarımız bu klasörün altında tutulur.


_site: Bu klasör bizim blogumuzun birebir çıktısıdır. Yazdığımız yazıların web sitemizde nasıl görüneceği, tarayıcı ile açıp görebiliriz.


_config: Bizim konfigurasyon dosyamızdır. Konfigurasyon ayarlarımızı bu dosya içerisinde yaparız.

*Not*: Eğer görselliği iyileştirmek istiyorsanız. Jekyll temaları için:[tıklayınız.](http://jekyllthemes.org/)

Artık sitemiz yayına hazır, bunu nasıl yayınlayabiliriz?
Github'ı sanırım herkes kullanıyordur, bilmeyen arkadaşlar araştırıp öğrenebilirler. Github'da repo oluşturup adını: http://githubHesapAdınız.github.io şeklinde belirliyoruz. Ardından web sitemizin bulunduğu klasörü bu repoya yüklüyoruz. http://githubHesapAdınız.github.io şeklinde yayınlanmış olduğunu görürsünüz. Sanırım belirli bir süre geçmesi gerekiyor.

Yazımı burada sonlandırıyorum, umarım faydalı olmuştur.

Saygılarımla.
