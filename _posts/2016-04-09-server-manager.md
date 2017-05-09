---
layout: post
title: Windows Server 2012 R2 Server Manager
excerpt:
categories: articles
comments: true
share: true
---
<span></span>

## İÇERİK

<li> <a href="#servermanager">Windows Server 2012 R2 Server Manager</a></li>
<li> <a href="#addrolfeature">Rol ve Feature Eklemek</a></li>
<li> <a href="#deleterolfeature">Rol veya Feature Kaldırmak</a></li>
<li> <a href="#addserver">Ağ Ortamındaki Sunucuları Konsola Eklemek</a></li>
<li> <a href="#remoteaddrolfeature">Ağdaki Sunucuya Uzaktan Rol Ve Feature Eklemek</a></li>
<li> <a href="#group">Server Manager Konsolunda Server Groupları ile Çalışmak</a></li>
<li> <a href="#otherfunction">Server Manager Konsolunda Diğer Fonksiyonlar</a></li>
<li> <a href="#eventfollow">Server Manager Konsolunda Olay Takibi</a></li>
<li> <a href="#diskmanaging">Server Manager Konsolunda Disk Yönetimi</a></li>



## <a id="servermanager">Windows Server 2012 R2 Server Manager</a>


<figure>
        <img src="http://yasinbaran.github.io/images/my-images/serverManager/1.png">
</figure>

**“Welcome To Server Manager”** ekranı inceleyelim.

 **“Add roles and features”** bağlantısını kullanarak hem yerel sunucumuza hem de uzaktaki sunucularımıza **rol (role) veya özellik (features)** ekleme sihirbazını başlatabiliriz.

**“Add other servers to manage”** ile ağda bulunan ve yönetmek istediğimiz diğer sunucuları **Server Manager** konsolouna ekleyebiliriz.

**“Create a server group”** ile ağdaki sunucuları categorize etmek için sunucu grupları oluşturabiliriz.


## <a id="addrolfeature">Rol ve Feature Eklemek</a>

Server Manager konsolundan rol ve özellik eklemek için **Quick Start* kategorisindeki **Add Roles and Features** kısayolundan veya sağ üstte gelen **Manage** menüsünden **Add Roles and Fetures** kısayolunu kullanabiliriz. 

**Add Roles and Features**’a tıkladığımızda, karşımıza **Add Roles an Features Wizard** sihirbazı gelecektir. **Before You Begin** aşamasında bu sihirbazın kullanım amaçları ile ilgili bilgiler verilir.


<figure>
        <img src="http://yasinbaran.github.io/images/my-images/serverManager/2.png">
</figure>


Bu açıklamaların her feature veya role eklemek istediğimizde karşımıza gelmemesi için  **Skip this page by default** kutucuğunu doldurmalıyız. Next’e tıklayıp, bir sonraki adıma geçelim.


<figure>
        <img src="http://yasinbaran.github.io/images/my-images/serverManager/3.png">
</figure>


Karşımıza **Select Installation Type** ekranı gelecektir. Bu aşamada kendi seçeceğimiz bir sunucuya role veya feature eklemek için **Role-based or feature-based installation** seçeneğini seçmeliyiz.

**Remote Desktop Services scenario-based installation** seçeneği ile de **domain** ortamlarında uzak masaüstü hizmetleri ya da sanal masaüstü altyapılarının kurulumu için hazırlanmış **senaryo tabanlı** arayüzden gerçekleştirilebilir. 

**Role-based or feature-based installation** seçeneği seçili iken **Next**’e tıklıyoruz.


<figure>
        <img src="http://yasinbaran.github.io/images/my-images/serverManager/4.png">
</figure>


Karşımıza **Select destination server** ekranı gelecektir. Bu ekranda role veya feature eklemesini hangi sunucuya ya da sunucular üzerine yapacağımızı belirliyoruz. **Select a server from the server pool** seçeneği ile Server Manager konsolumuza hali hazırda mevcut sunucu havuzundan seçeceğiniz sunucular üzerine role ya da feature’ları ekleyebileceğimiz gibi, **Select a virtual hard disk** seçeneği ile de bir sanal sistemin **VHD** dosyasını gösterip onun üzerine de yine bu kurulumu yapabiliriz.

