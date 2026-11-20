# Ürün ve Hizmet Sahipliği

**Ürün ve hizmet sahipliği, her ürüne veya hizmete hesap verebilir tek bir kişi ve onu geliştiren ve işleten tek bir ekip verir; böylece değer, kalite ve maliyet hakkındaki kararları sonuçlarıyla birlikte yaşayan kişiler alır.**

## Bu neden önemli

Birçok kurumda hiç kimse bir hizmetin tamamının sahibi değildir. Hizmeti bir proje geliştirir, bir operasyon ekibi işletir, bir tedarikçi bir parçasını sağlar, bir mali işler birimi de bedelini öder. Bir şey ters gittiğinde dört toplantı yapılır ama karar alınmaz. Kullanıcılar bir şeyin iyileştirilmesini istediğinde talep, kimseye ait olmayan bir kuyruğa düşer. Hizmet, ekiplerin arasında çürür.

Sahiplik bu sorunu doğrudan ele alır. İki şey ister: ürünün veya hizmetin değerinden hesap verebilir bir kişi ve onu geliştirmek, işletmek ve iyileştirmek için gereken becerilere ve yetkiye sahip bir ekip. Fikir bazı biçimlerde eskidir, bazılarında ise moda olmuştur; ayrıntılar kurumdan kuruma çok değişir. Bunu doğru kurmak, bu rehberdeki her şeyin işlemesi için en önemli koşullardan biridir.

Konunun arkasında iki fikir vardır. Birincisi, Scrum Guide'daki Product Owner'dır (Ürün Sahibi): ürünün değerini en üst düzeye çıkarmaktan ve ürün biriktirme listesini sıralamaktan sorumludur; bir kurul değil, tek bir kişidir (bkz. Konu 1.4 — Teslimat Tahmini ve Planlama Metrikleri). İkincisi, Amazon'un teknoloji direktörü Werner Vogels ile ilişkilendirilen ve 2006'da ACM Queue'da yayımlanan bir röportajdan gelen "you build it, you run it" (onu siz geliştirirsiniz, siz işletirsiniz) sloganıdır; bu rehber röportajı doğrudan okuyamamıştır (sayfa erişim hatası vermiştir) ve ikincil anlatımlardan bilmektedir. Bu anlatımların aktardığı kadarıyla Vogels, geliştiricilerin yazılımı duvarın ötesinden operasyona attığı eski modeli, geliştiricilerin yazılımlarının günlük işletimiyle ve müşteriyle temas halinde kaldığı bir modelle karşılaştırmıştır. [Ürün yönetimi hakkındaki Wikipedia maddesi](https://en.wikipedia.org/wiki/Product_management) disiplini genel olarak anlatır, ancak çevik ürün sahibi rolü veya hizmet sahipliği hakkında bir şey söylemez; bu nedenle bu konu bağlantıyı kurma işini yapar ve bunu açıkça belirtir.

## Temel kavramlar

### Ürün, hizmet, proje

| Terim | Yaygın kullanımdaki anlamı | Zaman ufku |
|---|---|---|
| **Proje** | Kapsamı, başlangıcı ve bitişi tanımlı geçici bir çaba | Kapsam teslim edildiğinde biter |
| **Ürün** | Müşterilere veya kullanıcılara sunulan, zaman içinde geliştirilen ve iyileştirilen bir şey | Değer yarattığı sürece devam eder |
| **Hizmet** | Başkalarına, maliyetlerin ve risklerin sahipliğini üstlenmeden değer sunma biçimi (bkz. Konu 2.1 — BT Hizmet Yönetimi) | Sunulduğu sürece devam eder |

Dijital bir ürün çoğu zaman aynı zamanda bir hizmettir: kullanıcılar onun iyi çalışmasına bağımlıdır. Ürün ile hizmet arasındaki ayrım, projeden sürekli sorumluluğa geçişten daha az önemlidir; Konu 1.9 — Çevik Yönetim bunu anlatır.

### Ürün yönetimi

