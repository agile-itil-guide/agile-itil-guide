# Değişiklik Sağlama

**Değişiklik sağlama (change enablement), yararlı değişikliklerin güvenle ve hızla gerçekleşmesine izin vermek için vardır; yazılım teslimat araştırmasından elde edilen kanıt, riskin her değişikliği bir kurula göndermekten çok küçük değişiklikler, akran gözden geçirmesi ve otomatik kontrollerle daha iyi denetlendiğini gösterir.**

## Bu neden önemli

Değişiklik, sürekli teslimat ile hizmet yönetiminin en sık çarpıştığı yerdir. Teslimat ekipleri sık sürüm yayımlamak ister, çünkü küçük ve sık değişiklikleri anlamak ve geri almak daha kolaydır. Operasyon ve yönetişim kesintilerden kaçınmak ve kayıt tutmak ister, çünkü geçmiş değişiklikler hizmetleri bozmuştur. İkisi de haklıdır. Anlaşmazlık genellikle riskin nasıl denetleneceği konusundadır: değişiklikten önce onayla mı, yoksa değişikliğin kalitesi ve toparlanma hızıyla mı.

Uygulamaya ITIL 4'te değişiklik sağlama denir. Yeni ad bir amaç beyanıdır. Amaç yararlı değişikliklerin gerçekleşmesini sağlamaktır; değişiklikleri önlemek değil. Eski ITIL sürümleri uygulamaya değişiklik yönetimi dedi ve ona onaylarda ve takvimlerde güçlü bir rol verdi; birçok ekip bunu bir kapı olarak yaşadı.

Bu konu elde bulunan en iyi kanıtı kullanır: DORA araştırma programının değişiklik onayı ve yazılım teslimat metrikleri hakkındaki rehberliği, programın kendi sayfalarından okunmuştur. DORA'nın sayfaları, ağır dış onayın daha kötü teslimat performansıyla ilişkili olduğunu bildirir. Ayrıca etki büyüklüğü veya istatistiksel ayrıntı vermezler ve altta yatan araştırma için 2019 tarihli bir rapora atıf yaparlar; bu nedenle rehberliği güçlü ama kesin değil olarak görün ve kendi bağlamınızda sınayın. Buradaki ITIL sözcük dağarcığı, bu kılavuzun çerçeve sahibinin metnine karşı kontrol edemediği, yaygın biçimde yayımlanmış anlatımlardan gelir (bkz. Konu 2.2 — ITIL).

## Temel kavramlar

### Değişiklik sağlama ne yapar

**Değişiklik** (change), bir hizmeti etkileyebilecek herhangi bir şeyin eklenmesi, değiştirilmesi veya kaldırılmasıdır. Değişiklik sağlama, değişikliklerin risk yönetilsin ve yararlı değişiklikler ilerlesin diye değerlendirilmesini, yetkilendirilmesini ve zamanlanmasını sağlama uygulamasıdır. Uygulama ayrıca neyin değiştiğinin kaydını tutar; bu, olay müdahalesi için hayati önemdedir, çünkü birçok olay yakın zamandaki bir değişiklikle başlar (bkz. Konu 3.2 — Olay Yönetimi).

### Değişiklik türleri

ITIL 4'ün her biri farklı bir yolu olan üç değişiklik türünü tanıdığı yaygın biçimde anlatılır:

| Tür | Nedir | Tipik yol |
|---|---|---|
| **Standart değişiklik** (standard change) | Belgelenmiş bir prosedürü izleyen, düşük riskli, iyi anlaşılmış bir değişiklik | Önceden yetkilendirilmiştir; kaydedilir, vaka bazında onay yoktur |
| **Normal değişiklik** (normal change) | Değerlendirme ve yetkilendirme gerektiren bir değişiklik | Risk ve etki bakımından değerlendirilir, ardından uygun kişi veya grup tarafından yetkilendirilir |
| **Acil değişiklik** (emergency change) | Örneğin hizmeti geri getirmek için acilen yapılması gereken bir değişiklik | Hızlandırılmış yetkilendirme; sonradan daha kapsamlı gözden geçirme |