Bu aşamada mevcut local sunucumuz üzerine role veya feature yüklemesi yapacağımız için,** Select a server from the server pool** seçeneği seçili iken lokal listeden sunucumuzu seçip, **Next**’e tıklıyoruz.


<figure>
        <img src="http://yasinbaran.github.io/images/my-images/serverManager/5.png">
</figure>


Karşımıza **Select Server Roles** ekranı gelecektir. Bu ekranda eklemek istediğimiz rol ya da rollerin seçimini yapıyoruz. Herhangi bir rolü seçtiğimizde karşımıza bu rol için kurulması gereken **feature**’ların listesini getirecektir. **Add features** butonuna tıklayarak role ilişkin feature’ların yüklenmesini sağlayabiliriz. Şuanda bir rol kurulumu yapmayacağımız için, bu aşamayı **Next** ile geçiyoruz.


<figure>
        <img src="http://yasinbaran.github.io/images/my-images/serverManager/6.png">
</figure>


Karşımıza **Select Features** sayfası gelecektir. Bir önceki aşamada, otomatik olarak yüklenmesi kararlaştırılan rollere ilişkin feature’ların da bu ekranda seçili olduğunu göreceğiz. İlave feature eklemek istersek, yine bu aşamada seçebiliriz. Bu aşamada **Telnet Client** bileşenini yüklemek için ilgili kutucuğu işaretleyip **Next** ile bir sonraki adıma geçiyoruz..


<figure>
        <img src="http://yasinbaran.github.io/images/my-images/serverManager/7.png">
</figure>


Eğer **Select Server Roles** adımında seçtiğimiz bir rol varsa, öncelikle bu rol ile ilgili rolün ne işe yaradığı ve bu role ilişkin önemli notlarla ilgili bilgileri bulacaksınız. Bu aşamayı **Next** ile geçebilirsiniz. Eğer sadece **feature** seçtiyseniz, bu durumda doğrudan **Confirm installation selections** ekranı gelecektir.

Bu ekranda **Restart the destination server automatically if required** kutucuğunu doldurarak, eğer sistemin otomatik olarak yeniden başlatma ihtiyacı varsa, rol eklenmesi sonrasında sistemin otomatik olarak yeniden başlatılması tetiklenmiş olur. Gelen onay ekranında Yes butonuna tıklayarak rol eklemesi sonrasında otomatik başlatma ihtiyacını onaylıyoruz. 

Ekranın altıdaki **Export configuration settings** bağlantısı ile eklediğimiz role ya da feature’ları içeren **XML** yapılandırma dosyasının çıktısını üretebiliriz.

**Specify an alternate source path** seçeneği ile yüklenen bileşen için yükleme dosyalarını özel bir konumdan almasını istiyorsak, buraya yol tanımını belirtiriz.

Ekranın sağ üst köşesinde rol ya da feature kurulumu yaptığımız hedef sunucu, bilgisayar adı **Destination Server** etiketinin altında gösterilmektedir.

**Install** butonuna tıklayarak seçilen bileşenlerin yüklenme sürecini başlatırız.


<figure>
        <img src="http://yasinbaran.github.io/images/my-images/serverManager/8.png">
</figure>


Yükleme süreci başladıktan sonra, bu ekranda beklemek zorunda değiliz. **Close** ile ekranı kapatabiliriz. 


<figure>
        <img src="http://yasinbaran.github.io/images/my-images/serverManager/9.png">
</figure>


Devam eden işlemler için **bayrak** simgesine tıklayıp, görüntüleme yapabiliriz. **Task Details** bağlantısına tıklayarak, kapattığımız **Installation progress** ekranına gidebiliriz.


<figure>
        <img src="http://yasinbaran.github.io/images/my-images/serverManager/10.png">
</figure>


Bu aşamadan sonra yüklenen rol ya da bileşene ait yapılandırma adımları varsa, örneğin DHCP Server rolü için sunucuyu yetkilendirme adımları gibi görevleri içeren sihirbazı başlatmamız gerekir. Telnet Client için böyle bir gereksinime ihtiyaç olmadığı için, biz kurulumu tamamlamış oluyoruz.


## <a id="deleterolfeature">Rol ve Feature Kaldırmak</a>

