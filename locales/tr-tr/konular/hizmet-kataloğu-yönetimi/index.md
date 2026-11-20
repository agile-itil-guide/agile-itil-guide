# Hizmet Kataloğu Yönetimi

**Hizmet kataloğu (ITIL bunu "service catalogue" diye yazar), bir kuruluşun sunduklarının, her hizmet için bir sahip ve sade bir açıklamayla birlikte derlenmiş bir listesidir; değeri, kullanıcıların onu yararlı bulmasına ve sahiplerin onu doğru tutmasına bağlıdır.**

## Bu neden önemli

Bir kullanıcıya BT'nin ne sunduğunu sorarsanız çoğu zaman muğlak bir yanıt alırsınız. BT ekibine sorarsanız sistemlerin bir listesini alırsınız. İki liste nadiren örtüşür ve aradaki fark yanlış anlamalara yol açar: kullanıcılar var olmayan şeyleri ister, ekipler kimsenin kullanmadığı hizmetleri destekler ve kimin neden sorumlu olduğunu kimse söyleyemez. Hizmet kataloğu, neyin sunulduğunu ve arkasında kimin durduğunu tek bir yerde ve sade terimlerle belirterek bu farkı kapatır.

Çevik ekipler için katalog aynı zamanda sahipliği görünür kılmanın bir yoludur. Bir hizmeti kuran ve işleten bir ekip, "sunduğumuz şey bu, soracağınız kişi bu, bekleyebileceğiniz şey bu" diyebilmelidir. Bu olmadan talepler yanlış yere ulaşır, olaylar ekipler arasında gidip gelir ve yeni personel yardım bulamaz.

