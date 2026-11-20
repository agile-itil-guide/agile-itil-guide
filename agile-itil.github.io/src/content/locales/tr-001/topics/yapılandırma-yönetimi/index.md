# Yapılandırma Yönetimi

**Yapılandırma yönetimi, bir hizmetin parçalarının ve bunların birbiriyle ilişkisinin doğru ve kullanılabilir bir resmini tutar; modern biçimi ise koddan ve keşiften üretilen, sistemin kendisi güncel tuttuğu için güvenilen bir kayıttır.**

## Bu neden önemli

Bir şey bozulduğunda ilk sorular hep aynıdır. Bu bileşen nedir? Neye bağlanır? Ne değişti? Sahibi kim? Yanıtları bulmak bir saat sürüyorsa, dakikalar içinde çözülebilecek bir olay uzar gider. Bir değişiklik planlandığında aynı sorular riski anlayıp anlamadığınıza karar verir. Hizmetin ve parçalarının iyi bir resmi, bir operasyon ekibinin sahip olabileceği en yararlı şeylerden biridir.

Aynı zamanda doğru tutulması en zor şeylerden biridir. Bir kez çizilen altyapı belgeleri haftalar içinde eskir. Elle sürdürülen bileşen veritabanları kimsenin göremediği biçimlerde yanlıştır. Çevik ve bulut çalışma biçimleri bunu bir yönden kötüleştirir, çok sayıda küçük ve hızlı değişen parçayla; bir yönden iyileştirir, çünkü yapılandırma kod olarak yazılabilir, sürüm denetiminde saklanabilir ve otomatik olarak uygulanabilir.

İngilizce Wikipedia'nın yapılandırma yönetimi maddesi onu, bir ürünün nitelikleri ile gereksinimleri, tasarımı ve operasyonel bilgisi arasındaki tutarlılığı ömrü boyunca kurmak ve sürdürmek için bir yönetim süreci olarak tanımlar; kökleri 1950'lerde ABD Savunma Bakanlığı'na uzanır. Yapılandırma yönetim veritabanları maddesi, yapılandırma öğeleri ve ilişkilerinin deposu için ITIL terimini anlatır. Kod olarak altyapı maddesi, kaynakların makine tarafından okunabilir tanım dosyalarıyla yönetilmesini anlatır. Bunlar birlikte geleneksel görüşü ve modern görüşü verir; bu konu ikisini birleştirir.

## Temel kavramlar

### Genel olarak yapılandırma yönetimi

Wikipedia'ya göre yapılandırma yönetimi (CM) askeri sistemlerde, ITIL kapsamında BT hizmet yönetiminde ve inşaat mühendisliğinde kullanılır. Tarihçesi, donanım için teknik bir disiplin olarak 1950'lerde ABD Savunma Bakanlığı'nda başlar; 1960'ların sonu ve 1970'lerdeki askeri standartlar onu başlı başına bir disiplin haline getirmiştir. Madde ANSI/EIA-649, ISO 10007 (2017 sürümü) ve IEEE 828-2012 dahil birkaç standardı anar. Askeri el kitaplarından ve EIA standardından sıraladığı temel disiplinler şunlardır:

| Disiplin | Ne yapar |
|---|---|
| **Planlama ve yönetim** | İnsanları, eğitimi, adlandırma kurallarını, denetimleri ve satıcı gereksinimlerini kapsayan bir plan |
| **Yapılandırma tanımlama** | Mimariyi ve bileşenleri tanımlayan temel çizgileri (baseline) belirlemek ve sürdürmek; izlenen ürünler **yapılandırma öğeleridir (CI)** |
| **Yapılandırma denetimi** | Değişiklik taleplerini değerlendirmek ve onaylamak ya da reddetmek |
| **Yapılandırma durum muhasebesi** | CI tanımlarını ve temel çizgiden sapmaları kaydetmek ve raporlamak |
| **Doğrulama ve denetim** | Sistemin belgelerine ve gereksinimlerine uyduğunun bağımsız kontrolleri |

**Temel çizgi (baseline)**, üzerinde anlaşılmış bir referans noktasıdır; bir nitelik temel çizgiye bağlandığında değişiklikler resmî denetimden geçer, değerlendirilir, onaylanır ve sonra yeniden temel çizgiye bağlanır. Madde yapılandırma yönetimini, BT varlıklarının mali muhasebesine ve değerine odaklanan varlık yönetiminden ayırır (bkz. Konu 4.1 — BT Varlık Yönetimi).

