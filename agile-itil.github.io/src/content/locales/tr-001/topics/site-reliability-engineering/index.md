# Site Reliability Engineering

**Site reliability engineering operasyonu bir mühendislik sorunu olarak ele alır; hizmetleri hızlı değişmeye devam ederken güvenilir tutmak için hizmet seviyesi hedeflerini, hata bütçelerini ve tekrarlayan elle işe konan bir üst sınırı kullanır.**

## Bu neden önemli

Birçok hizmet yönetimi uygulaması, operasyon çalışanlarının başkalarının yazdığı yazılımı işlettiği ve işletme maliyetinin hizmetin boyutuyla birlikte büyüdüğü bir dünya için tasarlandı. Site reliability engineering (SRE), bu model çok büyük bir ölçeğe çarptığında ne olduğuna bir kuruluşun verdiği yanıttır: yazılım mühendislerinden operasyon işlevini tasarlamalarını ve işletmelerini isteyin ve insanların aksi halde elle yapacağı işi sisteme yaptırın.

Bu kılavuzun okuyucuları için SRE üç nedenle yararlıdır. Hız ile güvenilirlik arasındaki ödünleşimi, hem ürün hem operasyon ekiplerinin okuyabileceği sayılarla açık kılar. Ne kadar elle işin fazla olduğuna dair sağlam bir fikir verir. Ve olay, sorun, değişiklik ve kapasite yönetimi gibi birçok ITIL uygulamasının mühendislik terimleriyle nasıl yapılabileceğini gösterir. SRE bunları yapmanın tek yolu değildir ve çok büyük bir internet şirketinin koşullarından doğmuştur; bu nedenle neyin aktarılabileceği sizin durumunuza bağlıdır.

Bu konu esas olarak Google'ın *Site Reliability Engineering* kitabının üç bölümüne dayanır ve Wikipedia'daki SRE maddesiyle desteklenir. Kitap uygulamayı tek bir kuruluşta anlatır ve yaklaşımını savunur; Wikipedia maddesi daha geniş ama daha ince bir tablo verir ve hiçbir eleştiri anmaz. İkisini de bir standart olarak değil, sınanacak fikirlerin kaynakları olarak okuyun.

## Temel kavramlar

### SRE nedir

