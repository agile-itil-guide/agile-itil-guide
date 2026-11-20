# BT Varlık Yönetimi

**BT varlık yönetimi, bir kuruluşun sahip olduğu veya ödemesini yaptığı donanımı, yazılımı ve ilgili kaynakları satın almadan elden çıkarmaya kadar izler; böylece maliyet, risk ve destek kararları tahminlere değil gerçeklere dayanır.**

## Bu neden önemli

Çoğu kuruluşa kaç dizüstü bilgisayarı, sunucusu, bulut hesabı ve yazılım lisansı olduğunu sorun; ilk yanıt bir tahmindir. Bir aramadan sonra gelen ikinci yanıt ise çoğu zaman farklıdır. Bu farkın bedeli vardır. Kimsenin kullanmadığı lisanslar satın alınır ya da satın alınmadan kullanılır. Eski donanım yamasız biçimde ağda kalır. Ayrılan çalışanlar, kimsenin kaldırmayı hatırlamadığı sistemlere erişmeye devam eder. Bir hizmet masası, var olduğunu bilmediği ekipmanı destekleyemez.

BT varlık yönetimi (ITAM) bu farkı kapatma uygulamasıdır. Hizmet yönetimiyle yakından bağlantılıdır: hizmetler varlıklar üzerinde çalışır, olaylar ve değişiklikler varlıklara dokunur, bir hizmetin maliyeti de büyük ölçüde varlıklarının maliyetidir. Çevik ekipler için bu uygulamanın kendine özgü bir yönü vardır. Varlıklar artık bir betikle saniyeler içinde oluşturulup dakikalar sonra yok edilen bulut kaynaklarını, kapsayıcı (container) imajlarını, açık kaynak kütüphanelerini ve kartla satın alınan aboneliklerini de içerir. Satın alınmış ekipmanların tutulduğu bir elektronik tablo biçimindeki eski model bunları kapsamaz.

İngilizce Wikipedia'daki "IT asset management" başlıklı madde şu anda veri merkezi yönetimi maddesine yönlendirir ve ITAM orada bir bölüm olarak yer alır. Bu bölüm ITAM'i, yaşam döngüsü yönetimini ve stratejik BT kararlarını desteklemek için mali, sözleşmesel ve envanter işlevlerini birleştiren iş uygulamaları olarak tanımlar ve kısadır. Bu konu tanım için o bölümü kullanır, ayrıntıları yazılım varlık yönetimi ve yapılandırma yönetim veritabanları maddelerinden ekler ve uygulamayı çevik bağlama yerleştirir. Kaynakların ötesine geçtiği yerde bunu belirtir.

## Temel kavramlar

### Nedir

Veri merkezi varlık yönetimi üzerine Wikipedia bölümüne göre, Gartner'a atıfla, ITAM yaşam döngüsü yönetimini ve stratejik BT kararlarını desteklemek için mali, sözleşmesel ve envanter işlevlerini birleştiren bir dizi iş uygulamasıdır. Varlıklar iş ortamındaki yazılım ve donanımı kapsar. Uygulama envanter yönetimi olarak da adlandırılır. Madde, uygulamanın envanterin lisans haklarıyla karşılaştırılabilmesi için otomatik keşif kullandığını ve tam yönetimin, tedarik zinciri, yardım masası, satın alma, insan kaynakları ve ITSM sistemleriyle bütünleşik, birkaç türde bilgi barındıran bir depo gerektirdiğini belirtir.

### Neler varlık sayılır

Bir hizmet kuruluşu için işe yarar bir çalışma listesi:

