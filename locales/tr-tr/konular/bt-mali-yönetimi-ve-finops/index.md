# BT Mali Yönetimi ve FinOps

**BT mali yönetimi hizmetlerin neye mal olduğunu ve karşılığında hangi değeri getirdiğini gösterir; FinOps ise mühendisleri, finans ve iş ekiplerini bir araya getirerek teknoloji harcamasının, özellikle bulutta, gerçekleştiği anda anlaşılmasını ve yönetilmesini sağlayan kültürel bir uygulamadır.**

## Bu neden önemli

Para, hangi hizmetlerin var olduğuna, ne kadar iyi kadrolandığına ve ne kadar süre dayandığına karar verir. Yıllar boyunca BT finansı yıllık bir bütçe, bir maliyet dağıtım elektronik tablosu ve ağın bedelini kimin ödeyeceğine dair ara sıra yapılan tartışmalar anlamına geldi. Bulut bilişim bunu değiştirdi. Kaynaklar, doğru izinlere sahip herkes tarafından saniyeler içinde oluşturulabilir ve faturalama kullanımı izler. Yanlış yapılandırılmış tek bir iş, kimse fark etmeden aylık faturaya binlerce ekleyebilir; düşünceli bir değişiklik de bu kadar tasarruf sağlayabilir.

Çevik ekipler için bu kayma iki ucu keskin bir kılıçtır. Donanım beklemeden deneme yapma ve ölçeklenme özgürlüğü kazanırlar. Aynı zamanda eskiden finans ve satın almada duran bir sorumluluğu üstlenirler: seçimlerinin neye mal olduğunu bilmek. Bu arada yıllık döngülerle planlama yapan finans çalışanları günlük değişen bir kullanımla karşılaşır. İki taraf da maliyeti tek başına iyi yönetemez.

İngilizce Wikipedia'da kontrol edilen adreste "FinOps" başlıklı bir madde yoktur. FinOps Foundation'ın kendi sitesi FinOps'u, mühendislik, finans ve iş ekipleri arasındaki işbirliğiyle teknolojinin iş değerini en üst düzeye çıkaran ve mali hesap verebilirlik yaratan operasyonel bir çerçeve ve kültürel bir uygulama olarak tanımlar. Wikipedia'daki bulut bilişim maddesi fiyatlandırma modellerini ve maliyet denetimini anlatır ve bazı bölümlerinin doğrulanmamış olabileceğine dair bir bakım bildirimi taşır. ITIL'in buradaki mali sözcük dağarcığı, örneğin bütçeleme, muhasebe ve ücretlendirme, çerçeve sahibinin metnine karşı doğrulanamayan, yaygın biçimde yayımlanmış anlatımlardan alınmıştır.

## Temel kavramlar

### BT mali yönetimi

