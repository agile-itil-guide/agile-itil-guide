# Teslimat Tahmini ve Planlama Metrikleri

**Teslimat tahmini ve planlama metrikleri, bir ekibin işin ne zaman bitmesinin olası olduğunu ve ne kadarını üstlenebileceğini dürüst aralıklarla söylemesini sağlar; bunu, biten işin sürekli akışını ve ekibin kapasitesini izleyerek yapar ve planlı iş ile kesintiyle gelen iş birlikte sayıldığında hizmet ekipleri için de işe yarar.**

## Bu neden önemli

Çevik ekipler sürekli yazılım teslimini hedefler ve bu teslime bağlı olan herkes aynı soruları sorar: bu ne zaman bitecek, ekip ne kadarını üstlenebilir ve acil bir şey geldiğinde ne olur? Bu sorulara kanıtla yanıt veremeyen bir ekip, tutamayacağı sözlere sığınır ve ona bağlı olanlar her tarihe güvenmemeyi öğrenir.

Hizmet işleten bir ekip bunu çoğu ekipten daha keskin hisseder. Planlı iyileştirme işi, hizmet talepleri ve olaylar aynı insanları paylaşır. Plansız kısmı yok sayan bir plan, bir olayın geldiği ilk haftada başarısız olur. Ekibin kendi geçmişinden gelen ve aralığını belirten bir tahmin, umuttan gelen bir tarihten gerçeklikle karşılaşmaya daha iyi dayanır.

Bu konu, tahminin biten işin akışından nasıl yapılacağını, ekip kapasitesi etrafında nasıl plan yapılacağını ve hangi planlama metriklerinin yardım ettiğini ya da yanılttığını anlatır. Scrum, sprintler ve hız (velocity) planlamanın bir yoludur; sona yakın kısa bir bölüm bunları kullanan ekipler için ele alır. Buradaki ölçüler Konu 1.5 — Kanban'daki akış ölçülerine ve Konu 5.6 — Metrikler ve Ölçüm'deki daha geniş ölçüm kılavuzuna dayanır.

## Temel kavramlar

### Sözlerden değil, akıştan tahmin edin

Tahmin, geçmişten gelen kanıta dayanan ve belirsizlik taşıyan, gelecek hakkında bir ifadedir. Kanban Guide, hizmet seviyesi beklentisini (service level expectation), geçmiş çevrim sürelerine dayanarak bir iş öğesinin iş akışından geçmesinin ne kadar süreceğine dair bir tahmin olarak tanımlar ve bunun bir anlaşma olmadığını söyler. Bu tanım, tüm teslimat tahminleri için iyi bir modeldir: gerçek geçmişi kullanın, neyi kapsadığını söyleyin ve ölçtüğünüzden fazlasını vaat etmeyin (bkz. Konu 1.5 — Kanban).

İki tür tahmin yaygındır:

- **Bir öğe ne kadar sürecek?** Benzer biten öğelerin ne kadar sürdüğüne bakın ve bir aralık ya da "bu türden öğelerin çoğu belirli bir gün sayısı içinde biter" gibi bir ifade verin.
- **Bir tarihe kadar ne kadarını bitireceğiz ya da bir öğe kümesi ne zaman bitecek?** Ekibin bir dönemde genellikle kaç öğe bitirdiğine bakın ve bu aralığı kalan işe uygulayın.

### Bir tahminin arkasındaki akış ölçüleri

Kanban Guide dört ölçü tanımlar ve bunlar teslimat tahmininin ham maddesidir:

| Ölçü | Size ne söyler | Tahmini nasıl besler |
|---|---|---|
| **Çevrim süresi (cycle time)** | Biten bir öğenin başından sonuna ne kadar sürdüğü | Yakın tarihli çevrim sürelerinin dağılımı, yeni bir öğenin ne kadar süreceğine dair bir aralık verir |
| **Çıktı hızı (throughput)** | Bir dönemde kaç öğenin bittiği | Yakın tarihli çıktı hızı aralığı, gelecek bir dönemde ne kadarının biteceğine dair bir aralık verir |
| **Süren iş (WIP)** | Kaç öğenin başlatılıp bitirilmediği | Çok fazla WIP çevrim sürelerini uzatır ve her tahmini daha az güvenilir kılar |
| **İş öğesi yaşı (work item age)** | Bitmemiş bir öğenin ne kadar süredir sürdüğü | Henüz harekete geçecek zaman varken, çoğu bitmiş öğeden daha yaşlı olan öğeleri gösterir |

