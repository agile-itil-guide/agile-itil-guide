# Hizmet Seviyesi Yönetimi

**Hizmet seviyesi yönetimi, kullanıcıların ihtiyaç duyduklarını bir ekibin ölçebileceği ve savunabileceği hedeflere dönüştürür; çevik ekipler için en yararlı biçim, başarısızlık için açık bir bütçeyle birlikte kullanıcıya odaklı az sayıda hedeftir.**

## Bu neden önemli

Her hizmetin, ölçülmüş olsun ya da olmasın, bir kalite seviyesi vardır. Bu seviye belirtilmezse kullanıcılar bir seviye varsayar, ekip başka bir seviye varsayar ve aradaki fark bir kesinti sırasında ortaya çıkar. Hizmet seviyesi yönetimi, seviyeyi belirtme, ölçme ve sonuçlara göre harekete geçme uygulamasıdır. Bir ekibe yön bulmak için bir dayanak, müşterilere de güvenebilecekleri bir şey verir.

Çevik ekipler çoğunlukla hizmet seviyelerine direnir, çünkü onları sözleşmelerle ve cezalarla ilişkilendirir. Oysa haftalık sürüm çıkaran çevik bir ekip, farkında olsun ya da olmasın, erişilebilirlikte ne kadar risk alacağına dair bir karar vermektedir. Net bir hedef bu kararı açık kılar. Google'ın *Site Reliability Engineering* kitabı, hizmet seviyesi hedefleri üzerine bölümünde bunun hızlı hareket eden ekiplere uygun bir yolla nasıl yapılacağını anlatır: kullanıcılar için önemli olan birkaç gösterge seçin, hedefler belirleyin ve ne zaman sürüm çıkarılacağına karar vermek için kusursuz ile kabul edilebilir arasındaki boşluğu, yani hata bütçesini (error budget) kullanın.