Kitabın girişi SRE'yi "bir yazılım mühendisinden bir operasyon ekibi tasarlamasını istediğinizde olan şey" olarak tanımlar. [Wikipedia'daki site reliability engineering maddesi](https://en.wikipedia.org/wiki/Site_reliability_engineering) onu, yazılım mühendisliği ve BT altyapı desteği içinde, dağıtılmış yazılımın ve büyük hizmetlerin erişilebilirliğini ve performansını izleyen ve iyileştiren, otomasyona ve kod olarak altyapıya odaklanan bir disiplin olarak anlatır. Madde SRE'yi DevOps'un belirli bir uygulaması olarak adlandırır; güvenilir sistemler kurmaya yoğunlaştığı için kapsamı daha dardır (bkz. Konu 5.2 — DevOps). Kitap DevOps'u, SRE'nin belirli bir biçimde uyguladığı daha geniş bir ilkeler kümesi olarak anlatır.

Maddeye göre Google'ın SRE uygulaması 2003'te Benjamin Treynor Sloss'un katılıp yedi üretim mühendisinden bir ekip kurmasıyla başladı; 2016'ya kadar ekipte 1.000'den fazla SRE vardı ve diğer büyük internet şirketleri uygulamayı benimsemişti. 572 profesyonelle yapılan 2020 tarihli bir anket, 10.000 veya daha fazla çalışanı olan kuruluşların yüzde 64'ünde, 101 ile 1.000 arasında olanların yüzde 44'ünde ve 100 veya daha azı olanların yüzde 32'sinde SRE ekipleri bulmuştur. SREcon konferans serisi 2014'ten beri her yıl yapılmaktadır.

### SRE'nin ele aldığı sorun

Giriş geleneksel modeli anlatır: geliştiriciler ve sistem yöneticileri ayrı ekiplere bölünmüştür. İki tür maliyeti adlandırır:

- **Doğrudan maliyetler.** Elle değişiklik yönetimi ve etkinlik ele alma pahalı hale gelir; çünkü operasyon ekibi yükle birlikte büyür.
- **Dolaylı maliyetler.** Ekiplerin farklı sözcük dağarcıkları, teşvikleri ve risk varsayımları vardır; bu da yayınlar üzerine çatışmaya yol açar. Operasyon devreye alma kapıları ekler, geliştiriciler de geçici çözümlerle karşılık verir.

SRE, operasyonu bir mühendislik sorunu olarak ele alarak bu bölünmeyi önlemeyi amaçlar. Bölüm, ekip boyutunun sistemden daha yavaş büyüdüğünü söyler; çünkü mühendislik operasyonel yükün trafikle birlikte büyümesini engeller.

### İlkeler

Giriş, SRE ekiplerinin sorumlu olduğu alanları listeler: erişilebilirlik, gecikme, performans, verimlilik, değişiklik yönetimi, izleme, acil durum müdahalesi ve kapasite planlaması. Wikipedia maddesi temel uygulamalar olarak şunları sıralar: tekrarlayan işi otomatikleştirmek; güvenilirlik hedeflerini hizmet seviyesi göstergeleri (SLI), hedefleri (SLO) ve hata bütçeleri aracılığıyla tanımlamak; riski azaltmak için sistemleri tasarlamak; gözlemlenebilirlik ve izleme; angaryayı yönetmek; test edilmiş bir olay yönetimi süreci; ve kapasite planlaması, sürüm yönetimi ve kaos mühendisliği.

### Hizmet seviyesi hedefleri ve hata bütçeleri

SRE güvenilirliği açık hedeflere bağlar (tam anlatım için bkz. Konu 3.7 — Hizmet Seviyesi Yönetimi). Kısaca:

- Kullanıcıların önemsediğini yansıtan birkaç gösterge seçin.
- Mükemmellik talep etmeyen bir hedef belirleyin.
- Bir **hata bütçesine (error budget)** izin verin: mükemmel ile hedef arasındaki boşluk.
- Bütçeyi yayın temposuna karar vermek için kullanın: bütçe kaldıkça yayınlar sürer; bütçe tükendiğinde yayınlar yavaşlar ve çaba güvenilirliğe kayar.

"Embracing Risk" bölümü nedenini açıklar: ürün ekipleri hız üzerinden, güvenilirlik ekipleri güvenilirlik üzerinden ölçülür; bu da gerilim yaratır ve bütçe ikisine ortak, nesnel bir ölçü verir. Aynı bölüm, güvenilirlik maliyetlerinin dik biçimde arttığını ve amacın bir hizmetin riskini işin kabul edeceği düzeye uydurmak olduğunu söyler (bkz. Konu 3.11 — Erişilebilirlik, Kapasite ve Performans).

### Angarya (toil)

"Eliminating Toil" bölümü **angaryayı (toil)** bir üretim hizmetini işletmeye bağlı operasyonel iş olarak tanımlar ve bunun yalnızca birinin hoşlanmadığı iş olmadığını ve toplantılar gibi genel giderden ayrı olduğunu söyler. Angarya genellikle şöyledir:

| Özellik | Anlamı |
|---|---|
| **Elle** | Adımları bir betik çalıştırsa bile uygulamalı insan çabası gerektirir |
| **Tekrarlayan** | Tekrar tekrar yapılır, yeni bir sorun değildir |
| **Otomatikleştirilebilir** | Bir makine yapabilir veya ihtiyaç tasarımla ortadan kaldırılabilir |
| **Taktik** | Kesinti güdümlü ve tepkiseldir; çağrılara yanıt vermek gibi |
| **Kalıcı değeri olmayan** | Sonrasında hizmet aynı durumdadır |
| **Büyümeyle doğrusal** | Çaba hizmetin boyutuyla, trafikle veya kullanıcılarla ölçeklenir |

Kitap, SRE'lerin angaryayı zamanlarının yüzde 50'sinin altında tutmayı, en az yarısını mühendislik proje işine ayırmayı hedeflediğini söyler; giriş toplam "ops" işine yüzde 50'lik bir üst sınır koyar ve fazlayı geliştirme ekiplerine geri gönderir. Çok fazla angaryanın kariyerde durgunluğa, düşük moral ve tükenmişliğe yol açtığını, özellik işini yavaşlattığını ve ayrılmaları artırdığını söyler; "angarya büyük miktarlarda deneyimlendiğinde zehirli hale gelir", ancak küçük miktarlar sakinleştirici olabilir ve bir kısmı kaçınılmazdır. Bölüm, nöbetin dayattığı tabanı hesaplamanın bir yolunu verir (örneğin örnek varsayımları altında altı kişilik bir çizelge için yüzde 33'lük bir alt sınır) ve kesintilerin en büyük angarya kaynağı olduğunu, bunu nöbet müdahalesinin, sonra yayınların izlediğini bildirir. Mühendislik işini yeni, yargı gerektiren, kalıcı iyileştirme üreten ve bir stratejiyi izleyen iş olarak tanımlar.

