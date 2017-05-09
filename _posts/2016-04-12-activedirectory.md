---
layout: post
title: Windows Server 2012 R2 Active Directory
excerpt:
categories: articles
comments: true
share: true
---
<span></span>

## İÇERİK

<li> <a href="#dizinservisi">Dizin Servisi (Directory Service) Nedir?</a></li>

<li> <a href="#ADDomain">Active Directory Domain Servisi</a></li>

<li> <a href="#ADY">Active Directory Yapısı</a></li>

<li> <a href="#OPM">Operation Master Roller</a></li>

<li> <a href="#Adisimlendirme">Active Directory’nin Domain Servislerinde Nesnelerin İsimlendirilmesi</a></li>

<li> <a href="#LDAP">LDAP İsimlendirme Standartları</a></li>



## <a id="dizinservisi">Dizin Servisi (Directory Service) Nedir?</a>


Dizin servisini günlük hayatımızdan bir örnek ile açıklayacak olursak; yemek siparişi vereceğimiz zaman, yemek yapan restoranların telefon numaralarının bulunduğu telefon defterini açıp, sipariş vermek istediğimiz restoranın telefon numarasını bulur ve arayıp, siparişimizi veririz. Yemek yapan restoranın telefon bilgisini bize veren telefon defteri örnek bir dizin servisidir. Dizin servisleri ulaşacağımız nesneye ait ihtiyacımız olan adres ve lokasyon bilgisini içerir. Bilgisayar dünyasında da dizin servisleri aynı mantıkla çalışır.

**Dizin Servisi**, **domain** içerisindeki fiziksel ve mantıksal nesnelerle ilgili bilgileri tutan, bu bilgileri organize eden, bu bilgilerin merkezi yönetimini sağlayan ve bu bilgilere ulaşmak istediğimizde bize ulaşmak istediğimiz nesneye ait ulaşım bilgilerini veren servistir. Microsoft’un dizin servisine de “**Active Directory Service**” adı verilir.

Dizin servisinde nesnelerin özelliklerini tanımlayan özniteliklere, attribute adı verilmektedir.

### Dizin Servisinin Avantajları

**Merkezi Yönetim(Centralized Administration)**: Kullanıcı, kaynak veya bilgisayar dünyanın öbür ucunda da olsa, Active Directory sayesinde merkezi olarak yönetebiliriz.

**Eşit Haklara Sahip Domain Controller ( DC) Sunucular (Multimaster DC)**: Aynı Active Directory içerisinde ki bütün domain controller sunucular eşit haklara ve eşit veritabanına sahiptirler. Dolayısıyla her DC, master özelliğine sahiptir.

**Genişletilebilme ve Büyütülebilme (Scalability)**: İhtiyacımıza göre Active Directory domain yapısını istediğimiz kadar genişletebiliriz.

**İnternet İsim Yapısı Desteği**: Active Directory domain isimlendirmelerinde internet ağında da kullanılan DNS isimlendirme standardını kullanır. Dolayısıyla **Active Directory Domain**’leri ayrıca birer **DNS domain** isimleridir.
 
**Dinamik DNS Desteği:** Active Directory sayesinde domain’e katılan bir bilgisayar hesabının, **DNS** veritabanında da otomatik olarak kayıtları oluşmuş olur.

**LDAP Protokol Desteği**: Active Directory domain yapılarının **çekirdek (core)** protokolüdür. Aynı zamanda Active Directory domain yapısını oluşturan ve bu yapıya erişimi sağlayan, **TCP/IP** protokol ailesinin alt protokolüdür. Kaynakların Active Directory içerisinde isimlendirilmesini de sağlayan protokoldür. Ağ içerisineki kaynaklara erişim bu protokol sayesinde daha da hızlandırılmış olur.

**Delegasyonlu Yönetim**: Active Directory içerisinde açılmış yapısal birimler (Organizational Unit-OU) kullanılarak o birim üzerinde delegasyon yöntemi ile yetki ataması yapılarak, admistrator kullanıcısının yükü azaltılabilir. Böylece bölüm veya şube bazında belli görevler için yardım masasında çalışan ekiplere yetki atanarak, yönetimin kollara dağıtılması ile domain yönetimi kolaylaştırılabilir. Delegelerin yapabilecekleri delegasyonla belirlenir.


