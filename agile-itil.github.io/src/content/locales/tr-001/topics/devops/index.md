# DevOps

**DevOps, geliştirme ve operasyonu ortak sahiplik, otomasyon ve hızlı geri bildirimle tek bir iş akışında buluşturma çabasıdır; ITIL'in önemsediği denetimleri hatta yerleştirerek hizmet yönetimini tamamlar.**

## Bu neden önemli

DevOps, çoğu kuruluşun sürekli teslimat ile BT operasyonu arasındaki buluşma noktasına verdiği addır. Bir hayal kırıklığından doğdu: geliştiriciler değişim için, operasyon çalışanları ise istikrar için ödüllendiriliyordu; bu yüzden iki grup zıt yönlere çekiyordu ve aralarındaki devir hız ile kalitenin kaybedildiği yerdi. DevOps ikisinden de fikirden çalışan hizmete uzanan yolun tamamının sorumluluğunu paylaşmasını ister.

ITSM'de çalışanlara DevOps ya tehdit edici ya da gereksiz görünebilir. Tehdit edici, çünkü operasyonun zor deneyimlerden sonra kurduğu süreçleri geçersiz sayıyor gibi görünür. Gereksiz, çünkü önerdiklerinin çoğu, örneğin olay gözden geçirmeleri, otomasyon ve sürekli iyileştirme, zaten ITIL'dedir. İki görüş de tam doğru değildir. Wikipedia'daki DevOps maddesi DevOps'u, ITIL'in 1990'lardaki "yukarıdan aşağı" ve katı çerçevesi olarak adlandırdığı şeyle karşılaştırır; bu eski sürümler için doğrudur; ITIL 4 çevik, DevOps ve yalın ile uyumlu olacak biçimde yazıldı (bkz. Konu 2.2 — ITIL).

DevOps'un tanımı tartışmalıdır ve Wikipedia maddesi bunu söyler. Bu konu maddeyi, DORA'nın araştırma sayfalarını ve Gene Kim'in "Üç Yol" anlatımını kullanır; neyin yerleşik, neyin tartışmalı olduğunu ve neyi bu kılavuzun doğrulayamadığını belirtir.

## Temel kavramlar

### DevOps nedir