BT mali yönetimi (ITIL'de "BT hizmetleri için mali yönetim") yaygın olarak bir BT hizmet sağlayıcısının parasını yönetme uygulaması olarak tanımlanır: bütçeleri planlamak, maliyetleri muhasebeleştirmek ve ilgili yerde hizmetler için ücret almak. Amacı, karar vericilere maliyeti değerle dengelemek için bilgi sağlamaktır. Bu kılavuz için okunan kaynaklar uygulamayı tanımlamaz; bu nedenle bu anlatımlar yaygın kullanımdır ve öyle sunulur.

| Etkinlik | Yanıtladığı soru |
|---|---|
| **Bütçeleme ve planlama** | Önümüzdeki dönemde ne kadar ve neye harcayacağız? |
| **Maliyet muhasebesi** | Her hizmetin sağlanması neye mal oluyor? |
| **Ücretlendirme veya dağıtım** | Kim, nasıl öder? |
| **Değer ve yatırım analizi** | Bir hizmet veya değişiklik maliyetine değer mi? |

### Showback ve chargeback

Maliyeti paylaşmak için yaygın olarak kullanılan iki düzenleme vardır. **Showback**'te tüketicilere ne kullandıkları ve bunun neye mal olduğu gösterilir ama fatura edilmezler. **Chargeback**'te fatura edilirler veya maliyet bütçelerine aktarılır. Showback az sürtünmeyle farkındalık oluşturur; chargeback hesap verebilirlik yaratır ve dağıtım kuralları üzerinde anlaşmazlıklar doğurabilir. Hangi davranışı istediğinizi ve verinin savunulabilecek kadar iyi olup olmadığını sorarak birini seçin.

### Bulut ve kullandıkça öde modeli

Wikipedia, bulut bilişimin maliyetlerin kullanımla ölçeklendiği bir işletme gideri modeline geçerek peşin sermaye harcamasını azaltabildiğini ve hizmet olarak altyapının (IaaS) kamu hizmeti esasına göre faturalandığını söyler. Hizmet olarak yazılımı (SaaS) tipik olarak kullanıcı başına aylık veya yıllık sabit bir ücret ya da kullandıkça öde olarak anlatır. Maliyet denetimi kaygıları listesinde kullanılmayan kaynaklar, verimsiz yapılandırmalar ve gizli maliyetler vardır. Sağlayıcıların maliyet araçları sunduğunu belirtir ve bulut mali operasyonlarını standartlaştırmak için bir çerçeve olarak FinOps'a atıf yapar.

Madde anket bulgularını bildirir: 200 BT liderinin katıldığı bir Gartner anketi, yüzde 69'unun 2023'te bulut bütçesi aşımı yaşadığını, diğerlerinin ise tahminleme, harcama izleme ve optimizasyona güvendiğini bulmuştur; Flexera'nın 2024 raporu bulut harcamasını yönetmeyi başlıca zorluk olarak anmış ve kamu bulutu harcamasının bütçeleri ortalama yüzde 15 aştığını bildirmiştir. Maddede doğrulanmamış metne dair bir bildirim vardır; bu nedenle bu rakamları alıntılamadan önce özgün raporlarla karşılaştırın.

### FinOps nedir

FinOps Foundation'ın sitesi FinOps'u "operasyonel bir çerçeve ve kültürel bir uygulama" olarak tanımlar; bu uygulama "teknolojinin iş değerini en üst düzeye çıkarır" ve "mühendislik, finans ve iş ekipleri arasındaki işbirliğiyle mali hesap verebilirlik yaratır." Adın "Finance" (finans) ve "DevOps" sözcüklerini birleştirdiğini ve odağın buluttan hizmet olarak yazılıma, lisanslamaya, veri merkezlerine ve daha fazlasına uzandığını söyler. Siteden temel noktalar:

- **Bir takım sporudur.** Site şu grupları anar: yöneticiler, mühendisler, FinOps uygulayıcıları, operasyon, finans ve satın alma; ve FinOps'un birbirinden farklı ekiplerin birlikte çalışma biçimini değiştirdiğini söyler. Tek bir ekip bunu tek başına yapamaz.
- **Bir olgunluk yaklaşımı kullanır;** "Crawl, Walk, Run" (emekle, yürü, koş) olarak tanımlanır.
- **Vakıf**, Linux Foundation'ın bir serisi olan LF Projects altında bir proje olarak tanımlanır ve FOCUS (FinOps Open Cost and Usage Specification) adlı açık kaynaklı bir teknik şartnameyi destekler. Ayrıca eğitim ve sertifikasyon sunar.

Bu kılavuz için okunan sayfa ilkeleri veya aşamaları listelemez; bu nedenle bu konu onları belirtmez. Vakfın ilkeler ve aşamalar sayfalarına doğrudan bakın.

### Maliyet verisi ve etiketleme

Uygulamaya ne ad verilirse verilsin, maliyeti atfedebilmeye bağlıdır. Bunun için iki şey gerekir: kaynaklar üzerinde kimin sahibi olduğunu ve hangi hizmeti desteklediğini söyleyen etiketler (bkz. Konu 4.1 — BT Varlık Yönetimi) ve bu etiketlere göre gruplanabilen faturalama verisi. FOCUS, maliyet ve kullanım verisinin biçimini sağlayıcılar arasında standartlaştırmak için vardır. Etiketsiz maliyet sahipsiz maliyettir.

### Birim maliyetler ve değer

Toplam fatura az şey söyler. Maliyeti iş için anlamlı bir şeye bölün: işlem başına, kullanıcı başına, hizmet başına, ortam başına. Birim maliyet düşerken toplam maliyetin artması sağlıklı büyüme olabilir. Birim maliyet artarken toplam maliyetin düşmesi bir soruna işaret edebilir. Birim maliyet finansı hizmet seviyelerine ve değere bağlar (bkz. Konu 3.7 — Hizmet Seviyesi Yönetimi).

### Maliyet, güvenilirlik ve hız

Para güvenilirlik ve hız satın alır ve her ek düzeyin bir fiyatı vardır (bkz. Konu 3.11 — Erişilebilirlik, Kapasite ve Performans). Maliyeti dikkatsizce kesen bir ekip dayanıklılığı azaltabilir. Maliyete hiç bakmayan bir ekip gereğinden fazla inşa edebilir. FinOps konuşmaları bu ödünleşimi açık kılmak için bir yerdir; mühendisler seçenekleri anlatır, finans ve iş bunları tartar.

### Yönetişim ve risk

Mali denetimler bütçeleri ve uyarıları, büyük taahhütler için onayı, pahalı kaynakları kimin oluşturabileceğine ilişkin sınırları ve düzenli gözden geçirmeleri içerir. Sağlayıcılara verilen taahhütler, örneğin uzun vadeli satın alma anlaşmaları, maliyeti düşürebilir ve kullanım azalırsa risk ekleyebilir. Bunlar finans, satın alma ve mühendisliğin birlikte vereceği kararlardır (bkz. Konu 5.7 — Yönetişim, Risk ve Uyum ve Konu 3.14 — Tedarikçi Yönetimi).

### Kaynakların sınırları

FinOps Foundation sayfası, uygulamayı teşvik eden kuruluşun bir özetidir ve kuruluş tarihi, üye rakamları veya sonuç kanıtı vermez. Bulut bilişim maddesi doğrulanmamış metin için işaretlenmiştir ve fiyatlandırma mekaniklerini, çıkış (egress) ücretlerini veya bir FinOps uygulamasının ayrıntılarını vermez. Bu konu bir giriş olarak ele alınmalıdır; ayrıntılar için Vakfın materyallerini ve sağlayıcınızın belgelerini okuyun.

## İyi uygulamalar

1. **Maliyeti, onu doğuran insanlara görünür kılın.** Her ekibe sahip olduğu hizmetlerin maliyetini, en az aylık olarak, anlayabilecekleri bir biçimde gösterin. İnsanlar gördüklerini yönetir.
2. **Para harcatan her şeyi etiketleyin.** Bulut kaynaklarında sahip, hizmet ve ortam etiketlerini zorunlu kılın ve etiketsiz harcamayı raporlayın. Başka bir şeyi ayarlamadan önce bunu düzeltin.
3. **Showback ile başlayın.** Ekiplere ücret yansıtmadan önce maliyetlerini gösterin. Chargeback'e yalnızca veriye güvenildiğinde ve yarar açık olduğunda geçin.
4. **Birim maliyetleri kullanın.** Maliyeti toplam olarak olduğu kadar işlem, kullanıcı veya hizmet başına da ifade edin. Eğilimi talep ve kaliteyle birlikte gözden geçirin.
5. **Bütçeler ve uyarılar belirleyin.** Bütçeleri hizmet veya ekip bazında kararlaştırın ve uyarıları sınırdan çok önce ayarlayın. Uyarıları yalnızca finansla değil, sahiplerle birlikte gözden geçirin.
6. **Finansı ve mühendisliği tek bir konuşmaya getirin.** Mühendislerin maliyeti neyin yönlendirdiğini, finansın kısıtları anlattığı düzenli bir gözden geçirme yapın. Değeri yargılayabilecek bir iş sahibini dahil edin.
7. **Önce israfı arayın.** Kullanılmayan veya gereğinden büyük kaynakları, boştaki ortamları ve unutulmuş abonelikleri bulun. Bu tasarruflar az risk taşır (abonelikler için bkz. Konu 4.2 — Yazılım Varlık Yönetimi).
8. **Tasarrufu güvenilirlikle tartın.** Kesmeden önce değişikliğin erişilebilirliğe, performansa ve kurtarmaya ne yaptığını sorun. Ödünleşimi kaydedin.
9. **Taahhütleri dikkatle planlayın.** Sağlayıcılara verilen satın alma taahhütleri maliyeti azaltabilir ama harcamayı kilitler. Bunları istikrarlı kullanıma dayandırın ve düzenli gözden geçirin.
10. **Ekiplere yetki ve sınır verin.** Ekiplerin anlaşılan sınırlar içinde maliyet kararları almasına izin verin ve bunların üzerindeki kararlar için onay isteyin. Görünürlükle birlikte özerklik, yalnızca merkezî denetimden daha iyi çalışır.
11. **Maliyeti tasarıma ve bitti tanımına dahil edin.** Tasarım gözden geçirmelerinde bir özelliğin işletilmesinin neye mal olacağını sorun ve yayından sonra kontrol edin.
12. **Öğrenin ve paylaşın.** Neyin tasarruf sağladığına ve neyin ters tepmesine dair kısa notlar yayımlayın. Uygulamayı büyütmek için "crawl, walk, run" gibi bir olgunluk yaklaşımı kullanın.

## Ekibinizle tartışılacak sorular

**Ana hizmetimizin işletme maliyetini biliyor muyuz ve bu sayının sahibi kim?**

En büyük hizmetin aylık maliyetini ve nasıl hesaplandığını isteyin. Çoğu zaman kimse yanıtlayamaz veya yanıt farklı kaynaklardan gelir. Kolaylaştırıcı, sayıyı güvenilir biçimde üretmek için neyin gerektiğini, örneğin etiketler ve bir rapor, sorabilir. Başlamak için bir hizmet seçin.

**Bulut harcamamızın ne kadarını adı belli bir sahibe atfedebiliyoruz?**

Etiketsiz payı sorun. Büyük bir pay maliyetin yönetilemediği anlamına gelir. Kaynakların neden etiketsiz olduğunu tartışın: kural yok, araç yok veya teşvik yok. Bir etiketleme kuralında ve ilk rapor için bir tarihte anlaşın.

**En son ne zaman bir maliyet sürprizi bulduk ve nasıl öğrendik?**

Örnekler toplayın: unutulmuş bir ortam, kontrolden çıkmış bir iş, yenilenen bir abonelik. Keşfedilmeden önce ne kadar süre çalıştığını sorun. Bunu yakalayabilecek uyarıları ve gözden geçirmeleri tartışın. Eklenecek bir uyarı seçin.

**Bütçe yüzde on düşseydi neyi keserdik ve neyi kaybederdik?**

Ekipten seçenekler önermesini ve güvenilirlik dahil sonuçlarını söylemesini isteyin. Bu soru ödünleşimleri açık kılar. Yanıtları bir plan olarak görmeyin; değer konusunda finans ve işle bir konuşma başlatmak için kullanın.

**Bugün mühendisler harcamayla ilgili hangi kararları veriyor ve hangilerini vermeli?**

Ekiplerin aldığı maliyet kararlarını listeleyin: boyutlar, ortamlar, araçlar, satın almalar. Hangi bilgiyi kullandıklarını sorun. Makul sınırların neler olacağını tartışın. Sınırlarla devredilecek tek bir karar üzerinde anlaşın.

**Finans ve mühendislik birbiriyle nasıl ve ne zaman konuşuyor?**

Her iki gruba da sorun. Tipik yanıtlar: bütçe zamanında veya bir şeyler ters gittiğinde. Düzenli bir ortak gözden geçirmeyi tartışın. FinOps Foundation sayfası mühendisler, finans ve iş ekipleri arasındaki işbirliğini uygulamanın kalbi olarak anar. İlkini kimin düzenleyeceğinde anlaşın.

## Uygulamada: çevik bir ITIL örneği

Ulusal bir kütüphane hizmeti dijital kataloğunu, aramasını ve kamuya açık arşivlerini üç yıl içinde bir bulut sağlayıcısına taşıdı. BT müdürüne finans departmanı, taşımadan beri aylık bulut faturasının neden üç katına çıktığını ve neden açıklanmasının zor olduğunu soruyor. Platformu on kişilik bir ekip yürütüyor ve beş proje ekibinin her birinin kendi bulut hesabı var.

BT müdürü ve bir finans analisti, maliyet verisini hizmete göre gruplanmış olarak isteyerek başlıyor. Kaynakların çoğu etiketsiz olduğundan maliyetin yalnızca üçte biri atfedilebiliyor. Beş ekiple bir etiketleme kuralında anlaşıyor ve hesaba göre etiketsiz harcamayı listeleyen haftalık bir rapor çalıştırıyorlar. Altı haftada etiketsiz pay onda birin altına iniyor. Analist sonra her ekip için, hizmete göre maliyeti ve arama hizmeti için bin arama başına maliyeti gösteren aylık bir showback raporu kuruyor. İlk gözden geçirmede mühendisler bir yıldır üretim boyutunda çalışan bir geliştirme ortamını ve bir arşivi gerekenden daha sık tarayan bir veri işleme işini fark ediyor. İkisi de düzeltiliyor. Kütüphanenin koleksiyonlar başkanıyla yapılan aylık bir toplantı, mühendislerin maliyeti neyin yönlendirdiğini, örneğin taranmış görüntülerin büyük hacmini, anlatmasını ve başkanın hangi koleksiyonların önce sayısallaştırılacağına karar vermesini sağlıyor.

İki çeyrek sonra birim maliyetler düşüyor ve fatura öngörülebilir hale geliyor. Her şey pürüzsüz değil. Arama dizinindeki maliyet kesici bir değişiklik yoğun saatlerde hızı düşürüyor ve ekip kapasiteyi geri getirene kadar kullanıcılar şikâyet ediyor. Finans departmanı ayrıca sağlayıcıyla bir yıllık taahhüt satın almak istiyor; mühendisler ise bir taşıma planlandığı için kullanımın istikrarlı kalacağından emin değil. Yalnızca kullanımın istikrarlı kısmı için taahhüt vermeye ve taşıma planı netleştiğinde taahhüdü gözden geçirmeye karar veriyorlar.

## Dört bakış açısı

### Ürün ve teslimat ekipleri

Maliyet kararlarının çoğunu teslimat ekipleri tasarım ve yapılandırma yoluyla verir. Oluşturduklarınızı etiketleyin, maliyetlerinizi izleyin ve bir özelliğin işletilmesinin neye mal olacağını sorun. Maliyet etkenlerini finansa ve işe sade bir dille anlatın.

### Hizmet ve operasyon ekipleri

Operasyon ekipleri kullanımı ve israfı görür. Boştaki ve gereğinden büyük kaynaklara ilişkin verileri paylaşın, makul uyarılar belirlemeye yardım edin ve maliyet tasarruflarının dayanıklılığı zayıflatmamasını sağlayın. Maliyet, kapasite ve hizmet seviyeleri arasındaki bağlantıyı görünür tutun.

### Liderlik ve yönetişim

Liderler ve finans bütçeleri, kuralları ve hesap verebilirliği belirler. Birim maliyetleri ve eğilimleri isteyin, insanların güvendiği bir showback veya chargeback modelini destekleyin ve taahhütlerle ilgili kararları mühendislerle birlikte alın. Ödünleşimi tartışmadan güvenilirliğe zarar veren kesintilerden kaçının.

### Müşteriler ve kullanıcılar

Müşteriler ve kullanıcılar hizmetler için doğrudan veya dolaylı olarak öder. Sağlayıcılara kullandığınız hizmetlerin fiyatını neyin belirlediğini sorun ve onlara en çok hangi değerin önemli olduğunu söyleyin. Size chargeback uygulanıyorsa net açıklamalar ve rakamları sorgulamanın bir yolunu bekleyin.

## Yaygın başarısızlık biçimleri

- **Etiketsiz maliyet.** Faturanın sahibi kimse değildir. Bunun yerine etiketleri zorunlu kılın ve boşluğu raporlayın.
- **Finans ve mühendislik ayrı odalarda.** Her taraf kısmi bilgiyle hareket eder. Bunun yerine bir iş sahibiyle düzenli ortak gözden geçirme yapın.
- **Veriye güvenilmeden chargeback.** Anlaşmazlıklar zaman yer. Bunun yerine showback ile başlayın ve veriyi iyileştirin.
- **Birim maliyet olmadan toplamlar.** Büyüme israf gibi ya da tersi görünür. Bunun yerine işlem, kullanıcı veya hizmet başına maliyeti izleyin.
- **Maliyeti dayanıklılık pahasına kesmek.** Tasarruflar kesintilere yol açar. Bunun yerine ödünleşimi belirtin ve hizmet sahibini dahil edin.
- **Aşırı taahhüt.** Uzun vadeli satın almalar, kullanımın destekleyemeyeceği harcamayı kilitler. Bunun yerine yalnızca istikrarlı kullanım için taahhütte bulunun ve gözden geçirin.
- **Yalnızca merkezî denetim.** Ekipler onay bekler ve süreci atlar. Bunun yerine ekiplere sınırlar içinde yetki verin ve görünürlük sağlayın.
- **Anket rakamlarını gerçek diye alıntılamak.** Satıcı anketlerinden gelen sayılar kararları yönlendirir. Bunun yerine özgün kaynakları kontrol edin ve kendi verilerinizi kullanın.

## Olgunluk modeli

| Boyut | Başlangıç | Gelişim | Standartlaştırma | Yönetim | Eşgüdüm |
|---|---|---|---|---|---|
| Görünürlük ve atfetme | Maliyet yalnızca toplam fatura olarak görülür | Bazı ekipler kendi maliyetlerini görür | Harcamanın çoğu etiketlenir ve hizmetlere ve sahiplere atfedilir | Birim maliyetler ve eğilimler talep ve kaliteye karşı gözden geçirilir | Maliyet verisi ekipler, tedarikçiler ve finans arasında ortak bir biçimle paylaşılır |
| Yönetişim ve bütçeler | Bütçeler yıllık ve sabittir | Bazı bütçeler ve uyarılar vardır | Bütçeler, uyarılar ve onay sınırları standarttır | Sapmalar incelenir ve kurallar ayarlanır | Bütçe kuralları kuruluş ve ortaklar genelinde hizalanır |
| İşbirliği | Finans ve mühendislik bütçe zamanında buluşur | Bazı ortak konuşmalar yapılır | Bir iş sahibiyle düzenli ortak gözden geçirme | Kararlar ve sonuçlar izlenir ve iyileştirilir | Finans, mühendislik, iş ve tedarikçiler hedefleri ve verileri paylaşır |
| Optimizasyon | Tasarruf krizlerden gelir | Bir miktar israf bulunur | İsraf, boyutlandırma ve taahhütler düzenli gözden geçirilir | Tasarruflar güvenilirlik risklerine karşı ölçülür | Optimizasyon rutindir, paylaşılır ve hizmet hedefleriyle dengelenir |

## Kontrol listesi

- [ ] Her büyük hizmetin aylık maliyetini ve sahibini söyleyebiliyoruz.
- [ ] Bulut kaynaklarında sahip, hizmet ve ortam etiketleri var ve etiketsiz harcama haftalık veya aylık raporlanıyor.
- [ ] Ekipler sahip oldukları hizmetler için düzenli bir maliyet raporu alıyor (showback).
- [ ] Her büyük hizmet için en az bir birim maliyeti izliyoruz.
- [ ] Bütçeler ve uyarılar sahipleriyle birlikte var ve uyarılar sınırlardan çok önce tetikleniyor.
- [ ] Finans, mühendislik ve bir iş sahibi maliyet ve değer konusunda düzenli buluşuyor.
- [ ] Kullanılmayan ve gereğinden büyük kaynakları ve abonelikleri en az üç ayda bir gözden geçiriyoruz.
- [ ] Maliyet kesintileri güvenilirlik ve performans üzerindeki etkileri açısından gözden geçiriliyor.
- [ ] Satın alma taahhütleri istikrarlı kullanıma dayanıyor ve gözden geçiriliyor.
- [ ] Satıcı anketlerinden gelen rakamları kullanmadan önce özgün kaynaklarla karşılaştırdık.

## Yapay zeka istemleri

**Amaç: bir maliyet raporunu sahipsiz ve olağandışı harcamalar açısından çözümlemek.**

```text
Here is a cost report for the last [period], grouped by account, service, and tag: [paste real data; remove sensitive details].

Using only this data, calculate: total cost, the share with no owner tag, the five largest cost items and their share of total, and any item whose cost changed by more than [threshold you choose, e.g. 25%] from the previous period if I included it. For each unusual item, suggest a question for its owner. Do not guess at causes or invent numbers. List what you are unsure of.
```

**Amaç: bir hizmet için birim maliyet tanımlamak.**

```text
Help me define a unit cost for [service].

What the service does: [describe].
What the business cares about (transactions, users, searches, documents): [describe].
Cost data we have: [describe sources and how they are grouped].
Demand data we have: [describe].

Propose two or three candidate unit costs, how to calculate each from the data I listed, what could distort them, and what decisions each would help. Do not invent figures. Ask clarifying questions first, and list what you are unsure of.
```

**Amaç: mühendislik ve finans arasındaki ortak bir gözden geçirmeye hazırlanmak.**

```text
Plan a 45-minute monthly review between engineering, finance, and a business owner about the cost of [service or portfolio].

Inputs: [cost report, unit cost, budget status, forecast; describe what you have].
Concerns on each side: engineering [list]; finance [list]; business [list].

Provide a timed agenda, five questions for each group, a one-page summary template with only the figures I supply, and a closing step that records decisions and owners. Ask clarifying questions first, mark assumptions, and list what you are unsure of.
```

**Amaç: bir maliyet tasarrufu önerisini güvenilirlikle tartmak.**

```text
We are considering this cost-saving change: [describe].
Expected saving, with source: [paste, or write "not estimated"].
What the service promises to users (service levels): [paste].
Current performance against those promises: [paste].
Known dependencies: [list].

List the ways the change could affect availability, performance, recovery, and security, as questions for the service owner. Suggest a small trial, what to monitor, and what would make us reverse it. Do not invent estimates. Ask clarifying questions first, and list what you are unsure of.
```

## Yapay zeka becerileri

- [budget-forecasting](../../../../skills/budget-forecasting/SKILL.md): BT ve bulut harcamasını tahmin etmek ve sapmaları açıklamak için kullanın.
- [demand-forecasting](../../../../skills/demand-forecasting/SKILL.md): maliyet tahminlerinin talebi yansıtması için gelecekteki yükü kestirmek amacıyla kullanın.
- [capacity-planning](../../../../skills/capacity-planning/SKILL.md): kaynak ihtiyaçlarını maliyete ve hizmet seviyelerine bağlamak için kullanın.
- [vendor-management](../../../../skills/vendor-management/SKILL.md): sağlayıcı sözleşmelerini ve taahhütlerini yönetmek için kullanın.
- [portfolio-management](../../../../skills/portfolio-management/SKILL.md): hizmetleri ve girişimleri değere ve maliyete göre seçmek ve fonlamak için kullanın.

## Temel kaynaklar

- **What is FinOps?** (FinOps Foundation, finops.org): Vakfın kendi tanımı ve mühendislik, finans ve iş ekipleri arasındaki işbirliğinin açıklaması.
- **Cloud computing** (Wikipedia): fiyatlandırma modelleri, maliyet denetimi ve paylaşılan sorumluluk üzerine arka plan; doğrulanmamış metne dair bir bildirimle.
- **Total cost of ownership** (Wikipedia): bir varlığın veya hizmetin ömrü boyunca tüm maliyetlerinin sayılması üzerine arka plan.
- **Software as a service** (Wikipedia): abonelik fiyatlandırması üzerine arka plan.

## Kaynakça

1. What is FinOps? — FinOps Foundation, finops.org — https://www.finops.org/introduction/what-is-finops/
2. Cloud computing — Wikipedia — https://en.wikipedia.org/wiki/Cloud_computing
3. Total cost of ownership — Wikipedia — https://en.wikipedia.org/wiki/Total_cost_of_ownership
4. Software as a service — Wikipedia — https://en.wikipedia.org/wiki/Software_as_a_service
5. IT service management — Wikipedia — https://en.wikipedia.org/wiki/IT_service_management
6. DevOps — Wikipedia — https://en.wikipedia.org/wiki/DevOps
7. Operating expense — Wikipedia — https://en.wikipedia.org/wiki/Operating_expense
8. Capital expenditure — Wikipedia — https://en.wikipedia.org/wiki/Capital_expenditure
9. IT asset management — Wikipedia — https://en.wikipedia.org/wiki/IT_asset_management
