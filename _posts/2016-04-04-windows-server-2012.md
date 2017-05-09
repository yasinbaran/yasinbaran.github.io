---
layout: post
title: Windows Server 2012 R2 Kurulumu
excerpt:
categories: articles
comments: true
share: true
---
<span></span>

## İÇERİK

<li> <a href="#kurulum">Windows Server 2012 R2 Kurulumu</a></li>
<li> <a href="#firewall">Firewall'ın Devre Dışı Bırakılması</a></li>



## <a id="kurulum">Windows Server 2012 R2 Kurulumu</a>

Windows Server 2012 R2 ISO’su ile sunucumuzu başlatıyoruz. 


<figure>
        <img src="http://yasinbaran.github.io/images/my-images/WindowsServer2012R2/1.png">
</figure>

**Language to install**, kurulacak sistemin dilidir. Bu kısımdan dil seçimimizi yapıyoruz. 

**Time and currency format**, sistemin dil, saat ve parasal biçiminin seçimini yaptığımız kısımdır.

**Keyboard or input method**, bu kısımdan da sistemin klavye dilini seçiyoruz ve next’e tıklıyoruz.



<figure>
        <img src="http://yasinbaran.github.io/images/my-images/WindowsServer2012R2/2.png">
</figure>

Yeni bir işletim sistemi kuruyorsak, bu kısımdan **Install Now**’a tıklıyoruz.
 
**Repair your computer**, bu seçenek ile kurulu Windows Server 2012 R2 işletim sistemi ile ilgili kurtarma seçeneklerinin bulunduğu moda geçebiliriz. Mevcut sistemimizde işletim sistemi dosyalarımızdan herhangi biri zarar gördüğü zaman veya bozulduğu zaman bu seçenek ile onarabiliriz.


<figure>
        <img src="http://yasinbaran.github.io/images/my-images/WindowsServer2012R2/3.png">
</figure>


Bu kısımda bizden ürün anahtarı istenmektedir. 25 hanelik ürün anahtarımızı girip Next’e tıklıyoruz.


<figure>
        <img src="http://yasinbaran.github.io/images/my-images/WindowsServer2012R2/4.png">
</figure>

Bu kısımda iso’muz içerisinde bulunan Windows Server 2012 R2 sürümleri listelenir. Kuracağımız işletim sürümünü seçiyoruz. Bu kısımda aynı işletim sistemine ait **“Server Core Installation”** ve **“Server with a GUI”** isimli iki türünü görmekteyiz. Eğer grafiksel arayüzün bulunduğu sürümünü kuracaksak **“Server with a GUI”** türünü, komut satırı tabanlı sürümünü kuracaksak da **“Server Core Intstallation”**  türünü seçeriz. Windows Server 2012 R2 64-bit mimaride çalışan bir işletim sistemi olduğu için Architecture kısmında sadece x64 görüyoruz. Grafiksel arayüzü seçip **Next**’e tıklıyoruz.


<figure>
        <img src="http://yasinbaran.github.io/images/my-images/WindowsServer2012R2/5.png">
</figure>


Lisans anlaşması metni gelecektir. **“I accept the licence terms”** kutucuğunu işaretleyerek, şartları kabul ediyoruz ve **Next**’e tıklıyoruz.


<figure>
        <img src="http://yasinbaran.github.io/images/my-images/WindowsServer2012R2/6.png">
</figure>


**Upgrade:** Install Windows and keep files, settings, and applicaitons, eski sürüm Windows Server sürümünden yeni işletim sistemne yükseltme yapacaksak bu seçeneği seçiyoruz.

**Custom:* Install Windows only (advanced), tamamen yeni bir Windows Server 2012 R2 kurulumu yapacaksak bu seçeneği seçiyoruz.


<figure>
        <img src="http://yasinbaran.github.io/images/my-images/WindowsServer2012R2/7.png">
</figure>


Bu adımda Windows Server 2012 R2 işletim sistemini hangi birim üzerine yükleyeceksek, bu seçimi gerçekleştirmekle ilgili yapılandırmaları gerçekleştireceğiz.
 
**Load Driver**, sürücü problemlerinden dolayı diski görememe gibi durumlarda, disk üreticisinden gelen uygun sürücüler yüklenerek disk medyasının tanınması sağlanır.