Adlar ve kesin tanımlar sahibin yayınlarına karşı kontrol edilmelidir. İlke sabittir: denetim düzeyini riske uydurun.

### Değişiklik yetkilisi

Her değişiklik türü, onu onaylama yetkisi olan birine ihtiyaç duyar. Eski uygulamada bu çoğu zaman bir değişiklik danışma kuruluydu (CAB). DORA sayfası CAB'ı kaldırmaz; ekipler arasında eşgüdüm sağlamak, süreç iyileştirmeyi desteklemek ve pazara çıkış süresine karşı risk gibi iş ödünleşim kararlarını vermek şeklinde "stratejik" bir rol önerir. Rutin değişiklikler için onayın en iyi, otomasyonla desteklenen, geliştirme sırasındaki akran gözden geçirmesiyle uygulandığını söyler.

### DORA onay hakkında ne bildirir

DORA'nın değişiklik onayını kolaylaştırmaya dair sayfası şunları söyler:

- CAB veya üst yönetici imzası gibi ağır dış onay, daha kötü yazılım teslimat performansıyla ilişkilidir.
- Sayfa, daha resmî dış gözden geçirmenin değişiklik başarısızlık oranlarını düşürdüğüne dair hiçbir kanıt bildirmez.
- Ağır onayın teslimatı yavaşlattığını, daha büyük, daha seyrek ve daha riskli sürümlere yol açtığını savunur ve verilerinin bu hipotezi desteklediğini söyler.

Sayfa tuzakları adlandırır: hataları yakalamak için merkezî bir CAB'a güvenmek, riske bakılmaksızın tüm değişikliklere aynı onay sürecini uygulamak, süreci metriklere karşı iyileştirmemek ve üretim kararsızlığına yanıt olarak süreç ve onay eklemek; bunun işleri daha kötü hâle getirme eğiliminde olduğunu söyler. "Kanıt bulunamadı", yararın kanıtının bulunamadığı anlamına gelir; dış gözden geçirmenin hiçbir etkisi olmadığını kanıtlamaz. Sayfa, neyin yüksek riskli bir değişiklik sayılacağına dair ölçüt, belirli düzenlemelere dair rehberlik veya düzenlenen sektörler için geçiş planı vermez.

### Alternatif: denetimi işlem hattında yapmak

DORA, görev ayrımını geliştirme platformunda kaydedilen akran gözden geçirmesiyle karşılamayı ve kötü değişiklikleri erken tespit etmek, önlemek ve düzeltmek için sürekli testi, sürekli tümleştirmeyi ve izlemeyi kullanmayı önerir. Ayrıca platformu, geliştiricilere güvenlik, performans, kararlılık ve kusurlar hakkında hızlı geri bildirim veren bir ürün olarak görmeyi, yüksek riskli değişiklikleri ek inceleme için işaretlemeyi ve normal değişiklik sürecini acil durumları ele alacak kadar hızlı kılmayı önerir. Denetim, işlem hattının ürettiği kanıttadır: kimin gözden geçirdiği, hangi testlerin geçtiği, neyin dağıtıldığı ve nasıl geri alınabileceği.

### Değişikliği ölçmek

DORA'nın yazılım teslimat performans metrikleri sayfası beş ölçüm listeler:

| Ölçüm | Nedir | Grup |
|---|---|---|
| Değişiklik teslim süresi (change lead time) | Bir değişikliğin sürüm denetimine işlenmesinden üretimde dağıtılmasına kadar geçen süre | Verim |
| Dağıtım sıklığı (deployment frequency) | Dağıtımların ne sıklıkta gerçekleştiği | Verim |
| Başarısız dağıtım kurtarma süresi (failed deployment recovery time) | Başarısız olan ve acil müdahale gerektiren bir dağıtımdan toparlanmanın ne kadar sürdüğü | Verim |
| Değişiklik başarısızlık oranı (change fail rate) | Geri alma veya acil yama gibi acil müdahale gerektiren dağıtımların payı | Kararsızlık |
| Dağıtım yeniden iş oranı (deployment rework rate) | Planlanmamış olan ve bir üretim olayından kaynaklanan dağıtımların payı | Kararsızlık |

Sayfa, hız ile kararlılığın bir ödünleşim olmadığını söyler: ölçümler çoğu ekip için ilişkilidir ve en iyi performans gösterenler beşinde de iyidir. Ölçümleri hedef olarak belirlemeye (Goodhart yasası), tek bir metriğe güvenmeye, çok farklı uygulamaları karşılaştırmaya ve diğer ekiplerle yarışmaya karşı uyarır. Ekiplerin kendi geçmiş performanslarına karşı iyileşmesini önerir. Sayfa ölçüt eşikleri veya formüller vermez; bu nedenle kullanmadan önce her ölçümü kendi bağlamınız için tanımlayın (bkz. Konu 5.6 — Metrikler ve Ölçüm).

### Kayıtlar ve yapılandırma görünümü

Bir değişiklik kaydı neyin değiştiğini, nedenini, kimin onayladığını ve ne zaman yapıldığını söylemeli ve ideal olarak etkilenen hizmetlere bağlanmalıdır. Sürüm denetimi, derleme ve dağıtım araçları bunların çoğunu otomatik olarak üretebilir. Değişiklikleri hizmetlerin yapılandırmasına bağlamak, etki çözümlemesini ve olay müdahalesini destekler (bkz. Konu 4.4 — Yapılandırma Yönetimi).

### Değişiklik ve sürüm

Değişiklik sağlama, bir değişikliğin ilerleyip ilerlemeyeceğine karar verir. Sürüm ve dağıtım yönetimi onu üretime ulaştırır (bkz. Konu 3.5 — Sürüm ve Dağıtım Yönetimi). Sürekli teslimatta ikisi uygulamada birleşir; onaylar işlem hattına gömülür.

## İyi uygulamalar