## <a id="ADDomain">Active Directory Domain Servisi</a>

Active Directory domain servisinin kurulduğu ve domain’in oluşturulduğu bilgisayara **Domain Controller (DC)** adı verilmektedir. **DC rolüne** sadece üzerinde **Windows Server** işletim sistemi kurulu olan  bilgisayarlar sahip olabilir.  Eğer bilgisayarın **Domain Controller (DC)** olması isteniyorsa işletim sisteminin kurulumundan sonra “**Active Directory Domain Service**” rolünün o bilgisayar üzerine kurulması gerekmektedir. **Stand-alone** ya da **member** olarak kuruluş bir bilgisayara active directory domain servis rolünün kurulumu ile DC rolüne yükseltilmesine **yükseltgeme (promote)** adı verilir.

Bir DC’nin yanına **yedekleme (backup)** ya da **yük paylaşımı (load balance)** amacıyla kurulan ilave domain controller sunucularına da **Additional Domain Controller (ADC)** adı verilir. Domain yapısı ilk DC’nin kurulumu ile oluşturulduktan sonra, ADC bilgisayarı mevcut domain yapısına sonradan katılır.

Active Directory ilk domain controller sunucusuna kurulduktan sonra, kurulan domain’e ait bir **domain ağacı (domain tree)** yapısı oluşur. Ayrıca farklı domain ağaçlarını da içerecek **orman (forest)** yapısı da oluşmuş olur. Active Directory  forest yapısında kurulan ilk domain’e **forest root domain** adı verilmektedir. Forest root domain içerisinde kurulan domain controller sunucuya da **forest root domain controller** adı verilir.


## <a id="ADY">Active Directory Yapısı</a>


Active Directory yapısı iki ayrı alanda değerlendirilir.

**•	Mantıksal Yapı (Logical Structure)**

**•	Fiziksel Yapı (Physical Structure)**

**Mantıksal Yapı Bileşenleri**

Active Directory içerisindeki kaynakların organize edilmesi ve gruplandırılmasını içeren yapı mantıksal yapıdır. Mantıksal olarak bir nesnenin konumu organize edildikten sonra, fiziksel konumu değiştirilse de kaynağa ulaşımda sorun yaşanmayacaktır.  Active Directorty içerisinde ki mantıksal bileşenler:

**•	Domain (Etki Alanı)**

**•	Organizational Unit (Yapısal Birim)**

**•	Domain Tree ( Domain Ağacı)**

**•	Forest (Orman)**

**•	Global Catalog**

**•	Trust Relationship (Güven İlişkisi)**

**Domain (Etki Alanı)**

Bir ağda merkezi yönetimi sağlamak  amacıyla kurulan çekirdek, yönetim birimine, **domain (etki alanı)** adı verilir. **Domain**, aynı isim altında toplanmış nesnelerin oluşturduğu yapılara verilen isimdir.

Aynı domain içerisinde bulunan bütün nesneler ortak bir veritabanı içerisinde depolanırlar. Windows Server 2012 R2 ağları üzerinde domain yapısının oluşturulabilmesi için Active Directory Domain Service rolünün Window Server 2012 R2 sunucu ailesinden bir işletim sistemine sahip bilgisayar üzerine kurulu olması gerekir.

**Organizational Unit (OU)**

Domain içerisinde ki nesneleri organize etmeyi sağlayan birimlerdir. Her domain içerisinde oluşturulan OU hiyerarşisi birbirinden bağımsızdır. Organizational Unit’ler, **kullanıcı hesapları (user account), grup hesapları (group account), bilgisayar hesapları (computer account), yazıcılar (printers), paylaştırılmış klasörler (shared folders)** gibi nesneleri içerirler.

Nesneleri OU’la içerisinde konumlandırarak dağınıklık ve yönetimi kolaylaştırmış oluruz.

OU’lar delegasyon avantajı da sağlarlar. OU yapısı oluşturarak, yönetim amacıyla sistemdeki kullanıcıları delege olarak atayabiliriz. Kullanıcının delege atanması esnasında hangi yetkilere sahip olacağı belirlenmektedir. Böylelikle **domain administrator** kullanıcısı üzerindeki yük azalmakta ve temel görevlerle ilgili yönetimin kollara ayrılması sağlanmış olacaktır.