Sunucu üzerinde tanıtılmış fakat henüz bölümleme yapılmamış diskler,**“Unallocated space”** olarak isimlendirilir.  **New**’e tıklayarak, bölümlemek istediğimiz diskin boyutunu belirleyebilir ve bölümleme yapabiliriz.

**Format,** seçili birimi biçimlendirir.
 
**Extend**, oluşturulan mevcut birimin kapasitesini artırmak için kullanılır.

**Delete,** seçili birimi silmek için kullanılır.

Diskimizin tamamında Windows Server 2012 R2 kurulumu yapacaksak, **Unallocated space** alanını seçip **Next**’e tıklıyoruz.


<figure>
        <img src="http://yasinbaran.github.io/images/my-images/WindowsServer2012R2/8.png">
</figure>


Kurulum sürecini başlatmış olduk. İşletim sistemi kurulum dosyaları disk üzerine kopyalanıp, kurulum için hazırlanacaktır. Temel işletim sistemi bileşenleri ve özellikleri yüklenecek, kurulum medyasında gelen güncellemeler yapılacak ve kurulum süreci tamamlanmış olacaktır.


<figure>
        <img src="http://yasinbaran.github.io/images/my-images/WindowsServer2012R2/9.png">
</figure>


Kurulum bittikten sonra sistem yeniden başlatılacak ve ilk açılışta **Settings** ekranı gelecektir. Ekranın sol alt köşesinden göre engelliler için erişebilirlik seçenekleri etkinleştirilebilir. Administrator kullanıcı hesabı ve şifre tanımlamasını yaparız. **Password** ve **Reenter password** kısımlarına aynı şifreyi girmeliyiz. Emin olmak için göz işaretine tıklayıp, girdiğimiz şifreyi görebiliriz. **Finish**’e tıklıyoruz.


<figure>
        <img src="http://yasinbaran.github.io/images/my-images/WindowsServer2012R2/10.png">
</figure>


Karşımıza oturum açma ekranı gelir. **Ctrl + Alt + Delete** ile oturum açma ekranını çağırırız.


<figure>
        <img src="http://yasinbaran.github.io/images/my-images/WindowsServer2012R2/11.png">
</figure>


Admistrator hesabımıza ait şifremizi girip, **ok**’a tıklanarak veya **enter**’a basılarak oturum açarız.


<figure>
        <img src="http://yasinbaran.github.io/images/my-images/WindowsServer2012R2/12.png">
</figure>


Karşımıza **Windows Server 2012 R2 kullanıcı arayüzü** ve **Server Manager** yönetim ekranı gelir. Server Manager ekranında bizi **Dashboard** ekranı karşılar. Dashboard ekranından kısayolları kullanarak sunucumuza **rol** ya da **özellik** ekleyebilir, uzaktan yönetmek istediğimiz sunucuları ekleyebilir ve sunucumuz üzerinde yüklü rollerin genel sağlık durumları hakkında bilgiler alabiliriz. 


<figure>
        <img src="http://yasinbaran.github.io/images/my-images/WindowsServer2012R2/13.png">
</figure>


**Local Server** seçeneğinden de oturum açmış olduğumuz sunucu ile ilgili bilgiler alabiliriz. **Local Server** ekranında sunucumuza ait bilgiler yer alır. Bu bilgilerin yapılandırılmasına ilişkin kısayollar bulunur. (Bilgisayar adı, Domain ve Workgroup tanımlamaları gibi). 


<figure>
        <img src="http://yasinbaran.github.io/images/my-images/WindowsServer2012R2/14.png">
</figure>


Ekranın sol alt köşesinden **Start** butonuna tıkladığımız zaman karşımıza **Start menüsü** gelecektir. Bu ekrandan sunucumuzun **TCP/IP** ayarlarını yapılandırmak için **Control Panel** aracına giriyoruz.


<figure>
        <img src="http://yasinbaran.github.io/images/my-images/WindowsServer2012R2/15.png">
</figure>


Control panel aracından **Network and Sharing Center**’ı açıyoruz. 


<figure>
        <img src="http://yasinbaran.github.io/images/my-images/WindowsServer2012R2/16.png">
</figure>


Gelen ekrandan **Change adapter settings** ile ağ bağlantılarını listeleme ekranına geçiyoruz.


