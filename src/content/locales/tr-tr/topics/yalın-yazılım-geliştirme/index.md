# Yalın Yazılım Geliştirme

**Yalın yazılım geliştirme, israfı ortadan kaldırma, hızlı öğrenme ve bütün sistemi en iyileme yönündeki yalın fikirleri yazılım işine uygular; hizmet ekiplerine, zamanın ve emeğin talepten değere giden akıştan nerede sızdığını görmek için ortak bir yol verir.**

## Bu neden önemli

Çevik yöntemler küçük adımlarla teslim etmenizi ve öğrenmenizi söyler. Yalın daha keskin bir soru sorar: zaman nereye gidiyor? Çoğu hizmet kuruluşunda bir talep üzerindeki çalışma süresi, geçen sürenin küçük bir bölümüdür. Gerisi onayları beklemek, ekipler arası devirler, kusurlardan doğan yeniden iş ve en baştan kimsenin istemediği işle geçer. Yalın size bu israfı görmek ve kaldırmak için sözcükler ve araçlar verir.

Yalın aynı zamanda odağı bütün sisteme koyar. Kendi parçasını hızlandırırken öncesindeki ya da sonrasındaki kuyruk büyüyen bir ekip, müşteri için hiçbir şeyi iyileştirmemiştir. Bu bakış hizmet yönetimine iyi uyar. Bir hizmet, birçok ekibin, aracın ve tedarikçinin toplamıdır ve herhangi bir yerdeki bir gecikme kullanıcı için bir gecikmedir. "Bütünü en iyile" ilkesi, uçtan uca akışa bakmak için kalıcı bir hatırlatmadır.

Yalın, bu kılavuzun başka yerlerinde görünen birçok şeyin kaynağıdır. Kanban aynı köklerden yararlanır (bkz. Konu 1.5 — Kanban), değer akışı yönetimi yalın haritalamayı dijital işe uygular (bkz. Konu 5.4 — Değer Akışı Yönetimi) ve sürekli iyileştirme, yalının sürekli küçük kazanımlar alışkanlığını yankılar (bkz. Konu 3.15 — Sürekli İyileştirme). Bu konu, fikirleri ve onları sloganlara dönüştürmeden nasıl kullanacağınızı açıklar.

## Temel kavramlar

### Yalın nereden geliyor

