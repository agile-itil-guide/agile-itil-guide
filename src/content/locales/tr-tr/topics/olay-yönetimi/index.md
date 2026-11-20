# Olay Yönetimi

**Olay yönetimi, bozulmuş bir hizmeti güvenli olduğu ölçüde en hızlı biçimde geri getirir; onu işleten çevik alışkanlık, baskı altında net roller ve ardından her olayı bir değişikliğe dönüştüren suçlamasız bir gözden geçirmedir.**

## Bu neden önemli

Olaylar, bir hizmetin yargılandığı andır. Kullanıcılar aylarca süren iyi erişilebilirliği hatırlamaz; kesintiyi ve nasıl ele alındığını hatırlar. Kimin ne yapacağını, nasıl iletişim kuracağını ve ne zaman yardım çağıracağını önceden belirlemiş bir ekip, doğaçlama yapan bir ekipten daha hızlı hizmeti geri getirir ve daha az hata yapar.

Geliştirdiklerini işleten çevik ekipler olayları çoğu zaman gayriresmî biçimde ele alır. Bu, bir olay büyük olana, birkaç ekibe yayılana veya geceleyin gerçekleşene kadar işe yarar. O zaman rollerin ve kayıtların eksikliği ortaya çıkar: mühendisler teknik soruna yığılır, kimse müşterilere söylemez ve iki kişi çelişen değişiklikler yapar. ITSM'nin olay yönetimi uygulaması, site güvenilirliği mühendisliğinden uygulamalarla birlikte, bunu önlemek için denenmiş yollar sunar.