| Varlık türü | Örnekler | Ele alındığı yer |
|---|---|---|
| **Donanım** | Dizüstü bilgisayarlar, sunucular, ağ cihazları, telefonlar, depolama | Konu 4.3 — Donanım Varlık Yönetimi |
| **Yazılım** | Lisanslı uygulamalar, işletim sistemleri, açık kaynak bileşenleri, abonelikler | Konu 4.2 — Yazılım Varlık Yönetimi |
| **Bulut ve hizmet kaynakları** | Sanal makineler, kapsayıcılar, depolama kovaları, SaaS hesapları | Konu 4.2 — Yazılım Varlık Yönetimi ve Konu 4.5 — BT Mali Yönetimi ve FinOps |
| **Veri ve bilgi** | Veri kümeleri, kayıtlar, yedekler | Konu 3.13 — Bilgi Güvenliği Yönetimi |
| **Sözleşmeler ve haklar** | Lisanslar, destek sözleşmeleri, garantiler | Konu 4.2 — Yazılım Varlık Yönetimi ve Konu 3.14 — Tedarikçi Yönetimi |
| **İnsanlar ve beceriler** | Personel ve yetkinlikler (genellikle varlık kaydında yer almaz ama hizmetin parçasıdır) | Konu 2.5 — Hizmet Yönetiminin Dört Boyutu |

Tablo bu kılavuzun çalışma listesidir, bir kaynaktan alınmış bir sınıflandırma değildir.

### Yaşam döngüsü

Wikipedia bölümü donanım varlık yönetimini, bilgisayar ve ağ bileşenlerinin edinilmesinden elden çıkarılmasına kadar olan süreci kapsayan bir uygulama olarak tanımlar; talep ve onay, satın alma, yaşam döngüsü yönetimi, yeniden konuşlandırma ve elden çıkarma uygulamalarını sayar ve donanım yaşam döngüsüne ilişkin mali bilginin yakalanmasının temel bir bileşen olduğunu söyler. Biçimsel bir aşama modeli vermez. Yaygın biçimde kullanılan ve burada da öyle sunulan pratik bir sıra şudur:

1. **Planlama ve talep:** neye ihtiyaç olduğuna karar verin ve onay alın.
2. **Edinme:** satın alın veya üretin, alımı kaydedin.
3. **Devreye alma:** hizmete sokun ve kullanıcıya ya da hizmete bağlayın.
4. **İşletme ve bakım:** yama uygulayın, destekleyin, taşıyın ve değişiklikleri izleyin.
5. **Emekliye ayırma ve elden çıkarma:** hizmetten çıkarın, verileri silin ve güvenli biçimde elden çıkarın.

Her aşamada kimin sorumlu olduğunu ve hangi kaydın tutulduğunu sorun.

### Envanter, keşif ve kayıtlar

Bir varlık kaydı ancak doğruysa işe yarar. Madde, otomatik keşfin envanterin haklarla karşılaştırılmasını desteklediğini belirtir. Keşif araçları var olanı bulmak için ağları ve bulut hesaplarını tarar; kayıt ise kuruluşun sahip olmayı ve ödemeyi amaçladığı şeyleri tutar. İkisi arasındaki farklar bulgudur: bilinmeyen cihazlar, kullanılmayan lisanslar, onaylanmamış abonelikler.

### ITSM ve CMDB ile ilişkisi

Wikipedia bölümü ITAM'in ITSM ile bütünleştiğini söyler ama onu ITIL süreçleriyle ayrıntılı biçimde eşlemez. ITIL anlatımları genellikle sahiplik, maliyet ve sözleşmelerle ilgilenen varlık yönetimini, bileşenler arasındaki ilişkilerle ilgilenen yapılandırma yönetiminden ayırır. Wikipedia'ya göre **yapılandırma yönetim veritabanı (CMDB)**, yapılandırma öğeleri adı verilen donanım ve yazılım varlıkları ile bunlar arasındaki ilişkilere dair bilgileri saklayan bir veritabanı için kullanılan ITIL terimidir (bkz. Konu 4.4 — Yapılandırma Yönetimi). Varlık kayıtları ile yapılandırma kayıtları çakışır; birçok kuruluş verileri, her kaynak kendi denetimini koruyacak biçimde birleştirir (federasyon).

### Standartlar

Wikipedia bölümü, yazılım varlık yönetimi için standart ailesi olarak ISO/IEC 19770'i anar ama parçalarını anlatmaz. Yazılım varlık yönetimi maddesi parçaları sıralar: kademeli düzeylerde uygulanabilen bir süreç çerçevesi olan BT varlık yönetim sistemi gereksinimleri üzerine 19770-1:2017; yazılım tanımlama etiketleri üzerine 19770-2:2015; hak yönetimi üzerine 19770-3:2016; kaynak kullanım ölçümü üzerine 19770-4:2017; genel bakış ve sözlük üzerine 19770-5:2015. Kesin ifade ve güncel sürümler için standartların kendisine bakın.