<figure>
        <img src="http://yasinbaran.github.io/images/my-images/WindowsServer2012R2/17.png">
</figure>


Ağ bağlantılarımızı yapılandırmak için,  sağ tuş **Properties**’i açıyoruz.


<figure>
        <img src="http://yasinbaran.github.io/images/my-images/WindowsServer2012R2/18.png">
</figure>

Bu aşamada **TCP/IPv4** ayarlarını yapılandıracağımız için, **TCP/Ipv4** seçili iken **Properties**’e tıklıyoruz.


<figure>
        <img src="http://yasinbaran.github.io/images/my-images/WindowsServer2012R2/19.png">
</figure>

**IP adresi, Subnet Mask ve Preferred DNS Server** ile ilgili kısımlara gerekli adresleme ayarlarını giriyoruz. Gerekli ayarları yaptıktan sonra **OK** butonu ile ekranları onaylıyoruz.

Bu ayarlarımızı grafiksel arayüzler dışında komut satırı araçlarını kullanarak da yapılandırabiliriz. **Netsh.exe** aracı veya **NETAdapter** isimli powershell komut kütüphanesi aracı ile bu işlemleri yapabiliriz.


**Netsh** ile yapılandırmak için;


<figure>
        <img src="http://yasinbaran.github.io/images/my-images/WindowsServer2012R2/20.png">
</figure>


**Netsh interface ip Show config** komutu ile mevcut **TCP/IP** konfigürasyonu listeleriz.


<figure>
        <img src="http://yasinbaran.github.io/images/my-images/WindowsServer2012R2/21.png">
</figure>


**Netsh interface ip set adress** ile yeni bir **ip adresi, subnet mask ve default gateway** ataması yapabiliriz.


<figure>
        <img src="http://yasinbaran.github.io/images/my-images/WindowsServer2012R2/22.png">
</figure>


**Netsh interface ip set dns** ile **DNS sunucu adresi** tanımlayabiliriz.


<figure>
        <img src="http://yasinbaran.github.io/images/my-images/WindowsServer2012R2/23.png">
</figure>


**Netsh interface ip set wins** ile **WINS sunucu adresi** tanımlayabiliriz.

**Netsh interface ip set adress “Ethernet” dhcp** komutu ile ip adresinin otomatik ip dağıtımı yapan ortamdaki **DHCP** sunucusundan alacak şekilde yapılandırabiliriz.

**Powershell** ile yapılandırmak için:

Öncelikle **“Import-Module NetAdapter”** komutu ile **NetAdapter Powershell** komut kütüphanesini belleğe yükleriz.

**IPv4, subnet mask ve default gateway** tanımlamaları için,

**New-NetIPAddress –IPAddress 192.168.1.100 –InterfaceAlias “Ethernet” – DefaultGateway 192.168.1.254 –AddresseFamily IPv4 –PrefixLength 22**

Komutunu kullanırız.

**DNS** sunucu adresi tanımlamak için de;

**Set- DnsClientServerAddress –InterfaceAlias “Ethernet” –ServerAddresses 192.168.1.100**

komutu kulanılır.


<figure>
        <img src="http://yasinbaran.github.io/images/my-images/WindowsServer2012R2/24.png">
</figure>


**Start** butonu üzerinde sağ tıklayıp, **System** kısayoluna tıklıyoruz. 


<figure>
        <img src="http://yasinbaran.github.io/images/my-images/WindowsServer2012R2/25.png">
</figure>


Karşımıza sistem arayüzü gelecekir. Bu ekranda **Computer name** kısmında sunucu kurulumunda otomatik olarak üretilen sunucu bilgisayar adını görebiliriz. Kendi isteğimize göre bir sunucu adı tanımlamak için **Change Settings** kısayoluna tıklarız.


<figure>
        <img src="http://yasinbaran.github.io/images/my-images/WindowsServer2012R2/26.png">
</figure>


Bu ekrandan da **Change** butonuna tıklarız.


<figure>
        <img src="http://yasinbaran.github.io/images/my-images/WindowsServer2012R2/27.png">
</figure>


Karşımıza gelen ekrandan **Computer name** kısmına sunucuya vereceğimiz yeni adı verdikten sonra **OK** butonuna tıklarız.


