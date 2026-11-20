# Hizmet Sürekliliği Yönetimi

**Hizmet sürekliliği yönetimi, bir kuruluşu ciddi bir kesintiden sonra en önemli hizmetlerini çalışır durumda tutmaya ya da hızla geri getirmeye hazırlar; değeri, raftaki planla değil, yalnızca tatbikatlarla kanıtlanır.**

## Bu neden önemli

Çoğu olay küçük ve yereldir. Birkaçı değildir: bir veri merkezi yangını, arızalanan bir bulut bölgesi, bir fidye yazılımı saldırısı, bir tedarikçinin çöküşü, bir salgın, bir sel. Bu olaylar kuruluşun hizmet verme yeteneğini bütünüyle tehdit eder ve bunları ele almak, sıradan olay yönetiminin kapsamadığı bir planlama gerektirir. En çok neyin önemli olduğunu ve nasıl devam edeceğini önceden düşünmüş bir ekibin atlatma şansı çok daha yüksektir.

Çevik ekipler bu konuyla belirli bir güçlükle karşılaşır. Sistemleri haftalık değişir, bu yüzden bir kez yazılıp dosyalanan süreklilik planı aylar içinde güncelliğini yitirir. Belirli bir sunucuya ya da betiğe bağlı kurtarma adımları artık geçerli olmayabilir. Çevik yanıt, planlamadan vazgeçmek değil, sürekliliği hizmetlerin nasıl inşa edilip işletildiğinin yaşayan bir parçası yapmaktır: kurtarma tasarımın içine yerleştirilir, sık sınanır ve kodla birlikte sürüm denetiminde tutulur.