**Domain Tree**
 
Aynı isim altında toplanmış bir veya daha fazla sayıda active directory domaininin hiyerarşik olarak oluşturduğu yapıya verilen isimdir. Aynı isim altında toplanan domainler topluluğuna **domain tree** adı verilir. Domain Tree, mevcut bir **parent domain**’e **child domainlerin** eklenmesi ile genişletilebilir. Aynı domain ağacı içerisindeki domainler ortak bir **domain isim alanına( domain namespace)** sahiptirler.

Domainle hiyerarşik bir isim yapısı kullanırlar. Child domainler, isim yapılarında parent domainlerin isimlerini kendi domain isimlerinin sonuna soy isim gibi ekleyerek kullanırlar. Örnek: parent domain: **yasinbaran.local**, child domain: **egitim.yasinbaran.local** şeklindedir.

İlk kurulan domaine (yasinbaran.local) **tree-root-domain**, o domain’in domain controller bilgisayarına da **tree-root-DC** adı verilir.

**Forest**

Active Directory domainlerinde mantıksal yapı içerisinde en dış katmandır. İçerisinde bir veya daha fazla sayıda **domain ağacını** barındıran yapıya verilen isimdir.
 
Forest içerisinde kurulan domain’e “**forest root domain**” adı verilir. Forest adı da **forest root domain** adı ile anılır.

**Global Catalog**

Active Directory  domain yapıları içerisinde bulunan bütün nesnelerin ve kaynakların adres bilgisini tutan ve bir kaynağa veya nesneye erişmek istediğimiz zaman, bize o kaynağın veya nesnenin adresini veren domain controller bilgisayarına “**global catalog sunucu**” adı verilir. Global Catalog forest yapısının haritasını tutar. Forest içerisinde **Global Catalog rolü** sadece forest içerisinde ilk kurulan DC olan **forest root DC**’ye otomatik olarak atanır. Global Catalog rolü forest yapısındaki diğer DC bilgisayarlarına da atanabilir.

Ayrıca active directory domain yapılarında **Universal** grup üyelikleri de yine global catalog sunucusundan sorgulanır. Global Catalog veritabanı aynı forest içerisinde bulunan tüm domainler içerisindeki tüm domain controller sunucular arasında olacaktır.

**Trust Relationships (Güven İlişkileri)**

Farklı iki domain arasında bilgi ve kaynak paylaşımı amacıyla kurulan mantıksal ilişkiye güven ilişkisi adı verilir. İki domain aynı forest içerisinde ise bu iki domain arasında güven ilişkisi otomatik olarak oluşur.
 
Aynı forest içerisindeki domainler arasında otomatik olarak oluşan güven ilişkilerinin iki önemli karakteristik özelliği vardır:

**•	Çift Yönlü (two way)**

**•	Geçişli (transitive)**

Çift yönlü olması her iki tarafında birbirine güvenmesi anlamına gelmektedir. İki tarafta birbirinin kaynaklarına erişebilir. 

Geçişlilik ise, doğrudan güven ilişkisine sahip olmayan iki domain’in her ikisinin parent domain ile kurdukları güven ilişkisi üzerinden birbirlerinin kaynaklarına erişmesi anlamına gelmektedir.

Güven ilişkileri mantıksal olarak da kuruludukları yapılara göre ikiye ayrılırlar:

**•	Parent-Child Trust**

**•	Tree-Root Trust**

**Parent-Child Trust**, bir üst domain ile hemen o domainin altındaki alt domain arasında kurulan güven ilişkisidir.  **Child domainden** bakılırsa, **Parent Trust, parent domainden** bakılırsa **Child Trust** olarak görülür. Bu güven ilişkisi çift yönlü ve geçişlilik özelliğine sahiptir.

**Tree-Root Trust**, forest root domain ile farklı isim alanı altında kurulmuş her domain ağacının ilk domain’i olan **tree root domain**’i arasında oluşan güven ilişkisidir. Bu güven ilişkisi de çift yönlü ve geçişlilik özelliğine sahiptir.

**Fiziksel Yapı Bileşenleri**

Fiziksel yapıyı ilgilendiren bileşenlerdir. Bunlar:

**•	Site**

**•	Domain Controller**

**Site**