Wikipedia maddesi ürün yönetimini, bir ürünü veya hizmeti planlama, geliştirme, piyasaya sürme ve yönetme iş süreci olarak tanımlar; bu süreç, ürünlerin hedef pazarın ihtiyaçlarını karşılamasını ve ürün yaşam döngüsü boyunca iş stratejisini desteklemesini sağlar. Ürün yöneticilerinin sorumluluklarını sıralar: ürün hattını günlük olarak yönetmek, iş gerekçesinin ve pazara sunumun sahibi olmak, müşteri araştırmasını ve rekabeti analiz etmek, gereksinimleri belgelemek, strateji belirleyip yol haritasını oluşturmak ve tasarım, geliştirme, pazarlama, satış, destek ve hukuk ile hizalanmak. Kavramı, Procter & Gamble başkanı Neil H. McElroy'un ürünleri yönetmek üzere "Brand Men" (marka adamları) isteyen 1931 tarihli bir notuna dayandırır. Ürün yöneticilerinin çoğunlukla kâr ve zarar sorumluluğuyla ölçüldüğünü söyler.

Madde, ürün yönetimini çevik Product Owner ile ilişkilendirmez; dolayısıyla bağlantı bu rehberin yorumudur: Product Owner ürünün değerinden sorumludur ve ürün biriktirme listesini sıralar; birçok kurumda daha geniş iş rolünü bir ürün yöneticisi üstlenir. Küçük ekiplerde ikisini tek kişi yapabilir.

### Ürün sahibi ve hizmet sahibi

| Rol | Hesap verdiği konu | Tipik sorular |
|---|---|---|
| **Ürün sahibi** (Scrum) | Ürünün değerini en üst düzeye çıkarmak; ürün biriktirme listesini sıralamak | Sırada neyi geliştirmeli veya iyileştirmeliyiz ve neden? |
| **Ürün yöneticisi** | Bir ürünün iş gerekçesi, stratejisi ve yol haritası | Bu doğru ürün mü, doğru pazar için mi? |
| **Hizmet sahibi** (BT hizmet yönetimi kullanımı) | Bir hizmetin ömrü boyunca performansı ve iyileştirilmesi | Hizmet, kullanıcıların ihtiyaçlarını kabul edilebilir bir maliyet ve riskle karşılıyor mu? |

Roller örtüşür. Bir iç BT hizmetinde tek kişi hem ürün sahibi hem hizmet sahibi olabilir. Scrum Guide, sıralama kararlarının net bir sahibi olması için Product Owner'ın bir kurul değil tek bir kişi olduğunu vurgular. Unvan ne olursa olsun ölçüt şudur: adı belli tek bir kişi yeni özellikler, güvenilirlik ve maliyet arasında ödünleşim yapabiliyor mu?

### "You build it, you run it"

Vogels'in 2006 röportajının ikincil özetlerinde anlatıldığı üzere bu ifade, bir hizmeti geliştiren ekibin onu aynı zamanda işlettiği ve böylece kullanıcılarla ve tasarımının sonuçlarıyla günlük temasta kaldığı bir modeli dile getirir. Röportajı Jim Gray yapmış ve 2006'da ACM Queue'da yayımlanmıştır; Amazon'un kendi blogu da röportaj çıktığında bunu duyurmuştur. Bu rehber özgün metni okumamıştır, bu nedenle ondan alıntı yapmaz. Modelin yararları kadar maliyetleri de vardır:

| Yarar | Maliyet veya risk |
|---|---|
| Geliştiriciler kötü işletilebilirliğin sıkıntısını hisseder ve düzeltir | Geliştiriciler nöbet yükü taşır ve tükenebilir |
| Kullanıcılardan ve olaylardan daha kısa geri bildirim | İşletim, güvenlik ve uyum becerileri ekipte bulunmalıdır |
| Bilgi kaybettiren devir teslim yok | Ekipler arası standartlar için başka mekanizmalar gerekir |
| Net hesap verebilirlik | Küçük ekipler tüm yükü fazla ağır bulabilir |

Site Reliability Engineering ve DevOps, bu tür ekipleri desteklemenin yollarını sunar (bkz. Konu 5.2 — DevOps ve Konu 5.3 — Site Reliability Engineering). Platform ekipleri ortak araçlar sağlayarak her ürün ekibinin bunları yeniden kurmasını önleyebilir.

### Sahip olan ekipler