[Hizmet kataloglarına ilişkin Wikipedia maddesi](https://en.wikipedia.org/wiki/Service_catalog), hizmet kataloğunu bir kuruluş içindeki iş ve bilgi teknolojisi hizmetlerinin düzenlenmiş ve derlenmiş bir koleksiyonu olarak, listelenen her hizmet için konu uzmanlarını belirleyen bir bilgi yönetimi aracı olarak tanımlar. ITIL'in Service Design cildinin, ITIL sürümünü belirtmeden, bir BT hizmet kataloğunu yalnızca BT hizmetlerinin kapsamlı bir listesi ve hizmet portföyünün müşterilere yayımlanan tek kısmı olarak tanımladığını not eder. Bu konu, bu betimleme ile rehberin diğer konularına dayanır ve kataloğu pratik ve hafif tutar.

## Temel kavramlar

### Bir katalogda neler vardır

Wikipedia'ya göre, bir hizmet kataloğundaki her kayıt genellikle adlandırılmış bir sahip, bir açıklama, bir kategori, ilgili talep türleri, destekleyici hizmetler, hak ediş (entitlement) bilgileri, maliyetler, hizmetin nasıl talep edildiği ve karşılandığı ve yükseltme (escalation) iletişim bilgilerini içerir. Yaygın kategoriler arasında BT, operasyonlar ve karşılama yer alır. Bunların hepsine her hizmet için ihtiyacınız yoktur. İyi bir katalog, kullanıcıların ve destek personelinin gerçekten ihtiyaç duyduğu birkaç alanla başlar.

| Alan | Neden yardımcı olur | Kim kullanır |
|---|---|---|
| **Sade sözcüklerle ad ve açıklama** | Kullanıcılar sunulanı tanır | Kullanıcılar, hizmet masası |
| **Sahip** | Hizmetin hesabını biri verir | Herkes |
| **Kimler kullanabilir (hak ediş)** | Boşa giden talepleri önler | Kullanıcılar, hizmet masası |
| **Nasıl talep edilir ya da yardım alınır** | Kullanıcıları doğru yere götürür | Kullanıcılar, hizmet masası |
| **Neye bağlı olduğu (destekleyici hizmetler)** | Başka nelerin çalışması gerektiğini gösterir | Operasyonlar, teslimat ekipleri |
| **Ücretlendiriliyorsa maliyet** | Kararları ve bütçeleri destekler | Müşteriler, finans |
| **Hizmet seviyesi ya da beklenti** | Beklentileri belirler | Kullanıcılar, müşteriler (bkz. Konu 3.7 — Hizmet Seviyesi Yönetimi) |
| **Yükseltme iletişim bilgisi** | Sorunlar sırasında yardımı hızlandırır | Hizmet masası, operasyonlar |

### Katalog ve portföy

Wikipedia maddesi BT hizmet kataloğunu, daha geniş kurumsal kataloğun bir alt kümesi olarak konumlandırır. ITIL sözcük dağarcığında hizmet portföyü, geliştirilmekte olanlar ve emekliye ayrılmakta olanlar dahil hizmetlerin tamamıdır ve katalog, müşterilere yayımlanan kısımdır. Burada okunan kaynaklar portföyü ayrıntılı olarak tanımlamaz: hizmet portföyü yönetimi maddesi BT portföy yönetimine yönlendirir ve bu madde yalnızca ITIL v3'ün, işlevsel olarak BT portföy yönetimine eşdeğer görünen bir hizmet portföyü yönetimi uygulaması gerektirdiğini söyler. Portföy fikrini şöyle ele alın: katalog şu anda sunduğunuz şeydir, portföy ise aynı zamanda inşa ettiğiniz ve emekliye ayırdığınız şeylerdir (portföy seçimleri için bkz. Konu 5.7 — Yönetişim, Risk ve Uyum).

### Kurumsal ve BT katalogları

Kurumsal hizmet kataloğu, insan kaynakları, tesis yönetimi ve BT gibi birkaç işlevin hizmetlerini kapsar. BT hizmet kataloğu bunun bir alt kümesidir. Madde, bir kataloğun faydalarını sayar: dağıtık kuruluşlarda hizmetleri merkezileştirmek, hizmet boşluklarını ve yinelenmeleri belirlemek, kaynak tahsisini izlemek ve hizmet talebini, arzını, onay sürelerini, teslim sürelerini ve mali durumu ölçmek. Bulut hizmetleri için self provizyonu (self-provisioning) ve kapasite planlamasına ve satın alma tahminlerine yardımcı olan standartlaştırılmış tanımları sayar. Bunlar, maddenin kendi atıf yaptığı kaynaklara dayanan iddialarıdır.

### İş görünümü ve teknik görünüm

Birçok kuruluş, müşterilerin gördüğü ile sağlayıcının dahili olarak ihtiyaç duyduğunu birbirinden ayırır. Burada okunan kaynaklar bu ayrımı yapmaz, bu yüzden bunu yaygın bir uygulama olarak ele alın. **Müşteriye dönük görünüm** hizmetleri kullanıcının terimleriyle listeler ("E-posta ve takvim"). **Teknik görünüm** bunların arkasındaki bileşenleri ve ekipleri listeler ("Posta sunucuları, istenmeyen posta filtresi, dizin hizmeti"). Müşteri görünümü kullanıcıların seçim yapmasına yardımcı olur. Teknik görünüm operasyonların bağımlılıkları anlamasına yardımcı olur (bkz. Konu 4.4 — Yapılandırma Yönetimi). İkisini bağlantılı ama ayrı tutun, böylece kullanıcılar bileşen adlarıyla karşılaşmaz.

### Bir bilgi aracı olarak katalog

Wikipedia maddesi, kataloğun her hizmet için konu uzmanlarını belirlediğini vurgular. Bu onu, kimin neyi bildiğinin bir haritası yapar. Güncel tutulan bir katalog, hizmet masasının iletişimleri yönlendirmesine, yeni personelin yardım bulmasına ve olay müdahale edenlerin doğru kişiye ulaşmasına yardımcı olur (bkz. Konu 3.9 — Bilgi Yönetimi).

### Katalog ve talepler

Katalog genellikle kullanıcıların her hizmet için yapabileceği talepleri içerir, örneğin "erişim talep et" ya da "arıza bildir". Bir talep modeli her birinin nasıl karşılandığını betimler (bkz. Konu 3.6 — Hizmet Talebi Yönetimi). Her hizmetin talebe, her talebin de katalog kaydına ihtiyacı yoktur, ancak sık talepler kolay bulunmalıdır.

### Doğru tutmak

Kimse sahip çıkmazsa bir katalog hızla bayatlar. Hizmetler değişir, ekipler yeniden örgütlenir ve açıklamalar gerçeklikten uzaklaşır. En yararlı disiplin bir gözden geçirme döngüsüdür: her sahip kayıtlarını bir takvime göre doğrular ve kullanılmayan hizmetler emekliye ayrılır. Wikipedia maddesi eleştirileri ya da sınırları tartışmaz, ancak pratik deneyim tutarlıdır: yanlış bir katalog hiç katalog olmamasından daha kötüdür, çünkü insanları yanlış yere güvenle gönderir.

### Kataloglar ve çevik ekipler

Çevik ekipler çoğunlukla bürokrasi bekledikleri için ağır kataloglara direnir. Hafif bir katalog çevik çalışma biçimleriyle uyumludur. Hizmet başına birkaç alanla, sahiplerin kendileri tarafından bakımı yapılan ortak bir belge ya da sayfa olabilir. Sınama kullanımdır: kullanıcılar ve masa ona gerçekten başvuruyor mu?

## İyi uygulamalar

1. **Hizmetleri kullanıcıların sözcükleriyle listeleyin.** Kullanıcılara ve hizmet masasına her şeye ne diyeceklerini sorarak başlayın. Hizmetleri teknolojiye göre ("Konferans platformu") değil, kullanıcıların yaptığına göre ("Bir görüntülü toplantıya katılın") adlandırın.
2. **Her hizmete adlandırılmış bir sahip verin.** Her hizmetin hesabını bir kişi vermelidir. Bir hizmetin birkaç parçası varsa, bütünün sahibini adlandırın ve katkıda bulunanları listeleyin.
3. **Küçük başlayın.** Kullanıcıların en sık sorduğu 10 ila 20 hizmetle başlayın. Neyin yararlı olduğunu öğrendikçe daha fazlasını ekleyin. Kısa ve doğru bir liste, uzun ve bayat bir listeden iyidir.
4. **Yalnızca insanların kullandığını ekleyin.** Her alan için kimin ne amaçla kullandığını sorun. Kimsenin kullanmadığı alanları kaldırın. Bir alanı yalnızca birinin ihtiyacı olduğunda ekleyin.
5. **Taleplere ve yardıma bağlayın.** Her hizmet için bir şeyin nasıl isteneceğini, arızanın nasıl bildirileceğini ve yardımın nerede bulunacağını gösterin. Bilgi tabanına bağlayın (bkz. Konu 3.9 — Bilgi Yönetimi).
6. **Hizmet beklentilerini gösterin.** Kullanıcıların neler bekleyebileceğini, örneğin destek saatlerini ve tipik yanıtı, sade terimlerle belirtin. Varsa resmî anlaşmaya bağlayın.
7. **Bağımlılıkları kaydedin.** Her hizmet için dayandığı ana hizmetleri ve tedarikçileri not edin. Bu, olay müdahalesine ve değişiklik planlamasına yardımcı olur.
8. **Müşteri görünümünü teknik görünümden ayırın.** Kullanıcıya dönük açıklamaları jargondan uzak tutun. Varsa teknik kayıtlara bağlayın.
9. **Bir takvime göre gözden geçirin.** Her sahipten kayıtlarını yılda en az iki kez doğrulamasını isteyin ve kimsenin kullanmadığı hizmetleri emekliye ayırın. Her kayıtta son gözden geçirme tarihini gösterin.
10. **Bulmayı ve kullanmayı kolaylaştırın.** Kataloğu kullanıcıların zaten baktığı yere, örneğin intranete ya da portala koyun. Aramayı gerçek sorgularla sınayın.
11. **Boşlukları ve örtüşmeleri bulmak için kataloğu kullanın.** Sahibi olmayan hizmetlere, birbirini yineleyen hizmetlere ve eşleşen hizmeti olmayan taleplere bakın. Bulguları planlamaya taşıyın (bkz. Konu 5.5 — Ürün ve Hizmet Sahipliği).
12. **Katalog değişikliklerini hizmet değişiklikleri olarak ele alın.** Bir hizmeti eklediğinizde, değiştirdiğinizde ya da emekliye ayırdığınızda, bir sürüm gibi masaya ve etkilenen kullanıcılara duyurun.

## Ekibinizle tartışılacak sorular

**Yeni bir meslektaş neler sunduğumuzu sorsa ne yanıt verirdik ve hepimiz aynı şeyi söyler miydik?**

Her kişiden iki dakikada hizmetleri listelemesini isteyin, sonra karşılaştırın. Farklar sınırların ne kadar bulanık olduğunu gösterir. Kolaylaştırıcı hangi kalemleri kullanıcıların tanımayacağını sorabilir. Birleşik listeyi taslak katalog olarak kullanın ve anlaşmazlık olan kalemleri işaretleyin.

**Hangi hizmetlerin net bir sahibi yok?**

Listeyi gözden geçirin ve hizmetin hesabını kimin verdiğini kimsenin söyleyemediği hizmetleri işaretleyin. Sahipsiz hizmetler çoğunlukla olaylarda ve taleplerde en uzun gecikmelere yol açar. Bir kişinin sahipliği üstlenmesini neyin engellediğini sorun: zaman, yetki ya da belirsiz sınırlar. Her biri için bir sahip ya da emekliye ayırma kararı üzerinde anlaşın.

**Kullanıcılar listelemediğimiz neleri istiyor ve kimsenin istemediği neleri listeliyoruz?**

Talep verilerini listeyle karşılaştırın. Eşleşen hizmeti olmayan talepler boşlukları, talebi olmayan listelenmiş hizmetler ise emekliye ayırma adaylarını ortaya çıkarır. Temkinli olun: bazı hizmetler sessizce kullanılır. Kaldırmadan önce kullanıcılara sorun. İncelenecek bir boşluk ve bir aday seçin.

**Bir kullanıcının bizi aramadan doğru hizmeti seçebilmesi için neyi görmesi gerekir?**

Dosya paylaşmak için hangi aracın kullanılacağı gibi yaygın bir seçimi ele alın. Hangi bilginin yardımcı olacağını sorun: kısa bir açıklama, kimin için olduğu, bir karşılaştırma. Bir paragraflık bir kayıt taslağı hazırlayın ve iki kullanıcıyla sınayın. Amaç, net olarak aramaları azaltan bir katalogdur.

**Bir hizmet değiştiğinde ve katalog güncelliğini yitirdiğinde bunu nasıl öğreniriz?**

Son gözden geçirmenin ne zaman ve kim tarafından yapıldığını sorun. Yeniden yapılanma ya da büyük bir sürüm gibi tetikleyicileri ve düzenli bir döngüyü tartışın. Her kayıtta görünür bir "son gözden geçirme" tarihi yardımcı olur. İlk gözden geçirme tarihi ve sorumlusu konusunda anlaşın.

**Katalogda olmayan neye bağımlıyız?**

Hizmetlerinizin arkasındaki platformları ve tedarikçileri listeleyin. Hangilerinin listelendiğini ve sahiplerinin kim olduğunu sorun. Sahibi olmayan bağımlılıklar risktir. Teknik görünüme eklenecek birini seçin.

## Uygulamada: çevik bir ITIL örneği

Bölgesel bir belediye meclisinin BT departmanında, 2.500 meclis çalışanına ve kamuya dönük birkaç hizmete hizmet veren 120 personel var. Personel yardım için kime başvuracağını bilmediğinden şikâyet ediyor ve hizmet masası zamanının büyük bölümünü çağrıları yönlendirmeye harcıyor. Meclis bir zamanlar 300 kayıtlı bir hizmet kataloğu kurmuştu, ancak nadiren kullanılıyor ve büyük ölçüde güncelliğini yitirmiş durumda.

Hizmet teslimatı başkanı küçük bir başlangıçla yeniden başlamaya karar veriyor. Hizmet masasından insanların kendisiyle iletişime geçtiği en yaygın 30 nedeni istiyor ve bunları kullanıcıların sözcükleriyle 15 hizmet altında grupluyor: "E-posta ve takvim", "Dosyalar ve paylaşım", "Dizüstü bilgisayarlar ve cihazlar", "Meclis web sitesi", "Finans sistemi" ve benzerleri. Her biri için adlandırılmış bir sahip dört şey yazıyor: iki cümlelik bir açıklama, kimin için olduğu, nasıl yardım alınacağı ve ne bekleneceği. Bağımlılıklar operasyonlar için ayrı bir teknik listede kaydediliyor. Katalog, meclisin intranetinde tek bir web sayfası ve her kayıt, sahibi tarafından en son ne zaman doğrulandığını gösteriyor.

Üç ay sonra, kime sorulacağıyla ilgili masaya gelen çağrılar azalıyor ve sahipler boşlukları fark ediyor: toplantı odası rezervasyon sisteminin sahibi yoktu ve iki hizmet örtüşüyordu. Bunlar atanıyor ve birleştiriliyor. Sorunlar sürüyor. Üç sahip kayıtlarını doğrulamadı ve bazı personel alışkanlıkla hâlâ masayı arıyor. Hizmet teslimatı başkanı bir hatırlatma döngüsü belirliyor ve masanın, arayanların talebini ele alırken onları kataloğa yönlendirmesini sağlıyor. Ayrıca bazı kayıtların teknik bir dille yazıldığını fark ediyor ve bir iletişim görevlisinden bunları gözden geçirmesini istiyor.

## Dört bakış açısı

### Ürün ve teslimat ekipleri

Teslimat ekipleri, kurup işlettikleri hizmetlerin sahibi olarak adlandırılmalı ve kayıtlarını güncel tutmalıdır. Bir hizmeti başlattığınızda ya da emekliye ayırdığınızda kataloğu güncelleyin ve hizmet masasına söyleyin. Bir bağımlılık hakkında kiminle konuşacağınızı bulmak için kataloğu kullanın.

### Hizmet ve operasyon ekipleri

Operasyon ve hizmet masası en yoğun kullanıcılardır. Sahiplere kayıtlarda neyin yanlış ya da eksik olduğunu söyleyin ve kataloğu yönlendirme ve yükseltme için kullanın. Teknik görünümü müşteri görünümüne bağlı tutun, böylece olay müdahale edenler neyin neye bağlı olduğunu görebilir.

### Liderlik ve yönetişim

Liderler, kuruluşun neler sunduğunu, nelerin örtüştüğünü ve nelerin sahipsiz kaldığını görmek için kataloğu kullanabilir. Boşlukların ve yinelenmelerin ele alınmasını ve sahiplerin adlandırılmasını isteyin. Her hizmet için her alanı zorunlu tutmayın; kararları destekleyeni isteyin.

### Müşteriler ve kullanıcılar

Müşteriler ve kullanıcılar neleri isteyebileceklerine ve ne bekleyeceklerine dair net bir görünüm elde eder. Doğru hizmeti bulmak için kataloğu kullanın ve bir kayıt yanlış ya da belirsiz olduğunda sahiplere söyleyin. İhtiyacınız olanı bulamıyorsanız bunu söyleyin, çünkü bu bir boşluğun kanıtıdır.

## Yaygın başarısızlık biçimleri

- **Çok büyük, çok erken.** Yüzlerce kayıt oluşturulur ve bakımı yapılmaz. Bunun yerine en çok kullanılan hizmetlerle başlayın ve büyütün.
- **Sağlayıcı diliyle yazılmış.** Kullanıcılar ihtiyaç duyduklarını bulamaz. Bunun yerine hizmetleri kullanıcıların yaptığına göre adlandırın ve kullanıcılarla sınayın.
- **Sahip yok.** Kayıtları kimse doğru tutmaz. Bunun yerine her kayıt için bir sahip adlandırın ve gözden geçirme tarihlerini gösterin.
- **Kimsenin kullanmadığı bir katalog.** Kullanıcıların uğramadığı bir sitede durur. Bunun yerine insanların zaten baktığı yere koyun ve masanın ona yönlendirmesini sağlayın.
- **Müşteri ve teknik görünümleri karıştırmak.** Kullanıcılar bileşen adlarıyla karşılaşır. Bunun yerine net bir müşteri görünümü tutun ve operasyonlar için teknik bir görünüme bağlayın.
- **Emekliye ayırma yok.** Ölü hizmetler listelenmeye devam eder. Bunun yerine kullanımı gözden geçirin ve kimsenin ihtiyaç duymadığını emekliye ayırın.
- **Bir kerelik proje olarak görmek.** Katalog yayımlandıktan sonra bayatlar. Bunun yerine bir gözden geçirme döngüsü belirleyin ve onu değişikliklerin parçası yapın.
- **Çok fazla zorunlu alan.** Sahipler şablonu tatmin etmek için alanları doldurur. Bunun yerine yalnızca birinin kullandığını zorunlu kılın.

## Olgunluk modeli

| Boyut | Başlangıç | Gelişim | Standartlaştırma | Yönetim | Eşgüdüm |
|---|---|---|---|---|---|
| Kapsam ve netlik | Hizmetler gayriresmî olarak bilinir | Bazı hizmetlerin bir listesi vardır | Ana hizmetlerin kullanıcıların sözcükleriyle ve sahipleriyle bir kataloğu vardır | Kullanım ve boşluklar ölçülür ve katalog ayarlanır | Katalog işlevleri ve ortakları kapsar ve kullanıcılarla şekillendirilir |
| Sahiplik ve güncellik | Listenin sahibi yoktur | Bazı sahipler kayıtları ara sıra doğrular | Her kaydın bir sahibi ve bir gözden geçirme tarihi vardır | Gecikmiş gözden geçirmeler izlenir ve çözülür | Sahiplik ve gözden geçirme kuruluş genelinde rutindir |
| Taleplere ve yardıma bağlantı | Talepler e-posta ya da telefonla gider | Bazı kayıtlar formlara ya da yardıma bağlanır | Kayıtlar taleplere, bilgiye ve destek yollarına bağlanır | Tıklama ve yönlendirmeyle çözüm (deflection) ölçülür | Talepler, bilgi ve destek işlevler arasında bütünleşiktir |
| Bağımlılıklar ve kararlar | Bağımlılıklar kulaktan kulağa bilgidir | Bazı bağımlılıklar listelenir | Bağımlılıklar kaydedilir ve olay ve değişiklik işlerinde kullanılır | Bağımlılık verileri planlamayı ve risk gözden geçirmesini destekler | Bağımlılıklar tedarikçilerle paylaşılır ve birlikte planlamada kullanılır |

## Kontrol listesi

- [ ] En çok kullanılanlardan başlayarak kullanıcıların sözcükleriyle bir hizmet listemiz var.
- [ ] Her hizmetin adlandırılmış bir sahibi var.
- [ ] Her kayıt kimin için olduğunu, nasıl yardım alınacağını ve ne bekleneceğini söylüyor.
- [ ] Katalog, kullanıcıların ve hizmet masasının zaten baktığı yerde.
- [ ] Kayıtlar en son doğrulandıkları tarihi gösteriyor.
- [ ] Sahipler kayıtlarını yılda en az iki kez gözden geçiriyor.
- [ ] Ana bağımlılıklar bir teknik görünümde kayıtlı.
- [ ] Kullanılmayan hizmetler emekliye ayırma açısından gözden geçiriliyor.
- [ ] Bir hizmeti eklemek, değiştirmek ya da emekliye ayırmak masaya ve kullanıcılara duyuruluyor.
- [ ] Kataloğu gerçek kullanıcı sorgularıyla sınadık.

## Yapay zeka istemleri

**Amaç: iletişim verilerini kullanıcıların sözcükleriyle hazırlanmış bir hizmet listesi taslağına dönüştürmek.**

```text
Below are the reasons people contacted our service desk in the last [period]: [paste short, anonymized descriptions or category counts].

Group them into 10 to 20 candidate services, each named in plain words that a non-technical user would recognize, such as "Email and calendar." For each, give a two-sentence description based only on the contacts, the contacts that fit under it, and a question to ask its owner. List contacts that do not fit. Do not invent services or systems that do not appear in the data. Ask clarifying questions first if the data is thin, and list what you are unsure of.
```

**Amaç: net bir katalog kaydı yazmak.**

```text
Help me write a service catalog entry for [service].

What it does, in my own words: [describe].
Who may use it: [describe].
How users get help or make requests: [describe].
Support hours and what users can expect: [describe, or write "unknown"].
Main things it depends on: [list].
Owner: [role].

Write a short entry for users (no jargon, under 80 words) and a separate technical note for operations. Mark anything you added as an assumption. Do not invent service levels or contacts. Ask clarifying questions first, and list what you are unsure of.
```

**Amaç: bir kataloğu boşluklar, örtüşmeler ve sahipsiz kayıtlar açısından gözden geçirmek.**

```text
Here is our service catalog (names, owners, descriptions, and last review dates): [paste].
Here is data on what users request or report: [paste counts by topic, or write "none"].

Using only this text, list: services with no owner or an overdue review; pairs of services that seem to overlap; request topics with no matching service; and services with no requests in the data. For each, suggest a question for the owner or the desk rather than a conclusion. Do not guess about services not listed. List what you are unsure of.
```

**Amaç: sahiplerle bir katalog gözden geçirmesi planlamak.**

```text
Plan a 60-minute review of our service catalog with [number] service owners.

State of the catalog: [describe, such as number of entries and how old they are].
Problems we know of: [list].

Give a timed agenda that has each owner confirm or correct their entries, look at overlaps and gaps, decide what to retire, and agree a review date. Include a one-page template for owners to prepare. Keep it free of any particular tool. Ask clarifying questions first if information is missing, mark assumptions, and list what you are unsure of.
```

## Yapay zeka becerileri

- [service-catalog](../../../../skills/service-catalog/SKILL.md): kayıtları taslaklamak ve bir hizmet kataloğunu yapılandırmak için kullanın.
- [stakeholder-analysis](../../../../skills/stakeholder-analysis/SKILL.md): her hizmeti kimlerin kullandığını ve neye ihtiyaç duyduklarını anlamak için kullanın.
- [demand-analysis](../../../../skills/demand-analysis/SKILL.md): hangi taleplerin ve hizmetlerin en çok kullanıldığını bulmak için kullanın.
- [raci-matrix](../../../../skills/raci-matrix/SKILL.md): her hizmetin kimin sahipliğinde olduğunu, kimin desteklediğini ve kime danışıldığını kaydetmek için kullanın.
- [product-roadmap](../../../../skills/product-roadmap/SKILL.md): hizmetlerin zaman içinde nasıl ekleneceğini, değiştirileceğini ya da emekliye ayrılacağını planlamak için kullanın.

## Temel kaynaklar

- **Service catalog** (Wikipedia): içeriğin, faydaların ve bir BT hizmet kataloğunun ITIL tanımının kısa bir betimlemesi.
- **IT portfolio management** (Wikipedia): ITIL v3 hizmet portföyü yönetiminin işlevsel olarak eşdeğer göründüğü notu dahil portföy kavramları üzerine arka plan.
- **ITIL** (Wikipedia): ITIL sürümleri ve katalog ile portföy fikirlerinin nereden geldiği üzerine bağlam.
- **Knowledge management** (Wikipedia): katalogların bilgi aracı olarak nasıl işlev gördüğü üzerine arka plan.

## Kaynakça

1. Service catalog — Wikipedia — https://en.wikipedia.org/wiki/Service_catalog
2. IT portfolio management — Wikipedia — https://en.wikipedia.org/wiki/IT_portfolio_management
3. ITIL — Wikipedia — https://en.wikipedia.org/wiki/ITIL
4. IT service management — Wikipedia — https://en.wikipedia.org/wiki/IT_service_management
5. Knowledge management — Wikipedia — https://en.wikipedia.org/wiki/Knowledge_management
6. Enterprise service management — Wikipedia — https://en.wikipedia.org/wiki/Enterprise_service_management
7. Help desk — Wikipedia — https://en.wikipedia.org/wiki/Help_desk
8. Service-level agreement — Wikipedia — https://en.wikipedia.org/wiki/Service-level_agreement