### Yararlar ve sınırlar

Wikipedia bölümü hiçbir yarar ve hiçbir eleştiri sıralamaz, hiçbir araç da anmaz. Daha düşük lisans maliyeti, azalan güvenlik riski ve daha iyi destek gibi pratik yararlar yaygın olarak ileri sürülür, ancak bu kılavuzun okunan kaynaklarında bunlara ilişkin ölçülmüş kanıt yoktur. Tasarruf iddialarına dikkatle yaklaşın, iddia edenlerden kanıtlarını isteyin ve kendi sonuçlarınızı ölçün.

### Çevik ve bulut bağlamında ITAM

Önceki on yılların uygulamaları, varlıkların BT tarafından satın alındığını, teslim edildiğini ve kurulduğunu varsayar. Bugün:

- **Ekipler kaynakları kendileri oluşturur,** bulut konsollarında veya kod aracılığıyla. Kayıt bunları satın alma siparişinden değil, bulut hesabından öğrenmelidir.
- **Varlıklar kısa ömürlüdür.** Bir kapsayıcı bir saat yaşayabilir. Her örneği değil, hizmeti ve hesabı izleyin.
- **Abonelikler lisansların yerini alır.** Yazılımın bedeli aylık olarak birinin kartından ödenir ve sahiplik belirsizdir.
- **Açık kaynak bileşenler** koda girerek, satın alma sisteminin dışından gelir (bkz. Konu 4.2 — Yazılım Varlık Yönetimi).

Bu değişiklikler ITAM'i otomasyona, etiketlemeye ve BT ile varlıkları kullanan ekipler arasında paylaşılan hesap verebilirliğe doğru iter.

## İyi uygulamalar

1. **En önemli olanla başlayın.** Önce maliyeti veya riski en yüksek varlıkları seçin: pahalı lisanslar, internete açık sunucular, hassas veri içeren cihazlar. Eksiksiz bir kayıt daha sonra gelebilir.
2. **Amaçlarınız için varlığın ne olduğunu tanımlayın.** İzleyeceğiniz varlık türlerinin kısa bir listesini ve her biri için ihtiyaç duyduğunuz bilgileri yazın: sahip, konum veya hesap, maliyet, sözleşme ve durum. Kimsenin kullanmayacağı alanlardan kaçının.
3. **Her varlık için bir sahip belirleyin.** Her varlıktan veya varlık grubundan bir kişi ya da ekip sorumlu olmalıdır. Sahipsiz varlıklar, israfın ve riskin biriktiği yerlerdir.
4. **Var olanı bulmak için keşfi kullanın.** Ağları, bulut hesaplarını ve uç noktaları tarayın ve kayıtla karşılaştırın. Farkları incelenecek maddeler olarak ele alın.
5. **Bulut kaynaklarını etiketleyin.** Bulut hesaplarında oluşturulan kaynaklarda sahip, hizmet ve ortam etiketlerini zorunlu kılın ve etiketsiz olanları raporlayın. Etiketler kaydın hızlı hareket eden varlıkları izlemesini sağlar.
6. **Satın almayı kayda bağlayın.** Abonelikler ve kartla yapılan alımlar dahil yeni satın almaların bir kayıt oluşturmasını veya güncellemesini sağlayın. Bunu yapmayan harcamaları gözden geçirin.
7. **Varlıkları hizmetlere bağlayın.** Her varlığın hangi hizmeti desteklediğini kaydedin. Bu, bir olayın, değişikliğin veya emekliye ayırmanın etkisini hesaplamanızı sağlar (bkz. Konu 4.4 — Yapılandırma Yönetimi).
8. **Mali yönü izleyin.** Maliyeti, sözleşme koşullarını, yenileme tarihlerini ve ilgili yerde amortismanı kaydedin. Wikipedia bölümünün de dediği gibi, yaşam döngüsü boyunca mali bilginin yakalanması donanım yönetiminin temel bir bileşenidir.
9. **Kullanım ömrünün sonunu yönetin.** Emekliye ayırmayı baştan planlayın: veri silme, iade ve elden çıkarma. Erişimi ve lisansları aynı anda kaldırın.
10. **Düzenli gözden geçirin.** En önemli varlık sınıfları için kaydı yılda en az iki kez gerçeklikle karşılaştırın. Herhangi bir farka yol açan süreci düzeltin.
11. **Veriyi paylaşın.** Varlık verisini hizmet masasının, güvenliğin, finansın ve ekiplerin kullanabileceği bir biçimde erişilebilir kılın. Yalnızca varlık yöneticisinin gördüğü verinin değeri azdır.
12. **Uygulamayı ölçün.** Kaydın ne kadar eksiksiz ve doğru olduğunu, bir varlığı bulmanın ne kadar sürdüğünü ve kullanılmayan kalemlerin maliyetini izleyin. Bunları insanları sıralamak için değil, iyileştirmek için kullanın.