### Acil durum müdahalesi ve izleme

Giriş, izlemenin uyarıları yorumlamak için bir insana ihtiyaç duymaması gerektiğini söyler: yazılım veriyi yorumlar ve insanlar yalnızca eylem gerektiğinde bilgilendirilir (bkz. Konu 3.10 — İzleme ve Etkinlik Yönetimi). Nöbetçi SRE'lerin vardiya başına en fazla yaklaşık iki etkinlik alması gerektiğini söyler. Playbook'ların, doğaçlamaya kıyasla ortalama onarım süresinde yaklaşık üç kat iyileşme sağladığını iddia eder. Olay ele alma bir olay komuta yaklaşımını izler ve suçlamasız postmortem'ler tüm önemli olaylar için yazılır (bkz. Konu 3.2 — Olay Yönetimi).

### Değişiklik yönetimi

Giriş, kesintilerin kabaca yüzde 70'inin canlı bir sistemdeki değişikliklerden kaynaklandığını belirtir ve kademeli devreye almaları, hızlı sorun tespitini ve güvenli geri almaları önerir. Bu, kitabın Google'ın deneyiminden gelen kendi iddiasıdır ve her kuruluş için geçerli olmayabilir. Mesajı, DORA'nın değişikliğe ilişkin rehberliğiyle tutarlıdır (bkz. Konu 3.4 — Değişiklik Sağlama ve Konu 3.5 — Sürüm ve Dağıtım Yönetimi).

### SRE ve ITIL

SRE, birkaç ITIL uygulamasını yürütmenin mühendislik biçimi olarak okunabilir:

| ITIL uygulaması | SRE yaklaşımı |
|---|---|
| Olay yönetimi | Olay komuta rolleri, canlı bir olay kaydı, suçlamasız postmortem'ler |
| Sorun yönetimi | İş listesindeki postmortem eylemleri, angaryanın nedende giderilmesi |
| Değişiklik sağlama | Kademeli devreye almalar, hızlı tespit, güvenli geri alma, otomatik denetimler |
| Hizmet seviyesi yönetimi | SLI'lar, SLO'lar, hata bütçeleri |
| İzleme ve etkinlik yönetimi | Belirti tabanlı uyarı, dört altın sinyal |
| Kapasite yönetimi | Yük testiyle, mühendislik görevi olarak kapasite planlaması |
| Sürekli iyileştirme | Angaryaya bir üst sınır, ana iş olarak mühendislik projeleri |

Eşleme bu kılavuza aittir, kaynaklara değil. Ne kitap ne de Wikipedia maddesi ITIL'i uyguladığını iddia eder.

### Dağıtım modelleri