Kılavuz, ekiplerin bu ölçüleri yeniden adlandırabileceğini ve yararlı olan yerde başkalarını eklemesi gerektiğini, ölçülerin yalnızca ekibin çalışma biçimini bilgilendirdiklerinde önemli olduğunu not eder. Yalnızca ortalamaları değil, yüzdelikleri (percentile) ve aralıkları kullanın; çünkü uzun kuyruklar ortalamalarda saklanır (bkz. Konu 5.6 — Metrikler ve Ölçüm).

### Basit bir tahmin yöntemi

Bir ekip özel araçlar olmadan tahmin yapabilir:

1. Son sekiz ila on iki haftanın ya da benzer dönemlerin her biri için çıktı hızını gerçek biten öğelerden toplayın.
2. Bu rakamların en düşüğünü, tipik olanını ve en yükseğini alın.
3. Kalan öğe sayısını her rakama bölerek bitirmek için gereken dönem aralığını elde edin.
4. Aralığı, geldiği veriyi ve onu neyin değiştireceğini, örneğin yeni işi, bir ekip değişikliğini ya da bir bağımlılığı belirtin.

Bu bir standart değil, başparmak kuralıdır. Gelecekteki işin geçmiş işe benzediğini ve öğelerin kabaca benzer boyutta olduğunu varsayar. Bu yanlış olduğunda bunu söyleyin ve aralığı daha geniş ele alın. Konu 3.11 — Erişilebilirlik, Kapasite ve Performans'ın talep tahminleri için önerdiği gibi, her tahmini olanlarla karşılaştırın ve yöntemi ayarlayın.

### Ekip kapasitesi

Kapasite, bir ekibin bir dönemde ne kadar işi üstlenebileceğidir. Bir teslimat ekibi için bu, kişi sayısının dönemdeki günlerle çarpımı değildir. İzinler, destek görevleri, toplantılar ve plansız iş, planlı öğelere ayrılabilecek miktarı azaltır. Yararlı bir kapasite ifadesi, kişileri ve mevcut günleri listeler, sonra son birkaç dönemin gösterdiğine dayanarak plansız iş için ayrılan payı çıkarır.

Kapasite planlama becerisi ve Konu 3.11 — Erişilebilirlik, Kapasite ve Performans, hizmetler ve altyapı için kapasiteyi anlatır. Aynı mantık bir ekip için de geçerlidir: aralıklarla planlayın, olanlarla karşılaştırın ve gerçekler değiştiğinde planı yeniden gözden geçirin.

### Planlı ve plansız iş birlikte

Hizmet ekipleri olaylar, acil talepler ve kimsenin takvime koymadığı değişiklikler alır. Bunlar sayılmazsa planlı iş tahmini fazla iyimser olur. Plansız işe kendi öğe türlerini verin, kaç tanesinin geldiğini ve ne kadar sürdüğünü sayın ve veriyi planlı işin yanında tutun. Bu aynı zamanda Ürün Sahibine (Product Owner) ya da hizmet sahibine, hangi tekrarlayan olayların kapasiteyi tükettiğine dair kanıt verir; bu da nedenleri düzeltme kararlarını destekler (bkz. Konu 3.3 — Sorun Yönetimi).

### Sürekli teslimat akışı ve sürüm ritmi

Sürekli teslim eden ekipler, bir planlama döneminin sonunu beklemek yerine, hazır olduklarında küçük değişiklikleri yayımlar. Bu, bitirmek ile teslim etmek arasındaki süreyi kısaltır ve tahminleri kontrol etmeyi kolaylaştırır: biten her öğe bir veri noktasıdır. Değişiklikler yine de kuruluşun değişiklik sağlama yaklaşımını izler ve önceden yetkilendirilmiş standart değişiklikler burada yardımcı olur (bkz. Konu 3.4 — Değişiklik Sağlama ve Konu 3.5 — Sürüm ve Dağıtım Yönetimi).

### Scrum, sprintler ve hız kullanıyorsanız