Sahiplik, teslim edecek ve işletecek becerilere ve harekete geçme yetkisine sahip bir ekip gerektirir. Scrum, işinin bütünü için başkalarına bağımlı olmayan, küçük, çok işlevli ve kendi kendini yöneten bir ekibi tarif eder. Uygulamada ürün ekipleri ortak platformlara, güvenliğe ve veri hizmetlerine de bağımlıdır. Bu bağımlılıkları yönetmek sahipliğin parçasıdır (bkz. Konu 1.8 — Çevikliği Ölçeklendirme).

### Finansman ve hedefler

Sahiplik, istikrarlı finansman ve net hedefler gerektirir. Proje proje finanse edilen bir ekip, proje bittiğinde dağıtılır ve hizmet sahibinin ekibi kalmaz. Bir ürün veya hizmet için finanse edilen, hedefleri öğrendikçe değişen kalıcı bir ekip olağan yanıttır (bkz. Konu 1.9 — Çevik Yönetim). Hedefler, kullanıcılar ve iş için sonuçlarla ilgili olmalı ve sahiple birlikte belirlenmelidir.

### Hizmet yönetiminde sahiplik

ITIL uygulamalarının sahipleri olmalıdır: her hizmetin bir sahibi, her uygulamanın bir sahibi ve her büyük sürecin bir sahibi vardır (bkz. Konu 5.1 — Çevik Hizmet Yönetimi). Hizmet sahibi; hizmet seviyesini, katalog kaydını, iyileştirme listesini ve müşterilerle ilişkiyi elinde tutar (bkz. Konu 3.7 — Hizmet Seviyesi Yönetimi ve Konu 3.8 — Hizmet Kataloğu Yönetimi).

### Sınırlar ve uyarılar

Bu rehber için okunan kaynaklar, sahiplik modellerinin ne kadar iyi işlediğine dair kanıt sunmaz ve ürün yönetimi hakkındaki Wikipedia maddesi hiçbir eleştiri listelemez. Deneyimden gelen pratik uyarılar arasında unvanı olup yetkisi olmayan sahipler, birden çok ürünle aşırı yüklenmiş sahipler, destek olmadan uygulanan ve tükenmişliğe yol açan "you build it, you run it" ve değer akışı sınırı aşarken ekip sınırında duran sahiplik yer alır (bkz. Konu 5.4 — Değer Akışı Yönetimi).

## İyi uygulamalar

1. **Her ürün veya hizmet için hesap verebilir tek bir kişi belirleyin.** Adı hizmet kataloğuna yazın (ITIL bunu "service catalogue" diye yazar). Öncelikler üzerinde yetkisi ve finansmanda sözü olduğundan emin olun.
2. **Sahibin neye karar verdiğini tanımlayın.** Sahibin hangi kararları tek başına, hangilerini ekiple birlikte verdiğini ve hangilerinin üst makama taşınması gerektiğini belirtin. Bu olmadan sahiplik bir unvandan ibarettir.
3. **Sahibe zaman verin.** Birkaç büyük ürünün sahibi olan kişilere veya aynı zamanda tam bir teslimat işi olan kişilere bu rolü vermeyin. Sahiplik gerçek bir iştir.
4. **Ekibi hizmetin ömrü boyunca finanse edin.** Projeler bittiğinde ekipleri dağıtmaktan kaçının. Finansmanı düzenli bir döngüde sonuçlara göre gözden geçirin.
5. **Sonuç hedeflerini sahiple birlikte belirleyin.** Kullanıcılar ve iş için neyin daha iyi olması gerektiğini, ekibin kendi üretebileceği birkaç ölçümle tanımlayın (bkz. Konu 5.6 — Metrikler ve Ölçüm).
6. **Mümkün olduğunda geliştirmeyi ve işletmeyi tek ekipte toplayın.** Geliştirme, işletim ve destek becerilerini dahil edin ve ekibe üretim verilerine ve araçlarına güvenli sınırlar içinde erişim verin. Mümkün olmadığında güçlü çalışma anlaşmaları oluşturun.
7. **Ekibi bir platformla destekleyin.** Her ekip kendi aracını kurmasın diye dağıtım, izleme ve güvenlik için ortak araçlar sağlayın. Platformu kullanıcıları olan bir ürün olarak ele alın.
8. **Nöbet yükünü adil paylaştırın.** Gece çağrılarını sınırlayın, uyarıları ayarlayın ve tükenmişliği izleyin. "You build it, you run it", işletenler yorgun düştüğünde başarısız olur.
9. **Ürün başına tek bir biriktirme listesi tutun.** Özellikleri, kusurları, operasyon işlerini ve iyileştirme kalemlerini tek bir sıralı listede toplayın; böylece sahip bunları birbirleriyle tartabilir.
10. **Sahipleri birbirine bağlayın.** Çatışmaları çözmek ve planları hizalamak için bağımlı ürün ve hizmetlerin sahipleri arasında düzenli sohbetler yapın.
11. **Sahipliği yılda bir gözden geçirin.** Her hizmetin hâlâ etkin bir sahibi, bir ekibi ve bir biriktirme listesi olduğunu ve rollerin hâlâ uygun olduğunu kontrol edin.
12. **Küçük ekiplere pay bırakın.** Bir ekip birçok küçük hizmetin sahibiyse bunları mantıklı biçimde gruplayın ve hafif uygulamalar kullanın. Küçük bir hizmete ağır bir model uygulamayın.