Wikipedia maddesi SRE için altı kurumsal model anlatır: "Kitchen Sink", altyapı, araçlar, ürün veya uygulama, gömülü ve danışmanlık. Büyük kuruluşlarda melez bir modelin yaygın olduğunu söyler, ancak bu iddiayı atıf gerektiren olarak işaretler. Hangi modelin size uyduğu boyutunuza ve hizmet sayınıza bağlıdır.

### Sınırlar ve eleştiriler

Wikipedia maddesi hiçbir eleştiri, maliyet veya başarısızlık biçimi belirtmez ve kitap tek bir kuruluşun başarısını anlatır. Pratik sınırlar deneyimden iyi bilinir ve burada öyle sunulur: SRE yazılım yazabilen ve operasyon yapmaya istekli mühendislere ihtiyaç duyar; yüzde 50'lik üst sınır yönetimin desteğini gerektirir; hata bütçeleri yalnızca ürün ekipleri onlara saygı gösterirse işler; ve yaklaşımı, onu üreten ölçek ve araçlar olmadan kopyalamak zordur. Daha küçük kuruluşlar, hedefler, bütçeler, angarya ölçümü ve suçlamasız gözden geçirme gibi fikirleri bir ekip kurmadan benimseyebilir.

## İyi uygulamalar

1. **Bir hizmet seçin ve bir hedef belirleyin.** Kullanıcı deneyimini yansıtan iki ila dört gösterge seçin, gevşek bir ilk hedef koyun ve sıkılaştırmadan önce birkaç ay ölçün.
2. **Bir hata bütçesi politikasında anlaşın.** Bütçe neredeyse tükendiğinde ve tükendiğinde ne olacağını ve kimin istisna yapabileceğini yazın. Bunu ürün ve operasyonun ortak kuralı yapın.
3. **Angaryayı ölçün.** İnsanlardan zamanlarının ne kadarının elle, tekrarlayan operasyonel işe gittiğini kaydetmelerini isteyin. Sınıflandırmak için altı özelliği kullanın. En büyük kaynaklara bakın.
4. **Elle işe üst sınır koyun.** Angarya için, bir kişinin zamanının yarısı gibi bir tavan belirleyin ve gözden geçirin. Sınır aşıldığında fazla işi nedenlerin sahibi ekiplere geri gönderin veya kapsamı azaltın.
5. **Önce en büyük angaryayı otomatikleştirin.** En çok zaman alan ve en tekrarlanabilir öğeyi seçin, testlerle otomatikleştirin ve tasarrufu ölçün. İhtiyacı tasarımla ortadan kaldırmayı otomatikleştirmeye tercih edin.
6. **Mühendislik zamanını koruyun.** Operasyon mühendisleri için proje işini sahipleri ve tarihleri olan gerçek iş olarak planlayın. O olmazsa angarya genişler.
7. **Kesintileri sınırlayın.** Nöbet vardiyası başına az etkinliği hedefleyin, çağrıların eyleme dönüştürülebilir olması için uyarıları ayarlayın ve tekrarlayan nedenleri düzeltin. Kitabın rehberliği vardiya başına en fazla yaklaşık iki etkinliktir.
8. **Playbook'lar yazın.** Yaygın arızalar için kısa, test edilmiş müdahale adımları yazın. Kitap bunların doğaçlamaya kıyasla onarım süresini iyileştirdiğini iddia eder.
9. **Değişiklikleri kademeli ve geri alınabilir yapın.** Kademeli devreye alın, sorunları hızla tespit edin ve güvenle geri alın. Kitabın deneyiminde değişiklikler kesintilerin en yaygın nedeni olduğundan önce buraya yatırım yapın.
10. **Önemli olaylar için suçlamasız postmortem'ler yürütün;** çağrı üretmeyen ramak kalalar dahil. Eylemleri iş listesi maddelerine dönüştürün.
11. **Ekiple değil, fikirlerle başlayın.** Daha küçük kuruluşlar, özel bir ekip kurmadan önce mevcut kadroyla hedefleri, bütçeleri, angarya ölçümlerini ve postmortem'leri benimseyebilir.
12. **Kurumsal modeli bilinçli seçin.** Bir SRE işlevi oluşturursanız araç sağlayıp sağlamayacağına, ürün ekipleriyle gömülü çalışıp çalışmayacağına veya danışmanlık yapıp yapmayacağına karar verin ve büyüdükçe seçimi gözden geçirin.