DC’ler arası replikasyon trafiğini ve süresini kontrol altına almak için oluşturulmuş yapılardır. Ağ içerisindeki **ip subnet**’lerini siteler içerisinde tanımlayarak kullanıcıların kendi site yapısı ve **subnet** ağı içerisindeki **domain controller** sunucu üzerinden oturum açma, kimlik doğrulama vb. **active directory** fonksiyonlarını yerine getirmeleri sağlanmış olur.


<figure>
        <img src="http://yasinbaran.github.io/images/my-images/Genel/3.png">
</figure>


Bir site birden fazla domain içerebilir.

Bir sitenin altında alt siteler oluşturulamaz. Site tek seviyeli bir nesnedir.


**Domain Controller**

Domain yapısını kuran ve domain içerisindeki bütün nesnelerin ve kaynakların veritabanını depolayan bilgisayarlara **DC (Domain Controller)** adı verilir. Bir domain içerisinde kurulan bütün domain controller’lar üzeride ortak domain veritabanı bilgileri bulunur. DC’lerden biri üzerinde bir değişiklik yapıldığı zaman bu değişiklik aynı domain içerisindeki diğer **DC** bilgisayarlarına otomatik olarak **replikasyon** adı verilen bir mekanizma ile güncelleme yapılır. Bir DC kapalı olsa bile kullanıcı domaine oturum açmak istediğinde diğer **DC**’ler üzerinden **kimlik kontrolü (authentication)** yapılarak sisteme girmesi sağlanır.

Her işletim sisteminin domain controller olma özelliği bulunmaz. Sunucu tabanlı işletim sistemlerinin DC olabilme özelliği vardır.


## <a id="OPM">Operation Master Roller</a>

Active Directory içerisinde meydana gelen değişikliklerin replikasyonundan sorumlu rolleri olan sunucusistemlerine **operation master** adı verilir. **Flexible Single Master Operations Role (FSMO)** olarak da bilinirler. **“fizmo”** olarak telaffuz edilir.  Forest ve domain bazında çeşitli operation master rol’leri bulunmaktadır.

### Forest bazında bulunan operation master roller:

**•	Schema Master**

**•	Domain Naming Master**

### Domain bazında operation master roller:

**•	PDC Emulator**

**•	RID Master**

**•	Infrastructure Master**

Forest bazında ki roller forest içinde sadece bir **domain controller** sunucuya atanabilir. Varsayılan olarak **forest root domain controller** bu rollere sahiptir.

Domain bazındaki roller her domain içinde sadece  bir **domain controller** sunucuya atanabilir.

Farklı roller farklı domain controller sunuculara dağıtılabilir, fakat her rol o domain içerisinde sadece bir domain controller sunucuda olabilir.

**Schema Master**: Active Directory Schema’nın yönetimi, güncellenmesi ve replikasyonundan sorumlu olan domain controller rolüdür. Forest içindeki tüm **nesne sınıfları** ve bunlara ait **attribute**’ler **active directory schema yapısını** oluşturur. Active directory schema yapısının yönetimini sadece **Schema Admins** grubunun üyesi olanlar yapabilir. Varsayılan olarak bu grup **forest root domain** içerisinde oluşur.

**Domain Naming Master**: Forest içerisine yeni bir domain eklendiğinde, mevcut domainlerden bir kaldırıldığında, bir domain adı değiştiğinde ya da domain isimlerinde çakışma olduğunda bütün bunların kontrolünü yapan roldür. Her forest içerisinde en az bir tane olmalıdır. Varsayılan olarak **forest root DC** bu role sahiptir. **Glocal Catalog ** rolüne sahip bir domain controller sunucuda olması önerilir.

**PDC Emulator**: FSMO rolleri içerisinde en etkin ve yoğun kaynak kullanan roldür. Görevleri, **Windows NT BDC** ve istemci bilgisayarlarına **PDC** desteği vermesi, istemci bilgisayarlarındaki **password** değişikliğini güncellemesi, **zaman senkronizasyonu**, uygulanan **GPO**’lardaki çakışmaların engellenmesi gelmektedir.

**Rid Master**: Active directory içerisindeki nesnelere ait **SID (Security Identifier)** numaralarının atamasını ve kontrolünü yapan, objelerin bir yerden başka bir yere taşınırken meydana gelebilecek çakışmaları önleyen roldür.