## Ekibinizle tartışılacak sorular

**Hizmetlerimizin her biri için kim hesap verebilir ve kendisi de öyle der mi?**

Ana hizmetleri listeleyin ve sahibini yazın. Ardından adı geçen her kişiye kendisini sahip olarak görüp görmediğini sorun. Liste ile yanıtlar arasındaki boşluklar, sahipliğin ne kadarının görünüşte kaldığını ortaya çıkarır. Kolaylaştırıcı hangi hizmetin sahipsiz olduğunu ve bunun neye mal olduğunu sorabilir.

**Sahibimiz bugün kimseye sormadan neye karar verebilir?**

Örnekler isteyin: öncelikler, harcama, bir sürüm, bir müşteri taahhüdü. Kararların çoğu başkalarının onayını gerektiriyorsa hangilerinin hangi sınırlarla devredilmesi gerektiğini tartışın. Taşınacak tek bir karar üzerinde anlaşın.

**Üretimde bir şey ters gittiğinde kim uyandırılır ve düzeltmek için olanağı var mı?**

Kimin nöbette olduğunu ve neyi değiştirebildiğini sorun. Geliştiriciler değilse nedenini sorun. Olaylardan gelen geri bildirimin hizmeti tasarlayanlara nasıl ulaştığını tartışın. Kısaltılacak tek bir yol üzerinde anlaşın.

**Bu hizmeti nasıl finanse ediyoruz ve bir proje bittiğinde ne oluyor?**

Ana bir hizmetin finansmanını baştan sona izleyin. İyileştirmeler için kimin harcama yapabildiğini ve durdurma kararını kimin verdiğini sorun. Ekip bir projeden sonra dağıtılıyorsa kaybolan bilginin maliyetini tartışın. Bir hizmet için kalıcı finansman denemesi önerin.

**Hizmetimizi geliştirmek ve işletmek için hangi becerilerden yoksunuz ve bunları nasıl edinebiliriz?**

İşin gerektirdiği becerileri listeleyin: geliştirme, işletim, güvenlik, veri, destek. Boşlukları işaretleyin. Eşli çalışmayı, eğitimi, bir uzmanı ödünç almayı veya ortak bir platformu tartışın. Kapatılacak tek bir boşluk seçin.

**Tek bir kişiden kaç farklı sahip olmasını istiyoruz?**

Her sahibin sorumlu olduğu ürün ve hizmetleri sayın. Aşırı yüklenmiş sahipler iyi karar veremez. Bölmeyi, devretmeyi veya hizmetleri kullanımdan kaldırmayı tartışın. Bir üst sınır ve bu sınırı aşan bir sahip için bir plan üzerinde anlaşın.

## Uygulamada: çevik bir ITIL örneği

Ulusal bir istihdam kurumu, iş arayanların ve işverenlerin kullandığı bir çevrimiçi iş eşleştirme hizmeti işletmektedir. Hizmeti bir proje ekibi geliştirmiş, bir operasyon grubuna devretmiş ve şimdi bir dizi küçük proje olarak finanse edilmektedir. Dijital hizmetler başkanı, hizmetin sahibini kimsenin söyleyemediğini görür: asıl proje sponsoru emekli olmuş, olayları operasyon yönetmekte ve bir politika birimi değişiklikleri aylar süren bir kuyruk üzerinden istemektedir. İşverenler üç yıldır değişmeyen bir kayıt formundan şikâyetçidir.