Bazı ekipler sabit uzunlukta döngülerle planlar. Ken Schwaber ve Jeff Sutherland'ın 2020 tarihli Scrum Guide'ı, Scrum'ı karmaşık sorunlara uyarlanabilir çözümler için hafif bir çerçeve olarak tanımlar. Etkinlikleri, bir ay ya da daha kısa bir zaman dilimi olan Sprint içinde gerçekleşir. Bu bölüm, onları kullanıyorsa bir ekibin ihtiyaç duyduğu asgariyi kapsar; bir ekibin çalışma biçimini değiştirmeden önce kılavuzun kendisini okuyun.

- **Sprint ve Sprint Goal:** Sprint zaman dilimidir ve Sprint Goal onun tek hedefidir. Ekip dışından birinin anlayabileceği bir hedef, bir bilet listesinden daha iyi yön verir.
- **Product Backlog, Product Owner ve Scrum Master:** Product Backlog, ürünün neye ihtiyaç duyduğunun sıralı bir listesidir. Product Owner, sırasından sorumlu tek kişidir ve Scrum Master, Scrum'ın kurulmasından ve ekibin onu uygulamasına yardım etmekten sorumludur.
- **Increment ve Definition of Done:** Increment, Ürün Hedefine doğru kullanılabilir, doğrulanmış bir adımdır ve Definition of Done, işin sayılması için karşılaması gereken kalite standardıdır. Bir hizmet ekibi buna izleme, bir çalışma kılavuzu ve sınanmış bir geri almayı dahil edebilir.
- **Etkinlikler:** Sprint Planning, Daily Scrum, Sprint Review ve Sprint Retrospective. Retrospektif, ekibin nasıl çalıştığını incelediği ve iyileştirmeleri planladığı yerdir (bkz. Konu 6.1 — Ekip Sohbetleri).
- **Hız (velocity):** bazı ekiplerin ne kadar iş alacaklarını planlamak için kullandığı, tahmine dayalı bir rakam. Yalnızca ekibin kendi planlaması için kullanın. Hedef haline gelirse ekipler tahminleri şişirir; bu yüzden biten öğeleri sayan akış ölçülerini ve sonuç ölçülerini tercih edin.

Kılavuz, Scrum'ın tam bir yöntem değil, bir çerçeve olduğunu söyler. Olay müdahalesini, hizmet seviyelerini ya da değişiklik sürecini kapsamaz ve yalnızca parçalarını kullanmak sonucu Scrum yapmaz. Uyarlarsanız, farkı dürüstçe adlandırın. Scrum etkinlikleri ile Kanban akışının bir karışımına bazen [Scrumban](https://en.wikipedia.org/wiki/Scrumban) denir.

## İyi uygulamalar

1. **Kendi geçmişinizden tahmin edin.** Yakın tarihli biten öğelerin çevrim sürelerini ve çıktı hızını kullanın ve verinin kapsadığı dönemi belirtin. Başka bir ekipten rakam ödünç almayın.
2. **Tek bir tarih değil, bir aralık verin.** Düşük, tipik ve yüksek bir durum gösterin ve sonucu neyin kaydıracağını söyleyin. Aralığı olmayan bir tarih, sahip olmadığınız bir kesinliği vaat eder.
3. **Plansız işi sayın.** Olayları, acil talepleri ve kesintileri kendi türleriyle iş öğeleri olarak kaydedin. Kaçının geldiğini ve ne kadar sürdüğünü ölçün.
4. **Kapasiteyi veriden belirleyin.** Kişileri ve mevcut günleri listeleyin, izinleri ve destek görevlerini çıkarın ve yakın tarihli dönemlere dayanarak plansız iş için bir pay ayırın. Payı düzenli olarak gözden geçirin.
5. **Süren işi sınırlayın.** Çok fazla başlatılmış iş çevrim sürelerini uzatır ve her tahmini zayıflatır. Bir sınır koyun ve veriler değiştiğinde gözden geçirin (bkz. Konu 1.5 — Kanban).
6. **İş öğesi yaşını her gün izleyin.** Yaş, henüz harekete geçecek zaman varken bitmemiş öğelerdeki sorunu gösterir. Önce en eski öğeleri gözden geçirin.
7. **Yüzdelikleri ve dağılımları kullanın.** Bir türün öğelerinin çoğunun belirli bir gün sayısı içinde bittiğini söyleyin ve yavaş kuyruğu gösterin. Ortalamalar onu gizler.
8. **Tahminleri gerçekleşenlerle karşılaştırın.** Her dönemden sonra neyin tahmin edildiğini ve neyin olduğunu kaydedin. Yalnızca sayıyı değil, yöntemi ayarlayın.
9. **Tahminleri planlama için tutun, yargılamak için değil.** Ekip öğeleri tahmin ediyorsa, rakamları kendi planlaması için kullanın ve kişileri ya da ekipleri bunlara göre sıralamayın (bkz. Konu 5.6 — Metrikler ve Ölçüm).
10. **Tahminleri onlara bağlı olan insanlara görünür kılın.** Aralığı ve varsayımları müşteriler ve paydaşlarla paylaşın ve gerçekler değiştiğinde güncelleyin.
11. **İyileştirme işini aynı akışa getirin.** Sorun düzeltmelerini, izleme işini ve otomasyonu özelliklerin yanına koyun; böylece ödünleşimler görünür olur (bkz. Konu 3.15 — Sürekli İyileştirme).
12. **Sprint ve hız kullanıyorsanız, onları küçük ve dürüst tutun.** Scrum'ın hangi kısımlarını izlediğiniz konusunda anlaşın, farkı adlandırın ve kesintiler baskınsa akış temelli bir yaklaşımı deneyin.

