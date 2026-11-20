# BT Hizmet Yönetimi

**BT hizmet yönetimi (ITSM), BT hizmetlerini müşterilerin ihtiyaçları etrafında tasarlama, sunma, işletme ve iyileştirme disiplinidir; hizmet işleten çevik ekipler bu adı kullansalar da kullanmasalar da zaten bunu yapmaktadır.**

## Bu neden önemli

Bir ekip yazılımı yayına aldıktan sonra onu işlettiğinde hizmet sağlayıcı olur. Kullanıcılar ona bağımlıdır, hizmetin erişilebilir olmasını bekler ve bozulduğunda yardım ister. ITSM, bu ilişki etrafında gelişmiş uygulama bütünüdür. Onu yok sayan ekipler çoğu zaman aynı dersi zor yoldan yeniden öğrenir: geceleri çağrılarak, nelerin değiştiğinin kaydını yitirerek ya da müşterilerle neyin vaat edildiği konusunda tartışarak.

ITSM'nin ağır süreçle anılan bir ünü vardır ve bu ünün bir kısmı hak edilmiştir. Çevik ekiplerin de hızlı ilerleyip sonucuyla başa çıkmayı operasyona bırakmakla anılan bir ünü vardır. Her iki ün de iki alanın niyetini değil, başarısızlıklarını anlatır. ITSM, müşterinin bir hizmetten ne beklediğini ve sağlayıcının onu nasıl sunup iyileştireceğini sorar. Çevik ekipler de bu soruyu önemser.