Başkan, işveren ilişkileri biriminden, hem işverenleri hem hizmeti anlayan bir kişiyi hizmet sahibi olarak atar ve ona biriktirme listesi üzerinde söz hakkı ile bütçeden bir pay verir. Hizmet üzerinde zaten çalışan kişilerden, geliştiricileri, bir işletim mühendisini, bir test uzmanını ve bir tasarımcıyı bir araya getiren sekiz kişilik kalıcı bir ekip kurulur. Ekip, gece çağrılarına sınır konarak nöbet çizelgesine katılır ve merkezi bir ekibin bakımını yaptığı ortak bir dağıtım ve izleme platformunu kullanır. Politika biriminin talepleri tek biriktirme listesine girer; sahip bunları iyileştirmeler ve düzeltmelerle karşılaştırarak sıralar. Ekip ve sahip, yıl için birkaç ölçümle üç sonuç hedefi üzerinde anlaşır: tamamlanan işveren kayıtlarının oranı, iş arayanların bir eşleşme bulma süresi ve tekrarlayan olayların sayısı.

Sekiz ay sonra kayıt formu yeniden yapılır, tamamlama oranı iyileşir ve tekrarlayan olaylar azalır. Sahip, işverenlerin neyin planlandığına dair sorularını yanıtlayabilir. Bazı zorluklar sürer. Sahip aynı zamanda başka bir küçük hizmetten de sorumludur ve zorlanmaktadır, politika birimi biriktirme listesinde yer için rekabet etmek zorunda kalmaktan rahatsızdır ve nöbetçi mühendisler ortak platformda ihtiyaç duydukları bir aracın eksik olduğunu söylemektedir. Dijital hizmetler başkanı sahibin diğer görevlerini azaltır, politika birimi ile sahipten aylık bir planlama toplantısı kurmalarını ister ve platform talebini merkezi ekibin biriktirme listesine koyar.

## Dört bakış açısı

### Ürün ve teslimat ekipleri

Teslimat ekipleri net bir sahiple çalışmalı ve geliştirdikleri şeyin işletilmesini üstlenmelidir. Sahibe kullanıcılardan, olaylardan ve maliyetlerden kanıt sunun ve ödünleşimler konusunda dürüst olun. Nöbeti adil taşımak için gereken araçları ve desteği isteyin.

### Hizmet ve operasyon ekipleri

Operasyon ekipleri ürün ekiplerini uzmanlık, platformlar ve ortak standartlarla destekler. Başkaları için hizmet işlettiklerinde sahipleri belirleyin ve hizmet seviyeleri üzerinde anlaşın. Her operasyon sorununu hiçbir şeyin sahibi olmayan merkezi bir gruba devretmeye direnin.

### Liderlik ve yönetişim

Liderler sahipleri belirleyerek, onlara yetki ve zaman vererek ve kalıcı ekipleri finanse ederek sahiplik yaratır. Sahiplerden sonuç ve kanıt isteyin ve öncelikleri tartışmadan geçersiz kılmaktan kaçının. Unvanı olup gücü olmayan sahiplere dikkat edin.

### Müşteriler ve kullanıcılar

Müşteriler ve kullanıcılar, bir hizmetin hesabını kimin verdiğini bildiklerinde ve ona ulaşabildiklerinde yarar sağlar. Sahibe en çok neyin önemli olduğunu ve neyin acı verdiğini söyleyin. Nelerin planlandığına dair net bilgi ve önceliklerin nasıl belirlendiğinde söz hakkı bekleyin.

## Yaygın başarısızlık biçimleri