## Ekibinizle tartışılacak sorular

**Önce hangi hizmete bir hedef koyardık ve hedef ne olurdu?**

Herkesten hizmeti ve kullanıcının deneyimini en iyi yansıtan göstergeyi adlandırmasını isteyin. Karşılaştırın. Farklar belirsiz öncelikleri gösterir. Kolaylaştırıcı, hizmet kullanıcıların beklediğinden yavaş veya daha az erişilebilir olduğunda bugün ne olduğunu sorabilir. Başlanacak bir hizmette ve neyin ölçüleceğinde anlaşın.

**Bu ay tüm hata bütçemizi harcarsak ne yapardık?**

Ekipten ve bir ürün temsilcisinden eylemleri, kimin karar verdiğini ve neyin korunduğunu anlatmasını isteyin. Birçok ekip hiç anlaşmamıştır. Riskli yayınlara bir ara verilmesinin kabul edilip edilmeyeceğini tartışın. Bir sayfalık bir politika taslağı hazırlayın.

**Haftamızın ne kadarı angarya ve ilk üç kaynak hangileri?**

İnsanlardan tahmin etmelerini, sonra iki hafta kayıt tutmalarını isteyin. Tahminleri kayıtlarla karşılaştırın. Amaç işin biçimini görmektir, suçlamak değil. En büyük kaynağı seçin ve tasarımla ortadan kaldırılıp kaldırılamayacağını sorun.

**Hangi tekrarlayan elle görevi bir betik veya bir tasarım değişikliği ortadan kaldırabilir?**

İnsanların bıktığı görevleri listeleyin. Her biri için sıklığı ve süreyi tahmin edin. En iyi adaylar sık, istikrarlı ve düşük risklidir. Otomasyonu neyin güvenli kılacağını, örneğin sınırlar ve günlükler, sorun. Otomatikleştirilecek birini seçin.

**Her nöbet vardiyası kaç etkinlik alıyor ve kaçı eylem gerektiriyor?**

Son çeyrek için sayın. Sayı yüksekse nereden geldiğini tartışın. Giriş vardiya başına yaklaşık iki etkinliği hedeflemeyi önerir. Düzeltilecek bir uyarı kaynağı seçin.

**Özel bir güvenilirlik ekibi kursaydık neyi kaybeder, neyi kazanırdık?**

Dürüst görüşler isteyin. Kazanımlar odak ve beceriler olabilir; kayıplar yeni bir silo veya operasyonel işin boşaltılması olabilir. Gömülü mühendisler veya bir rotasyon gibi alternatifleri tartışın. Küçük ölçekte neyi deneyeceğinize karar verin.

## Uygulamada: çevik bir ITIL örneği

Bölgesel bir elektrik dağıtıcısı bir kesinti bildirme uygulaması ve bir saha ekibi sevk sistemi işletiyor. On sekiz kişilik birleşik bir ekip ikisini de geliştiriyor ve işletiyor. Ekipteki operasyon çalışanları zamanlarının çoğunu elle işe harcıyor: takılan işleri yeniden başlatmak, veri akışlarını ayarlamak ve çağrılara yanıt vermek. Grup başkanı onların iyileştirme için çok az zaman kaldığını not ediyor ve ikisi başka ekiplere geçmek istedi.