## Ekibinizle tartışılacak sorular

**Birisi her türden kaç varlığımız olduğunu sorsa, ne kadar emin olurduk?**

Herkesten dizüstü bilgisayar, sunucu, bulut hesabı ve abonelik sayısını tahmin etmesini isteyin, sonra kayıtla karşılaştırın. Farklar ne kadarının bilinmediğini gösterir. Kolaylaştırıcı, insanların en az hangi kategoriye güvendiğini sorabilir. Önce uzlaştırılacak birini seçin.

**Her varlığımızın sahibi kim ve o kişi ayrılınca ne olur?**

Bir varlık örneklemi alın ve sahip alanına bakın. Sahibi olmayan veya sahibi ayrılmış olanları sayın. İnsanlar yer değiştirdiğinde sahipleri hangi sürecin güncellemesi gerektiğini sorun. İşten ayrılma süreci gibi tek bir tetikleyicide anlaşın.

**Kimsenin kullanmadığı neler için ödeme yapıyoruz?**

Lisanslara, aboneliklere ve bulut kaynaklarına bakın ve hangilerinin yakın zamanda kullanılmadığını sorun. Sürprizlere hazırlıklı olun. Bir şeyin iptaline kimin yetki verebileceğini sorun. En büyük üçünü seçin ve her birini kontrol edin.

**Yeni bir bulut kaynağını veya aboneliği nasıl öğreniyoruz?**

Sonuncusunun izini sürün. Yanıt çoğu zaman "faturada" veya "bozulduğunda" olur. Satın almanın, etiketlemenin ve keşfin bunu nasıl daha erken yakalayabileceğini tartışın. Zorunlu etiketler veya etiketsiz kalemlerin aylık raporu gibi tek bir denetimde anlaşın.

**Bir dizüstü bilgisayara veya sunucuya kullanım ömrünün sonunda ne oluyor?**

Adımları gözden geçirin: kim karar veriyor, veriler nasıl kaldırılıyor, kayıt ne diyor. Boşluklar genellikle veri silme ve kayıtlar çevresinde ortaya çıkar. Yakın tarihli bir elden çıkarmanın doğru yapıldığına dair kanıt isteyin. Kısa bir kontrol listesi planlayın.

**Diğer ekiplerin ihtiyaç duyduğu ama onlara vermediğimiz hangi varlık verileri var?**

Hizmet masasına, güvenliğe ve finansa görmek istediklerini sorun. Tipik talepler sahip, hizmet ve maliyettir. Bunun nasıl paylaşılacağını ve güncel tutulmasından kimin sorumlu olacağını tartışın. Üretilecek tek bir rapor seçin.

## Uygulamada: çevik bir ITIL örneği

1.800 çalışanı olan ulusal bir istatistik kurumu, anket işleme faaliyetlerini şirket içi bir veri merkezi ile bir genel bulut hesabının karışımında yürütüyor. Finans ekibi bulut faturasının bir yılda üçte bir oranında arttığını fark ediyor ve bir güvenlik denetimi veri merkezinde kimsenin tanımlayamadığı üç sunucu buluyor. ITAM işlevi, elektronik tablosu olan iki kişiden oluşuyor.