<figure>
        <img src="http://yasinbaran.github.io/images/my-images/WindowsServer2012R2/28.png">
</figure>


Sunucuyu yeniden başlatmamız için bir uyarı ekranı gelecektir. **Ok** ile onaylıyoruz.


<figure>
        <img src="http://yasinbaran.github.io/images/my-images/WindowsServer2012R2/29.png">
</figure>


**System Properties** ekranını **Close** butonuna tıklayarak kapatırız.


<figure>
        <img src="http://yasinbaran.github.io/images/my-images/WindowsServer2012R2/30.png">
</figure>


Karşımıza gelen Windows diyalog kutusundan, **Restart Now** ile sunucumuzu yeniden başlatırız.

Sunucu adını **Server Manager** ekranından da değiştirebiliriz.



<figure>
        <img src="http://yasinbaran.github.io/images/my-images/WindowsServer2012R2/31.png">
</figure>


Server Manager ekranında sol kısımda yer alan **Local Server** kategorisi altından, **Computer Name** kısmından gelen mevcut bilgisayar adı üzerine tıklayarak, **System Properties** ekranına ulaşarak, yukarıda ki adımları gerçekleştirip sunucuyu yeniden başlatmamız gerekir.

Komut satırı araçlarını kullanarak da sunucu bilgisayar adını değiştirebiliriz. 

**Netdom.exe** komut satırı aracı için;


<figure>
        <img src="http://yasinbaran.github.io/images/my-images/WindowsServer2012R2/32.png">
</figure>


**NETDOM RENAMECOMPUTER** ifadesinden sonra, mevcut sunucu adını  **NEWNAME** parametresi ile yeni sunucu adı verilerek, **REBOOT** paremetresi ile 3 saniye içerisinde bilgisayarın yeniden başlatılması tetiklenir.

**Powershell** ile **computer name**’i değiştirmek için:



<figure>
        <img src="http://yasinbaran.github.io/images/my-images/WindowsServer2012R2/33.png">
</figure>


**Readme-Computer** komutu ile sunucu bilgisayar adını değiştiririz. Değişikliğin geçerli olması için **Restart-Computer –Force** komutu ile yeniden başlatılması gerekmektedir.

**Computer name**’i **registry**’den değiştirmek için;


<figure>
        <img src="http://yasinbaran.github.io/images/my-images/WindowsServer2012R2/34.png">
</figure>


**HKEY_LOCALM_MACHINE\SYSTEM\CurrentControlSet\Control\ComputerName\ActiveComputerName** anahtarı içerisindeki **ComputerName string** değerini değiştirebiliriz. Böylelikle sunucu bilgisayar adını değiştirmiş oluruz. Bu işlem sonrasında sunucuyu yeniden başlatarak, değişikliği etkinleştirmiş oluruz.


## <a id="firewall">Firewall'ın Devre Dışı Bırakılması</a>

Domain içerisinde çalışacak iç ağdaki sunucular üzerinde gerek duyulan her uygulama ya da servis için, portları açmaya gerek kalmadan erişim için, **Windows Firewall** devre dışı bırakılmalıdır. **Server Manager** konsolundan **Local Server** kategorisini açıyoruz.


<figure>
        <img src="http://yasinbaran.github.io/images/my-images/WindowsServer2012R2/35.png">
</figure>


**Windows Firewall**’un karşısında ki **public off/public on** bağlantısına tıklıyoruz.


<figure>
        <img src="http://yasinbaran.github.io/images/my-images/WindowsServer2012R2/36.png">
</figure>


Gelen ekranın solundan **Turn Windows Firewall on or off** bağlantısına tıklıyoruz.


<figure>
        <img src="http://yasinbaran.github.io/images/my-images/WindowsServer2012R2/37.png">
</figure>


**Customize settings** ekranında hem **Private** hem de **Public** profil için **Turn Off** konumuna alıyoruz. **OK** butonu ile onaylıyoruz.



Yazımı burada sonlandırıyorum, umarım faydalı olmuştur.

Saygılarımla.


Kaynak: [Windows Server Sistem Yönetimi Kitabı](https://www.linkedin.com/pulse/windows-server-sistem-y%C3%B6netimi-cilt-i-kitab%C4%B1m%C4%B1z-%C3%A7ikti-mesut-aladag?published=u) 