Ekip lideri SRE'den esinlenen bir yaklaşım öneriyor. Kesinti bildirme uygulaması için ekip iki gösterge belirliyor: başarılı olan bildirim gönderimlerinin payı ve bir onayı göstermek için geçen süre. Müşteri hizmetleri yöneticisiyle gevşek bir hedefte ve aylık bir hata bütçesinde anlaşıyor ve bir sayfalık bir politika yazıyor: bütçenin dörtte üçünden fazlası harcandığında riskli yayınlar bekler. Ekip mühendislerden bir ay angarya günlüğü tutmalarını istiyor. Günlük, zamanlarının üçte birinin arızalanan bir veri içe aktarma işini yeniden başlatmaya ve talebin sıçradığı fırtınalardan sonraki elle ayarlamalara gittiğini gösteriyor. Angaryaya zamanlarının yarısı sınırı koyuyor, önce içe aktarma işinin nedenini düzeltmeye karar veriyor ve fırtına ayarlamalarını sınırları ve günlüğü olan bir betikle otomatikleştiriyorlar. Çağrılar, nöbetçi mühendisi yalnızca kullanıcıya görünen belirtiler uyaracak biçimde ayarlanıyor.

Dört ay sonra angarya ekibin zamanının yaklaşık üçte birine düşüyor, içe aktarma işi artık arızalanmıyor ve hata bütçesi politikası bir tedarikçi kesintisi olan bir ayda bir özellik yayınını ertelemek için bir kez kullanıldı. Zorluklar sürüyor. Sevk sisteminin henüz hedefleri yok ve müşteri hizmetleri yöneticisi acil özellikler için bütçe politikasını iki kez aşmaya yöneldi. Ekip lideri ve yönetici istisnaları aylık gözden geçirmeye ve sıradaki hedefleri sevk için belirlemeye karar veriyor. Ayrıca "üst sınır"ın bir söz değil bir rehber olduğunu öğreniyorlar: büyük bir fırtınadan sonra angarya iki hafta boyunca yarısının çok üzerine çıktı ve neyi keseceklerine karar vermeleri gerekti.

## Dört bakış açısı

### Ürün ve teslimat ekipleri

Teslimat ekipleri hedeflerin belirlenmesine katılır ve bütçeye saygı gösterir. Özelliklere işletilebilirlik inşa edin, angaryanın onu doğuran ekibe geri döndüğünü kabul edin ve otomasyona yardım edin. Tükenmiş bir bütçeyi bir ceza olarak değil, hizmet hakkında bilgi olarak görün.

### Hizmet ve operasyon ekipleri

Operasyon ekipleri SRE işini yapabilir veya fikirlerini benimseyebilir. Angaryayı ölçün, mühendislik için zamanı koruyun ve tekrar eden işi kaynağına geri itin. Bazı işlerin neden reddedilmesi gerektiğini açıklamak için hedefleri kullanın.

### Liderlik ve yönetişim

Liderler angarya üst sınırını ve hata bütçesi kuralını desteklemelidir; destek olmadan başarısız olurlar. Olay sayısını değil, hedefleri ve bütçe durumunu isteyin. Mühendislik işi için zaman sağlayın ve bütçe tükendiğinde özelliklere hayır demeye hazır olun.

### Müşteriler ve kullanıcılar

Müşteriler ve kullanıcılar net hizmet seviyelerinden ve işler bozulduğunda daha hızlı kurtarmadan yarar sağlar. Hedeflerin deneyiminizi yansıtması için ekibe en çok neyin önemli olduğunu söyleyin. Yeni özellikler ile güvenilirlik arasındaki ödünleşimler hakkında dürüst konuşmalar bekleyin.

## Yaygın başarısızlık biçimleri

- **Unvanı kopyalamak.** Operasyon yeniden adlandırılır ve hiçbir şey değişmez. Bunun yerine önce hedefleri, bütçeleri ve angarya ölçümlerini benimseyin.
- **Kimsenin saygı göstermediği bir hata bütçesi.** Özellikler onu her seferinde aşar. Bunun yerine kuralı ürün sahipleriyle anlaşın ve istisnaları gözden geçirin.
- **Mühendisliğe zaman olmaması.** Angarya haftayı doldurur. Bunun yerine ona sınır koyun ve proje zamanını koruyun.
- **Yanlış şeyi otomatikleştirmek.** Nadir bir görev otomatikleştirilirken sık olan kalır. Bunun yerine zaman ve sıklığa göre sıralayın.
- **Mükemmellik hedefleri.** Hedefler yüzde 100 talep eder. Bunun yerine kullanıcı ihtiyaçlarından gevşek hedefler koyun ve veriyle sıkılaştırın.
- **Çöp sahası olarak güvenilirlik ekibi.** Geliştirme tüm operasyonel işi ona gönderir. Bunun yerine fazla işi kaynağına geri döndürün.
- **Google'ın ölçeğini kopyalamak.** Büyük bir kuruluş gerektiren uygulamalar küçük bir kuruluş tarafından benimsenir. Bunun yerine hedefler ve postmortem'ler gibi uyan fikirleri alın.
- **İnsanları göz ardı etmek.** Nöbet yükü insanları tüketir. Bunun yerine vardiya başına etkinlikleri sınırlayın ve çizelgeyi paylaşın.