BT başkanı mütevazı bir hedef koyuyor: ana varlıkları, sahiplerini ve maliyetlerini bilmek, işe bulutla başlayarak. Yeni bir kural her bulut kaynağında sahip, hizmet ve ortam etiketleri istiyor. Haftalık bir rapor etiketsiz kaynakları listeliyor ve ekiplerin bunları sahiplenmek ya da kaldırmak için iki haftası var. Veri merkezinde iki ITAM çalışanı bir keşif taraması yapıp sonucu elektronik tabloyla karşılaştırıyor ve listede olmayan 40 cihaz buluyor. Çoğunun sahibini buluyorlar. Satın alma birimi, her yeni yazılım aboneliğinin bir hafta içinde ITAM'e bildirilmesi konusunda anlaşıyor.

Bir çeyrek sonra, bulut kaynaklarında etiketsiz payı yaklaşık üçte birden bir avuca iniyor ve finans bulut faturasını hizmetlere atfedebiliyor. Birkaç kullanılmayan kaynak kapatılıyor ve iki sunucu emekliye ayrılıyor. Sorunlar sürüyor. Bir araştırma grubu araçları bir bölüm kartıyla satın alıyor ve bildirmiyor; haftalık raporu da yalnızca birkaç ekip okuyor. ITAM çalışanları araştırma grubuyla basit bir kayıt formu konusunda konuşuyor ve finans başkanından abonelikleri aylık gözden geçirmeye eklemesini istiyor. Ayrıca kaydın bulut hizmetlerini her kısa ömürlü örnek yerine hesap ve hizmet düzeyinde kapsamasına karar veriyorlar.

## Dört bakış açısı

### Ürün ve teslimat ekipleri

Teslimat ekipleri çok sayıda varlık oluşturur. Oluşturduklarınızı etiketleyin, eklediğiniz abonelikleri ve kütüphaneleri kaydedin, artık ihtiyaç duymadıklarınızı emekliye ayırın. Kaydı, katkıda bulunduğunuz ve yararlandığınız bir hizmet olarak görün.

### Hizmet ve operasyon ekipleri

Operasyon ekipleri destek, yama ve olay müdahalesi için kayda bağımlıdır. Konuşlandırma, değişiklik ve emekliye ayırma sırasında güncelleyerek doğru tutun. Eksik olanı bulmak için keşfi kullanın ve farkları sahiplere bildirin.

### Liderlik ve yönetişim

Liderler ve finans, harcama, risk ve yenileme kararları için varlık verisini kullanır. Kusursuz bir kayıt yerine, hizmete göre harcama ve sahibi olan varlıkların payı gibi birkaç güvenilir sayı isteyin. Kaydı doğru tutan etiketler ve satın alma raporlaması gibi küçük denetimleri destekleyin.

### Müşteriler ve kullanıcılar

Kullanıcılar, ekipmanları ve erişimleri iyi yönetildiğinde yarar sağlar: çalışan cihazlar, hızlı yenileme ve sürpriz ücretlerin olmaması. Eklediğiniz veya artık ihtiyaç duymadığınız ekipmanı hizmet masasına bildirin ve elinizdekileri doğrulamanız istenmesini bekleyin.

## Yaygın başarısızlık biçimleri

- **Kimsenin güvenmediği bir kayıt.** Güncel değildir ve görmezden gelinir. Bunun yerine kapsamı daraltın, keşfi kullanın ve her yaşam döngüsü olayında güncelleyin.
- **Sahipsizlik.** Varlıklar kimseye ait değildir. Bunun yerine her varlık veya grup için bir sahip zorunlu kılın.
- **Her şeyi izlemek.** Çaba değeri gömer. Bunun yerine maliyetli veya riskli olanla başlayın ve büyütün.
- **Bulutu ve abonelikleri yok saymak.** Kayıt yalnızca satın alınmış donanımı kapsar. Bunun yerine bulut kaynaklarını etiketleyin ve abonelikleri yakalayın.
- **Süreç dışı satın alma.** Kartla yapılan alımlar kaydı atlar. Bunun yerine satın almayı ve harcama raporlarını ITAM'e bağlayın.
- **Kullanım ömrü sonu süreci olmaması.** Eski cihazlar veri ve erişimi korur. Bunun yerine emekliye ayırmayı, veri silmeyi ve elden çıkarmayı planlayın.
- **Verinin başkalarından saklanması.** Kaydı yalnızca ITAM görür. Bunun yerine hizmet masası, güvenlik ve finansla paylaşın.
- **Eyleme geçmeden saymak.** Raporlar kullanılmayan varlıkları gösterir ve hiçbir şey iptal edilmez. Bunun yerine bulgular üzerinde harekete geçmesi için sahipler atayın.