**Manage** menüsünden **“Remove Roles and Features”** seçeneğine tıklıyoruz.


<figure>
        <img src="http://yasinbaran.github.io/images/my-images/serverManager/11.png">
</figure>


İlk adımda karşımıza **Before you begin** ekranında rol ya da feature kaldırmadan önce, önerilen bilgileri inceledikten sonra **Next**’e tıklıyouz..


<figure>
        <img src="http://yasinbaran.github.io/images/my-images/serverManager/12.png">
</figure>


Karşımıza **Select Destination Server** ekranı gelir. Bu ekranda rol ya da feature kaldırmak istediğimiz sunucu ya da sanal diski seçmemizi isteyecektir.

<figure>
        <img src="http://yasinbaran.github.io/images/my-images/serverManager/13.png">
</figure>


İlgili sunucuyu seçtikten sonra **Next** ile bir sonraki adıma geçeriz. 


<figure>
        <img src="http://yasinbaran.github.io/images/my-images/serverManager/14.png">
</figure>


**Remove Server Roles** ekranında kaldırmak istediğimiz rolün kutucuğunu boşaltmamız gerekir. Kaşımıza o role ilişkin kaldırılması gereken feature’ların listesini getirir. Bu ekranda **Remove Features** butonuna basarak ilgili feature’ların da kaldırılmasını onaylıyoruz. Eğer amacımız rol kaldırmak değil de sadece feature kaldırmaksa, bu durumda **Remove server roles** ekranında herhangi bir değişiklik yapmadan feature’ların bulunduğu adıma geçebiliriz.** Next **ile bir sonraki adıma geçiyoruz.


<figure>
        <img src="http://yasinbaran.github.io/images/my-images/serverManager/15.png">
</figure>


Kaldırılacak **Telnet Client** kutucuğunu boşaltıyoruz. Ek olarak kaldırmak istediğimiz feature’lar varsa, bunlara ait kutucukları da boşaltmalıyız. **Next** ile devam ediyoruz. 


<figure>
        <img src="http://yasinbaran.github.io/images/my-images/serverManager/16.png">
</figure>


**Confirm removal selections** ekranında rol ya da feature kaldırılma sürecinden sonra, sunucuyu yeniden başlatma ihtiyacı varsa otomatik olarak yeniden başlatmasını istersek, **“Restart the destination server automatically if required”** kutucuğunu doldurmamız gerekir, aksi halde sunucuyu başlatma sürecini manuel olarak tetiklememiz gerekir. **Remove** butonuna tıklayarak rol ya da feature kaldırılmasını tamamlamış oluruz..


<figure>
        <img src="http://yasinbaran.github.io/images/my-images/serverManager/17.png">
</figure>


## <a id="addserver">Ağ Ortamındaki Sunucuları Konsola Eklemek</a>

Manage menüsünden Add Servers’a tıklıyoruz.


<figure>
        <img src="http://yasinbaran.github.io/images/my-images/serverManager/18.png">
</figure>


Gelen **Add Servers** ekranından Active Directory üzerinden, DNS üzerinden eklemek istediğimiz bilgisayar hesabını arama yapabileceğimiz gibi, eğer eklenecek sunucu isimleri bir metin dosyasında hazırsa, Import tabını kullanarak bu dosyadan da sunucu listesini alabiliriz.

Domain seviyesinde arama yapacağımız için domain seçili iken **Find Now**’a tıklıyoruz. Eğer **OU** bazında filtreleme yapmak isteseydik, **Location** kısmından **OU** bazında filtreleme yapabilirdik.


<figure>
        <img src="http://yasinbaran.github.io/images/my-images/serverManager/19.png">
</figure>


Alt kısımda sunucuya ait ismi seçip orta kısımdaki ok simgesine ile **Selected** listesine ekliyoruz. **OK** ile onaylıyoruz.

**Server Manager** konsolunda **All Servers** kategorisi  altında bu sunucuların geldiğini göreceksiniz.

Herhangi bir sunucu ismi üzerine sağ tuşla tıklandığında aşağıdaki menü gelecektir. 



<figure>
        <img src="http://yasinbaran.github.io/images/my-images/serverManager/20.png">
</figure>


**Add Roles and Features:** Uzaktan sunucuya rol ya da feature eklemeyi sağlar.