## Olgunluk modeli

| Boyut | Başlangıç | Gelişim | Standartlaştırma | Yönetim | Eşgüdüm |
|---|---|---|---|---|---|
| Hedefler ve bütçeler | Güvenilirlik hedefleri gayriresmîdir | Bazı hizmetlerin hedefleri vardır | Temel hizmetlerin hedefleri ve üzerinde anlaşılmış bir hata bütçesi politikası vardır | Bütçeler yayınlara yön verir ve politika istisnaları gözden geçirilir | Hedefler ve bütçeler bağımlı hizmetler arasında hizalanır |
| Angarya ve otomasyon | Angarya ölçülmez | Bazı ekipler angaryayı tahmin eder | Angarya ölçülür ve sınırlanır; otomasyon işi planlanır | Angarya kaynakları ve tasarruflar izlenir ve azaltılır | Otomasyon paylaşılır ve angarya ekipler genelinde azaltılır |
| Acil durum müdahalesi | Müdahale doğaçlamadır | Bazı playbook'lar ve bir çizelge vardır | Roller, playbook'lar ve suçlamasız postmortem'ler standarttır | Etkinlik yükü ve onarım süreleri ölçülür ve iyileştirilir | Müdahale ekipler ve tedarikçiler arasında prova edilir ve eşgüdümlüdür |
| Değişiklik ve kapasite | Değişiklikler risklidir ve elle yapılır | Bazı devreye almalar kademelidir | Kademeli devreye alma ve kapasite planlaması rutindir | Değişiklik başarısızlığı ve kapasite tahminleri ölçülür | Değişiklik ve kapasite uygulamaları kuruluş genelinde paylaşılır |

## Kontrol listesi

- [ ] En az bir hizmetin göstergeleri ve zaman içinde ölçülen gevşek bir hedefi var.
- [ ] Ürün sahipleriyle bir hata bütçesi politikası üzerinde anlaşıldı ve yazıldı.
- [ ] Angarya tutarlı bir tanımla ölçülüyor ve ilk kaynaklar biliniyor.
- [ ] Angarya için bir tavan var ve gözden geçiriliyor.
- [ ] Mühendislik projeleri için zaman planlanıyor ve korunuyor.
- [ ] Nöbet yükü ölçülüyor ve çağrılar eyleme dönüştürülebilir.
- [ ] En yaygın arızalar için playbook'lar var ve test edildi.
- [ ] Devreye almalar kademeli ve geri almalar test ediliyor.
- [ ] Önemli olaylar ve ramak kalalar sahipli eylemlerle suçlamasız postmortem alıyor.
- [ ] Güvenilirlik işinin nasıl organize edileceğini bilinçli olarak seçtik.

## Yapay zeka istemleri

**Amaç: işinizi angarya, mühendislik veya genel gider olarak sınıflandırmak.**

```text
Here is a list of what our operations engineers did in the last two weeks, with the time spent on each: [paste real data].

Classify each item as toil, engineering work, or overhead, using these definitions. Toil: manual, repetitive, automatable, tactical, without enduring value, and growing linearly with the service. Engineering work: novel, requires judgment, produces permanent improvement. Overhead: administrative work not tied to running a service. Give a one-sentence reason from my text for each. Compute the share of time in each class from my numbers only, and list the three largest toil items. Mark items you could not classify. Do not invent time figures. List what you are unsure of.
```