## Olgunluk modeli

| Boyut | Başlangıç | Gelişim | Standartlaştırma | Yönetim | Eşgüdüm |
|---|---|---|---|---|---|
| Envanter ve keşif | Varlıklar elektronik tablolarda listelenir ya da hiç listelenmez | Bazı varlık sınıfları envantere alınır | Keşif ve bir kayıt ana varlık sınıflarını kapsar ve düzenli olarak uzlaştırılır | Eksiksizlik ve doğruluk ölçülür, boşluklar giderilir | Envanter şirket içi, bulut ve tedarikçileri paylaşılan verilerle kapsar |
| Sahiplik ve hesap verebilirlik | Az sayıda varlığın sahibi vardır | Bazı varlıklar için sahipler belirlenmiştir | Her varlık veya grubun sahibi vardır ve süreçle güncel tutulur | Sahiplik boşlukları izlenir ve çözülür | Ekipler ve tedarikçiler arasındaki sahipler ortak kurallara göre çalışır |
| Yaşam döngüsü ve mali denetim | Satın alma ve elden çıkarma gayriresmidir | Bazı varlıkların maliyet ve sözleşme verisi vardır | Yaşam döngüsü adımları ve mali veriler ana varlıklar için kaydedilir | Maliyet, yenilemeler ve kullanım gözden geçirilir ve bunlara göre harekete geçilir | Mali ve yaşam döngüsü verileri hizmetlere bağlanır ve finansla paylaşılır |
| Verinin kullanımı | Veriyi az kişi kullanır | Hizmet masası kaydı ara sıra kullanır | Masa, güvenlik ve finans varlık verisini rutin olarak kullanır | Veri kalitesi ve kullanımı ölçülür ve iyileştirilir | Veri, kuruluş genelinde ve ortaklarla birlikte kararları besler |

## Kontrol listesi

- [ ] Kısa bir varlık türleri listemiz ve her biri için kaydettiğimiz bilgiler var.
- [ ] İzlenen her varlığın veya grubun adı belli bir sahibi var.
- [ ] Keşif sonuçları düzenli bir takvimle kayıtla karşılaştırılıyor.
- [ ] Bulut kaynaklarında sahip, hizmet ve ortam etiketleri var ve etiketsiz olanlar raporlanıyor.
- [ ] Abonelikler dahil yeni satın almalar bir kayıt oluşturuyor veya güncelliyor.
- [ ] Varlıklar desteklediği hizmetlere bağlı.
- [ ] Ana varlıklar için maliyet, sözleşme ve yenileme verileri kaydediliyor.
- [ ] Emekliye ayırma; veri kaldırmayı, erişim kaldırmayı ve bir kaydı içeriyor.
- [ ] Kayıt, ana varlık sınıfları için yılda en az iki kez gerçeklikle uzlaştırılıyor.
- [ ] Hizmet masası, güvenlik ve finans ihtiyaç duydukları veriyi görebiliyor.

## Yapay zeka istemleri

**Amaç: keşif sonuçlarını kayıtla uzlaştırmak.**

```text
I have two lists of assets: what our register says we have, and what a discovery scan found. 

Register: [paste a table with asset name or ID, type, owner, and status; remove personal data].
Discovery: [paste a table with name or ID, type, and any identifying details].

Using only these lists, identify: items in the register not found by discovery; items found by discovery not in the register; and items where the details differ. For each group, suggest a question to ask the owner or the team. Do not guess what an unknown item is. If the lists are too thin to match, say what to add. List what you are unsure of.
```