[Wikipedia'daki DevOps maddesi](https://en.wikipedia.org/wiki/DevOps) onu, geliştirme süresini kısaltabilen ve geliştirme yaşam döngüsünü iyileştirebilen yazılım geliştirme ile BT operasyonunun entegrasyonu ve otomasyonu olarak anlatır. Akademik araştırmacılar Len Bass, Ingo Weber ve Liming Zhu'dan, onu bir sistemde bir değişikliği işleme almak ile onun normal üretime yerleştirilmesi arasındaki süreyi azaltmayı amaçlayan bir dizi uygulama olarak tanımlayan alıntı yapar. Madde, terimin birkaç bağlamda kullanıldığını ve tanımının tartışmalı olduğunu, 2015 ile 2017 arasındaki akademik çalışmaların özellikleri konusunda bir uzlaşma bulamadığını belirtir.

Madde, geliştirme yöntemlerini dağıtım ve operasyonla birleştirme önerilerinin 1980'lerin sonuna ve 1990'ların başına dayandığını ve ilk DevOps Days konferansının 2009'da Belçika'nın Gent kentinde Patrick Debois tarafından kurulan bu konferansın yapıldığını bildirir. DevOps'u genellikle üç ilkeyle nitelendirir: ortak sahiplik, iş akışı otomasyonu ve hızlı geri bildirim; ve bu nitelendirmenin kendisinin de tartışmalı olduğunu belirtir.

### Üç Yol

*The Phoenix Project* ve *The DevOps Handbook*'un yazarlarından Gene Kim, DevOps örüntülerinin türetilebileceğini savunduğu üç ilke anlatır. Kim'in IT Revolution sitesindeki kendi yazısında ve ikincil özetlerde özetlendiği biçimde:

| Yol | Fikir | Örnekler |
|---|---|---|
| **Birinci Yol: akış** | Tek bir silonun değil, tüm sistemin performansına bakın; işi fikirden değere hızlandırın | Bilinen kusurları aşağıya geçirmeyin; yerel optimizasyonun bütünü bozmasına izin vermeyin; her zaman akışı artırmaya çalışın |
| **İkinci Yol: geri bildirim** | Sonraki aşamalardan önceki aşamalara geri akan sinyalleri kısaltın ve güçlendirin | Telemetri, hızlı başarısız olan hatlar, müşteri geri bildirimi |
| **Üçüncü Yol: sürekli öğrenme ve deney** | Küçük, bilinçli riskler alan ve bunlardan öğrenen bir kültür oluşturun | Öğrenmeye zaman ayırmak, yerel keşifleri genel iyileştirmelere dönüştürmek |

Bunlar bu kılavuzun kendi temalarıyla örtüşür: akış (bkz. Konu 1.5 — Kanban ve Konu 1.7 — Yalın Yazılım Geliştirme), geri bildirim (bkz. Konu 3.10 — İzleme ve Etkinlik Yönetimi) ve öğrenme (bkz. Konu 1.10 — Çevik Öğrenme). Terminolojiye dair bir not: Kim'in yazısı İkinci Yol'u "geri bildirim döngülerini güçlendirin" olarak adlandırır, Handbook ise "geri bildirim" der.

### Uygulamalar

Wikipedia'ya göre sürekli entegrasyon ve sürekli teslimat, otomasyonla birlikte DevOps başarısı için kritiktir. Madde sürüm denetimini, sanal makineleri, kapsayıcılaştırmayı ve sürüm denetimini, otomatik testleri ve CI/CD'yi şema ve veri değişikliklerine uygulayan veritabanı DevOps'unu anar. GitOps'u dağıtım yapılandırmasını sürüm denetiminde yönetmek, DevSecOps'u ise statik ve dinamik analiz dahil "sola kaydır" (shift left) testleriyle güvenliği teslimata entegre etmek olarak anlatır. DORA'nın yetkinlikler listesinde sürekli teslimat, sürekli entegrasyon, dağıtım otomasyonu, test otomasyonu, gövde tabanlı geliştirme (trunk-based development), sürüm denetimi, veritabanı değişiklik yönetimi, izleme ve gözlemlenebilirlik, yaygın güvenlik, küçük partilerle çalışma ve devam eden iş sınırları vardır (bkz. Konu 3.5 — Sürüm ve Dağıtım Yönetimi).

### Kültür

Bu kılavuz için okunan DORA yetkinlik listesi kültürel öğeleri içerir: üretken (generative) kurumsal kültür, öğrenme kültürü, dönüştürücü liderlik, iş tatmini, iyi oluş ve ekip deneyleri. Bunları listeleyen sayfa onları açıklamaz ve sıralamaz. Başka bir DORA sayfası, ölçümlerinin kurumsal performansı ve ekip üyelerinin iyi oluşunu öngördüğünü söyler, siloya dayalı sahipliğe karşı uyarır ve geliştirme, operasyon ve sürüm ekipleri arasında ortak sahipliği önerir. Bu, Üçüncü Yol ile uyumludur: DevOps, araçlar kadar insanların birlikte nasıl çalıştığıyla da ilgilidir.

Yaygın anımsatıcı **CALMS** (kültür, otomasyon, yalın, ölçüm, paylaşım) çoğu zaman DevOps'u özetlemek için kullanılır. Wikipedia'daki DevOps maddesi bundan söz etmez ve bu kılavuz kaynağını doğrulamadı; okuyucular karşılaşacağı için burada yalnızca anılmıştır.

### DevOps ve çeviklik

Madde, otomatik derleme ve testin, sürekli entegrasyonun ve sürekli teslimatın çevik dünyada ortaya çıktığını ve Scrum'ın mühendislik uygulamalarını dışarıda bırakmasının otomasyon işinin DevOps'a ayrılmasına yol açtığını söyler. Bu, Scrum'ın yazılımın nasıl geliştirileceğini, test edileceğini, dağıtılacağını veya işletileceğini söylemediğini belirten Konu 1.4 — Teslimat Tahmini ve Planlama Metrikleri ile uyumludur. Extreme Programming mühendislik uygulamalarının çoğunu zaten içerir (bkz. Konu 1.6 — Extreme Programming). DevOps çevik kaygıyı yayın noktasının ötesine genişletir.

### DevOps ve ITIL

Madde DevOps'u ITIL'in 1990'lardaki "yukarıdan aşağı" ve katı çerçevesiyle karşılaştırır ve ITSM'yi daha fazla ele almaz. Bugün için daha adil bir tablo:

| | Genellikle vurgular | Tek başına kullanılırsa risk |
|---|---|---|
| **DevOps** | Akış, otomasyon, ortak sahiplik, hızlı geri bildirim | Kayıtların, denetimlerin ve daha geniş hizmet görünümünün ihmal edilmesi |
| **ITIL 4** | Değer, uygulamalar, yönetişim, geniş bir hizmet uygulamaları yelpazesi | Uygulamaların ağır süreç olarak ele alınması |

ITIL 4'ün kendi sertifikasyon şeması, Wikipedia'daki ITIL maddesinin listelediği gibi, Managing Professional yolunda High Velocity IT (HVIT) adlı uzman bir modül içerir. Bu, sahibinin hızlı hareket eden dijital işi başlı başına bir konu olarak ele aldığını gösterir. Pratik bir birleşim: ITIL uygulamalarını hatta hayata geçirmek için DevOps uygulamalarını kullanın; örneğin değişiklikleri otomatik olarak kaydetmek, testleri risk denetimi olarak çalıştırmak ve izlemeyi etkinlik uygulaması olarak kullanmak (bkz. Konu 3.4 — Değişiklik Sağlama ve Konu 5.1 — Çevik Hizmet Yönetimi).

### DevOps ve site reliability engineering

Wikipedia maddesi Google'ın site reliability engineering'i 2003'te geliştirdiğini ve özgün yazarlarından bazılarının SRE'yi DevOps'un bir uygulaması olarak gördüğünü söyler. SRE maddesi onu DevOps'un belirli bir uygulaması olarak adlandırır; güvenilir sistemler kurmaya yoğunlaştığı için daha dardır (bkz. Konu 5.3 — Site Reliability Engineering).

### Ölçümler

DORA'nın yazılım teslimat performansı ölçümleri ortak bir sözcük dağarcığı sağlar: değişiklik teslim süresi (change lead time), dağıtım sıklığı, başarısız dağıtımdan kurtarma süresi, değişiklik başarısızlık oranı ve dağıtım yeniden iş oranı (bkz. Konu 3.4 — Değişiklik Sağlama ve Konu 5.6 — Metrikler ve Ölçüm). Wikipedia maddesi ölçümlerin 2016'da yayımlandığını, kurtarma ölçümünün 2023 raporunda yeniden adlandırıldığını, 2024'te bir yeniden iş ölçümünün eklendiğini ve 2025'te DORA'nın performans kademelerini yedi ekip arketipiyle değiştirdiğini bildirir. Ayrıca bazı uzmanların DORA araştırma yöntemini ve ölçümlerini eleştirdiğini kaydeder. Ölçümleri puan olarak değil, yararlı sorular olarak ele alın.

### Eleştiriler ve sınırlar

Yerleşik bir tanımın olmamasının ötesinde madde, DORA yöntemine yönelik eleştiriyi bildirir. Yaygın pratik eleştiriler, ki burada kaynak bulguları olarak değil pratik deneyim olarak sunulur, şunlardır: "DevOps"un eski operasyon rolü için bir iş unvanı olarak kullanılması, kültür değişikliği olmadan benimsenen araçlar ve hız peşinde uyumun ihmal edilmesi. Madde benimseme istatistikleri vermez.

## İyi uygulamalar

1. **DevOps ile neyi kastettiğinizde anlaşın.** Ekipleriniz için ne anlama geldiğine dair kısa bir ifade yazın; örneğin bir hizmetin ortak sahipliği, otomatik teslimat ve hızlı geri bildirim. Ortak bir tanım etiketler üzerine tartışmaları önler.
2. **Hizmetin sahipliğini paylaşın.** Bir hizmeti kuranları nasıl çalıştığından sorumlu kılın ve onlara araçları verin: nöbet, izleme ve erişim. Onları operasyon uzmanlığıyla destekleyin.
3. **Üretime giden yolu otomatikleştirin.** Her değişikliği derleyen, test eden ve dağıtan bir hat kurun. Ne yaptığını kaydedin. Hattı kullanıcıları olan bir ürün olarak görün.
4. **Küçük partilerle çalışın.** Küçük değişiklikleri sık yayımlayın. Bu, DORA'nın yetkinlik listesinin önerdiği gibi riski azaltır ve geri bildirimi hızlandırır.
5. **Geri bildirim döngülerini kısaltın.** Test sonuçlarını, izlemeyi ve kullanıcı geri bildirimini ekibe dakikalar veya saatler içinde görünür kılın. İkinci Yol'u izleyin: geri akan sinyalleri güçlendirin.
6. **Akışın tamamına bakın.** Fikirden çalışan hizmete giden yolu haritalayın ve geliştirme ekibinin dışındakiler dahil en uzun beklemeleri bulun. Birinci Yol'u izleyin: bir silonun optimizasyonunu bütünün pahasına yapmayın (bkz. Konu 5.4 — Değer Akışı Yönetimi).
7. **Güvenliği ve uyumu içine yerleştirin.** Otomatik güvenlik denetimlerini ve politika denetimlerini hatta koyun ve kanıtı yan ürün olarak kaydedin (bkz. Konu 3.13 — Bilgi Güvenliği Yönetimi ve Konu 5.7 — Yönetişim, Risk ve Uyum).
8. **Kültürü birinci sınıf bir kaygı olarak ele alın.** Öğrenmeye, suçlamasız gözden geçirmelere, psikolojik güvenliğe ve ortak hedeflere yatırım yapın. DORA'nın yetkinlik listesi kültürü teknik öğelerin yanında bir nedenle içerir.
9. **Öğrenmek ve denemek için zaman ayırın.** Deneyler için zaman ve güvenli alanlar ayırın ve dersleri paylaşın. Üçüncü Yol'u izleyin.
10. **ITIL uygulamalarını yardımcı oldukları yerde kullanın.** Olay, sorun, değişiklik ve bilgi uygulamalarını otomasyon ve hafif kayıtlarla uygulayarak koruyun. Amacına hizmet etmeyen adımları kaldırın.
11. **Dikkatle ölçün.** DORA tarzı ölçümleri hizmet başına izleyin, kendi geçmiş performansınıza göre iyileştirin ve bunları hedef olarak belirlemekten kaçının (bkz. Konu 5.6 — Metrikler ve Ölçüm).
12. **Unvan tuzağından kaçının.** Geliştirme ile operasyon arasında yeni bir silo haline gelen ayrı bir "DevOps ekibi" oluşturmayın. Uygulamaları ekiplere yayın ve yardım için platform veya destekleyici ekipler kullanın.

## Ekibinizle tartışılacak sorular

**DevOps burada ne anlama geliyor ve sözcüğü ilk nerede duyduk?**

Herkesten tek cümlelik bir tanım isteyin. Karşılaştırın. Wikipedia maddesi tanımın tartışmalı olduğunu söyler; bu yüzden farklar beklenir. Somut bir ortak ifade yazın: kim neyin sahibi, ne otomatik, hangi geri bildirim var. Kolaylaştırıcı, sözcük yüzünden şimdiye kadar ne değiştiğini sorabilir.

**Bir değişiklik "hazır" ile "canlı" arasında nerede bekliyor ve beklemenin sahibi kim?**

Yakın tarihli bir değişikliğin izini sürün ve beklemeleri listeleyin: gözden geçirmeler, onaylar, ortamlar, sürüm pencereleri. Ekibin dışındakileri işaretleyin. Hangi beklemelerin gerçek risklere karşı koruduğunu ve hangilerinin alışkanlık olduğunu sorun. Sahibiyle birlikte çalışarak kısaltılacak birini seçin.

**Üretimde bir şey bozulduğunda kim nöbette ve düzeltmek için araçları var mı?**

Kimin çağrıldığını ve tek başına neler yapabildiğini sorun. Geliştirenler nöbette değilse nedenini sorun. Operasyon çalışanları kodu değiştiremiyorsa ne yaptıklarını sorun. Burada ortak sahipliğin nasıl görüneceğini ve hangi desteğin gerekeceğini tartışın.

**Bir yayından sonra hangi geri bildirimi alıyoruz ve ne kadar hızlı?**

Sinyalleri listeleyin: testler, izleme, destek kayıtları, kullanıcı yorumları. Her birinin ekibe ulaşmasının ne kadar sürdüğünü sorun. Tipik yanıtlar: testler dakikalar içinde, kayıtlar günler içinde. Hızlandırılacak bir sinyal seçin.

**Bir şey denemek ve başarısız olmak ne kadar güvenli?**

Yakın tarihli başarısız bir deneyin örneğini ve ilgili kişilere ne olduğunu isteyin. Üçüncü Yol küçük başarısızlıklardan öğrenmeye dayanır. Deneyleri neyin daha güvenli kılacağını tartışın: sınırlar, geri almalar ve suçlamasız gözden geçirme.

**ITIL uygulamalarımız hatta nasıl görünüyor ve nerede görünmüyor?**

Değişiklik, olay ve bilgi uygulamalarını alın ve her birinin otomasyonda nerede göründüğünü sorun. Boşluklar elle işe veya kanıtlanmamış denetimlere işaret eder. Hatta taşınacak bir uygulamada anlaşın.

## Uygulamada: çevik bir ITIL örneği

Ulusal bir posta hizmetinin 40 kişilik bir geliştirme grubu ve 25 kişilik bir operasyon grubu var. Geliştiriciler her çeyrekte büyük bir sürüm yayımlıyor ve operasyona bir paket ile uzun bir belge devrediyor; operasyon bunu bir hafta sonunda dağıtıyor. Operasyon, geliştiricilerin üretimi anlamadığından şikâyet ediyor; geliştiriciler ise bir kusurun hızlı düzeltilmesi gerektiğinde operasyona ulaşılamadığından. Yakın tarihli bir sürüm 19 saat sürdü, koli izleme sayfasını bozdu ve bir gün süren karşılıklı suçlamaya yol açtı.

Yeni bir platform başkanı tek bir ürün ekibiyle, koli izleme hizmetiyle, bir deneme öneriyor. Dört geliştirici ve iki operasyon mühendisi hizmeti uçtan uca sahiplenen tek bir ekip oluşturuyor. Geliştiriciler, operasyon mühendislerinin desteğiyle nöbet çizelgesine katılıyor. Ekip, birleştirilen her değişikliği derleyen, test eden ve bir hazırlık (staging) ortamına dağıtan, üretime ise hizmet sahibinin verdiği tek bir onay adımıyla dağıtan bir hat kuruyor. Değişiklik kayıtlarını hat oluşturuyor. İzleme ekleniyor, uyarılar tüm ekibe gidiyor ve her üretim olayı kısa bir suçlamasız gözden geçirme alıyor. Ekip en az haftalık yayımlamaya karar veriyor ve platform başkanı ondan teslim süresini, dağıtım sıklığını, değişiklik başarısızlık oranını ve kurtarma süresini izlemesini istiyor.

Dört ay sonra ekip haftada iki kez yayımlıyor, birleştirmeden üretime geçen medyan süre bir günün altında ve son olay, değişikliği yazan geliştirici tarafından bir saatin altında düzeltildi. Her şey işlemiyor. Operasyon mühendisleri geliştiricilerin uyarılarının gürültülü olduğunu görüyor ve geliştiriciler geceleri nöbette olmaya içerliyor. Koli izlemeye bağımlı komşu bir ekibe yeni ritim söylenmemişti ve bir değişiklik karşısında şaşırdı. Platform başkanı ekibin uyarıları ayarlaması için zaman ayırıyor, gece çağrılarına sınır koyan bir nöbet çizelgesi ekliyor ve bağımlı ekiplerle aylık bir toplantı düzenliyor. İç denetim onaylara ilişkin kanıtı görmek istiyor ve platform başkanı hat kayıtlarını ve olay gözden geçirmelerini gösteriyor.

## Dört bakış açısı

### Ürün ve teslimat ekipleri

Teslimat ekipleri operasyonel sorumluluğu üstlenir: izleme, nöbet ve olay öğrenmesi. Hattı ve ihtiyaç duyduğunuz geri bildirimi kurun, devretmek yerine operasyon uzmanlığı isteyin. Değişiklikleri küçük ve görünür tutun.

### Hizmet ve operasyon ekipleri

Operasyon ekipleri hizmetlerin nasıl başarısız olduğuna ve hangi denetimlerin önemli olduğuna dair bilgi getirir. Platformu ve denetimleri kurmaya yardım edin, nöbeti paylaşın ve öğretin. Bir kapı olmaktan kaçının; güvenli yolu kolay yol yapan bir kolaylaştırıcı olun.

### Liderlik ve yönetişim

Liderler koşulları yaratır: geliştirme ve operasyon arasında ortak hedefler, otomasyon için zaman, başarısızlıktan öğrenen bir kültür ve hattan gelen kanıta güven. Teşvikleri değiştirmeden ekipleri yeniden adlandırmaktan kaçının ve DevOps benimsemesini değil, sonuçları isteyin.

### Müşteriler ve kullanıcılar

Müşteriler ve kullanıcılar DevOps'u daha hızlı iyileştirme ve daha hızlı kurtarma olarak görür. Sık, küçük değişiklikler ve bunlara dair net iletişim bekleyin. Hızla geri bildirim verin; çünkü ekip onu kullanacak biçimde kurulmuştur.

## Yaygın başarısızlık biçimleri

- **Yeni bir silo olarak DevOps ekibi.** Geliştirme ve operasyon hâlâ konuşmaz. Bunun yerine uygulamaları ekiplere yayın ve platform ekiplerini kolaylaştırıcı olarak kullanın.
- **Kültürsüz araçlar.** Bir hat kurulur ve başka hiçbir şey değişmez. Bunun yerine sahipliği, teşvikleri ve geri bildirimi birlikte değiştirin.
- **Güvenlik olmadan hız.** Yayınlar hızlanır ve başarısızlıklar artar. Bunun yerine tempodan önce testlere, izlemeye ve geri almaya yatırım yapın.
- **ITIL'i tamamen bırakmak.** Kayıtlar ve denetimler kaybolur. Bunun yerine uygulamaları koruyun ve hatta uygulayın.
- **Desteksiz nöbetçi geliştiriciler.** Tükenmişlik izler. Bunun yerine çizelgeyi paylaşın, uyarıları ayarlayın ve gece çağrılarını sınırlayın.
- **Hedef olarak metrikler.** Ekipler dağıtım sayılarını manipüle eder. Bunun yerine birden çok ölçüm kullanın ve kendi geçmişinizle karşılaştırın.
- **Bağımlı ekipleri göz ardı etmek.** Değişiklikler komşuları şaşırtır. Bunun yerine ritmi ve değişiklikleri sizin ekibinize bağımlı ekiplere iletin.
- **Sözcüğü hedef saymak.** Etiketler sonuçların yerini alır. Bunun yerine kullanıcılarınız için daha iyi akışın, geri bildirimin ve öğrenmenin neye benzediğini sorun.

## Olgunluk modeli

| Boyut | Başlangıç | Gelişim | Standartlaştırma | Yönetim | Eşgüdüm |
|---|---|---|---|---|---|
| Ortak sahiplik | Geliştirme ve operasyon yayında devreder | Bazı ekipler nöbeti paylaşır | Ekipler hizmetlerini uçtan uca destekle sahiplenir | Sahipliğin kalite ve yük üzerindeki etkileri ölçülür | Sahiplik modelleri ekipler, platformlar ve tedarikçiler arasında eşgüdümlüdür |
| Otomasyon ve akış | Teslimat elle ve partilidir | Bazı hatlar vardır | Ortak bir hat değişiklikleri derler, test eder, dağıtır ve kaydeder | Teslim süresi, sıklık, başarısızlık ve kurtarma ölçülür ve ayarlanır | Hatlar ve akış ekipler ve değer akışları genelinde optimize edilir |
| Geri bildirim | Geri bildirim kullanıcılardan sorunlardan sonra gelir | Bazı ekipler yayınları izler | Testler, izleme ve kullanıcı geri bildirimi ekiplere dakikalar veya saatler içinde ulaşır | Geri bildirimin hızı ve kalitesi ölçülür ve iyileştirilir | Geri bildirim döngüleri ekipleri, tedarikçileri ve müşterileri kapsar |
| Kültür ve öğrenme | Başarısızlığı suçlama izler | Bazı suçlamasız gözden geçirmeler yapılır | Suçlamasız gözden geçirmeler, deneyler ve öğrenme zamanı rutindir | Öğrenme eylemleri izlenir ve sonuçlar kontrol edilir | Öğrenme kuruluş genelinde sürekli yayılır |

## Kontrol listesi

- [ ] DevOps'un bizim için ne anlama geldiğine dair ortak yazılı bir tanımımız var.
- [ ] Bir hizmeti kuran ekipler onu işletme sorumluluğunu paylaşıyor.
- [ ] Bir hat değişiklikleri derliyor, test ediyor, dağıtıyor ve ne yaptığını kaydediyor.
- [ ] Değişiklikler küçük partilerle, sık yayımlanıyor.
- [ ] Test, izleme ve kullanıcı geri bildirimi ekibe hızla ulaşıyor.
- [ ] Güvenlik ve politika denetimleri hatta çalışıyor.
- [ ] Nöbet paylaşılıyor, gece çağrıları sınırlı ve uyarılar ayarlı.
- [ ] Olay gözden geçirmeleri suçlamasız ve sahipli eylemler üretiyor.
- [ ] Her hizmet için teslim süresini, dağıtım sıklığını, değişiklik başarısızlık oranını ve kurtarma süresini izliyoruz.
- [ ] Bağımlı ekiplere yayın ritmimiz ve büyük değişikliklerimiz bildiriliyor.

## Yapay zeka istemleri

**Amaç: "hazır" ile "canlı" arasındaki beklemeleri haritalamak.**

```text
Help me map the waits for a typical change in [team or service].

The steps from "ready" to "live," who does each, whether it is manual or automated, and how long work waits before it (use real data; mark estimates as estimates): [paste].

Produce a simple text diagram, highlight the three longest waits and which team owns each, and suggest, for each, a question to ask about whether the wait protects against a real risk. Do not invent durations. If the data are too thin, say what to collect. Ask clarifying questions first, and list what you are unsure of.
```

**Amaç: ITIL uygulamalarının hattınızda nerede göründüğünü kontrol etmek.**

```text
Help me compare our pipeline with service management practices.

What our pipeline does today, step by step: [paste].
The practices we want to check: change enablement, release and deployment, incident management, problem management, knowledge management, configuration management.

For each practice, say what in the pipeline description appears to support it (quote my words), what is missing, and one question to ask. Do not claim that a standard requires anything unless I pasted its text. Ask clarifying questions first, and list what you are unsure of.
```

**Amaç: bir ekiple ortak sahiplik pilotu planlamak.**

```text
Plan a four-month pilot of shared ownership for [service], bringing together [number] developers and [number] operations engineers.

Today's arrangement: [describe who builds, who runs, who is on call].
Concerns from each side: development [list]; operations [list].
Measures we have: [list].

Give a plan with: team formation, on-call arrangements with limits, pipeline and monitoring work, how the team learns from incidents, which measures to review (leave targets as [to be agreed]), what evidence to keep for audit, and how to tell dependent teams. Ask clarifying questions first, mark assumptions, and list what you are unsure of.
```

**Amaç: karma bir ekip için suçlamasız bir olay gözden geçirmesi tasarlamak.**

```text
Design a 45-minute blameless review for this incident: [describe the incident factually].

People involved: [roles from development and operations].
Information available (timeline, alerts, changes): [list].

Provide an agenda that builds the timeline first, identifies contributing causes in systems and processes, notes what went well, and ends with at most three actions with owners. Include prompts that avoid blame. Ask clarifying questions first, and list what you are unsure of.
```

## Yapay zeka becerileri

- [agile-delivery](../../../../skills/agile-delivery/SKILL.md): küçük, sık yayınları ve çevrelerindeki denetimleri planlamak için kullanın.
- [test-driven-development](../../../../skills/test-driven-development/SKILL.md): bir hattın dayandığı otomatik testleri oluşturmak için kullanın.
- [shift-left-testing](../../../../skills/shift-left-testing/SKILL.md): test ve güvenlik denetimlerini hatta daha erkene taşımak için kullanın.
- [on-call-rotation](../../../../skills/on-call-rotation/SKILL.md): adil sınırlarla paylaşılan nöbet tasarlamak için kullanın.
- [postmortem](../../../../skills/postmortem/SKILL.md): Üçüncü Yol'u besleyen suçlamasız gözden geçirmeler yürütmek için kullanın.

## Temel kaynaklar

- **DevOps** (Wikipedia): tanımlara, uygulamalara, çevik, SRE ve DevSecOps ile ilişkilere ve DORA ölçümlerine genel bakış; belirtilen tartışmalarla.
- **The Three Ways: The Principles Underpinning DevOps** (Gene Kim, IT Revolution): akış, geri bildirim ve sürekli öğrenmenin kaynağı.
- **DORA capabilities and metrics** (dora.dev): araştırma programının yetkinlik listesi ve yazılım teslimat ölçümleri.
- **The DevOps Handbook** ve **The Phoenix Project** (Gene Kim ve ortak yazarlar): Üç Yol'u ayrıntılı geliştiren kitaplar.

## Kaynakça

1. DevOps — Wikipedia — https://en.wikipedia.org/wiki/DevOps
2. The Three Ways: The Principles Underpinning DevOps — Gene Kim, IT Revolution — https://itrevolution.com/the-three-ways-principles-underpinning-devops/
3. DORA capabilities — DORA, dora.dev — https://dora.dev/capabilities/
4. DORA's software delivery performance metrics — DORA, dora.dev — https://dora.dev/guides/dora-metrics-four-keys/
5. Site reliability engineering — Wikipedia — https://en.wikipedia.org/wiki/Site_reliability_engineering
6. ITIL — Wikipedia — https://en.wikipedia.org/wiki/ITIL
7. Continuous delivery — Wikipedia — https://en.wikipedia.org/wiki/Continuous_delivery
8. Lean software development — Wikipedia — https://en.wikipedia.org/wiki/Lean_software_development
9. Agile software development — Wikipedia — https://en.wikipedia.org/wiki/Agile_software_development