### Yazılım yapılandırma yönetimi

Madde yazılım yapılandırma yönetimini, yazılım niteliklerini çeşitli noktalarda tanımlamak ve bütünlüğü ile izlenebilirliği korumak için değişiklikleri denetlemek olarak anlatır; tanımlama, denetim, durum muhasebesi ve denetimler olmak üzere aynı dört prosedürle. Sürüm denetim sistemleri, derleme araçları ve sürüm kayıtları modern örneklerdir.

### Yapılandırma yönetim veritabanı

Wikipedia **yapılandırma yönetim veritabanını (CMDB)**, bir kuruluşun donanım ve yazılım varlıkları olan CI'lara ve bunlar arasındaki ilişkilere dair bilgileri saklayan bir veritabanı için kullanılan ITIL terimi olarak tanımlar. Bu veritabanı "BT ortamının önemli bileşenlerinin yetkilendirilmiş yapılandırmasını temsil eder." Maddeden temel noktalar:

- **CI'ların nitelikleri vardır;** bir tanımlayıcı, adlar, açıklamalar, sahiplik ve önem gibi, ki bunlar yüzlerce olabilir.
- **İlişkiler** genellikle bir kaynak CI'yı bir hedef CI'ya bağlar. Daha gelişmiş ilişkiler, bir veritabanının bir uygulamanın bileşeni olması gibi bir tanımlayıcı ekler.
- **Federasyon:** uygulamalar çoğu zaman varlık yönetimi gibi kaynaklardan verileri federe eder; böylece her kaynak kendi verisinin denetimini korur; madde bunu verilerin CMDB'ye kopyalanmasıyla karşılaştırır.
- **Kullanımlar:** etki analizi, kök neden analizi, değişiklik yönetimi, olay yönetimi, envanter ve derlemeler.
- **CI türleri:** donanım, yazılım, iletişim ve ağlar, konum, belgelendirme ve insanlar; olgun kuruluşlar ürünler ve satıcılar gibi iş türleri ekler.
- **Zorluklar:** uygunluk (her CI'nın yaşam döngüsü boyunca veri toplamak), bakım (birkaç uzman rol gerektiren, veri kalitesini yüksek tutmak) ve kullanılabilirlik (CMDB'ler çoğu zaman görselleştirmeden yoksun düz veritabanlarıdır, bu yüzden ek bir uygulama katmanı gerekebilir).

Madde, CI'ların otomatik keşfini ve değişiklik izlemeyi temel başarı etkenleri olarak anar. Kuruluş tarihi, belirli bir ITIL sürümü veya benimsenme verisi belirtmez ve daha fazla atıf gerektiği etiketini taşır. Ayrıca ITIL'in süreci ITIL sürüm 3'te Hizmet Varlığı ve Yapılandırma Yönetimi olarak yeniden adlandırdığını söyler (bu bilgi yapılandırma yönetimi maddesinden gelir).

### Kod olarak altyapı

Kod olarak altyapı maddesi, veri merkezi kaynaklarını elle kurulum veya etkileşimli araçlar yerine, tanımları sürüm denetiminde tutulan makine tarafından okunabilir tanım dosyalarıyla yönetme ve sağlama uygulamasını anlatır. Şu ayrımı yapar:

- **Bildirimsel (declarative)** yaklaşımlar istenen son durumu tanımlar ve adımları sistemin bulmasına izin verir; **buyruksal (imperative)** yaklaşımlar ise komutları sırayla belirtir. Madde, IaC'nin daha sık bildirimsel tanımlar kullandığını söyler.
- **İtme (push)** yöntemlerinde bir denetim sistemi sunuculara talimat gönderir, **çekme (pull)** yöntemlerinde ise sunucular kendi talimatlarını alır.

CFEngine'den (1993) Terraform, Ansible, Puppet, Chef, Pulumi ve OpenTofu'ya kadar birçok aracı anar ve uygulamayı, geliştiricileri yapılandırmaya dahil ederek ve operasyonu daha erken devreye alarak DevOps ile ilişkilendirir. Maliyet, hız ve azalan insan hatası konusundaki yarar iddiaları atıf gerektiği etiketini taşır. Unit 42'nin 2020 tarihli bir raporuna atıf yapar; bu rapor IaC şablonlarında yaklaşık 200.000 olası güvenlik açığı bulmuştur, kodun da kusur taşıyabileceğinin bir hatırlatıcısıdır. Madde yapılandırma sapmasından (configuration drift) veya eşgüçlülükten (idempotence) söz etmez.