## Ekibinizle tartışılacak sorular

**Bugün "bu ne zaman bitecek?" sorusuna nasıl yanıt veriyoruz ve yanıt neye dayanıyor?**

Ekibin verdiği son üç yanıtı ve her birinin neye dayandığını isteyin. Bunları olanlarla karşılaştırın. Ekipler genellikle tarihlerin umuttan ya da en kıdemli kişinin görüşünden geldiğini bulur. Ekibin bunun yerine hangi geçmişi kullanabileceğini sorarak devam edin.

**Zamanımızın ne kadarı kimsenin planlamadığı işe gidiyor ve bunu veriden biliyor muyuz?**

Son birkaç hafta boyunca planlı öğeleri, acil talepleri ve olayları sayın. Kolaylaştırıcı payın sabit mi yoksa mevsime göre değişken mi olduğunu ve bir kesintinin planlı işe ne zaman üstün geldiğine kimin karar verdiğini sorabilir. Bunu bundan sonra nasıl kaydedeceğiniz konusunda anlaşın.

**Çevrim sürelerimiz neye benziyor ve bir müşteri tipik bir talebin ne kadar sürdüğünü sorsa ne söylerdik?**

Son biten öğelerin çevrim sürelerini çizin ya da listeleyin. Çoğunun ne kadar sürdüğünü, en yavaşların ne kadar sürdüğünü ve yavaş olanları neyin açıkladığını sorun. Bu geçmişe dayanan bir hizmet seviyesi beklentisinin adil olup olmayacağını ve kimin duyması gerektiğini tartışın.

**Mevcut öğelerimizden hangileri zaten çoğu biten öğeden daha yaşlı?**

En eski açık öğelere bakın. Her birinin neden takıldığını, kimin engeli kaldırabileceğini ve ekibin bugün ne yapacağını sorun. Ekibin yaşı ne sıklıkla gözden geçireceğine karar vererek bitirin.

**Tahminimiz en son ne zaman yanlış çıktı ve sonrasında ne değiştirdik?**

Yakın tarihli bir örnek, tahmin ve sonucu isteyin. Tahminin neyi kaçırdığına bakın: plansız iş, bir bağımlılık ya da beklenenden büyük öğeler. Yöntemde tek bir değişiklik ve ekibin bunu nasıl kontrol edeceği konusunda anlaşın.

**Sprint ya da hız kullanıyorsak, bunlar bizim için ne yapıyor ve bırakırsak neyi kaybederiz?**

Her birinin hangi sorunu çözdüğünü dürüstçe sorun. Daha iyi odaklanma ya da daha net hedefler gibi kanıtı ve şişirilmiş tahminler ya da göz ardı edilen kesintiler gibi zararı arayın. Kolaylaştırıcı, yararlı kısımlar olan geri bildirim döngülerini ortadan kaldıran her değişikliğe dikkat etmelidir. Bir deney ve sonuçların nasıl karşılaştırılacağı konusunda anlaşın.

## Uygulamada: çevik bir ITIL örneği