Bu konu, söz konusu bölümü anlaşmaların tanımları için [hizmet seviyesi anlaşmalarına ilişkin Wikipedia maddesi](https://en.wikipedia.org/wiki/Service-level_agreement) ile ve bu rehberin çerçeve sahibinin metnine karşı doğrulayamadığı, yaygın olarak kullanılan ITIL sözcük dağarcığıyla birleştirir. SRE bölümü tek bir kuruluşun uygulamasını yansıtır ve belirli bir yaklaşımı savunur; onu evrensel bir kural olarak değil, iyi açıklanmış bir seçenek olarak okuyun.

## Temel kavramlar

### Gösterge, hedef, anlaşma

SRE bölümü, çoğunlukla birbirine karıştırılan üç terimi ayırır:

| Terim | Anlamı | Örnek |
|---|---|---|
| **Hizmet seviyesi göstergesi (SLI)** | Hizmet seviyesinin bir yönünün dikkatle tanımlanmış nicel ölçüsü | Doğru biçimlendirilmiş isteklerden başarılı olanların oranı |
| **Hizmet seviyesi hedefi (SLO)** | Bir SLI için hedef değer ya da aralık | İsteklerin en az %99,9'u bir ay boyunca başarılıdır |
| **Hizmet seviyesi anlaşması (SLA)** | Hedeflerin karşılanmasının ya da karşılanmamasının, çoğunlukla mali, sonuçlarını içeren, kullanıcılarla yapılmış açık ya da örtük bir sözleşme | Erişilebilirlik belirtilen seviyenin altına düşerse geri ödeme |

Bölümün bir SLA'yı bir SLO'dan ayırma sınaması, açık bir sonuç olup olmadığıdır. Yoksa bu bir SLO'dur. Tablodaki örnek sayılar birer örnektir, öneri değildir.

Wikipedia maddesi SLA'yı, bir sağlayıcı ile bir müşteri arasında, genellikle bağlayıcı bir sözleşme olarak, hizmetin kalite, erişilebilirlik ve sorumluluklar gibi yönlerini tanımlayan bir anlaşma olarak betimler. Tipik içeriği sayar: hizmetin tanımı, performans seviyeleri, izleme ve raporlama, sorunların nasıl bildirileceği, yanıt ve çözüm süreleri ve performans gösterilmemesinin sonuçları. Arızalar arası ortalama süre, ortalama onarım süresi, çalışma süresi (uptime), ilk çağrıda çözüm ve geri dönüş süresi gibi yaygın ölçütleri adlandırır. Büyük kuruluşların çoğunlukla birimler arasında iç SLA'lar kullandığını belirtir. Türleri kapsama göre betimler: müşteri tabanlı, hizmet tabanlı ve çok düzeyli.

### Gösterge seçimi

SRE bölümü, izleyebileceğiniz her ölçüyü değil, kullanıcıların önemsediğini yansıtan birkaç gösterge seçmeyi önerir. Kullanıcıya dönük sistemler genellikle erişilebilirliğe, gecikmeye (latency) ve işlem hacmine (throughput) odaklanır. Depolama sistemleri dayanıklılığı ekler ve tüm sistemler doğruluğu izlemelidir. İstemci tarafı ölçümün, sunucu tarafı ölçülerin kaçırdığı sorunları yakalayabileceğini öne sürer. Hizmet ekipleri için pratik sonuç: kullanıcının deneyimiyle başlayın, örneğin "Randevu alabiliyorum ve birkaç saniye sürüyor", sonra buna yaklaşan bir gösterge bulun.

### Ortalamalar acıyı gizler

Bölüm ortalamalara dayanmaya karşı çıkar: "Çoğu ölçü ortalamalardan çok dağılımlar olarak düşünülmelidir." 99. ya da 99,9. gibi yüksek yüzdelikler (percentile) makul en kötü durumları gösterirken medyan tipik durumu gösterir. Ortalamalar yavaş isteklerden oluşan uzun bir kuyruğu gizleyebilir. Ölçünüz bir ortalamaysa, birkaç kullanıcı çok kötü zaman geçiriyor olabilir ve sayı kımıldamayabilir.

### Hedef seçimi

Bölümün hedefler konusundaki yönlendirmesi doğrudan ve yararlıdır:

- **Kullanıcılardan başlayın.** "Ölçebildiğinizi değil, kullanıcılarınızın neyi önemsediğini düşünerek (ya da öğrenerek!) başlayın."
- **Mevcut performansa demir atmayın.** Hedefi şu anda başardığınıza göre seçmek kahramanca çabayı kilitleyebilir.
- **Basit tutun.** Karmaşık toplulaştırmalar değişiklikleri gizler ve üzerinde akıl yürütmeyi zorlaştırır.
- **Mutlaklardan kaçının.** "Her zaman" erişilebilir olma sözleri gerçekçi değildir.
- **Mümkün olduğunca az SLO'nuz olsun.** Her biri bir öncelik tartışmasında savunmaya değer olmalıdır.
- **Kusursuzluk bekleyebilir.** Daha sonra gevşetilmesi gereken bir hedeften çok, sıkılaştıracağınız gevşek bir hedefle başlamak daha iyidir.

### Hata bütçeleri

Bölüm, %100 uyum şartının gerçekçi olmadığını ve yeniliği yavaşlattığını söyler. Bunun yerine ekipler bir **hata bütçesine** izin verir: bir SLO'nun günlük, haftalık ya da aylık izlenen, kaçırılabileceği oran. Bütçe sürümlerle ilgili kararları bilgilendirir. Bol bütçe kaldığında ekip değişiklikte daha fazla risk alabilir; bütçe neredeyse tükendiğinde ekip değişikliği yavaşlatır ve güvenilirliğe yatırım yapar. Bu, çevik ekiplere ve operasyona hız ile kararlılığı otoriteyle tartışmak yerine paylaşılan, sayısal bir yolla tartışma olanağı verir.

### Beklentileri belirleme

Bölüm, bir SLO yayımlamanın kullanıcı beklentilerini belirlediğini not eder. Ekipler daha sıkı bir iç hedefle bir güvenlik payı tutabilir. Ayrıca aşırı başarıya karşı da uyarır, çünkü kullanıcılar gözlemledikleri performansa bağımlı hale gelir. Bir hizmet belirtilen hedefinden çok daha iyiyse kullanıcılar bunun üzerine bina eder ve hedef artık ekibi korumaz.

### Kontrol döngüsü

Bölüm SLI'ları ve SLO'ları bir kontrol döngüsünün temeli olarak betimler: SLI'ları izleyin, SLO'larla karşılaştırın, harekete geçmek gerekip gerekmediğine karar verin, hedefi hangi eylemin karşılayacağını belirleyin ve uygulayın. SLO olmadan bir ekip harekete geçip geçmeyeceğini ya da ne zaman geçeceğini bilemez (bkz. Konu 3.10 — İzleme ve Etkinlik Yönetimi).

### İç ve dış anlaşmalar

Bir SLA bir sağlayıcı ile bir müşteri arasındadır. Bir sağlayıcının içinde ekipler birbirine ve tedarikçilere bağımlıdır. Wikipedia maddesi SLA'ların işletim düzeyi anlaşmalarıyla (OLA) desteklenebileceğini söyler ama bunları açıklamaz. ITIL sözcük dağarcığında OLA, bir SLA'yı destekleyen iç ekipler arasındaki bir anlaşmadır ve destekleyici sözleşme (underpinning contract) harici bir tedarikçiyle olan karşılığıdır. Burada okunan kaynaklar bu tanımları doğrulamaz, bu yüzden ITIL yayınlarına karşı denetleyin. Pratik nokta, bir müşteriye verilen sözün arkasındaki sözler kadar iyi olduğudur (bkz. Konu 3.14 — Tedarikçi Yönetimi).

### Kanban'da hizmet seviyesi beklentileri

Kanban'da **hizmet seviyesi beklentisi (service level expectation)**, geçmiş çevrim sürelerine dayanarak bir iş öğesinin ne kadar sürmesi gerektiğine ilişkin bir tahmindir (bkz. Konu 1.5 — Kanban). Bir anlaşma değildir, ancak iş öğeleri için benzer bir amaca hizmet eder ve talepler ile olaylar için hedefleri besleyebilir.

## İyi uygulamalar

1. **Kullanıcıların ihtiyacıyla başlayın.** Kullanıcılara ve müşterilere neyin en çok önemli olduğunu ve başarısız olduğunda neyin acıttığını sorun. Bir ölçü seçmeden önce bunu onların sözcükleriyle yazın.
2. **Birkaç gösterge seçin.** Her hizmet için başarı oranı ve hız gibi kullanıcı deneyimini yansıtan iki ila dört gösterge seçin. Bunları kullanana kadar daha fazlasını eklemeye direnin.
3. **Hız için yüzdelikleri kullanın.** Kötü deneyim yaşayan kullanıcıların görünür olması için yalnızca ortalamayı değil, dağılımın yavaş ucunu da ölçün.
4. **Önce gevşek hedefler koyun, sonra sıkılaştırın.** Karşılayabileceğiniz ve savunabileceğiniz bir hedefle başlayın ve veriye ve güvene sahip olunca sıkılaştırın. Bu, bölümün kusursuzluğun bekleyebileceği yönündeki tavsiyesini izler.
5. **Mevcut performansı kopyalamayın.** Hizmetiniz şu anda mükemmelse, kullanıcıların gerektirmediği sürece hedefi o seviyede belirlemeyin. Daha gevşek bir hedef değişikliğe yer açar ve kahramanca çabadan kaçınır.
6. **Bir hata bütçesi üzerinde anlaşın ve kullanın.** Bir dönemde ne kadar başarısızlığın kabul edilebilir olduğunu tanımlayın ve kalan bütçenin sürüm kararlarına yol göstermesine izin verin. Bunu teslimat ve operasyonun birlikte katıldığı düzenli bir toplantıda gözden geçirin.
7. **Anlaşmayı sade bir dille yazın.** Bir SLA neyin sağlandığını, nasıl ölçüldüğünü, sorunların nasıl bildirildiğini, hedefler kaçırıldığında ne olacağını ve ne zaman gözden geçirileceğini söylemelidir. Yalnızca bir avukatın ya da mühendisin okuyabileceği terimlerden kaçının.
8. **Hedefleri anlaşmalardan ayırın.** İmzaladığınız anlaşmalardan daha sıkı iç hedefler tutun. Pay, bir şey borçlanmadan önce tepki vermeniz için size alan sağlar.
9. **Sözünüzün neye bağlı olduğunu bilin.** Hizmet seviyenizin dayandığı ekipleri ve tedarikçileri listeleyin ve onların taahhütlerinin sizinkini desteklediğini denetleyin.
10. **Müşterilerin kullanabileceği biçimde raporlayın.** Sonuçları, ne olduğuna ve ne yaptığınıza dair kısa bir yorumla düzenli olarak paylaşın. Yorumsuz panolardan kaçının.
11. **Hedefleri müşterilerle gözden geçirin.** En az yılda bir, seviyelerin müşterilerin ihtiyaçlarına ve sizin sunabileceklerinize hâlâ uyup uymadığını sorun. Yanıt hayırsa değiştirin.
12. **Hizmet seviyelerini insanları cezalandırmak için kullanmayın.** Onları konuşmaları ve kararları başlatmak için kullanın. Sopa olarak kullanılan bir hedef oyunlaştırılır (bkz. Konu 5.6 — Metrikler ve Ölçüm).

## Ekibinizle tartışılacak sorular

**Kullanıcılarımız için iyi bir gün nasıl görünür ve bunu nasıl anlarız?**

Ekipten, kullanıcının sözcükleriyle, hizmetin iyi bir deneyiminin ne olduğunu betimlemesini isteyin. Sonra buna karşılık gelen neyi ölçtüğümüzü sorun. Çoğu zaman elimizdeki ölçüler kullanıcının deneyimini değil sistemlerimizi betimler. Kolaylaştırıcı, bir kullanıcı grubu kötü bir gün geçirse bunu fark edip etmeyeceğimizi sorabilir. Eklenecek ya da değiştirilecek bir gösterge seçin.

**Söz verdiğimiz ya da hedeflediğimiz bir sayımız var mı ve buna kim onay verdi?**

Resmî ya da gayriresmî mevcut hedefleri listeleyin. Her biri için kimin, ne zaman ve hangi temelde belirlediğini sorun. Birçok hedefin alışkanlıkla ya da ayrılmış biri tarafından belirlendiği anlaşılır. Hangilerinin doğrulanması, değiştirilmesi ya da bırakılması gerektiğini tartışın. Her birinin sahibi konusunda anlaşın.

**Ne kadar başarısızlığı göze alabiliriz ve bu alanla ne yapardık?**

Hata bütçesi fikrini tanıtın. Kullanıcıların ne kadar erişilemezliğe tahammül edeceğini ve ekibin bu alanla, örneğin daha hızlı sürümlerle, neler yapabileceğini sorun. Amaç, ödünleşimi sayılarla görmektir. Kesin yanıtlar beklemeyin; sınanacak ilk bir tahmin isteyin.

**Ortalamalarımız kötü deneyimleri nerede gizliyor?**

Bir ortalama bildiren bir ölçüye bakın. En yavaş yüzde birlik kullanıcı diliminin ne yaşadığını sorun. Bilmiyorsanız, nasıl öğreneceğinizi tartışın. Çoğu zaman küçük bir kullanıcı grubu ya da günün belirli bir saati çok daha kötü bir deneyim yaşar. Bir ay boyunca bir yüzdeliğe bakmayı planlayın.

**Hakkında sormadığımız hangi bağımlılıklarımız var?**

Hizmetinizin dayandığı hizmetleri, tedarikçileri ve ekipleri listeleyin. Her biri için neyi taahhüt ettiklerini ve kaçırdıklarını nasıl anlayacağınızı sorun. Birçok bağımlılığın belirtilmiş bir seviyesi yoktur. En önemlisini seçin ve bir konuşma başlatın.

**Bir hedef en son ne zaman değişti ve neyi tetikledi?**

Son değişikliği sorun. Uzun zaman önceyse, o zamandan beri kullanıcı ihtiyaçlarında ya da ekibin yeteneğinde neyin değiştiğini sorun. Düzenli bir gözden geçirmeyi tartışın. İyi tetikleyiciler yeni kullanıcı ihtiyaçları, gerçekçi olmayan bir hedefi açığa çıkaran olaylar ya da mimaride bir değişikliktir.

## Uygulamada: çevik bir ITIL örneği

Ulusal bir piyango işletmecisi çevrim içi bilet satın alma hizmeti işletiyor. On iki kişilik bir ekip bunu geliştiriyor ve işletiyor. İşletmenin, hizmetin "her zaman ayakta" olması gerektiğine dair gayriresmî bir kuralı var; ekip ise haftada iki kez sürüm çıkarıyor ve bir yılda dört kısa kesinti yaşadı. Kötü bir hafta sonunun ardından yönetici sponsor "%100 erişilebilirlik" talep ediyor ve ekip lideri bunun sık sürümlere son vereceğinden endişe ediyor.

Ekip lideri ve sponsor, müşteri hizmetleri başkanıyla bir çalıştay düzenliyor. Oyuncular için neyin önemli olduğunu soruyorlar. Yanıt, oyuncuların bir çekilişin kapanmasından önceki saatte bilet alabilmesi gerektiği; o saatin dışında hizmetin zarar vermeden dakikalarca kapalı kalabileceği. Bir gösterge tanımlıyorlar: her çekilişin kapanmasından önceki iki saatte başarılı olan satın alma girişimlerinin payı. Ekibin karşılayabileceğine inandığı, son performansının biraz altında bir hedef belirliyorlar ve her ay için bir hata bütçesi üzerinde anlaşıyorlar. Ayrıca bütçe neredeyse tükendiğinde, satın almaya dokunan sürümlerin bir sonraki aya kadar durdurulması ve ekibin güvenilirliğe yatırım yapması konusunda anlaşıyorlar.

Üç ay sonra bütçe, bir ödeme sağlayıcısı arızasının yaşandığı bir ayda bir kez tükeniyor ve ekip riskli sürümleri iki hafta boyunca çatışma olmadan durduruyor. Hedef, ekibe ve sponsora konuşmak için ortak bir yol veriyor. Bazı zorluklar sürüyor. Ödeme sağlayıcısının kendi taahhüdü ekibin hedefinden zayıf; dolayısıyla ekibin sözü, buna razı olmamış bir tedarikçiye bağlı. Ölçü ayrıca yalnızca başarıyı saydığı için kullanıcıların şikâyet ettiği yavaş bir ödeme sayfasını da göz ardı ediyor. Ekip 99. yüzdelikte bir hız göstergesi ekliyor ve sağlayıcıyla hizmet seviyeleri hakkında görüşmeler başlatıyor.

## Dört bakış açısı

### Ürün ve teslimat ekipleri

Teslimat ekipleri göstergelerin seçilmesine yardım etmeli ve planlamada hata bütçesini kullanmalıdır. Sayıların güvenilir olması için ölçümü hizmetin içine yerleştirin. Tükenmiş bir bütçeyi bir ceza olarak değil, güvenilirlik üzerinde çalışmak için bir neden olarak ele alın.

### Hizmet ve operasyon ekipleri

Operasyon ekipleri genellikle izlemeyi yürütür ve seviyeleri raporlar. Ölçü kümesini küçük tutun, yorumla birlikte gösterin ve verileri planlama konuşmalarına getirin. Hizmetinizin neye bağlı olduğunun bir listesini tutun ve taahhütlerin örtüştüğünü denetleyin.

### Liderlik ve yönetişim

Liderler ve sponsorlar beklentileri belirler. Kusursuzluk istemekten kaçının; kullanıcıların neye ihtiyaç duyduğunu ve ödünleşimin neye mal olduğunu sorun. Hata bütçesinin ortak bir kural olarak kullanılmasını destekleyin ve bunun kendi taleplerinize de uygulandığından emin olun. Hizmet seviyelerini müşterilerle bir takvime göre gözden geçirin.

### Müşteriler ve kullanıcılar

Müşteriler ve kullanıcılar, hizmet seviyesi belirtildiğinde ve karşılandığında yarar sağlar. Sizin için neyin ve ne zaman önemli olduğunu söyleyin. Anlayabileceğiniz biçimde raporlar isteyin ve belirtilen seviye artık ihtiyaçlarınıza uymadığında sağlayıcıya söyleyin.

## Yaygın başarısızlık biçimleri

- **Çok fazla ölçü.** Hangisinin önemli olduğunu kimse bilmez. Bunun yerine kullanıcı deneyimini yansıtan birkaçını seçin.
- **Yalnızca ortalamalar.** Ortalama iyi görünürken bir kullanıcı grubu acı çeker. Bunun yerine yüksek yüzdelikli bir ölçü ekleyin.
- **Mevcut performanstan kopyalanan hedefler.** Ekip kahramanlıklara kilitlenir. Bunun yerine hedefleri kullanıcı ihtiyaçlarından belirleyin ve veriyle sıkılaştırın.
- **%100 talep etmek.** Sürümler durur ve yenilik yavaşlar. Bunun yerine bir hata bütçesi ve onu kullanma kuralı üzerinde anlaşın.
- **Karşılığı olmayan sözler.** Hizmet seviyesi, razı olmamış tedarikçilere bağlıdır. Bunun yerine bağımlılıkları denetleyin ve taahhütleri hizalayın.
- **Kimsenin okumadığı anlaşmalar.** Şartlar hukuk diliyle yazılmıştır. Bunun yerine sade yazın ve müşterilerle gözden geçirin.
- **Yorumsuz panolar.** Sayılar anlamsız biçimde raporlanır. Bunun yerine ne olduğuna ve neyin değişeceğine dair kısa bir açıklama ekleyin.
- **Kaçırmaları cezalandırmak.** İnsanlar sorunları gizler. Bunun yerine kaçırmaları kararları ve öğrenmeyi tetiklemek için kullanın.

## Olgunluk modeli

| Boyut | Başlangıç | Gelişim | Standartlaştırma | Yönetim | Eşgüdüm |
|---|---|---|---|---|---|
| Seviyeleri tanımlama | Seviyeler varsayılır ya da gayriresmîdir | Bazı hizmetlerin belirtilmiş hedefleri vardır | Her hizmetin sahipleriyle birlikte kullanıcı tabanlı göstergeleri ve hedefleri vardır | Hedefler kullanıcı ihtiyaçlarına ve verilere karşı gözden geçirilir | Seviyeler müşteriler ve tedarikçilerle birlikte belirlenir |
| Ölçme | Ölçüler ad hoctur | Bazı göstergeler ölçülür | Göstergeler yüzdelikler dahil güvenilir biçimde ölçülür | Ölçüm kalitesi gözden geçirilir ve boşluklar giderilir | Ölçüm ekipler ve tedarikçiler arasında paylaşılır ve doğrulanır |
| Hata bütçelerini kullanma | Başarısızlık plansızdır | Bazı ekipler kabul edilebilir başarısızlığı tartışır | Bütçeler kilit hizmetlerde sürüm kararlarına yol gösterir | Bütçe kullanımı gözden geçirilir ve kurallar ayarlanır | Bütçeler birbirine bağımlı hizmetler arasında eşgüdümlüdür |
| Anlaşmalar ve bağımlılıklar | Sözler gayriresmîdir | Bazı anlaşmalar vardır | Anlaşmalar sade dille yazılmıştır, bağımlılıklar bilinir | Anlaşmalar ve tedarikçi taahhütleri sonuçlara karşı denetlenir | Anlaşmalar ekipler, tedarikçiler ve müşteriler arasında tutarlı bir zincir oluşturur |

## Kontrol listesi

- [ ] Her hizmet için iyinin neye benzediğini kullanıcıların sözcükleriyle betimledik.
- [ ] Her hizmetin kullanıcı deneyimini yansıtan iki ila dört göstergesi var.
- [ ] En az bir hız ölçüsü yalnızca ortalamayı değil, yüksek bir yüzdeliği kullanır.
- [ ] Hedefler yalnızca mevcut performanstan değil, kullanıcı ihtiyaçlarından belirlenir.
- [ ] Bir hata bütçesi vardır ve en az bir hizmet için sürüm kararlarına yol gösterir.
- [ ] Anlaşmalar sade bir dille yazılır ve müşterilerle gözden geçirilir.
- [ ] Diğer ekiplere ve tedarikçilere bağımlılıklar taahhütleriyle birlikte listelenmiştir.
- [ ] Sonuçlar yorumla birlikte düzenli olarak raporlanır.
- [ ] Hedefler yılda en az bir kez gözden geçirilir.
- [ ] Hizmet seviyesi verileri planlamada kullanılır, sopa olarak değil.

## Yapay zeka istemleri

**Amaç: kullanıcı ihtiyaçlarını aday göstergelere ve hedeflere dönüştürmek.**

```text
Help me move from user needs to indicators and objectives for [service].

What users do with the service and what matters to them (in their words, with any feedback or complaints): [paste].
Measurements we can already collect: [list].
Rules or contracts that set levels, with the source text: [paste, or write "none known"].

Propose two to four candidate indicators that reflect the user experience, say how each would be measured with the data I listed, and suggest how to express an objective for each, leaving numeric targets as [to be agreed with users and data]. Mark any indicator we cannot measure yet. Do not invent targets or performance figures. Ask clarifying questions first, and list what you are unsure of.
```

**Amaç: ortalamaların kötü deneyimleri gizleyip gizlemediğini çözümlemek.**

```text
Here are response times (or other measurements) for [service] over [period]: [paste a column of real values, or summary figures such as median, 90th, 99th percentile if you have them].

Using only my data, compute or describe the average, the median, and the high percentiles if the data allows. Explain in plain words what the gap between the average and the high percentiles suggests for users. Suggest one indicator and one question to ask. Do not invent data, and say if the data is too thin. List what you are unsure of.
```

**Amaç: sade dilli bir hizmet seviyesi anlaşması taslağının ana hatlarını çıkarmak.**

```text
Draft an outline for a service level agreement for [service] between [provider] and [customer].

What we provide: [describe].
Measures and targets already agreed or being proposed: [paste, or write "to be agreed"].
Support hours and contacts: [describe].
Dependencies on suppliers: [list].
Terms we must include because of contract or law, with source text: [paste, or write "none known"].

Produce an outline with plain-language sections: service description, hours, measures and how they are measured, how to report a problem, response and resolution expectations (marked [to be agreed]), what happens if targets are missed, reporting, review date. Do not invent legal terms. Ask clarifying questions first, mark assumptions, and list what you are unsure of.
```

**Amaç: bir hata bütçesi politikası planlamak.**

```text
Help me draft an error budget policy for [service].

Objective and period: [for example, "success rate of purchase attempts in the two hours before a draw closes, measured monthly"].
Current performance if known: [paste, or write "unknown"].
Release rhythm: [describe].
Who decides, and who is affected: [roles].

Draft a one-page policy: how the budget is calculated from the objective, how its use is tracked and shown, what happens at three stages of consumption (use [to be agreed] for thresholds), who may override and how, and how the policy is reviewed. Do not invent numbers. Ask clarifying questions first, and list what you are unsure of.
```

## Yapay zeka becerileri

- [service-level-agreement](../../../../skills/service-level-agreement/SKILL.md): bir anlaşmayı sade bir dille taslaklamak ya da gözden geçirmek için kullanın.
- [software-engineering-metrics](../../../../skills/software-engineering-metrics/SKILL.md): teslimat ve hizmet performansı ölçülerini seçmek ve yorumlamak için kullanın.
- [key-risk-indicators](../../../../skills/key-risk-indicators/SKILL.md): bir hizmet seviyesinin risk altında olduğunu gösteren erken uyarı göstergelerini seçmek için kullanın.
- [capacity-planning](../../../../skills/capacity-planning/SKILL.md): kapasitenin sözünü verdiğiniz seviyeleri desteklediğini denetlemek için kullanın.
- [vendor-management](../../../../skills/vendor-management/SKILL.md): tedarikçi taahhütlerini sunduğunuz seviyelerle hizalamak için kullanın.

## Temel kaynaklar

- **Service Level Objectives** (*Site Reliability Engineering*, Google, sre.google): göstergelerin, hedeflerin, anlaşmaların, yüzdeliklerin ve hata bütçelerinin en açık kamuya açık açıklaması.
- **Service-level agreement** (Wikipedia): SLA'ların tanımı, tipik içeriği, türleri ve tarihçesi.
- **DORA's software delivery performance metrics** (dora.dev): teslimat hızı ve kararlılığının ilişkili ölçüleri.
- **Quality of service** (Wikipedia): hizmet kalitesinin nasıl betimlendiği ve ölçüldüğü üzerine arka plan.

## Kaynakça

1. Service Level Objectives — Google SRE book, sre.google — https://sre.google/sre-book/service-level-objectives/
2. Service-level agreement — Wikipedia — https://en.wikipedia.org/wiki/Service-level_agreement
3. DORA's software delivery performance metrics — DORA, dora.dev — https://dora.dev/guides/dora-metrics-four-keys/
4. Quality of service — Wikipedia — https://en.wikipedia.org/wiki/Quality_of_service
5. Percentile — Wikipedia — https://en.wikipedia.org/wiki/Percentile
6. Service-level objective — Wikipedia — https://en.wikipedia.org/wiki/Service-level_objective
7. Site reliability engineering — Wikipedia — https://en.wikipedia.org/wiki/Site_reliability_engineering
8. Goodhart's law — Wikipedia — https://en.wikipedia.org/wiki/Goodhart%27s_law
9. Kanban (development) — Wikipedia — https://en.wikipedia.org/wiki/Kanban_(development)
