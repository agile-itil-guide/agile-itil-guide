# Çevikliği Ölçeklendirme

**Çevikliği ölçeklendirmek, çevikliği işe yarar kılan kısa geri bildirim döngülerini kaybetmeden birçok ekibi, hizmeti ve tedarikçiyi eşgüdümlemek demektir; ana risk, hangi sorunu çözdüğünüzü bilmeden süreç katmanları eklemektir.**

## Bu neden önemli

On kişiye kadar tek bir çevik ekip her gün birbiriyle konuşabilir. Gerçek bir hizmet genellikle daha fazlasını kapsar: birkaç teslimat ekibi, bir operasyon grubu, bir hizmet masası, güvenlik, bir ağ ekibi ve tedarikçiler. Birçok grubun işinin birbirine uyması gerektiğinde, tek bir ekibin günlük sohbeti yeterli değildir ve yeni sorunlar ortaya çıkar. Öncelikler çatışır, bağımlılıklar işi durdurur ve her ekip kendi parçasını iyileştirirken hizmetin bütünü iyileşmez.

Birkaç çerçeve bunu çözdüğünü iddia eder. Boyut, maliyet ve felsefe bakımından ayrılırlar ve güçlü görüşler çekerler. Bazı kuruluşlar büyük bir çerçeveyi bir program olarak benimser ve devreye almaya yıllar harcar. Diğerleri engelleri kaldırarak ve küçük bir kurallar kümesi tutarak ölçeklenir. [Çevik yazılım geliştirme hakkındaki Wikipedia maddesinin](https://en.wikipedia.org/wiki/Agile_software_development) desteklediği dürüst konum, ölçeklendirme çerçevelerinin etkililiği konusunda görüşlerin ayrıldığı ve kanıtın sınırlı olduğudur.

BT hizmet yönetimi (ITSM) alanındaki insanlar için ölçeklendirme önemlidir; çünkü ITIL zaten ölçekte çalışır. Birçok uygulamayı ve tarafı birbirine bağlayan bir hizmet değer sistemi tanımlar (bkz. Konu 2.3 — ITIL Hizmet Değeri Sistemi). Bu konunun yardımcı olduğu soru ikisinin nasıl birleştirileceğidir: kullanıcıları koruyan hizmet yönetimi uygulamalarını sürdürürken ve birincinin üzerine ikinci bir bürokrasi katmanı kurmadan birçok çevik ekibi nasıl eşgüdümleyeceğiniz.

## Temel kavramlar

### Bir ekip neden çoğundan farklıdır

Çevik yazılım geliştirme hakkındaki Wikipedia maddesi, bir proje yaklaşık 20'den fazla geliştirici içerdiğinde ya da ekipler lokasyonlara dağıldığında ölçeklendirmenin zorluklar getirdiğini bildirir. Bu durumlar için stratejiler ve çerçeveler vardır, ama madde bunların çevikliğin tanımına uyup uymadığı konusunda çelişen görüşleri not eder.

Ekip eklediğinizde üç sorun yinelenir:

- **Hizalanma:** ekiplerin ortak bir yöne ve tutarlı önceliklere ihtiyacı vardır; yoksa farklı şeyleri en iyilerler.
- **Bağımlılıklar:** bir ekipteki iş bir diğerini bekler ve ekip sayısı arttıkça beklemeler çoğalır.
- **Entegrasyon:** birçok ekibin çıktısı bir hizmet olarak çalışan bir şeyde bir araya gelmelidir ve bunu ne kadar geç test ederseniz sürprizler o kadar maliyetli olur.

### Dört tanınmış yaklaşım

Aşağıdaki tablo dört adlandırılmış yaklaşımı özetler. Özetler Wikipedia maddelerine ve bu kılavuz için okunan çerçeve sahiplerinin kendi sayfalarına dayanır; ayrıntılara güvenmeden önce güncel sürümleri kaynaklarında denetleyin.

| Yaklaşım | Yaratıcılar ya da sahibi | Ana fikir | Boyut ve biçim |
|---|---|---|---|
| **Scaled Agile Framework (SAFe)** | İlk olarak Dean Leffingwell'in 2007 tarihli *Scaling Software Agility* kitabında anlatıldı; materyaller Scaled Agile, Inc. tarafından yayımlanır | Çevik, yalın ürün geliştirme ve sistem düşüncesinden yararlanan bir örgütlenme ve iş akışı kalıpları kümesi | Bir ekip ve program düzeyinden (Agile Release Trains) büyük çözümlere ve portföylere kadar yapılandırmalar |
| **Large-Scale Scrum (LeSS)** | Craig Larman ve Bas Vodde | Scrum'ın kendisini ölçeklendirin: tek bir ürün için tek bir Product Owner ve tek bir Product Backlog, çok sayıda çapraz işlevli özellik ekibi ve mümkün olduğunca az ek rol ve çıktı | Yaklaşık iki ila sekiz ekip için LeSS; daha fazlası için, her biri birkaç ekipten oluşan Requirement Areas ile LeSS Huge |
| **Disciplined Agile (DA)** | Scott Ambler ve Mark Lines; Ağustos 2019'da Project Management Institute (PMI) tarafından satın alındı | Bir ekibin bağlam içinde kendi çalışma biçimini seçmesine yardımcı olan süreç hedefleri ve seçenekleri araç takımı | Birkaç yaşam döngüsü ve kuruluş için bir katmanla karma ve bağlama duyarlı |
| **Scrum@Scale ve diğerleri** | Wikipedia maddesinde SAFe ile birlikte anılır | Birden çok Scrum ekibini eşgüdümlemek için başka çerçeveler | Sahiplerinin sitelerine bakın |

### SAFe daha ayrıntılı

Wikipedia maddesi, SAFe'in ilk kez 2007'de resmen anlatıldığını, ilk sürümünün 2011'de ve 6.0 sürümünün Mart 2023'te çıktığını söyler. 5.1 sürümü için dört yapılandırma listeler: Essential SAFe (ekip ve program düzeyi), Large Solution SAFe, Portfolio SAFe ve Full SAFe. Madde ayrıca ekonomik bir bakış almak ve sistem düşüncesini uygulamak dahil on ilke listeler.

SAFe, maddenin kaydettiği açık eleştiri çekmiştir. Thoughtworks, yukarıdan aşağıya denetimin israf ürettiğini savundu, Ken Schwaber onu 2013'te bir yazıda eleştirdi ve Jeff Gothelf 2021'de SAFe'in çevik olmadığını savundu. Eleştirmenler onu hiyerarşik ve esnek olmayan olarak niteler ve bir kuruluşa eski süreçleri korurken çeviklik görüntüsü verebileceğini söyler. Destekçiler ortak sözcük dağarcığını ve büyük kuruluşlar için yapısını değerli bulur. Karar vermeden önce her iki tarafı okuyun.

### LeSS: çıkararak ölçeklendirin

Larman ve Vodde, LeSS'i tek bir ürün üzerinde çalışan birçok ekibe uygulanan Scrum olarak tanımlar. Scrum'ın üzerine hiçbir katman eklemez. Çerçevenin kendi girişine göre tek bir Product Owner tek bir Product Backlog yönetir ve ekipler ortak bir Sprint'te tek bir sevk edilebilir ürün üretir. LeSS "daha azla daha fazla" fikrini ortaya koyar: daha az rol, çıktı ve kural daha sorumlu ekipler üretir. Altta yatan yöntem için bkz. Konu 1.4 — Teslimat Tahmini ve Planlama Metrikleri.

### Disciplined Agile: çalışma biçiminizi seçin

Disciplined Agile Delivery hakkındaki Wikipedia maddesi, tüm teslimat yaşam döngüsünü kapsayan, insan öncelikli, karma bir araç takımını anlatır. Altı yaşam döngüsünü destekler ve 21 süreç hedefi tanımlar. Yaklaşım, bir çerçeveyi dayatmak yerine ekiplerin durumlarına uygun uygulamaları seçmesine yardım etmektir. Madde, konuya yakın kaynaklara fazla güvenmiş olabileceğine dair bir bakım bildirimi taşır.

### Scrum of Scrums ve basit eşgüdüm

Bir çerçeve benimsemeden önce en basit araçları düşünün. Bir "scrum of scrums", ilerlemeyi paylaşmak ve bağımlılıkları çözmek için birkaç ekibin temsilcilerini bir araya getirir. Ortak üç aylık planlama, bir ürün için ortak bir iş listesi ve ekip liderlerinin düzenli bir toplantısı diğer hafif seçeneklerdir. Birçok kuruluş bunlarla yeterince iyi ölçeklenir.

### Bir hizmet kuruluşunda ölçeklendirme

Bir BT kuruluşunda ekipler birkaç biçimde örgütlenebilir ve seçim, çevikliğin ne kadar iyi ölçeklendiğini etkiler:

| Örgütlenme | Ekipler nasıl örgütlenir | Ölçeklendirmeye etkisi |
|---|---|---|
| **Bileşene göre** | Her teknik katman ya da sistem için bir ekip | Özellikler birkaç ekip gerektirir, bu yüzden bağımlılıklar çoktur |
| **Özelliğe ya da ürüne göre** | Müşteriye dönük bir dilimin sahibi olan çapraz işlevli ekipler | Daha az bağımlılık; platformlar için ortak standartlar gerekir |
| **Hizmete göre** | Her hizmet için, inşa ve işletmesinin sahibi olan bir ekip | Hizmet yönetimine yakın; ortak platformlarla başa çıkmanın bir yolu gerekir |
| **Platform artı akış** | Bir platform sağlayan ekipler ve onu kullanan ekipler | Aralarında net hizmet anlaşmaları gerekir |

Hiçbir kalıp herkes için en iyisi değildir. Bileşen ekiplerinden ürün ya da hizmet etrafında örgütlenmiş ekiplere geçmek yaygın bir adımdır ve yapması zordur; çünkü kimin kime rapor verdiğini değiştirir.

### Araştırma ve eleştiri ne diyor

Çevik yazılım geliştirme maddesi, genel olarak çevik yöntemler için ampirik kanıtın sınırlı ve kesin sonuç vermeyen nitelikte olduğunu belirtir. Ölçeklendirme çerçeveleri için başvurulan kaynaklar çoğunlukla görüşler ve satıcı materyali sunar. Ölçülmüş iyileşme iddialarına dikkatle yaklaşın, arkasındaki kanıtı isteyin ve herhangi bir çerçeveyi önce kuruluşunuzun küçük bir parçasında sınayın.

## İyi uygulamalar

1. **Çerçeveden değil, sorundan başlayın.** Neyin ters gittiğini adlandırın: yavaş bağımlılıklar, çatışan öncelikler, geç entegrasyon. Bunu ele alan en hafif yaklaşımı seçin ve yalnızca yetersiz kalırsa daha fazlasını benimseyin.
2. **Önce en basit eşgüdümü deneyin.** Ortak planlama, bir scrum of scrums ve her ürün için ortak bir iş listesi birçok sorunu küçük maliyetle çözer. Yapıyı yalnızca bunlar işlemeyi bıraktığında ekleyin.
3. **Ekipleri değer etrafında örgütleyin.** Bir ürünün ya da hizmetin baştan sona sahibi olan, onu inşa etme ve işletme becerilerine sahip ekipleri tercih edin. Bu, devirleri ve bağımlılıkları azaltır ve ITIL'in hizmetleri düşünme biçimine uyar (bkz. Konu 2.6 — Hizmet Değer Zinciri).
4. **Ürün başına tek sıralı bir liste tutun.** LeSS'in önerdiği gibi, tek bir sorumlu sahibi olan tek bir ürün iş listesi, ekipler arasındaki çatışmanın büyük kısmını ortadan kaldırır. Bu mümkün olmadığında, ekipler arasındaki öncelik sırasını görünür kılın.
5. **Düzenli bir ritimle birlikte planlayın.** Hedefler, bağımlılıklar ve riskler üzerinde hizalanmak için ekipleri ve temel paydaşları birkaç ayda bir bir araya getirin. Etkinliği kısa ve kanıta dayalı tutun ve ayrıntılı planlar üzerine bir pazarlığa dönüşmesini önleyin.
6. **Sürekli entegre edin.** Tüm ekiplerin çıktısını mümkün olduğunca sık, ideal olarak her gün birlikte test edin. Geç entegrasyon, büyük programların sponsorlarını şaşırtmasının en yaygın nedenidir (bkz. Konu 1.6 — Extreme Programming).
7. **Bağımlılıkları görünür kılın ve azaltın.** Hangi ekiplerin hangilerini beklediğini listeleyin ve beklemeleri sayın. Ekip sınırlarını değiştirerek, becerileri paylaşarak ya da net arayüzlü ortak platformlar kurarak azaltın.
8. **Ekipler arasında hizmet anlaşmaları tanımlayın.** Bir ekip diğerine bir platform ya da hizmet sağladığında, neyin beklendiği konusunda anlaşın: erişilebilirlik, yanıt, destek saatleri ve değişiklik nasıl istenir (bkz. Konu 3.7 — Hizmet Seviyesi Yönetimi).
9. **Uyarlayın ve neyi değiştirdiğinizi yazın.** Hangi çerçeveyi benimserseniz benimseyin, hangi parçaları izlediğinizi, hangilerini dışarıda bıraktığınızı ve nedenini kaydedin. Dürüst etiketler, bir karmanın hiç izlemeyi amaçlamadığı bir çerçeveye karşı yargılandığı durumu önler.
10. **Yaygınlaştırmadan önce pilot yapın.** Yaklaşımı birkaç ekiple deneyin, önemsediğiniz sonuçları ölçün ve öğrenin. Yalnızca pilot, tarif edebileceğiniz bir yarar gösterdiğinde genişletin.
11. **Yönetişimi hafif ve sonuç temelli tutun.** Her ekibin farklı biçimde yazdığı durum raporları değil, teslimat akışı, olay eğilimleri ve kullanıcı geri bildirimi gibi kanıt isteyin (bkz. Konu 5.7 — Yönetişim, Risk ve Uyum).
12. **Yapıyı düzenli gözden geçirin.** Ekip sınırlarının, rollerin ve törenlerin işe hâlâ hizmet edip etmediğini sormak için yılda bir ya da iki kez bir gözden geçirme yapın. 30 kişi için doğru olan yapılar 300 kişi için yanlış olabilir.

## Ekibinizle tartışılacak sorular

**Ölçeklendirmenin hangi sorunu çözmesini bekliyoruz ve çözüldüğünü nasıl anlayacağız?**

İnsanlardan acıyı adlandırmalarını isteyin: geç entegrasyon, çatışan öncelikler, diğer ekipler için uzun beklemeler. Her birini yakın tarihli bir örnekle yazın. Belirtilmiş bir sorun olmadan seçilen bir çerçeve, bir sorun arayan bir çözümdür. Kolaylaştırıcı her sorun için mümkün olan en basit çözümün ne olacağını ve işe yaradığını hangi kanıtın göstereceğini sorabilir.

**En çok hangi diğer ekipleri bekliyoruz ve ne kadar bekliyoruz?**

Bağımlılıkları bir duvarda haritalayın ve her biri için tipik beklemeyi ekleyin. Kendini bağımsız gören ekipler çoğunlukla şaşırır. Hangi bağımlılıkların gerçek, hangilerinin tarihsel ekip sınırlarından geldiğini sorun. Ekiplerin nasıl örgütlendiğini değiştirerek ya da becerileri paylaşarak kaldırılacak bir bağımlılık seçin.

**Ekiplerimiz arasında işin sırasına kim karar veriyor ve bunu nasıl öğreniyoruz?**

Yakın tarihli bir öncelik çatışmasını başından çözümüne kadar izleyin. Üst kademeye taşımalara, toplantılara ve gayriresmî anlaşmalara bakın. LeSS'te olduğu gibi tek bir sorumlu kişinin kararı verip veremeyeceğini sorun. Neyin kaybedileceğini ya da kazanılacağını düşünün. İyi bir sonuç, yeni bir rol olmasa bile çatışmaları karara bağlamak için net bir yoldur.

**SAFe, LeSS ya da Disciplined Agile gibi bir çerçeve bize daha ucuza elde edemeyeceğimiz neyi verirdi?**

Her biri hakkında okumuş birinden onu birkaç cümleyle açıklamasını ve en güçlü eleştirileri istemesini isteyin. SAFe hakkındaki Wikipedia maddesi birkaçını listeler ve çerçeve sahiplerinin siteleri yararları listeler. Kolaylaştırıcı tartışmayı pratik tutmalıdır: onu benimseseydik Pazartesi ne yapardık ve kimin neyi değiştirmesi gerekirdi? Neyi deneyeceğinize, varsa, ve neyi olduğu gibi bırakacağınıza karar verin.

**Tüm ekiplerimizin işinin birbirine uyduğunu nasıl sınıyoruz ve ne sıklıkla?**

Bir ekibin bir değişikliği ile bunun diğer herkesin değişiklikleriyle ilk testi arasındaki günleri sayın. Daha uzun boşluklar daha büyük sürprizler demektir. Ortamlar, test verisi ya da sahiplik gibi günlük entegrasyonu neyin engellediğini sorun. Kaldırılacak bir engel seçin.

**Denetimlerimizden hangileri her ekibe aynı biçimde uygulanıyor ve hangileri riske bağlı olmalı?**

Gözden geçirmeler, onaylar ve raporlama gibi standart denetimleri listeleyin. Hangilerinin düşük riskli iş için ayarlandığını sorun. Tekdüze denetimlerin yönetimi kolaydır ve herkes için yavaştır. Riske bağlı denetimler net ölçütlere ihtiyaç duyar. Gözden geçirilecek bir denetim seçin.

## Uygulamada: çevik bir ITIL örneği

Büyük bir perakende bankasının BT grubunun 14 teslimat ekibi ve merkezi bir operasyon grubu var. Her ekip Scrum'ı benimsemiş, ama bankanın müşterileri çok az iyileşme görüyor. Mobil bankacılık uygulamasının sürümleri beş ekipten değişiklik gerektiriyor ve her sürümü bağımlılıkları bir elektronik tabloda izleyen bir program ofisi eşgüdümlüyor. Yakın tarihli bir sürüm, iki ekip değişikliklerinin uyumsuz olduğunu son dakikada keşfettiği için üç hafta gecikti.

Bir mimar ve operasyon başkanı altı aylık sürümler üzerinde bir inceleme yürütür. Gecikmelerin çoğunun geç entegrasyondan ve mobil özelliklerin iş listesini paylaşan ekipler arasındaki belirsiz önceliklerden geldiğini bulurlar. Büyük bir çerçeve benimsemeyi düşünürler, ama küçük başlamaya karar verirler. Mobil uygulama için tek bir sorumlu ürün sahibi olan tek bir iş listesi oluştururlar ve beş ekibin planlamasını altı haftada bir ortak bir oturumda birleştirirler. Tüm ekiplerin değişikliklerini her gece birlikte derleyen ve test eden ortak bir boru hattı kurarlar ve operasyon grubunu ortak planlama oturumuna eklerler.

İki çeyrek sonra son dakika uyumsuzluklarının sayısı düşer ve sürümler iki haftada bir gelir. Bazı sorunlar sürer. Ürün sahibi taleplerin hacmiyle boğuşur ve zamanının çoğunu hakemlikle geçirir ve iki ekip hâlâ uzun kuyruğu olan merkezi bir veritabanı ekibine bağımlıdır. Banka, veritabanı ekibinin kuyruğunu ortak planlamada görünür kılmayı ve yaygın veritabanı değişiklikleri için bir self servis yolu denemeyi kabul eder. Ayrıca, ikinci bir ürün alanı aynı yaklaşımı deneyene kadar herhangi bir çerçeve kararını ertelemeye karar verir.

## Dört bakış açısı

### Ürün ve teslimat ekipleri

Teslimat ekipleri ölçeklendirmenin yükünün çoğunu taşır: ortak planlama, ortak boru hatları ve komşularla anlaşmalar. Bağımlılıkları kaynağında azaltmak için, bir sonraki ekibin becerilerini öğrenerek ya da eşgüdüm gerektirmeyen arayüzler kurarak çalışın. Planlama etkinliklerine ilerleme ve risk hakkında gerçek bilgiyle katılın.

### Hizmet ve operasyon ekipleri

Operasyon çalışanları planlamanın başından itibaren parçası olmalıdır; çünkü ekipler arası bağımlılıkların çoğu operasyoneldir: ortamlar, erişim, izleme ve destek. Planlama oturumuna hizmet verisi getirin ve size bağımlı ekiplerle hizmet seviyeleri konusunda anlaşın. Teslimat ekiplerine self servis sağlayan platformları savunun.

### Liderlik ve yönetişim

Liderler, ölçeklendirmenin ne kadar iyi işlediğini belirleyen yapıyı şekillendirir. Kuruluşun ne olmak istediğine karar vermenin yerine bir çerçeve satın alma dürtüsüne direnin. Sorunun net bir ifadesini, bir pilot ve kanıt isteyin. Raporlamayı hafif tutun ve yapı değişikliklerinin yöneticiler için rahatsız edici olabileceğini kabul edin.

### Müşteriler ve kullanıcılar

Müşteriler ekipler arasındaki dikişleri değil, tutarlı bir hizmet görmelidir. Bir ürün için tek bir temas noktası ve talepler için net bir yol bekleyin. Ürün sahibine sizin için en çok neyin önemli olduğunu söyleyin ve yanıtın rakip talepler arasındaki ödünleşimleri içermesini bekleyin.

## Yaygın başarısızlık biçimleri

- **Bir karardan kaçınmak için çerçeve satın almak.** Bir kuruluş, öncelikler üzerindeki anlaşmazlıkları çözeceği umuduyla bir çerçeve benimser. Bunun yerine, öncelikler üzerinde kimin yetkisi olduğuna karar verin ve sonra varsa hangi çerçevenin yardımcı olduğuna bakın.
- **Bir diyagramı kopyalamak.** Roller ve toplantılar nedenleri anlaşılmadan eklenir. Bunun yerine, yalnızca adlandırılmış bir sorunu ele alan öğeleri benimseyin.
- **Katman eklemek.** Koordinatörler, program ofisleri ve komiteler çoğalırken ekipler özerklik kaybeder. Bunun yerine, eşgüdümlenecek daha az şey olsun diye bağımlılıkları kaldırın.
- **Geç entegrasyon.** Ekipler uzun bir döngünün sonunda entegre eder. Bunun yerine, tüm değişiklikleri her gün birlikte entegre edin ve test edin.
- **Tekdüze denetimler.** Her ekip riskten bağımsız olarak aynı ağır süreci izler. Bunun yerine, denetimleri riske dayandırın ve düşük riskli yolları hızlı yapın.
- **Operasyonu göz ardı etmek.** Planlama geliştiricileri ve ürün yöneticilerini içerir ama operasyon çalışanlarını içermez. Bunun yerine, operasyonu ortak planlamaya dahil edin ve hizmet verisini paylaşın.
- **Bir karmayı çerçeveye karşı yargılamak.** Eleştirmenler çerçeve olmadığını, destekçiler ise olduğunu söyler. Bunun yerine, yaklaşımınıza kendi adını verin ve betimleyin.
- **Yapıyı hiç yeniden ele almamak.** 30 kişide çizilen sınırlar 300 kişide de sürer. Bunun yerine, ekip ve rol yapısını en az yılda bir gözden geçirin.

## Olgunluk modeli

| Boyut | Başlangıç | Gelişim | Standartlaştırma | Yönetim | Eşgüdüm |
|---|---|---|---|---|---|
| Hizalanma ve öncelikler | Her ekip kendi önceliklerini belirler | Bazı ekipler bir iş listesini paylaşır ya da hizalanmak için buluşur | Ürünlerin tek sıralı bir iş listesi ve düzenli ritimle ortak planlaması vardır | Hizalanma sonuçlara göre kontrol edilir ve bağımlılıklar ölçülür | Öncelikler ekipler, müşteriler ve tedarikçiler arasında sürekli ayarlanır |
| Bağımlılıklar | Diğer ekipler için beklemeler yönetilmez | Bazı ekipler bağımlılıklarını listeler | Bağımlılıklar görünürdür ve ekipler arasında anlaşmalar vardır | Bağımlılık bekleme süreleri ölçülür ve azaltılır | Ekip sınırları bağımlılıkları kaldırmak için kanıta dayanarak yeniden şekillendirilir |
| Entegrasyon | Entegrasyon sonda yapılır | Bazı ekipler daha sık entegre eder | Ortak boru hatları herkesin değişikliklerini sık sık entegre eder ve test eder | Entegrasyon hataları ve nedenleri izlenir ve düzeltilir | Entegrasyon ortamları ve testleri ekipler arasında paylaşılır ve iyileştirilir |
| Yönetişim ve yapı | Denetimler tekdüze ve yavaştır | Bazı düşük riskli yollar vardır | Denetimler net ölçütlerle riske göre değişir | Sonuçlar ve denetim etkililiği gözden geçirilir | Yapı ve denetimler kuruluş genelinde rutin olarak gözden geçirilir ve ayarlanır |

## Kontrol listesi

- [ ] Ölçeklendirmenin çözmesi gereken sorunu bir cümleyle söyleyebiliyoruz.
- [ ] Ekiplerimiz arasındaki bağımlılıkları haritaladık ve her biri için tipik beklemeyi biliyoruz.
- [ ] Her ürünün bir sorumlu sahibi olan tek sıralı bir iş listesi var.
- [ ] Ekipler ve temel paydaşlar düzenli bir ritimle birlikte planlıyor.
- [ ] Tüm ekiplerin çıktısı en az günlük olarak birlikte derleniyor ve test ediliyor.
- [ ] Başkalarına platform ya da hizmet sağlayan ekiplerin yazılı hizmet anlaşmaları var.
- [ ] Operasyon çalışanları ekipler arası planlamaya katılıyor.
- [ ] Denetimler riske göre değişiyor ve düşük riskli yol hızlı.
- [ ] Benimsediğimiz her çerçeve önce küçük ölçekte pilot edildi.
- [ ] Herhangi bir çerçevenin hangi parçalarını izlediğimizi ve hangilerini izlemediğimizi yazdık.
- [ ] Ekiplerin ve rollerin yapısı en az yılda bir gözden geçiriliyor.

## Yapay zeka istemleri

**Amaç: yakın tarihli işin bir betimlemesinden ekipler arasındaki bağımlılıkları haritalamak.**

```text
Help me understand the dependencies between teams in a recent delivery.

Teams involved: [list the teams and what each does].
Recent delivery: [describe a recent release or project that needed work from several teams, with approximate dates for when each team finished and what it waited for].

Using only what I wrote, produce a table of dependencies (which team waited on which, for what, and for roughly how long). Highlight the three longest waits. For each, suggest one way to reduce the dependency and one question to ask the teams. Do not invent durations. Ask me clarifying questions first if the description is thin, mark assumptions, and list what you are unsure of.
```

**Amaç: ölçeklendirme seçeneklerini belirtilmiş bir soruna karşı karşılaştırmak.**

```text
Our problem: [describe in 3-5 sentences, with a recent example].
Number of teams and people: [numbers].
Our current coordination: [for example weekly meeting of team leads, a program office, none].

From the text I paste below, summarize what each of these approaches proposes: [paste short excerpts or summaries from the owners' public pages for the approaches you are considering, such as SAFe, LeSS, Disciplined Agile, or a simple scrum of scrums]. Use only the pasted text.

Then, for each approach, list which parts of our problem it addresses, what it would require of us, and what questions we should ask its owner. Do not state anything about an approach that is not in the pasted text. Ask clarifying questions first, mark assumptions, and list what you are unsure of.
```

**Amaç: birkaç ekip için ortak bir planlama oturumu planlamak.**

```text
Plan a half-day joint planning session for [number] teams working on [product or service].

Participants: [roles].
Inputs available: [for example each team's backlog, a list of dependencies, recent incident data].
Constraints: [for example people in different time zones].

Give a timed agenda that covers shared goals, dependencies, risks, and the plan for the next [period]. Include what each team brings, what the facilitator does, and a closing step that records agreed commitments and open questions. Keep it free of any particular tool. Ask clarifying questions first, and list what you are unsure of.
```

**Amaç: bir platform ekibi ile onu kullanan ekipler arasında bir anlaşma yazmak.**

```text
Help me draft a one-page working agreement between a team that provides [platform or service] and the teams that use it.

What the platform team does today: [describe].
What the using teams need: [list, or write "unknown"].
Known constraints: [support hours, security rules, tools].

Draft sections for scope, how to request changes, availability and response expectations (leave numbers as [to be agreed] and do not invent them), how incidents are handled, and how the agreement is reviewed. Mark every item that is an assumption. Ask clarifying questions first, and list what you are unsure of.
```

## Yapay zeka becerileri

- [scaled-agile-framework](../../../../skills/scaled-agile-framework/SKILL.md): SAFe'in rollerini, etkinliklerini ve düzeylerini anlamak ve hangi parçalara ihtiyacınız olduğunu yargılamak için kullanın.
- [large-scale-scrum](../../../../skills/large-scale-scrum/SKILL.md): Scrum'ı tek bir ürün üzerinde çalışan birkaç ekibe uygulamak için kullanın.
- [disciplined-agile](../../../../skills/disciplined-agile/SKILL.md): bağlamınız için uygulamaları süreç hedefine göre seçmek için kullanın.
- [scrum-of-scrums](../../../../skills/scrum-of-scrums/SKILL.md): bir çerçeve benimsemeden önce birkaç ekibi eşgüdümlemenin hafif bir yolu olarak kullanın.
- [portfolio-management](../../../../skills/portfolio-management/SKILL.md): bir dizi ürün ve girişimin nasıl seçildiğine ve finanse edildiğine karar vermek için kullanın.

## Temel kaynaklar

- **Scaled agile framework** (Wikipedia): atıflarla birlikte SAFe'in tarihçesine, yapılandırmalarına ve eleştirilerine genel bakış.
- **Introduction to LeSS** (less.works): yaratıcıların Large-Scale Scrum ve "daha azla daha fazla" fikrine dair kısa tanımı.
- **Disciplined agile delivery** (Wikipedia): araç takımının, yaşam döngülerinin ve hedeflerinin özeti.
- **Agile software development** (Wikipedia): büyük ölçekli, uzak ve dağıtık işe ilişkin bölüm ve ölçeklendirme çerçeveleri hakkındaki çelişen görüşlerin tartışması.

## Kaynakça

1. Agile software development — Wikipedia — https://en.wikipedia.org/wiki/Agile_software_development
2. Scaled agile framework — Wikipedia — https://en.wikipedia.org/wiki/Scaled_agile_framework
3. Disciplined agile delivery — Wikipedia — https://en.wikipedia.org/wiki/Disciplined_agile_delivery
4. LeSS framework introduction — Craig Larman and Bas Vodde, less.works — https://less.works/less/framework/introduction
5. Scrum (software development) — Wikipedia — https://en.wikipedia.org/wiki/Scrum_(software_development)
6. Project Management Institute — Wikipedia — https://en.wikipedia.org/wiki/Project_Management_Institute
7. Lean software development — Wikipedia — https://en.wikipedia.org/wiki/Lean_software_development