Bölgesel bir hastanenin BT departmanında, hasta randevu uygulamasını sürdüren yedi kişilik bir ekip var. Klinik yöneticileri tarih istiyor ve ekip veriyor. Tarihlerin çoğu kaçırılıyor; çünkü servislerden gelen olaylar, kliniklerden gelen talepler ve güvenlik yamaları gelmeye devam ediyor ve ekip günlerinin çoğunu onlarla geçiriyor.

Ekip lideri her öğeyi, planlı olsun olmasın, başlangıç ve bitiş tarihleriyle kaydetmeye başlar. Sekiz hafta sonra veriler, ekibin zamanının yaklaşık yarısının plansız işe gittiğini ve planlı öğelerin çoğunun iki haftadan kısa sürede bittiğini, ancak başka bir ekibi bekleyen öğelerden oluşan uzun bir kuyruk olduğunu gösterir. Ekip üç değişiklik üzerinde anlaşır. Her tahmini, yakın tarihli çıktı hızı ve çevrim sürelerini kullanarak bir aralık olarak belirtecek. Kapasitesinin yarısını plansız iş için ayıracak ve yalnızca kalanına karşı plan yapacak. En eski açık öğeleri her sabah gözden geçirecek.

Sonraki iki ayda tahminler çoğunlukla doğru çıkar ve artık bir aralık ve varsayımlarını gören klinik yöneticileri bunun etrafında plan yapar. Bir klinik operasyon yöneticisi olan hizmet sahibi, hangi tekrarlayan olayların kapasiteyi tükettiğini görebilir ve tekrarlayan bir randevu eşitleme hatasının düzeltmesinin önceliğini yükseltir; hata durur. Zorluklar kalır. Büyük bir olay yine de bazı işleri öteler ve eski düzenin hızlı yanıtlarını seven yöneticiler aralıkları daha az tatmin edici bulur. Ekip, tahmin her kaydığında onlara neyin değiştiğini söylemeyi ve bir sonraki gözden geçirmede yaklaşımını iyileştirme işi için sabit döngülü bir yöntemle karşılaştırmayı kabul eder.

## Dört bakış açısı

### Ürün ve teslimat ekipleri

Teslimat ekipleri en çok kendi akış verileriyle tahmin yapmaktan kazanır. İşi başlarken ve biterken kaydedin, süren işi sınırlayın ve küçük değişiklikleri sürekli yayımlayın. Aralığı bekleyen insanlarla paylaşın ve varsa Definition of Done'ı, bir sürümü desteklenebilir kılan operasyonel işi de içerecek şekilde kullanın.

### Hizmet ve operasyon ekipleri

Operasyon ekipleri, tahminlerin başarısız olmasına yol açan plansız işin sahibidir. Olayları, talepleri ve değişiklikleri iş öğeleri olarak kaydedin ve tekrarlayan kalıpları paylaşın ki işin sırasını etkilesinler. Müşterilerle gerçekçi beklentiler belirlemek için çevrim süresi verilerini kullanın ve kapasitenin ne kadarının planlı iyileştirmeye gittiği konusunda açık olun.

### Liderlik ve yönetişim

Liderler, durum raporlarından çok tahmin aralıklarından ve akış ölçülerinden daha dürüst bir tablo elde eder. Varsayımlarıyla birlikte aralıkları, zaman içinde tahmin doğruluğunu ve ekibin verilere dayanarak neyi değiştirdiğini isteyin. Tek tek rakamları hedeflemekten kaçının; bu manipülasyon üretir ve gerçekler değiştiğinde tahminin de değişeceğini kabul edin.

### Müşteriler ve kullanıcılar

Müşteriler ve kullanıcılar daha net beklentilerden ve daha az kaçırılan tarihten yararlanır. Ekipten talep türünüz için beklenen süreyi sorun ve bunun geçmişe dayanmasını bekleyin. Talebiniz aciliyse nedenini sormalarını bekleyin; çünkü onu öne almak herkesin işini etkiler.

## Yaygın başarısızlık biçimleri

