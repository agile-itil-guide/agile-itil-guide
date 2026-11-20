# Metrikler ve Ölçüm

**İyi ölçüm, bir ekibin çalışmasının kullanıcılara yardımcı olup olmadığını ve iyileşip iyileşmediğini görmesini sağlar; herhangi bir ölçümü kullanmanın en güvenli yolu onu bir hedef olarak değil, tartışılacak bir soru olarak kullanmaktır.**

## Bu neden önemli

Ekiplerin yön vermek için sayılara ihtiyacı vardır. Sayılar olmadan kararlar hafızaya, yüksek sesli kişilere ve en son konuşana dayanır. Yanlış sayılarla kararlar hiç sayı olmamasından da kötü olabilir: kapattığı bilet sayısını sayan bir ekip, kullanıcıların sorunları çözülsün ya da çözülmesin biletleri hızla kapatmayı öğrenir. Ölçüm güçlüdür ve tasarımcılarının her zaman öngörmediği biçimlerde davranışı değiştirir.

Bu rehber şimdiye kadar birçok ölçüm kullandı: DORA'nın yazılım teslimat ölçümleri (bkz. Konu 3.4 — Değişiklik Sağlama), Kanban Guide'ın dört akış ölçümü (bkz. Konu 1.5 — Kanban), hizmet seviyesi göstergeleri ve hedefleri (bkz. Konu 3.7 — Hizmet Seviyesi Yönetimi) ve çağrı cihazı yükü (bkz. Konu 3.10 — İzleme ve Etkinlik Yönetimi). Bu konu hepsini bir araya getirir, hedefler ve anahtar sonuçlarla hedef belirlemeyi ve müşteri memnuniyeti ölçümlerini ekler ve alandaki en eski uyarıyla, Goodhart yasasıyla karşılaştırır.