**Amaç: bulut kaynakları için kısa bir etiketleme standardı taslağı hazırlamak.**

```text
Help me draft a one-page tagging standard for cloud resources.

Our cloud accounts and teams: [describe].
Facts we need to know about a resource: [for example owner, service, environment, cost center, data sensitivity].
Problems today: [for example untagged resources and unknown owners].

Propose three to six required tags with allowed values or formats, how untagged resources will be found and reported, who is responsible for fixing them, and a grace period (leave the length as [to be agreed]). Mark assumptions. Do not invent our tooling. Ask clarifying questions first, and list what you are unsure of.
```

**Amaç: bir cihaz veya sunucu için emekliye ayırma kontrol listesi planlamak.**

```text
Help me write a retirement checklist for [asset type, for example "laptops" or "servers"].

Our current practice: [describe].
Data it may hold: [describe sensitivity].
Records we must keep: [list, or write "unknown"].
Rules or contracts that apply, with source text: [paste, or write "none known"].

Produce a checklist covering: approval, removing access and licenses, data wiping or destruction and evidence, updating the register, financial records, and disposal or return. Mark every item that is an assumption. Do not state that a law requires a step unless I pasted its text. Ask clarifying questions first, and list what you are unsure of.
```

**Amaç: kullanım verilerinden tasarruf adaylarını bulmak.**

```text
Here is a table of our subscriptions and licenses with cost per month, number of paid seats, and number of active users in the last 90 days: [paste real data].

Using only my numbers, list items where paid seats exceed active users and compute the difference and the cost of the unused seats. Rank by cost. For the top five, suggest a question to ask the owner before changing anything. Do not assume that inactive users can lose access; flag it as a question. List what you are unsure of.
```

## Yapay zeka becerileri

- [configuration-management](../../../../skills/configuration-management/SKILL.md): varlıkların ve aralarındaki ilişkilerin nasıl kaydedileceğini ve doğru tutulacağını planlamak için kullanın.
- [vendor-management](../../../../skills/vendor-management/SKILL.md): varlıkların arkasındaki sözleşmeleri ve yenilemeleri yönetmek için kullanın.
- [budget-forecasting](../../../../skills/budget-forecasting/SKILL.md): varlıkların ve aboneliklerin maliyetini tahmin etmek için kullanın.
- [raci-matrix](../../../../skills/raci-matrix/SKILL.md): her varlık sınıfının kimin sahipliğinde, desteğinde ve onayında olduğunu netleştirmek için kullanın.
- [data-governance](../../../../skills/data-governance/SKILL.md): varlıklarda tutulan verinin sahibini ve nasıl emekliye ayrılacağını belirlemek için kullanın.

## Temel kaynaklar

- **IT asset management** (Wikipedia, şu anda veri merkezi yönetimi maddesinin içinde): kısa bir tanım ve donanım varlık yönetiminin bir tanımı.
- **Software asset management** (Wikipedia): tanım, hedefler, teknolojiler ve ISO/IEC 19770 parçaları.
- **Configuration management database** (Wikipedia): yapılandırma öğeleri ve ilişkilerin deposu için ITIL terimi.
- **ITIL** (Wikipedia): ITAM'i hizmet yönetimiyle birlikte ele alan çerçeve.

## Kaynakça

1. IT asset management — Wikipedia — https://en.wikipedia.org/wiki/IT_asset_management
2. Software asset management — Wikipedia — https://en.wikipedia.org/wiki/Software_asset_management
3. Configuration management database — Wikipedia — https://en.wikipedia.org/wiki/Configuration_management_database
4. ITIL — Wikipedia — https://en.wikipedia.org/wiki/ITIL
5. IT service management — Wikipedia — https://en.wikipedia.org/wiki/IT_service_management
6. Data center management — Wikipedia — https://en.wikipedia.org/wiki/Data_center_management
7. Cloud computing — Wikipedia — https://en.wikipedia.org/wiki/Cloud_computing
8. Asset management — Wikipedia — https://en.wikipedia.org/wiki/Asset_management
9. Inventory — Wikipedia — https://en.wikipedia.org/wiki/Inventory