- **Umuttan tarih vaat etmek.** Tarihler görüşten gelir ve kaçırılır. Bunun yerine, yakın tarihli biten öğelerden tahmin edin ve aralığı gösterin.
- **Plansız işi göz ardı etmek.** Kesintiler planı her dönem bozar. Bunun yerine, onları iş öğesi olarak sayın ve veriye dayanarak kapasite ayırın.
- **Tek sayılı tahminler.** Tek bir tarih belirsizliği gizler. Bunun yerine, varsayımlarla birlikte düşük, tipik ve yüksek bir durum verin.
- **Yalnızca ortalama kullanmak.** Yavaş öğelerin uzun kuyruğu gizlenir. Bunun yerine, yüzdelikleri ve dağılımları kullanın.
- **Çok fazla başlamak.** Yüksek süren iş her çevrim süresini uzatır. Bunun yerine, onu sınırlayın ve başlamadan önce bitirin.
- **Hızı ya da çıktı hızını performans hedefi olarak kullanmak.** Ekipler iyi görünmek için tahminleri şişirir ya da öğeleri böler. Bunun yerine, rakamları planlama için kullanın ve sonuçlara göre yargılayın (bkz. Konu 5.6 — Metrikler ve Ölçüm).
- **Tahmini hiç kontrol etmemek.** Yöntem hiç iyileşmez. Bunun yerine, her tahmini olanlarla karşılaştırın.
- **Sabit döngüleri uymayan işe uygulamak.** Öngörülemeyen taleplerden oluşan bir kuyruğu sabit dönemlere zorlamak hayal kırıklığı yaratır. Bunun yerine, akış temelli bir yaklaşımı deneyin ve sonuçları karşılaştırın.

## Olgunluk modeli

| Boyut | Başlangıç | Gelişim | Standartlaştırma | Yönetim | Eşgüdüm |
|---|---|---|---|---|---|
| Tahmin | Tarihler görüşten gelir | Bazı ekipler geçmiş verileri kullanır | Ekipler kendi akış verilerinden aralıklar olarak tahmin eder | Tahmin doğruluğu izlenir ve yöntem iyileştirilir | Tahminler ekipler ve tedarikçiler arasında eşgüdümlenir |
| Akış ölçüleri | Az ölçü toplanır | Bazı ekipler çevrim süresini ya da çıktı hızını kaydeder | Dört akış ölçüsü tutarlı biçimde toplanır | Ölçüler gözden geçirilir ve beklentileri belirlemek için kullanılır | Akış verileri ekipler arasında paylaşılır ve birlikte planlamak için kullanılır |
| Kapasite ve plansız iş | Kesintiler sayılmaz | Bazı ekipler plansız işi izler | Plansız iş kapasitesi veriden belirlenir | Plansız işin payı ve nedenleri gözden geçirilir ve azaltılır | Operasyon ve teslimat ekipleri kapasiteyi birlikte planlar |
| Tahmin ve sabit döngü kullanımı | Tahminler insanları yargılamak için kullanılır | Bazı ekipler tahminleri kendi planlamaları için kullanır | Ekipler hangi uygulamaları kullandıkları konusunda anlaşır ve farkları adlandırır | Uygulamaların etkileri akışa ve sonuçlara göre gözden geçirilir | Uygulamalar ortak öğrenmeden yola çıkarak ekipler arasında ayarlanır |

## Kontrol listesi

- [ ] Tahminler ekibin kendi biten öğe geçmişinden geliyor.
- [ ] Her tahmin, belirtilmiş varsayımlarla bir aralıktır.
- [ ] Olaylar, talepler ve iyileştirme işi iş öğeleri olarak kaydediliyor.
- [ ] Plansız iş için kapasite veriden belirleniyor ve gözden geçiriliyor.
- [ ] Çevrim süresi, çıktı hızı, süren iş ve iş öğesi yaşı izleniyor.
- [ ] Süren işin ekibin gözden geçirdiği bir sınırı var.
- [ ] En eski açık öğeler düzenli gözden geçiriliyor.
- [ ] Tahminler her dönemden sonra gerçekleşenlerle karşılaştırılıyor.
- [ ] Tahminler ve hız, kullanılıyorsa, hedef değil.
- [ ] Scrum, sprint ya da bir varyasyonun her kullanımı yazılı ve dürüstçe adlandırılmış.

## Yapay zeka istemleri

**Amaç: kendi çıktı hızı verilerinizden bir tahmin aralığı oluşturmak.**