**Amaç: bir hata bütçesi politikası taslağı hazırlamak.**

```text
Draft a one-page error budget policy for [service].

Objective and period: [for example, "99.9% of purchase requests succeed, per month"].
Release rhythm and who decides: [describe].
Customer and product concerns: [list].

Write sections: how the budget is calculated and shown, what happens at three stages of consumption (leave thresholds as [to be agreed]), who can override and how overrides are recorded, how the policy is reviewed, and what we do after an exhausted budget. Do not invent numbers. Ask clarifying questions first, and list what you are unsure of.
```

**Amaç: önce otomatikleştirilecek bir angarya öğesi seçmek.**

```text
Here are our top toil items with how often each occurs, time per occurrence, risk if the automation fails, and whether the cause could be designed away: [paste].

Rank them by total time saved per month (computed from my numbers only). For the top three, say whether I should design the need away or automate it, and what safeguards the automation needs (tests, limits, logs). Do not invent numbers. Ask clarifying questions first, and list what you are unsure of.
```

**Amaç: bir playbook girdisi yazmak.**

```text
Write a playbook entry for this recurring failure: [describe symptom and impact].

What I know about causes and fixes: [paste].
Who to escalate to: [role, or "unknown"].

Provide a short entry: how to confirm the failure, the first checks, the usual fix, how to confirm recovery, when to escalate, and what to record. Mark any step you inferred with [CHECK]. Ask clarifying questions first, and list what you are unsure of.
```

## Yapay zeka becerileri

- [on-call-rotation](../../../../skills/on-call-rotation/SKILL.md): vardiya başına etkinliklere sınır koyan adil bir çizelge tasarlamak için kullanın.
- [runbook](../../../../skills/runbook/SKILL.md): onarımı hızlandıran playbook'ları yazmak için kullanın.
- [postmortem](../../../../skills/postmortem/SKILL.md): suçlamasız gözden geçirmeler yürütmek ve eylemleri izlemek için kullanın.
- [chaos-testing](../../../../skills/chaos-testing/SKILL.md): güvenilirlik tasarımlarının çalıştığını, güvenli biçimde arızalar yaratarak sınamak için kullanın.
- [capacity-planning](../../../../skills/capacity-planning/SKILL.md): kapasiteyi talebe bağlı bir mühendislik görevi olarak planlamak için kullanın.

## Temel kaynaklar

- **Introduction** (*Site Reliability Engineering*, Google, sre.google): SRE'nin tanımı, yüzde 50 üst sınırı, ilkeler ve kaçınmayı amaçladığı geliştirme/operasyon bölünmesi.
- **Eliminating Toil** (*Site Reliability Engineering*, Google, sre.google): angaryanın tanımı ve ona üst sınır koymanın nedenleri.
- **Embracing Risk** (*Site Reliability Engineering*, Google, sre.google): güvenilirliğin ekonomisi ve hata bütçesi.
- **Site reliability engineering** (Wikipedia): disiplinin daha geniş bir özeti, dağıtım modelleri, benimseme anketi ve ileri okuma.

## Kaynakça

1. Introduction — Google SRE book, sre.google — https://sre.google/sre-book/introduction/
2. Eliminating Toil — Google SRE book, sre.google — https://sre.google/sre-book/eliminating-toil/
3. Embracing Risk — Google SRE book, sre.google — https://sre.google/sre-book/embracing-risk/
4. Site reliability engineering — Wikipedia — https://en.wikipedia.org/wiki/Site_reliability_engineering
5. DevOps — Wikipedia — https://en.wikipedia.org/wiki/DevOps
6. Chaos engineering — Wikipedia — https://en.wikipedia.org/wiki/Chaos_engineering
7. Infrastructure as code — Wikipedia — https://en.wikipedia.org/wiki/Infrastructure_as_code
8. Observability (software) — Wikipedia — https://en.wikipedia.org/wiki/Observability_(software)
9. Incident management — Wikipedia — https://en.wikipedia.org/wiki/Incident_management