[Olay yönetimi hakkındaki Wikipedia maddesi](https://en.wikipedia.org/wiki/Incident_management), acil durum müdahalesinden bilgisayar güvenliğine kadar birçok alanı kapsar. BT hizmet yönetimi için amacın, normal hizmeti kararlaştırılan hizmet seviyesi içinde mümkün olduğunca çabuk geri getirmek olduğunu söyler, olayı bir BT hizmetinde planlanmamış bir kesinti veya kalitesinde bir azalma olarak tanımlarken ITIL 2011'den alıntı yapar ve üç zorluk sıralar: uyarı gürültüsü, uzun süren sorun çözümü ve kesintileri öngörmenin zorluğu. Ayrıntı için bu konu, büyük bir kuruluşun uygulamasından bir olay komuta yaklaşımını ve suçlamasız postmortem'leri anlatan Google'ın *Site Reliability Engineering* kitabının iki bölümüne yoğun olarak dayanır. Bu bölümleri tek yaklaşım olarak değil, iyi belgelenmiş bir yaklaşım olarak görün.

## Temel kavramlar

### Olay nedir

ITSM kullanımında **olay** (incident), bir hizmette planlanmamış bir kesinti veya kalitesinde bir azalmadır. ITSM maddesi ayrıca "olası" bir kesintiyi de içerir. Olay, altta yatan neden olan **sorunla** (problem) veya rutin bir istek olan **hizmet talebiyle** (service request) aynı şey değildir (bkz. Konu 3.3 — Sorun Yönetimi ve Konu 3.6 — Hizmet Talebi Yönetimi). Üçünü ayrı tutmak önemlidir, çünkü her biri farklı bir hedef için yönetilir: hizmeti geri getirmek, nedenleri ortadan kaldırmak ve rutin talebi karşılamak.

### Hedef: hizmeti geri getirmek, kanıtı korumak

Olay yönetiminin ilk amacı hizmeti geri getirmektir. Olay yönetimine dair SRE bölümü ikinci bir amaç ekler: kök nedeni sonradan bulmak için gereken kanıtı korumak. Bölümün kendi iyi uygulamaları, bu ruhla, hizmeti geri getirmeye ve kanıtı korumaya öncelik vermeyi söyler. Nedeni düzeltmek daha sonra, sorun yönetiminde gelebilir.

### Yönetilmeyen olaylar neden ters gider

Andrew Stribblehill tarafından yazılan SRE bölümü, kesintisi tam bir çöküşe dönüşen bir nöbetçi mühendisin uzun bir örneğini kullanır. Yönetilmeyen olayların üç tehlikesini adlandırır:

- **Teknik soruna keskin odaklanma.** Bir düzeltmeye gömülen mühendisler hafifletmeyi ve daha geniş resmi gözden kaçırır.
- **Zayıf iletişim.** Kimse başkalarının ne yaptığını bilmez ve paydaşlar bilgisiz kalır.
- **Başıboş çalışma (freelancing).** Son dakika dağıtımı gibi eşgüdümsüz değişiklikler durumu kötüleştirir.

### Baskı altında roller

Bölüm yaklaşımını, acil durum müdahalesinden gelen Olay Komuta Sistemi'ne (Incident Command System) dayandırır (olay yönetimi hakkındaki Wikipedia maddesi de bundan söz eder). Ana fikirleri:

| Rol | Ne yapar |
|---|---|
| **Olay komutanı** | Üst düzey durumu tutar, müdahaleyi yapılandırır, engelleri kaldırır ve henüz devredilmemiş her rolü üstlenir |
| **Operasyon lideri** | Araçları soruna uygular; olay sırasında sistemi yalnızca operasyon ekibi değiştirir |
| **İletişim lideri** | Müdahalenin kamusal yüzüdür; düzenli güncellemeler yayımlar ve olay belgesini güncel tutar |
| **Planlama lideri** | Hata kaydı açmak, devirleri düzenlemek ve değişikliklerin geri alınabilmesi için normalden sapmaları izlemek gibi daha uzun vadeli konuları ele alır |

Bölüm ilkeyi, sorumlulukların özyinelemeli ayrımı olarak adlandırır. Net roller, insanların meslektaşlarını sorgulamak zorunda kalmadığı için özerklik sağlar ve aşırı yüklenmiş bir kişi daha fazla personel ister ve işin parçalarını devreder. Komutanlar arasındaki devirler açık ve onaylıdır.

### Canlı olay belgesi

Bölüm, komutanın en önemli görevinin, ideal olarak aynı anda birkaç kişi tarafından düzenlenebilen, olayın durumuna dair canlı bir belge tutmak olduğunu söyler. Dağınık olabilir ama yararlı kalmalıdır; kilit bilgiler üstte olmalı ve sonraki çözümleme için saklanmalıdır. Ortak bir kanal veya fiziksel bir oda komuta noktası olarak hizmet eder.

### Bir olay ne zaman ilan edilir

Bölüm, kötüleşen bir sorunun saatler içine girmesini beklemek yerine olayı erken ilan etmeyi önerir. Bir olayı, onu düzeltmek için ikinci bir ekibin devreye girmesi gerekiyorsa, kesinti müşterilere görünür durumdaysa veya bir saat yoğun çözümlemeden sonra hâlâ çözülmediyse olay olarak görmeyi önerir. Bunlar tek bir kuruluşun pratik kurallarıdır. Kendi eşikleriniz hizmetlerinizi ve kullanıcılarınızı yansıtmalıdır.

### Öncelik ve ciddiyet

Bu kılavuz için okunan kaynaklar öncelik veya ciddiyet düzeylerini tanımlamaz ve Wikipedia maddesi hiçbirini belirtmez. Pratikte ekipler düzeyleri kullanıcılar üzerindeki etkiden ve ihtiyacın aciliyetinden tanımlar ve her düzeyde kimin çağrılacağına önceden karar verir. Şemayı kısa tutun, örneklerle birlikte verin ve geçmiş olaylara uygulayarak sınayın.

### İletişim

İletişimin iki kitlesi vardır. Müdahale edenlerin durumu ve kimin ne yaptığını bilmesi gerekir. Paydaşların ve kullanıcıların neyin etkilendiğini, ne yapıldığını ve bir sonraki güncellemeyi ne zaman bekleyeceklerini bilmesi gerekir. SRE bölümündeki iletişim lideri ikinci kitleye hizmet eder ve birinci için günlüğü tutar. Kamuya dönük kesintiler için kriz iletişimi planı yararlıdır (aşağıdaki kriz iletişimi becerisine bakın).

### Suçlamasız postmortem'ler

Postmortem kültürüne dair SRE bölümü öğrenme yarısını ortaya koyar. Bir postmortem olayı, etkisini, hafifletmeyi, kök nedenleri ve izleme eylemlerini kaydeder. Amaçları olayı belgelemek, katkıda bulunan tüm kök nedenleri anlamak ve etkili önleyici eylemler başlatmaktır. Suçlamasızdır: bireyleri veya ekipleri suçlamadan katkıda bulunan nedenleri belirler ve herkesin "iyi niyetli olduğunu ve elindeki bilgiyle doğru olanı yaptığını" varsayar. Bölümün sözleriyle, "İnsanları 'düzeltemezsiniz' ama sistemleri ve süreçleri düzeltebilirsiniz."

Bölüm, postmortem tetikleyicilerini önceden tanımlamayı önerir; örneğin bir eşiği aşan kullanıcıya görünür kesinti, herhangi bir veri kaybı, geri alma gibi nöbetçi müdahalesi, bir eşiğin üzerinde çözüm süresi veya bir izleme arızası. Ayrıca "Gözden geçirilmemiş bir postmortem hiç var olmamış gibidir" der ve bu nedenle düzenli gözden geçirme oturumlarını ve ortak bir depoyu önerir. Aylık bir bülten, okuma kulüpleri ve geçmiş olayların yeniden canlandırıldığı bir "Talihsizlik Çarkı" (Wheel of Misfortune) gibi kültür oluşturma etkinliklerini anlatır.

### Büyük olaylar

Birçok ITSM uygulaması, olağandan daha resmî bir müdahale gerektiren olayı **büyük olay** (major incident) olarak tanımlar. Burada okunan kaynaklar bunu tanımlamaz; bu nedenle kendi sözlerinizle yapın: örneğin birçok kullanıcıyı veya kritik bir hizmeti etkileyen ve ekipler arasında eşgüdümlü bir müdahale gerektiren bir olay. Önemli olan, insanların neyin değiştiğini önceden bilmesidir: kim komuta eder, kim çağrılır, güncellemeler ne sıklıkla gider.

### Olaylar ve sürekli teslimat

Olaylar çoğu zaman yakın zamandaki değişikliklerden doğar. Çevik ekipler sık sürüm yayımladıkları ve kısa geri bildirim döngüleri olduğu için bunlardan öğrenmeye elverişlidir. Öğrenmenin bir yola ihtiyacı vardır: postmortem eylemleri sahipleri ve tarihleriyle iş listesine girer ve tekrarlayan olaylar sorun yönetimine gider. Bu yol olmadan olay ele alma, bir onarım rutinine dönüşür.

## İyi uygulamalar

1. **Neyin olay sayılacağına önceden karar verin.** Örneklerle kısa bir tanım yazın ve bir tane ilan etmenin eşiğini düşürün. SRE bölümünün pratik kuralı, ikinci bir ekibe ihtiyaç duyulduğunda, müşteriler sorunu görebildiğinde veya bir saatlik çözümleme çözmediğinde erken ilan etmektir.
2. **Örneklerle birkaç ciddiyet düzeyi tanımlayın.** Bunları kullanıcı etkisine dayandırın ve her düzeyde kimin çağrıldığını belirtin. Şemayı geçmiş olaylarda sınayın ve ayarlayın.
3. **Her olayın başında rolleri atayın.** Bir olay komutanı, bir operasyon lideri ve bir iletişim lideri adlandırın. Küçük ekiplerde bir kişi birden fazla rol tutabilir; bunu yüksek sesle söyleyin.
4. **Düzeltmeyi eşgüdümden ayırın.** Sistemi değiştiren insanlar aynı zamanda soruları yanıtlıyor olmamalıdır. Komutanın eşgüdüm sağlamasına ve iletişim liderinin bilgilendirmesine izin verin.
5. **Canlı bir kayıt tutun.** Zaman damgaları, kararlar ve yapılan değişikliklerle tek bir ortak belge veya kanal kullanın. Devirleri destekler ve postmortem'e malzemesini verir.
6. **Yalnızca yetkili değişikliklere izin verin.** SRE bölümü, bir olay sırasında sistemi yalnızca operasyon ekibinin değiştirmesi gerektiğini söyler. Kimin neyi değiştirebileceğini belirtin ve diğerlerinden komutanla konuşmalarını isteyin.
7. **Bir takvime göre iletişim kurun.** Her ciddiyet için güncelleme aralığı üzerinde anlaşın ve yeni bir şey olmasa bile ona uyun. Sessizlik endişe ve tekrarlanan sorular doğurur.
8. **Açıkça devredin.** Bir komutan veya müdahale eden değiştirildiğinde bunu yüksek sesle söyleyin ve diğer kişinin onaylamasını sağlayın. Belirsiz devirler bağlamı kaybettirir.
9. **Pratik yapın.** Roller ciddi bir kesintiden önce tanıdık olsun diye olay sürecini küçük olaylarda ve tatbikatlarda çalıştırın. İnsanları roller arasında döndürün.
10. **Tetikleyicileriniz karşılandığında suçlamasız bir postmortem yapın.** Olaya karışanlarla birlikte yazın, katkıda bulunan nedenlere ve sistem düzeltmelerine odaklanın ve geniş biçimde paylaşın (aşağıdaki postmortem becerisine bakın).
11. **Eylemleri iş listesi kalemlerine dönüştürün.** Her izleme kalemine bir sahip ve bir tarih verin ve bunları düzenli bir toplantıda gözden geçirin. Gözden geçirilmemiş bir postmortem değişiklik üretmez.
12. **Kanıtı sorun yönetimine iletin.** Tekrarlayan olayları bir sorun kaydına bağlayın; böylece nedenler yalnızca onarılmak yerine ortadan kaldırılır (bkz. Konu 3.3 — Sorun Yönetimi).

## Ekibinizle tartışılacak sorular

**Bir olayın ilk on dakikasında ne yapıyoruz ve kim karar veriyor?**

Son önemli olayı dakika dakika gözden geçirin. Kimin önderlik ettiğini, kimin iletişim kurduğunu ve kimin neyi değiştirdiğini not edin. Birçok ekip, rollerin üzerinde anlaşılmadığını, varsayıldığını görür. Kolaylaştırıcı, olağan liderin yerinde olmaması durumunda ne olacağını sorabilir. Bir sonraki sefer rollerin nasıl atanacağı üzerinde anlaşarak sürdürün.

**Bir şeye ne zaman olay diyoruz ve ne zaman bekliyoruz?**

Geç ilan edilen olaylara örnekler toplayın. İnsanları neyin tuttuğunu sorun: başkalarını rahatsız etmek istememek, belirsizlik veya suçlanma korkusu. SRE bölümünün tetikleyicileriyle karşılaştırın. Bir eşik ve bir olayı yaygara koparmadan ilan etmenin bir yolu üzerinde anlaşın.

**Kullanıcılarımız bir kesinti sırasında neler olduğunu nasıl ve ne sıklıkla öğreniyor?**

Son kesintiye kullanıcının tarafından bakın. Onlara kimin söylediğini, ne söylendiğini ve boşluğun ne kadar sürdüğünü sorun. Çoğu zaman yanıt, uzun bir sessizliği izleyen kısa bir nottur. İletişimin sahibinin kim olması gerektiğini ve ilk mesajın ne söylemesi gerektiğini sorun. Bir şablon ve bir güncelleme ritmi üzerinde anlaşın.

**Son postmortem'imiz neyi değiştirdi ve bunu nasıl biliyoruz?**

Eylemleri, sahiplerini ve durumunu isteyin. Hiçbiri tamamlanmadıysa nedenini sorun: sahip yok, zaman yok ya da belirsiz değer. Postmortem'lerin ekibin ötesinde kimse tarafından okunup okunmadığını öğrenin. Açık eylemleri gözden geçirmek için düzenli bir oturum üzerinde anlaşın.

**İnsanlar neyi yanlış yaptıklarını söylemekte kendilerini güvende hissediyor mu?**

Bu soru suçlamasızlığı sınar. İnsanlardan bir postmortem'de kendi hataları hakkında yazmanın nasıl hissettireceğini anlatmalarını isteyin. Sonuçlardan korkuyu ve suçlamanın gerçekleştiği örnekleri dinleyin. Açıklık talep etmeyin; ekibin ve liderlerin bunu güvenli kılmak için ne yapması gerektiğini sorun. Görünür tek bir adım seçin.

**Nasıl pratik yapıyoruz ve en son ne zaman yaptık?**

Ekibin bir tatbikat veya simüle edilmiş bir olay yürütüp yürütmediğini ve ne öğrendiğini sorun. Hiç yapılmadıysa, geçmiş bir olayı bir saat içinde yeniden oynatmak gibi küçük bir başlangıcı tartışın. SRE bölümü, süreci rutin değişikliklerde ve felaket kurtarma tatbikatlarında çalıştırmaktan söz eder. Bir sonraki çeyrek için birini planlayın.

## Uygulamada: çevik bir ITIL örneği

Bölgesel bir elektrik şirketinin müşteri portalı, hanelerin kesintileri bildirmesine ve faturalarını görmesine olanak tanır. On bir kişilik bir ekip bunu geliştirir ve işletir; dört kişilik bir nöbet çizelgesi vardır. Bir fırtına sırasında bildirim trafiği sıçrar, portal yavaşlar ve ardından çöker. Nöbetçi mühendis bir veritabanı yeniden başlatması dener, ikinci bir mühendis aynı anda bir yapılandırma düzeltmesi dağıtır ve üçüncüsü daha önceki bir sürümü geri alır. Portal üç saat sonra geri gelir ve hiç bilgilendirilmeyen çağrı merkezi binlerce öfkeli çağrıyı karşılamıştır.

Postmortem'de ekip SRE bölümündeki üç tehlikeyi görür: herkes teknik düzeltmeye odaklandı, kimse iletişim kurmadı ve değişiklikler çarpıştı. Tek sayfalık bir olay süreci yazarlar. Herkes bir olay ilan edebilir ve ikinci bir ekibin devreye girmesi, müşteri görünürlüğü veya bir saat ilerleme olmaması ilan etmeyi zorunlu kılar. Nöbetçi mühendis operasyon lideri olur ve bir çizelge daha geniş ekipten bir olay komutanı ile bir iletişim lideri adlandırır. Üretimi yalnızca operasyon lideri değiştirir. İletişim lideri çağrı merkezine ve kontrol odasına her 30 dakikada bir güncelleme gönderir. Ortak bir kanal canlı günlüğü tutar.

Bir sonraki fırtınada portal yine yavaşlar, on dakika içinde bir olay ilan edilir ve hizmet 70 dakikada geri getirilir; çağrı merkezine boyunca güncellemeler gider. Sorunlar kalır. Komutan çizelgesinde tatillerde boşluklar vardır ve ekip bir bağımlılığın, bir kısa mesaj sağlayıcısının, yükseltme iletişim kişisinin olmadığını bulur. Postmortem sahipleri olan iki eylem üretir: çizelgeyi bir yedekle tamamlamak ve sağlayıcıyla bir yükseltme yolu üzerinde anlaşmak. Ekip, fırtına olayının yeni çizelge üyeleri için yeniden oynatılmasını planlar.

## Dört bakış açısı

### Ürün ve teslimat ekipleri

Birçok olayın nedeni ve çözümü teslimat ekipleridir. Nöbet çizelgesine katılın veya ona doğrudan destek verin ve postmortem eylemlerini iş listesi kalemleri olarak ele alın. Sorunları tespit etme ve geri alma araçlarını sürümlerinize yerleştirin. Roller tanıdık olsun diye tatbikatlara katılın.

### Hizmet ve operasyon ekipleri

Süreç operasyon ekiplerine aittir. Kısa ve pratik edilmiş tutun, insanlara harekete geçme yetkisi verin ve başkalarının kullanabileceği kayıtlar tutun. Öğrendiklerinizi teslimat ekipleriyle paylaşın ve dersleri sorun yönetimine ve planlamaya taşıyın.

### Liderlik ve yönetişim

Kültürü liderler belirler. Postmortem isteyin ve okuyun, sorunları bildiren insanları övün ve suçlayacak birini aramayı reddedin. Pratik yapmak ve eylemleri tamamlamak için zamanı koruyun. Kimin para harcayabileceğine veya en yüksek müdahale düzeyini çağırabileceğine karar verin.

### Müşteriler ve kullanıcılar

Müşteriler ve kullanıcılar zamanında, dürüst güncellemelere ve sorunları bildirmenin net bir yoluna ihtiyaç duyar. Sağlayıcınıza bir kesinti sırasında ne bekleyebileceğinizi ve size nasıl haber verileceğini sorun. Bir postmortem sizinle paylaşıldığında, sağlayıcının neyi değiştireceği için okuyun.

## Yaygın başarısızlık biçimleri

- **Rollerin olmaması.** Herkes teknik düzeltme üzerinde çalışır ve kimse eşgüdüm sağlamaz veya iletişim kurmaz. Bunun yerine her seferinde bir olay komutanı, operasyon lideri ve iletişim lideri adlandırın.
- **Geç ilan etmek.** İnsanlar sorun kötüleşene kadar bekler. Bunun yerine düşük, net eşikler belirleyin ve ilan etmeyi olağanlaştırın.
- **Başıboş çalışma.** Birkaç kişi aynı anda sistemi değiştirir. Bunun yerine değişikliklere yalnızca operasyon lideri aracılığıyla izin verin.
- **Sessizlik.** Kullanıcılar ve paydaşlar hiçbir şey duymaz. Bunun yerine bir güncelleme aralığı ve bir şablon üzerinde anlaşın.
- **Suçlama.** Bir postmortem kusurlu kişiyi arar. Bunun yerine sistemde hataya neyin izin verdiğini sorun ve onu düzeltin.
- **Hiçbir yere gitmeyen postmortem'ler.** Eylemlerin sahipleri yoktur. Bunun yerine bunları tarihlerle iş listesine koyun ve düzenli olarak gözden geçirin.
- **Hiç pratik yapmamak.** Sürecin ilk kullanıldığı zaman büyük bir olaydır. Bunun yerine küçük olaylarda ve tatbikatlarda prova yapın.
- **Onarımı çözüm saymak.** Aynı olay geri döner. Bunun yerine tekrarları sorun yönetimine bağlayın ve nedeni düzeltin.

## Olgunluk modeli

| Boyut | Başlangıç | Gelişim | Standartlaştırma | Yönetim | Eşgüdüm |
|---|---|---|---|---|---|
| Tespit ve ilan | Olaylar kullanıcı şikâyetleriyle fark edilir | Bazı uyarılar vardır ve bazı olaylar ilan edilir | Yazılı eşikler ve basit bir ciddiyet şeması tutarlı biçimde kullanılır | Tespit süresi ve ilan süresi izlenir ve azaltılır | Tespit ve ilan ekipler ve tedarikçiler arasında paylaşılır |
| Müdahale ve roller | Müdahale edenler doğaçlama yapar | Bazı ekipler bir lider adlandırır | Roller, devirler ve canlı bir kayıt standarttır | Müdahale süreleri ve rol performansı gözden geçirilir | Müdahale, ortak tatbikatlarla ekipler ve tedarikçiler arasında eşgüdümlenir |
| İletişim | Güncellemeler gelişigüzeldir | Bazı güncellemeler bazı kitlelere gider | Her ciddiyet için güncelleme ritmi ve şablonlar vardır | İletişimin zamanlılığı ölçülür ve kullanıcılara sorulur | İletişim müşteriler ve ortaklarla eşgüdümlenir |
| Öğrenme | Gözden geçirmeler yalnızca en kötü olayları izler | Bazı postmortem'ler yazılır | Suçlamasız postmortem'ler tanımlı tetikleyicileri izler ve eylemler takip edilir | Eylem tamamlama ve tekrarlama ölçülür | Dersler ekipler arasında paylaşılır ve kuruluş genelindeki değişikliği besler |

## Kontrol listesi

- [ ] Bir olayın örneklerle kısa bir tanımına sahibiz.
- [ ] Kullanıcı etkisi örnekleri ve çağrı listeleriyle küçük bir ciddiyet şemamız var.
- [ ] Her olay bir olay komutanı, bir operasyon lideri ve bir iletişim lideri adlandırılarak başlar.
- [ ] Her olay için canlı bir kayıt tutulur.
- [ ] Bir olay sırasında üretimi yalnızca adlandırılmış operasyon lideri değiştirir.
- [ ] Her ciddiyet için güncelleme aralıkları kararlaştırılmıştır.
- [ ] Postmortem tetikleyicileri yazılıdır.
- [ ] Postmortem'ler suçlamasızdır, paylaşılır ve gözden geçirilir.
- [ ] Her postmortem eyleminin bir sahibi ve bir tarihi vardır ve açık eylemler gözden geçirilir.
- [ ] Süreci son altı ayda pratik ettik.

## Yapay zeka istemleri

**Amaç: mevcut uygulamanızdan tek sayfalık bir olay süreci taslağı hazırlamak.**

```text
Help me draft a one-page incident process for a team of [number] people who run [service].

How we handle incidents today: [describe in a few sentences].
Our on-call arrangement: [describe].
Who needs to be told during an incident: [list audiences].
Rules we must follow (contracts, regulations), with source text if you have it: [paste, or write "none known"].

Produce a short process with: what counts as an incident, a simple severity scheme with user-impact examples (leave numeric thresholds as [to be agreed]), the roles and what each does, how to communicate, and when to hold a postmortem. Mark every item that is an assumption. Do not invent obligations. Ask clarifying questions first, and list what you are unsure of.
```

**Amaç: bir olay günlüğünü suçlamasız bir postmortem taslağına dönüştürmek.**

```text
Below is the log of an incident: [paste timestamps, messages, and actions; remove personal data].
Impact as we know it: [describe users affected and for how long, using only facts].

Draft a blameless postmortem with: summary, impact, timeline, how it was detected, how it was mitigated, contributing causes (separate known from suspected), what went well, what went badly, and proposed actions with a suggested type (prevent, detect, respond) but no owners or dates. Describe actions of people neutrally, as roles. Do not invent facts or causes. Mark gaps with [UNKNOWN], and list what you are unsure of.
```

**Amaç: teknik olmayan paydaşlar için bir olay durum güncellemesi yazmak.**

```text
Write a status update for stakeholders who are not technical about this incident.

Facts: what is affected: [describe]; since when: [time]; what we know about the cause: [what is known, or "not yet known"]; what we are doing: [describe]; when the next update will come: [time].

Write under 120 words in plain language. State what we know and what we do not, without guessing at the cause or the time of recovery. Do not promise a resolution time unless I gave one. Offer two versions: one for customers and one for internal staff. List what you are unsure of.
```

**Amaç: küçük bir olay tatbikatı tasarlamak.**

```text
Design a 60-minute incident exercise for [number] people who run [service].

Scenario basis: [describe a past incident or a plausible failure, using only facts you want to use].
Roles to practice: incident commander, operations lead, communications lead.
Constraints: [for example no use of production systems].

Give a timed plan: briefing, the scenario released in three stages, prompts for each role, and a short review with questions on roles, communication, and records. Do not use real production access. Ask clarifying questions first if information is missing, mark assumptions, and list what you are unsure of.
```

## Yapay zeka becerileri

- [incident-response-plan](../../../../skills/incident-response-plan/SKILL.md): ekibiniz için rolleri, eşikleri ve iletişimi belirleyen planı yazmak için kullanın.
- [postmortem](../../../../skills/postmortem/SKILL.md): bir olaydan sonra suçlamasız bir gözden geçirme yürütmek ve eylemleri kaydetmek için kullanın.
- [runbook](../../../../skills/runbook/SKILL.md): bilinen düzeltmeleri müdahale eden için kısa prosedürlere dönüştürmek için kullanın.
- [on-call-rotation](../../../../skills/on-call-rotation/SKILL.md): yedek ve devirleri olan adil bir çizelge tasarlamak için kullanın.
- [crisis-communication-plan](../../../../skills/crisis-communication-plan/SKILL.md): büyük bir kesinti sırasında kullanıcılara, personele ve kamuya ne söyleyeceğinizi planlamak için kullanın.

## Temel kaynaklar

- **Managing Incidents** (Andrew Stribblehill, *Site Reliability Engineering* içinde, Google, sre.google): hizmet ekipleri için olay komutasının en net herkese açık anlatımı.
- **Postmortem Culture: Learning from Failure** (*Site Reliability Engineering*, Google, sre.google): suçlamasız postmortem'ler için gerekçe; tetikleyiciler ve kültür oluşturma fikirleriyle.
- **Incident management** (Wikipedia): BT hizmet yönetimi bölümü olan, çok alanlı bir genel bakış.
- **IT service management** (Wikipedia): olayın tanımı ve olay ele almanın hizmet masasındaki yeri.

## Kaynakça

1. Managing Incidents — Andrew Stribblehill, Google SRE book, sre.google — https://sre.google/sre-book/managing-incidents/
2. Postmortem Culture: Learning from Failure — Google SRE book, sre.google — https://sre.google/sre-book/postmortem-culture/
3. Incident management — Wikipedia — https://en.wikipedia.org/wiki/Incident_management
4. IT service management — Wikipedia — https://en.wikipedia.org/wiki/IT_service_management
5. Incident Command System — Wikipedia — https://en.wikipedia.org/wiki/Incident_Command_System
6. Root cause analysis — Wikipedia — https://en.wikipedia.org/wiki/Root_cause_analysis
7. Site reliability engineering — Wikipedia — https://en.wikipedia.org/wiki/Site_reliability_engineering
8. ITIL — Wikipedia — https://en.wikipedia.org/wiki/ITIL
9. Computer security incident management — Wikipedia — https://en.wikipedia.org/wiki/Computer_security_incident_management