1. **Değişiklikleri riske göre sınıflandırın.** Ölçütleri ve örnekleriyle kısa bir değişiklik türü listesi tanımlayın. Yolu riske uydurun; böylece rutin değişiklikler hızlı olur ve riskli değişiklikler ilgi görür.
2. **Düşük riskli değişiklikleri önceden yetkilendirin.** İyi anlaşılmış, sınanmış ve geri alınabilir değişiklikler için standart bir prosedür üzerinde anlaşın ve vaka bazında onay olmadan ilerlemelerine izin verin. Bunları otomatik olarak kaydedin.
3. **Akran gözden geçirmesini varsayılan onay yapın.** Değişikliklerin birleştirmeden önce ikinci bir kişi tarafından gözden geçirilmesini isteyin ve gözden geçirmeyi geliştirme platformunda kaydedin. Bu, DORA sayfasının anlattığı gibi çoğu değişiklik için görev ayrımını karşılar.
4. **Kontrolleri otomatikleştirin.** Her değişiklikte testleri, güvenlik taramalarını ve politika kontrollerini çalıştırın ve sonuçları kaydın bir parçası yapın. Kanıta dayalı bir onay, bir forma dayalı olandan daha güçlüdür.
5. **Değişiklikleri küçük tutun.** Küçük değişiklikleri gözden geçirmek, sınamak ve geri almak daha kolaydır. Bir değişiklik riskli hissettiriyorsa bölünüp bölünemeyeceğini sorun.
6. **Geri almayı kolay ve prova edilmiş yapın.** Her değişiklik türü için nasıl geri alınacağını bilin ve pratik yapın. Hızla toparlanabilme yeteneği, her arızayı öngörme ihtiyacını azaltır.
7. **Yüksek riskli değişiklikleri işaretleyin.** Ödeme mantığındaki veya paylaşılan altyapıdaki değişiklikler gibi ek gözden geçirmeyi tetikleyen sinyaller tanımlayın. Daha ağır yolu yalnızca onlara uygulayın.
8. **Değişiklik yetkilisine stratejik bir rol verin.** Herhangi bir merkezî kurulu ekipler arasında eşgüdüm sağlamak, çatışmaları çözmek ve iş ödünleşimleri yapmak için kullanın. Onu her değişiklik için bir kontrol noktası olarak kullanmayın.
9. **Acil durumları normal yolla ele alın.** Düzenli süreci, acil değişikliklerin ardından gözden geçirmeyle onu izleyecek kadar hızlı ve güvenilir yapın. Sık kullanılan acil yollar, normal yolun çok yavaş olduğuna işaret eder.
10. **Bir olaydan sonra varsayılan olarak onay eklemeyin.** DORA'nın sayfası, kararsızlığa yanıt olarak süreç eklemenin işleri daha kötü yapma eğiliminde olduğunu söyler. Önce düzeltmenin daha iyi testler mi, daha küçük değişiklikler mi yoksa daha hızlı toparlanma mı olduğunu sorun.
11. **Süreci ölçün.** Teslim süresini, onay için beklemede geçen zamanı, elle onay olmadan geçen değişikliklerin payını ve değişiklik başarısızlık oranını izleyin. Ölçümleri ekipleri sıralamak için değil, iyileştirmek için kullanın.
12. **Süreci açıklayın.** DORA'nın sayfası, mevcut süreci net biçimde iletmenin ve ekiplerin onda yol bulmasına yardımcı olmanın, onu değiştirmeden önce bile daha iyi performansla ilişkili olduğunu not eder. Örneklerle tek sayfalık bir rehber yayımlayın.

## Ekibinizle tartışılacak sorular

**Değişikliklerimizin ne kadarı düşük riskli ve iyi anlaşılmış ve bugün nasıl onaylanıyor?**

Bir aylık değişiklik alıp sınıflandırın. Çoğu ekip büyük çoğunluğun rutin olduğunu görür. Rutin değişikliklerin onay için ne kadar beklediğini ve onaylayanın ne kattığını sorun. Kolaylaştırıcı, onayın başarısız olacak rutin bir değişikliği engellediğini hatırlayan biri olup olmadığını sorabilir. Cevabı, önceden yetkilendirme için ilk adayı belirlemekte kullanın.

**Onay adımımız gerçekte neyi yakalıyor?**

Onayda reddedilen veya geciktirilen son on değişikliği ve nedenlerini listeleyin. Onaya rağmen üretime ulaşan sorunlarla karşılaştırın. Onay az şey yakalıyorsa, aynı sorunları testler veya akran gözden geçirmesi gibi neyin daha erken yakalayacağını sorun. DORA sayfasının, daha resmî dış gözden geçirmenin değişiklik başarısızlık oranlarını düşürdüğüne dair hiçbir kanıt bildirmediğini unutmayın. Denenecek bir değişiklik üzerinde anlaşın.

**Kötü bir değişikliği nasıl ve ne kadar çabuk geri alırız?**

Yakın zamandan bir değişiklik seçin ve geri almayı anlatın. Belirsizse, sınanmamışsa veya elle yapılıyorsa risk budur. Ne kadar süreceğini ve kimin yapacağını sorun. Bu ay bir geri almayı prova etmek üzere anlaşın. Dakikalar içinde toparlanabilen bir ekip daha fazla değişikliği kabul edebilir.

**Değişikliklerimizden hangileri ek inceleme gerektiriyor ve bunları nasıl tanırız?**