**Restart Server:** Uzaktan sunucuyu yeniden başlatacaktır.

**Computer Management:** Uzaktaki sunucunun Computer Management konsoluna bağlanarak o konsol içerisindeki fonksiyonları yönetmeyi sağlar.

**Remote Desktop Connection:** Seçilen sunucuya RDP bağlantısı yapmayı sağlar.

**Windows Powershell:** Seçilen sunucu için uzaktan Powershell komutları ve script’leri çalıştırmayı sağlar.

**Configure Network Adapter Teaming:** Seçilen sunucu üzerindeki ağ kartları arasında uzaktan Teaming yapmayı sağlar.

**Configure Windows Automatic Feedback:** Seçili sunucu üzerindeki Microsoft Customer Improvement Program özelliklerini etkinleştirmek ve konfigure etmek için kullanılır.

**Manage As:** Seçili sunucuya uzaktan farklıbir kullanıcı ve yetkileri ile işlem yapmak için kullanılır.

**Start Performance Counters:** Server Manager konsolu içerisinde Performance segmentini kullanarak sunucunun **CPU, RAM, Disk ve Ağ performansını** izlemek için gerekli sayaçların(performance counter) aktifleşmesi ve sunucudan veriler toplanarak performans göstergesinin **Server Manager** konsolundan izlenmesini tetikleyen özellik.

**Remove Server:** **Manage** menüsünden **Add Server** ile eklenen sunucuyu Server Manager konsolundaki sunucu listesinden kaldırır.

**Refresh:** Sunucuya ait bilgileri yineler.


## <a id="remoteaddrolfeature">Ağdaki Sunucuya Uzaktan Rol Ve Feature Eklemek</a>

**Server Manager** konsolundan **All Servers** kategorisindeki eklenen uzaktan sunucu üzerinde sağ tuşa basılınca, gelen **Add Roles and Features** linkine tıklıyoruz. Karşımıza gelen **Before you begin** ekranında sağ üst köşede **Destination Server** olarak bu sunucunun adının görüldüğünü görüyor olacağız. **Next** ile geçiyoruz. **Select installation type** ekranında **Role-based or feature-based installation** seçeneği seçili  iken **Next** ile geçiyoruz. 

**Select destination server** ekranında **Server Pool** altından üzerine kurulum yapılan sunucu otomatik olarak seçili gelecektir. Bu aşamada istersek farklı bir sunucu da seçilebilir. **Next** ile bir sonraki aşamaya geçtiğimizde karşımıza **Select Server Roles** ekranı gelecektir. Ağdaki sunucuya eklemek istediğimiz rolü seçip, **Next** ile devam ediyoruz. 


<figure>
        <img src="http://yasinbaran.github.io/images/my-images/serverManager/21.png">
</figure>


Bu role ait feature’ların da otomatik olarak kurulacağı mesajı gelecektir. **Add features** ile onaylıyoruz ve **Next** ile devam ediyoruz.

**Select features** ekranı karşımıza gelecektir. İlave etmek istediğimiz features varsa seçip, **Next** ile bir sonraki adıma geçiyoruz. Karşımıza gelen bilgilendirme ekranını da **Next** ile geçiyoruz. 

**Confirm installations selections** ekranından **Install** butonuna tıklıyoruz ve kurulumu başlatıyoruz.

Kurulum tamamlandıktan sonra **Server Manager** konsolunda sol tarafta gezinti menüsünde o rolün geldiğini göreceksiniz.


## <a id="group">Server Manager Konsolunda Server Groupları ile Çalışmak</a>

Server Manager konsolu içerisine eklenen ağdaki sunucular için gruplar oluşturup, sunucuları da bu gruplar içerisine dahil edip, sınıflandırma yapabiliriz.

Sunucu grupları oluşturmak için, **Server Manager** konsolundan **Manage** menüsünden **Create Server Group** bağlantısına tıklarız.


<figure>
        <img src="http://yasinbaran.github.io/images/my-images/serverManager/22.png">
</figure>


**Create Server Group** ekranı karşımıza gelecektir. **Server group name** kutusuna grup için bir isim veririz. **Server Pool** listesinden hangi sunucuları bu gruba dahil edecekseki onları seçip **OK** simgesine basarak **Selected** listesine ekleriz.


