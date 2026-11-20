# Yazılım Varlık Yönetimi

**Yazılım varlık yönetimi, bir kuruluşun ihtiyaç duyduğu yazılımı satın almasını, satın aldığını kullanmasını ve kabul ettiği koşullara uymasını sağlar; çevik ekipler için bu artık lisanslı ürünlerin yanı sıra açık kaynak bileşenlerin ve aboneliklerin de izlenmesi anlamına gelir.**

## Bu neden önemli

Yazılım, BT'deki en büyük ve en az görünür maliyetlerden biridir. Ayrılmış kişiler için lisans alınır, abonelikler fark edilmeden yenilenir ve ürünler lisansın izin vermediği biçimlerde kurulur. Her biri bir maliyet ya da risktir. Bir satıcı denetimi küçük bir uyumsuzluğu büyük bir faturaya dönüştürebilir; unutulmuş bir uygulamadaki yamasız bir bileşen de bir saldırgana kapı açabilir.

Çevik ekipler tabloyu değiştirir. Geliştiriciler tek bir komutla kütüphane çeker ve modern uygulamalar büyük ölçüde üçüncü taraf ve açık kaynak parçalardan derlenir. Wikipedia'daki yazılım tedarik zinciri maddesi, Synopsys'e atıfla, bir satıcının 2024'te çözümlediği ticari kod tabanlarının yüzde 96'sında açık kaynak yazılım bulunduğunu bildirir. Ekipler ayrıca bulut hizmetlerini ve abonelikleri satın alma sürecinin dışında kartlarla satın alır. Bu nedenle yazılım varlık yönetimi (SAM), birkaç büyük ürünün kurulumlarını saymaktan, neyin kullanıldığını, neyin borçlanıldığını ve neye güvenildiğini kapsayan bir uygulamaya dönüşmüştür.

