# Kanban

**Kanban işi bir akış olarak yönetir: iş akışını görünür kılar, süren işi sınırlar ve iyileşmek için akış ölçülerini kullanır; bu da işi sürekli gelen ve sabit döngülerle planlanamayan hizmet ekiplerine uyar.**

## Bu neden önemli

Bir hizmet masası, bir operasyon ekibi ve bir platform ekibi aynı özelliği paylaşır: iş geldiği zaman gelir. Olaylar, talepler ve küçük değişiklikler bir akış halinde gelir ve ekip bunların bir aylığını önceden planlayamaz. Scrum gibi sabit döngüler etrafında kurulmuş çerçeveler bu işe ancak ayarlamalarla uyar (bkz. Konu 1.4 — Teslimat Tahmini ve Planlama Metrikleri). Kanban akış için tasarlandı; bu yüzden daha doğal biçimde uyar.

Kanban aynı zamanda hizmet yönetiminin dilini konuşur. İşin ne kadar sürdüğünü, ne kadarının beklediğini ve hangi adımın darboğaz olduğunu sorar; bunlar hizmet seviyelerinin, kuyruk yönetiminin ve kapasite planlamanın ardındaki sorulardır. İşinin yaşını ve çevrim süresini (cycle time) izleyen bir ekip, hizmet seviyeleri hakkında izlenimlerle değil, verilerle konuşabilir.

Kanban başlamak için basittir ve şaşırtıcı biçimde kötü yapmak kolaydır. Süren işi hiçbir şey sınırlamıyorsa ve kimse ölçüleri kullanmıyorsa, sütunlu bir pano Kanban değildir. Bu konu, Kanban Guide'ın bir ekipten ne istediğini, yöntemin nereden geldiğini ve onu hizmet işine nasıl uygulayacağınızı açıklar.

## Temel kavramlar

### Kanban nedir

Güncel sürümü Mayıs 2025 tarihli olan ve yazarları arasında John Coleman ile Daniel Vacanti'yi sayan [Kanban Guide](https://kanbanguides.org/english/), Kanban'ı değerin bir süreçten akışını en iyileme stratejisi olarak tanımlar. Akışı, potansiyel değerin bir sistem içinden hareketi olarak tanımlar. Amaç üç şeyin dengesidir: etkinlik (paydaşların istediğini istedikleri zaman teslim etmek), verimlilik (kaynakları iyi kullanmak) ve öngörülebilirlik (teslimi kabul edilebilir bir belirsizlik düzeyiyle tahmin etmek). Kılavuz, her sektörde bilgi işine uygulandığını söyler.