### Bildirilen ve keşfedilen yapılandırma

Modern yapılandırma yönetimini düşünmenin yararlı bir yolu, iki doğruluk kaynağı olduğu ve değerin bunları karşılaştırmakta yattığıdır:

| Kaynak | Ne söyler | Güçlü yön | Zayıf yön |
|---|---|---|---|
| **Bildirilen** (sürüm denetimindeki kod, tanımlar) | Sistemin ne olmasını amaçladığımız | Gözden geçirilebilir, sürümlenmiş, tekrarlanabilir | Çalışan şeyle eşleşmeyebilir |
| **Keşfedilen** (taramalar, bulut API'leri, ajanlar) | Şu anda ne var | Gerçekliği yansıtır | Ne amaçlandığını veya nedenini söylemez |

Her ikisiyle beslenen bir CMDB, amaçlanan ile gerçek durum arasındaki fark olan **sapmayı (drift)** gösterebilir. Bu kılavuz için okunan kaynaklar sözcüğü kullanmaz, ancak o, CM disiplinlerinden durum muhasebesi ve denetimin yakalamak üzere tasarlandığı sorunu adlandırır.

### Yapılandırma yönetimi ve değişiklik

Yapılandırma denetimi ve değişiklik sağlama yakın ortaklardır (bkz. Konu 3.4 — Değişiklik Sağlama). CM disiplinleri, temel çizgiye bağlanmış öğelerdeki değişikliklerin değerlendirilip onaylandığını söyler. Hat tabanlı bir düzende, altyapıyı tanımlayan koddaki bir değişiklik diğerleri gibi gözden geçirilir ve test edilir; hattın kaydı kimin neyi ne zaman değiştirdiğini gösterir. CMDB veya eşdeğeri de sonucu yansıtır.

### Hizmet yönetiminde kullanımlar

Yapılandırma verisinde kaydedilen ilişkiler diğer uygulamalar genelindeki soruları yanıtlar:

- **Olaylar:** bu arızalı bileşene ne bağlı ve sahibi kim (bkz. Konu 3.2 — Olay Yönetimi)?
- **Sorunlar:** hangi bileşenler tekrarlayan olaylarda yer aldı (bkz. Konu 3.3 — Sorun Yönetimi)?
- **Değişiklikler:** bu değişikliğin patlama yarıçapı (blast radius) nedir?
- **Süreklilik:** neyin, hangi sırayla kurtarılması gerekir (bkz. Konu 3.12 — Hizmet Sürekliliği Yönetimi)?
- **Güvenlik:** neler açıkta ve ne değişti?

### Kaynakların sınırları

Yapılandırma yönetimi maddesi yeniden yazılmaya ihtiyaç duyabileceği etiketini taşır ve pratik uygulama hakkında az şey söyler. CMDB maddesinin bir eleştiri bölümü yoktur ve atıfları azdır. Sahadaki deneyim, CMDB'lerin çoğu zaman çok fazlasını, çok doğru, çok uzun süre tutmaya çalışarak başarısız olduğudur. Bunu bu kılavuzun sunduğu pratik deneyim olarak ele alın, kaynaklardan çıkan bir bulgu olarak değil.

## İyi uygulamalar

1. **Yanıtlamanız gereken sorulardan başlayın.** Olaya müdahale edenlerin, değişiklik gözden geçirenlerin ve süreklilik planlayıcılarının sorduğu soruları, örneğin "buna ne bağlı?" ve "sahibi kim?" gibi, listeleyin. Yalnızca bunları yanıtlayanı kaydedin.
2. **Küçük bir yapılandırma öğesi türü kümesi tanımlayın.** Hizmetler, uygulamalar, konaklar veya kapsayıcılar, veritabanları ve temel dış bağımlılıklarla başlayın. Bir soru gerektirdiğinde tür ekleyin.
3. **Yalnızca öğeleri değil, ilişkileri de kaydedin.** Hangi öğenin hangisine bağlı olduğunu ve hangi hizmeti desteklediğini yakalayın. İlişkiler veriyi etki analizi için yararlı kılar.
4. **Her öğe için bir sahip belirleyin.** Sahipsiz öğe bir risktir. Sahipliği öğelerin nasıl oluşturulduğunun bir parçası yapın.
5. **Amaçlanan yapılandırmayı sürüm denetiminde tutun.** Altyapıyı ve yapılandırmayı kod olarak ifade edin, diğer kodlar gibi gözden geçirin ve hattın uygulamasına izin verin. Depo böylece niyetin ve geçmişin kaydı olur.
6. **Gerçekliği bulmak için keşfi kullanın.** Var olanı görmek için ağları ve bulut hesaplarını tarayın ve bildirilen yapılandırmayla karşılaştırın. Farkları (sapmayı) görmezden gelmek yerine inceleyin.
7. **Mümkün olduğunda kopyalamak yerine federe edin.** Her veri kaynağının (varlık kaydı, bulut hesapları, dağıtım araçları) kendi gerçeklerinin sahibi olmasına izin verin ve CMDB maddesinin anlattığı gibi yapılandırma verisinden onlara bağlantı verin.
8. **Güncellemeleri otomatikleştirin.** Yapılandırma verisini hattan ve keşiften besleyin; böylece sistem değiştikçe o da değişir. Elle güncellemeler geride kalır.
9. **Önemli olanı temel çizgiye bağlayın.** Kritik hizmetler için onaylı yapılandırmayı kaydedin ve ondan sapmalara resmî değişiklik denetimi uygulayın. Geri kalanı için daha hafif denetim yeterlidir.
10. **Düzenli denetleyin.** Her çeyrekte bir öğe örneklemi için veriyi gerçeklikle karşılaştırın ve herhangi bir farkın arkasındaki süreci düzeltin. Bu, uygulamada doğrulama ve denetim disiplinidir.
11. **Veriyi kullanımı kolay kılın.** Müdahale edenler ve planlayıcılar için görselleştirme ve arama sağlayın; çünkü hızla okunamayan veri kullanılmaz.
12. **Güvenliği gözden kaçırmayın.** Yapılandırma kodunu hassas olarak ele alın, şablonları zayıflıklar için tarayın ve temel çizgiyi kimin değiştirebileceğini denetleyin. Kod olarak altyapı maddesindeki Unit 42 rakamı riskin bir hatırlatıcısıdır.

## Ekibinizle tartışılacak sorular

**Bir olay olduğunda, arızalı bileşene neyin bağlı olduğunu bulmamız ne kadar sürüyor?**

Son olaya ve bu soruya harcanan zamana bakın. Yanıtın nereden geldiğini sorun: bir diyagram, bir kişi, bir arama. Kolaylaştırıcı, en çok zamanı neyin kurtaracağını sorabilir. Çoğu zaman bu, en önemli hizmetler için bir bağımlılık ve sahip listesidir. Bir hizmet için bir tane üretmekte anlaşın.

**Altyapımız nerede tanımlı ve bu çalışan şeyle eşleşiyor mu?**

Ana ortamların koddan kurulup kurulmadığını ve birinin bunları ne sıklıkla elle değiştirdiğini sorun. Farkları arayın. Bilmiyorsanız bir ortam için karşılaştırma planlayın. Elle değişiklikleri nasıl önleyeceğinizi veya hızla tespit edeceğinizi tartışın.

**Yapılandırma kayıtlarımızdaki hangi öğelerin sahibi yok veya son zamanlarda doğrulanmadı?**

Bir örneklem alın ve sayın. Neden bu durumda olduklarını sorun: sahipler için süreç yok, hatırlatma yok, sonuç yok. Yıllık bir doğrulama veya oluşturulurken zorunlu bir sahip etiketi gibi hafif bir mekanizmayı tartışın. Birini seçin.

**Kimsenin kullanmadığı hangi verileri tutuyoruz?**

Alanları ve kayıt türlerini listeleyin ve son çeyrekte kimin kullandığını sorun. CMDB maddesi bakımı temel bir zorluk olarak anar ve kullanılmayan veri, yararı olmayan bir maliyettir. Kimsenin kullanmadığını kaldırın veya sürdürmeyi bırakın.

**Kritik bir hizmette bir değişikliği güvenle onaylayabilmek için neyi görmemiz gerekir?**

Gözden geçirenlere sorun. Tipik yanıtlar: değişikliğin neye dokunduğu, neyin ona bağlı olduğu, geçen sefer ne yaptığı. Bunlardan hangisini yapılandırma verisinin verebildiğini sorun. Eklenecek eksik bir parça seçin.

**Kritik hizmetlerimizin temel çizgisini kimin değiştirmesine izin var ve bunu yaptıklarında nasıl anlarız?**

Listeyi ve değişikliklerin kanıtını isteyin. Hat dışındaki değişikliklerin tespit edilip edilmediğini tartışın. Sapmanın nasıl bulunacağında ve kimin harekete geçeceğinde anlaşın.

## Uygulamada: çevik bir ITIL örneği

Ulusal bir vergi idaresi 120 uygulama ve şirket içi sunucular ile bulut hizmetlerinin bir karışımını işletiyor. Altı operasyon mühendisinden oluşan bir ekip, üç yıl önce bir elektronik tablodan yüklenmiş bir CMDB'yi sürdürüyor. Beyanname portalındaki büyük bir olay sırasında mühendisler, CMDB'nin bir yıl önce emekliye ayrılmış bir veritabanı sunucusunu listelediğini ve gerçekte arızalanan yük dengeleyiciyi atladığını keşfediyor. Portalın neye bağlı olduğunu çözmek o kadar uzun sürdüğü için olay üç saat daha geç çözülüyor.

Operasyon başkanı ve bir mühendis, müdahale edenlerin hangi soruları sorduğunu gözden geçiriyor. CMDB'nin kapsamını hizmetlere, uygulamalara, bunların arkasındaki ana altyapı bileşenlerine ve temel dış bağımlılıklara daraltıyor, düşük değerli türleri bırakıyorlar. Beyanname portalının altyapısı sürüm denetimindeki koda taşınıyor ve hat, dağıtılan her bileşenin kaydını CMDB'ye yazıyor. Ağın ve bulut hesaplarının bir keşif taraması her gece çalışıyor ve bir rapor bildirilen ile keşfedilen veri arasındaki farkları listeliyor. Her öğenin bir sahip alanı var ve rapor bunu da kontrol ediyor. Verilerden beyanname portalı için basit bir bağımlılık görünümü oluşturuluyor.

Bir çeyrek sonra, portalın bağımlılık görünümü sonraki olay ekibinin ilk on dakikada kullanacağı kadar doğru. Gecelik fark raporu 14 yönetilmeyen sunucu buluyor; bunların çoğu emekliye ayrılmış veya sahipleri tarafından sahiplenmiş. Sorunlar sürüyor. Beyanname portalı dışındaki hizmetler hâlâ eski verilere dayanıyor ve bir ekip, hattın sonradan üzerine yazdığı bir veritabanı sunucusunda elle değişiklik yapmaya devam ederek kısa bir kesintiye neden oluyor. Operasyon başkanı yaklaşımı sonraki üç hizmete genişletiyor, üretim değişikliklerinin hattan geçmesi kuralını ekliyor ve keşif raporundan elle değişiklikleri işaretlemesini istiyor.

## Dört bakış açısı

### Ürün ve teslimat ekipleri

Teslimat ekipleri yapılandırmayı kodla tanımlar. Altyapıyı ve ayarları sürüm denetimine koyun, gözden geçirin ve hattın uygulamasına izin verin. Kaynakları sahip ve hizmetle etiketleyin ve bağımlılıkları depoda veya hizmet kaydında tanımlayın.

### Hizmet ve operasyon ekipleri

Operasyon ekipleri yapılandırma verisini kullanır ve sürdürür. Kapsamı küçük tutun, bildirilen ve keşfedilen yapılandırmayı karşılaştırın ve sapmanın peşinden gidin. Olaylardan öğrendiklerinizi kaydettiğiniz türlere ve ilişkilere geri besleyin.

### Liderlik ve yönetişim

Liderler yapılandırma verisinin ne kadar çabayı hak ettiğine karar verir. Etki analizi ve süreklilik planlaması gibi hangi kararları desteklediğini sorun ve kullanıma göre yargılayın. Kendi başına dev bir veritabanını fonlamaktan kaçının. Kayıtları doğru tutan hat denetimlerini destekleyin.

### Müşteriler ve kullanıcılar

Müşteriler ve kullanıcılar, olaylar daha hızlı çözüldüğünde ve değişiklikler daha az bozulduğunda yarar sağlar; iyi yapılandırma verisi buna yardımcı olur. Veriyi nadiren görürler. Sağlayıcılara, bir değişikliğin neyi etkilediğini nasıl bildiklerini ve bir kesintinin nedenini nasıl bulduklarını sorun.

## Yaygın başarısızlık biçimleri

- **Her şeyi kaydetmeye çalışmak.** Veri, doğru tutulamayacak kadar büyüktür. Bunun yerine sorulardan ve kritik hizmetlerden başlayın.
- **Elle bakım.** Kayıtlar geride kalır. Bunun yerine veriyi hattan ve keşiften besleyin.
- **İlişki olmaması.** Öğeler listelenir ama bağlanmaz. Bunun yerine bağımlılıkları ve her öğenin desteklediği hizmeti yakalayın.
- **Sahip olmaması.** Kimse kayıtları doğrulamaz veya düzeltmez. Bunun yerine bir sahip zorunlu kılın ve düzenli olarak kontrol edin.
- **Hat dışı elle değişiklikler.** Gerçeklik ve niyet birbirinden ayrışır. Bunun yerine değişiklikleri hattan geçirin ve sapmayı tespit edin.
- **Okunamayan veri.** Müdahale edenler veritabanını kullanamaz. Bunun yerine arama ve görselleştirme sağlayın.
- **Federe etmek yerine kopyalamak.** Çoğaltılmış veri eskir. Bunun yerine gerçeklerin sahibi olan kaynağa bağlantı verin.
- **Yapılandırma kodunun zararsız sayılması.** Şablonlar güvenlik açıkları taşır. Bunun yerine onları tarayın ve gözden geçirin.

## Olgunluk modeli

| Boyut | Başlangıç | Gelişim | Standartlaştırma | Yönetim | Eşgüdüm |
|---|---|---|---|---|---|
| Kapsam ve ilişkiler | Bileşenler gayriresmî olarak bilinir | Bazı hizmetlerin bileşen listeleri vardır | Temel hizmetler için öğeler, sahipler ve bağımlılıklar kaydedilir | Kapsama ve doğruluk ölçülür, boşluklar kapatılır | Yapılandırma verisi ekipleri, bulutları ve tedarikçileri kapsar |
| Bildirilen yapılandırma | Sistemler elle yapılandırılır | Bazı ortamlar kod kullanır | Temel hizmetlerin altyapısı ve yapılandırması sürüm denetiminde koddur | Değişiklik geçmişi ve sapma izlenir | Yapılandırma kodu ekipler arasında paylaşılır ve yeniden kullanılır |
| Keşif ve doğrulama | Gerçeklik varsayılır | Ara sıra taramalar yapılır | Düzenli keşif bildirilen veriyle karşılaştırılır | Farklar ve nedenleri ölçülür ve azaltılır | Keşif ve doğrulama kuruluş genelinde otomatiktir |
| Verinin kullanımı | Veriye nadiren başvurulur | Bazı olaylarda kullanılır | Olaylar, değişiklikler ve süreklilik planlaması için rutin olarak kullanılır | Kullanım ve yarar ölçülür ve veri iyileştirilir | Veri, kuruluş genelinde ve ortaklarla birlikte kararları destekler |

## Kontrol listesi

- [ ] Müdahale edenlerimizin ve gözden geçirenlerimizin yapılandırma verisinin yanıtlamasını istediği soruları listeledik.
- [ ] Sahipleri ve ilişkileri olan küçük bir öğe türü kümesi kaydediyoruz.
- [ ] Temel hizmetlerin altyapısı ve yapılandırması sürüm denetiminde.
- [ ] Bu hizmetlerdeki üretim değişiklikleri hattan geçiyor.
- [ ] Keşif sonuçları bir takvimle bildirilen yapılandırmayla karşılaştırılıyor.
- [ ] Farklar (sapma) inceleniyor ve düzeltiliyor.
- [ ] Mümkün olan yerde kayıtlar hattan ve keşiften otomatik besleniyor.
- [ ] Kayıtların bir örneklemi her çeyrek gerçeklikle denetleniyor.
- [ ] Veri, müdahale edenler tarafından kolayca aranabiliyor ve görselleştirilebiliyor.
- [ ] Yapılandırma kodu gözden geçiriliyor ve zayıflıklar için taranıyor.

## Yapay zeka istemleri

**Amaç: yanıtlamanız gereken soruları listeleyerek neyin kaydedileceğine karar vermek.**

```text
Help me decide what configuration data to record for [service].

The questions responders and change reviewers ask, in our words: [list].
What we record today: [describe, or write "nothing"].
Where data lives (tools, repositories, cloud accounts): [list].

For each question, say what item types and relationships would be needed to answer it, where the data could come from automatically, and what would still need a person. Propose a minimal set of item types and fields. Mark guesses. Do not invent tools we do not have. Ask clarifying questions first, and list what you are unsure of.
```

**Amaç: bildirilen ve keşfedilen yapılandırma arasındaki sapmayı özetlemek.**

```text
Here is a list of items found by discovery and a list of items declared in our configuration code or records.

Discovered: [paste names or IDs, with type and key attributes].
Declared: [paste names or IDs, with type and key attributes].

Using only these lists, identify items found but not declared, items declared but not found, and items where attributes differ. Group them and suggest a question to ask about each group (for example whether it is retired, owned by someone else, or created by hand). Do not guess the cause. List what you are unsure of.
```

**Amaç: bir hizmet için bağımlılık görünümü oluşturmak.**

```text
Help me describe the dependencies of [service] so that responders can use them in an incident.

What the service does: [describe].
Components I know (applications, databases, network, cloud services, external suppliers): [list with how they connect].
Owners I know: [list].

Produce a simple text diagram and a table with: component, what depends on it, owner (or "unknown"), and what to check first if it fails (only from my text; otherwise "ask owner"). Highlight single points of failure that appear in my description. Do not invent components. Ask clarifying questions first, and list what you are unsure of.
```

**Amaç: yapılandırma kayıtlarının üç aylık denetimini planlamak.**

```text
Plan a one-hour quarterly audit of our configuration records for [scope].

How records are created and updated today: [describe].
Sample size we can handle: [number].

Give a method: how to choose a sample, how to check each item against reality, what to record, how to calculate the share that is accurate (from the audit results only), and how to turn errors into process fixes. Keep it tool-free. Ask clarifying questions first, mark assumptions, and list what you are unsure of.
```

## Yapay zeka becerileri

- [configuration-management](../../../../skills/configuration-management/SKILL.md): neyin kaydedileceğini, nasıl doğru tutulacağını ve nasıl kullanılacağını planlamak için kullanın.
- [change-request](../../../../skills/change-request/SKILL.md): etkilenen öğelere atıf yapan değişiklik kayıtları yazmak için kullanın.
- [runbook](../../../../skills/runbook/SKILL.md): yapılandırma bilgisini müdahale edenlerin izleyebileceği adımlara dönüştürmek için kullanın.
- [enterprise-architecture](../../../../skills/enterprise-architecture/SKILL.md): hizmetleri, uygulamaları ve altyapıyı bir mimari resim içine yerleştirmek için kullanın.
- [evolutionary-architecture](../../../../skills/evolutionary-architecture/SKILL.md): yapılandırma ve tasarımın zaman içinde güvenle değişmesini sağlamak için kullanın.

## Temel kaynaklar

- **Configuration management** (Wikipedia): yapılandırma yönetiminin tarihçesi, temel disiplinleri, temel çizgileri ve standartları.
- **Configuration management database** (Wikipedia): bir CMDB'nin tanımı, içeriği, kullanımları ve zorlukları.
- **Infrastructure as code** (Wikipedia): kaynakların makine tarafından okunabilir tanımlarla yönetilmesi; araç listesi ile yararlar ve risklere dair notlarla.
- **ITIL** (Wikipedia): CMDB'nin ve yapılandırma yönetiminin yer aldığı çerçeve.

## Kaynakça

1. Configuration management — Wikipedia — https://en.wikipedia.org/wiki/Configuration_management
2. Configuration management database — Wikipedia — https://en.wikipedia.org/wiki/Configuration_management_database
3. Infrastructure as code — Wikipedia — https://en.wikipedia.org/wiki/Infrastructure_as_code
4. ITIL — Wikipedia — https://en.wikipedia.org/wiki/ITIL
5. IT asset management — Wikipedia — https://en.wikipedia.org/wiki/IT_asset_management
6. Software configuration management — Wikipedia — https://en.wikipedia.org/wiki/Software_configuration_management
7. Version control — Wikipedia — https://en.wikipedia.org/wiki/Version_control
8. DevOps — Wikipedia — https://en.wikipedia.org/wiki/DevOps
9. Change management — Wikipedia — https://en.wikipedia.org/wiki/Change_management