- **Yetkisiz unvan.** Sahip hiçbir şeye karar veremez. Bunun yerine sahibin neye karar verdiğini belirtin ve arkasında durun.
- **Kurul sahipliği.** Hiç kimse hesap vermez. Bunun yerine her ürün veya hizmet için tek bir kişiyi belirleyin.
- **Aşırı yüklenmiş sahipler.** Bir kişi çok fazla ürünün sahibidir. Bunun yerine sayıyı sınırlayın ve devredin.
- **Projelerden sonra ekipleri dağıtmak.** Bilgi ekiple birlikte gider. Bunun yerine sürekli hizmetler için kalıcı ekipleri finanse edin.
- **Destek olmadan "you build it, you run it".** Ekipler tükenir. Bunun yerine bir platform, paylaşılan nöbet ve ayarlanmış uyarılar sağlayın.
- **Ekipte biten sahiplik.** Değer akışı ekipleri aşar. Bunun yerine bağımlı hizmetlerin sahiplerini birbirine bağlayın.
- **Birden çok biriktirme listesi.** Özellikler, kusurlar ve operasyon işleri gizli kuyruklarda yarışır. Bunun yerine ürün başına tek bir sıralı biriktirme listesi tutun.
- **Bağlamsız model kopyalamak.** Büyük bir şirketin kalıbı küçük bir hizmete uygulanır. Bunun yerine modeli büyüklüğe ve riske uydurun.

## Olgunluk modeli

| Boyut | Başlangıç | Gelişim | Standartlaştırma | Yönetim | Eşgüdüm |
|---|---|---|---|---|---|
| Hesap verebilirlik | Hizmetlerin net bir sahibi yoktur | Bazı hizmetlerin resmî olmayan sahipleri vardır | Her hizmetin, tanımlı karar hakları ve zamanı olan adı belli bir sahibi vardır | Sahip etkinliği ve sonuçlar gözden geçirilir | Sahipler bağımlı hizmetler arasında ve müşterilerle eşgüdüm sağlar |
| Ekip ve beceriler | Geliştirme ve işletme ayrı ekiplerdir | Bazı ekipler nöbeti paylaşır | Kalıcı ekipler, ihtiyaç duydukları becerilerle geliştirme ve işletmenin sahibidir | Beceri boşlukları ve yük ölçülür ve ele alınır | Beceriler ve platformlar ekipler ve tedarikçiler arasında paylaşılır |
| Finansman ve hedefler | Finansman proje bazındadır | Bazı kalıcı ekipler vardır | Hizmetlerin kalıcı finansmanı ve sonuç hedefleri vardır | Finansman ölçülen sonuçları izler | Finansman ve hedefler hizmetler arasında ve müşterilerle hizalıdır |
| Biriktirme listesi ve öncelikler | Öncelikler birçok kuyruktan gelir | Bazı sahipler bir liste tutar | Ürün başına tek bir sıralı biriktirme listesi her tür işi içerir | Biriktirme listesi akışı ve öncelikler paydaşlarla gözden geçirilir | Öncelikler sahipler arasında ve müşterilerle hizalıdır |

## Kontrol listesi

- [ ] Her ürün veya hizmetin hizmet kataloğunda listelenmiş, adı belli ve hesap verebilir tek bir sahibi var.
- [ ] Her sahibin tek başına, ekiple birlikte ve üst makama taşıyarak neye karar verdiği yazılı.
- [ ] Sahiplerin rol için zamanı ve yönetilebilir sayıda hizmeti var.
- [ ] Her sürekli hizmet için kalıcı bir ekip finanse ediliyor.
- [ ] Her hizmetin birkaç ölçümle sonuç hedefleri var.
- [ ] Bir hizmeti geliştiren ekibin onu işletmek için becerileri ve erişimi var ya da işletenlerle net çalışma anlaşmaları var.
- [ ] Nöbet yükü sınırlarla ve ayarlanmış uyarılarla adil paylaşılıyor.
- [ ] Ortak bir platform, ekipleri dağıtım, izleme ve güvenlikle destekliyor.
- [ ] Her ürünün özellikleri, kusurları, operasyonu ve iyileştirmeyi kapsayan tek bir sıralı biriktirme listesi var.
- [ ] Sahiplik en az yılda bir gözden geçiriliyor.

## Yapay zeka istemleri

**Amaç: bir ürün veya hizmet sahibi için karar haklarını taslak olarak hazırlamak.**

```text
Help me draft decision rights for the owner of [product or service].

What the service does and who uses it: [describe].
Decisions that come up often: [list 8-12, such as priorities, spending, releases, customer commitments, supplier choices].
Rules we must follow (financial, security, legal), with source text if you have it: [paste, or write "none known"].
Current arrangement: [describe].

Produce a table with three columns: owner decides alone, owner decides with the team, and escalate. Place each decision in one column with a one-sentence reason. Mark any placement that is a guess. Do not invent rules. Ask clarifying questions first, and list what you are unsure of.
```