Ciddi olaylara neden olan değişikliklerin örneklerini toplayın. Ortak özelliklerine bakın: paylaşılan altyapı, güvenlik kontrolleri, veri taşımaları. Bir değişikliği yüksek riskli olarak işaretleyecek üç sinyal taslağı hazırlayın. İşaretlenen değişiklikleri kimin ve ne kadar hızlı gözden geçirmesi gerektiğini sorun.

**Bir olaydan sonra ne zaman bir kontrol ekledik ve işe yaradı mı?**

Örnekler isteyin. Nelerin eklendiğini, hangi sorunlara yönelik olduğunu ve sorunun yinelenip yinelenmediğini listeleyin. DORA sayfası kararsızlığa yanıt olarak onay eklemeyi bir tuzak olarak adlandırır. Daha iyi testler veya daha küçük değişiklikler gibi farklı bir yanıtın işe yarayıp yaramayacağını tartışın. Bir ders kaydedin.

**Bir denetçi, işlem hattımızdan bir imza yerine hangi kanıtı kabul ederdi?**

Bir denetçiden veya uyum meslektaşından katılmasını isteyin. İşlem hattının zaten ürettiği kanıtı listeleyin: gözden geçirmeler, test sonuçları, dağıtım kayıtları. Neyin eksik olduğunu sorun. Birçok denetçi, güvenilir olduğunda kaydedilmiş akran gözden geçirmesini ve otomatik kanıtı kabul eder. Kontrolün kısa bir tanımı ve bir deneme süresi üzerinde anlaşın.

## Uygulamada: çevik bir ITIL örneği

Bölgesel bir hastanenin BT departmanı, yedi kişilik kurum içi bir ekip tarafından güncellenen bir klinik randevu sistemini destekler. Bir yazım hatası düzeltmesinden bir veritabanı taşımasına kadar her değişiklik haftalık bir değişiklik danışma kuruluna gider. Küçük düzeltmeler sekiz güne kadar bekler. Klinisyenler yakınır ve geliştiriciler kuyruktan kaçınmak için düzeltmeleri daha büyük sürümlerde toplamaya başlamıştır; bu da her sürümü daha riskli yapar.

BT başkanı ve kurul başkanı bir yıllık değişikliği gözden geçirir. Çoğu küçüktü, ikisi olaylara neden olmuştu ve ikisi de kurul tarafından yakalanmamıştı. Üç şeritli bir yaklaşım tasarlarlar. Üzerinde anlaşılan sınırlar içindeki metin ve yapılandırma değişiklikleri gibi, geçen otomatik testleri ve sınanmış bir geri almayı olan standart değişiklikler önceden yetkilendirilir ve otomatik olarak günlüğe kaydedilir. Normal değişiklikler, geliştirme platformunda kaydedilen bir akran gözden geçirmesi ve hasta verisi işlemedeki değişiklikler gibi kısa bir yüksek riskli sinyal listesine karşı bir kontrol gerektirir. Yüksek riskli olarak işaretlenen değişiklikler, haftada iki kez toplanan kurula gider. Acil değişiklikler normal yolu, uygulama sonrası gözden geçirmeyle izler.

Dört ay sonra standart değişiklikler bir gün içinde canlıya çıkar ve kurul eskiden gördüğü hacmin yaklaşık beşte birini görür. Değişiklik başarısızlık oranı artmaz. Sorunlar kalır. İki geliştirici yüksek riskli sinyalleri tutarsız uygular ve işaretlenen bir değişiklik kurula geç ulaşmıştır; iç denetim ise akran gözden geçirmelerinin lastik damga olmadığına dair kanıt ister. Ekip sinyallerin örneklerini yazar, kıdemli bir mühendis tarafından akran gözden geçirmelerinin örnekleme gözden geçirmesini ekler ve kanıtı bir sonraki üç aylık toplantıda gözden geçirmek üzere denetimle anlaşır.

## Dört bakış açısı

### Ürün ve teslimat ekipleri