[İş sürekliliği planlamasına ilişkin Wikipedia maddesi](https://en.wikipedia.org/wiki/Business_continuity_planning), iş sürekliliğini bir kuruluşun bir kesintiden sonra ürünleri ya da hizmetleri kabul edilebilir seviyelerde sunmaya devam etme yeteneği olarak tanımlar ve süreklilik planlamasını risk yönetiminin bir alt kümesi olarak ele alır. İngilizce Wikipedia'nın "Disaster recovery" sayfası yalnızca bir anlam ayrımı sayfasıdır ve tam bir madde istendiğine dair bir not taşır; bu nedenle bu konu tanımlar için iş sürekliliği maddesini kullanır ve rehberin diğer konularından pratik yönlendirme ekler, bunun bildirilmiş kaynak materyal değil uygulama olduğunu belirtir.

## Temel kavramlar

### Süreklilik, kurtarma ve dayanıklılık

Terimler gevşek biçimde kullanılır, bu yüzden dikkatle kullanın:

| Terim | Yaygın kullanımıyla anlamı | Odak |
|---|---|---|
| **İş sürekliliği (business continuity)** | Bir kesintiden sonra ürünleri ya da hizmetleri kabul edilebilir seviyelerde sunmaya devam etme yeteneği | Kuruluşu ayakta tutmak |
| **İş sürekliliği planlaması** | Kuruluşa yönelik tehditler için önleme ve kurtarma sistemleri oluşturmak | Planlar ve düzenlemeler |
| **BT felaket kurtarma (IT disaster recovery)** | Hayati bilgi teknolojisi altyapısını sürdürmek ya da yeniden kurmak (Wikipedia anlam ayrımı sayfasında verilen betimleme) | Teknoloji |
| **Hizmet sürekliliği (ITSM)** | BT hizmetlerinin bir kesintiden sonra üzerinde anlaşılan seviyelere geri getirilebilmesini sağlamak | Daha büyük plan içindeki BT hizmetleri |

Wikipedia maddesi, felaket kurtarmanın iş sürekliliği planlamasıyla, özellikle çözüm aşamasında örtüştüğünü ve sürekliliğin her ikisini yürütmenin amaçlanan sonucu olduğunu söyler. Hizmet sürekliliği yönetimi, aynı amacın BT hizmeti görünümüdür.

### İş etki çözümlemesi

Maddeye göre **iş etki çözümlemesi (BIA)**, kesintilerin operasyonları nasıl etkilediğini belirleme ve değerlendirme ve kurtarma önceliklerini belirleme yöntemidir. Hedefleri arasında kritik faaliyetleri ve bağımlılıkları belirlemek, mali, operasyonel, itibar ve hukuki etkileri değerlendirmek, kurtarma hedeflerini belirlemek ve risk değerlendirmesini bilgilendirmek yer alır. BT hizmetleri için BIA, kuruluşun hangi hizmetlerden vazgeçemeyeceğini, hangi sırayla geri gelmeleri gerektiğini ve her birinin neye bağlı olduğunu sorar (bağımlılıklar için bkz. Konu 4.4 — Yapılandırma Yönetimi).

### Kurtarma hedefleri

Madde iki kilit terimi tanımlar:

- **Kurtarma süresi hedefi (RTO):** bir işlevi geri getirmek için kabul edilebilir süre.
- **Kurtarma noktası hedefi (RPO):** kabul edilebilir veri gecikmesi miktarı, yani ne kadar veri kaybına tahammül edilebileceği.

Ayrıca azami tahammül edilebilir kesinti süresini de sayar. Madde, belirli bir kuruluş için bu değerleri seçmenin bir yöntemini vermez; bu yüzden bunlar işten gelmelidir: bir saatlik, bir günlük ve bir haftalık kesintinin neye mal olduğunu ve işin hangi veriyi kaybetmeyi göze alabileceğini sorun. Bunları belirlemek, bir fiyatı olan bir iş kararıdır, çünkü daha sıkı bir hedefi karşılamanın maliyeti artar (bkz. Konu 3.11 — Erişilebilirlik, Kapasite ve Performans).

### Planlar

Bir süreklilik ya da kurtarma planı, bir kesintiden sonra kritik hizmetleri geri getirmek için kimin neyi hangi sırayla yapacağını betimler. Şunları kapsamalıdır: planın nasıl ve kimin tarafından devreye alındığı, insanların nasıl bilgilendirilip toplandığı, hizmetler için kurtarma sırası, kurtarmanın nerede yapılacağı, verilerin nereden geleceği, müşteriler ve personelle nasıl iletişim kurulacağı ve normale nasıl dönüleceği. BT hizmetleri için planlar, tek tek sistemlerin çalışma kılavuzlarına bağlanmalıdır (bkz. Konu 3.9 — Bilgi Yönetimi).

### Sınama ve tatbikatlar

Madde, İngiliz Standartlar Enstitüsü'nün 2008 tarihli bir kitabına atıf yapar; bu kitap üç tür tatbikatı betimler: küçük bir grubun planın bir yönünü tartıştığı bir **masa başı (tabletop)** tatbikat, birkaç ekibin kurgulanmış sürprizlerle birden çok yön üzerinde çalıştığı bir **orta (medium)** tatbikat ve önceden haber vermeden devreye alma, gerçek tahliye ve bir felaket kurtarma sitesinin kullanımını ekleyen bir **karmaşık (complex)** tatbikat. Teknik çözümlerin ve kurtarma yordamlarının sınanmasını da içeren, bulguların çözümleme aşamasına döndüğü, yıllık ya da iki yıllık bir bakım döngüsünü betimler. Tatbikatlar, planların yanlış olduklarını öğrendikleri yerdir.

### Kurtarma kademeleri

Madde SHARE'in yedi felaket kurtarma kademesinden (1992) söz eder; bunlar daha sonra IBM tarafından sekiz kademeye (0'dan 7'ye) güncellenmiştir. Burada okunan kaynaklar kademeleri ayrıntılandırmaz. Genel bir uygulama olarak kuruluşlar hizmetleri ne kadar çabuk geri getirilmeleri gerektiğine göre kademelere ayırır ve kurtarma yaklaşımını ve maliyetini kademeye uydurur.

### Standartlar

Madde, 2012 sürümünün yerini alan ve kuruluşların süreklilik hedeflerini, asgari kabul edilebilir hizmet seviyelerini ve azami tahammül edilebilir kesinti süresini tanımlamasını gerektiren ISO 22301:2019, *Security and resilience, Business continuity management systems, Requirements* standardına atıf yapar. ISO 22313:2020 onu kullanma konusunda rehberlik verir. Bunlar bir kuruluşun benimseyebileceği bir yönetim sistemi için standartlardır; pratik planlamanın yerini almazlar. Müşterileriniz ya da düzenleyiciler uyum gerektiriyorsa standart metnini doğrudan denetleyin.

### Çevik süreklilik

Çevik ve DevOps uygulamaları sürekliliğe yardımcı olur:

- **Kod olarak altyapı ve yapılandırma**, ortamların sürüm denetiminden yeniden kurulmasına olanak tanır; bu da kurtarmayı daha hızlı ve sınanabilir yapar.
- **Otomatik hatlar (pipeline)**, hizmetleri bir kurtarma sitesine yeniden dağıtabilir.
- **Sık sürümler**, ekibi dağıtım konusunda alıştırmalı tutar.
- **Düzenli tatbikatlar**, biriktirme listesinde bir sınama biçimi olarak ele alınabilir.

Ayrıca riskler de yaratırlar: tek bir bulut hesabına yoğun bağımlılık, kendisi tek bir hata noktası olan bir CI sistemi ve bir felakette erişilemeyecek yerlerde saklanan sırlar. Kurtarmanın kendisinin dayandığı araçlar için plan yapın.

### İnsan etkenleri

Madde, bölümlere ayrılmış ve rotasyonlu ekiplere örnek olarak 2002-2003 SARS salgınından söz eder; bu, sürekliliğin insanları da kapsadığının bir hatırlatmasıdır: bireylere yayılmış kilit beceriler, uzaktan çalışma, olağan kanallar çöktüğünde iletişim ve stres altındaki personelin gözetilmesi.

### Kaynakların sınırları

Madde, hedefleri belirlemek için bir yöntem, yıllık ya da iki yıllık bakım döngüsünün ötesinde ne sıklıkla sınama yapılacağına dair yönlendirme ve araç önerileri vermez. Genel bir iş maddesidir, BT maddesi değildir. Teknik kurtarma ayrıntıları için kendi platformlarınızın belgelerini ve rehberin felaket kurtarma planlama ve sınama becerilerini kullanın.

## İyi uygulamalar

1. **Bir iş etki çözümlemesiyle başlayın.** Kuruluşun vazgeçemeyeceği hizmetleri, kayıplarının zaman içindeki maliyetini ve neye bağlı olduklarını belirleyin. Bunu iş sahipleri için değil, onlarla birlikte yapın.
2. **Kurtarma hedeflerini işle birlikte belirleyin.** Her kritik hizmet için bir kurtarma süresi ve bir kurtarma noktası üzerinde uzlaşın ve bunları karşılamanın maliyetini kaydedin. İş ya da teknoloji değiştiğinde yeniden ele alın.
3. **Hizmetlerinizi kademelendirin.** Hizmetleri ne kadar çabuk geri gelmeleri gerektiğine göre gruplayın ve her kademeye uyan kurtarma yaklaşımını uygulayın. En pahalı yaklaşımı her şeye uygulamayın.
4. **İnsanların kullanabileceği kısa bir plan yazın.** Planın nasıl devreye alınacağını, kimin karar vereceğini, kimin ne yapacağını, nasıl iletişim kurulacağını ve kurtarma sırasını belirtin. Çalışma kılavuzlarına bağlantılarla birkaç sayfada tutun.
5. **Planları kodla ve ortamla birlikte tutun.** Kurtarma betiklerini, yapılandırmayı ve çalışma kılavuzlarını sürüm denetiminde saklayın ve hizmetler değiştiğinde gözden geçirin. Sistemle birlikte güncellenmeyen bir plan başarısız olur.
6. **Kurtarmanın dayandığı araçlar için plan yapın.** Teslimat hattına, sırlara, belgelere ve iletişim araçlarına erişimin, desteklediği sistemlerin kaybından sağ çıktığından emin olun.
7. **Düzenli olarak tatbikat yapın.** Masa başı tartışmalarla başlayın, geri yükleme ve yük devretme (failover) teknik sınamalarına geçin ve en kritik hizmetler için daha büyük tatbikatlar yapın. Bunları diğer işler gibi takvime koyun.
8. **Yalnızca yedekleri değil, geri yüklemeleri de sınayın.** Bir yedek, ondan geri yükleyerek kanıtlanır. Verilerin kurtarma noktası içinde geri geldiğini ve hizmetin onlarla çalıştığını sınayın (aşağıdaki felaket kurtarma sınaması becerisine bakın).
9. **Bulguları biriktirme listesi kalemleri olarak ele alın.** Her tatbikat boşluklar üretir. Bunları sahipleri ve tarihleriyle kaydedin ve bir sonraki tatbikattan önce yapıldıklarını denetleyin.
10. **İletişimi planlayın.** Müşterilere, personele, düzenleyicilere ve kamuoyuna kimin neyi söyleyeceğine karar verin ve şablonlar hazırlayın. Olağan kanallar çalışmıyorsa insanlara ulaşmanın bant dışı yollarını dahil edin (aşağıdaki kriz iletişimi becerisine bakın).
11. **Tedarikçileri dahil edin.** Kritik tedarikçilere kendi süreklilik düzenlemelerini sorun ve mümkün olduğunda onları tatbikatlara dahil edin (bkz. Konu 3.14 — Tedarikçi Yönetimi).
12. **Yıllık olarak ve her ciddi olaydan ya da büyük değişiklikten sonra gözden geçirin.** İş ya da teknoloji değiştiğinde, yalnızca takvime göre değil, çözümlemeyi, hedefleri ve planları güncelleyin.

## Ekibinizle tartışılacak sorular

**Hangi hizmetlerimiz önce geri gelmeli ve bunu nasıl biliyoruz?**

Her kişiden hizmetleri kurtarma önceliği sırasına dizmesini isteyin. Karşılaştırın. Anlaşmazlık bilgi vericidir: sıranın hiç işle uzlaşılmadığını gösterir. Kolaylaştırıcı, her birinin bir saat, bir gün ve bir hafta kapalı kalmasının kuruluşa neye mal olacağını sorabilir. Soruyu iş sahiplerine götürün ve bir liste üzerinde uzlaşın.

**Ne kadar veri kaybedebiliriz ve bunu kimse kabul etti mi?**

Kilit verilerin son yedeğinin ne zaman alındığını ve ne sıklıkla alındığını sorun. İşin tahammül edeceğiyle karşılaştırın. Birçok ekip yanıtın varsaydığı gibi olmadığını görür. Daha sıkı bir kurtarma noktasının neye mal olacağını tartışın. Kararı ve kimin verdiğini kaydedin.

**En son ne zaman bir yedekten geri yükledik ve ne oldu?**

Gerçek bir tarih ve gerçek bir sonuç isteyin. Yanıt "hiç" ise bu en önemli bulgudur. Yapıldıysa neyin ters gittiğini ve neyin düzeltildiğini sorun. Önümüzdeki ay içinde kritik bir hizmet için bir geri yükleme sınaması planlayın.

**Kurtarmamız gereken şeylerin arızalanan şeye bağlı olanları hangileri?**

Bir bulut hesabının ya da bir veri merkezinin kaybı gibi bir senaryoyu inceleyin. Çalışma kılavuzlarının, sırların ve hattın nerede yaşadığını sorun. Arızalanan sisteme bağımlılıklar yaygındır; örneğin kapalı bir sunucuda saklanan bir çalışma kılavuzu. Bunları listeleyin ve her birini taşımayı ya da kopyalamayı planlayın.

**Bir felaketi ilan etme ve planı başlatma yetkisi kimde?**

İnsanlara kimin karar vereceğini ve bunu bilip bilmediklerini sorun. Bir planı devreye almadaki gecikme zamana mal olur. Net bir kural ve bir vekil tartışın. Olağan kanallar çalışmıyorsa kişiye nasıl ulaşılacağını denetleyin.

**En çok şey bilen kişiler ulaşılamaz olsa ne yapardık?**

Kilit personelin ulaşılamaz olduğunu hayal edin. Kurtarmayı başka kimin yürütebileceğini ve neye ihtiyaç duyacağını sorun. Bu soru sürekliliği bilgi yönetimine bağlar. Kritik bilgiyi yaymak için bir yol planlayın.

## Uygulamada: çevik bir ITIL örneği

Bir eyalet hükümetinin tapu sicili, avukatların ve haritacıların mülk işlemlerini bildirdiği çevrim içi bir hizmet işletiyor. On iki kişilik bir ekip, tek bir bulut sağlayıcısı bölgesi kullanarak bunu geliştiriyor ve işletiyor. Bir iş sürekliliği gözden geçirmesi, hizmetin bakanlık tarafından kritik olarak sınıflandırıldığını, dört saat içinde geri getirilebileceği yönünde bir beklenti bulunduğunu ve bunun mümkün olup olmadığını hiç kimsenin sınamadığını ortaya koyuyor.

Ekip bir masa başı tatbikatla başlıyor. Senaryo: bulut bölgesi bir gün boyunca kullanılamıyor. Çalışma kılavuzlarının aynı bölgede barındırılan bir wiki'de saklandığını, kod olarak altyapının ortamın yalnızca bir kısmını kapsadığını ve veritabanı yedeklerinin aynı bölgeye kopyalandığını keşfediyorlar. Bakanlığın dört saatlik beklentisinin yıllar önce bir yönetici tarafından yazıldığı ve hiç maliyetlendirilmediği anlaşılıyor. Ekip ile bakanlığın iş sahibi buluşuyor. Sahip, bir günlük kesintinin tapu bildirim son tarihleri için ne anlama geldiğini açıklıyor ve ay sonundaki bildirim günlerinde dört saatin gerektiğini, ancak diğer zamanlarda sekiz saatin kabul edilebilir olduğunu kabul ediyor.

Ekip, çalışma kılavuzlarını ve yedekleri ikinci bir bölgeye kopyalıyor, kod olarak altyapıyı tamamlıyor ve bir günlük bir tatbikatta ortamı bir sınama bölgesinde koddan yeniden kuruyor. İlk deneme, çoğunlukla elle yapılan adımlar ve eksik bir sır yüzünden on bir saat sürüyor. Düzeltmelerden sonra ikinci deneme beş saat sürüyor. Bazı sorunlar sürüyor. Ay sonu için dört saatlik hedef hâlâ ulaşılamaz durumda, personelin oturum açmak için kullandığı kimlik sağlayıcının kendi kurtarma düzenlemesi yok ve ekip, süreklilik planını hiç görmediği bir tedarikçiye bağımlı olduğunu fark ediyor. Ekip kimlik sağlayıcıyı ve tedarikçi sorusunu biriktirme listesine koyuyor ve bakanlık, iş sürerken yoğun olmayan dönemler için daha uzun bir kurtarma süresini kabul ediyor.

## Dört bakış açısı

### Ürün ve teslimat ekipleri

Teslimat ekipleri tasarım yoluyla kurtarmayı mümkün ya da imkânsız kılar. Hizmetleri koddan yeniden kurulabilecek biçimde inşa edin, verileri çoğaltılmış tutun ve kurtarma adımlarını bitti tanımının parçası olarak yazın. Tatbikatlara katılın ve buldukları boşlukları düzeltin.

### Hizmet ve operasyon ekipleri

Operasyon ekipleri planları tutar ve tatbikatları yürütür. Planları kısa tutun ve çalışma kılavuzlarına bağlayın, geri yüklemeleri ve yük devretmeleri sınayın ve kurtarmanın bağımlılıklarını görünür kılın. Her tatbikatın bulgularını kapanana kadar izleyin.

### Liderlik ve yönetişim

Liderler hedefleri belirler ve bedelini öder. İş etki çözümlemesini ve kurtarma hedeflerini isteyin, neye mal olduklarını anlayın ve bir tatbikata katılın. Bazı hizmetlerin kurtarılmasının daha uzun süreceğini kabul edin ve bu kararı bilinçli olarak verin.

### Müşteriler ve kullanıcılar

Müşteriler ve kullanıcılar hizmetin devam etmesine ya da geri gelmesine bağlıdır. Sağlayıcıya hizmetsiz ne kadar kalabileceğinizi ve hangi veriyi kaybedemeyeceğinizi söyleyin. Süreklilik düzenlemelerini ve bir felakette ne yapmanız gerektiğini, örneğin acil işleri göndermek için alternatif bir yolu sorun.

## Yaygın başarısızlık biçimleri

- **Kimsenin sınamadığı bir plan.** İlk sınama felaketin kendisidir. Bunun yerine masa başı tatbikatlarla başlayın ve teknik geri yüklemelere ilerleyin.
- **Kimsenin uzlaşmadığı hedefler.** Kurtarma süresini ayrılmış biri yazmıştır. Bunun yerine kurtarma süresini ve noktasını iş sahipleriyle belirleyin ve maliyeti kaydedin.
- **Hiç geri yüklenmeyen yedekler.** Yedekler vardır ama geri yükleme başarısız olur. Bunun yerine geri yüklemeleri bir takvime göre sınayın ve süreyi ölçün.
- **Kurtarma, arızalanan şeye bağlıdır.** Çalışma kılavuzları, sırlar ve araçlar arızalanan sistemdedir. Bunun yerine kurtarmanın bağımlılıklarını haritalayın ve kopyalarını başka yerde tutun.
- **Her şey için tek kademe.** Tüm hizmetlere en pahalı işlem uygulanır ya da hiçbirine uygulanmaz. Bunun yerine hizmetleri ihtiyaca göre kademelendirin.
- **Güncelliğini yitirmiş planlar.** Sistemler değişir, planlar değişmez. Bunun yerine planları kodla birlikte tutun ve hizmetler değiştiğinde gözden geçirin.
- **İnsanları göz ardı etmek.** Planlar olağan personelin hazır olduğunu varsayar. Bunun yerine yokluk ve kanallar çöktüğünde iletişim için plan yapın.
- **Tedarikçileri göz ardı etmek.** Kritik bağımlılıkların süreklilik düzenlemeleri yoktur. Bunun yerine tedarikçilere sorun ve onları tatbikatlara dahil edin.

## Olgunluk modeli

| Boyut | Başlangıç | Gelişim | Standartlaştırma | Yönetim | Eşgüdüm |
|---|---|---|---|---|---|
| Etki çözümlemesi ve hedefler | Kritik hizmetler varsayılır | Bazı hizmetlerin kaba kurtarma hedefleri vardır | Kritik hizmetlerin maliyetleriyle birlikte uzlaşılmış kurtarma süresi ve noktası vardır | Hedefler tatbikat sonuçlarına ve iş değişikliğine karşı gözden geçirilir | Hedefler müşteriler, tedarikçiler ve düzenleyicilerle hizalanır |
| Planlar ve kurtarma tasarımı | Kurtarma doğaçlamadır | Bazı hizmetlerin kurtarma notları vardır | Kritik hizmetler için planlar ve kurtarma kodu vardır ve sistemle birlikte tutulur | Plan güncelliği ve kurtarma süresi ölçülür ve geliştirilir | Kurtarma hizmetler, ekipler ve tedarikçiler arasında eşgüdümlüdür |
| Tatbikatlar ve sınama | Çok az ya da hiç sınama yok | Bazı geri yüklemeler sınanır | Masa başı ve teknik sınamalar bir takvime göre yapılır | Bulgular kapanana kadar izlenir ve sınamalar riske göre ayarlanır | Tatbikatlar tedarikçileri içerir ve kuruluşlar arasında yayılır |
| İletişim ve insanlar | İletişim ad hoctur | Bazı iletişim listeleri vardır | Planlar kimin kime söyleyeceğini, bant dışı yollar ve vekillerle birlikte kapsar | İletişim ve kadro boşlukları ölçülür ve kapatılır | İletişim müşteriler, tedarikçiler ve düzenleyicilerle prova edilir |

## Kontrol listesi

- [ ] Kritik hizmetlerimizi iş sahipleriyle belirledik.
- [ ] Her kritik hizmetin maliyeti bilinen, uzlaşılmış bir kurtarma süresi ve kurtarma noktası var.
- [ ] Hizmetler, kurtarma ihtiyaçlarına uyan kademelere gruplanmıştır.
- [ ] Planı kimin devreye alabileceği ve onlara nasıl ulaşılacağıyla birlikte kısa bir kurtarma planı var.
- [ ] Kurtarma kodu, yapılandırma ve çalışma kılavuzları sürüm denetiminde ve değişikliklerle birlikte gözden geçiriliyor.
- [ ] Kurtarma için gereken çalışma kılavuzları, sırlar ve araçlar birincil ortamın kaybından sağ çıkıyor.
- [ ] Her kritik hizmet için son yılda bir yedekten geri yükleme sınandı.
- [ ] Son yılda bir masa başı tatbikat yapıldı ve bulgular izleniyor.
- [ ] İletişim şablonları ve bant dışı yollar var.
- [ ] Kritik tedarikçilere kendi süreklilik düzenlemeleri soruldu.

## Yapay zeka istemleri

**Amaç: bir iş etki çözümlemesi için soruları taslaklamak.**

```text
Help me prepare a business impact analysis for these services: [list services].

About the organization: [describe sector and who relies on the services].
Peak periods or deadlines: [list, or write "unknown"].
Rules or contracts that set recovery requirements, with source text: [paste, or write "none known"].

Write, for each service, a short set of questions to put to business owners about the impact of an outage after one hour, one day, and one week (financial, operational, reputational, legal), what data loss would be tolerable, what the service depends on, and what workarounds exist. Do not invent impacts or numbers. Ask clarifying questions first, and list what you are unsure of.
```

**Amaç: bir masa başı tatbikat planlamak.**

```text
Design a 90-minute tabletop exercise for [number] people from [teams] on this scenario: [describe, for example "our cloud region is unavailable for 24 hours"].

Services in scope: [list].
Existing plans and runbooks: [describe, or write "none"].

Give a timed plan with: the scenario released in three stages, prompts for each role, questions on dependencies of recovery (where runbooks, secrets, and tools live), decisions that must be made and who makes them, and a closing step that records gaps with owners and dates. Do not use real production access. Ask clarifying questions first, mark assumptions, and list what you are unsure of.
```

**Amaç: tatbikat notlarını bir boşluk listesine dönüştürmek.**

```text
Below are the notes from a continuity exercise: [paste what happened, what went wrong, what people said].

List the gaps found, grouped as: plan (what was missing or unclear), technology (what failed or was slow), people (who was missing or unsure), and dependencies (what recovery depended on that was itself unavailable). For each gap, suggest a backlog item title and a question about priority. Use only the notes. Do not invent causes. List what you are unsure of.
```

**Amaç: tek bir hizmet için kısa bir kurtarma planı taslağı yazmak.**

```text
Help me outline a recovery plan for [service].

What it does and who depends on it: [describe].
Agreed recovery time and recovery point, if any: [paste, or write "not agreed"].
Where it runs, where data and backups are kept: [describe].
Dependencies (other services, suppliers, identity, networks): [list].
People who can recover it: [roles].

Write a plan outline of no more than two pages: how it is invoked, who decides, communication, order of recovery steps (with links to runbooks as [LINK]), testing evidence needed, and how to return to normal. Mark each item that is an assumption. Do not invent recovery times. Ask clarifying questions first, and list what you are unsure of.
```

## Yapay zeka becerileri

- [business-continuity-plan](../../../../skills/business-continuity-plan/SKILL.md): kritik işlevleri ayakta tutmak için kuruluş düzeyinde planı yazmak için kullanın.
- [disaster-recovery-plan](../../../../skills/disaster-recovery-plan/SKILL.md): BT hizmetlerinin teknik kurtarmasını planlamak için kullanın.
- [disaster-recovery-testing](../../../../skills/disaster-recovery-testing/SKILL.md): geri yükleme ve yük devretme sınamaları tasarlamak için kullanın.
- [crisis-communication-plan](../../../../skills/crisis-communication-plan/SKILL.md): bir kesinti sırasında müşterilere, personele ve kamuoyuna ne söyleyeceğinizi planlamak için kullanın.
- [risk-register](../../../../skills/risk-register/SKILL.md): süreklilik risklerini ve nasıl yönetildiklerini kaydetmek için kullanın.

## Temel kaynaklar

- **Business continuity planning** (Wikipedia): sürekliliğin, iş etki çözümlemesinin, kurtarma hedeflerinin, tatbikatların ve standartların tanımları.
- **ISO 22301** (International Organization for Standardization): iş sürekliliği yönetim sistemleri için şartlar standardı; uyum iddiaları için standardı okuyun.
- **Incident management** (Wikipedia): sürekliliği olay müdahalesinin yanına yerleştiren çok alanlı genel bakış.
- **Embracing Risk** (*Site Reliability Engineering*, Google, sre.google): kurtarma hedeflerini çerçeveleyen güvenilirlik ekonomisi.

## Kaynakça

1. Business continuity planning — Wikipedia — https://en.wikipedia.org/wiki/Business_continuity_planning
2. Disaster recovery — Wikipedia (disambiguation page) — https://en.wikipedia.org/wiki/Disaster_recovery
3. Incident management — Wikipedia — https://en.wikipedia.org/wiki/Incident_management
4. Embracing Risk — Google SRE book, sre.google — https://sre.google/sre-book/embracing-risk/
5. ISO 22301 — Wikipedia — https://en.wikipedia.org/wiki/ISO_22301
6. Risk management — Wikipedia — https://en.wikipedia.org/wiki/Risk_management
7. Backup — Wikipedia — https://en.wikipedia.org/wiki/Backup
8. Infrastructure as code — Wikipedia — https://en.wikipedia.org/wiki/Infrastructure_as_code