[Goodhart yasası hakkındaki Wikipedia maddesi](https://en.wikipedia.org/wiki/Goodhart%27s_law) özdeyişi olağan biçimiyle verir: "When a measure becomes a target, it ceases to be a good measure" (Bir ölçüm hedef haline geldiğinde iyi bir ölçüm olmaktan çıkar). Bunu, Birleşik Krallık para politikası üzerine 1975 tarihli bir makalede gözlenen her istatistiksel düzenliliğin, kontrol amacıyla üzerine baskı uygulandığında çökme eğiliminde olduğunu yazan İngiliz iktisatçı Charles Goodhart'a atfeder. Olağan ifade daha sonraki bir tarihtendir; madde bunu Keith Hoskin'e (1996) ve Marilyn Strathern'in 1997 tarihli makalesine atfeder. Bu görüşün farklı alanlarda uzun bir geçmişi vardır ve bu konu için doğru başlangıç noktasıdır.

## Temel kavramlar

### Ölçümler, hedefler ve Goodhart yasası

Bir **ölçüm** bir şeyi tanımlar. Bir **hedef**, birinin tutturması beklenen bir sayıdır. Sorun, birinden diğerine geçişte başlar. İnsanlar bir sayı için ödüllendirildiğinde veya cezalandırıldığında, sayıyı, tanımladığı şeyi iyileştirmekle aynı olmayan yollarla hareket ettirmenin yollarını bulur. Madde para politikasından, okul sistemlerinden ve sağlık hizmetlerinden örnekler verir. Bir hizmet kuruluşunda kolay örnekler şunlardır: biletler erken kapatıldığı için bilet kapatma süresinin düşmesi, değişiklikler bölündüğü için dağıtım sayısının artması ve kesintiler yeniden sınıflandırıldığı için erişilebilirliğin artmış görünmesi.

Çare ölçmekten kaçınmak değil, dikkatle ölçmektir:

- Hız ve kalite gibi birbirine karşı çeken birkaç ölçüm kullanın.
- Sayıları, çalışmasını anlattıkları kişilerle tartışın.
- Bireysel ödülleri veya disiplini tek bir sayıya bağlamayın.
- Ölçümler bilgilendirici olmaktan çıktığında değiştirin.

### Ölçüm türleri

| Tür | Yanıtladığı soru | Örnekler |
|---|---|---|
| **Sonuç** | Kullanıcılar ve iş daha iyi durumda mı? | Kullanıcı memnuniyeti, görev başarısı, gelir, kullanıcılara zarar veren olaylar |
| **Akış** | İş ne kadar iyi akıyor? | Çevrim süresi (cycle time), verim (throughput), iş kalemi yaşı, devam eden iş |
| **Teslimat performansı** | Değişiklikler üretime ne kadar iyi ulaşıyor? | Değişiklik teslim süresi, dağıtım sıklığı, değişiklik başarısızlık oranı, kurtarma süresi |
| **Hizmet seviyesi** | Hizmet kullanıcıların ihtiyaçlarını karşılıyor mu? | Hedeflere göre erişilebilirlik, gecikme, hata oranı |
| **Sağlık ve sürdürülebilirlik** | Bu böyle sürebilir mi? | Çağrı cihazı yükü, angarya (toil), fazla mesai, personel duyarlılığı |
| **Maliyet** | Değer birimi başına maliyeti nedir? | İşlem başına veya kullanıcı başına maliyet |

Dengeli bir küme birçok satırdan seçer; böylece birini iyileştirmek diğerinin pahasına olmaz.

### DORA ölçümleri

DORA'nın yazılım teslimat performansı ölçümleri değişiklik teslim süresi, dağıtım sıklığı, başarısız dağıtımdan kurtarma süresi, değişiklik başarısızlık oranı ve dağıtım yeniden iş oranıdır. DORA'nın ölçümler üzerine rehberi, ölçümler çoğu ekip için ilişkili olduğundan hız ile istikrarın bir ödünleşim olmadığını söyler. Bunları hedef olarak belirlemeye, tek birine dayanmaya, çok farklı uygulamaları karşılaştırmaya ve diğer ekiplerle rekabete karşı uyarır ve kişinin kendi geçmiş performansına göre iyileşmesini önerir. DevOps hakkındaki Wikipedia maddesi, bazı uzmanların DORA araştırma yöntemini ve ölçümlerini eleştirdiğini ekler; bu nedenle bunları sınırları olan yararlı sorular olarak ele alın (bkz. Konu 5.2 — DevOps).

### Akış ölçümleri

Kanban Guide dört ölçümü tanımlar: devam eden iş, verim, iş kalemi yaşı ve çevrim süresi. Ekiplerin bunları yeniden adlandırabileceğini ve gerektiğinde başkalarını ekleyeceğini belirtir ve ölçümlerin yalnızca iş akışını tanımlama, içindeki kalemleri yönetme ve iyileştirme uygulamalarını bilgilendirdiklerinde önemli olduğunu söyler. İş kalemi yaşı özellikle yararlıdır çünkü sorunu hâlâ harekete geçmek için zaman varken gösterir (bkz. Konu 5.4 — Değer Akışı Yönetimi).

### Hizmet seviyesi ölçümleri

Hizmet seviyesi göstergeleri ve hedefleri (bkz. Konu 3.7 — Hizmet Seviyesi Yönetimi) kullanıcıların ne yaşadığına dair en doğrudan görünümü verir. SRE kitabı, kullanıcıların önemsediği şeylerden seçilmiş birkaç gösterge için, yalnızca ortalamalar değil yüzdelikler (percentile) için ve mükemmellik olmayan hedefler için görüş bildirir. Hata bütçeleri aradaki farkı ortak bir karar kuralına dönüştürür (bkz. Konu 5.3 — Site Reliability Engineering).

### Hedefler ve anahtar sonuçlar

**Hedefler ve anahtar sonuçlar (OKR)** bir hedef belirleme çerçevesidir. Wikipedia maddesi bir OKR'yi, önemli, somut ve net tanımlanmış bir hedef olan bir amaç (objective) ile ölçülebilir başarı ölçütleri olan üç ila beş anahtar sonucun eşleşmesi olarak tanımlar. Yaklaşımı 1970'lerde Intel'de yaygınlaştırıp *High Output Management* (1983) kitabında belgeleyen kişi olarak Andrew Grove'u, 1999'da Google'a getiren kişi olarak John Doerr'ı gösterir. Madde, OKR'lerin 0,0 ile 1,0 arasında puanlandığını, iddialı anahtar sonuçların yaklaşık 0,7'yi hedeflediğini ve Doerr'ın yaklaşık yüzde 70'lik bir başarı oranı hedefi önerdiğini, dolayısıyla hep karşılanan bir anahtar sonucun yeniden değerlendirilmesi gerektiğini söyler. Her zamanki işi sürdürmeye yönelik amaçlardan kaçınmayı ve geriden gelen göstergeler yerine öncü göstergeleri tercih etmeyi önerir.

Madde eleştirileri de kaydeder: çoğu kuruluş bireysel katkıcı OKR'lerini belirlemeyi bırakmıştır; bunlar görev listelerine benzeme ve performans değerlendirmelerine karışma eğilimindedir ve çok katmanlı OKR'ler şelale yaklaşımı yaratabilir. Etkinliğe dair bağımsız kanıt sunmaz ve konuya yakın kaynaklara dayanmaya ilişkin bir bakım etiketi taşır. Hizmet ekipleri için OKR'ler, bireysel hedeflere dönüştürülmedikleri sürece sonuçları (örneğin "kullanıcılar kaydı yardım almadan tamamlar") ölçülebilir anahtar sonuçlara bağlayabilir.

### Müşteri memnuniyeti

Kullanıcıların ne düşündüğünü ölçmek iyi yapılması zor bir iştir. Yaygın bir araç **net tavsiye skoru (NPS)** olarak bilinir. Wikipedia'ya göre bu skor, yanıtlayanların bir şirketi, ürünü veya hizmeti tavsiye etme olasılığına dair tek bir soruya dayanır; destekçiler 9 veya 10, tarafsızlar 7 veya 8, eleştirenler 6 veya daha düşük puan verir; skor, destekçilerin yüzdesinden eleştirenlerin yüzdesinin çıkarılmasıyla bulunur. Bain & Company'den Fred Reichheld bunu 2003 tarihli bir *Harvard Business Review* makalesiyle yaygınlaştırmıştır. Madde sınırları kaydeder: akademisyenler şirket büyümesini güvenilir biçimde öngörüp öngörmediğini sorgular, tek bir madde çok sayıda yanıt gerektirir, belirli sorunlar hakkında az şey söyler, aşırı anket şikâyet çeker ve maaşa bağlamak davranışı bozabilir; bu yüzden Reichheld ikisinin ayrılmasını önermiştir. Müşteri memnuniyeti skorları ve müşteri çaba skorları gibi başka araçlar da vardır, ancak madde bunları ele almaz.

Hangi araç olursa olsun, kısa bir soru sorun, her zaman serbest metinli yanıta izin verin, yorumları okuyun ve öğrendiklerinizin ardını izleyin.

### İnsanları ve sürdürülebilirliği ölçmek

Çağrı cihazı yükü, angarya, fazla mesai ve duyarlılık gibi personel yükü ve sağlığı ölçümleri, hizmetin sürdürülebilirliğinin ölçümleridir (bkz. Konu 5.3 — Site Reliability Engineering). Bunları bireylerin performansının ölçümleri olarak değil, sistem hakkında bilgi olarak ele alın.

### Yapay zekayı ve otomasyonu ölçmek

Otomatik veya yapay zeka destekli bir adım getirildiğinde, kalitesine ilişkin ölçümler ekleyin: insanların onu ne sıklıkla geçersiz kıldığı, ne sıklıkla yanlış olduğu ve neye mal olduğu (bkz. Konu 6.2 — BT Hizmet Yönetiminde Yapay Zeka).

### Sınırlar

Ölçümler kısmidir. Güven, ustalık ve yargı gibi saymanın zor olduğu şeyleri dışarıda bırakır. Veriler eksik olduğunda veya tanımlar ekipler arasında farklı olduğunda yanıltabilir. Burada okunan maddeler, ölçüm programlarının sonuçları iyileştirip iyileştirmediğine dair çok az görgül kanıt sunar. Her programı bir deney olarak ele alın ve gözden geçirin.

## İyi uygulamalar

1. **Soruyla başlayın.** Bir ölçümün hangi kararı bilgilendireceğini ve kimin buna göre harekete geçeceğini sorun. Kimse geçmeyecekse toplamayın.
2. **Küçük ve dengeli bir küme seçin.** Sonuç, akış, teslimat, hizmet seviyesi ve sağlık alanlarından birkaç ölçüm seçin. Bazılarının birbirine karşı çektiğinden emin olun.
3. **Her ölçümü kesin biçimde tanımlayın.** Neyin, nereden sayıldığını ve neyin hariç tutulduğunu yazın. Aynı sözcüğü farklı şeyler için kullanan iki ekip, karşılaştırılamayan sayılar üretir.
4. **Hizmet veya ekip başına ölçün ve kendi geçmişiyle karşılaştırın.** Ekipleri sıralamaktan kaçının. DORA, kişinin kendi geçmiş performansına göre iyileşmesini ve farklı uygulamaları karşılaştırırken dikkatli olmayı önerir.
5. **Tek bir sayıyı hedef yapmayın.** Ölçümleri tartışma başlatıcısı olarak kullanın ve hedefleri sonuç olarak belirleyin. Bir ölçüm hedef olduğunda oyunlaştırmaya dikkat edin (bkz. Goodhart yasası).
6. **Sayıları hikâyelerle eşleştirin.** Her eğilim için birkaç gerçek vakaya bakın. Sayılar nereye bakacağınızı söyler; vakalar nedenini söyler.
7. **Dağılımlara bakın.** Süre ve boyut ölçümleri için yalnızca ortalamaları değil, yüzdelikleri ve aralıkları kullanın.
8. **Mümkün olduğunda öncü göstergeleri tercih edin.** İş kalemi yaşı gibi ölçümler, geçmiş sonuç ölçümlerinden farklı olarak sorunu gerçekleşmeden önce gösterir.
9. **Hedefleri ve anahtar sonuçları dikkatle kullanın.** OKR kullanıyorsanız bunları ekip ve kurum düzeyinde tutun, her zamanki işi sürdürmeye yönelik amaçlardan kaçının ve hep karşılanan bir sonucu daha yükseğe hedeflemek için bir işaret sayın.
10. **Kullanıcılara kısa ve sık sorun.** Serbest metinli kısa bir soru kullanın, yorumları okuyun ve yanıt verin. Anket skorlarını bireysel maaşa bağlamayın.
11. **Ölçmenin maliyetine dikkat edin.** Araçların işin yan ürünü olarak ürettiği verileri tercih edin. Kimsenin kullanmadığı elle raporlamayı bırakın.
12. **Ölçümlerin kendisini gözden geçirin.** Yılda bir veya iki kez hangi ölçümlerin karara yol açtığını ve hangilerinin açmadığını sorun, ikincileri emekliye ayırın.

## Ekibinizle tartışılacak sorular

**Ölçümlerimizden hangisi son altı ayda bir karara yol açtı?**

Ölçümleri listeleyin ve her biriyle bağlantılı bir karar isteyin. Bağlantısı olmayan ölçümler kaldırma adayıdır. Kolaylaştırıcı insanların en az hangi ölçüme güvendiğini ve nedenini sorabilir. Birini kaldırın veya düzeltin.

**Bir sayı hedef olduğunda davranışımıza ne oluyor?**

Bir sayının hedef olduğu yakın tarihli bir örnek isteyin. İnsanların ona ulaşmak için ne yaptığını irdeleyin. Çerçeve Goodhart özdeyişidir. Daha iyi bir ölçümün veya ölçüm eşleşmesinin nasıl görüneceğini sorun. Tek bir değişiklik üzerinde anlaşın.

**Hızı ve kaliteyi birlikte ölçüyor muyuz?**

Hız ölçümlerini ve kalite ölçümlerini listeleyin. Listeler dengesizse etkisini tartışın. Örneğin, tekrarlayan temaslar olmadan bilet kapatma süresini ölçmek erken kapatmayı teşvik eder. Bir eşleşme seçin.

**Kullanıcılar bize işlerin nasıl gittiğini söylüyor mu ve onlara nasıl soruyoruz?**

Kullanıcılara sorduğunuz sorulara ve ne sıklıkla sorduğunuza bakın. Serbest metinli yanıtlardan bazılarını yüksek sesle okuyun. Bunlar yüzünden neyin değiştiğini sorun. Denemek için kısa bir soru üzerinde anlaşın.

**Ölçümlerimizden hangileri bireyleri yargılamak için kullanılabilir ve bu konuda ne yapmalıyız?**

İnsanların korkabileceği ölçümleri belirleyin. Riskleri tartışın ve sayıların neler için kullanılmayacağına dair açık kurallar üzerinde anlaşın. Bunları yazın.

**Yalnızca beş ölçümü koruyabilecek olsak hangilerini korurduk?**

Her kişiden beş seçmesini isteyin ve karşılaştırın. Örtüşme çekirdeği, farklılıklar ise farklı ihtiyaçları gösterir. Sonuç bir başlangıç kümesidir. Sonuçları, akışı, hizmet seviyelerini ve sağlığı kapsadığını kontrol edin.

## Uygulamada: çevik bir ITIL örneği

Ulusal bir demiryolu şirketinin BT grubu, yolcu bilgilendirme sistemlerini işletmektedir. Grup, her ay yönetim ekibine 40 ölçümden oluşan bir gösterge paneli sunar. Paneli az kişi okur ve tartışmaya iki ölçüm egemendir: hedef süre içinde kapatılan olay sayısı ve çeyrek başına sürüm sayısı. Olay ekibi olayları hızla kapatmayı ve aynı arıza için yenilerini yeniden açmayı öğrenmiş, birkaç teslimat ekibi de sayıyı tutturmak için işi önemsiz sürümlere bölmüştür.

BT grubunun başkanı küçük bir ekipten ölçümleri yeniden kurmasını ister. Gösterge panelinin hangi kararları bilgilendirmesi gerektiğini sorarak başlarlar. Her hizmet için bir avuç ölçüm seçerler: kullanıcıya dönük bir hizmet seviyesi göstergesi ve hedefi, değişiklik teslim süresi ve değişiklik başarısızlık oranı, açık sorun kalemleri için iş kalemi yaşı, mühendis başına çağrı cihazı yükü ve istasyon personeline yönelik, serbest metin kutulu, aylık tek soruluk bir memnuniyet anketi. Eski sayımlar emekliye ayrılır. Yönetim ekibi hiçbir ölçümün ekipleri sıralamak veya bireysel ikramiye belirlemek için kullanılmayacağı konusunda anlaşır ve BT başkanı bunu gösterge paneline bir kural olarak yazar. Ekiplerden, sahibi oldukları hizmetler için iyileştirme hedeflerini yalnızca ekip düzeyinde, anahtar sonuçlu amaçlar olarak belirlemeleri istenir.

Bir yıl sonra gösterge panelinde on iki ölçüm vardır ve aylık gözden geçirme, en eski açık sorunlar ve serbest metinli yorumlar üzerine bir sohbete dönüşmüştür. Tekrarlayan olaylar azalır ve sürümler daha anlamlı hale gelir. Bazı zorluklar sürer. Memnuniyet anketi gece personelinden az yanıt alır, bir ekibin teslim süresi kötü görünür çünkü süreyi commit'ten değil fikirden başlatarak sayan tek ekiptir ve bir yönetici anket skorunu bir performans değerlendirmesinde anmaya başlamıştır. BT başkanı ekipten tanımları hizalamasını ister, yöneticilere kuralı hatırlatır ve gece vardiyası devrinde yürütülecek kısa bir anket düzenler.

## Dört bakış açısı

### Ürün ve teslimat ekipleri

Teslimat ekipleri yön vermelerine yardımcı olan ölçümleri seçmeli, sayıları araçlarından almalı ve retrospektiflerde tartışmalıdır. İşi bölmeyi veya başarısızlıkları gizlemeyi ödüllendiren ölçümlere dikkat edin. Öğrendiklerinizi diğer ekiplerle paylaşın.

### Hizmet ve operasyon ekipleri

Operasyon ekipleri hizmet seviyesi ve sağlık ölçümlerinin çoğunu taşır. Tanımları net ve verileri güvenilir tutun, çağrı cihazı yükünü ve angaryayı dahil edin ve sayıları vakalar ve yorumlarla sunun. Bir ölçüm hedef olarak kullanıldığında karşı çıkın.

### Liderlik ve yönetişim

Liderler ölçüm kültürünü şekillendirir. Sayıların neler için kullanılıp kullanılmayacağını söyleyin, sıralama tabloları değil eğilimler ve hikâyeler isteyin ve her yeni kaygı için ölçüm eklemeye direnin. Tüm kümeyi zaman zaman gözden geçirin.

### Müşteriler ve kullanıcılar

Müşteriler ve kullanıcılar hem ölçümlerin kaynağı hem de konusudur. Mümkün olduğunda kısa anketlere yanıt verin ve neyin önemli olduğunu söyleyin. Sağlayıcılara deneyiminiz hakkında neyi ölçtüklerini ve sonuçlarla ne yaptıklarını sorun.

## Yaygın başarısızlık biçimleri

- **Hedef olarak ölçümler.** Oyunlaştırma izler. Bunun yerine ölçümleri tartışma için kullanın ve hedefleri sonuç olarak belirleyin.
- **Tek sayı.** Tek bir ölçüm davranışı çarpıtır. Bunun yerine kendi içinde birbirine karşı çeken dengeli bir küme kullanın.
- **Tutarsız tanımlar.** Ekipler farklı sayar. Bunun yerine her ölçümü ve kaynağını tanımlayın.
- **Sıralama tabloları.** Ekipler rekabet eder ve sorunları gizler. Bunun yerine her ekibi kendi geçmişiyle karşılaştırın.
- **Yalnızca ortalamalar.** Uzun kuyruklar gizlenir. Bunun yerine dağılımlara ve yüzdeliklere bakın.
- **Kolay olanı ölçmek.** Elverişli sayılar önemli olanların yerini alır. Bunun yerine kararlardan ve kullanıcıların sonuçlarından başlayın.
- **Görev listesi olarak bireysel OKR'ler.** Hedefler performans değerlendirmelerine dönüşür. Bunun yerine OKR'leri ekip ve kurum düzeyinde tutun.
- **Anket yorgunluğu ve maaş bağlantıları.** Kullanıcılar yanıtlamayı bırakır veya skorlar manipüle edilir. Bunun yerine anketleri kısa tutun ve maaştan ayırın.

## Olgunluk modeli

| Boyut | Başlangıç | Gelişim | Standartlaştırma | Yönetim | Eşgüdüm |
|---|---|---|---|---|---|
| Seçim ve tanım | Ölçümler geçici (ad hoc) | Bazı ekipler birkaç ölçüm tanımlar | Hizmet başına net tanımlı dengeli bir küme kullanılır | Küme yararlılık ve boşluklar açısından gözden geçirilir | Ölçümler ekipler, tedarikçiler ve müşteriler arasında hizalanır |
| Kararlarda kullanım | Sayılar raporlanır ama nadiren kullanılır | Bazı ekipler bunları gözden geçirmelerde tartışır | Ölçümler düzenli kararları ve iyileştirmeyi besler | Ölçümlere bağlı kararlar izlenir ve onlardan öğrenilir | Ölçümler kurum genelinde kararlara yön verir |
| Oyunlaştırmaya karşı korunma | Hedefler tek sayılara konur | Çarpıtmaya dair bir miktar farkındalık vardır | Ölçümlerin nasıl kullanılabileceğine dair kurallar yazılıdır ve izlenir | Oyunlaştırma işaretleri izlenir ve ölçümler ayarlanır | Ölçüm kültürü kurum genelinde paylaşılır |
| Kullanıcı ve sağlık ölçümleri | Az kullanıcı veya personel verisi vardır | Bazı anketler veya yük verileri vardır | Kısa kullanıcı anketleri ve sürdürülebilirlik ölçümleri rutindir | Sonuçlar planlı eyleme yol açar ve kontrol edilir | Kullanıcı ve personel sesleri hizmetler genelinde öncelikleri şekillendirir |

## Kontrol listesi

- [ ] Raporladığımız her ölçümün bilgilendirdiği belirtilmiş bir karar var.
- [ ] Sonuç, akış, hizmet seviyesi, teslimat ve sağlık ölçümlerini içeren küçük ve dengeli bir küme kullanıyoruz.
- [ ] Her ölçümün yazılı bir tanımı ve kaynağı var.
- [ ] Ekipler sıralanmıyor, kendi geçmişleriyle karşılaştırılıyor.
- [ ] Ölçümlerin neler için kullanılmayacağını yazdık.
- [ ] Süre ölçümleri dağılımları veya yüzdelikleri gösteriyor.
- [ ] Kullanıcılara düzenli olarak yorum alanı olan kısa bir soru soruluyor ve yanıtlar okunuyor.
- [ ] OKR kullanıyorsak bunlar ekip veya kurum düzeyinde ve bireysel hedef değil.
- [ ] Veriler mümkün olduğunda işin yan ürünü olarak araçlardan alınıyor.
- [ ] Ölçümlerin kendisini en az yılda bir gözden geçiriyoruz.

## Yapay zeka istemleri

**Amaç: bir hizmet için dengeli bir ölçüm kümesi seçmek.**

```text
Help me choose a small balanced set of measures for [service].

What the service does and who uses it: [describe].
Decisions the team and its owner need to make in the next quarter: [list].
Data we already have: [list tools and records].
Measures we currently report: [list].

Propose five to eight measures across outcome, flow, delivery performance, service level, and health (for example work item age, change lead time, an availability indicator, pager load, and a short satisfaction question). For each, say what decision it informs, what data it needs, and one way it could be gamed. Do not set targets. Ask clarifying questions first, mark assumptions, and list what you are unsure of.
```

**Amaç: bir ölçümün nasıl oyunlaştırılabileceğini bulmak.**

```text
Here is a measure we use and how it is used: [describe the measure, its definition, and who sees it or is rewarded for it].

List ways people might change their behavior to improve the number without improving the underlying work, using only the description. Suggest a paired measure that would reveal each distortion and a question to ask the team. Do not accuse anyone. List what you are unsure of.
```

**Amaç: bir hizmet ekibi için OKR'leri görev listesine dönüştürmeden yazmak.**

```text
Help me draft OKRs for [team] for the next quarter.

Context: [describe the service and the main problem users face].
Outcomes we want for users: [list].
Measures we already collect: [list].
Risks we have seen with goals in the past: [for example, gaming or task lists].

Draft two or three objectives, each with three to five key results that are measurable outcomes (not tasks), using only measures we can collect, and leave target values as [to be agreed with the team]. For each key result, name the data source and a possible distortion. Do not set individual OKRs. Ask clarifying questions first, and list what you are unsure of.
```

**Amaç: serbest metinli anket yorumlarını analiz etmek.**

```text
Here are free-text comments from our latest user survey: [paste anonymized comments].

Group the comments into themes based only on what they say. For each theme, give a name, the number of comments from my list, two short example quotes, and a question for the team. Highlight themes that appear in both positive and negative comments. Do not infer demographics or sentiment beyond the text. If the sample is small, say so. List what you are unsure of.
```

## Yapay zeka becerileri

- [software-engineering-metrics](../../../../skills/software-engineering-metrics/SKILL.md): teslimat ve hizmet performansı ölçümlerini seçmek ve yorumlamak için kullanın.
- [key-risk-indicators](../../../../skills/key-risk-indicators/SKILL.md): bir hizmetin riskleri için erken uyarı ölçümlerini seçmek için kullanın.
- [survey-design](../../../../skills/survey-design/SKILL.md): kullanılabilir yanıtlar üreten kısa kullanıcı ve personel anketleri tasarlamak için kullanın.
- [getting-feedback](../../../../skills/getting-feedback/SKILL.md): kullanıcılardan ve meslektaşlardan geri bildirim toplamak ve yanıtlamak için kullanın.
- [feature-prioritization](../../../../skills/feature-prioritization/SKILL.md): sonuç ölçümlerini ekibin sırada üzerinde çalışacağı işe bağlamak için kullanın.

## Temel kaynaklar

- **DORA's software delivery performance metrics** (dora.dev): beş ölçümün tanımları ve kullanımlarına dair uyarılar.
- **Goodhart's law** (Wikipedia): hedef olarak kullanılan bir ölçümün iyi bir ölçüm olmaktan çıktığını söyleyen özdeyişin kökeni ve ifadesi.
- **Objectives and key results** (Wikipedia): çerçeve, kökenleri, puanlama ve eleştiriler.
- **Net promoter score** (Wikipedia): bir memnuniyet ölçümünün tanımı, kullanımları ve eleştirileri.

## Kaynakça

1. DORA's software delivery performance metrics — DORA, dora.dev — https://dora.dev/guides/dora-metrics-four-keys/
2. Goodhart's law — Wikipedia — https://en.wikipedia.org/wiki/Goodhart%27s_law
3. Objectives and key results — Wikipedia — https://en.wikipedia.org/wiki/Objectives_and_key_results
4. Net promoter score — Wikipedia — https://en.wikipedia.org/wiki/Net_promoter_score
5. The Kanban Guide — John Coleman, Daniel Vacanti, and contributors, kanbanguides.org — https://kanbanguides.org/english/
6. Service Level Objectives — Google SRE book, sre.google — https://sre.google/sre-book/service-level-objectives/
7. DevOps — Wikipedia — https://en.wikipedia.org/wiki/DevOps
8. Performance indicator — Wikipedia — https://en.wikipedia.org/wiki/Performance_indicator
9. Customer satisfaction — Wikipedia — https://en.wikipedia.org/wiki/Customer_satisfaction