Denetimin çoğunu teslimat ekipleri taşır: gözden geçirme, testler, küçük değişiklikler ve geri alma. Bunları işlem hattına yerleştirin ve kanıtı görünür kılın. Değişiklikleri küçük tutun ve operasyona neyin geldiğini söyleyin. Değişiklik sürecini yalnızca izin almak için değil, risk bilgisini paylaşmak için de bir yer olarak kullanın.

### Hizmet ve operasyon ekipleri

Operasyon ekipleri hangi değişikliklerin hizmetlere zarar verdiğini bilir. Bu bilgiyi ek gözden geçirme için sinyaller olarak paylaşın ve onları erken yakalayan kontroller oluşturmaya yardım edin. Düşük riskli değişiklikler için daha hafif yolları destekleyin ve olay müdahalesini hızlandıran kayıtları tutun.

### Liderlik ve yönetişim

Kuruluşun ne kadar onay gerektireceğine liderler karar verir. DORA rehberliği, her değişiklikte imza değil, denetim kanıtı istemeyi önerir. Teslim süresinin ve değişiklik başarısızlık oranının ölçülmesini destekleyin ve nedenleri incelemeden olaylardan sonra süreç eklemekten kaçının. Denetimle hangi kanıtın kabul edilebilir olduğu konusunda anlaşın.

### Müşteriler ve kullanıcılar

Müşteriler ve kullanıcılar sık küçük iyileştirmelerden ve daha az büyük kesintiden yararlanır. Sizi etkileyen değişiklikler hakkında önceden, sade bir dille bilgilendirilmeyi bekleyin. Dondurma dönemleri gibi özel ihtiyaçlarınız varsa, planlanabilmeleri için sağlayıcıya erkenden söyleyin.

## Yaygın başarısızlık biçimleri

- **Her değişiklik için tek yol.** Rutin değişiklikler riskli olanların arkasında kuyruğa girer. Bunun yerine riske göre sınıflandırın ve her sınıfa kendi yolunu verin.
- **Tek denetim olarak onay.** Bir imza kalitenin yerini tutar. Bunun yerine testleri, gözden geçirmeyi ve geri almayı işlem hattına yerleştirin.
- **Değerlendiremediğini gözden geçiren bir kurul.** Üyeler anlamadıkları değişiklikleri onaylar. Bunun yerine değişiklikleri bilgisi olan kişilere gönderin ve kurulu eşgüdüm için kullanın.
- **Kuyruktan kaçınmak için toplulaştırma.** Ekipler değişiklikleri birleştirir ve her sürümü daha riskli yapar. Bunun yerine kuyruğu küçük değişikliklerin kolay yol olacağı kadar kısa tutun.
- **Her olaydan sonra kontrol eklemek.** Süreç büyür ve hız düşer. Bunun yerine nedeni arayın ve testler, daha küçük değişiklikler veya daha hızlı toparlanmayla düzeltin.
- **Lastik damga akran gözden geçirmesi.** Gözden geçirmeler biçimsel ama yüzeyseldir. Bunun yerine gözden geçirmelerden örnek alın, iyi olanların örneklerini paylaşın ve değişiklikleri gözden geçirilebilecek kadar küçük tutun.
- **Geri alma olmaması.** Değişiklikler geri alınamaz. Bunun yerine her değişiklik türü için bir geri alma gerektirin ve prova edin.
- **Metrikleri manipüle etmek.** Ekipler iyi görünmek için değişiklikleri böler veya başarısızlıkları gizler. Bunun yerine birkaç ölçüm kullanın, birlikte gözden geçirin ve zaman içinde iyileşmeye odaklanın.

## Olgunluk modeli