[Yalın üretim hakkındaki Wikipedia maddesine](https://en.wikipedia.org/wiki/Lean_manufacturing) göre yalın, [Toyota Üretim Sistemi'nden](https://en.wikipedia.org/wiki/Toyota_Production_System) doğdu. İkinci Dünya Savaşı'ndan sonra Japon üreticilerin nakdi, alanı ya da hammaddesi azdı ve Taiichi Ohno ile Shigeo Shingo, W. Edwards Deming'in öğretisine dayanarak Toyota'nın sürecini küçük fabrikalar ve düşük stok etrafında yeniden tasarladı. John Krafcik "yalın" (lean) terimini 1988'de bir makalede ortaya attı ve James Womack ile Daniel Jones onu 1996 tarihli *Lean Thinking* kitabında resmen tanımladı.

[Yalın yazılım geliştirme hakkındaki Wikipedia maddesine](https://en.wikipedia.org/wiki/Lean_software_development) göre "yalın yazılım geliştirme" terimi, Mary ve Tom Poppendieck'in 2003 tarihli *Lean Software Development: An Agile Toolkit* kitabından gelir. Kitap yalın üretim ilkelerini yazılıma uyarlar ve yalın araçları çevik uygulamalarla karşılaştırır. Poppendieck'lerin çevik konferanslardaki konuşmaları fikirlerin çevik topluluğa girmesine yardımcı oldu.

### Yalın düşüncenin beş ilkesi

Womack ve Jones, üretim maddesinin kaydettiği şekilde yalın düşüncenin beş ilkesini ortaya koydu:

1. **Değer:** değeri müşterinin bakış açısından tanımlayın.
2. **Değer akışı:** o değeri yaratan adımların tüm dizisini belirleyin ve hiçbir değer katmayan adımlara meydan okuyun.
3. **Akış:** kalan adımları kesintisiz akıtın.
4. **Çekme:** işi itmek yerine, müşterinin talebinin işi çekmesine izin verin.
5. **Mükemmellik:** israf kaldırılmaya devam edilsin diye iyileştirmeyi sürdürün.

### Yazılım için yedi ilke

Yalın yazılım geliştirme hakkındaki Wikipedia maddesi yazılım için yedi ilke listeler:

| İlke | Ne ister | Hizmet işinde |
|---|---|---|
| **İsrafı ortadan kaldırın** | Müşteri için değer katmayan her şeyi kaldırın | Hiçbir şeyi reddetmeyen onayları, kimsenin okumadığı raporları ve kimsenin kullanmadığı özellikleri bırakın |
| **Öğrenmeyi güçlendirin** | Bir şeyi denemekten nasıl gittiğini öğrenmeye kadar olan döngüyü kısaltın | Küçük değişiklikleri yayımlayın ve kullanıcıların ne yaptığını izleyin |
| **Kararları mümkün olduğunca geç verin** | Seçenekleri açık tutarak, olgulara sahip olana kadar taahhütleri geciktirin | Bir hizmetin tüm geleceğinin tasarımını, nasıl kullanıldığını bilmeden önce sabitlemeyin |
| **Mümkün olduğunca hızlı teslim edin** | Fikirden değere giden süreyi azaltın; hızlı teslim sonuçları daha çabuk görmenizi ve analiz etmenizi sağlar | Küçük değişiklikler ve rutin talepler için yolu kısaltın |
| **Ekibi güçlendirin** | İşi yapan kişilerin onun hakkında karar vermesine izin verin | Hizmet masasına yaygın sorunları üst kademeye taşımadan çözme yetkisi verin |
| **Bütünlüğü içine inşa edin** | İşi yaparken kaliteyi içine inşa edin; sonradan denetlemeyin | İşin parçası olarak otomatik testler, izleme ve net çalışma kılavuzları |
| **Bütünü en iyileyin** | Bir parçanın performansını değil, uçtan uca akışı iyileştirin | Her ekibin kendi kuyruğunu değil, ekipler arasında talepten çözüme süreyi ölçün |

Madde, bu ilkelerin yalnızca birlikte ve ortam hakkında sağlam yargıyla uygulandıklarında başarılı olduğunu söyler. Ayrıca "acele israf getirir" inancını bir efsane olarak nitelendirir ve hızlı teslimin ekiplerin çıktıyı daha erken görmesine ve analiz etmesine yardım ettiğini savunur. Bu iddia bir görüştür, bir yasa değildir: içine kalite inşa edilmemiş hız gerçekten israf üretir; bu yüzden "bütünlüğü içine inşa edin", "mümkün olduğunca hızlı teslim edin"in yanında yer alır.

### Yazılım ve hizmet işinde israf

Yalının yedi israfı (*muda* denir), Shingo'nun üretim listesinden gelir: stok, fazla üretim, aşırı işleme, taşıma, fazla hareket, bekleme ve kusurlar. Yalın yazılım maddesi bunları yazılıma şöyle eşler:

| Üretim israfı | Yazılım karşılığı | Bir hizmet ekibinde örnek |
|---|---|---|
| Stok | Yarım kalmış iş | Başlanmış ama bitmemiş değişikliklerin uzun bir listesi |
| Fazla üretim | Fazladan özellikler | Kimsenin istemediği bir rapor ya da hizmet |
| Aşırı işleme | Fazladan süreçler | Düşük riskli bir değişiklikte dört onay |
| Taşıma | Görev değiştirme | Olaylar ile proje işi arasında çekiştirilen bir mühendis |
| Bekleme | Bekleme | Başka bir ekibin kuyruğunu bekleyen bir bilet |
| Hareket | Devirler | Beş kişiden geçen bir talep |
| Kusurlar | Kusurlar | Yeniden işe ve tekrarlayan olaylara yol açan bir hata |

Japonca *mura* (dengesizlik) ve *muri* (aşırı yük) terimleri bazen israf tartışmalarına eklenir. Burada başvurulan Wikipedia maddeleri yalnızca yedi israfı listeler; bu yüzden ek terimleri dikkatle kullanın ve kullandığınızda tanımlayın.

### Değer akışı haritalama

Yalın yazılım maddesi, israfı bulma tekniği olarak değer akışı haritalamayı adlandırır; israf yinelenen turlarda kaldırılır. Bir harita, talepten teslim edilen değere giden yoldaki her adımı, işin üzerinde çalışılarak geçirdiği süre ve beklemekle geçirdiği süreyle gösterir. Sonuç çoğunlukla bir şoktur: haftalar süren bir yol, saatlerle ölçülen gerçek iş içerebilir.

### Çekme, akış ve kanban

Yalının çekme ilkesi, Kanban'ın süren iş sınırlarının arkasındadır. Yazılım maddesi, müşterinin gereken sonucu belirttiği ve ekibin kendi görevlerini örgütleyerek kapasite elverdikçe iş çektiği tam zamanında geliştirmeyi anlatır. Kanban kartları bu çekmenin görünür bir biçimidir (bkz. Konu 1.5 — Kanban).

### Kaizen: sürekli küçük iyileştirme

Kaizen, sürekli, artımlı iyileştirme demektir. Üretim maddesi onun izini 1936'da Toyota'daki iyileştirme ekiplerine kadar sürer. Bir hizmet ekibinde, işe en yakın kişilerce sık sık yapılan küçük değişiklikler olarak görünür; örneğin gözden geçirilmiş bir şablon, yeni bir otomatik kontrol ya da daha net bir devir. Büyük iyileştirme programlarından farkı, bir bütçe döngüsünü asla beklememesidir.

### Yalının sınırları

Başvurulan maddeler resmî bir eleştiri adlandırmaz, ama pratik sınırlar bilinir. Yalın, tekrarlanabilir üretimden geldi ve bilgi işi çok daha fazla değişir. İsrafı saymak, bir ekibin sürprizlerle başa çıkmak için ihtiyaç duyduğu boşluğu azaltabilir; bu yüzden tam yüklü bir ekip bir olaya yanıt vermekte yavaştır. Yalını israfı bulan bir mercek olarak ele alın ve değişkenliğin yüksek olduğu yerde yedek kapasite tutun (bkz. Konu 3.11 — Erişilebilirlik, Kapasite ve Performans).

## İyi uygulamalar

1. **Değeri müşterinin tarafından tanımlayın.** Her hizmet için kullanıcının gerçekte ne aldığını ve onu ne zaman aldığını yazın. Bunu her adımı yargılamak için kullanın: kullanıcı için değer katıyor mu, yoksa yalnızca kendi sürecimize mi hizmet ediyor?
2. **Bir gerçek talep türü için değer akışını haritalayın.** Yaygın bir talep ya da değişiklik seçin ve ilk temastan teslime kadar izleyin. Her adımda çalışma süresini ve bekleme süresini kaydedin. Bir saatte çizilmiş kabaca bir harita, bir çeyrekte çizilmiş mükemmel bir haritadan daha yararlıdır.
3. **Bulduğunuz israfları adlandırın.** Yedi kategoriyi kontrol listesi olarak kullanın: yarım kalmış iş, fazladan özellikler, fazladan süreç, görev değiştirme, bekleme, devirler, kusurlar. Onları adlandırmak, bireyleri suçlamadan tartışmayı kolaylaştırır.
4. **Önce en uzun beklemeye saldırın.** Haritadaki en büyük gecikme genellikle adımların içinde değil, arasındadır. Onu azaltmak genellikle zaten hızlı olan bir adımı cilalamaktan iyidir.
5. **Süren işi sınırlayın.** İşi bitirmek, onu hokkabazlık yaparak taşımaktan hızlıdır. Ekip başına açık öğe sayısını sınırlayın ve her birinin aldığı süreye ne olduğunu izleyin.
6. **Kaliteyi içine inşa edin.** Kusurların erken bulunması için otomatik testler, eş gözden geçirme ve sürüm öncesi izleme gibi kontrolleri işin anında ekleyin. Sonda denetlemek daha yavaş ve daha pahalıdır.
7. **Henüz iyi veremeyeceğiniz kararları erteleyin.** Olgulara sahip olana kadar seçenekleri açık tutun, ama karar vereceğiniz bir tarih belirleyin. Bu, hem yanlış bir tasarıma erken bağlanmayı hem de bitmeyen kararsızlığı önler.
8. **İşe en yakın insanları güçlendirin.** Hizmet masası analistlerinin, nöbetçi mühendislerin ve geliştiricilerin net sınırlar içinde karar vermesine izin verin. Harcama ya da risk eşikleri gibi sınırları belirtin ve olaylardan sonra gözden geçirin.
9. **Parçaya değil, bütüne bakın.** Talepten çözüme uçtan uca süreyi ölçün ve ilgili tüm ekiplerle tartışın. Bir ekibe yardımcı olup diğerini yavaşlatan bir değişiklik bir iyileştirme değildir.
10. **İyileştirmeyi küçük, sık ve yerel yapın.** Her ekibi bir ya da iki haftada bir küçük iyileştirme yapmaya ve öğrendiklerini paylaşmaya teşvik edin. Değişikliği ve sonucunu kaydedin.
11. **Değişkenliğin yüksek olduğu yerde boşluk bırakın.** Bir nöbetçi ekibin her saatini doldurmayın. Sürprizler için kapasite bırakın ve bir şeyler ters gittiğinde ekibin ne kadar çabuk toparlandığıyla yargılayın.
12. **Yalını diğer uygulamalarla birlikte kullanın.** Değer akışı haritalarını Kanban'dan akış ölçüleriyle ve tekrarlayan kusurlar için sorun yönetimiyle birleştirin (bkz. Konu 3.3 — Sorun Yönetimi).

## Ekibinizle tartışılacak sorular

**Yaygın bir talebi baştan sona izlesek, geçen sürenin ne kadarı gerçek iş olurdu?**

Tipik bir talep seçin ve her adımın tarihlerini toplayın. Birinin üzerinde çalıştığı zamanı ve bir kuyrukta durduğu zamanı işaretleyin. Oran çoğunlukla bir şoktur. İnsanlara beklemelerin nerede olmasını bekledikleri ve gerçekte nerede olduklarını sorun. Kolaylaştırıcı önce çözümlere direnmeli ve gruptan haritanın ne gösterdiği konusunda anlaşmasını istemelidir.

**Günlük işimizde yedi israftan hangisini en sık görüyoruz?**

İnsanlara listeyi verin ve her biri için yakın tarihli bir örnek isteyin. Yarım kalmış işin, görev değiştirmenin, beklemenin ve devirlerin sık gündeme gelmesini bekleyin. Hangilerini ekibin tek başına değiştirebileceğini ve hangilerinin başka ekipler ya da yöneticiler gerektirdiğini sorun. Bu ay azaltılacak bir israf seçerek bitirin.

**Bırakırsak müşterilerimizin özlemeyeceği neleri yapıyoruz?**

Raporları, toplantıları, formları ve onayları listeleyin. Her biri için kimin kullandığını ve durursa ne olacağını sorun. Bazıları denetim ya da güvenlik için gerekli olacaktır; bu iyi bir nedendir. Diğerleri alışkanlık çıkacaktır. Kaldırmadan önce her şüpheli öğeyi denetlemek için birini görevlendirin.

**Kaliteyi içine inşa etmek yerine nerede sonda denetliyoruz?**

Sürüm, değişiklik ve olay süreçlerinizde hat sonu kontrollerine bakın. Bu kontrollerin hangi kusurları bulduğunu ve bunların ne zaman daha erken bulunabileceğini sorun. Tipik yanıtlar, geliştirme bittikten sonra test etmeyi ve belgeleri sonradan gözden geçirmeyi içerir. Daha erkene alınacak bir kontrol seçin ve yardımcı olup olmadığını nasıl anlayacağınızı tanımlayın.

**Ekibimizde kim sormadan karar verebilir ve kim vermeli?**

İnsanlardan vermek isteyip veremedikleri son beş kararı ve nedenini listelemelerini isteyin. Harcama sınırları, değişiklik onayları ya da öncelik kararları gibi kalıplara bakın. Bu kararlardan birini işe daha yakına taşımayı neyin güvenli kılacağını, örneğin bir korkuluk ya da sonradan gözden geçirme gibi, sorun. "Evet" demeye zorlamayın; amaç insanların neye ihtiyaç olduğuna inandığını bulmaktır.

**Şimdi yaptığımız her şey hızlansa, önce ne bozulurdu?**

Bu soru "mümkün olduğunca hızlı teslim edin" ve "bütünlüğü içine inşa edin"i birlikte sınar. Daha hızlı bir akışın bir ekibi, bir aracı ya da bir kişiyi nerede aşırı yükleyeceğini sorun. Tipik yanıtlar test, onaylar ve nöbet yüküdür. Yanıtları iyileştirilecek sonraki şeyler olarak ele alın. Yalının bütün sistemin akışına değer verdiğini hatırlayın; bu yüzden darboğaz yatırım yapılacak yerdir.

## Uygulamada: çevik bir ITIL örneği

Ulusal bir vergi idaresinin BT departmanı, personelin yazılım erişimi talep etmesi için bir iç hizmet işletir. Tipik bir talep yaklaşık üç hafta sürer ve personel yüksek sesle şikâyet eder. Talepleri karşılayan beş kişilik ekip çok çalıştığına inanır ve şikâyete şaşırır.

Bir yönetici, ekip, güvenlik grubu ve iki iş kullanıcısıyla bir değer akışı haritalama oturumu yürütür. Birlikte yakın tarihli on talebi izlerler. Her talep sekiz adımdan geçer: form gönderimi, hat yöneticisi onayı, veri sahibi onayı, güvenlik gözden geçirmesi, lisans kontrolü, bilet atama, kurulum ve onay. Harita, gerçek işin yaklaşık bir saat sürdüğünü ve üç haftanın neredeyse tamamının, çoğunlukla iki onay ve güvenlik gözden geçirmesi için adımlar arasında beklemek olduğunu gösterir. On vakanın üçünde, formda eksik bir alan yüzünden talep kullanıcıya geri döndürülmüştü.

Grup üç değişiklik üzerinde anlaşır. Forma zorunlu alanlar ve kısa bir kılavuz eklenir; bu iadeleri ortadan kaldırır. Kısa bir yaygın, düşük riskli uygulama listesi için talepler, veri sahibine bilgi verilerek hat yöneticisinden tek bir onay alır. Güvenlik grubu, kurulumdan önce her talebi değil, bu tür taleplerin bir örneklemini her hafta gözden geçirmeyi kabul eder. İki ay sonra tipik süre yaklaşık bir haftaya düşer. Bir zorluk kalır: hassas uygulamalar için talepler hâlâ üç hafta sürer ve güvenlik grubu, örneklemenin reddedilmesi gereken iki talebi yakaladığını not eder. Hızlı onaya uygun uygulamalar listesini ayarlarlar ve her çeyrek gözden geçirmeye karar verirler.

## Dört bakış açısı

### Ürün ve teslimat ekipleri

Teslimat ekipleri, kendi sprintlerinin ya da panolarının ötesine bakmak için yalını kullanabilir. Bir fikirden bir kullanıcının eline kadar olan yolu, test, güvenlik gözden geçirmesi ve sürüm onayları dahil haritalayın ve işin nerede beklediğini bulun. Bitmemiş işi israf olarak ele alın ve başlamak yerine bitirmeyi tercih edin.

### Hizmet ve operasyon ekipleri

Operasyon ekipleri israfı her gün görür: tekrarlanan olaylar, katmanlar arası devirler ve geri dönen talepler. İşin nerede beklediğini göstermek için haritaları kullanın ve tekrarların nedenlerini kaldırmak için sorun yönetimini kullanın. Her saat planlandığında akışa ne olduğunu göstererek yedek kapasite için gerekçe oluşturun.

### Liderlik ve yönetişim

Liderler, israfın çoğunu yaratan sistemi şekillendirir: onay kuralları, finansman döngüleri ve raporlama. Ekiplerinize bu kuralların en çok nerede zamana mal olduğunu ve her birinin hangi riske karşı koruduğunu sorun. Bir denetimi aynı amacı karşılayan daha hafif bir kontrolle değiştirmeye hazır olun.

### Müşteriler ve kullanıcılar

Müşteriler yalın düşüncede değeri tanımlar ve israfı gecikme olarak hisseder. Gerçekte neye ihtiyacınız olduğunun ve ne kadar çabuk olduğunun sorulmasını bekleyin. Ekibe bir hizmetin hangi kısmının sizin için en önemli olduğunu söyleyin; çünkü bu emeğin nereye gideceğini yönlendirir. Karşılığında daha kısa, daha öngörülebilir beklemeler bekleyebilirsiniz.

## Yaygın başarısızlık biçimleri

- **Israf adına kapasiteyi kesmek.** Ekipler tam yükte çalışır ve sürprizlere yanıt veremez. Bunun yerine, değişkenliğin yüksek olduğu yerde boşluk bırakın ve ekibin ne kadar çabuk toparlandığına göre yargılayın.
- **Harekete geçmeden haritalamak.** Değer akışı haritası bir duvara asılır ve hiçbir şey değişmez. Bunun yerine, en büyük beklemeyi seçin ve oturum bitmeden bir sahibi olan bir değişiklik üzerinde anlaşın.
- **Tek bir ekibi en iyilemek.** Yerel bir kazanç kuyruğu başka yere taşır. Bunun yerine, uçtan uca süreyi ölçün ve akıştaki tüm ekiplerle değişiklikler üzerinde anlaşın.
- **Denetimleri anlamadan kaldırmak.** İsraf gibi görünen bir adım gerçek bir riske karşı koruyordu. Bunun yerine, her adımın neyi koruduğunu sorun ve mümkün olan yerde onu daha hafif bir kontrolle değiştirin.
- **Yalın sözcükleri slogan olarak kullanmak.** İnsanlar meslektaşlarının işini geçiştirmek için "israf" der. Bunun yerine, terimleri akışı betimlemek için kullanın ve sohbeti sistem hakkında tutun.
- **Hızı kalitenin önüne koymak.** Daha hızlı teslim daha fazla kusur ve yeniden iş üretir. Bunun yerine, "bütünlüğü içine inşa edin"i hızın ön koşulu olarak ele alın.
- **Üretim rakamlarını bilgi işine uygulamak.** Bir fabrikadan hedefler değişken işe uymaz. Bunun yerine, yalını görmenin ve sormanın bir yolu olarak kullanın ve ölçüleri kendi verilerinizden belirleyin.
- **Yalını tek seferlik bir proje olarak görmek.** Dikkat başka yere kayınca kazanımlar solar. Bunun yerine, küçük iyileştirmeleri her ekibin rutininin parçası yapın.

## Olgunluk modeli

| Boyut | Başlangıç | Gelişim | Standartlaştırma | Yönetim | Eşgüdüm |
|---|---|---|---|---|---|
| İsrafı görmek | İsraf hissedilir ama betimlenmez | Bazı ekipler kendi işlerini haritalar | Ekipler ortak israf kategorileri ve değer akışı haritaları kullanır | Bekleme ve yeniden iş değer akışı boyunca ölçülür | Haritalar ve ölçüler ekipleri ve tedarikçileri aşar |
| Akış ve çekme | İş itilir ve toplu başlatılır | Bazı ekipler süren işi sınırlar | Çekme kuralları ve sınırlar standarttır | Akış ölçüleri sınırlara ve politikalara yapılan değişiklikleri yönlendirir | Akış bütün akış boyunca eşgüdümlenir |
| Kaliteyi içine inşa etmek | Kalite sonda denetlenir | Bazı ekipler erken test eder ve işi gözden geçirir | Otomatik kontroller ve yerleşik gözden geçirmeler standarttır | Kusur kaçış oranları izlenir ve azaltılır | Kalite uygulamaları ekipler arasında paylaşılır ve iyileştirilir |
| Sürekli iyileştirme | İyileştirme krizleri izler | Bazı ekipler küçük, düzenli değişiklikler yapar | Her ekibin düzenli bir iyileştirme rutini vardır | İyileştirmeler izlenir ve etkileri kontrol edilir | İyileştirmeler ekipler ve tedarikçiler arasında rutin olarak yayılır |

## Kontrol listesi

- [ ] En az bir hizmet için değerin kullanıcı tarafından ne anlama geldiğini tanımladık.
- [ ] Yaygın bir talep türü için değer akışını, çalışma süresi ve bekleme süresiyle haritaladık.
- [ ] Ekip yedi israfı adlandırabiliyor ve her biri için yakın tarihli bir örnek verebiliyor.
- [ ] Süren iş sınırlı ve bitmemiş iş görünür.
- [ ] Kalite kontrolleri sonda olduğu kadar iş sırasında da yapılıyor.
- [ ] Azaltılacak en az bir beklemeyi, bir sahip ve bir tarihle seçtik.
- [ ] Ekibin sormadan verebileceği kararlar için net sınırları var.
- [ ] Ekipler arasında en az bir akış için uçtan uca süreyi ölçüyoruz.
- [ ] Talebin değiştiği yerde sürprizler için yedek kapasite tutuyoruz.
- [ ] Her ekip düzenli bir ritimle küçük bir iyileştirme yapıyor ve kaydediyor.

## Yapay zeka istemleri

**Amaç: sağladığınız sürelerden bir değer akışını analiz etmek.**

```text
Help me analyze a value stream for [type of request, e.g. "software access requests"].

Here are the steps in order, with who does each step, how long work was actually done on it, and how long the item waited before and after it. Use real numbers from a few recent cases: [paste as a table, with one row per step and one column per case].

Calculate, using only my numbers, the total elapsed time, the total working time, and the share of time spent waiting. Identify the three longest waits. For each wait, ask what the step protects against, and suggest one lighter alternative. Do not invent data. If numbers are missing, ask me first, mark assumptions, and list what you are unsure of.
```

**Amaç: kendi ekibinizin işinden israf örneklerini sınıflandırmak.**

```text
Here is a list of things that frustrate our team or customers: [paste 8-12 short, factual examples].

Classify each one under the seven wastes of lean software development: partially done work, extra features, extra process, task switching, waiting, handoffs, and defects. If an item does not fit any, say so. Give one sentence of reasoning per item based only on what I wrote. Then say which two categories seem most common in this list and suggest two questions the team should discuss. Mark assumptions, and list what you are unsure of.
```

**Amaç: bir denetimi kaldırmanın güvenli olup olmadığını sınamak.**

```text
We are considering removing or simplifying this control: [describe the approval, report, or step].

What we believe it is for: [describe the purpose, or write "unknown"].
Who uses its output: [list people or teams, or write "unknown"].
Rules we know apply (audit, security, legal), with the actual text if you have it: [paste text, or write "none known"].

List the questions we should answer before changing it. Describe two lighter ways to meet its purpose, and a way to check after the change that nothing worse happened. Do not claim any law or standard applies unless I pasted its text. Mark assumptions, and list what you are unsure of.
```

**Amaç: bir değer akışı haritalama çalıştayı planlamak.**

```text
Plan a 90-minute value stream mapping workshop for [number] people from [teams or roles]. We want to examine [request type or service].

Include: a timed agenda, who must attend, what data to bring (use only data we really have), how to draw the map step by step, how to mark working time and waiting time, and a closing step that records one agreed change with an owner and a date. Keep it free of any particular tool. Ask clarifying questions first if information is missing, and list what you are unsure of.
```

## Yapay zeka becerileri

- [value-stream-map](../../../../skills/value-stream-map/SKILL.md): bir talebin adımlarını, çalışma süresini ve bekleme süresini baştan sona haritalamak için kullanın.
- [kaizen](../../../../skills/kaizen/SKILL.md): israf bulunduktan sonra küçük, sürekli iyileştirmeleri planlamak için kullanın.
- [workflow-analysis](../../../../skills/workflow-analysis/SKILL.md): işin roller arasında nasıl hareket ettiğini analiz etmek ve devirleri ve gecikmeleri bulmak için kullanın.
- [kanban](../../../../skills/kanban/SKILL.md): haritalamış olduğunuz akışa çekme ve süren iş sınırlarını uygulamak için kullanın.
- [six-sigma](../../../../skills/six-sigma/SKILL.md): ana sorun yalnızca bekleme değil, kusurlar ve değişkenlikse ve bunları azaltmak için veriye dayalı bir yönteme ihtiyacınız varsa kullanın.

## Temel kaynaklar

- **Lean software development** (Wikipedia): yedi ilke, israf eşlemesi ve ileri okumalara bağlantılar.
- **Lean manufacturing** (Wikipedia): Toyota'da yalının tarihçesi, israflar ve yalın düşüncenin beş ilkesi.
- **Lean Software Development: An Agile Toolkit** (Mary ve Tom Poppendieck, 2003): yalın fikirleri çevik topluluğa getiren kitap.
- **Lean Thinking** (James Womack ve Daniel Jones, 1996): yalının beş ilkesinin resmî ifadesi.

## Kaynakça

1. Lean software development — Wikipedia — https://en.wikipedia.org/wiki/Lean_software_development
2. Lean manufacturing — Wikipedia — https://en.wikipedia.org/wiki/Lean_manufacturing
3. Toyota Production System — Wikipedia — https://en.wikipedia.org/wiki/Toyota_Production_System
4. Kaizen — Wikipedia — https://en.wikipedia.org/wiki/Kaizen
5. Value-stream mapping — Wikipedia — https://en.wikipedia.org/wiki/Value-stream_mapping
6. Kanban (development) — Wikipedia — https://en.wikipedia.org/wiki/Kanban_(development)
7. Agile software development — Wikipedia — https://en.wikipedia.org/wiki/Agile_software_development
8. Muda (Japanese term) — Wikipedia — https://en.wikipedia.org/wiki/Muda_(Japanese_term)