"Kanban" sözcüğü Japoncadır ve tabela ya da pano anlamına gelir. [Geliştirmede Kanban hakkındaki Wikipedia maddesi](https://en.wikipedia.org/wiki/Kanban_(development)), yöntemin yalın üretimden ve [Toyota Üretim Sistemi'nden](https://en.wikipedia.org/wiki/Toyota_Production_System) geldiğini, tam zamanında (just-in-time) bir sistemin 1940'ların sonlarında Toyota'da başlatıldığını söyler. David J. Anderson'ın 2010 tarihli kitabı, yazılım sürümünün izini Microsoft'taki 2004 tarihli bir projeye ve Corbis'teki 2006-2007 tarihli bir projeye kadar sürer.

### Üç uygulama

Kanban Guide üç uygulama adlandırır. Üçünü de yapan ve aşağıdaki ölçüleri kullanan bir ekip, kılavuzun anlamıyla Kanban uygulamaktadır.

| Uygulama | Ekip ne yapar | Hizmet ekipleri için bir not |
|---|---|---|
| **İş akışını tanımlayın ve görselleştirin** | Bir İş Akışı Tanımı (Definition of Workflow, DoW) üzerinde anlaşın: iş öğesinin ne olduğu, nerede başlayıp bittiği, arasındaki durumlar, süren işin nasıl sınırlandığı, işi hareket ettirme politikaları ve bir hizmet seviyesi beklentisi (SLE). Bunu bir panoda gösterin. | Bir hizmet masasının DoW'u olay, talep ve değişiklik öğelerini, her biri için farklı durumlar ve politikalarla tanımlayabilir |
| **İş akışındaki öğeleri etkin biçimde yönetin** | Süren öğe sayısını denetleyin, yaşlanan öğeleri izleyin ve takılıp kalan öğelerin engelini kaldırın. | Mühendis başına açık olay sınırı, ekibi yenilerine başlamadan önce işi bitirmeye ya da devretmeye zorlar |
| **İş akışını iyileştirin** | Etkinliği, verimliliği ve öngörülebilirliği artırmak için DoW'u zamanla, belirli aralıklarla ya da gerektiğinde değiştirin. | Büyük bir olaydan sonra DoW'un gözden geçirilmesi politikaları, sınırları ya da durumları değiştirebilir |

Kılavuz bir pano düzeni ya da herhangi bir toplantı dayatmaz. Çekirdek uygulamalar, ölçüler ve değeri en iyileme hedefi bozulmadığı sürece ekipler uygulama eklemekte özgürdür.

### Süren iş sınırları ve çekme

Süren işi (WIP) denetlemek, kılavuzun çekme sistemi (pull system) dediği şeyi yaratır: yeni iş yalnızca onun için kapasite olduğunda başlar. Wikipedia maddesi, sınırı beş olan bir "dağıtım" (deployment) adımı örneğini verir. Adım dolduğunda, bir şey bitene kadar hiçbir şey giremez; böylece bir tıkanıklık görünür olur ve insanlar onu gidermeye yardım edebilir. Sınırlar olmadan bir pano yalnızca karmaşanın resmidir.

### Dört akış ölçüsü

Kılavuz, Kanban kullanan bir ekibin izlediği dört ölçüyü listeler:

- **Süren iş:** başlatılmış ama henüz bitmemiş öğelerin sayısı.
- **Çıktı hızı (throughput):** belirli bir dönemde biten öğelerin sayısı.
- **İş öğesi yaşı:** bitmemiş bir öğenin ne kadar süredir sürdüğü.
- **Çevrim süresi:** biten bir öğenin başından sonuna ne kadar sürdüğü.

Kılavuz, ekiplerin bunları yeniden adlandırabileceğini ve yararlı olan yerde başka ölçüler eklemesi gerektiğini, ölçülerin yalnızca üç uygulamayı bilgilendirdiklerinde önemli olduğunu söyler. Hizmet seviyesi beklentisi, geçmiş çevrim sürelerine dayanan, bir öğenin ne kadar sürmesi gerektiğine dair bir tahmindir. Bir söz değildir ve bir müşteriyle müzakere edilen hizmet seviyesi anlaşmasından (SLA) farklıdır. Bkz. Konu 3.7 — Hizmet Seviyesi Yönetimi.

### Daha geniş Kanban yazını

Başka yazarlar yöntemi daha geniş biçimde anlatmıştır. Wikipedia maddesi, Don Reinertsen'in akış üzerine çalışmasını, Jim Benson ve Tonianne DeMaria Barry'nin *Personal Kanban* kitabını, Mike Burrows'un *Kanban From the Inside* kitabını ve Kanban'ı Scrum'ı iyileştirmenin bir yolu olarak öneren Corey Ladas'ın *Scrumban* kitabını listeler. Bu kaynaklardan bazıları, politikaları açık hale getirmek, geri bildirim döngüleri uygulamak ve iş birliği içinde iyileştirmek gibi kılavuzdaki üçün ötesinde uygulamalar sayar. Bunları kılavuzun gereklilikleri olarak değil, yararlı eklemeler olarak ele alın.

Wikipedia maddesi, önemli bir katkıda bulunanın konuyla yakın bağı olabileceğini belirten bir etiket taşır; bu nedenle iddialarını birincil kaynaklara karşı denetleyin.

### Kanban'ın söylemedikleri

Kanban bir proje planı, bir roller kümesi ya da bir sürüm süreci değildir. Bir hizmetin nasıl tasarlanacağını ya da bir olayın nasıl yönetileceğini söylemez. Akışı görmenin ve yönetmenin bir yolunu verir ve işinizin içeriğini sizin getirmenize güvenir. Bu aynı zamanda gücüdür: elinizdeki süreçle başlayabilir ve onu küçük adımlarla iyileştirebilirsiniz (bkz. Konu 3.15 — Sürekli İyileştirme).

## İyi uygulamalar

1. **Şu an yaptığınızla başlayın.** Gerçek iş akışını, işin gerçekte geçtiği durumlarla, beklemeler dahil çizin. Sahip olmak istediğiniz süreci çizmeyin. Yalnızca görebildiğinizi iyileştirebilirsiniz.
2. **İş öğesinin ne olduğunu tanımlayın.** Olayların, taleplerin ve değişikliklerin tek bir öğe türü mü yoksa birkaç tür mü olduğuna karar verin ve her birine net bir başlangıç ve bitiş verin. Karışık tanımlar ölçüleri anlamsız kılar.
3. **WIP sınırları koyun ve onlara uyun.** Biraz sıkı hissettiren bir sınırla, örneğin kişi başına bir ya da iki öğeyle başlayın ve deneyime göre ayarlayın. Rutin olarak çiğnenen bir sınır bilgi vermez; bu yüzden her ihlali tartışın.
4. **Politikaları açık hale getirin.** Bir öğenin sonraki duruma ne zaman geçebileceğini, onu kimin çekebileceğini ve neyin engelli sayıldığını panoya yazın. Görünür politikalar tartışmaları azaltır ve ekibe katılımı kolaylaştırır.
5. **Yalnızca çevrim süresini değil, iş öğesi yaşını da izleyin.** Çevrim süresi ancak bir öğe bittikten sonra bilinir; yaş ise henüz harekete geçecek zaman varken sorunları gösterir. En eski öğeleri her gün gözden geçirin.
6. **Geçmişe dayanan bir hizmet seviyesi beklentisi kullanın.** Yakın tarihli biten öğelerin çevrim sürelerini alın ve örneğin bir türün öğelerinin çoğunun belirli bir gün sayısı içinde bittiğini belirtin. Veriler değiştikçe gözden geçirin. Müşterilere ölçmediğiniz bir sayıyı vaat etmeyin.
7. **Hızlandırılmış işi açık bir istisna olarak ele alın.** Acil olaylar kuyruğu atlayacaktır. İstisnalar görünür olsun ve akışı sessizce bozmasın diye, kendi sınırı olan bir hat gibi bir politika tanımlayın (bkz. Konu 3.2 — Olay Yönetimi).
8. **Darboğazı arayın ve ona yardım edin.** Bir durum hep doluysa, daha fazla kapasiteye mi, değiştirilmiş bir politikaya mı yoksa farklı bir yukarı akışa mı ihtiyacı olduğunu sorun. İnsanları darboğaza kaydırmak genellikle ona daha fazla iş itmekten iyidir.
9. **Düzenli bir ritimle gözden geçirmeler yapın.** Kılavuz iyileştirmeye belirli aralıklarla ya da gerektiğinde izin verir. Ölçülerin kısa haftalık gözden geçirilmesi ve DoW'a aylık bir bakış birçok ekip için işe yarar.
10. **Panoyu kuruluşun geri kalanına bağlayın.** Panoyu müşterilere ve komşu ekiplere görünür kılın. Öğelerin panolar arasında nasıl geçeceği, örneğin bir hizmet masasından bir geliştirme ekibine, konusunda anlaşın.
11. **Ölçüleri öğrenme için tutun.** Sayıları insanları sıralamak için değil, soru sormak için kullanın. Akış verisi bir hedef haline geldiğinde ekipler onu manipüle eder (bkz. Konu 5.6 — Metrikler ve Ölçüm).
12. **Diğer çerçevelerle bilinçli biçimde birleştirin.** Ekip planlama için Scrum etkinliklerini, akış için Kanban'ı kullanıyorsa, her birinin ne için olduğunu söyleyin ve birleşimin karışıklığı azalttığını denetleyin (birkaç ekibi eşgüdümlemek için bkz. Konu 1.8 — Çevikliği Ölçeklendirme).

## Ekibinizle tartışılacak sorular

**Gerçek iş akışımızı, beklemeler dahil çizsek neye benzerdi?**

Her kişiden yakın tarihli bir öğenin yolunu çizmesini isteyin, sonra çizimleri bir duvarda birleştirin. Çizimler arasındaki farklar gizli adımları ve gayriresmî devirleri gösterir. Sürprizler bekleyin: kimsenin anmadığı onaylar, başka bir ekibi bekleyen öğeler ve yeniden iş döngüleri. En uzun üç beklemeyi işaretleyerek devam edin.

**Şu anda her birimizin elinde ne kadar iş var ve bunun ne kadarı bekliyor?**

Kişi başına açık öğeleri sayın ve hangilerinin engelli ya da boşta olduğunu işaretleyin. Birçok ekip öğelerin çoğunun beklediğini ve azının üzerinde çalışıldığını bulur. Her kişinin engellendiğinde ne yaptığını ve yeni bir öğeye başlamanın olağan yanıt olup olmadığını sorun. Amaç, başlamanın neden ödüllendirildiğini ve bitirmenin neden ödüllendirilmediğini tartışmaktır.

**Panomuzdaki en eski öğe hangisi ve neden hâlâ orada?**

En eski üç öğeyi seçin ve ne olduğunu izleyin. Yaygın yanıtlar belirsiz bir sahip, başka bir ekibe bağımlılık ya da kimsenin iptal etmek istemediği bir öğedir. Öğenin bitirilmesi, iptal edilmesi mi yoksa üst kademeye taşınması mı gerektiğini sorun. Kolaylaştırıcı hangi politikanın öğeyi daha erken yakalayacağını sorabilir.

**Müşterilerimize işlerin ne kadar süreceği konusunda ne vaat ediyoruz ve kendi sayılarımız ne diyor?**

Üzerinde anlaşılan hizmet seviyelerini biten öğelerin gerçek çevrim süreleriyle karşılaştırın. Verileriniz yoksa önce bir ay boyunca toplayın. Her boşluğu açıkça tartışın. Hedefin mi yoksa çalışma biçiminin mi değişmesi gerektiğini sorun. Veriye dayanan bir hizmet seviyesi beklentisinin bir tahmin, SLA'nın ise bir anlaşma olduğunu unutmayın.

**Acil iş geldiğinde diğer her şeye ne oluyor?**

Son acil olayı baştan sona izleyin ve hangi öğelerin durduğuna bakın. Ekibin acil iş için bir politikası olup olmadığını ve ayda kaç acil öğeyi ele aldığını bilen biri olup olmadığını sorun. Ekipler genellikle acil işin istisna değil rutin olduğunu ve politikanın bunu yansıtması gerektiğini keşfeder. Hızlandırılmış öğeler için bir sınır üzerinde anlaşarak devam edin.

**Ölçülerimizden hangilerine bir kararı dayandıracak kadar güvenirdik, hangilerini yok sayardık?**

İnsanlardan mevcut ölçüleri ne kadar güvendiklerine göre ve nedenini belirterek sıralamalarını isteyin. Güvensizlik çoğunlukla tutarsız öğe tanımlarından ya da verideki boşluklardan gelir. Bunu insanlar hakkında bir tartışmaya dönüştürmeyin; verinin kalitesine odaklanın. Önümüzdeki ay iyileştirilecek bir ölçü seçerek bitirin.

## Uygulamada: çevik bir ITIL örneği

Bir üniversitenin BT hizmet masasında, öğrencilerden ve personelden gelen olayları ve talepleri ele alan sekiz analist var. Ekibin kuyrukları olan ama sınırları olmayan bir bilet aracı var ve her analistin 20 ila 40 açık bileti var. Müşteriler biletlerin kaybolduğundan şikâyet ediyor ve masa yöneticisi tipik bir talebin ne kadar sürdüğünü söyleyemiyor.

Yönetici ve analistler aracı yansıtan bir pano kurar: yeni, ayıklanmış, sürüyor, müşteriyi bekliyor, başka bir ekibi bekliyor ve çözüldü. Analist başına sekiz etkin öğe sınırı ve başkalarını bekleyen biletlerin bir sonraki adımdan sorumlu kişiyi adlandırması gerektiği kuralı üzerinde anlaşırlar. Acil olaylar için, sınırı iki olan bir hat ayırırlar. Bir ay boyunca yalnızca çevrim süresi ve yaş verisi toplarlar.

Aydan sonra veriler, taleplerin çoğunun birkaç günde çözüldüğünü ama uzun bir kuyruğun haftalarca, çoğunlukla "başka bir ekibi bekliyor" durumunda beklediğini gösterir. Ekip verilerden bir hizmet seviyesi beklentisi belirler ve en eski öğelerin günlük gözden geçirmesini başlatır. Uzun süredir bekleyen birkaç bilet ilk haftada kapatılır ya da üst kademeye taşınır. Bir sorun kalır: bekleyen biletlerin çoğunun sahibi olan ağ ekibinin kendi panosu yoktur ve masa onun kuyruğunu göremez. Masa yöneticisi ağ ekibi liderle haftalık bir sohbet ayarlar ve iki ekip aralarında geçen öğelerin ortak bir görünümünü paylaşmayı tartışmaya başlar.

## Dört bakış açısı

### Ürün ve teslimat ekipleri

Teslimat ekipleri, işin tasarım, inşa, test ve sürüm arasında nerede beklediğini görmek için Kanban'ı kullanabilir. Süren iş sınırları yarım kalmış değişikliklerin sayısını azaltır ve akış verileri bir sürüm sürecinin nerede dikkat gerektirdiğini gösterebilir. Operasyondan gelen talepleri, kendi politikalarıyla aynı akıştaki öğeler olarak ele alın.

### Hizmet ve operasyon ekipleri

Operasyon ekipleri Kanban'ın doğal yuvasıdır. Olayları, talepleri ve değişiklikleri kendi durumlarında görselleştirin, sınırlar koyun ve yaşlanmayı izleyin. Müşterilerle gerçekçi beklentiler belirlemek için çevrim süresi verilerini kullanın ve diğer ekiplerle sohbetleri başlatmak için engelli ve bekleyen durumları kullanın.

### Liderlik ve yönetişim

Liderler, durum raporlarına göre daha dürüst bir tablo olarak akış ölçülerinden yararlanır. İş türüne göre çevrim süresi, çıktı hızı ve yaşı isteyin ve ekibin bunlar yüzünden neyi değiştirdiğini sorun. Tek tek rakamları hedeflemekten kaçının; bu manipülasyon üretir. Paydaşlar daha fazlasının başlatılmasını istese bile süren iş sınırlarını destekleyin.

### Müşteriler ve kullanıcılar

Müşteriler daha net tahminlerden ve daha az kaybolan talepten yararlanır. Ekipten talep türünüz için hizmet seviyesi beklentisini sorun ve geçmişe dayanmasını bekleyin. Talebiniz aciliyse nedenini sormalarını bekleyin; çünkü ekip başkalarının akışını korumak zorundadır.

## Yaygın başarısızlık biçimleri

- **Sınırsız bir pano.** Pano karmaşayı gösterir ama azaltmaz. Bunun yerine, süren iş sınırlarını koyun ve uygulayın ve her ihlali gözden geçirin.
- **Karışık öğe tanımları.** Olaylar, projeler ve görevler tek bir sütun kümesini paylaşır ve ölçüler hiçbir şey ifade etmez. Bunun yerine, ayrı durum ve politikalarla öğe türleri tanımlayın.
- **Yaşlanmayı yok saymak.** Eski öğeler, bir müşteri şikâyet edene kadar fark edilmeden durur. Bunun yerine, en eski öğeleri her gün gözden geçirin ve her biri hakkında karar verin.
- **Ölçüleri hedefe dönüştürmek.** Ekipler sayıları iyileştirmek için öğeleri böler ya da kapatır. Bunun yerine, ölçüleri soru sormak için kullanın ve ekiple birlikte gözden geçirin.
- **Gizli hızlandırma hatları.** Acil iş sınırları iz bırakmadan atlar. Bunun yerine, acil işe görünür bir hat, bir sınır ve bir politika verin.
- **Bir pano düzenini kopyalamak.** Bir ekip kendi akışını anlamadan başka bir ekibin sütunlarını benimser. Bunun yerine, önce gerçek iş akışını haritalayın.
- **Kanban'a bir raporlama aracı gibi davranmak.** Yöneticiler panoyu akışı iyileştirmek için değil, insanları izlemek için kullanır. Bunun yerine, onu ekibin bir sonraki adıma karar vermek için aracı olarak kullanın.
- **İş akışını hiç iyileştirmemek.** Pano yıllarca aynı kalır. Bunun yerine, İş Akışı Tanımı'nın düzenli gözden geçirmelerini yapın ve veriler gerektirdiğinde değiştirin.

## Olgunluk modeli

| Boyut | Başlangıç | Gelişim | Standartlaştırma | Yönetim | Eşgüdüm |
|---|---|---|---|---|---|
| İş akışını görselleştirme | İş bireysel gelen kutularında ve kafalarda yaşar | Bazı ekiplerin durumlarını gösteren panoları vardır | Ekipler, öğe türleri ve politikalarla bir İş Akışı Tanımı paylaşır | Pano gözden geçirilir ve gerçekte olanlara göre düzeltilir | Ekipler arası panolar ekipler arası öğeleri ve devirleri gösterir |
| Süren işi sınırlama | Sınır yok; insanlar bitirdiklerinden fazlasını başlatır | Bazı ekipler gayriresmî sınırlar koyar | Sınırlar konur ve ihlaller tartışılır | Sınırlar akış verilerine göre ayarlanır | Sınırlar ve kapasite ekipler ve tedarikçiler arasında dengelenir |
| Akış ölçüleri | Az ölçü toplanır | Bazı ekipler çevrim süresini ya da çıktı hızını kaydeder | Dört ölçü tutarlı biçimde toplanır | Ölçüler gözden geçirilir ve hizmet seviyesi beklentilerini belirlemek için kullanılır | Akış verileri ekipler arasında paylaşılır ve kapasiteyi birlikte planlamak için kullanılır |
| İyileştirme | Değişiklikler krizleri izler | Ekipler panoyu ara sıra ayarlar | Ekipler iş akışını düzenli bir ritimle gözden geçirir | Değişiklikler ölçülere bağlanır ve sonuçlar kontrol edilir | İyileştirmeler merkezi yönlendirme olmadan ekipler arasında yayılır |

## Kontrol listesi

- [ ] Gerçek iş akışımızı, beklemeler ve devirler dahil çizdik.
- [ ] İş öğelerimiz, her tür için net bir başlangıç ve bitişle tanımlanmış.
- [ ] Süren iş sınırları var ve her ihlal tartışılıyor.
- [ ] Öğeleri hareket ettirme ve engelleme politikaları panoda ya da yanında yazılı.
- [ ] Çevrim süresini, çıktı hızını, süren işi ve iş öğesi yaşını izliyoruz.
- [ ] En eski öğeleri her gün ya da en azından her hafta gözden geçiriyoruz.
- [ ] Kendi geçmişimize dayanan bir hizmet seviyesi beklentimiz var.
- [ ] Acil işin kendi görünür hattı, sınırı ve politikası var.
- [ ] İş Akışı Tanımı düzenli bir ritimle gözden geçiriliyor.
- [ ] Komşu ekipler ve müşteriler kendilerini ilgilendiren öğeleri görebiliyor.

## Yapay zeka istemleri

**Amaç: gerçek iş akışınızı betimlemek ve işin nerede beklediğini bulmak.**

```text
You are helping me map the real workflow of a team that handles [type of work, e.g. "service desk incidents and requests"].

Here are the states a typical item goes through, as best I can describe them: [paste the steps in order, including waits and handovers].
Here is what happened to three recent items, with dates for each state change: [paste three short timelines, using only real data].

Draw the workflow as a simple text diagram. Identify where each item waited longest, using only the dates I provided. Suggest three questions I should ask the team about those waits. Do not invent numbers. If the data are too thin, ask me for more first, mark your assumptions, and list what you are unsure of.
```

**Amaç: bir ekip için İş Akışı Tanımı taslağı hazırlamak.**

```text
Help me write a first Definition of Workflow for [team name and what it does].

Item types we handle: [list them, e.g. incidents, requests, changes].
States an item can be in: [list, or write "unknown"].
Current policies for starting, finishing, and blocking items: [paste, or write "none written"].
Roughly how many items each person has open at a time: [number, or "unknown"].

Produce a draft with: the item types, start and finish points, states, a proposed WIP limit approach, policies for moving items, a policy for urgent work, and how a service level expectation would be set from our own history. Mark every proposal that is a guess. Do not state any numbers I have not given you. Ask me clarifying questions first, and list what you are unsure of.
```

**Amaç: bilet sisteminizdeki akış verilerini analiz etmek.**

```text
Below are the start and finish dates of [number] items our team completed recently, and the start dates of [number] items still open: [paste as a table, real data only].

Calculate the cycle time of each completed item and the current age of each open item. Describe the spread: what most items take, what the slowest take, and which open items are older than most finished items. Do not extrapolate beyond the data. Suggest two questions to ask the team about the oldest items. Tell me what extra data would make the analysis more reliable, and list what you are unsure of.
```

**Amaç: ekiple panonun gözden geçirilmesini planlamak.**

```text
Plan a 30-minute weekly flow review for a team of [number] people that uses a Kanban board for [type of work].

Our measures: [list which of work in progress, throughput, cycle time, and work item age you track].
Current frustration: [describe in one or two sentences].

Include a timed agenda, five questions to ask about the measures and the oldest items, and a closing step that records at most two changes with owners. Keep it free of any particular tool. Ask clarifying questions first if information is missing, and list what you are unsure of.
```

## Yapay zeka becerileri

- [kanban](../../../../skills/kanban/SKILL.md): bir hizmet ya da operasyon ekibi için bir panoyu, süren iş sınırlarını ve politikaları tasarlamak ya da gözden geçirmek için kullanın.
- [scrumban](../../../../skills/scrumban/SKILL.md): bir ekip Scrum'ın planlama etkinliklerini Kanban'ın akış yönetimiyle birlikte istediğinde kullanın.
- [value-stream-map](../../../../skills/value-stream-map/SKILL.md): panoyu tasarlamadan önce işin ekipler arasında nasıl hareket ettiğini ve nerede beklediğini haritalamak için kullanın.
- [kaizen](../../../../skills/kaizen/SKILL.md): bir akış gözden geçirmesinden sonra iş akışında küçük iyileştirmeler planlamak için kullanın.
- [demand-analysis](../../../../skills/demand-analysis/SKILL.md): sınırlar ve kapasite belirlemeden önce hangi tür işin hangi hacimde geldiğini anlamak için kullanın.

## Temel kaynaklar

- **The Kanban Guide** (John Coleman ve Daniel Vacanti ve diğerleri, kanbanguides.org): üç uygulamanın ve dört ölçünün özlü, yetkili tanımı.
- **Kanban (development)** (Wikipedia): ana kitaplara atıflarla, tarihçeye ve daha geniş uygulamalara genel bakış.
- **Kanban: Successful Evolutionary Change for Your Technology Business** (David J. Anderson, 2010): Kanban'ın yazılım işine nasıl uygulandığının anlatımı.
- **Toyota Production System** (Wikipedia): kanban'ın yalın üretim kökenlerine dair arka plan.

## Kaynakça

1. The Kanban Guide — John Coleman, Daniel Vacanti, and contributors, kanbanguides.org — https://kanbanguides.org/english/
2. Kanban (development) — Wikipedia — https://en.wikipedia.org/wiki/Kanban_(development)
3. Kanban — Wikipedia — https://en.wikipedia.org/wiki/Kanban
4. Toyota Production System — Wikipedia — https://en.wikipedia.org/wiki/Toyota_Production_System
5. Theory of constraints — Wikipedia — https://en.wikipedia.org/wiki/Theory_of_constraints
6. Scrumban — Wikipedia — https://en.wikipedia.org/wiki/Scrumban
7. Lean software development — Wikipedia — https://en.wikipedia.org/wiki/Lean_software_development
8. Agile software development — Wikipedia — https://en.wikipedia.org/wiki/Agile_software_development