| Boyut | Başlangıç | Gelişim | Standartlaştırma | Yönetim | Eşgüdüm |
|---|---|---|---|---|---|
| Sınıflandırma ve yollar | Tüm değişiklikler tek bir yolu izler ya da hiçbirini izlemez | Bazı ekiplerin basit değişiklikler için hızlı bir yolu vardır | Ölçütleri ve ayrı yolları olan değişiklik türleri standarttır | Yola göre değişiklik payı ve bekleme süreleri ölçülür ve ayarlanır | Yollar ortak kanıta dayanarak ekipler arasında ayarlanır |
| Onay ve kanıt | Onay imzayla yapılır ya da kaydedilmez | Bazı değişiklikler akran gözden geçirmesinden geçer | Akran gözden geçirmesi ve otomatik kontroller çoğu değişiklik için kaydedilir | Gözden geçirme kalitesi ve kanıt örneklenir ve iyileştirilir | Kanıt denetime ve ortaklara otomatik olarak akar |
| Toparlanma | Geri alma gelişigüzeldir | Bazı değişikliklerin geri alma adımları vardır | Geri alma her değişiklik türü için tanımlanır ve prova edilir | Toparlanma süresi ölçülür ve azaltılır | Toparlanma uygulamaları ekipler ve tedarikçiler arasında paylaşılır ve sınanır |
| Ölçüm ve iyileştirme | Az ölçüm | Bazı ekipler teslim süresini izler | Teslim süresi, sıklık, başarısızlık oranı ve toparlanma süresi hizmet başına izlenir | Ölçümler planlı iyileştirmeleri yönlendirir ve hedef olarak kullanılmaz | Ekipler birbirlerinin ölçümlerinden öğrenir ve kuruluş genelinde iyileştirir |

## Kontrol listesi

- [ ] Ölçütleri ve örnekleriyle değişiklik türleri tanımladık.
- [ ] Düşük riskli, iyi anlaşılmış değişiklikler önceden yetkilendirilmiş ve otomatik olarak kaydediliyor.
- [ ] Normal değişiklikler için akran gözden geçirmesi geliştirme platformunda kaydediliyor.
- [ ] Her değişiklikte otomatik testler ve kontroller çalışıyor.
- [ ] Her değişiklik türünün prova edilmiş bir geri alması var.
- [ ] Yüksek riskli değişiklikleri ek inceleme için işaretleyen sinyallerimiz var.
- [ ] Herhangi bir merkezî kurulun eşgüdüm ve ödünleşimlerde net bir rolü var.
- [ ] Her hizmet için değişiklik teslim süresini, dağıtım sıklığını, başarısız dağıtım kurtarma süresini ve değişiklik başarısızlık oranını izliyoruz.
- [ ] Denetçilerimiz imza yerine hangi kanıtı kabul ettiklerini söyledi.
- [ ] Örneklerle değişiklik sürecine dair tek sayfalık bir rehberimiz var.

## Yapay zeka istemleri

**Amaç: geçen ayın değişikliklerini risk ve onay yoluna göre sınıflandırmak.**

```text
Below is a list of the changes we made last month: [paste one line per change with a short description, who reviewed it, how long it waited for approval, and whether it caused an incident; remove personal data].

Help me sort them into three groups: routine and low risk, needs normal assessment, and needs extra scrutiny. For each group, say what features of the changes in my list led you to the grouping, using only the text. Calculate the share in each group and the average wait for approval from my numbers only. Suggest which routine changes might be pre-authorized and what safeguards I would want first. Do not guess at risks beyond what I wrote. List what you are unsure of.
```

**Amaç: standart bir değişiklik prosedürü yazmak.**

```text
Help me write a procedure for a standard (pre-authorized) change: [name the change, for example "update a configuration value within agreed limits"].

How it is done today, step by step: [paste].
Checks that exist: [tests, scans, reviews].
How to undo it: [describe, or write "unknown"].
Who owns the procedure: [role].

Write a one-page procedure with: when it applies, the criteria that make a change standard, the steps, the checks that must pass, how it is recorded, how to undo it, and when to treat it as a normal change instead. Mark every statement you added as an assumption. Do not claim any rule requires something unless I pasted its text. Ask clarifying questions first, and list what you are unsure of.
```