<figure>
        <img src="http://yasinbaran.github.io/images/my-images/serverManager/23.png">
</figure>


**Active Directory** tabından **Location** bilgisi yanında işletim sistemi versiyonun göre de Operating System özelliğini kullanarak filtreleme yapabiliriz. **OK** ile bir sonraki adıma geçiyoruz.

**Server Manager** konsolunda soldaki gezinti menüsünde bu yeni grubun geldiğini ve seçilen sunucuların da gruba eklendiğini görmüş olacağız.

Grup adı üzerinde sağ tıklayarak, özellik ve üyelikleri değiştirebilir, sunucu gurubumuzu **Delete Server Group** ile kaldırabiliriz.

## <a id="otherfunction">Server Manager Konsolunda Diğer Fonksiyonlar</a>

**Server Manager** konsolundan **Manage** menüsünden **Server Manager Properties** linkine tıklayarak konsol ile ilgili bazı temel özellikleri ayarlayabiliriz.


<figure>
        <img src="http://yasinbaran.github.io/images/my-images/serverManager/24.png">
</figure>


**Server Manager Properties** ekranı karşımıza gelecektir. **Specify the Server  Manager data refresh period (in minutes)** seçeneğiyle belirtilen sürede otomatik olarak **Server Manager** konsolundaki verilerin yenilenmesini sağlayabiliriz. 

**OK** ile onaylıyoruz. 


<figure>
        <img src="http://yasinbaran.github.io/images/my-images/serverManager/25.png">
</figure>


**Server Manager** konsolunda **Tools** menüsünü açtığımız zaman yerel sunucumuzun yönetimsel görevlerini gerçekleştirebileceğimiz **MMC** konsollara erişim sağlayabiliriz. 


<figure>
        <img src="http://yasinbaran.github.io/images/my-images/serverManager/26.png">
</figure>


Tools menüsünde standart olarak gelen bağlantılara ek olarak kendi kısayollarımızı ekleyebiliriz.**“C:\ProgramData\Microsoft\Windows\StartMenu\Programs\Administrative Tools”** altına istediğimiz kısayolları kopyalamamız yeterlidir.


<figure>
        <img src="http://yasinbaran.github.io/images/my-images/serverManager/27.png">
</figure>


**View** menüsü ile konsolun görünüm yüzdesini değiştirebiliriz. **Hide Welcome Tile** bağlantısı ile de Dashboard görünümünde **Welcome To Server Manager** ekranını gizleyebiliriz.


<figure>
        <img src="http://yasinbaran.github.io/images/my-images/serverManager/28.png">
</figure>


**Help** menüsü ile de **Server Manager** yardım dosyalarına erişebiliriz.

## <a id="eventfollow">Server Manager Konsolunda Olay Takibi</a>


<figure>
        <img src="http://yasinbaran.github.io/images/my-images/serverManager/29.png">
</figure>


**Server Manager** konsolunun alt kısmında **EVENTS** segmentinde **Event Viewer** içerisine düşen olaylara ait kayıtları görebiliriz.


## <a id="diskmanaging">Server Manager Konsolunda Disk Yönetimi</a>


**Server Manager** konsolundan **File and Storage Services** rolü altından **Volumes and Storage Pools** seçeneğine tıklıyoruz. **Volumes**’e tıkladığımız zaman sağ tarafta sunuculara kategorilendirilmiş ler ve bunların doluluk oranları gelir. Buradan varsa bölümlendirilmemiş alanları da yapılandırabiliriz. 


<figure>
        <img src="http://yasinbaran.github.io/images/my-images/serverManager/30.png">
</figure>


**Shares** bağlantısına tıklyarak da sunucular üzerindeki paylaştırılmış klasörler ve bu klasörlerin diskten kullandıkları alanlara ait bilgilere ulaşabiliriz..


Yazımı burada sonlandırıyorum, umarım faydalı olmuştur.

Saygılarımla.


Kaynak: [Windows Server Sistem Yönetimi Kitabı](https://www.linkedin.com/pulse/windows-server-sistem-y%C3%B6netimi-cilt-i-kitab%C4%B1m%C4%B1z-%C3%A7ikti-mesut-aladag?published=u) 