**Infrastructure Master:** Active Directory içerisindeki grup üyelikleri bilgilerini kontrol ederek, tüm domain’lere bildirir. Diğer domain’lerin  üyesi bulunan nesnelerin güncellenmesini yapar. Global Catalog ile aynı domain controller sunucuda **olmaması** önerilir.



## <a id="Adisimlendirme">Active Directory’nin Domain Servislerinde Nesnelerin İsimlerndirilmesi</a>


**LDAP (Lightweight Directory Access Protocol)**: TCP/IP protokol kümesi içerisinde bulunan ve **istemci-sunucu** mimari modeline göre çalışan dizin hizmetlerini inşa eden, yöneten, güvenliğini ve erişimini sağlayan protokoldür.

Microsoft Active Directory yapısının altında bulunan çekirdek protokol **LDAP**’tır. Active Directory yapısının kurulumu, oluşturulması, erişimi, güvenliği, nesnelerin isimlendirilmesi vb. faaliyetler LDAP tarafından gerçekleştirilir.

LDAP isimlendirme standardındaki bazı tanımlamalar:

**•	DC (Domain Controller):** Active Directory yapısında oluşturulan bütün domainler DC ile tanımlanır.

**•	OU (Organizational Unit)**: Active Directory yapısında oluşturulan bütün organizational unitler OU ile tanımlanır.

**•	CN (Common Name)**: Active Directory yapısında oluşturulan kullanıcı, grup, bilgisayar, priter vb. gibi nesneler CN ile tanımlanırlar.

Örnek isimlendirmeler ve LDAP karşılıkları:

1.	**yasinbaran.local**  isimli domainimizin LDAP karşılığı: **DC=yasinbaran,DC=local**’dir.

2.	**egitim.yasinbaran.local** isimli child domainimizin LDAP karşılığı: **DC=egitim, DC=yasinbaran,DC:local**’dir.

3.	**yasinbaran.local** domaini altına oluşturulan **IT** isimli **OU**’nun LDAP karşılığı: **OU=IT,DC=yasinbaran,DC=local**’dir.

4.	IT isimli OU altındaki **Admin** isimli kullanıcının LDAP karşılığı: **CN=Admin, OU=IT, DC=yasinbaran,DC=local**’dir.


## <a id="LDAP">LDAP İsimlendirme Standartları</a>



LDAP protokolü Active Directory yapısında üç farklı tanımlama yapar:

**•	LDAP Distinguished Name (Aranan İsim)**

**•	LDAP Relative Distinguished Name (Asıl Aranan İsim)**

**•	Canonical Name (Takma İsim)**

**LDAP Distinguisged Name**: Bir nesneyi benzersiz bir şekilde bulunduğu konum içerisinde tanımlayan isimdir. Kısaca “**dn**” olarak ifade edilir. Örneğin, yasinbaran.local domaini altında, IT isimli OU altındaki **Admin** isimli kullanıcının **DN** karşılığı: **CN=Admin, OU=IT, DC=yasinbaran,DC=local**’dir. Aynı dn’ye sahip iki farklı nesne olamaz. Benzersizdir.

**LDAP Relative Distiguished Name:** Distinguished Name içerisinde asıl belirtilmek istenen nesne adına **Relative Distinguished Name** adı verilir. Örneğin, dn’si **CN=Admin, OU=IT, DC=yasinbaran,DC=local** bir nesnenin Relative Distinguished Name’i **CN=Admin**’dir. Yani **RDN**’si **Admin**’dir.

**Canonical Name**: DN ile aynı söz dizimine sahiptir, fakat gösterim tipi farklıdır. **yasinbaran.local** domain’i içerisinde bulunan **IT** isimli **OU** için **canonical name, yasinbaran.local/IT** şeklindedir. Active Directory yöneticileri takma isimleri yönetimsel araçlarda kullanırlar. Amaç yönetimsel araç içerisinde hiyerarşiyi göstermektir.




Yazımı burada sonlandırıyorum, umarım faydalı olmuştur.

Saygılarımla.


Kaynak: [Windows Server Sistem Yönetimi Kitabı](https://www.linkedin.com/pulse/windows-server-sistem-y%C3%B6netimi-cilt-i-kitab%C4%B1m%C4%B1z-%C3%A7ikti-mesut-aladag?published=u) 