**Amaç: işlem hattımızın ürettiği kanıtı bir denetçiyle tartışmaya hazırlanmak.**

```text
An auditor asks how we authorize changes. Our pipeline does the following: [describe code review, tests, scans, deployment record, who can approve, and where records are kept].

The auditor's concern in their words: [paste, or write "unknown"].
Rules we know apply, with source text if you have it: [paste, or write "none known"].

Make a table of what evidence each step produces, where it is stored, who can alter it, and what gaps the auditor may notice. Suggest three lightweight ways to strengthen the weakest points. Do not state that any standard requires something unless I pasted its text. Mark assumptions, and list what you are unsure of.
```

**Amaç: daha hafif onayın bir denemesini tasarlamak.**

```text
Design a three-month trial of lighter approval for [service].

Current process: [describe].
Change volume and types last quarter: [paste counts from your records].
Measures we already have: [list, for example lead time and change fail rate].
Concerns from audit or operations: [list].

Propose: which change types to include, safeguards, what to measure and how often (without inventing targets), what would make us stop or pause the trial, and how to report results. Ask clarifying questions first, mark assumptions, and list what you are unsure of.
```

## Yapay zeka becerileri

- [change-request](../../../../skills/change-request/SKILL.md): operasyonun ve denetçilerin ihtiyaç duyduğunu taşıyan değişiklik kayıtları taslağı hazırlamak için kullanın.
- [enterprise-change-management](../../../../skills/enterprise-change-management/SKILL.md): bir değişiklik kurumsal olduğunda ve sistemlerin yanı sıra insanlar için de planlama gerektirdiğinde kullanın.
- [release-notes](../../../../skills/release-notes/SKILL.md): kullanıcılara ve hizmet masasına bir değişikliğin ne yaptığını anlatmak için kullanın.
- [two-way-door-decisions](../../../../skills/two-way-door-decisions/SKILL.md): hızlıca alınabilecek geri döndürülebilir kararları daha fazla özen gerektiren geri döndürülemez olanlardan ayırmak için kullanın.
- [risk-register](../../../../skills/risk-register/SKILL.md): değişikliğin getirdiği riskleri ve nasıl denetlendiklerini kaydetmek ve gözden geçirmek için kullanın.

## Temel kaynaklar

- **Streamlining change approval** (DORA, dora.dev): araştırma programının akran gözden geçirmesi, otomasyon ve bir değişiklik kurulunun rolü hakkındaki rehberliği.
- **DORA's software delivery performance metrics** (dora.dev): değişiklik teslim süresi, dağıtım sıklığı, toparlanma süresi, değişiklik başarısızlık oranı ve yeniden iş oranı için tanımlar ve uyarılar.
- **ITIL** (Wikipedia): ITIL sürümleri ve ITIL 4'e geçiş hakkında arka plan.
- **Continuous delivery** (Wikipedia): küçük, sık değişiklikleri güvenli kılan uygulamalar hakkında arka plan.

## Kaynakça

1. Streamlining change approval — DORA, dora.dev — https://dora.dev/capabilities/streamlining-change-approval/
2. DORA's software delivery performance metrics — DORA, dora.dev — https://dora.dev/guides/dora-metrics-four-keys/
3. ITIL — Wikipedia — https://en.wikipedia.org/wiki/ITIL
4. Continuous delivery — Wikipedia — https://en.wikipedia.org/wiki/Continuous_delivery
5. Change management — Wikipedia — https://en.wikipedia.org/wiki/Change_management
6. DevOps — Wikipedia — https://en.wikipedia.org/wiki/DevOps
7. Separation of duties — Wikipedia — https://en.wikipedia.org/wiki/Separation_of_duties
8. Version control — Wikipedia — https://en.wikipedia.org/wiki/Version_control
9. Goodhart's law — Wikipedia — https://en.wikipedia.org/wiki/Goodhart%27s_law