[Wikipedia'daki yazılım varlık yönetimi maddesi](https://en.wikipedia.org/wiki/Software_asset_management) SAM'i, yazılımın satın alınmasını, dağıtımını, bakımını, kullanımını ve elden çıkarılmasını yönetmek ve optimize etmek için bir iş uygulaması olarak tanımlar; hedefleri BT maliyetlerini azaltmak, iş ve hukuki riski sınırlamak ve son kullanıcı verimliliğini artırmaktır. Madde bulut hizmetlerini, SBOM'ları veya olgunluk modellerini kapsamaz; bu nedenle bu konu yazılım tedarik zinciri ve açık kaynak yazılım maddelerini ekler. Bu konu uygulamayı anlatır ve hukuki danışmanlık vermez; lisans koşulları değişir ve doğru kaynak lisansın veya sözleşmenin metnidir.

## Temel kavramlar

### SAM nedir

Wikipedia'ya göre SAM, BT varlık yönetiminin bir parçasıdır (bkz. Konu 4.1 — BT Varlık Yönetimi). Maddede ITIL'e atıf yapılarak, SAM'in yazılım varlıklarının etkili yönetimini, denetimini ve korunmasını içerdiği belirtilir. Maddenin sıraladığı stratejik hedefler arasında; toplu sözleşmelerle ve kullanılmayan lisansların yeniden tahsisiyle yazılım ve destek maliyetlerini azaltmak, güvenlik politikalarını ve masaüstü, sunucu ve mobil standartlarını uygulatmak, teknolojiyi daha hızlı ve güvenilir dağıtarak verimliliği artırmak, otomasyonla yönetim yükünü sınırlamak ve edinme, dağıtım, kullanım ve emekliye ayırma politikalarını oluşturmak vardır.

### Lisans uyumu

Madde SAM'i, satın alınan lisans sayısı ile gerçekten tüketilen sayı arasında denge kurmak ve kullanımın her satıcının lisans koşullarıyla eşleşmesini sağlamak olarak anlatır. Tüketimin en yaygın ölçüsünün kurulumlar olduğunu, ancak bazı yazılımların kullanıcıya, sermayeye, işlemciye veya CPU çekirdeğine göre lisanslandığını belirtir. Maddeye göre kuruluşlar, satıcılar veya Business Software Alliance gibi üçüncü taraflarca yapılan denetimlerde yükümlülüklerini sürekli yazılım envanterleri, satın alma politikaları ve araçlarla azaltabilir. Madde denetim prosedürlerini anlatmaz. Çalışmanın amacı **hakkınızı** (kullanmanıza izin verilen), **tüketiminizi** (kullandığınız) ve ikisi arasındaki farkı bilmektir.

### Üç soru

Bir SAM uygulaması her önemli ürün için üç soruyu yanıtlar:

| Soru | Neye ihtiyaç duyar |
|---|---|
| Neyi kullanma hakkımız var? | Sözleşmeler, lisans koşulları, faturalar ve satın alma kanıtı |
| Neyi kullanıyoruz? | Keşif ve ölçümden gelen envanter ve kullanım verisi |
| Fark nedir ve ne yapacağız? | Karşılaştırma; satın alma, yeniden tahsis etme veya kaldırma kararları |

Fark iki yönde olabilir: uyum riski olan eksik lisanslama ve israf olan fazla lisanslama.

### Standartlar: ISO/IEC 19770

Madde, ISO/IEC 19770 ailesinin parçalarını sıralar: 19770-1:2017 (kademeli düzeylerde uygulanabilen bir süreç çerçevesi olan BT varlık yönetim sistemi gereksinimleri), 19770-2:2015 (yazılım tanımlama etiketleri), 19770-3:2016 (lisans, sözleşme ve fatura ayrıntıları için bir hak yönetimi şeması), 19770-4:2017 (kaynak kullanım ölçümü verileri) ve 19770-5:2015 (genel bakış ve sözlük). Madde, yazılım tanımlama standardının IBM, Microsoft ve Adobe tarafından desteklendiğini söyler. Güncel sürümler ve kesin içerik için standartlara bakın.

### SAM teknolojileri ve sınırları

Madde yazılım envanteri, lisans yönetimi, ölçüm, uygulama denetimi, dağıtım, yama yönetimi, talep yönetimi ve ürün kataloglama için araçları sıralar. Ayrıca ölçeğe bir örnek verir: Microsoft'un System Center Configuration Manager'ındaki ölçüm kuralları küçük yapılar için iyi çalışır ancak kurumsal ölçekte yönetilemez veri hacimleri üretir. Araçlar yardımcı olur, ama net bir soruya ve bir sahibe ihtiyaç duyarlar.

### Açık kaynak yazılım

Wikipedia açık kaynak yazılımı, kaynak kodu kamuya açık olan ve kullanıcıların genellikle açık bir lisans altında kullanabildiği, inceleyebildiği, değiştirebildiği ve dağıtabildiği yazılım olarak tanımlar. Open Source Initiative, on ölçüt ve onaylı lisanslar listesiyle en yaygın tanımı sürdürür; ancak madde OSI'nin terim üzerinde hukuki bir yetkisi olmadığını söyler. İki lisans ailesini anlatır:

| Aile | Alıcılardan ne ister | Anılan örnekler |
|---|---|---|
| **Serbest (permissive)** | Telif hakkı bildirimlerini korumak ve lisansı eklemek; kendi kodunuzu aynı lisansla yayımlama zorunluluğu yok | BSD, MIT, Apache |
| **Copyleft** | Dağıttığınızın en azından bazı parçaları için aynı lisansı kullanmak (güçlü copyleft tüm türev eserlere uygulanır; zayıf copyleft yalnızca belirli koşullarda) | GNU GPL (güçlü); MPL, EPL (zayıf) |

Madde, her iki ailenin de telif hakkı bildirimlerinin korunmasını ve kodla birlikte lisansın bir kopyasının sağlanmasını gerektirdiğini söyler. Bir mahkemenin, atıf dahil bir açık lisansın koşullarını telif hakkı yasası uyarınca uygulattığı *Jacobson v Katzer* (2008) davasına atıf yapar. Kuruluşların stratejilerini yönetmek için açık kaynak program ofisleri kurduğunu belirtir. Açık kaynak koşulları gerçek yükümlülüklerdir. Hangilerinin geçerli olduğu yazılımı nasıl kullandığınıza ve dağıttığınıza bağlıdır; hukuk işlevinize danışın ve lisansı okuyun.

### Yazılım tedarik zinciri ve SBOM'lar

Yazılım tedarik zinciri maddesi, onu bir yazılım yapıtını geliştirmek, derlemek ve yayımlamak için kullanılan bileşenler, kütüphaneler, araçlar ve süreçler olarak anlatır. Riskleri sayar: saldırganlar tüm aşağı akış kullanıcılarına ulaşmak için yukarı akıştaki bir bileşeni ele geçirebilir; madde 2021'deki Log4Shell, 2020'deki SolarWinds saldırısı ve 2024'teki XZ Utils arka kapısı gibi örnekleri anar. **Yazılım malzeme listesini (SBOM)** bir yazılım yapıtındaki açık kaynak ve tescilli parçalar dahil bileşenlerin envanteri, üretimdeki malzeme listesinin yazılım karşılığı olarak tanımlar. SBOM'lar güvenlik açığı ve lisans çözümlemesini destekler.

Madde sınırları bildirir: elektronik tablolar güvenlik açığı verisiyle otomatik olarak zenginleştirilemez ve sorgulanabilir bir depoda saklanmalıdır; politika güdümlü SBOM'lar nadirdir, bir çalışma popüler GitHub depolarının yaklaşık yüzde 0,56'sında bunların bulunduğunu saptamıştır; test edilen projelerin yarısından azı sürümlerinde SBOM içerir ve çoğu eksiktir; altı Java SBOM aracı üzerine bir çalışma sık yanlışlıklar bulmuştur. Yalnızca görünürlüğün bütünlüğü garanti edemeyeceğini belirtir. Ayrıca ABD'nin 14028 sayılı Başkanlık Kararnamesi'nin (12 Mayıs 2021'de imzalandı) NIST ve NTIA'ya SBOM'lar dahil yazılım tedarik zinciri güvenliği konusunda rehberlik yayımlama talimatı verdiğini ve NTIA'nın asgari unsurlarının veri alanları, otomasyon desteği ile uygulamalar ve süreçler olarak sınıflandığını bildirir. Madde SBOM biçimlerini adlandırmaz ve Avrupa Birliği'nin Siber Dayanıklılık Yasası'nı anlatmaz. SBOM'lara ilişkin kurallar ülkeye ve sektöre göre değişir; size neyin uygulandığını uyum işlevinize sorun.

### SaaS ve bulut abonelikleri

SAM maddesi hizmet olarak yazılımı (SaaS) veya bulutu ele almaz. Pratik deneyim, abonelik yazılımının yeni sorunlar yarattığını gösterir: satın alma dışından yapılan alımlar, kimsenin kaldırmadığı kullanıcı lisansları, çakışan araçlar ve incelenmeden tedarikçilere verilen veriler (bkz. Konu 3.14 — Tedarikçi Yönetimi ve Konu 4.5 — BT Mali Yönetimi ve FinOps). Abonelikler için SAM, neyin satın alındığını, sahibinin kim olduğunu, kimin kullandığını ve ne zaman yenilendiğini keşfetmeye odaklanır.

### Kaynakların sınırları

SAM maddesi denetim prosedürlerini, lisans türü kataloglarını veya olgunluk modellerini kapsamaz ve ana kaynakçası 2006 ile 2009 arasına ait eski öğeler içerir. Yazılım tedarik zinciri maddesi, kalitesi eşit olmayan anketlerden ve çalışmalardan rakamlar bildirir. Kaynakları soruları çerçevelemek için, yanıtlar için ise lisans metinlerini ve sözleşmeleri kullanın.

## İyi uygulamalar

1. **En önemli ürünlerle başlayın.** Maliyet veya hukuki maruziyet açısından en büyük veya en riskli birkaç ürünü seçin ve önce bunlar için hak, envanter ve kullanımı netleştirin.
2. **Hak kanıtını saklayın.** Sözleşmeleri, faturaları ve lisans koşullarını bulunabilecekleri yerde saklayın ve ürün kayıtlarına bağlayın. Kanıt olmadan bir denetimde pozisyonunuzu savunamazsınız.
3. **Lisans ölçütünü bilin.** Her ürün için nasıl sayıldığını kaydedin: kullanıcı, cihaz, işlemci, çekirdek veya başka biçimde. Lisans çekirdek başınayken kurulumları saymak yanlış yanıt verir.
4. **Hakkı kullanımla düzenli olarak karşılaştırın.** Büyük ürünler için en az üç ayda bir, kullanabileceğiniz ile kullandığınızı karşılaştırın. Farka satın alarak, yeniden tahsis ederek veya kaldırarak karşılık verin.
5. **Kullanılmayan lisansları geri alın.** Kullanım verisiyle belirli bir süre kimsenin kullanmadığı lisansları bulun ve sahibine danıştıktan sonra yeniden atayın veya iptal edin.
6. **Yazılımın nasıl girdiğini denetleyin.** Onaylı yazılımı talep etmeyi kolay, süreç dışında satın almayı zor kılın. Abonelikleri ve kartla yapılan alımları harcama gözden geçirmelerine dahil edin.
7. **Açık kaynak bileşenleri varlık olarak ele alın.** Ürünlerinizdeki açık kaynak bileşenlerin lisans ve sürümleriyle birlikte bir envanterini tutun. Lisansları, yazılımı nasıl kullandığınıza ve dağıttığınıza göre hukuki danışmanlıkla denetleyin.
8. **SBOM'ları derleme sırasında üretin.** Her derleme için otomatik olarak bir yazılım malzeme listesi üretin, sorgulanabilir bir yerde saklayın ve güvenlik açıklarına yanıt vermek ve müşteri sorularını yanıtlamak için kullanın. Araçlar yanlış olabileceğinden SBOM'u derlemeyle karşılaştırın.
9. **Abonelikleri izleyin.** Her biri için sahibi, amacı, maliyeti, kullanıcı lisansı sayısını, kullanıcıları, yenileme tarihini ve tutulan veriyi kaydedin. Yenilemeden önce gözden geçirin.
10. **Yazılımı hizmetlere bağlayın.** Hangi hizmetlerin hangi yazılımı ve sürümleri kullandığını kaydedin; böylece bir güvenlik açığı veya lisans değişikliği etkilenen hizmetlere kadar izlenebilir (bkz. Konu 4.4 — Yapılandırma Yönetimi).
11. **Denetimlere sakin biçimde hazırlanın.** Kayıtları güncel tutun, bir irtibat kişisi belirleyin ve sözleşmeden haklarınızı ve görevlerinizi bilin. Toparlanmaya bildirimi beklemeden başlayın.
12. **Yazılımı düzgün biçimde emekliye ayırın.** Sistemlerden kaldırın, lisansları ve abonelikleri sonlandırın ve kayıtları güncelleyin. Kullanılmayan yazılım bir maliyet ve bir saldırı yüzeyidir.

## Ekibinizle tartışılacak sorular

**En pahalı üç yazılım ürünümüz için neyi kullanabileceğimizi ve neyi kullandığımızı biliyor muyuz?**

Her biri için sahip olunan lisans sayısını ve kullanımdaki sayıyı isteyin. Karşılaştırın. Yaygın sonuçlar şaşırtıcıdır: kullanıcıdan fazla lisans ya da lisansı aşan kullanıcılar. Kolaylaştırıcı hak kanıtının nerede tutulduğunu sorabilir. En büyük farkı uzlaştırmayı planlayın.

**İnsanlar kimseye söylemeden hangi yazılımları satın aldı veya kurdu?**

Dürüst olun ve yargılamayın. Kartla alınan araçları, işte kullanılan ücretsiz araçları ve tarayıcı eklentilerini sorun. Tipik nedenler hız ve belirsiz süreçtir. Onaylı yolu yeterince hızlı yapacak şeyleri tartışın. Bir kayıt adımında anlaşın.

**Ürünlerimiz hangi açık kaynak bileşenlere dayanıyor ve lisansları neler?**

Birinin bir liste çıkarıp çıkaramayacağını sorun. Çıkaramıyorsa derlemeden nasıl üretileceğini tartışın. Sonra lisansların nasıl denetlendiğini sorun. Yükümlülüklerin serbest ve copyleft lisanslar arasında farklılaştığını unutmayın. Yüksek riskli durumları gözden geçirmek için hukukla birlikte plan yapın.

**Yarın yaygın bir kütüphanede ciddi bir güvenlik açığı çıksa, onu kullanıp kullanmadığımızı öğrenmemiz ne kadar sürer?**

Adımları gözden geçirin: kime haber verilir, nasıl aranır, her hizmetteki sürüm nasıl bilinir. Yanıt, SBOM'ların ve envanterlerin ne kadar yardımcı olacağını gösterir. Hat içinde bir malzeme listesi üretmek gibi ilk bir iyileştirmede anlaşın.

**Gelecek çeyrek hangi abonelikler yenileniyor ve bunları tutup tutmamaya kim karar veriyor?**

Yenilemeleri listeleyin. Her biri için sahibinin kim olduğunu, kaç kullanıcı lisansının etkin olduğunu ve iptal edilirse ne olacağını sorun. Çoğu zaman karar kimsenin değildir. Sahipler atayın ve her yenilemeden önce bir gözden geçirme tarihi ekleyin.

**Bir satıcı denetim bildirimine nasıl yanıt verirdik?**

Bunu kimin ele alacağını ve elinde ne kanıt olduğunu sorun. Kayıtların eksiksiz olup olmadığını tartışın. Amaç sakin bir plandır, denetim korkusu değil. Bir irtibat kişisi ve bir kontrol listesinde anlaşın.

## Uygulamada: çevik bir ITIL örneği

Ulusal bir posta hizmeti yaklaşık 60 dahili uygulama ve on beş kişilik bir ekibin geliştirdiği müşteriye dönük bir koli izleme platformu işletiyor. Bir satıcı BT departmanına bir veritabanı ürününde lisans denetimi yapılacağını bildiriyor. ITAM görevlisi, lisans kayıtlarının üç elektronik tabloya dağıldığını ve sanal makineler konaklar arasında çok kez taşındığı için veritabanının şu anda kaç işlemci çekirdeğinde çalıştığını kimsenin söyleyemediğini görüyor.

ITAM görevlisi, bir veritabanı yöneticisi ve satın alma sorumlusu kanıtları bir araya getiriyor. Sözleşmeyi, lisans ölçütünü (işlemci çekirdeği başına), faturaları ve veritabanının nerede çalıştığına dair keşif verisini topluyorlar. Ürünün bir ortamda satın alınandan daha fazla çekirdekte, lisansların kullanılmadığı bir diğerinde ise daha azında çalıştığını buluyorlar. Satıcıyla görüştükten sonra kullanılmayan lisansları yeniden tahsis ediyor, az sayıda ek lisans satın alıyor ve temel olmayan bir ortamı ücretsiz bir alternatife taşıyorlar. Maliyet, bir denetim bulgusunun doğuracağından çok daha düşüktür ama önemsiz değildir.

Aynı sıralarda büyük bir müşteri platform ekibinden koli izleme platformundaki yazılım bileşenlerinin bir listesini istiyor. Ekip bir liste üretemeyeceğini fark ediyor. Her sürüm için bir malzeme listesi üreten ve bunu bir depoda saklayan bir derleme adımı ekliyor. İlk çıktı, hukuk ekibinin incelemediği bir lisansa sahip bir kütüphane içeriyor ve bunu değiştirmeye karar veriyorlar. Sorunlar sürüyor. Ekibin SBOM aracı bir dildeki bileşenleri kaçırıyor ve ayrı bir araştırma grubu bir bölüm kartıyla abonelik satın almaya devam ediyor. ITAM görevlisi aracın satıcısına boşluğu soruyor ve bölümü aboneliklerini kaydetmeye ikna ediyor.

## Dört bakış açısı

### Ürün ve teslimat ekipleri

Yazılımın çoğunu kuruluşa teslimat ekipleri getirir. Eklediğiniz bileşenleri ve abonelikleri kaydedin, derlemelerinizde malzeme listeleri üretin ve tanımadığınız bir lisansa sahip bir kütüphaneyi kullanmadan önce sorun. Bulguları hukuk ve güvenlikle paylaşın.

### Hizmet ve operasyon ekipleri

Operasyon ekipleri envanteri, yamalamayı ve ölçümü yürütür. Yazılım envanterini hizmetlere bağlı tutun, güvenlik açıkları ortaya çıktığında hızla yama uygulayın ve kullanılmayan lisansları geri alın. Satın almanın ürünlerin gerçekte nasıl kullanıldığını anlamasına yardımcı olun.

### Liderlik ve yönetişim

Liderler, uyumsuzluk riskinin ve harcamanın sahibidir. En büyük ürünler için hak ve tüketimi, aboneliklere dair bir görünümü ve açık kaynak ile tedarik zinciri riski için bir plan isteyin. İnsanların kullanacağı kadar hızlı bir satın alma yolunu destekleyin.

### Müşteriler ve kullanıcılar

Müşteriler ve kullanıcılar, yazılım erişilebilir ve güvenli olduğunda yarar sağlar. İhtiyacınız olanı uygun yoldan talep edin, artık kullanmadığınızı iade edin ve yararlı bulduğunuz araçları ekibe bildirin. Ürünlerinizin müşterileri malzeme listeleri isteyebilir; bunun istenmesini bekleyin.

## Yaygın başarısızlık biçimleri

- **Yalnızca kurulumları saymak.** Lisans ölçütü çekirdek veya kullanıcı başınadır. Bunun yerine ölçütü kaydedin ve doğru şeyi sayın.
- **Kaybolan hak kanıtı.** Sözleşmeler ve faturalar bulunamaz. Bunun yerine ürün kaydıyla birlikte saklayın.
- **Raf yazılımı (shelfware).** Lisanslar alınır ve kullanılmaz. Bunun yerine hakkı kullanımla karşılaştırın ve geri alın.
- **Gölge satın almalar.** Kartlarla alınan abonelikler süreçten kaçar. Bunun yerine onaylı yolu hızlı yapın ve harcamaları istisnalar için gözden geçirin.
- **Bilinmeyen açık kaynak bileşenler.** Kimse bunları listeleyemez. Bunun yerine derlemelerde otomatik olarak malzeme listeleri üretin.
- **Açık kaynağın lisans koşullarını yok saymak.** Copyleft yükümlülükleri gözden kaçar. Bunun yerine lisansları kullanım ve dağıtıma göre hukuki danışmanlıkla denetleyin.
- **Araçlara körü körüne güvenmek.** Araçlar bileşenleri kaçırır veya yanlış olanları listeler. Bunun yerine çıktıyı bir örneklem üzerinde doğrulayın ve boşlukları satıcılara sorun.
- **Denetim paniği.** Kayıtlar bildirimden sonra toplanır. Bunun yerine kayıtları güncel tutun ve bir denetim irtibat kişisi belirleyin.

## Olgunluk modeli

| Boyut | Başlangıç | Gelişim | Standartlaştırma | Yönetim | Eşgüdüm |
|---|---|---|---|---|---|
| Hak ve kullanım | Kayıtlar dağınıktır; kullanım bilinmez | Büyük ürünlerin hak kayıtları vardır | Ana ürünler için hak ve kullanım kaydedilir ve düzenli olarak karşılaştırılır | Farklar ve kullanılmayan lisanslar ölçülür ve bunlara göre harekete geçilir | Hak ve kullanım finans, satın alma ve tedarikçilerle paylaşılır |
| Edinme ve abonelikler | Yazılımı herkes satın alır | Bazı satın almalar için onaylı bir yol vardır | Satın almalar ve abonelikler sahipleri ve yenileme tarihleriyle tek bir yolu izler | Harcama ve kullanıcı lisansı kullanımı yenilemeden önce gözden geçirilir | Satın alma, kullanım ve sözleşmeler kuruluş genelinde eşgüdümlüdür |
| Açık kaynak ve tedarik zinciri | Bileşenler bilinmez | Bazı ekipler kütüphaneleri listeler | Malzeme listeleri derlemelerde üretilir ve lisanslar gözden geçirilir | Güvenlik açığı ve lisans bulguları kapanışa kadar izlenir | Malzeme listeleri gerektiğinde müşteriler ve tedarikçilerle paylaşılır |
| Denetim ve uyum | Denetim bildirimleri paniğe yol açar | Bir irtibat kişisi vardır | Kayıtlar güncel tutulur ve bir denetim rutini vardır | Uyum riski ölçülür ve gözden geçirilir | Uyum uygulaması satıcılar ve yargı bölgeleri arasında hizalanmıştır |

## Kontrol listesi

- [ ] En büyük yazılım ürünlerimiz için hakkı, lisans ölçütünü ve kullanımı biliyoruz.
- [ ] Sözleşmeler, faturalar ve lisans koşulları ürün kayıtlarıyla birlikte saklanıyor.
- [ ] Büyük ürünler için hak ve kullanım en az üç ayda bir karşılaştırılıyor.
- [ ] Kullanılmayan lisanslar sahiplerine danışıldıktan sonra geri alınıyor.
- [ ] Satın almalar ve abonelikler tek bir yolu izliyor; sahipler ve yenileme tarihleri kaydediliyor.
- [ ] Sunduğumuz veya işlettiğimiz ürünler için derlemede bir malzeme listesi üretiyoruz.
- [ ] Bileşenlerimizdeki açık kaynak lisansları, kullanımımıza göre hukuki danışmanlıkla gözden geçiriliyor.
- [ ] Belirli bir bileşeni veya ürünü hangi hizmetlerin kullandığını bulabiliyoruz.
- [ ] Adı belli bir kişi satıcı denetim bildirimlerini ele alıyor.
- [ ] Emekliye ayrılan yazılım sistemlerden ve kayıtlardan kaldırılıyor.

## Yapay zeka istemleri

**Amaç: bir ürün için hak ve tüketimi karşılaştırmak.**

```text
Help me compare entitlement and usage for [product].

License metric (how the vendor counts, with the exact wording from the contract): [paste].
Entitlement (what we purchased, with dates): [paste].
Usage data (installations, users, cores, or whatever the metric requires): [paste real data].

Using only this information, compute the difference between entitlement and usage, in the vendor's unit, and say whether it indicates a shortfall or a surplus. List what is unclear in the contract wording as questions for the vendor or legal. Do not interpret legal terms beyond the text. Ask clarifying questions first, and list what you are unsure of.
```

**Amaç: bir açık kaynak bileşen listesini lisans soruları açısından gözden geçirmek.**

```text
Here is a list of open-source components in our product with name, version, and license as reported by our tooling: [paste].
How we use and distribute the product: [for example internal use only, hosted service, shipped to customers].

Group the licenses into permissive and copyleft families based on the license names. For each group, list the types of question we should put to our legal team given how we use and distribute the product. Flag components with missing or unknown licenses. Do not give legal advice or say what the licenses require; list questions only. List what you are unsure of.
```

**Amaç: malzeme listesi kullanarak bir güvenlik açığı müdahale sorgusu hazırlamak.**

```text
Help me plan how we would answer: "Do we use [component name and version range] and where?"

What we have today: [for example bills of materials in a repository, a spreadsheet, nothing].
Systems and services in scope: [list].

Describe the steps to find out, who does each, what data they need, what could go wrong, and how long each step might take (leave durations as [to be measured]). Propose one improvement that would shorten the answer. Do not invent our tools. Ask clarifying questions first, and list what you are unsure of.
```

**Amaç: gelecek çeyrek için bir abonelik gözden geçirmesi oluşturmak.**

```text
Here is a list of our subscriptions with owner, monthly cost, paid seats, active users in the last 90 days, renewal date, and data held: [paste real data].

Using only this data, list renewals in the next 90 days, compute unused seats and their cost for each, and highlight subscriptions with no owner. For each, suggest a question for the owner before renewal. Do not recommend canceling anything; flag candidates for review. List what you are unsure of.
```

## Yapay zeka becerileri

- [vendor-management](../../../../skills/vendor-management/SKILL.md): yazılım satıcılarıyla sözleşmeleri, yenilemeleri ve ilişkileri yönetmek için kullanın.
- [legal-compliance-audit](../../../../skills/legal-compliance-audit/SKILL.md): bir satıcı veya uyum denetimine hazırlanmak için kullanın.
- [budget-forecasting](../../../../skills/budget-forecasting/SKILL.md): yazılım ve abonelik maliyetlerini tahmin etmek için kullanın.
- [risk-register](../../../../skills/risk-register/SKILL.md): lisans, güvenlik açığı ve tedarik zinciri risklerini kaydetmek için kullanın.
- [security-testing](../../../../skills/security-testing/SKILL.md): bağımlılıkları ve derlemeleri bilinen zayıflıklar açısından denetlemek için kullanın.

## Temel kaynaklar

- **Software asset management** (Wikipedia): tanım, hedefler, teknolojiler ve ISO/IEC 19770 parçaları.
- **Software supply chain** (Wikipedia): riskler, yazılım malzeme listesi, benimsenme rakamları ve düzenleyici arka plan.
- **Open-source software** (Wikipedia): tanım, lisans aileleri ve riskler ile yükümlülüklere dair notlar.
- **ISO/IEC 19770** (International Organization for Standardization): standart ailesinin kendisi; kesin gereksinimler için güncel parçaları okuyun.

## Kaynakça

1. Software asset management — Wikipedia — https://en.wikipedia.org/wiki/Software_asset_management
2. Software supply chain — Wikipedia — https://en.wikipedia.org/wiki/Software_supply_chain
3. Open-source software — Wikipedia — https://en.wikipedia.org/wiki/Open-source_software
4. IT asset management — Wikipedia — https://en.wikipedia.org/wiki/IT_asset_management
5. Software license — Wikipedia — https://en.wikipedia.org/wiki/Software_license
6. Copyleft — Wikipedia — https://en.wikipedia.org/wiki/Copyleft
7. Permissive software license — Wikipedia — https://en.wikipedia.org/wiki/Permissive_software_license
8. Software as a service — Wikipedia — https://en.wikipedia.org/wiki/Software_as_a_service
9. Open Source Initiative — Wikipedia — https://en.wikipedia.org/wiki/Open_Source_Initiative