Bu konu, kılavuzun geri kalanında kullanılan sözcük dağarcığını verir: hizmet nedir, müşteriler ve kullanıcılar kimlerdir, ITSM neleri kapsar ve başlıca çerçeveleri nereden gelir. Haritası olarak [BT hizmet yönetimi hakkındaki Wikipedia maddesini](https://en.wikipedia.org/wiki/IT_service_management) kullanır. Bu madde kısadır ve çerçeveleri açıklamaktan çok sıralar; bu nedenle konu pratik yorum ekler ve bunu yaptığı yerleri belirtir.

## Temel kavramlar

### ITSM nedir

Wikipedia maddesi ITSM'yi, bir kuruluşun müşterilere sunulan BT hizmetlerini tasarlamak, oluşturmak, sunmak, işletmek ve denetlemek için yürüttüğü etkinlikler bütünü olarak tanımlar. ITSM'yi ağ yönetimi ve sistem yönetimi gibi teknoloji odaklı yaklaşımlarla karşılaştırır. Madde, ITSM'nin süreç yaklaşımı benimsediğini, sistemlere değil müşteri ihtiyaçlarına odaklandığını ve sürekli iyileştirmeyi vurguladığını söyler.

Madde, CIO WaterCooler'ın 2017 tarihli bir anketine atıf yapar; ankete göre işletmeler ITSM'yi çoğunlukla müşteri deneyimini (%35) ve hizmet kalitesini (%48) desteklemek için kullanmaktadır. Bu tek bir ankettir ve örneklemi maddede anlatılmamıştır; bu nedenle rakamları, uygulayıcıların hedeflerini nasıl dile getirdiğinin bir örneği olarak görün, her hedefin ne kadar yaygın olduğunun ölçüsü olarak değil.

### Hizmet, müşteri ve kullanıcı

**Hizmet**, maliyetlere ve risklere sahip olmak zorunda kalmadan başkalarına değer sunmanın bir yoludur. Bir bankanın çevrimiçi ödemeleri, bir hastanenin randevu sistemi ve bir şirketin paylaşımlı dosya depolaması birer hizmettir. Madde, hizmeti kullanan **kullanıcıları**, hizmetin bedelini ödeyen veya sipariş eden **müşterilerden** ayırır. Bir şirketin kurum içi BT'sinde müşteri bir iş biriminin başındaki kişi, kullanıcılar da o birimin çalışanları olabilir. Bir kamu hizmetinde müşteri bir bakanlık, kullanıcılar da vatandaşlar olabilir. İki grubun ihtiyaçları farklıdır ve yalnızca müşteriyi dinleyen bir sağlayıcı, kullanıcıların yaşadıklarını gözden kaçırabilir.

### Tipik ITSM etkinlikleri

Madde birkaç temel fikri adlandırır, standart ITSM uygulaması ise başkalarını ekler. Birlikte tanınabilir bir yapı oluştururlar:

| Etkinlik | Ne işe yarar | Kılavuzda nerede ele alınır |
|---|---|---|
| **Hizmet masası** | Sağlayıcılar ile kullanıcılar arasında tek iletişim noktası; olayları ve hizmet taleplerini ele alır | Konu 3.1 — Hizmet Masası |
| **Olay ele alma** | Bir şey hizmeti kesintiye uğrattığında veya tehdit ettiğinde hizmeti geri getirme | Konu 3.2 — Olay Yönetimi |
| **Hizmet talepleri** | Kullanıcıların istediği erişim veya ekipman gibi rutin şeyleri sağlama | Konu 3.6 — Hizmet Talebi Yönetimi |
| **Sorunlar ve değişiklikler** | Altta yatan nedenleri bulup gidermek ve hizmetlerde yapılan değişiklikleri denetlemek | Konu 3.3 — Sorun Yönetimi ve Konu 3.4 — Değişiklik Sağlama |
| **Hizmet seviyeleri ve katalog** | Neyin, ne kadar iyi sunulacağı üzerinde anlaşmak | Konu 3.7 — Hizmet Seviyesi Yönetimi ve Konu 3.8 — Hizmet Kataloğu Yönetimi |
| **Sürekli iyileştirme** | Hizmetleri zamanla daha iyi hâle getirme | Konu 3.15 — Sürekli İyileştirme |

Madde **olayı** (incident), hizmetin erişilebilirliğinde veya kalitesinde bir kesinti ya da olası kesinti; **hizmet talebini** (service request) ise bir hizmet için rutin bir istek olarak tanımlar. **Hizmet seviyesi anlaşmalarından (SLA)** yalnızca geçerken söz eder; bu nedenle kılavuz bunları Konu 3.7 — Hizmet Seviyesi Yönetimi'nde açıklar.

### Kurumsal hizmet yönetimi ve otomasyon

Madde iki uzantıyı not eder. **Kurumsal hizmet yönetimi (ESM)**, ITSM araçlarını ve fikirlerini bir işletmenin insan kaynakları veya tesis yönetimi gibi, onlar da talep alıp hizmet sunan diğer bölümlerine uygular. **BT süreç otomasyonu**, rutin elle yapılan adımları otomatik adımlarla değiştirir; böylece personel daha öncelikli işlere odaklanabilir. İkisi de çevik ekipler için önemlidir: ESM, disiplinin BT'ye bağlı olmadığını gösterir; otomasyon ise küçük ekiplerin hacme yetişme yoludur.

### Çerçeveler ve standartlar

Madde birçok çerçeveyi ve standardı sıralar. Aşağıdaki liste, maddenin tek satırlık tanımlarını yineler ve Konu 2.7 — BT Hizmet Yönetimi Çerçeveleri ve Standartları'nda genişletilir.

| Ad | Maddenin söylediği |
|---|---|
| [ITIL](https://en.wikipedia.org/wiki/ITIL) | ITSM ve BT varlık yönetimi için ayrıntılı uygulamalar; BT'yi iş hedefleriyle uyumlu hâle getirir |
| [ISO/IEC 20000](https://en.wikipedia.org/wiki/ISO/IEC_20000) | Hizmet yönetim sistemleri için, bir kuruluşun belgelendirilebileceği uluslararası standart |
| [COBIT](https://en.wikipedia.org/wiki/COBIT) | Kontrol hedefleri, metrikler ve olgunluk modelleri içeren bir BT yönetişim çerçevesi |
| [FitSM](https://en.wikipedia.org/wiki/FitSM) | Büyük ölçüde ISO/IEC 20000 ile uyumlu, hafif bir standart |
| [CMMI](https://en.wikipedia.org/wiki/CMMI) | Hizmetleri oluşturmak, yönetmek ve iyileştirmek için bir model |
| [TOGAF](https://en.wikipedia.org/wiki/TOGAF) | İş hedeflerini mimari hedeflere bağlayan bir çerçeve |
| [Microsoft Operations Framework](https://en.wikipedia.org/wiki/Microsoft_Operations_Framework) | Microsoft teknolojilerine dayalı hizmet yönetimi rehberliği |
| [Application Services Library](https://en.wikipedia.org/wiki/Application_Services_Library) | Profesyonel uygulama yönetimi için bir çerçeve |
| [Business Information Services Library](https://en.wikipedia.org/wiki/Business_Information_Services_Library) | Bilgi yönetimi için en iyi uygulama çerçevesi |
| Business Process Framework (eTOM) | Telekomünikasyon sağlayıcıları için bir süreç çerçevesi |

Madde, ITSM çerçevelerinin ISO 9000, ISO/IEC 27000 ve CMMI'dan yararlandığını, ayrıca ITIL sürüm 2 ile ISO/IEC 20000'in öncülü olan BS 15000'in birbiriyle uyumlu olduğunu ekler. Ayrıca Hollanda hükümeti tarafından benimsenen, ilke temelli bir yönetim sistemi olan USM'yi anlatır.

### Maddenin kapsamadıkları

Maddede tarih bölümü, eleştiri ya da çevik veya DevOps'tan söz eden bir bölüm yoktur. Bu sessizlik önemlidir. ITSM süreç yükü ve yavaş değişim nedeniyle eleştirilmiştir, çevik ekipler de operasyonu ihmal ettikleri için eleştirilmiştir; ancak bu eleştirilerin hiçbirini orada bulamazsınız. Kılavuz bu boşluğu 5. Bölüm'de, Konu 5.1 — Çevik Hizmet Yönetimi ile başlayarak ele alır. Bu konunun sorunlardan söz ettiği yerlerde kılavuzun diğer kaynaklarına ve pratik deneyime dayanılır ve bu belirtilir.

### ITSM ve ITAM

ITIL maddesi, ITIL'i hem ITSM'yi hem de BT varlık yönetimini (ITAM) kapsayan bir yapı olarak anlatır. ITAM, bir kuruluşun hangi BT varlıklarına sahip olduğunu, bunların maliyetini ve nasıl kullanıldığını bilme disiplinidir. Hizmetler varlıklara bağlıdır ve iki disiplin bilgi paylaşır; 4. Bölüm'ün ITSM'yi yakından izlemesinin nedeni budur (bkz. Konu 4.1 — BT Varlık Yönetimi).

## İyi uygulamalar

1. **Hizmetlerinizi müşterinin tarafından tanımlayın.** Müşterilerin ve kullanıcıların gerçekte kullandığı şeyleri, onların sözleriyle listeleyin; örneğin "oturum aç", "randevu al" ve "fatura gönder". Her birinin arkasındaki teknolojiyi gruplayın. Bu, bir hizmet kataloğunun başlangıcıdır (ITIL bunu "service catalogue" diye yazar; bkz. Konu 3.8 — Hizmet Kataloğu Yönetimi).
2. **Müşterilerin ve kullanıcıların kim olduğunu adlandırın.** Her hizmet için kimin ödediğini veya sipariş ettiğini ve kimin kullandığını yazın. Farklı kişilerse, her iki grubun da sesinin duyulduğundan emin olun.
3. **Her hizmete bir sahip atayın.** Hizmetin performansından ve zaman içinde iyileşmesinden sorumlu tek bir kişiyi belirleyin. Sahip olmadan hizmetle ilgili sorunlar kimsenin işi olmaz.
4. **En çok can yakan etkinliklerle başlayın.** Kesintiler acı veriyorsa önce olay ele almayı güçlendirin. Neyin değiştiğini kimse bilmiyorsa değişiklik kayıtlarıyla başlayın. Her ITSM uygulamasını bir anda devreye almayın.
5. **Tek bir ön kapı kullanın.** Kullanıcılara yardım istemek ve talepte bulunmak için tek bir yer verin ve bunu kolaylaştırın. Ulaşılması zor bir hizmet masası atlanır ve ITSM'nin dayandığı bilgiyi kaybedersiniz.
6. **Olayları, talepleri ve sorunları birbirinden ayırın.** Olay bir kesintidir, talep rutin bir istektir, sorun ise altta yatan bir nedendir. Karışık kuyruklar örüntüleri gizler ve ölçümleri bozar.
7. **Önemli olanı kaydedin, fazlasını değil.** Karar vermek için kullanacağınız olay, değişiklik ve varlık kayıtlarını tutun. Kimsenin okumadığı alanları silin. Kayıtlar bir maliyettir ve her birinin ne işe yaradığını söyleyebilmelisiniz.
8. **Çerçeveleri moda değil, soruna göre seçin.** ITIL'i, ISO/IEC 20000'i, COBIT'i veya daha hafif modelleri, sahip olduğunuz sorun için fikir kaynağı olarak kullanın. Yardımcı olan kısımları benimseyin ve hangilerini dışarıda bıraktığınızı söyleyin.
9. **Rutini otomatikleştirin.** Parola sıfırlama ve erişim verme gibi tekrarlayan adımları arayın ve özenle otomatikleştirin. Otomatik eylemleri, kullanıcıların ihtiyaçlarından uzaklaşmasınlar diye düzenli aralıklarla gözden geçirin.
10. **Müşterilerin hissettiğini ölçün.** İç etkinliği saymadan önce erişilebilirliği, hizmeti geri getirme süresini ve kullanıcı memnuniyetini izleyin. Wikipedia maddesindeki anketi, uygulayıcıların ana hedefler olarak müşteri deneyimini ve kaliteyi zaten andığının hatırlatıcısı olarak kullanın.
11. **BT'nin ötesine bakın.** Kuruluşun diğer bölümleri talepleri kötü yönetiyorsa, kurumsal hizmet yönetimi yoluyla ortak araçları ve uygulamayı değerlendirin. BT'nin sözcük dağarcığını onlara dayatmayın.
12. **Sürekli iyileştirin.** Nelerin işe yaradığını olay ve talep verileriyle gözden geçirmek ve küçük değişiklikler yapmak için düzenli zaman ayırın (bkz. Konu 3.15 — Sürekli İyileştirme).

## Ekibinizle tartışılacak sorular

**Hangi hizmetleri sunuyoruz ve bunları kullanıcılarımızın kullanacağı sözlerle nasıl anlatırız?**

Her kişiden, kullanıcıların en sık bize bağlandığı üç şeyi yazmasını isteyin. Listeleri karşılaştırın. Farklılıklar genellikle ekibin hizmet hakkında farklı resimler taşıdığını ya da hizmetleri kullanıma göre değil teknolojiye göre anlattığını gösterir. Kolaylaştırıcı hangi hizmetin net bir sahibi olmadığını sorabilir. İlk hizmet listesi üzerinde anlaşarak sürdürün.

**Ana hizmetimizin müşterileri ve kullanıcıları kimdir ve aynı şeyleri mi isterler?**

Sipariş veren veya ödeyen kişiyi ve kullanan kişileri adlandırın. Her birinin hizmetten ne beklediğini sorun. Kurum içi BT'de müşteri maliyeti ve riski, kullanıcılar ise hızı ve kolaylığı önemseyebilir. Nerede çatıştıklarını ve ekibin bunu nasıl öğrendiğini sorun. Gerçek insanlarla konuşulacak bir çatışma seçin.

**Kullanıcılar yardıma ihtiyaç duyduklarında nereye gidiyor ve kaç yol var?**

Yolları sayın: bir portal, bir telefon numarası, e-posta, sohbet, bir meslektaşın masası. Kullanıcıların hangi yolu neden tercih ettiğini sorun. Birden çok gayriresmî yol, talebin bir kısmının görünmez olduğu anlamına gelir. Tartışma, hangi yolların tutulacağı, hangilerinin birleştirileceği ve gayriresmî yollardan gelenlerin nasıl yakalanacağı kararıyla bitmelidir.

**Bir olayı bir talepten, bir sorundan ne kadar iyi ayırt edebiliyoruz ve bunları karıştırdığımızda ne oluyor?**

Yakın zamandan on bilet alıp sınıflandırın. Anlaşmazlıklar, tanımların ekip içinde farklı olduğunu gösterir. Karışık kategorilerin raporlara ve önceliklere ne yaptığını sorun. Örneğin bir olay kuyruğundaki çok sayıda talep, olay ele almayı yavaş gösterebilir. Basit tanımlar ve örnekler üzerinde anlaşın.

**Hangi ITSM uygulamalarını eksik yapıyoruz ya da yalnızca kâğıt üzerinde yapıyoruz?**

Yukarıdaki tabloda yer alan uygulamaları listeleyin ve her birini çalışıyor, kısmen çalışıyor ya da yalnızca kâğıt üzerinde olarak derecelendirin. Çalışıyor diye derecelendirilenlerin her biri için yakın zamandan bir örnek isteyin. Kolaylaştırıcı her boşluğu doldurma dürtüsüne direnmeli ve hangi boşluğun müşteriler için en çok zarar verdiğini sormalıdır.

**Bir çerçevenin bizim için ne yapmasını isteriz ve bize ne yapmasından korkarız?**

ITIL veya ISO/IEC 20000'i benimsemeye ilişkin umutları ve korkuları toplayın. Umutlar çoğunlukla tutarlılık ve itibardır. Korkular çoğunlukla evrak işi ve yavaşlıktır. İkincisi olmadan birincisini nasıl elde edeceğinizi sorun. Örneğin sözcük dağarcığını ve birkaç uygulamayı benimseyin, formlardan kaçının. Ekibin ihtiyaç duyacağı koşulları kaydedin.

## Uygulamada: çevik bir ITIL örneği

Orta ölçekli bir çevrimiçi perakendeci, kurucunun web sitesinden on iki mühendislik ekibi, büyüyen bir müşteri tabanı ve küçük bir destek grubu olan bir işletmeye dönüşmüştür. Müşteriler sorunları paylaşılan bir gelen kutusuna e-postayla bildirir ve ödeme çöktüğünde kişisel bir cep telefonu numarasını arar. Mühendisler duyduklarını düzeltir ve nadiren bir şey yazıya geçirir. Üç saat süren bir ödeme kesintisinden sonra kurucu, bir müşteri arayana kadar neden kimsenin bilmediğini sorar.

Mühendislik başkanı olabilecek en hafif ITSM'yi önerir. Ekip hizmetlerini müşteri terimleriyle listeler: gezinme ve arama, ödeme ve tahsilat, sipariş takibi ve müşteri hesapları. Her birine bir sahip atanır. Paylaşılan bir destek adresi tek ön kapı olur ve olaylar ile talepler için ayrı türleri olan basit bir bilet aracını besler. 30 dakikadan uzun süren her olay için ortak bir belgede yazılan kısa bir gözden geçirme yapılır. Ödeme ve tahsilat değişiklikleri, gerçekleşmeden önce bir ekip kanalında duyurulur.

Üç ay sonra ekip kaç olay ele aldığını bilir ve çoğunun iki nedenden geldiğini görür. İkisini de düzeltir ve ödeme kesintisi yinelenmez. Bazı zorluklar sürer. Müşteriler üzüldüklerinde hâlâ kurucuyu arıyor, bu nedenle talebin bir kısmı bilet aracını atlıyor. Mühendisler ayrıca gözden geçirmeleri yazmanın zaman aldığından yakınıyor ve yoğun bir ayda iki gözden geçirme atlandı. Mühendislik başkanı gözden geçirmeleri kısa tutmaya, kurucudan aramaları destek adresine yönlendirmesini istemeye ve bir çeyrek daha veri topladıktan sonra daha kapsamlı bir ITIL tarzı sürece ihtiyaç olup olmadığını yeniden ele almaya karar verir.

## Dört bakış açısı

### Ürün ve teslimat ekipleri

Kendi geliştirdiklerini işleten teslimat ekipleri zaten ITSM yapıyordur. Hizmetlerinizi adlandırın, olayları ve değişiklikleri hafif biçimde kaydedin ve verileri hizmetlerinizi destekleyen herkesle paylaşın. Hizmet masasını, kullanıcıların nerede zorlandığına dair bir kanıt kaynağı olarak görün.

### Hizmet ve operasyon ekipleri

ITSM uygulamasının çoğunu operasyon ve hizmet masası personeli taşır. Çevik fikirler, işinizi görünür kılarak, kullanıcılarla geri bildirim döngülerini kısaltarak ve iyileştirmeyi yıllık projelerden küçük düzenli değişikliklere kaydırarak yardımcı olabilir. Meslektaşlarınızın kuralı makul biçimde uyarlayabilmesi için her ITSM kuralının ardındaki amacı açıklayın.

### Liderlik ve yönetişim

Liderler ne kadar yapı isteneceğine ve ne kadar kanıt talep edileceğine karar verir. Müşterilerin hissettiği sonuçları ve ekiplerin araçlarından üretebileceği birkaç ölçümü isteyin. Bir çerçeve satın almayı bir işaret olarak görmeye karşı dikkatli olun; Wikipedia maddesi birçoğunu sıralar ve hiçbiri kendi hizmetlerinizi bilmenin yerini tutmaz.

### Müşteriler ve kullanıcılar

Müşteriler ve kullanıcılar ITSM'nin var olma nedenidir. Yardım istemek için net bir yol, ne bekleneceğine dair dürüst bilgi ve her hizmetin bir sahibi olmasını bekleyin. Karşılığında, bir şey ters gittiğinde sağlayıcının ondan öğrenebilmesi için zamanında ve ayrıntılı bilgi verin.

## Yaygın başarısızlık biçimleri

- **Kendi iyiliği için süreç.** Formlar ve onaylar çoğalır ve kimse nedenini hatırlamaz. Bunun yerine her uygulamayı bir amaca bağlayın ve artık bir amaca hizmet etmeyenleri silin.
- **Tek ön kapının olmaması.** Kullanıcılar tanıdıkları kişiye gider ve talep görünmez kalır. Bunun yerine tek bir kolay yol sunun ve gayriresmî talepleri o yola yakalayın.
- **Olayları, talepleri ve sorunları karıştırmak.** Raporlar yanıltır ve nedenler gizli kalır. Bunun yerine basit tanımlar kullanın ve biletleri tutarlı biçimde sınıflandırın.
- **Hizmetlerin teknolojiyle tanımlanması.** Kullanıcılar ihtiyaç duyduklarını bulamaz ve sahipler belirsizdir. Bunun yerine hizmetleri müşteri terimleriyle tanımlayın ve her birine bir sahip atayın.
- **Bir çerçeveyi toptan benimsemek.** Ekipler büyük bir çerçeveyi kopyalar ve süreçlere gömülür. Bunun yerine sorunla başlayın ve yalnızca yardımcı olan kısımları alın.
- **Kullanıcıları yok saymak.** Sağlayıcı yalnızca ödeyen müşteriyle konuşur. Bunun yerine hem müşterileri hem kullanıcıları dinleyin ve çatışmaları arayın.
- **Etkinliği ölçmek.** Bilet ve arama sayıları, hizmet kalitesinin kanıtının yerini alır. Bunun yerine erişilebilirliği, hizmeti geri getirme süresini ve kullanıcı memnuniyetini ölçün.
- **ITSM'yi teslimattan ayrı görmek.** Teslimat ekipleri yayına alır ve operasyonun başa çıkmasını bekler. Bunun yerine ikisini ortak hizmetler, ortak veriler ve ortak gözden geçirmelerle bağlayın (bkz. Konu 5.1 — Çevik Hizmet Yönetimi).

## Olgunluk modeli

| Boyut | Başlangıç | Gelişim | Standartlaştırma | Yönetim | Eşgüdüm |
|---|---|---|---|---|---|
| Hizmet tanımı | Hizmetler teknolojiyle tanımlanır ya da hiç tanımlanmaz | Bazı hizmetler sahipleriyle listelenir | Tüm hizmetler müşteri terimleriyle ve adlandırılmış sahiplerle tanımlanır | Hizmet tanımları kullanım ve geri bildirimle karşılaştırılarak denetlenir | Hizmet tanımları müşteriler ve tedarikçilerle paylaşılır ve birlikte ayarlanır |
| Destek ve talepler | Yardım gayriresmî yollarla istenir | Bazı ekiplerin bilet aracı veya paylaşılan gelen kutusu vardır | Olaylar ve talepler için net türleri olan tek bir ön kapı | Talep ve çözüm süreleri izlenir ve gözden geçirilir | Destek, ekipler ve tedarikçiler arasında ortak verilerle eşgüdümlenir |
| Kayıtlar ve ölçümler | Az kayıt tutulur | Bazı ekipler olayları ve değişiklikleri kaydeder | Kayıtlar tutarlıdır ve her birinin belirtilmiş bir amacı vardır | Müşteriye dönük ölçümler düzenli gözden geçirilir | Ölçümler hizmetler arasında paylaşılır ve öncelikleri birlikte belirlemek için kullanılır |
| İyileştirme | Düzeltmeler krizleri izler | Bazı ekipler olayları gözden geçirir | Olay ve talep verilerinin düzenli gözden geçirilmesi planlı değişikliklere yol açar | İyileştirme çalışmasına kaynak ayrılır ve sonuçları denetlenir | İyileştirme ekipler arasında ve müşterilerle rutindir |

## Kontrol listesi

- [ ] Hizmetlerimizin müşteri dilinde bir listesi var.
- [ ] Her hizmetin adlandırılmış bir sahibi var.
- [ ] Her hizmet için müşterilerin ve kullanıcıların kim olduğunu biliyoruz.
- [ ] Kullanıcıların yardım ve talepler için tek bir net ön kapısı var.
- [ ] Olaylar, talepler ve sorunlar farklı şeyler olarak kaydediliyor.
- [ ] Her kayıt türünün belirtilmiş bir amacı var ve kullanılmayan alanlar kaldırılmış.
- [ ] Erişilebilirlik veya hizmeti geri getirme süresi gibi müşterilerin hissettiği en az bir şeyi ölçüyoruz.
- [ ] Olay ve talep verilerini düzenli olarak gözden geçiriyor ve bunlara göre harekete geçiyoruz.
- [ ] Hangi çerçeve fikirlerini kullandığımızı ve hangilerini dışarıda bıraktığımızı söyleyebiliyoruz.
- [ ] Güvenle otomatikleştirilebilecek rutin görevler belirlendi.

## Yapay zeka istemleri

**Amaç: hizmetlerinizin müşteri dilinde bir listesini taslak olarak hazırlamak.**

```text
Help me describe the services my team provides in the words our users would use.

Who we are and what we run: [describe the team and its main systems in a few sentences].
Who uses what: [list user groups and what each group does with our systems].
What we currently call our services: [paste a list, or write "none"].

Produce a draft list of 5 to 10 services, each with a one-sentence description from the user's point of view, the customer or user groups, and a suggested owner role. Mark each item that is a guess. Do not invent systems I did not mention. Ask clarifying questions first if information is missing, and list what you are unsure of.
```

**Amaç: yakın zamandaki biletleri olay, talep ve sorun olarak sınıflandırmak.**

```text
Here are [number] recent tickets or messages to our team: [paste short, anonymized descriptions, one per line].

Definitions to use: an incident is an unplanned disruption or potential disruption to a service; a service request is a routine request for something the service normally provides; a problem is the underlying cause of one or more incidents.

Classify each item as incident, request, or possible problem, with one sentence of reasoning that uses only what I wrote. List items you could not classify and the question I should ask to decide. At the end, tell me the share in each category from my list only. Do not invent details, and list what you are unsure of.
```

**Amaç: durumunuz için küçük bir ilk ITSM uygulamaları kümesi seçmek.**

```text
Help me choose a first set of IT service management practices for a team in this situation.

Team size and type: [describe].
Our biggest pains (with a recent example for each): [list].
Existing tools and records: [list, or write "none"].
Rules we must follow (audit, security, contracts), with source text if you have it: [paste, or write "none known"].

From these practices: service desk, incident management, problem management, change enablement, service request management, service level management, service catalog management, knowledge management, continual improvement, propose the two or three to start with and say why, using only the information above. Say what you would leave for later. Mark assumptions, ask clarifying questions first, and list what you are unsure of.
```

**Amaç: bir teslimat ekibi ile hizmet masası arasındaki görüşmeye hazırlanmak.**

```text
Plan a 45-minute conversation between a delivery team and the service desk about how new changes are handed over.

Delivery team: [describe]. Service desk: [describe].
Recent example of a handover that went badly: [describe factually].
What the service desk says it needs: [list, or write "unknown"].

Produce an agenda, five questions for each side, and a closing step that records one agreed change with an owner. Keep it free of any particular tool. Ask clarifying questions first if information is missing, mark assumptions, and list what you are unsure of.
```

## Yapay zeka becerileri

- [service-catalog](../../../../skills/service-catalog/SKILL.md): müşteri dilinde, sahipleri ve açıklamalarıyla bir hizmet listesi taslağı hazırlamak veya gözden geçirmek için kullanın.
- [service-level-agreement](../../../../skills/service-level-agreement/SKILL.md): müşterilerle ne düzeyde hizmet bekleneceği konusunda anlaşmaya hazır olduğunuzda kullanın.
- [incident-response-plan](../../../../skills/incident-response-plan/SKILL.md): ekibinizin bir olayı, o gerçekleşmeden önce nasıl ele alacağını hazırlamak için kullanın.
- [demand-analysis](../../../../skills/demand-analysis/SKILL.md): ne tür taleplerin ve olayların hangi hacimde geldiğini anlamak için kullanın.
- [raci-matrix](../../../../skills/raci-matrix/SKILL.md): her hizmetin sahibinin kim olduğunu ve kime danışıldığını veya kimin bilgilendirildiğini netleştirmek için kullanın.

## Temel kaynaklar

- **IT service management** (Wikipedia): ilgili çerçevelerin ve standartların listesini içeren kısa bir tanım; harita olarak yararlıdır.
- **ITIL** (Wikipedia): en bilinen ITSM çerçevesinin tarihi ve sürümleri, sahiplik değişiklikleri dâhil.
- **ISO/IEC 20000** (Wikipedia): hizmet yönetim sistemleri için uluslararası standartla ilgili arka plan.
- **Enterprise service management** (Wikipedia): ITSM fikirlerini BT'nin ötesinde uygulamaya giriş.

## Kaynakça

1. IT service management — Wikipedia — https://en.wikipedia.org/wiki/IT_service_management
2. ITIL — Wikipedia — https://en.wikipedia.org/wiki/ITIL
3. ISO/IEC 20000 — Wikipedia — https://en.wikipedia.org/wiki/ISO/IEC_20000
4. COBIT — Wikipedia — https://en.wikipedia.org/wiki/COBIT
5. FitSM — Wikipedia — https://en.wikipedia.org/wiki/FitSM
6. CMMI — Wikipedia — https://en.wikipedia.org/wiki/CMMI
7. TOGAF — Wikipedia — https://en.wikipedia.org/wiki/TOGAF
8. Microsoft Operations Framework — Wikipedia — https://en.wikipedia.org/wiki/Microsoft_Operations_Framework
9. Application Services Library — Wikipedia — https://en.wikipedia.org/wiki/Application_Services_Library
10. Business Information Services Library — Wikipedia — https://en.wikipedia.org/wiki/Business_Information_Services_Library
11. Enterprise service management — Wikipedia — https://en.wikipedia.org/wiki/Enterprise_service_management
12. IT asset management — Wikipedia — https://en.wikipedia.org/wiki/IT_asset_management