```text
Help me forecast delivery for a team of [number and type of people].

Throughput (items finished) for each of the last [number] weeks: [paste the real figures as a list].
Items remaining: [number], and a note on how similar in size they are: [paste].
Known changes that may affect the next weeks (leave, new work, dependencies): [paste, or write "none known"].

Calculate the lowest, typical, and highest weekly throughput from the figures, and divide the remaining items by each to give a range of weeks. State the assumptions. Do not extrapolate beyond the data or invent numbers. If the data are too thin, say so and ask what to add. List what you are unsure of.
```

**Amaç: çevrim sürelerini analiz etmek ve bir hizmet seviyesi beklentisi önermek.**

```text
Below are the start and finish dates of the last [number] finished work items of type [type]: [paste as a table; use only real data].

Calculate the cycle time of each item. Describe the spread: what most items take, what the slowest take, and what might explain the slow ones. Suggest a service level expectation in the form "most items of this type finish within N days", and say how confident the data allow us to be. Do not state it as a promise. If the data are too few, say so and ask what to collect. List what you are unsure of.
```

**Amaç: kapasitenin ne kadarının plansız işe gittiğini ölçmek.**

```text
Below is a list of the work items our team completed over the last [number] weeks, each marked as planned or unplanned, with the time it took: [paste as a table; use only real data].

Calculate the share of time on planned and unplanned work for each week, using only the numbers I gave. Describe the pattern, suggest what share of capacity to hold back for unplanned work, and name two assumptions behind the suggestion. Ask clarifying questions first if the data are thin, and list what you are unsure of.
```

**Amaç: en eski açık öğeleri gözden geçirmek ve engelleri kaldırmayı planlamak.**

```text
Our open work items, with start dates and current state: [paste as a table; use only real data].
Cycle times of our last [number] finished items: [paste].

Calculate the current age of each open item and flag those older than most finished items. For each flagged item, suggest two questions to ask about what blocks it. Do not guess the cause. List what you are unsure of.
```

## Yapay zeka becerileri

- [kanban](../../../../skills/kanban/SKILL.md): akış ölçülerini, süren iş sınırlarını ve bir hizmet seviyesi beklentisini kurmak için kullanın.
- [capacity-planning](../../../../skills/capacity-planning/SKILL.md): mevcut kapasitenin öngörülen talebi karşılayıp karşılamadığını ve bir boşluk için ne yapılacağını denetlemek için kullanın.
- [demand-forecasting](../../../../skills/demand-forecasting/SKILL.md): gelecekteki yükü geçmiş verilerden ve iş planlarından bir aralık olarak tahmin etmek için kullanın.
- [software-engineering-metrics](../../../../skills/software-engineering-metrics/SKILL.md): bir metrik seçmek, onun manipülasyon vektörünü ve korkuluğunu adlandırmak ve bir metrik şartı doldurmak için kullanın.
- [scrum](../../../../skills/scrum/SKILL.md): ekip sprintlerle planlıyorsa, rollerini, etkinliklerini ve çıktılarını kurmak ya da gözden geçirmek için kullanın.

## Temel kaynaklar

- **The Kanban Guide** (kanbanguides.org): akış ölçülerini ve geçmiş çevrim sürelerine dayanan bir tahmin olarak hizmet seviyesi beklentisini tanımlar.
- **The Scrum Guide** (Ken Schwaber ve Jeff Sutherland, scrumguides.org): sprint kullanan ekipler için Scrum'ın yetkili, kısa tanımı.
- **Kanban (development)** (Wikipedia): Kanban'ın akış ölçülerine ve çekme sistemine genel bakış.
- **Scrum (software development)** (Wikipedia): Scrum'ın tarihçesine, rollerine, etkinliklerine ve eleştirisine genel bakış.

## Kaynakça

1. The Kanban Guide — John Coleman, Daniel Vacanti, and contributors, kanbanguides.org — https://kanbanguides.org/english/
2. Kanban (development) — Wikipedia — https://en.wikipedia.org/wiki/Kanban_(development)
3. The Scrum Guide (November 2020) — Ken Schwaber and Jeff Sutherland, scrumguides.org — https://scrumguides.org/scrum-guide.html
4. Scrum (software development) — Wikipedia — https://en.wikipedia.org/wiki/Scrum_(software_development)
5. Scrumban — Wikipedia — https://en.wikipedia.org/wiki/Scrumban
6. Agile software development — Wikipedia — https://en.wikipedia.org/wiki/Agile_software_development
7. Site reliability engineering — Wikipedia — https://en.wikipedia.org/wiki/Site_reliability_engineering