**Amaç: net bir sahibi olmayan hizmetleri bulmak.**

```text
Here is a list of our services with the owner we have recorded, the team that builds, the team that runs, and who funds each: [paste].

Using only this list, identify services with no owner, with different people named as owner by different columns, or with build and run split between teams. For each, suggest a question to ask. Do not decide who should own anything. List what you are unsure of.
```

**Amaç: hem geliştiren hem işleten bir ekip için nöbet modeli planlamak.**

```text
Help me plan an on-call model for a team of [number] people who build and run [service].

Current incidents and pages (counts by week, out-of-hours share): [paste real data].
Skills in the team: [list].
Constraints: [for example time zones, leave rules].

Propose a rota design, limits on night calls, how alerts will be tuned, what support the team needs from a platform or operations group, and what to review each quarter. Leave numeric limits as [to be agreed]. Do not invent data. Ask clarifying questions first, mark assumptions, and list what you are unsure of.
```

**Amaç: bir hizmetin kalıcı finansmanı için gerekçe hazırlamak.**

```text
Help me prepare a short case for funding [service] with a standing team instead of by project.

How it is funded today and what happens at the end of each project: [describe].
Costs of the current arrangement, in facts (rework, lost knowledge, delays; use only real examples): [paste].
What a standing team would need: [describe roles and rough size].
Outcome goals proposed: [list].

Write a one-page case with the problem, the proposal, risks (including the risk of a standing team becoming complacent), what we will measure, and how funding would be reviewed. Do not invent figures. Ask clarifying questions first, and list what you are unsure of.
```

## Yapay zeka becerileri

- [raci-matrix](../../../../skills/raci-matrix/SKILL.md): her ürün veya hizmet için kimin sahip olduğunu, kimin desteklediğini ve kime danışıldığını netleştirmek için kullanın.
- [product-roadmap](../../../../skills/product-roadmap/SKILL.md): bir ürün veya hizmetin yönünü ve yakın vadeli planlarını anlatmak için kullanın.
- [agile-charter](../../../../skills/agile-charter/SKILL.md): bir ekibin amacını, sonuçlarını ve sınırlarını başlangıçta belirlemek için kullanın.
- [feature-prioritization](../../../../skills/feature-prioritization/SKILL.md): bir sahibin biriktirme listesini değer ve maliyete göre sıralamasına yardımcı olmak için kullanın.
- [agile-discovery](../../../../skills/agile-discovery/SKILL.md): bir ürün veya hizmetin sırada ne yapması gerektiğini geliştirmeden önce doğrulamak için kullanın.

## Temel kaynaklar

- **The Scrum Guide** (Ken Schwaber ve Jeff Sutherland, scrumguides.org): Product Owner sorumluluğunun ve çok işlevli, kendi kendini yöneten ekibin tanımı.
- **Product management** (Wikipedia): disiplinin, sorumluluklarının ve tarihinin genel bir açıklaması.
- **A Conversation with Werner Vogels** (Jim Gray, ACM Queue, 2006): "you build it, you run it" ifadesinin anlatıldığı röportaj; kesin ifade için özgün metni okuyun.
- **Site Reliability Engineering** (Google, sre.google): geliştirdiğini işleten ekipleri desteklemenin bir yolu.

## Kaynakça

1. The Scrum Guide (November 2020) — Ken Schwaber and Jeff Sutherland, scrumguides.org — https://scrumguides.org/scrum-guide.html
2. Product management — Wikipedia — https://en.wikipedia.org/wiki/Product_management
3. ACM Queue interview with Werner Vogels (2006), noted on the AWS News Blog — Amazon Web Services — https://aws.amazon.com/blogs/aws/acm_queue_inter/
4. Introduction — Google SRE book, sre.google — https://sre.google/sre-book/introduction/
5. DevOps — Wikipedia — https://en.wikipedia.org/wiki/DevOps
6. Scrum (software development) — Wikipedia — https://en.wikipedia.org/wiki/Scrum_(software_development)
7. Project management — Wikipedia — https://en.wikipedia.org/wiki/Project_management
8. Site reliability engineering — Wikipedia — https://en.wikipedia.org/wiki/Site_reliability_engineering
9. Platform engineering — Wikipedia — https://en.wikipedia.org/wiki/Platform_engineering
